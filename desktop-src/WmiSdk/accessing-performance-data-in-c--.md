---
description: L'API WMI a prestazioni elevate è una serie di interfacce che ottengono dati dalle classi dei contatori delle prestazioni.
ms.assetid: ee0a2ead-f53a-4651-a287-04a62eba3f84
ms.tgt_platform: multiple
title: Accesso ai dati sulle prestazioni in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b076e1ab15b934f347ee491711d7d3d1b8fbbe0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319312"
---
# <a name="accessing-performance-data-in-c"></a>Accesso ai dati sulle prestazioni in C++

L'API WMI a prestazioni elevate è una serie di interfacce che ottengono dati dalle [classi dei contatori delle prestazioni](/windows/desktop/CIMWin32Prov/performance-counter-classes). Queste interfacce richiedono l'uso di un oggetto di [*aggiornamento*](gloss-r.md) per aumentare la frequenza di campionamento. Per ulteriori informazioni sull'utilizzo dell'oggetto di aggiornamento nello scripting, vedere [accesso ai dati sulle prestazioni nelle attività script](accessing-performance-data-in-script.md) e [WMI: monitoraggio delle prestazioni](wmi-tasks--performance-monitoring.md).

Le sezioni seguenti sono illustrate in questo argomento:

-   [Aggiornamento dei dati sulle prestazioni](#refreshing-performance-data)
-   [Aggiunta di enumeratori al nuovo aggiornamento WMI](#adding-enumerators-to-the-wmi-refresher)
-   [Esempio](#example)
-   [Argomenti correlati](#related-topics)

## <a name="refreshing-performance-data"></a>Aggiornamento dei dati sulle prestazioni

Un oggetto di aggiornamento aumenta le prestazioni del provider di dati e del client recuperando i dati senza superare i limiti del processo. Se il client e il server si trovano nello stesso computer, un aggiornamento carica il provider a prestazioni elevate in-process nel client e copia i dati direttamente dagli oggetti provider in oggetti client. Se il client e il server si trovano in computer diversi, l'aggiornamento aumenta le prestazioni memorizzando nella cache gli oggetti nel computer remoto e trasmettendo al client set di dati minimi.

Un aggiornamento anche:

-   Riconnette automaticamente un client a un servizio WMI remoto quando si verifica un errore di rete o il computer remoto viene riavviato.

    Per impostazione predefinita, un aggiornamento tenta di riconnettere l'applicazione al provider ad alte prestazioni pertinente quando una connessione remota tra i due computer ha esito negativo. Per evitare la riconnessione, passare il **\_ flag WBEM \_ Aggiorna nessun flag di \_ \_ \_ riconnessione automatica** nella chiamata al metodo [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) . Per i client di scripting è necessario impostare la proprietà [**SWbemRefresher. AutoReconnect**](swbemrefresher-autoreconnect.md) su **false**.

-   Carica più oggetti ed enumeratori forniti dallo stesso provider o da provider diversi.

    Consente di aggiungere più oggetti, enumeratori o entrambi a un aggiornamento.

-   Enumera gli oggetti.

    Analogamente ad altri provider, un provider a prestazioni elevate può enumerare gli oggetti.

Al termine della scrittura del client a prestazioni elevate, potrebbe essere necessario migliorare il tempo di risposta. Poiché l'interfaccia [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) è ottimizzata per la velocità, l'interfaccia non è intrinsecamente threadsafe. Pertanto, durante un'operazione di aggiornamento, non accedere all'oggetto o all'enumerazione aggiornabile. Per proteggere gli oggetti tra thread durante le chiamate al metodo **IWbemObjectAccess** , usare i metodi [**IWbemObjectAccess:: Lock**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-lock) e [**Unlock**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-unlock) . Per migliorare le prestazioni, sincronizzare i thread in modo da non dover bloccare i singoli thread. La riduzione dei thread e la sincronizzazione di gruppi di oggetti per le operazioni di aggiornamento offrono le migliori prestazioni complessive.

## <a name="adding-enumerators-to-the-wmi-refresher"></a>Aggiunta di enumeratori al nuovo aggiornamento WMI

Sia il numero di istanze che i dati in ogni istanza vengono aggiornati aggiungendo un enumeratore all'aggiornamento, in modo che ogni chiamata a [**IWbemRefresher:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) comportano un'enumerazione completa.

Nell'esempio di codice C++ seguente sono necessari i riferimenti seguenti e le \# istruzioni include per la compilazione corretta.


```C++
#define _WIN32_DCOM

#include <iostream>
using namespace std;
#include <Wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



Nella procedura seguente viene illustrato come aggiungere un enumeratore a un aggiornamento.

**Per aggiungere un enumeratore a un aggiornamento**

1.  Chiamare il metodo [**IWbemConfigureRefresher:: AddEnum**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addenum) usando il percorso dell'oggetto aggiornabile e l'interfaccia [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .

    L'aggiornamento restituisce un puntatore a un'interfaccia [**IWbemHiPerfEnum**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemhiperfenum) . Per accedere agli oggetti nell'enumerazione, è possibile usare l'interfaccia **IWbemHiPerfEnum** .

    ```C++
    IWbemHiPerfEnum* pEnum = NULL;
    long lID;
    IWbemConfigureRefresher* pConfig;
    IWbemServices* pNameSpace;

    // Add an enumerator to the refresher.
    if (FAILED (hr = pConfig->AddEnum(
        pNameSpace, 
        L"Win32_PerfRawData_PerfProc_Process", 
        0, 
        NULL,
        &pEnum, 
        &lID)))
    {
        goto CLEANUP;
    }
    pConfig->Release();
    pConfig = NULL;
    ```

    

2.  Creare un ciclo che esegua le azioni seguenti:

    -   Aggiorna l'oggetto tramite una chiamata a [**IWbemRefresher:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh).
    -   Fornisce una matrice di puntatori dell'interfaccia [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) al metodo [**IWbemHiPerfEnum:: GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects) .
    -   Accede alle proprietà dell'enumeratore usando i metodi [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) passati in [**GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects).

        È possibile passare un handle di proprietà a ogni istanza di [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) per recuperare il valore aggiornato. Il client deve chiamare [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) per rilasciare i puntatori **IWbemObjectAccess** restituiti da [**GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects).

## <a name="example"></a>Esempio

Nell'esempio di codice C++ riportato di seguito viene enumerata una classe a prestazioni elevate, in cui il client recupera un handle di proprietà dal primo oggetto e riutilizza l'handle per il resto dell'operazione di aggiornamento. Ogni chiamata al metodo [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) aggiorna il numero di istanze e i dati dell'istanza.


```C++
#define _WIN32_DCOM

#include <iostream>
using namespace std;
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")

int __cdecl wmain(int argc, wchar_t* argv[])
{
    // To add error checking,
    // check returned HRESULT below where collected.
    HRESULT                 hr = S_OK;
    IWbemRefresher          *pRefresher = NULL;
    IWbemConfigureRefresher *pConfig = NULL;
    IWbemHiPerfEnum         *pEnum = NULL;
    IWbemServices           *pNameSpace = NULL;
    IWbemLocator            *pWbemLocator = NULL;
    IWbemObjectAccess       **apEnumAccess = NULL;
    BSTR                    bstrNameSpace = NULL;
    long                    lID = 0;
    long                    lVirtualBytesHandle = 0;
    long                    lIDProcessHandle = 0;
    DWORD                   dwVirtualBytes = 0;
    DWORD                   dwProcessId = 0;
    DWORD                   dwNumObjects = 0;
    DWORD                   dwNumReturned = 0;
    DWORD                   dwIDProcess = 0;
    DWORD                   i=0;
    int                     x=0;

    if (FAILED (hr = CoInitializeEx(NULL,COINIT_MULTITHREADED)))
    {
        goto CLEANUP;
    }

    if (FAILED (hr = CoInitializeSecurity(
        NULL,
        -1,
        NULL,
        NULL,
        RPC_C_AUTHN_LEVEL_NONE,
        RPC_C_IMP_LEVEL_IMPERSONATE,
        NULL, EOAC_NONE, 0)))
    {
        goto CLEANUP;
    }

    if (FAILED (hr = CoCreateInstance(
        CLSID_WbemLocator, 
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_IWbemLocator,
        (void**) &pWbemLocator)))
    {
        goto CLEANUP;
    }

    // Connect to the desired namespace.
    bstrNameSpace = SysAllocString(L"\\\\.\\root\\cimv2");
    if (NULL == bstrNameSpace)
    {
        hr = E_OUTOFMEMORY;
        goto CLEANUP;
    }
    if (FAILED (hr = pWbemLocator->ConnectServer(
        bstrNameSpace,
        NULL, // User name
        NULL, // Password
        NULL, // Locale
        0L,   // Security flags
        NULL, // Authority
        NULL, // Wbem context
        &pNameSpace)))
    {
        goto CLEANUP;
    }
    pWbemLocator->Release();
    pWbemLocator=NULL;
    SysFreeString(bstrNameSpace);
    bstrNameSpace = NULL;

    if (FAILED (hr = CoCreateInstance(
        CLSID_WbemRefresher,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_IWbemRefresher, 
        (void**) &pRefresher)))
    {
        goto CLEANUP;
    }

    if (FAILED (hr = pRefresher->QueryInterface(
        IID_IWbemConfigureRefresher,
        (void **)&pConfig)))
    {
        goto CLEANUP;
    }

    // Add an enumerator to the refresher.
    if (FAILED (hr = pConfig->AddEnum(
        pNameSpace, 
        L"Win32_PerfRawData_PerfProc_Process", 
        0, 
        NULL, 
        &pEnum, 
        &lID)))
    {
        goto CLEANUP;
    }
    pConfig->Release();
    pConfig = NULL;

    // Get a property handle for the VirtualBytes property.

    // Refresh the object ten times and retrieve the value.
    for(x = 0; x < 10; x++)
    {
        dwNumReturned = 0;
        dwIDProcess = 0;
        dwNumObjects = 0;

        if (FAILED (hr =pRefresher->Refresh(0L)))
        {
            goto CLEANUP;
        }

        hr = pEnum->GetObjects(0L, 
            dwNumObjects, 
            apEnumAccess, 
            &dwNumReturned);
        // If the buffer was not big enough,
        // allocate a bigger buffer and retry.
        if (hr == WBEM_E_BUFFER_TOO_SMALL 
            && dwNumReturned > dwNumObjects)
        {
            apEnumAccess = new IWbemObjectAccess*[dwNumReturned];
            if (NULL == apEnumAccess)
            {
                hr = E_OUTOFMEMORY;
                goto CLEANUP;
            }
            SecureZeroMemory(apEnumAccess,
                dwNumReturned*sizeof(IWbemObjectAccess*));
            dwNumObjects = dwNumReturned;

            if (FAILED (hr = pEnum->GetObjects(0L, 
                dwNumObjects, 
                apEnumAccess, 
                &dwNumReturned)))
            {
                goto CLEANUP;
            }
        }
        else
        {
            if (hr == WBEM_S_NO_ERROR)
            {
                hr = WBEM_E_NOT_FOUND;
                goto CLEANUP;
            }
        }

        // First time through, get the handles.
        if (0 == x)
        {
            CIMTYPE VirtualBytesType;
            CIMTYPE ProcessHandleType;
            if (FAILED (hr = apEnumAccess[0]->GetPropertyHandle(
                L"VirtualBytes",
                &VirtualBytesType,
                &lVirtualBytesHandle)))
            {
                goto CLEANUP;
            }
            if (FAILED (hr = apEnumAccess[0]->GetPropertyHandle(
                L"IDProcess",
                &ProcessHandleType,
                &lIDProcessHandle)))
            {
                goto CLEANUP;
            }
        }
           
        for (i = 0; i < dwNumReturned; i++)
        {
            if (FAILED (hr = apEnumAccess[i]->ReadDWORD(
                lVirtualBytesHandle,
                &dwVirtualBytes)))
            {
                goto CLEANUP;
            }
            if (FAILED (hr = apEnumAccess[i]->ReadDWORD(
                lIDProcessHandle,
                &dwIDProcess)))
            {
                goto CLEANUP;
            }

            wprintf(L"Process ID %lu is using %lu bytes\n",
                dwIDProcess, dwVirtualBytes);

            // Done with the object
            apEnumAccess[i]->Release();
            apEnumAccess[i] = NULL;
        }

        if (NULL != apEnumAccess)
        {
            delete [] apEnumAccess;
            apEnumAccess = NULL;
        }

       // Sleep for a second.
       Sleep(1000);
    }
    // exit loop here
    CLEANUP:

    if (NULL != bstrNameSpace)
    {
        SysFreeString(bstrNameSpace);
    }

    if (NULL != apEnumAccess)
    {
        for (i = 0; i < dwNumReturned; i++)
        {
            if (apEnumAccess[i] != NULL)
            {
                apEnumAccess[i]->Release();
                apEnumAccess[i] = NULL;
            }
        }
        delete [] apEnumAccess;
    }
    if (NULL != pWbemLocator)
    {
        pWbemLocator->Release();
    }
    if (NULL != pNameSpace)
    {
        pNameSpace->Release();
    }
    if (NULL != pEnum)
    {
        pEnum->Release();
    }
    if (NULL != pConfig)
    {
        pConfig->Release();
    }
    if (NULL != pRefresher)
    {
        pRefresher->Release();
    }

    CoUninitialize();

    if (FAILED (hr))
    {
        wprintf (L"Error status=%08x\n",hr);
    }

    return 1;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Classi del contatore delle prestazioni](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[Accesso ai dati sulle prestazioni nello script](accessing-performance-data-in-script.md)
</dt> <dt>

[Aggiornamento dei dati WMI negli script](refreshing-wmi-data-in-scripts.md)
</dt> <dt>

[Attività WMI: monitoraggio delle prestazioni](wmi-tasks--performance-monitoring.md)
</dt> <dt>

[Monitoraggio dei dati sulle prestazioni](monitoring-performance-data.md)
</dt> <dt>

[Qualificatori di proprietà per le classi del contatore delle prestazioni formattate](property-qualifiers-for-performance-counter-classes.md)
</dt> <dt>

[Tipi di contatori delle prestazioni WMI](wmi-performance-counter-types.md)
</dt> <dt>

[**Wmiadap.exe**](wmiadap.md)
</dt> <dt>

[**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)
</dt> </dl>

 

 
