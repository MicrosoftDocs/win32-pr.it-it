---
title: Ciclo di vita dell'istanza di virtualizzazione
description: Panoramica del ciclo di vita di un'istanza di virtualizzazione ProjFS.
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/17/2018
ms.topic: article
ms.openlocfilehash: 567eff1f7b8acf330dba7c652e2e12b724072b9b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516852"
---
# <a name="virtualization-instance-lifecycle"></a><span data-ttu-id="364c5-103">Ciclo di vita dell'istanza di virtualizzazione</span><span class="sxs-lookup"><span data-stu-id="364c5-103">Virtualization Instance Lifecycle</span></span>

<span data-ttu-id="364c5-104">L'applicazione provider gestisce una o più istanze di virtualizzazione.</span><span class="sxs-lookup"><span data-stu-id="364c5-104">The provider application maintains one or more virtualization instances.</span></span>  <span data-ttu-id="364c5-105">Ogni istanza di virtualizzazione passa attraverso quattro fasi del ciclo di vita:</span><span class="sxs-lookup"><span data-stu-id="364c5-105">Each virtualization instance goes through four stages in its lifecycle:</span></span>

1. <span data-ttu-id="364c5-106">Creazione</span><span class="sxs-lookup"><span data-stu-id="364c5-106">Creation</span></span>
2. <span data-ttu-id="364c5-107">Avvio</span><span class="sxs-lookup"><span data-stu-id="364c5-107">Startup</span></span>
3. <span data-ttu-id="364c5-108">Runtime</span><span class="sxs-lookup"><span data-stu-id="364c5-108">Runtime</span></span>
4. <span data-ttu-id="364c5-109">Arresta</span><span class="sxs-lookup"><span data-stu-id="364c5-109">Shutdown</span></span>

<span data-ttu-id="364c5-110">Si noti che dopo l'arresto di un'istanza di virtualizzazione, il provider non deve ricrearlo per riutilizzarlo.</span><span class="sxs-lookup"><span data-stu-id="364c5-110">Note that after shutting down a virtualization instance the provider does not need to re-create it to reuse it.</span></span>  <span data-ttu-id="364c5-111">Può semplicemente riavviarlo.</span><span class="sxs-lookup"><span data-stu-id="364c5-111">It can simply start it up again.</span></span>

> <span data-ttu-id="364c5-112">**Nota**: in questa sezione vengono illustrati esempi di API ProjFS.</span><span class="sxs-lookup"><span data-stu-id="364c5-112">**Note**: This section shows examples of ProjFS APIs.</span></span>  <span data-ttu-id="364c5-113">Ogni esempio ha lo scopo di illustrare l'utilizzo delle API di base.</span><span class="sxs-lookup"><span data-stu-id="364c5-113">Each example is meant to illustrate basic API usage.</span></span>  <span data-ttu-id="364c5-114">Per la documentazione delle opzioni non usate in questi esempi, vedere le informazioni di [riferimento sull'API ProjFS](/windows/desktop/api/_projfs).</span><span class="sxs-lookup"><span data-stu-id="364c5-114">For documentation of options unused in these examples please consult the [ProjFS API reference](/windows/desktop/api/_projfs).</span></span>

## <a name="creating-a-virtualization-root"></a><span data-ttu-id="364c5-115">Creazione di una radice di virtualizzazione</span><span class="sxs-lookup"><span data-stu-id="364c5-115">Creating a virtualization root</span></span>

<span data-ttu-id="364c5-116">Prima che un provider possa avviare l'istanza di virtualizzazione che proietta gli elementi nel file system locale, deve creare la radice di virtualizzazione.</span><span class="sxs-lookup"><span data-stu-id="364c5-116">Before a provider can start up the virtualization instance that will project items into the local file system, it must create the virtualization root.</span></span>  <span data-ttu-id="364c5-117">La radice di virtualizzazione è la directory in cui il provider proietta una struttura ad albero di directory e file.</span><span class="sxs-lookup"><span data-stu-id="364c5-117">The virtualization root is the directory under which the provider projects a tree of directories and files.</span></span>

<span data-ttu-id="364c5-118">Per creare una radice di virtualizzazione, il provider deve:</span><span class="sxs-lookup"><span data-stu-id="364c5-118">To create a virtualization root the provider must:</span></span>

1. <span data-ttu-id="364c5-119">Creare una directory che funga da radice di virtualizzazione.</span><span class="sxs-lookup"><span data-stu-id="364c5-119">Create a directory to serve as the virtualization root.</span></span>

    <span data-ttu-id="364c5-120">Il provider crea una directory che funge da radice di virtualizzazione usando, ad esempio **[CreateDirectory](/windows/desktop/api/fileapi/nf-fileapi-createdirectoryw)**:</span><span class="sxs-lookup"><span data-stu-id="364c5-120">The provider creates a directory to serve as the virtualization root using, for example **[CreateDirectory](/windows/desktop/api/fileapi/nf-fileapi-createdirectoryw)**:</span></span>

    ```C++
    HRESULT hr;
    const wchar_t* rootName = LR"(C:\virtRoot)";
    if (!CreateDirectoryW(rootName, nullptr))
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        wprintf(L"Failed to create virtualization root (0x%08x)\n", hr);
        return;
    }
    ```

1. <span data-ttu-id="364c5-121">Creare un ID istanza di virtualizzazione.</span><span class="sxs-lookup"><span data-stu-id="364c5-121">Create a virtualization instance ID.</span></span>

    <span data-ttu-id="364c5-122">Ogni istanza di virtualizzazione ha un ID univoco denominato _ID istanza di virtualizzazione_.</span><span class="sxs-lookup"><span data-stu-id="364c5-122">Every virtualization instance has a unique ID called the _virtualization instance ID_.</span></span>  <span data-ttu-id="364c5-123">Questo valore viene utilizzato dal sistema per identificare l'istanza di virtualizzazione a cui è associato il contenuto.</span><span class="sxs-lookup"><span data-stu-id="364c5-123">The system uses this value to identify which virtualization instance its contents are associated to.</span></span>

    ```C++
    GUID instanceId;
    hr = CoCreateGuid(&instanceId);
    if (FAILED(hr))
    {
        wprintf(L"Failed to create instance ID (0x%08x)\n", hr);
        return;
    }
    ```

1. <span data-ttu-id="364c5-124">Contrassegnare la nuova directory come radice di virtualizzazione.</span><span class="sxs-lookup"><span data-stu-id="364c5-124">Mark the new directory as the virtualization root.</span></span>

    <span data-ttu-id="364c5-125">Il provider chiama **[PrjMarkDirectoryAsPlaceholder](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder)** per contrassegnare la nuova directory come radice di virtualizzazione e assegnarla all'istanza di virtualizzazione.</span><span class="sxs-lookup"><span data-stu-id="364c5-125">The provider calls **[PrjMarkDirectoryAsPlaceholder](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder)** to mark the new directory as the virtualization root and assign it to the virtualization instance.</span></span>

    ```C++
    hr = PrjMarkDirectoryAsPlaceholder(rootName,
                                       nullptr,
                                       nullptr,
                                       &instanceId);
    if (FAILED(hr))
    {
        wprintf(L"Failed to mark virtualization root (0x%08x)\n", hr);
        return;
    }
    ```

<span data-ttu-id="364c5-126">Il provider deve solo creare la radice di virtualizzazione una sola volta per ogni istanza di virtualizzazione.</span><span class="sxs-lookup"><span data-stu-id="364c5-126">The provider only needs to create the virtualization root once for each virtualization instance.</span></span>  <span data-ttu-id="364c5-127">Una volta creata una radice, l'istanza associata può essere avviata ripetutamente e arrestata senza ricreare la radice.</span><span class="sxs-lookup"><span data-stu-id="364c5-127">Once a root has been created, its associated instance can be repeatedly started and stopped without recreating the root.</span></span>

## <a name="starting-a-virtualization-instance"></a><span data-ttu-id="364c5-128">Avvio di un'istanza di virtualizzazione</span><span class="sxs-lookup"><span data-stu-id="364c5-128">Starting a virtualization instance</span></span>

<span data-ttu-id="364c5-129">Una volta creata la radice di virtualizzazione, il provider deve avviare l'istanza di virtualizzazione.</span><span class="sxs-lookup"><span data-stu-id="364c5-129">Once the virtualization root has been created the provider must start the virtualization instance.</span></span>  <span data-ttu-id="364c5-130">Questo segnala a ProjFS che il provider è pronto a ricevere i callback e a fornire i dati.</span><span class="sxs-lookup"><span data-stu-id="364c5-130">This signals ProjFS that the provider is ready to receive callbacks and provide data.</span></span>

<span data-ttu-id="364c5-131">Per avviare l'istanza di virtualizzazione, il provider deve:</span><span class="sxs-lookup"><span data-stu-id="364c5-131">To start the virtualization instance the provider must:</span></span>

1. <span data-ttu-id="364c5-132">Configurare la tabella di callback.</span><span class="sxs-lookup"><span data-stu-id="364c5-132">Set up the callback table.</span></span>

    <span data-ttu-id="364c5-133">ProjFS comunica con il provider richiamando le routine di callback implementate dal provider.</span><span class="sxs-lookup"><span data-stu-id="364c5-133">ProjFS communicates with the provider by invoking callback routines implemented by the provider.</span></span>  <span data-ttu-id="364c5-134">Il provider popola un [PRJ_CALLBACKS](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callbacks) struct con i puntatori alle relative routine di callback.</span><span class="sxs-lookup"><span data-stu-id="364c5-134">The provider populates a [PRJ_CALLBACKS](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callbacks) struct with pointers to its callback routines.</span></span>

    ```C++
    PRJ_CALLBACKS callbackTable;

    // Supply required callbacks.
    callbackTable.StartDirectoryEnumerationCallback = MyStartEnumCallback;
    callbackTable.EndDirectoryEnumerationCallback = MyEndEnumCallback;
    callbackTable.GetDirectoryEnumerationCallback = MyGetEnumCallback;
    callbackTable.GetPlaceholderInfoCallback = MyGetPlaceholderInfoCallback;
    callbackTable.GetFileDataCallback = MyGetFileDataCallback;

    // The rest of the callbacks are optional.
    callbackTable.QueryFileNameCallback = nullptr;
    callbackTable.NotificationCallback = nullptr;
    callbackTable.CancelCommandCallback = nullptr;
    ```

1. <span data-ttu-id="364c5-135">Avviare l'istanza di.</span><span class="sxs-lookup"><span data-stu-id="364c5-135">Start the instance.</span></span>

    <span data-ttu-id="364c5-136">Il provider chiama **[PrjStartVirtualizing](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing)** per avviare l'istanza di virtualizzazione.</span><span class="sxs-lookup"><span data-stu-id="364c5-136">The provider calls **[PrjStartVirtualizing](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing)** to start the virtualization instance.</span></span>

    ```C++
    PRJ_NAMESPACE_VIRTUALIZATION_CONTEXT instanceHandle;
    hr = PrjStartVirtualizing(rootName,
                              &callbackTable,
                              nullptr,
                              nullptr,
                              &instanceHandle);
    if (FAILED(hr))
    {
        wprintf(L"Failed to start the virtualization instance (0x%08x)\n", hr);
        return;
    }
    ```
    <span data-ttu-id="364c5-137">Il parametro _InstanceHandle_ di **PrjStartVirtualizing** restituisce un handle per l'istanza di virtualizzazione.</span><span class="sxs-lookup"><span data-stu-id="364c5-137">**PrjStartVirtualizing**'s _instanceHandle_ parameter returns a handle to the virtualization instance.</span></span>  <span data-ttu-id="364c5-138">Il provider usa questo handle quando chiamano altre API ProjFS.</span><span class="sxs-lookup"><span data-stu-id="364c5-138">The provider uses this handle when calling other ProjFS APIs.</span></span>

## <a name="virtualization-instance-runtime"></a><span data-ttu-id="364c5-139">Runtime dell'istanza di virtualizzazione</span><span class="sxs-lookup"><span data-stu-id="364c5-139">Virtualization instance runtime</span></span>

<span data-ttu-id="364c5-140">Una volta che la chiamata a **PrjStartVirtualizing** restituisce, ProjFS richiamerà le routine di callback del provider in risposta a file System operazioni nell'istanza di virtualizzazione.</span><span class="sxs-lookup"><span data-stu-id="364c5-140">Once the call to **PrjStartVirtualizing** returns, ProjFS will invoke the provider's callback routines in response to file system operations in the virtualization instance.</span></span>  <span data-ttu-id="364c5-141">Per informazioni sul modo in cui il provider è in grado di gestire diverse operazioni di file system, vedere le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="364c5-141">For information on how the provider can handle various file system operations, refer to the following sections:</span></span>

* [<span data-ttu-id="364c5-142">Enumerazione di file e directory</span><span class="sxs-lookup"><span data-stu-id="364c5-142">Enumerating Files and Directories</span></span>](enumerating-files-and-directories.md)
* [<span data-ttu-id="364c5-143">Fornire dati di file</span><span class="sxs-lookup"><span data-stu-id="364c5-143">Providing File Data</span></span>](providing-file-data.md)
* [<span data-ttu-id="364c5-144">Notifiche delle operazioni del file System</span><span class="sxs-lookup"><span data-stu-id="364c5-144">File System Operation Notifications</span></span>](file-system-operation-notifications.md)
* [<span data-ttu-id="364c5-145">Gestione delle modifiche della visualizzazione</span><span class="sxs-lookup"><span data-stu-id="364c5-145">Handling View Changes</span></span>](handling-view-changes.md)

## <a name="shutting-down-a-virtualization-instance"></a><span data-ttu-id="364c5-146">Arresto di un'istanza di virtualizzazione</span><span class="sxs-lookup"><span data-stu-id="364c5-146">Shutting down a virtualization instance</span></span>

<span data-ttu-id="364c5-147">Per segnalare a ProjFS che il provider vuole arrestare la ricezione di callback e fornire dati, il provider deve arrestare l'istanza di virtualizzazione.</span><span class="sxs-lookup"><span data-stu-id="364c5-147">To signal ProjFS that the provider wants to stop receiving callbacks and providing data, the provider must stop the virtualization instance.</span></span>  <span data-ttu-id="364c5-148">A tale scopo, il provider chiama **[PrjStopVirtualizing](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstopvirtualizing)**, passando l'handle all'istanza di virtualizzazione ricevuta dalla chiamata a **PrjStartVirtualizing**.</span><span class="sxs-lookup"><span data-stu-id="364c5-148">To do this the provider calls **[PrjStopVirtualizing](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstopvirtualizing)**, passing it the handle to the virtualization instance that it received from the call to **PrjStartVirtualizing**.</span></span>

```C++
PrjStopVirtualizing(instanceHandle);
```

<span data-ttu-id="364c5-149">Si noti che finché la chiamata non restituisce, ProjFS può continuare a richiamare le routine di callback del provider.</span><span class="sxs-lookup"><span data-stu-id="364c5-149">Note that until this call returns, ProjFS may continue to invoke the provider's callback routines.</span></span>