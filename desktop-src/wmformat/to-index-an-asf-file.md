---
title: Per indicizzare un file ASF
description: Per indicizzare un file ASF
ms.assetid: 33175444-365c-4b94-8b91-07198431062f
keywords:
- Windows Media Format SDK, indicizzazione di file ASF
- ASF (Advanced Systems Format), indicizzazione di file
- ASF (Advanced Systems Format), indicizzazione di file
- indici, indicizzazione di file ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7206e1856abb9705e18e885ba06cb8253a93c84b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299400"
---
# <a name="to-index-an-asf-file"></a><span data-ttu-id="63184-107">Per indicizzare un file ASF</span><span class="sxs-lookup"><span data-stu-id="63184-107">To Index an ASF File</span></span>

<span data-ttu-id="63184-108">Il processo di indicizzazione di un file ASF è molto semplice.</span><span class="sxs-lookup"><span data-stu-id="63184-108">The process of indexing an ASF file is very simple.</span></span> <span data-ttu-id="63184-109">Effettuare una chiamata a [**IWMIndexer:: startindexing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing) e passare il nome del file.</span><span class="sxs-lookup"><span data-stu-id="63184-109">Make a call to [**IWMIndexer::StartIndexing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing) and pass the file name.</span></span> <span data-ttu-id="63184-110">L'indicizzatore esegue il resto.</span><span class="sxs-lookup"><span data-stu-id="63184-110">The indexer does the rest.</span></span> <span data-ttu-id="63184-111">La chiamata a **startIndex** è asincrona, pertanto lo stato deve essere monitorato tramite il callback **OnStatus** .</span><span class="sxs-lookup"><span data-stu-id="63184-111">The call to **StartIndexing** is asynchronous, so status must be monitored using the **OnStatus** callback.</span></span>

<span data-ttu-id="63184-112">Nel codice seguente viene illustrato come indicizzare un file ASF.</span><span class="sxs-lookup"><span data-stu-id="63184-112">The following code shows how to index an ASF file.</span></span> <span data-ttu-id="63184-113">Se si vuole configurare l'indicizzatore prima di indicizzare il file, sarà necessario includere il codice dell'esempio incluso in [per configurare l'indicizzatore](to-configure-the-indexer.md).</span><span class="sxs-lookup"><span data-stu-id="63184-113">If you want to configure the indexer prior to indexing the file, you will need to include code from the example included in [To Configure the Indexer](to-configure-the-indexer.md).</span></span>

<span data-ttu-id="63184-114">Per questo esempio, è necessario creare l'handle che punta all'evento come variabile globale in modo che sia accessibile dal callback.</span><span class="sxs-lookup"><span data-stu-id="63184-114">For this example, the handle that points to the event must be created as a global variable so it will be accessible by the callback.</span></span> <span data-ttu-id="63184-115">La dichiarazione seguente dovrebbe essere visualizzata in un ambito globale.</span><span class="sxs-lookup"><span data-stu-id="63184-115">The following declaration should appear in a global scope.</span></span>


```C++
HANDLE g_hEvent = NULL;

```



<span data-ttu-id="63184-116">In uno scenario più realistico, l'handle di evento deve essere un membro dati della classe che contiene sia il callback che la logica per l'avvio dell'indicizzatore.</span><span class="sxs-lookup"><span data-stu-id="63184-116">In a more realistic scenario, the event handle should be a data member of the class that contains both the callback and the logic for starting the indexer.</span></span>

<span data-ttu-id="63184-117">L'indicizzatore invia diversi eventi al callback **OnStatus** dopo la chiamata a **IWMIndexer:: startindexing**.</span><span class="sxs-lookup"><span data-stu-id="63184-117">The indexer sends several events to the **OnStatus** callback after the call to **IWMIndexer::StartIndexing**.</span></span> <span data-ttu-id="63184-118">È possibile intercettarli in base alle esigenze dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="63184-118">You can trap them as needed for your application.</span></span> <span data-ttu-id="63184-119">Come minimo, è necessario intercettare la chiusura di WMT \_ , che viene inviata al termine dell'indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="63184-119">At a minimum, you need to trap WMT\_CLOSED, which is sent when indexing is complete.</span></span> <span data-ttu-id="63184-120">Utilizzare la seguente logica all'interno dell'opzione Message nell'implementazione del callback **OnStatus** .</span><span class="sxs-lookup"><span data-stu-id="63184-120">Use the following logic within the message switch in your implementation of the **OnStatus** callback.</span></span>


```C++
// Inside the status switch statement.
case WMT_CLOSED:
   // You may want to deal with the HRESULT value passed with the status.
   // If you do, you should do it here.

   // Signal the event.
   SetEvent(g_hEvent);
   break;

```



<span data-ttu-id="63184-121">Per questo esempio si presuppone che l'implementazione del callback **OnStatus** sia accessibile tramite un oggetto denominato callback.</span><span class="sxs-lookup"><span data-stu-id="63184-121">For this example it is assumed that your implementation of the **OnStatus** callback is accessed through an object called MyCallback.</span></span> <span data-ttu-id="63184-122">Per altre informazioni sull'uso di eventi e callback con questo SDK, vedere [uso dei metodi di callback](using-the-callback-methods.md).</span><span class="sxs-lookup"><span data-stu-id="63184-122">For more information about using events and callbacks with this SDK, see [Using the Callback Methods](using-the-callback-methods.md).</span></span>


```C++
IWMIndexer* pMyIndexer     = NULL;
HRESULT     hr             = S_OK;
WCHAR       pwszFileName[] = L"C:\SomeFile.wmv";

// Initialize COM.
hr = CoInitialize(NULL);

// Create an event for asynchronous calls.
g_hEvent = CreateEvent(NULL, TRUE, FALSE, NULL);

// Create an indexer.
hr = WMCreateIndexer(&pMyIndexer);

// TODO: Configure the indexer if needed. See To Configure the Indexer.

// Start the indexer.
hr = pMyIndexer->StartIndexing(pwszFileName, &MyCallback, NULL);

// Wait for the indexer to finish.
WaitForSingleObject(g_hEvent, INFINITE);

// Clean up.
pMyIndexer->Release();
pMyIndexer = NULL

CloseHandle(g_hEvent);
g_hEvent = NULL;

```



## <a name="related-topics"></a><span data-ttu-id="63184-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="63184-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63184-124">**Interfaccia IWMIndexer**</span><span class="sxs-lookup"><span data-stu-id="63184-124">**IWMIndexer Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)
</dt> <dt>

[<span data-ttu-id="63184-125">**Per configurare l'indicizzatore**</span><span class="sxs-lookup"><span data-stu-id="63184-125">**To Configure the Indexer**</span></span>](to-configure-the-indexer.md)
</dt> <dt>

[<span data-ttu-id="63184-126">**WMCreateIndexer**</span><span class="sxs-lookup"><span data-stu-id="63184-126">**WMCreateIndexer**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)
</dt> <dt>

[<span data-ttu-id="63184-127">**Operazioni con gli indici**</span><span class="sxs-lookup"><span data-stu-id="63184-127">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




