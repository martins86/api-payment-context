## Comandos VSCode

```
  (Bash - Diretótio)
  > mkdir api-payment-context
  > cd api-payment-context/
  
  (Bash - Api dotnet)
  > dotnet new classlib --name Payment.Context.Domain --output Payment.Context.Domain
  > dotnet new classlib --name Payment.Context.Shared --output Payment.Context.Shared
  > dotnet new mstest --name Payment.Context.Tests --output Payment.Context.Tests
  
  > dotnet new sln --name Payment.Context
  
  > dotnet sln Payment.Context.sln add Payment.Context.Domain/Payment.Context.Domain.csproj
  > dotnet sln Payment.Context.sln add Payment.Context.Shared/Payment.Context.Shared.csproj
  > dotnet sln Payment.Context.sln add Payment.Context.Tests/Payment.Context.Tests.csproj
  
  > dotnet add Payment.Context.Domain/Payment.Context.Domain.csproj reference Payment.Context.Shared/Payment.Context.Shared.csproj
  
  > dotnet add Payment.Context.Tests/Payment.Context.Tests.csproj reference Payment.Context.Domain/Payment.Context.Domain.csproj
  > dotnet add Payment.Context.Tests/Payment.Context.Tests.csproj reference Payment.Context.Shared/Payment.Context.Shared.csproj

  > dotnet restore
  > dotnet build Payment.Context.sln
  
```