# Project Setup

1. Used .NET SDK 6.0.100 on Windows 10 Pro Version 20H2 OS Build 19042.746.
2. Created `global.json` specifying SDK version `6.0.100`.
3. (Powershell 7.1.3) `dotnet new blazorwasm --name RazorForStatementSuspectedBug1 --framework net6.0 --no-https`.

# To Reproduce
1. (Powershell 7.1.3) `dotnet run --project ./RazorForStatementSuspectedBug1/`.
2. Expected output at `/` route:
```
foreach statement
Counter: 0
Counter (captured): 0
Counter: 1
Counter (captured): 1
Counter: 2
Counter (captured): 2
Counter: 3
Counter (captured): 3
for statement
Counter: 0
Counter (captured): 0
Counter: 1
Counter (captured): 1
Counter: 2
Counter (captured): 2
Counter: 3
Counter (captured): 3
```
3. Actual output:
```
foreach statement
Counter: 0
Counter (captured): 0
Counter: 1
Counter (captured): 1
Counter: 2
Counter (captured): 2
Counter: 3
Counter (captured): 3
for statement
Counter: 0
Counter (captured): 4
Counter: 1
Counter (captured): 4
Counter: 2
Counter (captured): 4
Counter: 3
Counter (captured): 4
```
