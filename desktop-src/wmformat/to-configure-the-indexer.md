---
title: Per configurare l'indicizzatore
description: Per configurare l'indicizzatore
ms.assetid: 0e28e8dd-1586-45e6-8a08-5245d465d068
keywords:
- Windows Media Format SDK, configurazione degli indicizzatori
- Formato di sistemi avanzati (ASF), configurazione degli indicizzatori
- ASF (formato avanzato dei sistemi), configurazione degli indicizzatori
- indici, configurazione degli indicizzatori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 618316e22b13ca05ff0fc1bbfb6b4583e79ca858
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398606"
---
# <a name="to-configure-the-indexer"></a><span data-ttu-id="1f3a5-107">Per configurare l'indicizzatore</span><span class="sxs-lookup"><span data-stu-id="1f3a5-107">To Configure the Indexer</span></span>

<span data-ttu-id="1f3a5-108">È possibile configurare l'indicizzatore prima di utilizzarlo per indicizzare un file ASF.</span><span class="sxs-lookup"><span data-stu-id="1f3a5-108">You can configure the indexer before using it to index an ASF file.</span></span> <span data-ttu-id="1f3a5-109">Ogni flusso del file può essere configurato separatamente oppure è possibile impostare la stessa configurazione per tutti i flussi.</span><span class="sxs-lookup"><span data-stu-id="1f3a5-109">Each stream in the file can be configured separately, or you can set the same configuration for all streams.</span></span>

<span data-ttu-id="1f3a5-110">Se si configurano più Vapor per l'indicizzazione in un file, è necessario configurarli tutti e quindi avviare l'indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="1f3a5-110">If you are configuring multiple steams for indexing in a file, you must configure them all and then begin indexing.</span></span> <span data-ttu-id="1f3a5-111">Se si configura e indicizza un flusso e quindi si configura un altro flusso nello stesso file, l'avvio dell'indicizzatore eliminerà nuovamente il primo indice.</span><span class="sxs-lookup"><span data-stu-id="1f3a5-111">If you configure and index a stream and then configure another stream in the same file, starting the indexer again will delete the first index.</span></span> <span data-ttu-id="1f3a5-112">Questa operazione deve essere conforme al formato di file ASF.</span><span class="sxs-lookup"><span data-stu-id="1f3a5-112">This is to comply with the ASF file format.</span></span>

<span data-ttu-id="1f3a5-113">Il codice seguente illustra come configurare l'indicizzatore.</span><span class="sxs-lookup"><span data-stu-id="1f3a5-113">The following code shows how to configure the indexer.</span></span> <span data-ttu-id="1f3a5-114">Il codice presuppone che il file da indicizzare abbia due flussi: il primo è un flusso audio che non deve essere indicizzato e il secondo è un flusso video.</span><span class="sxs-lookup"><span data-stu-id="1f3a5-114">The code assumes that the file to be indexed has two streams: the first is an audio stream which does not need to be indexed, and the second is a video stream.</span></span> <span data-ttu-id="1f3a5-115">Questo codice Mostra solo come configurare l'indicizzatore.</span><span class="sxs-lookup"><span data-stu-id="1f3a5-115">This code shows only how to configure the indexer.</span></span> <span data-ttu-id="1f3a5-116">Per indicizzare un file, è necessario seguire la procedura illustrata in [per indicizzare un file ASF](to-index-an-asf-file.md).</span><span class="sxs-lookup"><span data-stu-id="1f3a5-116">To index a file, you must follow the steps presented in [To Index an ASF File](to-index-an-asf-file.md).</span></span>


```C++
IWMIndexer*  pBaseIndexer = NULL;
IWMIndexer2* pMyIndexer   = NULL;

DWORD          dwInterval;
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create an indexer.
hr = WMCreateIndexer(&pBaseIndexer);

// Retrieve an IWMIndexer2 interface pointer for the indexer just created.
hr = pBaseIndexer->QueryInterface(IID_IWMIndexer2, (void**)&pMyIndexer);

// Release the base indexer.
pBaseIndexer->Release();
pBaseIndexer = NULL;

// Set the index interval to 5 frames.
dwInterval = 5;

// Configure the indexer to create a frame-based index.
hr = pMyIndexer->Configure(2,                    // Stream Number.
                           WMT_IT_FRAME_NUMBERS, // Indexer type.
                           (void *)&dwInterval,  // Index interval.
                           NULL;        // Index type, use default.

// TODO: Index the file. See To Index an ASF File.

// Release the remaining interface.
pMyIndexer->Release();
pMyIndexer = NULL;

```



> [!Note]  
> <span data-ttu-id="1f3a5-117">Il tipo di indice predefinito è \_ WMT \_ punto di pulizia più vicino \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1f3a5-117">The default index type is WMT\_IT\_NEAREST\_CLEAN\_POINT.</span></span> <span data-ttu-id="1f3a5-118">Sebbene sia possibile impostare il tipo di indice su altri valori, in questo modo si riduce la ricerca delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="1f3a5-118">Although you can set the index type to other values, doing so will degrade seeking performance.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="1f3a5-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1f3a5-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f3a5-120">**IWMIndexer2:: Configure**</span><span class="sxs-lookup"><span data-stu-id="1f3a5-120">**IWMIndexer2::Configure**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer2-configure)
</dt> <dt>

[<span data-ttu-id="1f3a5-121">**Per indicizzare un file ASF**</span><span class="sxs-lookup"><span data-stu-id="1f3a5-121">**To Index an ASF File**</span></span>](to-index-an-asf-file.md)
</dt> <dt>

[<span data-ttu-id="1f3a5-122">**WMCreateIndexer**</span><span class="sxs-lookup"><span data-stu-id="1f3a5-122">**WMCreateIndexer**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)
</dt> <dt>

[<span data-ttu-id="1f3a5-123">**Operazioni con gli indici**</span><span class="sxs-lookup"><span data-stu-id="1f3a5-123">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




