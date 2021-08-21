---
description: È possibile utilizzare la procedura e gli esempi di codice in questo argomento per creare un'applicazione client WMI completa che esegue l'inizializzazione COM, si connette a WMI nel computer locale, recupera i dati in modo semisincrono e quindi esegue la pulizia.
ms.assetid: 35dc97aa-dcef-48c1-af8b-ce43e3cf1d3e
ms.tgt_platform: multiple
title: 'Esempio: Recupero di dati WMI dal computer locale'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71036d95996926ce9e5a0200587a15abb8dc992c82999aa65c54be50d0e1691b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050909"
---
# <a name="example-getting-wmi-data-from-the-local-computer"></a>Esempio: Recupero di dati WMI dal computer locale

È possibile utilizzare la procedura e gli esempi di codice in questo argomento per creare un'applicazione client WMI completa che esegue l'inizializzazione COM, si connette a WMI nel computer locale, recupera i dati in modo semisincrono e quindi esegue la pulizia. Questo esempio ottiene il nome del sistema operativo nel computer locale e lo visualizza. Per recuperare dati da un computer remoto, vedere [Esempio: Recupero di dati WMI da un computer remoto.](example--getting-wmi-data-from-a-remote-computer.md) Per ottenere i dati in modo asincrono, vedere Esempio: Recupero di dati WMI dal computer locale in [modo asincrono.](example--getting-wmi-data-from-the-local-computer-asynchronously.md)

La procedura seguente viene utilizzata per eseguire l'applicazione WMI. I passaggi da 1 a 5 contengono tutti i passaggi necessari per configurare e connettersi a WMI e i passaggi 6 e 7 sono la posizione in cui i dati vengono sottoposti a query e ricevuti.

1.  Inizializzare i parametri COM con una chiamata a [**CoInitializeEx.**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex)

    Per altre informazioni, vedere [Inizializzazione di COM per un'applicazione WMI.](initializing-com-for-a-wmi-application.md)

2.  Inizializzare la sicurezza dei processi COM chiamando [**CoInitializeSecurity.**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)

    Per altre informazioni, vedere [Impostazione del livello di sicurezza del processo predefinito tramite C++.](setting-the-default-process-security-level-using-c-.md)

3.  Ottenere il localizzatore iniziale in WMI chiamando [**CoCreateInstance.**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)

    Per altre informazioni, vedere [Creazione di una connessione a uno spazio dei nomi WMI.](creating-a-connection-to-a-wmi-namespace.md)

4.  Ottenere un puntatore [**a IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) per lo spazio dei nomi radice cimv2 nel computer locale \\ chiamando [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver). Per connettersi a un computer remoto, vedere [Esempio: Recupero di dati WMI da un computer remoto.](example--getting-wmi-data-from-a-remote-computer.md)

    Per altre informazioni, vedere [Creazione di una connessione a uno spazio dei nomi WMI.](creating-a-connection-to-a-wmi-namespace.md)

5.  Impostare la sicurezza del proxy [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) in modo che il servizio WMI possa rappresentare il client chiamando [**CoSetProxyBlanket.**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)

    Per altre informazioni, vedere [Impostazione dei livelli di sicurezza in una connessione WMI.](setting-the-security-levels-on-a-wmi-connection.md)

6.  Usare il [**puntatore IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) per effettuare richieste di WMI. In questo esempio viene eseguita una query per il nome del sistema operativo chiamando [**IWbemServices::ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery).

    La query WQL seguente è uno degli argomenti del metodo .

    `SELECT * FROM Win32_OperatingSystem`

    Il risultato di questa query viene archiviato in un [**puntatore IEnumWbemClassObject.**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) In questo modo gli oggetti dati della query possono essere recuperati in modo semisincrono con **l'interfaccia IEnumWbemClassObject.** Per altre informazioni, vedere [Enumerazione di WMI.](enumerating-wmi.md) Per ottenere i dati in modo asincrono, vedere Esempio: Recupero di dati WMI dal computer locale in [modo asincrono.](example--getting-wmi-data-from-the-local-computer-asynchronously.md)

    Per altre informazioni sull'esecuzione di richieste a WMI, vedere [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md), [Querying WMI](querying-wmi.md)e Calling a [Method](calling-a-method.md).

7.  Ottenere e visualizzare i dati dalla query WQL. Il [**puntatore IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) è collegato agli oggetti dati restituiti dalla query e gli oggetti dati possono essere recuperati con il metodo [**IEnumWbemClassObject::Next.**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) Questo metodo collega gli oggetti dati a un [**puntatore IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) passato al metodo . Usare il [**metodo IWbemClassObject::Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) per ottenere le informazioni desiderate dagli oggetti dati.

    L'esempio di codice seguente viene usato per ottenere la proprietà Name dall'oggetto dati , che fornisce il nome del sistema operativo.

    ```C++
    VARIANT vtProp;

    // Get the value of the Name property
    hr = pclsObj->Get(L"Name", 0, &vtProp, 0, 0);
    ```

    

    Dopo che il valore della proprietà Name è stato archiviato nella [**variabile VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) vtProp, può essere visualizzato all'utente.

    Per altre informazioni, vedere [Enumerazione di WMI.](enumerating-wmi.md)

Nell'esempio di codice seguente vengono recuperati dati WMI in modo semisincrono da un computer locale.


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

    // Step 1: --------------------------------------------------
    // Initialize COM. ------------------------------------------

    hres =  CoInitializeEx(0, COINIT_MULTITHREADED); 
    if (FAILED(hres))
    {
        cout << "Failed to initialize COM library. Error code = 0x" 
            << hex << hres << endl;
        return 1;                  // Program has failed.
    }

    // Step 2: --------------------------------------------------
    // Set general COM security levels --------------------------

    hres =  CoInitializeSecurity(
        NULL, 
        -1,                          // COM authentication
        NULL,                        // Authentication services
        NULL,                        // Reserved
        RPC_C_AUTHN_LEVEL_DEFAULT,   // Default authentication 
        RPC_C_IMP_LEVEL_IMPERSONATE, // Default Impersonation  
        NULL,                        // Authentication info
        EOAC_NONE,                   // Additional capabilities 
        NULL                         // Reserved
        );

                      
    if (FAILED(hres))
    {
        cout << "Failed to initialize security. Error code = 0x" 
            << hex << hres << endl;
        CoUninitialize();
        return 1;                    // Program has failed.
    }
    
    // Step 3: ---------------------------------------------------
    // Obtain the initial locator to WMI -------------------------

    IWbemLocator *pLoc = NULL;

    hres = CoCreateInstance(
        CLSID_WbemLocator,             
        0, 
        CLSCTX_INPROC_SERVER, 
        IID_IWbemLocator, (LPVOID *) &pLoc);
 
    if (FAILED(hres))
    {
        cout << "Failed to create IWbemLocator object."
            << " Err code = 0x"
            << hex << hres << endl;
        CoUninitialize();
        return 1;                 // Program has failed.
    }

    // Step 4: -----------------------------------------------------
    // Connect to WMI through the IWbemLocator::ConnectServer method

    IWbemServices *pSvc = NULL;
 
    // Connect to the root\cimv2 namespace with
    // the current user and obtain pointer pSvc
    // to make IWbemServices calls.
    hres = pLoc->ConnectServer(
         _bstr_t(L"ROOT\\CIMV2"), // Object path of WMI namespace
         NULL,                    // User name. NULL = current user
         NULL,                    // User password. NULL = current
         0,                       // Locale. NULL indicates current
         NULL,                    // Security flags.
         0,                       // Authority (for example, Kerberos)
         0,                       // Context object 
         &pSvc                    // pointer to IWbemServices proxy
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


    // Step 5: --------------------------------------------------
    // Set security levels on the proxy -------------------------

    hres = CoSetProxyBlanket(
       pSvc,                        // Indicates the proxy to set
       RPC_C_AUTHN_WINNT,           // RPC_C_AUTHN_xxx
       RPC_C_AUTHZ_NONE,            // RPC_C_AUTHZ_xxx
       NULL,                        // Server principal name 
       RPC_C_AUTHN_LEVEL_CALL,      // RPC_C_AUTHN_LEVEL_xxx 
       RPC_C_IMP_LEVEL_IMPERSONATE, // RPC_C_IMP_LEVEL_xxx
       NULL,                        // client identity
       EOAC_NONE                    // proxy capabilities 
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

    // Step 6: --------------------------------------------------
    // Use the IWbemServices pointer to make requests of WMI ----

    // For example, get the name of the operating system
    IEnumWbemClassObject* pEnumerator = NULL;
    hres = pSvc->ExecQuery(
        bstr_t("WQL"), 
        bstr_t("SELECT * FROM Win32_OperatingSystem"),
        WBEM_FLAG_FORWARD_ONLY | WBEM_FLAG_RETURN_IMMEDIATELY, 
        NULL,
        &pEnumerator);
    
    if (FAILED(hres))
    {
        cout << "Query for operating system name failed."
            << " Error code = 0x" 
            << hex << hres << endl;
        pSvc->Release();
        pLoc->Release();
        CoUninitialize();
        return 1;               // Program has failed.
    }

    // Step 7: -------------------------------------------------
    // Get the data from the query in step 6 -------------------
 
    IWbemClassObject *pclsObj = NULL;
    ULONG uReturn = 0;
   
    while (pEnumerator)
    {
        HRESULT hr = pEnumerator->Next(WBEM_INFINITE, 1, 
            &pclsObj, &uReturn);

        if(0 == uReturn)
        {
            break;
        }

        VARIANT vtProp;

        // Get the value of the Name property
        hr = pclsObj->Get(L"Name", 0, &vtProp, 0, 0);
        wcout << " OS Name : " << vtProp.bstrVal << endl;
        VariantClear(&vtProp);

        pclsObj->Release();
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



 

 
