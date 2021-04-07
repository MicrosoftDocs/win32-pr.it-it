---
description: Interfacce per il controllo di un grafico di filtro
ms.assetid: f7de0165-e356-45d5-baed-d127caeebaf6
title: Interfacce per il controllo di un grafico di filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61e88dc4ba2143bbbf33a58763a5ff9005254236
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747106"
---
# <a name="interfaces-for-controlling-a-filter-graph"></a><span data-ttu-id="89100-103">Interfacce per il controllo di un grafico di filtro</span><span class="sxs-lookup"><span data-stu-id="89100-103">Interfaces for Controlling a Filter Graph</span></span>

<span data-ttu-id="89100-104">Queste interfacce forniscono metodi per il controllo di un grafico di filtro.</span><span class="sxs-lookup"><span data-stu-id="89100-104">These interfaces provide methods for controlling a filter graph.</span></span>



| <span data-ttu-id="89100-105">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="89100-105">Interface</span></span>                                  | <span data-ttu-id="89100-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="89100-106">Description</span></span>                                                                                               |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="89100-107">**IAMClockAdjust**</span><span class="sxs-lookup"><span data-stu-id="89100-107">**IAMClockAdjust**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust)   | <span data-ttu-id="89100-108">Modificare il clock del grafico.</span><span class="sxs-lookup"><span data-stu-id="89100-108">Adjust the graph clock.</span></span>                                                                                   |
| [<span data-ttu-id="89100-109">**IAMGraphStreams**</span><span class="sxs-lookup"><span data-stu-id="89100-109">**IAMGraphStreams**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamgraphstreams) | <span data-ttu-id="89100-110">Sincronizzare i flussi live in un grafico di filtro.</span><span class="sxs-lookup"><span data-stu-id="89100-110">Synchronize live streams in a filter graph.</span></span>                                                               |
| [<span data-ttu-id="89100-111">**IFilterChain**</span><span class="sxs-lookup"><span data-stu-id="89100-111">**IFilterChain**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifilterchain)       | <span data-ttu-id="89100-112">Catene di controllo dei filtri.</span><span class="sxs-lookup"><span data-stu-id="89100-112">Control chains of filters.</span></span>                                                                                |
| [<span data-ttu-id="89100-113">**IMediaControl**</span><span class="sxs-lookup"><span data-stu-id="89100-113">**IMediaControl**</span></span>](/windows/desktop/api/Control/nn-control-imediacontrol)     | <span data-ttu-id="89100-114">Eseguire, sospendere e arrestare il grafico del filtro.</span><span class="sxs-lookup"><span data-stu-id="89100-114">Run, pause, and stop the filter graph.</span></span> <span data-ttu-id="89100-115">Fornisce anche metodi compatibili con l'automazione per la creazione di grafici.</span><span class="sxs-lookup"><span data-stu-id="89100-115">(Also provides Automation-compatible methods for building graphs.)</span></span> |
| [<span data-ttu-id="89100-116">**IMediaEventEx**</span><span class="sxs-lookup"><span data-stu-id="89100-116">**IMediaEventEx**</span></span>](/windows/desktop/api/Control/nn-control-imediaeventex)     | <span data-ttu-id="89100-117">Rispondere agli eventi nel grafico.</span><span class="sxs-lookup"><span data-stu-id="89100-117">Respond to events in the graph.</span></span>                                                                           |
| [<span data-ttu-id="89100-118">**IMediaSeeking**</span><span class="sxs-lookup"><span data-stu-id="89100-118">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)     | <span data-ttu-id="89100-119">Ricerca all'interno di un file.</span><span class="sxs-lookup"><span data-stu-id="89100-119">Seek within a file.</span></span>                                                                                       |
| [<span data-ttu-id="89100-120">**IQueueCommand**</span><span class="sxs-lookup"><span data-stu-id="89100-120">**IQueueCommand**</span></span>](/windows/desktop/api/Control/nn-control-iqueuecommand)     | <span data-ttu-id="89100-121">Accodare i comandi da eseguire in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="89100-121">Queue commands to run at a later time.</span></span>                                                                    |
| [<span data-ttu-id="89100-122">**IVideoFrameStep**</span><span class="sxs-lookup"><span data-stu-id="89100-122">**IVideoFrameStep**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) | <span data-ttu-id="89100-123">Frame-Step in un flusso video.</span><span class="sxs-lookup"><span data-stu-id="89100-123">Frame-step through a video stream.</span></span>                                                                        |



 

 

 



