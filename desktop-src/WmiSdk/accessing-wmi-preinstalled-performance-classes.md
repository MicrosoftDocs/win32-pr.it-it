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
# <a name="accessing-wmi-preinstalled-performance-classes"></a><span data-ttu-id="07f12-103">Accesso alle classi di prestazioni preinstallate WMI</span><span class="sxs-lookup"><span data-stu-id="07f12-103">Accessing WMI Preinstalled Performance Classes</span></span>

<span data-ttu-id="07f12-104">Il repository WMI contiene classi di prestazioni preinstallate per tutti gli oggetti della libreria delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="07f12-104">The WMI repository contains preinstalled performance classes for all the performance library objects.</span></span> <span data-ttu-id="07f12-105">Ad esempio, le istanze della classe prestazioni dati non elaborati [**Win32 \_ PerfRawData \_ PerfProc \_ processo**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) rappresentano i processi.</span><span class="sxs-lookup"><span data-stu-id="07f12-105">For example, instances of the raw data performance class [**Win32\_PerfRawData\_PerfProc\_Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) represent processes.</span></span> <span data-ttu-id="07f12-106">Questo oggetto prestazione è visibile in monitoraggio di sistema come oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="07f12-106">This performance object is visible in System Monitor as the Process object.</span></span>

<span data-ttu-id="07f12-107">La proprietà **PageFaultsPerSec** del [**\_ \_ \_ processo Win32 PerfRawData PerfProc**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) rappresenta il contatore delle prestazioni errori di pagina al secondo per il processo.</span><span class="sxs-lookup"><span data-stu-id="07f12-107">The **PageFaultsPerSec** property of [**Win32\_PerfRawData\_PerfProc\_Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) represents the Page Faults per second performance counter for the process.</span></span> <span data-ttu-id="07f12-108">Le classi [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) contengono i valori dei dati calcolati visualizzati in Monitor di sistema (Perfmon.exe).</span><span class="sxs-lookup"><span data-stu-id="07f12-108">The [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) classes contain the calculated data values displayed in System Monitor (Perfmon.exe).</span></span> <span data-ttu-id="07f12-109">Il valore della proprietà **PageFaultsPerSec** del [**processo Win32 \_ PerfFormattedData \_ PerfProc \_**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) è uguale a quello visualizzato in Monitor di sistema.</span><span class="sxs-lookup"><span data-stu-id="07f12-109">The value of the **PageFaultsPerSec** property of [**Win32\_PerfFormattedData\_PerfProc\_Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) is the same as when it appears in System Monitor.</span></span>

<span data-ttu-id="07f12-110">Utilizzare l' [API com per WMI](com-api-for-wmi.md) o l' [API di scripting per WMI](scripting-api-for-wmi.md) per accedere ai dati sulle prestazioni tramite le [classi del contatore delle prestazioni](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span><span class="sxs-lookup"><span data-stu-id="07f12-110">Use either the [COM API for WMI](com-api-for-wmi.md) or the [Scripting API for WMI](scripting-api-for-wmi.md) to access performance data through the [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span></span> <span data-ttu-id="07f12-111">In entrambi i casi è necessario un oggetto di [*aggiornamento*](gloss-r.md) per ottenere ogni campione di dati.</span><span class="sxs-lookup"><span data-stu-id="07f12-111">In both cases a [*refresher*](gloss-r.md) object is required to obtain each data sample.</span></span> <span data-ttu-id="07f12-112">Per ulteriori informazioni ed esempi di codice di script per l'utilizzo di aggiornamenti e per l'accesso alle classi di prestazioni, vedere [attività WMI: monitoraggio delle prestazioni](wmi-tasks--performance-monitoring.md).</span><span class="sxs-lookup"><span data-stu-id="07f12-112">For more information and script code examples for using refreshers and accessing performance classes, see [WMI Tasks: Performance Monitoring](wmi-tasks--performance-monitoring.md).</span></span> <span data-ttu-id="07f12-113">Per ulteriori informazioni, vedere [accesso ai dati sulle prestazioni nello script](accessing-performance-data-in-script.md).</span><span class="sxs-lookup"><span data-stu-id="07f12-113">For more information, see [Accessing Performance Data in Script](accessing-performance-data-in-script.md).</span></span>

## <a name="accessing-performance-data-from-c"></a><span data-ttu-id="07f12-114">Accesso ai dati sulle prestazioni da C++</span><span class="sxs-lookup"><span data-stu-id="07f12-114">Accessing Performance Data from C++</span></span>

<span data-ttu-id="07f12-115">Nell'esempio di codice C++ riportato di seguito viene utilizzato il provider del contatore delle prestazioni per accedere alle classi a prestazioni elevate predefinite.</span><span class="sxs-lookup"><span data-stu-id="07f12-115">The following C++ code example uses the Performance Counter provider to access predefined high-performance classes.</span></span> <span data-ttu-id="07f12-116">Viene creato un oggetto di aggiornamento e viene aggiunto un oggetto al nuovo aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="07f12-116">It creates a refresher object and adds an object to the refresher.</span></span> <span data-ttu-id="07f12-117">L'oggetto è un'istanza del [**\_ \_ \_ processo PerfProc Win32 PerfRawData**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) che monitora le prestazioni di un processo specifico.</span><span class="sxs-lookup"><span data-stu-id="07f12-117">The object is a [**Win32\_PerfRawData\_PerfProc\_Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) instance that monitors the performance of a specific process.</span></span> <span data-ttu-id="07f12-118">Il codice legge solo una proprietà del contatore nell'oggetto processo, ovvero la proprietà **byte virtuali** .</span><span class="sxs-lookup"><span data-stu-id="07f12-118">The code only reads one counter property in the process object, the **VirtualBytes** property.</span></span> <span data-ttu-id="07f12-119">Il codice richiede i riferimenti seguenti e le istruzioni **\# include** per la compilazione corretta.</span><span class="sxs-lookup"><span data-stu-id="07f12-119">The code requires the following references and **\#include** statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="07f12-120">Nella procedura seguente viene illustrato come accedere ai dati da un provider a prestazioni elevate in C++.</span><span class="sxs-lookup"><span data-stu-id="07f12-120">The following procedure shows how to access data from a high-performance provider in C++.</span></span>

<span data-ttu-id="07f12-121">**Per accedere ai dati da un provider a prestazioni elevate in C++**</span><span class="sxs-lookup"><span data-stu-id="07f12-121">**To access data from a high-performance provider in C++**</span></span>

1.  <span data-ttu-id="07f12-122">Stabilire una connessione allo spazio dei nomi WMI e impostare la sicurezza WMI utilizzando una chiamata a [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) e [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="07f12-122">Establish a connection to the WMI namespace, and set WMI security by using a call to [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) and [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

    <span data-ttu-id="07f12-123">Questo passaggio è un passaggio standard per la creazione di qualsiasi applicazione client WMI.</span><span class="sxs-lookup"><span data-stu-id="07f12-123">This step is a standard step for creating any WMI client application.</span></span> <span data-ttu-id="07f12-124">Per ulteriori informazioni, vedere [creazione di un'applicazione WMI con C++](creating-a-wmi-application-using-c-.md).</span><span class="sxs-lookup"><span data-stu-id="07f12-124">For more information, see [Creating a WMI Application Using C++](creating-a-wmi-application-using-c-.md).</span></span>

2.  <span data-ttu-id="07f12-125">Creare un oggetto di aggiornamento utilizzando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con CLSID \_ WbemRefresher.</span><span class="sxs-lookup"><span data-stu-id="07f12-125">Create a refresher object by using [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with CLSID\_WbemRefresher.</span></span> <span data-ttu-id="07f12-126">Richiedere un'interfaccia [**IWbemConfigureRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemconfigurerefresher) tramite il metodo [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) .</span><span class="sxs-lookup"><span data-stu-id="07f12-126">Request an [**IWbemConfigureRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemconfigurerefresher) interface through the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method.</span></span> <span data-ttu-id="07f12-127">Richiedere un'interfaccia [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) tramite il metodo **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="07f12-127">Request an [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) interface through the **QueryInterface** method.</span></span>

    <span data-ttu-id="07f12-128">L'interfaccia [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) è l'interfaccia principale per l'oggetto di [**aggiornamento**](swbemrefreshableitem-refresher.md) WMI.</span><span class="sxs-lookup"><span data-stu-id="07f12-128">The [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) interface is the main interface for the WMI [**Refresher**](swbemrefreshableitem-refresher.md) object.</span></span>

    <span data-ttu-id="07f12-129">Nell'esempio di codice C++ riportato di seguito viene illustrato come recuperare [**IWbemConfigureRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher).</span><span class="sxs-lookup"><span data-stu-id="07f12-129">The following C++ code example shows how to retrieve [**IWbemConfigureRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher).</span></span>

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

    

3.  <span data-ttu-id="07f12-130">Aggiungere un oggetto all'aggiornamento tramite una chiamata al metodo [**IWbemConfigureRefresher:: AddObjectByPath**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath) .</span><span class="sxs-lookup"><span data-stu-id="07f12-130">Add an object to the refresher through a call to the [**IWbemConfigureRefresher::AddObjectByPath**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath) method.</span></span>

    <span data-ttu-id="07f12-131">Quando si aggiunge un oggetto all'aggiornamento, WMI aggiorna l'oggetto ogni volta che si chiama il metodo [**IWbemRefresher:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) .</span><span class="sxs-lookup"><span data-stu-id="07f12-131">When you add an object to the refresher, WMI refreshes the object whenever you call the [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) method.</span></span> <span data-ttu-id="07f12-132">L'oggetto aggiunto designa il provider nei qualificatori di classe.</span><span class="sxs-lookup"><span data-stu-id="07f12-132">The object you add designates the provider in its class qualifiers.</span></span>

    <span data-ttu-id="07f12-133">Nell'esempio di codice C++ riportato di seguito viene illustrato come chiamare [**AddObjectByPath**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath).</span><span class="sxs-lookup"><span data-stu-id="07f12-133">The following C++ code example shows how to call [**AddObjectByPath**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath).</span></span>

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

    

4.  <span data-ttu-id="07f12-134">Per configurare un accesso più rapido all'oggetto, connettersi all'interfaccia [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) tramite [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sull'interfaccia [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) .</span><span class="sxs-lookup"><span data-stu-id="07f12-134">To set up faster access to the object, connect to the [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) interface through [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) interface.</span></span>

    <span data-ttu-id="07f12-135">Nell'esempio di codice C++ riportato di seguito viene illustrato come recuperare un puntatore all'oggetto utilizzando [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) anziché [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject).</span><span class="sxs-lookup"><span data-stu-id="07f12-135">The following C++ code example shows how to retrieve a pointer to the object using [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) instead of [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject).</span></span>

    ```C++
        // For quick property retrieval, use IWbemObjectAccess.
        IWbemObjectAccess* pAcc = NULL;
        pObj->QueryInterface( IID_IWbemObjectAccess, (void**) &pAcc );
        // This is not required.
        pObj->Release();
    ```

    

    <span data-ttu-id="07f12-136">L'interfaccia [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) consente di aumentare le prestazioni in quanto è possibile ottenere handle per specifiche proprietà dei contatori ed è necessario bloccare e sbloccare l'oggetto nel codice, ovvero un'operazione eseguita da [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) per ogni accesso alla proprietà.</span><span class="sxs-lookup"><span data-stu-id="07f12-136">The [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) interface increases performance because you can get handles to specific counter properties, and it requires that you lock and unlock the object in your code, which is an operation that [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) performs for each property access.</span></span>

5.  <span data-ttu-id="07f12-137">Ottenere gli handle delle proprietà da esaminare usando le chiamate al metodo [**IWbemObjectAccess:: GetPropertyHandle**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-getpropertyhandle) .</span><span class="sxs-lookup"><span data-stu-id="07f12-137">Obtain the handles of the properties to examine by using calls to the [**IWbemObjectAccess::GetPropertyHandle**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectaccess-getpropertyhandle) method.</span></span>

    <span data-ttu-id="07f12-138">Gli handle di proprietà sono gli stessi per tutte le istanze di una classe, il che significa che usa l'handle di proprietà recuperato da un'istanza specifica per tutte le istanze di una classe specifica.</span><span class="sxs-lookup"><span data-stu-id="07f12-138">Property handles are the same for all instances of a class, which means that use the property handle you retrieve from a specific instance for all instances of a specific class.</span></span> <span data-ttu-id="07f12-139">È anche possibile ottenere un handle da un oggetto classe per recuperare i valori delle proprietà da un oggetto istanza.</span><span class="sxs-lookup"><span data-stu-id="07f12-139">You can also obtain a handle from a class object to retrieve property values from an instance object.</span></span>

    <span data-ttu-id="07f12-140">Nell'esempio di codice C++ riportato di seguito viene illustrato come recuperare un handle di proprietà.</span><span class="sxs-lookup"><span data-stu-id="07f12-140">The following C++ code example shows how to retrieve a property handle.</span></span>

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

    

6.  <span data-ttu-id="07f12-141">Creare un ciclo di programmazione che esegua le azioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="07f12-141">Create a programming loop that performs the following actions:</span></span>

    -   <span data-ttu-id="07f12-142">Aggiornare l'oggetto con una chiamata a [**IWbemRefresher:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) utilizzando il puntatore creato nella precedente chiamata a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="07f12-142">Refresh the object with a call to [**IWbemRefresher::Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) by using the pointer created in the previous call to [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

        <span data-ttu-id="07f12-143">In questa chiamata, l'aggiornamento WMI aggiorna l'oggetto client usando i dati forniti dal provider.</span><span class="sxs-lookup"><span data-stu-id="07f12-143">In this call, the WMI Refresher refreshes the client object by using data that the provider supplies.</span></span>

    -   <span data-ttu-id="07f12-144">Eseguire tutte le azioni necessarie per l'oggetto, ad esempio il recupero di un nome di proprietà, di un tipo di dati o di un valore.</span><span class="sxs-lookup"><span data-stu-id="07f12-144">Perform any action as necessary on the object, such as retrieving a property name, data type, or value.</span></span>

        <span data-ttu-id="07f12-145">È possibile accedere alla proprietà tramite l'handle di proprietà ottenuto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="07f12-145">You can access the property through the property handle obtained earlier.</span></span> <span data-ttu-id="07f12-146">A causa della chiamata di [**aggiornamento**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) , WMI aggiorna la proprietà ogni volta nel ciclo.</span><span class="sxs-lookup"><span data-stu-id="07f12-146">Due to the [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) call, WMI refreshes the property each time through the loop.</span></span>

<span data-ttu-id="07f12-147">Nell'esempio C++ riportato di seguito viene illustrato come utilizzare l'API WMI a prestazioni elevate.</span><span class="sxs-lookup"><span data-stu-id="07f12-147">The following C++ example shows how to use the WMI high-performance API.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="07f12-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="07f12-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07f12-149">Classi del contatore delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="07f12-149">Performance Counter Classes</span></span>](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[<span data-ttu-id="07f12-150">Attività WMI: monitoraggio delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="07f12-150">WMI Tasks: Performance Monitoring</span></span>](wmi-tasks--performance-monitoring.md)
</dt> </dl>

 

 
