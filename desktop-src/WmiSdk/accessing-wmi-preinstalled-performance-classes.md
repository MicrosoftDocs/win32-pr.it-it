---
description: Il repository WMI contiene classi di prestazioni preinstallate per tutti gli oggetti della libreria delle prestazioni.
ms.assetid: 2158385f-d0dc-4102-84db-ce02d2b0ee53
ms.tgt_platform: multiple
title: Accesso alle classi di prestazioni preinstallate WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0265f9b4008913a463545ed03cd6f1025b58ef5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313205"
---
# <a name="accessing-wmi-preinstalled-performance-classes"></a>Accesso alle classi di prestazioni preinstallate WMI

Il repository WMI contiene classi di prestazioni preinstallate per tutti gli oggetti della libreria delle prestazioni. Ad esempio, le istanze della classe prestazioni dati non elaborati [**Win32 \_ PerfRawData \_ PerfProc \_ processo**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) rappresentano i processi. Questo oggetto prestazione è visibile in monitoraggio di sistema come oggetto processo.

La proprietà **PageFaultsPerSec** del [**\_ \_ \_ processo Win32 PerfRawData PerfProc**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) rappresenta il contatore delle prestazioni errori di pagina al secondo per il processo. Le classi [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) contengono i valori dei dati calcolati visualizzati in Monitor di sistema (Perfmon.exe). Il valore della proprietà **PageFaultsPerSec** del [**processo Win32 \_ PerfFormattedData \_ PerfProc \_**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) è uguale a quello visualizzato in Monitor di sistema.

Utilizzare l' [API com per WMI](com-api-for-wmi.md) o l' [API di scripting per WMI](scripting-api-for-wmi.md) per accedere ai dati sulle prestazioni tramite le [classi del contatore delle prestazioni](/windows/desktop/CIMWin32Prov/performance-counter-classes). In entrambi i casi è necessario un oggetto di [*aggiornamento*](gloss-r.md) per ottenere ogni campione di dati. Per ulteriori informazioni ed esempi di codice di script per l'utilizzo di aggiornamenti e per l'accesso alle classi di prestazioni, vedere [attività WMI: monitoraggio delle prestazioni](wmi-tasks--performance-monitoring.md). Per ulteriori informazioni, vedere [accesso ai dati sulle prestazioni nello script](accessing-performance-data-in-script.md).

## <a name="accessing-performance-data-from-c"></a>Accesso ai dati sulle prestazioni da C++

Nell'esempio di codice C++ riportato di seguito viene utilizzato il provider del contatore delle prestazioni per accedere alle classi a prestazioni elevate predefinite. Viene creato un oggetto di aggiornamento e viene aggiunto un oggetto al nuovo aggiornamento. L'oggetto è un'istanza del [**\_ \_ \_ processo PerfProc Win32 PerfRawData**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) che monitora le prestazioni di un processo specifico. Il codice legge solo una proprietà del contatore nell'oggetto processo, ovvero la proprietà **byte virtuali** . Il codice richiede i riferimenti seguenti e le istruzioni **\# include** per la compilazione corretta.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



Nella procedura seguente viene illustrato come accedere ai dati da un provider a prestazioni elevate in C++.

**Per accedere ai dati da un provider a prestazioni elevate in C++**

1.  Stabilire una connessione allo spazio dei nomi WMI e impostare la sicurezza WMI utilizzando una chiamata a [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) e [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).

    Questo passaggio è un passaggio standard per la creazione di qualsiasi applicazione client WMI. Per ulteriori informazioni, vedere [creazione di un'applicazione WMI con C++](creating-a-wmi-application-using-c-.md).

2.  Creare un oggetto di aggiornamento utilizzando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con CLSID \_ WbemRefresher. Richiedere un'interfaccia [**IWbemConfigureRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemconfigurerefresher) tramite il metodo [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) . Richiedere un'interfaccia [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) tramite il metodo **QueryInterface** .

    L'interfaccia [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) è l'interfaccia principale per l'oggetto di [**aggiornamento**](swbemrefreshableitem-refresher.md) WMI.

    Nell'esempio di codice C++ riportato di seguito viene illustrato come recuperare [**IWbemConfigureRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher).

    ```C++
    IWbemRefresher* pRefresher = NULL;

    HRESULT hr = CoCreateInstance(
        CLSID_WbemRefresher,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_IWbemRefresher,
        (void**) &pRefresher);

    IWbemConfigureRefresher* pConfig = NULL;

    pRefresher->QueryInterface( 
        IID_IWbemConfigureRefresher,
        (void**) &pConfig
      );
    ```

    

3.  Aggiungere un oggetto all'aggiornamento tramite una chiamata al metodo [**IWbemConfigureRefresher:: AddObjectByPath**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath) .

    Quando si aggiunge un oggetto all'aggiornamento, WMI aggiorna l'oggetto ogni volta che si chiama il metodo [**IWbemRefresher:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) . L'oggetto aggiunto designa il provider nei qualificatori di classe.

    Nell'esempio di codice C++ riportato di seguito viene illustrato come chiamare [**AddObjectByPath**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath).

    ```C++
    IWbemClassObject* pObj = NULL;
    IWbemServices* pNameSpace = NULL;

    // Add the instance to be refreshed.
    hr = pConfig->AddObjectByPath(
         pNameSpace,
         L"Win32_PerfRawData_PerfProc_Process.Name=\"WINWORD\"",
         0L,
         NULL,
         &pObj,
         NULL
    );
    if (FAILED(hr))
    {
       cout << "Could not add object. Error code: 0x"
            << hex << hr << endl;
       pNameSpace->Release();
       return hr;
    }
    ```

    

4.  Per configurare un accesso più rapido all'oggetto, connettersi all'interfaccia [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) tramite [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sull'interfaccia [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) .

    Nell'esempio di codice C++ riportato di seguito viene illustrato come recuperare un puntatore all'oggetto utilizzando [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) anziché [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject).

    ```C++
        // For quick property retrieval, use IWbemObjectAccess.
        IWbemObjectAccess* pAcc = NULL;
        pObj->QueryInterface( IID_IWbemObjectAccess, (void**) &pAcc );
        // This is not required.
        pObj->Release();
    ```

    

    L'interfaccia [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) consente di aumentare le prestazioni in quanto è possibile ottenere handle per specifiche proprietà dei contatori ed è necessario bloccare e sbloccare l'oggetto nel codice, ovvero un'operazione eseguita da [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) per ogni accesso alla proprietà.

5.  Ottenere gli handle delle proprietà da esaminare usando le chiamate al metodo [**IWbemObjectAccess:: GetPropertyHandle**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-getpropertyhandle) .

    Gli handle di proprietà sono gli stessi per tutte le istanze di una classe, il che significa che usa l'handle di proprietà recuperato da un'istanza specifica per tutte le istanze di una classe specifica. È anche possibile ottenere un handle da un oggetto classe per recuperare i valori delle proprietà da un oggetto istanza.

    Nell'esempio di codice C++ riportato di seguito viene illustrato come recuperare un handle di proprietà.

    ```C++
        // Get a property handle for the VirtualBytes property
        long lVirtualBytesHandle = 0;
        DWORD dwVirtualBytes = 0;
        CIMTYPE variant;

        hr = pAcc->GetPropertyHandle(L"VirtualBytes",
             &variant,
             &lVirtualBytesHandle 
        );
        if (FAILED(hr))
        {
           cout << "Could not get property handle. Error code: 0x"
                << hex << hr << endl;
           return hr;
        }
    ```

    

6.  Creare un ciclo di programmazione che esegua le azioni seguenti:

    -   Aggiornare l'oggetto con una chiamata a [**IWbemRefresher:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) utilizzando il puntatore creato nella precedente chiamata a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

        In questa chiamata, l'aggiornamento WMI aggiorna l'oggetto client usando i dati forniti dal provider.

    -   Eseguire tutte le azioni necessarie per l'oggetto, ad esempio il recupero di un nome di proprietà, di un tipo di dati o di un valore.

        È possibile accedere alla proprietà tramite l'handle di proprietà ottenuto in precedenza. A causa della chiamata di [**aggiornamento**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) , WMI aggiorna la proprietà ogni volta nel ciclo.

Nell'esempio C++ riportato di seguito viene illustrato come utilizzare l'API WMI a prestazioni elevate.


```C++
// Get the local locator object
IWbemServices* pNameSpace = NULL;
IWbemLocator* pWbemLocator = NULL;
CIMTYPE variant;
VARIANT VT;

CoCreateInstance( CLSID_WbemLocator, NULL,
    CLSCTX_INPROC_SERVER, IID_IWbemLocator, (void**) &pWbemLocator
);

// Connect to the desired namespace
BSTR bstrNameSpace = SysAllocString( L"\\\\.\\root\\cimv2" );

HRESULT hr = WBEM_S_NO_ERROR;

hr = pWbemLocator->ConnectServer(
     bstrNameSpace,      // Namespace name
     NULL,               // User name
     NULL,               // Password
     NULL,               // Locale
     0L,                 // Security flags
     NULL,               // Authority
     NULL,               // Wbem context
     &pNameSpace         // Namespace
);

if ( SUCCEEDED( hr ) )
{
    // Set namespace security.
    IUnknown* pUnk = NULL;
    pNameSpace->QueryInterface( IID_IUnknown, (void**) &pUnk );

    hr = CoSetProxyBlanket(
         pNameSpace, 
         RPC_C_AUTHN_WINNT, 
         RPC_C_AUTHZ_NONE, 
         NULL, 
         RPC_C_AUTHN_LEVEL_DEFAULT, 
         RPC_C_IMP_LEVEL_IMPERSONATE,
         NULL, 
         EOAC_NONE 
    );
    if (FAILED(hr))
    {
       cout << "Cannot set proxy blanket. Error code: 0x"
            << hex << hr << endl;
       pNameSpace->Release();
       return hr;
    }

    hr = CoSetProxyBlanket(pUnk, 
         RPC_C_AUTHN_WINNT, 
         RPC_C_AUTHZ_NONE, 
         NULL, 
         RPC_C_AUTHN_LEVEL_DEFAULT, 
         RPC_C_IMP_LEVEL_IMPERSONATE,
         NULL, 
         EOAC_NONE 
    );
    if (FAILED(hr))
    {
       cout << "Cannot set proxy blanket. Error code: 0x"
            << hex << hr << endl;
       pUnk->Release();
       return hr;
    }

    // Clean up the IUnknown.
    pUnk->Release();

    IWbemRefresher* pRefresher = NULL;
    IWbemConfigureRefresher* pConfig = NULL;

    // Create a WMI Refresher and get a pointer to the
    // IWbemConfigureRefresher interface.
    CoCreateInstance(CLSID_WbemRefresher, 
                     NULL,
                     CLSCTX_INPROC_SERVER, 
                     IID_IWbemRefresher, 
                     (void**) &pRefresher 
    );
    
    pRefresher->QueryInterface(IID_IWbemConfigureRefresher,
                               (void**) &pConfig );

    IWbemClassObject* pObj = NULL;

    // Add the instance to be refreshed.
    pConfig->AddObjectByPath(
       pNameSpace,
       L"Win32_PerfRawData_PerfProc_Process.Name=\"WINWORD\"",
       0L,
       NULL,
       &pObj,
       NULL 
    );
    if (FAILED(hr))
    {
       cout << "Cannot add object. Error code: 0x"
            << hex << hr << endl;
       pNameSpace->Release();
       
       return hr;
    }

    // For quick property retrieval, use IWbemObjectAccess.
    IWbemObjectAccess* pAcc = NULL;
    pObj->QueryInterface(IID_IWbemObjectAccess, 
                         (void**) &pAcc );

    // This is not required.
    pObj->Release();

    // Get a property handle for the VirtualBytes property.
    long lVirtualBytesHandle = 0;
    DWORD dwVirtualBytes = 0;

    pAcc->GetPropertyHandle(L"VirtualBytes", 
                            &variant, 
                            &lVirtualBytesHandle );

    // Refresh the object ten times and retrieve the value.
    for( int x = 0; x < 10; x++ )
    {
        pRefresher->Refresh( 0L );
        pAcc->ReadDWORD( lVirtualBytesHandle, &dwVirtualBytes );
        printf( "Process is using %lu bytes\n", dwVirtualBytes );
        // Sleep for a second.
        Sleep( 1000 );
    }
    // Clean up all the objects.
    pAcc->Release();
    // Done with these too.
    pConfig->Release();
    pRefresher->Release();
    pNameSpace->Release();
}
SysFreeString( bstrNameSpace );
pWbemLocator->Release();
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Classi del contatore delle prestazioni](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[Attività WMI: monitoraggio delle prestazioni](wmi-tasks--performance-monitoring.md)
</dt> </dl>

 

 
