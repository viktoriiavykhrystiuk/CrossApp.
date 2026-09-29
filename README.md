# CrossApp

Проєкт з крос-платформного програмування.

Предметна область: Бібліотека. Сутності: Book (видання), BookCopy (примірник), Reader (читач), Loan (видача).
Призначення: облік видач примірників книг читачам і повернень.

## Структура solution

```
CrossApp/
  CrossApp.sln
  README.md
  .gitignore
  src/
    Core/
      Core.csproj
      EnvironmentInfo.cs
    Cli/
      Cli.csproj
      Program.cs
```

## Запуск

```
dotnet build
dotnet run --project src/Cli
```

## Публікація

```
dotnet publish src/Cli -c Release -r win-x64 --self-contained true
dotnet publish src/Cli -c Release -r win-x64 --self-contained false
```

| RID     | Режим               | Розмір   | Потрібен встановлений runtime |
|---------|---------------------|----------|-------------------------------|
| win-x64 | self-contained      | 76,7 МБ  | ні                            |
| win-x64 | framework-dependent | 0,19 МБ  | так (.NET 10)                 |

## Середовище

.NET SDK 10.0.400, Windows 11 x64 (RID: win-x64)
