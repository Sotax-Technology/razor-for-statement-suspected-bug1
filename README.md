# Project Setup

1. Used .NET SDK 6.0.100 on Windows 10 Pro Version 20H2 OS Build 19042.746.
2. Created `global.json` specifying SDK version `6.0.100`.
3. (Powershell 7.1.3) `dotnet new blazorwasm --name RazorForStatementSuspectedBug1 --framework net6.0 --no-https`.

# To Reproduce
1. (Powershell 7.1.3) `dotnet run --project ./RazorForStatementSuspectedBug1/`.
