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
# <a name="accessing-performance-data-in-c"></a><span data-ttu-id="97798-103">Accesso ai dati sulle prestazioni in C++</span><span class="sxs-lookup"><span data-stu-id="97798-103">Accessing Performance Data in C++</span></span>

<span data-ttu-id="97798-104">L'API WMI a prestazioni elevate è una serie di interfacce che ottengono dati dalle [classi dei contatori delle prestazioni](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span><span class="sxs-lookup"><span data-stu-id="97798-104">The WMI high-performance API is a series of interfaces that obtain data from [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span></span> <span data-ttu-id="97798-105">Queste interfacce richiedono l'uso di un oggetto di [*aggiornamento*](gloss-r.md) per aumentare la frequenza di campionamento.</span><span class="sxs-lookup"><span data-stu-id="97798-105">These interfaces require use of a [*refresher*](gloss-r.md) object to increase the sampling rate.</span></span> <span data-ttu-id="97798-106">Per ulteriori informazioni sull'utilizzo dell'oggetto di aggiornamento nello scripting, vedere [accesso ai dati sulle prestazioni nelle attività script](accessing-performance-data-in-script.md) e [WMI: monitoraggio delle prestazioni](wmi-tasks--performance-monitoring.md).</span><span class="sxs-lookup"><span data-stu-id="97798-106">For more information about using the refresher object in scripting, see [Accessing Performance Data in Script](accessing-performance-data-in-script.md) and [WMI Tasks: Performance Monitoring](wmi-tasks--performance-monitoring.md).</span></span>

<span data-ttu-id="97798-107">Le sezioni seguenti sono illustrate in questo argomento:</span><span class="sxs-lookup"><span data-stu-id="97798-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="97798-108">Aggiornamento dei dati sulle prestazioni</span><span class="sxs-lookup"><span data-stu-id="97798-108">Refreshing Performance Data</span></span>](#refreshing-performance-data)
-   [<span data-ttu-id="97798-109">Aggiunta di enumeratori al nuovo aggiornamento WMI</span><span class="sxs-lookup"><span data-stu-id="97798-109">Adding Enumerators to the WMI Refresher</span></span>](#adding-enumerators-to-the-wmi-refresher)
-   [<span data-ttu-id="97798-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="97798-110">Example</span></span>](#example)
-   [<span data-ttu-id="97798-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="97798-111">Related topics</span></span>](#related-topics)

## <a name="refreshing-performance-data"></a><span data-ttu-id="97798-112">Aggiornamento dei dati sulle prestazioni</span><span class="sxs-lookup"><span data-stu-id="97798-112">Refreshing Performance Data</span></span>

<span data-ttu-id="97798-113">Un oggetto di aggiornamento aumenta le prestazioni del provider di dati e del client recuperando i dati senza superare i limiti del processo.</span><span class="sxs-lookup"><span data-stu-id="97798-113">A refresher object increases data provider and client performance by retrieving data without crossing process boundaries.</span></span> <span data-ttu-id="97798-114">Se il client e il server si trovano nello stesso computer, un aggiornamento carica il provider a prestazioni elevate in-process nel client e copia i dati direttamente dagli oggetti provider in oggetti client.</span><span class="sxs-lookup"><span data-stu-id="97798-114">If both the client and the server are located on the same computer, a refresher loads the high-performance provider in-process to the client, and copies data directly from provider objects into client objects.</span></span> <span data-ttu-id="97798-115">Se il client e il server si trovano in computer diversi, l'aggiornamento aumenta le prestazioni memorizzando nella cache gli oggetti nel computer remoto e trasmettendo al client set di dati minimi.</span><span class="sxs-lookup"><span data-stu-id="97798-115">If the client and the server are located on different computers, the refresher increases performance by caching objects on the remote computer, and transmitting minimal data sets to the client.</span></span>

<span data-ttu-id="97798-116">Un aggiornamento anche:</span><span class="sxs-lookup"><span data-stu-id="97798-116">A refresher also:</span></span>

-   <span data-ttu-id="97798-117">Riconnette automaticamente un client a un servizio WMI remoto quando si verifica un errore di rete o il computer remoto viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="97798-117">Automatically reconnects a client to a remote WMI service when a network error occurs, or the remote computer is restarted.</span></span>

    <span data-ttu-id="97798-118">Per impostazione predefinita, un aggiornamento tenta di riconnettere l'applicazione al provider ad alte prestazioni pertinente quando una connessione remota tra i due computer ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="97798-118">By default, a refresher attempts to reconnect your application to the relevant high-performance provider when a remote connection between the two computers fails.</span></span> <span data-ttu-id="97798-119">Per evitare la riconnessione, passare il **\_ flag WBEM \_ Aggiorna nessun flag di \_ \_ \_ riconnessione automatica** nella chiamata al metodo [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) .</span><span class="sxs-lookup"><span data-stu-id="97798-119">To prevent the reconnection, pass the **WBEM\_FLAG\_REFRESH\_NO\_AUTO\_RECONNECT** flag in the [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) method call.</span></span> <span data-ttu-id="97798-120">Per i client di scripting è necessario impostare la proprietà [**SWbemRefresher. AutoReconnect**](swbemrefresher-autoreconnect.md) su **false**.</span><span class="sxs-lookup"><span data-stu-id="97798-120">Scripting clients must set the [**SWbemRefresher.AutoReconnect**](swbemrefresher-autoreconnect.md) property to **FALSE**.</span></span>

-   <span data-ttu-id="97798-121">Carica più oggetti ed enumeratori forniti dallo stesso provider o da provider diversi.</span><span class="sxs-lookup"><span data-stu-id="97798-121">Loads multiple objects and enumerators that are provided by the same or different providers.</span></span>

    <span data-ttu-id="97798-122">Consente di aggiungere più oggetti, enumeratori o entrambi a un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="97798-122">Allows you to add multiple objects, enumerators, or both to a refresher.</span></span>

-   <span data-ttu-id="97798-123">Enumera gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="97798-123">Enumerates objects.</span></span>

    <span data-ttu-id="97798-124">Analogamente ad altri provider, un provider a prestazioni elevate può enumerare gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="97798-124">Like other providers, a high-performance provider can enumerate objects.</span></span>

<span data-ttu-id="97798-125">Al termine della scrittura del client a prestazioni elevate, potrebbe essere necessario migliorare il tempo di risposta.</span><span class="sxs-lookup"><span data-stu-id="97798-125">After you finish writing your high-performance client, you may want to improve your response time.</span></span> <span data-ttu-id="97798-126">Poiché l'interfaccia [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) è ottimizzata per la velocità, l'interfaccia non è intrinsecamente threadsafe.</span><span class="sxs-lookup"><span data-stu-id="97798-126">Because the [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) interface is optimized for speed, the interface is not intrinsically threadsafe.</span></span> <span data-ttu-id="97798-127">Pertanto, durante un'operazione di aggiornamento, non accedere all'oggetto o all'enumerazione aggiornabile.</span><span class="sxs-lookup"><span data-stu-id="97798-127">Therefore, during a refresh operation, do not access the refreshable object or enumeration.</span></span> <span data-ttu-id="97798-128">Per proteggere gli oggetti tra thread durante le chiamate al metodo **IWbemObjectAccess** , usare i metodi [**IWbemObjectAccess:: Lock**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-lock) e [**Unlock**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-unlock) .</span><span class="sxs-lookup"><span data-stu-id="97798-128">To protect objects across threads during **IWbemObjectAccess** method calls, use the [**IWbemObjectAccess::Lock**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-lock) and [**Unlock**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-unlock) methods.</span></span> <span data-ttu-id="97798-129">Per migliorare le prestazioni, sincronizzare i thread in modo da non dover bloccare i singoli thread.</span><span class="sxs-lookup"><span data-stu-id="97798-129">For improved performance, synchronize your threads so that you do not need to lock individual threads.</span></span> <span data-ttu-id="97798-130">La riduzione dei thread e la sincronizzazione di gruppi di oggetti per le operazioni di aggiornamento offrono le migliori prestazioni complessive.</span><span class="sxs-lookup"><span data-stu-id="97798-130">Reducing threads and synchronizing groups of objects for refresh operations provides the best overall performance.</span></span>

## <a name="adding-enumerators-to-the-wmi-refresher"></a><span data-ttu-id="97798-131">Aggiunta di enumeratori al nuovo aggiornamento WMI</span><span class="sxs-lookup"><span data-stu-id="97798-131">Adding Enumerators to the WMI Refresher</span></span>

<span data-ttu-id="97798-132">Sia il numero di istanze che i dati in ogni istanza vengono aggiornati aggiungendo un enumeratore all'aggiornamento, in modo che ogni chiamata a [**IWbemRefresher:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) comportano un'enumerazione completa.</span><span class="sxs-lookup"><span data-stu-id="97798-132">Both the number of instances and data in each instance are refreshed by adding an enumerator to the refresher so that each call to [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) results in a complete enumeration.</span></span>

<span data-ttu-id="97798-133">Nell'esempio di codice C++ seguente sono necessari i riferimenti seguenti e le \# istruzioni include per la compilazione corretta.</span><span class="sxs-lookup"><span data-stu-id="97798-133">The following C++ code example requires the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM

#include <iostream>
using namespace std;
#include <Wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="97798-134">Nella procedura seguente viene illustrato come aggiungere un enumeratore a un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="97798-134">The following procedure shows how to add an enumerator to a refresher.</span></span>

<span data-ttu-id="97798-135">**Per aggiungere un enumeratore a un aggiornamento**</span><span class="sxs-lookup"><span data-stu-id="97798-135">**To add an enumerator to a refresher**</span></span>

1.  <span data-ttu-id="97798-136">Chiamare il metodo [**IWbemConfigureRefresher:: AddEnum**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addenum) usando il percorso dell'oggetto aggiornabile e l'interfaccia [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="97798-136">Call the [**IWbemConfigureRefresher::AddEnum**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addenum) method using the path to the refreshable object and the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface.</span></span>

    <span data-ttu-id="97798-137">L'aggiornamento restituisce un puntatore a un'interfaccia [**IWbemHiPerfEnum**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemhiperfenum) .</span><span class="sxs-lookup"><span data-stu-id="97798-137">The refresher returns a pointer to an [**IWbemHiPerfEnum**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemhiperfenum) interface.</span></span> <span data-ttu-id="97798-138">Per accedere agli oggetti nell'enumerazione, è possibile usare l'interfaccia **IWbemHiPerfEnum** .</span><span class="sxs-lookup"><span data-stu-id="97798-138">You can use the **IWbemHiPerfEnum** interface to access the objects in the enumeration.</span></span>

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

    

2.  <span data-ttu-id="97798-139">Creare un ciclo che esegua le azioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="97798-139">Create a loop that performs the following actions:</span></span>

    -   <span data-ttu-id="97798-140">Aggiorna l'oggetto tramite una chiamata a [**IWbemRefresher:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh).</span><span class="sxs-lookup"><span data-stu-id="97798-140">Refreshes the object by using a call to [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh).</span></span>
    -   <span data-ttu-id="97798-141">Fornisce una matrice di puntatori dell'interfaccia [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) al metodo [**IWbemHiPerfEnum:: GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects) .</span><span class="sxs-lookup"><span data-stu-id="97798-141">Provides an array of [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) interface pointers to the [**IWbemHiPerfEnum::GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects) method.</span></span>
    -   <span data-ttu-id="97798-142">Accede alle proprietà dell'enumeratore usando i metodi [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) passati in [**GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects).</span><span class="sxs-lookup"><span data-stu-id="97798-142">Accesses the properties of the enumerator by using the [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) methods passed into [**GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects).</span></span>

        <span data-ttu-id="97798-143">È possibile passare un handle di proprietà a ogni istanza di [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) per recuperare il valore aggiornato.</span><span class="sxs-lookup"><span data-stu-id="97798-143">A property handle can be passed to each [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) instance to retrieve the refreshed value.</span></span> <span data-ttu-id="97798-144">Il client deve chiamare [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) per rilasciare i puntatori **IWbemObjectAccess** restituiti da [**GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects).</span><span class="sxs-lookup"><span data-stu-id="97798-144">The client must call [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) to release the **IWbemObjectAccess** pointers returned by [**GetObjects**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects).</span></span>

## <a name="example"></a><span data-ttu-id="97798-145">Esempio</span><span class="sxs-lookup"><span data-stu-id="97798-145">Example</span></span>

<span data-ttu-id="97798-146">Nell'esempio di codice C++ riportato di seguito viene enumerata una classe a prestazioni elevate, in cui il client recupera un handle di proprietà dal primo oggetto e riutilizza l'handle per il resto dell'operazione di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="97798-146">The following C++ code example enumerates a high-performance class, where the client retrieves a property handle from the first object, and reuses the handle for the remainder of the refresh operation.</span></span> <span data-ttu-id="97798-147">Ogni chiamata al metodo [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) aggiorna il numero di istanze e i dati dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="97798-147">Each call to the [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) method updates the number of instances and the instance data.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="97798-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="97798-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97798-149">Classi del contatore delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="97798-149">Performance Counter Classes</span></span>](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[<span data-ttu-id="97798-150">Accesso ai dati sulle prestazioni nello script</span><span class="sxs-lookup"><span data-stu-id="97798-150">Accessing Performance Data in Script</span></span>](accessing-performance-data-in-script.md)
</dt> <dt>

[<span data-ttu-id="97798-151">Aggiornamento dei dati WMI negli script</span><span class="sxs-lookup"><span data-stu-id="97798-151">Refreshing WMI Data in Scripts</span></span>](refreshing-wmi-data-in-scripts.md)
</dt> <dt>

[<span data-ttu-id="97798-152">Attività WMI: monitoraggio delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="97798-152">WMI Tasks: Performance Monitoring</span></span>](wmi-tasks--performance-monitoring.md)
</dt> <dt>

[<span data-ttu-id="97798-153">Monitoraggio dei dati sulle prestazioni</span><span class="sxs-lookup"><span data-stu-id="97798-153">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> <dt>

[<span data-ttu-id="97798-154">Qualificatori di proprietà per le classi del contatore delle prestazioni formattate</span><span class="sxs-lookup"><span data-stu-id="97798-154">Property Qualifiers for Formatted Performance Counter Classes</span></span>](property-qualifiers-for-performance-counter-classes.md)
</dt> <dt>

[<span data-ttu-id="97798-155">Tipi di contatori delle prestazioni WMI</span><span class="sxs-lookup"><span data-stu-id="97798-155">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> <dt>

[<span data-ttu-id="97798-156">**Wmiadap.exe**</span><span class="sxs-lookup"><span data-stu-id="97798-156">**Wmiadap.exe**</span></span>](wmiadap.md)
</dt> <dt>

[<span data-ttu-id="97798-157">**QueryPerformanceCounter**</span><span class="sxs-lookup"><span data-stu-id="97798-157">**QueryPerformanceCounter**</span></span>](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)
</dt> </dl>

 

 
