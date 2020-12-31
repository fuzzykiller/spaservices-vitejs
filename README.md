# SpaServices.ViteJsDevServer

Brings plug'n'play support for Vite.js to ASP.NET Core. [Vite.js](https://vitejs.dev) is an
opinionated build tool that enables lighning-fast development by relying on non-bundled
JavaScript modules.

## Usage:

    app.UseSpa(
        spa =>
        {
            spa.Options.SourcePath = "ClientApp";

            if (env.IsDevelopment())
            {
                spa.UseViteJsDevServer(npmScript: "dev");
            }
        });

## Copyright

Includes code taken directly from `Microsoft.AspNetCore.SpaServices.Extensions`. This includes
all source files included from the `aspnetcore` submodule.

## License

Available under Apache License 2.0
