# Copilot instructions for this repository

Purpose: Give an AI coding agent the minimal, actionable context to be productive in this small C# console repository.

1) Big picture
- This repo contains a single minimal .NET console app under `probando/` that prints a message. See [probando/Program.cs](probando/Program.cs#L1-L3).
- The project file is [probando/probando.csproj](probando/probando.csproj#L1-L20). Target framework is `net10.0` and the project uses top-level statements, `ImplicitUsings` enabled and `Nullable` enabled.

2) Developer workflows (explicit commands)
- Build the project:

  dotnet build probando

- Run the project (project folder recommended):

  cd probando
  dotnet run

- There are no test projects or CI workflows in the repository; run and debug locally using the `dotnet` CLI or your IDE.

3) Project-specific patterns and conventions
- Single-file entrypoint using C# top-level statements — expect `Program.cs` to contain immediate executable code rather than a `Main` method.
- Project-level features enabled in the csproj:
  - `ImplicitUsings` means common namespaces are available without `using` directives.
  - `Nullable` is enabled; prefer null-safety-aware edits.
- `appsettings.json` exists at [probando/appsettings.json](probando/appsettings.json) but is currently empty; treat it as optional configuration for now.

4) What to change (guidance for suggested edits)
- Keep changes minimal and focused: modify `probando/` contents when altering runtime behavior.
- Avoid editing `README.md` ASCII-art unless asked — it's decorative and not authoritative for code behavior.

5) Integration points and external dependencies
- No external NuGet packages are declared; the project is self-contained.
- No CI, Docker, or other integrations found — assume local `dotnet` CLI is the canonical workflow.

6) Useful file references (quick links)
- Entrypoint: [probando/Program.cs](probando/Program.cs#L1-L3)
- Project file: [probando/probando.csproj](probando/probando.csproj#L1-L20)
- Configuration: [probando/appsettings.json](probando/appsettings.json)
- Repo README: [README.md](README.md)

7) Constraints for automated edits
- Do not introduce new frameworks or target changes (e.g., changing `TargetFramework`) without explicit confirmation — keep the project on `net10.0`.
- Because there are no tests, add unit tests only if requested and include a test project and a simple `dotnet test` workflow.

If any section is unclear or you want me to expand examples (for example, add a debug/run launch task, or scaffold a test project), tell me which area to expand.
