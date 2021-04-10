---
description: Argomenti sull'acquisizione avanzata
ms.assetid: 407702b2-5f4f-424d-a3ec-b0473e1b0da3
title: Argomenti sull'acquisizione avanzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4c4e5a077f6f8b17543250efa0f10091f0917e8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125067"
---
# <a name="advanced-capture-topics"></a><span data-ttu-id="1d7e4-103">Argomenti sull'acquisizione avanzata</span><span class="sxs-lookup"><span data-stu-id="1d7e4-103">Advanced Capture Topics</span></span>

<span data-ttu-id="1d7e4-104">Questa sezione descrive alcuni aspetti avanzati dell'acquisizione video in DirectShow.</span><span class="sxs-lookup"><span data-stu-id="1d7e4-104">This section describes some advanced aspects of video capture in DirectShow.</span></span> <span data-ttu-id="1d7e4-105">La maggior parte dei problemi descritti in questa sezione viene gestita automaticamente dall'interfaccia [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) .</span><span class="sxs-lookup"><span data-stu-id="1d7e4-105">Most of the issues described in this section are automatically handled by the [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface.</span></span> <span data-ttu-id="1d7e4-106">Tuttavia, le informazioni potrebbero essere utili se è necessario risolvere i problemi relativi a un'applicazione di acquisizione video.</span><span class="sxs-lookup"><span data-stu-id="1d7e4-106">However, the information here may be useful if you need to troubleshoot a video capture application.</span></span> <span data-ttu-id="1d7e4-107">È inoltre consigliabile leggere questa sezione se l'applicazione compila un grafico di acquisizione personalizzato di un certo tipo e si ritiene che ICaptureGraphBuilder2 non soddisfi le proprie esigenze.</span><span class="sxs-lookup"><span data-stu-id="1d7e4-107">You should also read this section if your application builds a custom capture graph of some kind and you find that ICaptureGraphBuilder2 does not suit your needs.</span></span> <span data-ttu-id="1d7e4-108">Infine, in questa sezione vengono fornite alcune informazioni sull'utilizzo del filtro VMR (video Mixing Renderer) in un'applicazione di acquisizione video.</span><span class="sxs-lookup"><span data-stu-id="1d7e4-108">Finally, this section contains some information about using the Video Mixing Renderer (VMR) filter in a video capture application.</span></span>

<span data-ttu-id="1d7e4-109">È possibile creare un grafico di acquisizione video completamente usando i metodi [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) .</span><span class="sxs-lookup"><span data-stu-id="1d7e4-109">It is possible to build a video capture graph entirely using [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) methods.</span></span> <span data-ttu-id="1d7e4-110">È anche possibile combinare le due interfacce, usando ICaptureGraphBuilder2 per alcune attività e IGraphBuilder per altri.</span><span class="sxs-lookup"><span data-stu-id="1d7e4-110">You can also combine the two interfaces, using ICaptureGraphBuilder2 for some tasks and IGraphBuilder for others.</span></span>

<span data-ttu-id="1d7e4-111">Questa sezione contiene i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="1d7e4-111">This section contains the following topics:</span></span>

-   [<span data-ttu-id="1d7e4-112">Gestione degli eventi di ridisegno in acquisizione video</span><span class="sxs-lookup"><span data-stu-id="1d7e4-112">Handling Repaint Events in Video Capture</span></span>](handling-repaint-events-in-video-capture.md)
-   [<span data-ttu-id="1d7e4-113">Utilizzo delle categorie pin</span><span class="sxs-lookup"><span data-stu-id="1d7e4-113">Working with Pin Categories</span></span>](working-with-pin-categories.md)
-   [<span data-ttu-id="1d7e4-114">Uso del filtro Smart Tee</span><span class="sxs-lookup"><span data-stu-id="1d7e4-114">Using the Smart Tee Filter</span></span>](using-the-smart-tee-filter.md)
-   [<span data-ttu-id="1d7e4-115">Uso del mixer overlay in acquisizione video</span><span class="sxs-lookup"><span data-stu-id="1d7e4-115">Using the Overlay Mixer in Video Capture</span></span>](using-the-overlay-mixer-in-video-capture.md)
-   [<span data-ttu-id="1d7e4-116">PIN della porta video</span><span class="sxs-lookup"><span data-stu-id="1d7e4-116">Video Port Pins</span></span>](video-port-pins.md)
-   [<span data-ttu-id="1d7e4-117">Tipo di formato VideoInfo2</span><span class="sxs-lookup"><span data-stu-id="1d7e4-117">VideoInfo2 Format Type</span></span>](videoinfo2-format-type.md)
-   [<span data-ttu-id="1d7e4-118">Creazione di filtri Kernel-Mode</span><span class="sxs-lookup"><span data-stu-id="1d7e4-118">Creating Kernel-Mode Filters</span></span>](creating-kernel-mode-filters.md)
-   [<span data-ttu-id="1d7e4-119">Filtri driver di classe WDM</span><span class="sxs-lookup"><span data-stu-id="1d7e4-119">WDM Class Driver Filters</span></span>](wdm-class-driver-filters.md)
-   [<span data-ttu-id="1d7e4-120">Uso di WDDM Capture in DirectShow</span><span class="sxs-lookup"><span data-stu-id="1d7e4-120">Using WDDM Capture in DirectShow</span></span>](using-wddm-capture-in-directshow.md)

## <a name="related-topics"></a><span data-ttu-id="1d7e4-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1d7e4-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d7e4-122">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="1d7e4-122">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



