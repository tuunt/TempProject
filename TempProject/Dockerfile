FROM mcr.microsoft.com/dotnet/aspnet:8.0 AS base
#------------------------------------------------------------------------------
# Copy publishing artifacts.
#------------------------------------------------------------------------------

    WORKDIR /app
    COPY bin/Release/net8.0/publish/ /app/
    
    ENV ASPNETCORE_URLS=http://0.0.0.0:8080
    
    #------------------------------------------------------------------------------
    # Run application in Kestrel.
    #------------------------------------------------------------------------------
    
    ENTRYPOINT ["dotnet", "TempProject.dll"]