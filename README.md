# PackIssue
This repo is setup to show an issue I am encountering with dotnet pack on the 5.0.201 SDK.

## Reproduction steps
1. Set the .NET version in the `global.json` file
2. Run `dotnet pack`

Observed on 5.0.201
> "D:\Dev\PackIssue\PackIssue\PackIssue.csproj" (pack target) (2:6) ->
>       (GenerateNuspec target) ->
>          C:\Program Files\dotnet\sdk\5.0.201\Sdks\NuGet.Build.Tasks.Pack\build\NuGet.Build.Tasks.Pack.targets(221,5): error NU1012: Some included files are included under TFMs which are missing a platform version: net5.0-windows [D:\Dev\PackIssue\PackIssue\PackIssue.csproj]

You can see the verbose output in the VerboseLog.txt file as well.