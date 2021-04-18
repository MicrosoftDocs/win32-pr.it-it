---
description: Uso del filtro Smart Tee
ms.assetid: d2828269-6841-41a8-8d45-f864c7e85857
title: Uso del filtro Smart Tee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5260469634c613fe05c25eb9f55e24e108e8c434
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314383"
---
# <a name="using-the-smart-tee-filter"></a><span data-ttu-id="431fd-103">Uso del filtro Smart Tee</span><span class="sxs-lookup"><span data-stu-id="431fd-103">Using the Smart Tee Filter</span></span>

<span data-ttu-id="431fd-104">Se un filtro di acquisizione presenta pin di acquisizione e di anteprima distinti, è possibile acquisire da uno durante l'anteprima dell'altro.</span><span class="sxs-lookup"><span data-stu-id="431fd-104">If a capture filter has separate capture and preview pins, you can capture from one while previewing from the other.</span></span> <span data-ttu-id="431fd-105">Tuttavia, se il filtro non ha un pin di anteprima, è possibile eseguire la stessa operazione includendo il filtro [Smart Tee](smart-tee-filter.md) nel grafico.</span><span class="sxs-lookup"><span data-stu-id="431fd-105">But if the filter has no preview pin, you can do the same thing by including the [Smart Tee](smart-tee-filter.md) filter in the graph.</span></span> <span data-ttu-id="431fd-106">Questo filtro suddivide i dati dal pin di acquisizione in due flussi identici, uno per l'acquisizione e uno per l'anteprima.</span><span class="sxs-lookup"><span data-stu-id="431fd-106">This filter splits data from the capture pin into two identical streams, one for capture and one for preview.</span></span> <span data-ttu-id="431fd-107">La figura seguente illustra questo processo.</span><span class="sxs-lookup"><span data-stu-id="431fd-107">The following diagram illustrates this process.</span></span>

![Acquisisci grafico con filtro Smart Tee](images/vidcap05.png)

<span data-ttu-id="431fd-109">Se necessario, il metodo [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) inserisce automaticamente il filtro Smart Tee.</span><span class="sxs-lookup"><span data-stu-id="431fd-109">The [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method automatically inserts the Smart Tee Filter if it is required.</span></span> <span data-ttu-id="431fd-110">Tuttavia, se si usano i metodi **IGraphBuilder** per compilare il grafo e non **RenderStream**, potrebbe essere necessario inserire il filtro Smart Tee.</span><span class="sxs-lookup"><span data-stu-id="431fd-110">However, if you use **IGraphBuilder** methods to build your graph, and not **RenderStream**, you may need to insert the Smart Tee filter.</span></span>

<span data-ttu-id="431fd-111">Prima di eseguire il rendering dei pin nel filtro di acquisizione, controllare se il filtro ha un pin di anteprima o un PIN della porta video.</span><span class="sxs-lookup"><span data-stu-id="431fd-111">Before you render pins on the capture filter, check whether the filter has a preview pin or a video port pin.</span></span> <span data-ttu-id="431fd-112">In caso contrario, aggiungere il filtro Smart Tee al grafico e connetterlo al pin di acquisizione nel filtro di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="431fd-112">If it does not, and you wish to preview, add the Smart Tee filter to the graph and connect it to the capture pin on the capture filter.</span></span>

> [!Note]  
> <span data-ttu-id="431fd-113">È possibile trattare un PIN della porta video (VP) come tipo di pin di anteprima, pertanto un filtro con un pin VP non necessita di un filtro per Smart Tee.</span><span class="sxs-lookup"><span data-stu-id="431fd-113">You can treat a video port (VP) pin as a kind of preview pin, so a filter with a VP pin does not need a Smart Tee filter.</span></span> <span data-ttu-id="431fd-114">Tuttavia, i pin VP hanno altri requisiti particolari.</span><span class="sxs-lookup"><span data-stu-id="431fd-114">However, VP pins have some other special requirements.</span></span> <span data-ttu-id="431fd-115">Per altre informazioni, vedere [pin della porta video](video-port-pins.md).</span><span class="sxs-lookup"><span data-stu-id="431fd-115">For more information, see [Video Port Pins](video-port-pins.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="431fd-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="431fd-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="431fd-117">Argomenti sull'acquisizione avanzata</span><span class="sxs-lookup"><span data-stu-id="431fd-117">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> <dt>

[<span data-ttu-id="431fd-118">Combinazione di acquisizione video e anteprima</span><span class="sxs-lookup"><span data-stu-id="431fd-118">Combining Video Capture and Preview</span></span>](combining-video-capture-and-preview.md)
</dt> <dt>

[<span data-ttu-id="431fd-119">Utilizzo delle categorie pin</span><span class="sxs-lookup"><span data-stu-id="431fd-119">Working with Pin Categories</span></span>](working-with-pin-categories.md)
</dt> </dl>

 

 



