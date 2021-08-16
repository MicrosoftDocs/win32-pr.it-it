---
description: È possibile utilizzare la procedura e gli esempi di codice in questo argomento per creare un'applicazione client WMI completa che esegue l'inizializzazione COM, si connette a WMI nel computer locale, legge alcuni dati ed esegue la pulizia.
ms.assetid: d80bcf9f-e57c-499f-b7b8-cf25678c5a82
ms.tgt_platform: multiple
title: "Esempio: Creazione di un'applicazione WMI"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49e7633c666beb900da4cdbe41909880d9766c903be0fc8b6aa1d4e45be8d90f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118319310"
---
# <a name="example-creating-a-wmi-application"></a>Esempio: Creazione di un'applicazione WMI

È possibile utilizzare la procedura e gli esempi di codice in questo argomento per creare un'applicazione client WMI completa che esegue l'inizializzazione COM, si connette a WMI nel computer locale, legge alcuni dati ed esegue la pulizia. [Connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md) descrive come ottenere dati da computer remoti.

La procedura seguente include tutti i passaggi richiesti da tutte le applicazioni WMI C++.

1.  Inizializzare i parametri COM con una chiamata a [**CoInitializeEx.**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex)

    Per altre informazioni, vedere [Inizializzazione di COM per un'applicazione WMI.](initializing-com-for-a-wmi-application.md)

2.  Inizializzare la sicurezza dei processi COM chiamando [**CoInitializeSecurity.**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)

    Per altre informazioni, vedere [Impostazione del livello di sicurezza del processo predefinito tramite C++.](setting-the-default-process-security-level-using-c-.md)

3.  Ottenere un puntatore a [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) per uno spazio dei nomi in un computer host specifico, nel caso più semplice, il computer locale, chiamando [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).

    Per connettersi a un computer remoto, ad esempio computer \_ A, usare il parametro del percorso dell'oggetto seguente:

    ```C++
    _bstr_t(L"\\COMPUTER_A\ROOT\\CIMV2")
    ```

    

    Per altre informazioni, vedere [Creazione di una connessione a uno spazio dei nomi WMI.](creating-a-connection-to-a-wmi-namespace.md)

4.  Impostare la sicurezza del proxy [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) in modo che il servizio WMI possa rappresentare il client chiamando [**CoSetProxyBlanket.**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)

    Per altre informazioni, vedere [Impostazione dei livelli di sicurezza in una connessione WMI.](setting-the-security-levels-on-a-wmi-connection.md)

5.  Usare il [**puntatore IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) per effettuare richieste di WMI. Ad esempio, l'esecuzione di una query per [**tutte le istanze del servizio Win32 \_**](/windows/desktop/CIMWin32Prov/win32-service) per determinare quali servizi vengono arrestati.

    Per altre informazioni, vedere [Modifica delle informazioni su classi e istanze,](manipulating-class-and-instance-information.md)Esecuzione di query su [WMI](querying-wmi.md)e Ricezione di un [evento WMI.](receiving-a-wmi-event.md)

6.  Pulire gli oggetti e COM.

    Per altre informazioni, vedere [Pulizia e arresto di un'applicazione WMI.](cleaning-up-and-shutting-down-a-wmi-application.md)

Il codice di esempio seguente è un'applicazione client WMI completa.


```C++

#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")

int main(int argc, char **argv)
{
    HRESULT hres;

    // Initialize COM.
    hres =  CoInitializeEx(0, COINIT_MULTITHREADED); 
    if (FAILED(hres))
    {
        cout << "Failed to initialize COM library. " 
            << "Error code = 0x" 
            << hex << hres << endl;
        return 1;              // Program has failed.
    }

    // Initialize 
    hres =  CoInitializeSecurity(
        NULL,     
        -1,      // COM negotiates service                  
        NULL,    // Authentication services
        NULL,    // Reserved
        RPC_C_AUTHN_LEVEL_DEFAULT,    // authentication
        RPC_C_IMP_LEVEL_IMPERSONATE,  // Impersonation
        NULL,             // Authentication info 
        EOAC_NONE,        // Additional capabilities
        NULL              // Reserved
        );

                      
    if (FAILED(hres))
    {
        cout << "Failed to initialize security. " 
            << "Error code = 0x" 
            << hex << hres << endl;
        CoUninitialize();
        return 1;          // Program has failed.
    }

    // Obtain the initial locator to Windows Management
    // on a particular host computer.
    IWbemLocator *pLoc = 0;

    hres = CoCreateInstance(
        CLSID_WbemLocator,             
        0, 
        CLSCTX_INPROC_SERVER, 
        IID_IWbemLocator, (LPVOID *) &pLoc);
 
    if (FAILED(hres))
    {
        cout << "Failed to create IWbemLocator object. "
            << "Error code = 0x"
            << hex << hres << endl;
        CoUninitialize();
        return 1;       // Program has failed.
    }

    IWbemServices *pSvc = 0;

    // Connect to the root\cimv2 namespace with the
    // current user and obtain pointer pSvc
    // to make IWbemServices calls.

    hres = pLoc->ConnectServer(
        
        _bstr_t(L"ROOT\\CIMV2"), // WMI namespace
        NULL,                    // User name
        NULL,                    // User password
        0,                       // Locale
        NULL,                    // Security flags                 
        0,                       // Authority       
        0,                       // Context object
        &pSvc                    // IWbemServices proxy
        );                              
    
    if (FAILED(hres))
    {
        cout << "Could not connect. Error code = 0x" 
            << hex << hres << endl;
        pLoc->Release();     
        CoUninitialize();
        return 1;                // Program has failed.
    }

    cout << "Connected to ROOT\\CIMV2 WMI namespace" << endl;

    // Set the IWbemServices proxy so that impersonation
    // of the user (client) occurs.
    hres = CoSetProxyBlanket(
       
       pSvc,                         // the proxy to set
       RPC_C_AUTHN_WINNT,            // authentication service
       RPC_C_AUTHZ_NONE,             // authorization service
       NULL,                         // Server principal name
       RPC_C_AUTHN_LEVEL_CALL,       // authentication level
       RPC_C_IMP_LEVEL_IMPERSONATE,  // impersonation level
       NULL,                         // client identity 
       EOAC_NONE                     // proxy capabilities     
    );

    if (FAILED(hres))
    {
        cout << "Could not set proxy blanket. Error code = 0x" 
             << hex << hres << endl;
        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 1;               // Program has failed.
    }


    // Use the IWbemServices pointer to make requests of WMI. 
    // Make requests here:

    // For example, query for all the running processes
    IEnumWbemClassObject* pEnumerator = NULL;
    hres = pSvc->ExecQuery(
        bstr_t("WQL"), 
        bstr_t("SELECT * FROM Win32_Process"),
        WBEM_FLAG_FORWARD_ONLY | WBEM_FLAG_RETURN_IMMEDIATELY, 
        NULL,
        &pEnumerator);
    
    if (FAILED(hres))
    {
        cout << "Query for processes failed. "
             << "Error code = 0x" 
             << hex << hres << endl;
        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 1;               // Program has failed.
    }
    else
    { 
        IWbemClassObject *pclsObj;
        ULONG uReturn = 0;
   
        while (pEnumerator)
        {
            hres = pEnumerator->Next(WBEM_INFINITE, 1, 
                &pclsObj, &uReturn);

            if(0 == uReturn)
            {
                break;
            }

            VARIANT vtProp;

            // Get the value of the Name property
            hres = pclsObj->Get(L"Name", 0, &vtProp, 0, 0);
            wcout << "Process Name : " << vtProp.bstrVal << endl;
            VariantClear(&vtProp);
            
            pclsObj->Release();
            pclsObj = NULL;
        }
         
    }
 
    // Cleanup
    // ========
    
    pSvc->Release();
    pLoc->Release();
    pEnumerator->Release();  
    
    CoUninitialize();

    return 0;   // Program successfully completed.
}
```



 

 
