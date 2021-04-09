---
description: La classe CVideoTransformFilter è progettata principalmente come classe di base per i filtri di decompressione AVI.
ms.assetid: 8eb87f9f-24b3-4dbe-a390-54db993d2724
title: Classe CVideoTransformFilter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter
api_type:
- COM
api_location: ''
ms.openlocfilehash: 360f46eb7242de01d5e734c5efa17399f23adf7d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103877042"
---
# <a name="cvideotransformfilter-class"></a><span data-ttu-id="2aa48-103">Classe CVideoTransformFilter</span><span class="sxs-lookup"><span data-stu-id="2aa48-103">CVideoTransformFilter class</span></span>

![gerarchia di classi cvideotransformfilter](images/vtsip01.png)

<span data-ttu-id="2aa48-105">La `CVideoTransformFilter` classe è progettata principalmente come classe di base per i filtri di decompressione AVI.</span><span class="sxs-lookup"><span data-stu-id="2aa48-105">The `CVideoTransformFilter` class is designed primarily as a base class for AVI decompressor filters.</span></span> <span data-ttu-id="2aa48-106">Questa classe aggiunge il supporto per il controllo qualità alla classe [**CTransformFilter**](ctransformfilter.md) .</span><span class="sxs-lookup"><span data-stu-id="2aa48-106">This class adds support for quality control to the [**CTransformFilter**](ctransformfilter.md) class.</span></span> <span data-ttu-id="2aa48-107">Il metodo di **ricezione** del filtro può decidere di eliminare i frame, in base ai messaggi di qualità del renderer e alle misurazioni delle prestazioni che il filtro raccoglie durante il flusso.</span><span class="sxs-lookup"><span data-stu-id="2aa48-107">The filter's **Receive** method can decide to drop frames, based on quality messages from the renderer and performance measurements that the filter collects while it is streaming.</span></span>

<span data-ttu-id="2aa48-108">Se il filtro rilascia un frame, continua a rilasciare i frame fino a raggiungere il fotogramma chiave successivo.</span><span class="sxs-lookup"><span data-stu-id="2aa48-108">If the filter drops a frame, it continues to drop frames until it reaches the next key frame.</span></span> <span data-ttu-id="2aa48-109">Per i flussi MPEG, il filtro non distingue tra B frame e P frame.</span><span class="sxs-lookup"><span data-stu-id="2aa48-109">For MPEG streams, the filter does not distinguish between B frames and P frames.</span></span>



| <span data-ttu-id="2aa48-110">Variabili membro protette</span><span class="sxs-lookup"><span data-stu-id="2aa48-110">Protected Member Variables</span></span>                                                      | <span data-ttu-id="2aa48-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2aa48-111">Description</span></span>                                                                                    |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2aa48-112">**\_bQualityChanged m**</span><span class="sxs-lookup"><span data-stu-id="2aa48-112">**m\_bQualityChanged**</span></span>](cvideotransformfilter-m-bqualitychanged.md)           | <span data-ttu-id="2aa48-113">Indica se il filtro ha eliminato i frame.</span><span class="sxs-lookup"><span data-stu-id="2aa48-113">Indicates whether the filter has dropped frames.</span></span>                                               |
| [<span data-ttu-id="2aa48-114">**\_bSkipping m**</span><span class="sxs-lookup"><span data-stu-id="2aa48-114">**m\_bSkipping**</span></span>](cvideotransformfilter-m-bskipping.md)                       | <span data-ttu-id="2aa48-115">Indica se il filtro sta attualmente eliminando i frame.</span><span class="sxs-lookup"><span data-stu-id="2aa48-115">Indicates whether the filter is currently dropping frames.</span></span>                                     |
| [<span data-ttu-id="2aa48-116">**\_itrAvgDecode m**</span><span class="sxs-lookup"><span data-stu-id="2aa48-116">**m\_itrAvgDecode**</span></span>](cvideotransformfilter-m-itravgdecode.md)                 | <span data-ttu-id="2aa48-117">Durata media del tempo impiegato per decodificare un frame.</span><span class="sxs-lookup"><span data-stu-id="2aa48-117">Average length of time it has taken to decode a frame.</span></span>                                         |
| [<span data-ttu-id="2aa48-118">**\_itrLate m**</span><span class="sxs-lookup"><span data-stu-id="2aa48-118">**m\_itrLate**</span></span>](cvideotransformfilter-m-itrlate.md)                           | <span data-ttu-id="2aa48-119">Indica la fine dell'arrivo degli esempi nel renderer.</span><span class="sxs-lookup"><span data-stu-id="2aa48-119">Indicates how late the samples are arriving at the renderer.</span></span>                                   |
| [<span data-ttu-id="2aa48-120">**\_nFramesSinceKeyFrame m**</span><span class="sxs-lookup"><span data-stu-id="2aa48-120">**m\_nFramesSinceKeyFrame**</span></span>](cvideotransformfilter-m-nframessincekeyframe.md) | <span data-ttu-id="2aa48-121">Numero di frame ricevuti dal filtro dall'ultimo fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="2aa48-121">The number of frames that the filter has received since the last key frame.</span></span>                    |
| [<span data-ttu-id="2aa48-122">**\_nKeyFramePeriod m**</span><span class="sxs-lookup"><span data-stu-id="2aa48-122">**m\_nKeyFramePeriod**</span></span>](cvideotransformfilter-m-nkeyframeperiod.md)           | <span data-ttu-id="2aa48-123">Intervallo osservato più grande tra fotogrammi chiave.</span><span class="sxs-lookup"><span data-stu-id="2aa48-123">The largest observed interval between key frames.</span></span>                                              |
| [<span data-ttu-id="2aa48-124">**\_nWaitForKey m**</span><span class="sxs-lookup"><span data-stu-id="2aa48-124">**m\_nWaitForKey**</span></span>](cvideotransformfilter-m-nwaitforkey.md)                   | <span data-ttu-id="2aa48-125">Numero massimo corrente di fotogrammi Delta da eliminare.</span><span class="sxs-lookup"><span data-stu-id="2aa48-125">The current maximum number of delta frames to drop.</span></span>                                            |
| [<span data-ttu-id="2aa48-126">**\_tDecodeStart m**</span><span class="sxs-lookup"><span data-stu-id="2aa48-126">**m\_tDecodeStart**</span></span>](cvideotransformfilter-m-tdecodestart.md)                 | <span data-ttu-id="2aa48-127">Tempo impiegato per decodificare l'esempio più recente.</span><span class="sxs-lookup"><span data-stu-id="2aa48-127">Length of time that it took to decode the most recent sample.</span></span>                                  |
| <span data-ttu-id="2aa48-128">Metodi protetti</span><span class="sxs-lookup"><span data-stu-id="2aa48-128">Protected Methods</span></span>                                                               | <span data-ttu-id="2aa48-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2aa48-129">Description</span></span>                                                                                    |
| [<span data-ttu-id="2aa48-130">**AbortPlayback**</span><span class="sxs-lookup"><span data-stu-id="2aa48-130">**AbortPlayback**</span></span>](cvideotransformfilter-abortplayback.md)                    | <span data-ttu-id="2aa48-131">Utilizzato per segnalare un errore di streaming.</span><span class="sxs-lookup"><span data-stu-id="2aa48-131">Used to signal a streaming error.</span></span>                                                              |
| [<span data-ttu-id="2aa48-132">**AlterQuality**</span><span class="sxs-lookup"><span data-stu-id="2aa48-132">**AlterQuality**</span></span>](cvideotransformfilter-alterquality.md)                      | <span data-ttu-id="2aa48-133">Notifica al filtro che è richiesta una modifica di qualità.</span><span class="sxs-lookup"><span data-stu-id="2aa48-133">Notifies the filter that a quality change is requested.</span></span>                                        |
| [<span data-ttu-id="2aa48-134">**Ricevere**</span><span class="sxs-lookup"><span data-stu-id="2aa48-134">**Receive**</span></span>](cvideotransformfilter-receive.md)                                | <span data-ttu-id="2aa48-135">Riceve un esempio multimediale, lo elabora e recapita un esempio di output al filtro downstream.</span><span class="sxs-lookup"><span data-stu-id="2aa48-135">Receives a media sample, processes it, and delivers an output sample to the downstream filter.</span></span> |
| [<span data-ttu-id="2aa48-136">**ShouldSkipFrame**</span><span class="sxs-lookup"><span data-stu-id="2aa48-136">**ShouldSkipFrame**</span></span>](cvideotransformfilter-shouldskipframe.md)                | <span data-ttu-id="2aa48-137">Determina se il filtro deve eliminare un campione specificato.</span><span class="sxs-lookup"><span data-stu-id="2aa48-137">Determines whether the filter should drop a specified sample.</span></span>                                  |
| [<span data-ttu-id="2aa48-138">**StartStreaming**</span><span class="sxs-lookup"><span data-stu-id="2aa48-138">**StartStreaming**</span></span>](cvideotransformfilter-startstreaming.md)                  | <span data-ttu-id="2aa48-139">Chiamato quando il filtro passa allo stato sospeso.</span><span class="sxs-lookup"><span data-stu-id="2aa48-139">Called when the filter switches to the paused state.</span></span>                                           |
| <span data-ttu-id="2aa48-140">Metodi pubblici</span><span class="sxs-lookup"><span data-stu-id="2aa48-140">Public Methods</span></span>                                                                  | <span data-ttu-id="2aa48-141">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2aa48-141">Description</span></span>                                                                                    |
| [<span data-ttu-id="2aa48-142">**CVideoTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="2aa48-142">**CVideoTransformFilter**</span></span>](cvideotransformfilter-cvideotransformfilter.md)    | <span data-ttu-id="2aa48-143">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="2aa48-143">Constructor method.</span></span>                                                                            |
| [<span data-ttu-id="2aa48-144">**EndFlush**</span><span class="sxs-lookup"><span data-stu-id="2aa48-144">**EndFlush**</span></span>](cvideotransformfilter-endflush.md)                              | <span data-ttu-id="2aa48-145">Termina un'operazione di svuotamento.</span><span class="sxs-lookup"><span data-stu-id="2aa48-145">Ends a flush operation.</span></span>                                                                        |



 

 

 



