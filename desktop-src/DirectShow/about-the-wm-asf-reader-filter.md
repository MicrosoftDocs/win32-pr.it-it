---
description: Informazioni sul filtro WM ASF Reader
ms.assetid: e698c0da-88b2-497a-8a25-9d3b76c85a7d
title: Informazioni sul filtro WM ASF Reader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 350e6597aa6aa66193af37a30ed54c37139d5f81
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876858"
---
# <a name="about-the-wm-asf-reader-filter"></a><span data-ttu-id="0f1bf-103">Informazioni sul filtro WM ASF Reader</span><span class="sxs-lookup"><span data-stu-id="0f1bf-103">About the WM ASF Reader Filter</span></span>

<span data-ttu-id="0f1bf-104">La riproduzione dei file ASF viene gestita dal filtro [WM ASF Reader](wm-asf-reader-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="0f1bf-104">Playback of ASF files is handled by the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span> <span data-ttu-id="0f1bf-105">Quando il lettore WM ASF legge un file, viene creato automaticamente un pin di output per ogni flusso, inclusi i flussi Web, i flussi dei comandi di script e qualsiasi altro tipo di flusso arbitrario.</span><span class="sxs-lookup"><span data-stu-id="0f1bf-105">When the WM ASF Reader reads a file, it automatically creates an output pin for each stream, including web streams, script command streams, and any other type of arbitrary stream.</span></span> <span data-ttu-id="0f1bf-106">Nel caso di file a più velocità in bit, i PIN vengono creati solo per i flussi attualmente selezionati.</span><span class="sxs-lookup"><span data-stu-id="0f1bf-106">In the case of multiple bit rate files, pins are created only for the currently selected streams.</span></span> <span data-ttu-id="0f1bf-107">Per riprodurre un file ASF con il filtro WM ASF Reader, chiamare [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) o [**IGraphBuilder:: AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter).</span><span class="sxs-lookup"><span data-stu-id="0f1bf-107">To play an ASF file with the WM ASF Reader filter, call [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) or [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter).</span></span>

<span data-ttu-id="0f1bf-108">Il lettore WM ASF supporta l'interfaccia DirectShow [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) , che consente alle applicazioni di eseguire ricerche temporali all'interno del file.</span><span class="sxs-lookup"><span data-stu-id="0f1bf-108">The WM ASF Reader supports the DirectShow [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface, which enables applications to perform temporal seeking within the file.</span></span> <span data-ttu-id="0f1bf-109">Tuttavia, la riproduzione a velocità diverse da 1,0 (come specificato in [**IMediaSeeking:: serate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)) non è supportata.</span><span class="sxs-lookup"><span data-stu-id="0f1bf-109">However, playback at speeds other than 1.0 (as specified in [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)) is not supported.</span></span>

<span data-ttu-id="0f1bf-110">Il filtro WM ASF Reader espone inoltre diverse interfacce di Windows Media Format SDK, come descritto nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="0f1bf-110">The WM ASF Reader filter also exposes several Windows Media Format SDK interfaces as described in the following table.</span></span> <span data-ttu-id="0f1bf-111">Queste interfacce sono documentate nella documentazione di Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="0f1bf-111">These interfaces are documented in the Windows Media Format SDK documentation.</span></span>



| <span data-ttu-id="0f1bf-112">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="0f1bf-112">Interface</span></span>                                             | <span data-ttu-id="0f1bf-113">Modalità di esposizione</span><span class="sxs-lookup"><span data-stu-id="0f1bf-113">How exposed</span></span>                                 | <span data-ttu-id="0f1bf-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="0f1bf-114">Comments</span></span>                                                                                                                       |
|-------------------------------------------------------|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0f1bf-115">**IWMDRMReader**</span><span class="sxs-lookup"><span data-stu-id="0f1bf-115">**IWMDRMReader**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)             | <span data-ttu-id="0f1bf-116">Tramite **IServiceProvider** sul filtro.</span><span class="sxs-lookup"><span data-stu-id="0f1bf-116">Through **IServiceProvider** on the filter.</span></span> | <span data-ttu-id="0f1bf-117">Fornito per le applicazioni che devono riprodurre contenuti protetti da Rights Management digitali (DRM).</span><span class="sxs-lookup"><span data-stu-id="0f1bf-117">Provided for applications that need to play content protected by Digital Rights Management (DRM)..</span></span>                             |
| [<span data-ttu-id="0f1bf-118">**IWMHeaderInfo**</span><span class="sxs-lookup"><span data-stu-id="0f1bf-118">**IWMHeaderInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | <span data-ttu-id="0f1bf-119">**QueryInterface** sul filtro.</span><span class="sxs-lookup"><span data-stu-id="0f1bf-119">**QueryInterface** on the filter.</span></span>           | <span data-ttu-id="0f1bf-120">Fornito in modo che le applicazioni possano leggere gli attributi di file e contenuto, nonché informazioni su marcatore e script e metadati.</span><span class="sxs-lookup"><span data-stu-id="0f1bf-120">Provided so that applications can read file and content attributes, as well as marker and script information and metadata.</span></span>     |
| [<span data-ttu-id="0f1bf-121">**IWMReaderAdvanced**</span><span class="sxs-lookup"><span data-stu-id="0f1bf-121">**IWMReaderAdvanced**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)   | <span data-ttu-id="0f1bf-122">**QueryInterface** sul filtro.</span><span class="sxs-lookup"><span data-stu-id="0f1bf-122">**QueryInterface** on the filter.</span></span>           | <span data-ttu-id="0f1bf-123">Implementato parzialmente sul filtro in modo che le applicazioni possano accedere ai metodi informativi nell'oggetto WM Reader.</span><span class="sxs-lookup"><span data-stu-id="0f1bf-123">Partially implemented on the filter so that applications can access the informational methods on the WM Reader object.</span></span>         |
| [<span data-ttu-id="0f1bf-124">**IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="0f1bf-124">**IWMReaderAdvanced2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) | <span data-ttu-id="0f1bf-125">**QueryInterface** sul filtro.</span><span class="sxs-lookup"><span data-stu-id="0f1bf-125">**QueryInterface** on the filter.</span></span>           | <span data-ttu-id="0f1bf-126">Implementato parzialmente sul filtro in modo che le applicazioni possano accedere ai metodi informativi nell'oggetto Reader di Format SDK.</span><span class="sxs-lookup"><span data-stu-id="0f1bf-126">Partially implemented on the filter so that applications can access the informational methods on the Format SDK Reader Object.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="0f1bf-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0f1bf-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f1bf-128">Lettura di file ASF in DirectShow</span><span class="sxs-lookup"><span data-stu-id="0f1bf-128">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



