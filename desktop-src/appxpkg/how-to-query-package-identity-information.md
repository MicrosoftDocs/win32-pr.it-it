---
title: Informazioni sul manifesto del pacchetto dell'applicazione di query (C++)
description: Informazioni su come ottenere informazioni dal manifesto del pacchetto dell'app per un'app di Windows con l'API per la creazione di pacchetti.
ms.assetid: A29986F9-C620-48CD-87F8-525DFA076AAB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9940f92a4412be7731db2454d68b4429522b63f6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046566"
---
# <a name="query-app-package-manifest-info-c"></a>Informazioni sul manifesto del pacchetto dell'applicazione di query (C++)

Informazioni su come ottenere informazioni dal manifesto del pacchetto dell'app per un'app di Windows con l'API per la creazione di [pacchetti](interfaces.md).

### <a name="create-a-package-manifest-reader"></a>Creazione di un reader del manifesto del pacchetto

Per creare un reader del manifesto del pacchetto, chiamare [**IAppxFactory:: CreatePackageReader**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxfactory-createpackagereader) per creare un lettore di pacchetti. Il primo parametro è un flusso di input per il pacchetto (file con estensione appx). Il secondo parametro è un parametro di output che riceve un puntatore a un puntatore [**IAppxPackageReader**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxpackagereader) . Successivamente, chiamare [**IAppxPackageReader:: getmanifest**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxpackagereader-getmanifest) per ottenere il lettore del manifesto. Il parametro è un parametro di output che riceve un puntatore a un puntatore [**IAppxManifestReader**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxmanifestreader) .


```C++
int wmain(
    _In_ int argc,
    _In_reads_(argc) wchar_t** argv)
{
    HRESULT hr = S_OK;
 
    if (argc != 2)
    {
        wprintf(L"Usage: DescribeAppx.exe inputFile\n");
        wprintf(L"       inputFile: Path to the app package to read\n");
        return 2;
    }

    // Specify the appropriate COM threading model
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);

    if (SUCCEEDED(hr))
    {
        IAppxPackageReader* packageReader = NULL;
        IAppxManifestReader* manifestReader = NULL;

        // Create a package reader using the file name given in command line
        hr = GetPackageReader(argv[1], &packageReader);

        // Get manifest reader for the package and read from the manifest
        if (SUCCEEDED(hr))
        {
            hr = packageReader->GetManifest(&manifestReader);
        }
        if (SUCCEEDED(hr))
        {
            hr = ReadManifest(manifestReader);
        }
    }
}

//
// Creates an app package reader.
//
// Parameters:
//   inputFileName 
//     Fully qualified name of the app package (.appx file) to be opened.
//   reader 
//     On success, receives the created instance of IAppxPackageReader.
//
HRESULT GetPackageReader(
    _In_ LPCWSTR inputFileName,
    _Outptr_ IAppxPackageReader** reader)
{
    HRESULT hr = S_OK;
    IAppxFactory* appxFactory = NULL;
    IStream* inputStream = NULL;

    // Create a new factory
    hr = CoCreateInstance(
            __uuidof(AppxFactory),
            NULL,
            CLSCTX_INPROC_SERVER,
            __uuidof(IAppxFactory),
            (LPVOID*)(&appxFactory));

    // Create a stream over the input app package
    if (SUCCEEDED(hr))
    {
        hr = SHCreateStreamOnFileEx(
                inputFileName,
                STGM_READ | STGM_SHARE_EXCLUSIVE,
                0, // default file attributes
                FALSE, // do not create new file
                NULL, // no template
                &inputStream);
    }

    // Create a new package reader using the factory.  For 
    // simplicity, we don't verify the digital signature of the package.
    if (SUCCEEDED(hr))
    {
        hr = appxFactory->CreatePackageReader(
                inputStream,
                reader);
    }

    // Clean up allocated resources
    if (inputStream != NULL)
    {
        inputStream->Release();
        inputStream = NULL;
    }
    if (appxFactory != NULL)
    {
        appxFactory->Release();
        appxFactory = NULL;
    }
    return hr;
}
```



### <a name="read-package-identity-info"></a>Leggere le informazioni sull'identità del pacchetto

L'identificazione del pacchetto viene specificata utilizzando l'elemento [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) nel manifesto. Usare [**IAppxManifestReader:: GetPackageId**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestreader-getpackageid) per ottenere un [**IAppxManifestPackageId**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxmanifestpackageid) per leggere le informazioni sull'identità del pacchetto, come illustrato di seguito.

Questo codice usa [**IAppxManifestPackageId:: GetPackageFullName**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestpackageid-getpackagefullname) per ottenere il nome completo del pacchetto, [**IAppxManifestPackageId:: GetName**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestpackageid-getname) , per ottenere il nome del pacchetto e [**IAppxManifestPackageId:: GetVersion**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestpackageid-getversion) per ottenere la versione del pacchetto.


```C++
//
// Reads a subset of the manifest Identity element.
//
//
HRESULT ReadManifestPackageId(
    _In_ IAppxManifestReader* manifestReader)
{
    HRESULT hr = S_OK;

    IAppxManifestPackageId* packageId = NULL;

    // Get elements and attributes from the manifest reader
    hr = manifestReader->GetPackageId(&packageId);
    if (SUCCEEDED(hr))
    {
        LPWSTR packageFullName = NULL;
        LPWSTR packageName = NULL;
        UINT64 packageVersion = 0;

        hr = packageId->GetPackageFullName(&packageFullName);

        if (SUCCEEDED(hr))
        {
            hr = packageId->GetName(&packageName);
        }
        if (SUCCEEDED(hr))
        {
            hr = packageId->GetVersion(&packageVersion);
        }
        if (SUCCEEDED(hr))
        {
            wprintf(L"Package full name: %s\n", packageFullName);
            wprintf(L"Package name: %s\n", packageName);
            wprintf(L"Package version: ");

            // Convert version number from 64-bit integer to dot-quad form
            for (int bitPosition = 0x30; bitPosition >= 0; bitPosition -= 0x10)
            {
                UINT64 versionWord = (packageVersion >> bitPosition) & 0xFFFF;
                wprintf(L"%llu.", versionWord);
            }
            wprintf(L"\n");
        }

        // Free all string buffers returned from the manifest API
        CoTaskMemFree(packageFullName);
        CoTaskMemFree(packageName);
    }

    // Clean up allocated resources
    if (packageId != NULL)
    {
        packageId->Release();
        packageId = NULL;
    }
     
    return hr;
}
```



### <a name="read-metadata-that-describes-the-package-to-users"></a>Leggere i metadati che descrivono il pacchetto per gli utenti

Le proprietà vengono specificate usando l'elemento [**Properties**](/uwp/schemas/appxpackage/appxmanifestschema/element-properties) nel manifesto. Usare [**IAppxManifestReader:: GetProperties**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestreader-getproperties) per ottenere un [**IAppxManifestProperties**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxmanifestproperties) per la lettura del nodo, come illustrato di seguito.

Questo codice usa [**IAppxManifestProperties:: GetStringValue**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestproperties-getstringvalue) per ottenere il nome visualizzato del pacchetto e la descrizione del pacchetto.


```C++
//
// Reads a subset of the manifest Properties element.
//
//
HRESULT ReadManifestProperties(
    _In_ IAppxManifestReader* manifestReader)
{
    HRESULT hr = S_OK;

    IAppxManifestProperties* properties = NULL;

    // Get elements and attributes from the manifest reader
    hr = manifestReader->GetProperties(&properties);
    if (SUCCEEDED(hr))
    {
        LPWSTR displayName = NULL;
        LPWSTR description = NULL;

        hr = properties->GetStringValue(L"DisplayName", &displayName);

        if (SUCCEEDED(hr))
        {
            hr = properties->GetStringValue(L"Description", &description);
        }
        if (SUCCEEDED(hr))
        {
            wprintf(L"Package display name: %s\n", displayName);
            wprintf(L"Package description:  %s\n", description);
        }

        // Free all string buffers returned from the manifest API
        CoTaskMemFree(displayName);
        CoTaskMemFree(description);
    }
    // Clean up allocated resources
    if (properties != NULL)
    {
        properties->Release();
        properties = NULL;
    }

    return hr;
}
```



### <a name="read-metadata-about-the-apps-included-in-the-package"></a>Leggere i metadati sulle app incluse nel pacchetto

Le app vengono specificate usando l'elemento [**Applications**](/uwp/schemas/appxpackage/appxmanifestschema/element-applications) nel manifesto. Usare [**IAppxManifestReader:: GetApplications**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestreader-getapplications) per ottenere un [**IAppxManifestApplicationsEnumerator**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxmanifestapplicationsenumerator) per la lettura di questo nodo. Usare [**IAppxManifestApplicationsEnumerator:: GetCurrent**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestapplicationsenumerator-getcurrent) e [**IAppxManifestApplicationsEnumerator:: MoveNext**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestapplicationsenumerator-movenext) per ottenere un [**IAppxManifestApplication**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxmanifestapplication) per ogni app nel pacchetto.

Questo codice usa [**IAppxManifestApplication:: GetStringValue**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestapplication-getstringvalue) per ottenere il nome visualizzato per ogni app.


```C++
//
// Reads a subset of the manifest Applications element.
//
//
HRESULT ReadManifestApplications(
    _In_ IAppxManifestReader* manifestReader)
{
    HRESULT hr = S_OK;
    BOOL hasCurrent = FALSE;
    UINT32 applicationsCount = 0;

    IAppxManifestApplicationsEnumerator* applications = NULL;

    // Get elements and attributes from the manifest reader
    hr = manifestReader->GetApplications(&applications);
    if (SUCCEEDED(hr))
    {
        hr = applications->GetHasCurrent(&hasCurrent);

        while (SUCCEEDED(hr) && hasCurrent)
        {
            IAppxManifestApplication* application = NULL;
            LPWSTR applicationName = NULL;

            hr = applications->GetCurrent(&application);
            if (SUCCEEDED(hr))
            {
                application->GetStringValue(L"DisplayName", &applicationName);
            }
            if (SUCCEEDED(hr))
            {
                applicationsCount++;
                wprintf(L"App #%u: %s\n", applicationsCount, applicationName);
            }

            if (SUCCEEDED(hr))
            {
                hr = applications->MoveNext(&hasCurrent);
            }
            if (application != NULL)
            {
                application->Release();
                application = NULL;
            }
            CoTaskMemFree(applicationName);
        }

        wprintf(L"Count of apps in the package: %u\n", applicationsCount);
    }

    // Clean up allocated resources
    if (applications != NULL)
    {
        applications->Release();
        applications = NULL;
    }

    return hr;
}
```



### <a name="clean-up-the-package-manifest-reader"></a>Pulire il reader del manifesto del pacchetto

Prima di restituire dalla `wmain` funzione, chiamare il metodo [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) per pulire il reader del manifesto del pacchetto e chiamare la funzione [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) .


```C++
// Clean up allocated resources
if (manifestReader != NULL)
{
    manifestReader->Release();
    manifestReader = NULL;
}
if (packageReader != NULL)
{
    packageReader->Release();
    packageReader = NULL;
}

CoUninitialize();
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Esempi**
</dt> <dt>

[Esempio di query del pacchetto dell'app e del manifesto dell'applicazione](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingDescribeAppx)
</dt> <dt>

**Riferimento**
</dt> <dt>

[**IAppxManifestReader**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxmanifestreader)
</dt> </dl>

 

 