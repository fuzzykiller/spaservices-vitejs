# SpaServices.ViteJsDevServer

[![CI Build](https://github.com/fuzzykiller/spaservices-vitejs/workflows/CI%20Build/badge.svg)](https://github.com/fuzzykiller/spaservices-vitejs/actions)

Brings plug'n'play support for Vite.js to ASP.NET Core. [Vite.js](https://vitejs.dev) is an
opinionated build tool that enables lightning-fast development by relying on non-bundled
JavaScript modules.

## Caveats:

The HMR WebSocket setup is not relative to the web root in Vite.js. This means it cannot 
reliably work with the ASP.NET Core development reverse proxy.

That’s why a NuGet package will not be properly published for now.

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
