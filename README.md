# WinForm Designer Partial Resource Bug

This project demonstrates a bug that occurs when editing a partial control (or form) with the designer. When the partial file is edited, the designer generates a new resource file. This resource file then conflicts with the existing resource file, causing the compilation to fail with the following error:

```
Error	MSB3577	Two output file names resolved to the same output path: "obj\Debug\net8.0-windows\WinFormDesignerPartialResourceBug.Form1.resources"
```

## Steps to Reproduce

1. Clone the repo.
2. Open the file `Form1_partial.cs` with the WinForm Designer.
3. The file `Form1_partial.resx` should have been generated.
4. Try to compile the project.

## Resources

* [Linked GitHub issue](https://github.com/dotnet/winforms/issues/11411)