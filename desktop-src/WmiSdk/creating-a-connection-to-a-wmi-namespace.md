---
description: Dopo aver impostato le chiamate standard a COM, è necessario connettersi a WMI tramite una chiamata al metodo IWbemLocator::ConnectServer.
ms.assetid: f0b33ff0-47b0-4aea-ab0f-9220ae367f67
ms.tgt_platform: multiple
title: Creazione di una connessione a uno spazio dei nomi WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2587024d7f581cd28a8fdaf339db9567b17c509599c01aca0599b701186fb786
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119412141"
---
# <a name="creating-a-connection-to-a-wmi-namespace"></a>Creazione di una connessione a uno spazio dei nomi WMI

Dopo aver impostato le chiamate standard a COM, è necessario connettersi a WMI tramite una chiamata al metodo [**IWbemLocator::ConnectServer.**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) Il **metodo ConnectServer** restituisce un proxy di [**un'interfaccia IWbemServices.**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) Tramite **IWbemServices** è possibile accedere alle diverse funzionalità di WMI.

Gli esempi di codice in questo argomento richiedono i riferimenti seguenti e includono \# istruzioni per la compilazione corretta.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <windows.h>
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



La procedura seguente descrive come creare una connessione a uno spazio dei nomi WMI.

**Per creare una connessione a uno spazio dei nomi WMI**

-   Inizializzare [**l'interfaccia IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) tramite una chiamata a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

    WMI non richiede l'esecuzione di procedure aggiuntive quando si chiama [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) in [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).

    Nell'esempio di codice seguente viene descritto come inizializzare [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator).

    ```C++
        IWbemLocator *pLoc = 0;
        HRESULT hr;

        hr = CoCreateInstance(CLSID_WbemLocator, 0, 
            CLSCTX_INPROC_SERVER, IID_IWbemLocator, (LPVOID *) &pLoc);
     
        if (FAILED(hr))
        {
            cout << "Failed to create IWbemLocator object. Err code = 0x"
                 << hex << hr << endl;
            CoUninitialize();
            return hr;     // Program has failed.
        }
    ```

    

    -   Connessione wmi tramite una chiamata al [**metodo IWbemLocator::ConnectServer.**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)

        Il [**metodo ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) restituisce un proxy a un'interfaccia [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) che usa per accedere allo spazio dei nomi WMI locale o remoto specificato nella chiamata a **ConnectServer**.

        Nell'esempio di codice seguente viene descritto come chiamare [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).

        ```C++
        IWbemServices *pSvc = 0;

            // Connect to the root\default namespace with the current user.
            hr = pLoc->ConnectServer(
                    BSTR(L"ROOT\\DEFAULT"),  //namespace
                    NULL,       // User name 
                    NULL,       // User password
                    0,         // Locale 
                    NULL,     // Security flags
                    0,         // Authority 
                    0,        // Context object 
                    &pSvc);   // IWbemServices proxy


            if (FAILED(hr))
            {
                cout << "Could not connect. Error code = 0x" 
                     << hex << hr << endl;
                pLoc->Release();
                CoUninitialize();
                return hr;      // Program has failed.
            }

            cout << "Connected to WMI" << endl;
        ```

        

Dopo aver ricevuto un puntatore al proxy [**IWbemServices,**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) è necessario impostare la sicurezza sul proxy per accedere a WMI. Per altre informazioni, vedere [Impostazione dei livelli di sicurezza in una connessione WMI.](setting-the-security-levels-on-a-wmi-connection.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un'applicazione WMI con C++](creating-a-wmi-application-using-c-.md)
</dt> <dt>

[Supporto IPv6 e IPv4 in WMI](ipv6-and-ipv4-support-in-wmi.md)
</dt> </dl>

 

 
