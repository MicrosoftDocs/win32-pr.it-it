---
description: Eventi di origine dei supporti
ms.assetid: c7b6ea86-e919-45b8-a1f9-bd18c3aed163
title: Eventi di origine dei supporti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72c40755a32f610b33ef3a5c66d3acb448223813
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320781"
---
# <a name="media-source-events"></a><span data-ttu-id="865af-103">Eventi di origine dei supporti</span><span class="sxs-lookup"><span data-stu-id="865af-103">Media Source Events</span></span>

<span data-ttu-id="865af-104">Questo argomento elenca gli eventi inviati da origini multimediali e flussi multimediali.</span><span class="sxs-lookup"><span data-stu-id="865af-104">This topic lists the events that are sent by media sources and media streams.</span></span> <span data-ttu-id="865af-105">Le origini supporto possono anche inviare eventi personalizzati non elencati qui.</span><span class="sxs-lookup"><span data-stu-id="865af-105">Media sources can also send custom events not listed here.</span></span>

## <a name="media-source-events"></a><span data-ttu-id="865af-106">Eventi di origine dei supporti</span><span class="sxs-lookup"><span data-stu-id="865af-106">Media Source Events</span></span>



| <span data-ttu-id="865af-107">Event</span><span class="sxs-lookup"><span data-stu-id="865af-107">Event</span></span>                                                                      | <span data-ttu-id="865af-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="865af-108">Description</span></span>                                                                                      |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="865af-109">Evento MEEndOfPresentation</span><span class="sxs-lookup"><span data-stu-id="865af-109">MEEndOfPresentation Event</span></span>](meendofpresentation.md)                       | <span data-ttu-id="865af-110">Presentazione terminata.</span><span class="sxs-lookup"><span data-stu-id="865af-110">The presentation ended.</span></span> <span data-ttu-id="865af-111">Tutti i flussi nella presentazione hanno raggiunto la fine del flusso.</span><span class="sxs-lookup"><span data-stu-id="865af-111">All streams in the presentation have reached the end of the stream.</span></span>      |
| [<span data-ttu-id="865af-112">Evento MENewStream</span><span class="sxs-lookup"><span data-stu-id="865af-112">MENewStream Event</span></span>](menewstream.md)                                       | <span data-ttu-id="865af-113">È stato creato un nuovo flusso.</span><span class="sxs-lookup"><span data-stu-id="865af-113">A new stream was created.</span></span> <span data-ttu-id="865af-114">L'evento contiene un puntatore al flusso.</span><span class="sxs-lookup"><span data-stu-id="865af-114">The event contains a pointer to the stream.</span></span>                            |
| [<span data-ttu-id="865af-115">Evento MESourceCharacteristicsChanged</span><span class="sxs-lookup"><span data-stu-id="865af-115">MESourceCharacteristicsChanged Event</span></span>](mesourcecharacteristicschanged.md) | <span data-ttu-id="865af-116">Le caratteristiche dell'origine sono state modificate.</span><span class="sxs-lookup"><span data-stu-id="865af-116">The characteristics of the source have changed.</span></span> <span data-ttu-id="865af-117">Facoltativo.</span><span class="sxs-lookup"><span data-stu-id="865af-117">(Optional.)</span></span>                                      |
| [<span data-ttu-id="865af-118">Evento MESourceMetadataChanged</span><span class="sxs-lookup"><span data-stu-id="865af-118">MESourceMetadataChanged Event</span></span>](mesourcemetadatachanged.md)               | <span data-ttu-id="865af-119">I metadati dell'origine sono stati modificati.</span><span class="sxs-lookup"><span data-stu-id="865af-119">The source's metadata has changed.</span></span> <span data-ttu-id="865af-120">Facoltativo.</span><span class="sxs-lookup"><span data-stu-id="865af-120">(Optional.)</span></span>                                                   |
| [<span data-ttu-id="865af-121">Evento MESourcePaused</span><span class="sxs-lookup"><span data-stu-id="865af-121">MESourcePaused Event</span></span>](mesourcepaused.md)                                 | <span data-ttu-id="865af-122">L'origine è stata sospesa.</span><span class="sxs-lookup"><span data-stu-id="865af-122">The source was paused.</span></span> <span data-ttu-id="865af-123">Non tutte le origini supportano la sospensione.</span><span class="sxs-lookup"><span data-stu-id="865af-123">Not all sources support pausing.</span></span>                                          |
| [<span data-ttu-id="865af-124">Evento MESourceRateChanged</span><span class="sxs-lookup"><span data-stu-id="865af-124">MESourceRateChanged Event</span></span>](mesourceratechanged.md)                       | <span data-ttu-id="865af-125">La frequenza di riproduzione dell'origine è cambiata.</span><span class="sxs-lookup"><span data-stu-id="865af-125">The source's playback rate has changed.</span></span> <span data-ttu-id="865af-126">(Facoltativo; si applica se l'origine supporta il controllo della frequenza).</span><span class="sxs-lookup"><span data-stu-id="865af-126">(Optional; applies if the source supports rate control.)</span></span> |
| [<span data-ttu-id="865af-127">Evento MESourceRateChangeRequested</span><span class="sxs-lookup"><span data-stu-id="865af-127">MESourceRateChangeRequested Event</span></span>](mesourceratechangerequested.md)       | <span data-ttu-id="865af-128">L'origine richiede una nuova velocità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="865af-128">The source is requesting a new playback rate.</span></span> <span data-ttu-id="865af-129">Facoltativo.</span><span class="sxs-lookup"><span data-stu-id="865af-129">(Optional.)</span></span>                                        |
| [<span data-ttu-id="865af-130">Evento MESourceSeeked</span><span class="sxs-lookup"><span data-stu-id="865af-130">MESourceSeeked Event</span></span>](mesourceseeked.md)                                 | <span data-ttu-id="865af-131">L'origine è stata ricercata.</span><span class="sxs-lookup"><span data-stu-id="865af-131">The source was seeked.</span></span> <span data-ttu-id="865af-132">Non tutte le origini supportano la ricerca.</span><span class="sxs-lookup"><span data-stu-id="865af-132">Not all sources support seeking.</span></span>                                          |
| [<span data-ttu-id="865af-133">Evento MESourceStarted</span><span class="sxs-lookup"><span data-stu-id="865af-133">MESourceStarted Event</span></span>](mesourcestarted.md)                               | <span data-ttu-id="865af-134">Origine avviata.</span><span class="sxs-lookup"><span data-stu-id="865af-134">The source was started.</span></span>                                                                          |
| [<span data-ttu-id="865af-135">Evento MESourceStopped</span><span class="sxs-lookup"><span data-stu-id="865af-135">MESourceStopped Event</span></span>](mesourcestopped.md)                               | <span data-ttu-id="865af-136">Origine arrestata.</span><span class="sxs-lookup"><span data-stu-id="865af-136">The source was stopped.</span></span>                                                                          |
| [<span data-ttu-id="865af-137">Evento MEUpdatedStream</span><span class="sxs-lookup"><span data-stu-id="865af-137">MEUpdatedStream Event</span></span>](meupdatedstream.md)                               | <span data-ttu-id="865af-138">Un flusso esistente è stato cercato o riavviato.</span><span class="sxs-lookup"><span data-stu-id="865af-138">An existing stream was seeked or re-started.</span></span> <span data-ttu-id="865af-139">L'evento contiene un puntatore al flusso.</span><span class="sxs-lookup"><span data-stu-id="865af-139">The event contains a pointer to the stream.</span></span>         |



 

## <a name="media-stream-events"></a><span data-ttu-id="865af-140">Eventi del flusso multimediale</span><span class="sxs-lookup"><span data-stu-id="865af-140">Media Stream Events</span></span>



| <span data-ttu-id="865af-141">Event</span><span class="sxs-lookup"><span data-stu-id="865af-141">Event</span></span>                                                    | <span data-ttu-id="865af-142">Descrizione</span><span class="sxs-lookup"><span data-stu-id="865af-142">Description</span></span>                                                                                                                    |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="865af-143">Evento MEEndOfStream</span><span class="sxs-lookup"><span data-stu-id="865af-143">MEEndOfStream Event</span></span>](meendofstream.md)                 | <span data-ttu-id="865af-144">Il flusso è terminato.</span><span class="sxs-lookup"><span data-stu-id="865af-144">The stream ended.</span></span>                                                                                                              |
| [<span data-ttu-id="865af-145">Evento MEError</span><span class="sxs-lookup"><span data-stu-id="865af-145">MEError Event</span></span>](meerror.md)                             | <span data-ttu-id="865af-146">Si è verificato un errore durante il flusso.</span><span class="sxs-lookup"><span data-stu-id="865af-146">An error has occurred during streaming.</span></span> <span data-ttu-id="865af-147">Utilizzare questo evento per gli errori non correlati ad altri eventi elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="865af-147">Use this event for errors that are not related to any of the other events listed here.</span></span> |
| [<span data-ttu-id="865af-148">Evento MEMediaSample</span><span class="sxs-lookup"><span data-stu-id="865af-148">MEMediaSample Event</span></span>](memediasample.md)                 | <span data-ttu-id="865af-149">Il flusso ha generato un nuovo esempio.</span><span class="sxs-lookup"><span data-stu-id="865af-149">The stream has generated a new sample.</span></span>                                                                                         |
| [<span data-ttu-id="865af-150">Evento MEStreamFormatChanged</span><span class="sxs-lookup"><span data-stu-id="865af-150">MEStreamFormatChanged Event</span></span>](mestreamformatchanged.md) | <span data-ttu-id="865af-151">Il tipo di supporto è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="865af-151">The media type has changed.</span></span> <span data-ttu-id="865af-152">Facoltativo.</span><span class="sxs-lookup"><span data-stu-id="865af-152">(Optional.)</span></span>                                                                                        |
| [<span data-ttu-id="865af-153">Evento MEStreamPaused</span><span class="sxs-lookup"><span data-stu-id="865af-153">MEStreamPaused Event</span></span>](mestreampaused.md)               | <span data-ttu-id="865af-154">Il flusso è stato sospeso.</span><span class="sxs-lookup"><span data-stu-id="865af-154">The stream was paused.</span></span>                                                                                                         |
| [<span data-ttu-id="865af-155">Evento MEStreamSeeked</span><span class="sxs-lookup"><span data-stu-id="865af-155">MEStreamSeeked Event</span></span>](mestreamseeked.md)               | <span data-ttu-id="865af-156">Il flusso è stato cercato.</span><span class="sxs-lookup"><span data-stu-id="865af-156">The stream was seeked.</span></span>                                                                                                         |
| [<span data-ttu-id="865af-157">Evento MEStreamStarted</span><span class="sxs-lookup"><span data-stu-id="865af-157">MEStreamStarted Event</span></span>](mestreamstarted.md)             | <span data-ttu-id="865af-158">Il flusso è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="865af-158">The stream was started.</span></span>                                                                                                        |
| [<span data-ttu-id="865af-159">Evento MEStreamStopped</span><span class="sxs-lookup"><span data-stu-id="865af-159">MEStreamStopped Event</span></span>](mestreamstopped.md)             | <span data-ttu-id="865af-160">Il flusso è stato interrotto.</span><span class="sxs-lookup"><span data-stu-id="865af-160">The stream was stopped.</span></span>                                                                                                        |
| [<span data-ttu-id="865af-161">Evento MEStreamThinMode</span><span class="sxs-lookup"><span data-stu-id="865af-161">MEStreamThinMode Event</span></span>](mestreamthinmode.md)           | <span data-ttu-id="865af-162">La modalità di assottigliamento è stata avviata o arrestata.</span><span class="sxs-lookup"><span data-stu-id="865af-162">Thinning mode has started or stopped.</span></span> <span data-ttu-id="865af-163">Facoltativo.</span><span class="sxs-lookup"><span data-stu-id="865af-163">(Optional.)</span></span>                                                                              |
| [<span data-ttu-id="865af-164">Evento MEStreamTick</span><span class="sxs-lookup"><span data-stu-id="865af-164">MEStreamTick Event</span></span>](mestreamtick.md)                   | <span data-ttu-id="865af-165">Si è verificato un gap nel flusso.</span><span class="sxs-lookup"><span data-stu-id="865af-165">There is a gap in the stream.</span></span> <span data-ttu-id="865af-166">Facoltativo.</span><span class="sxs-lookup"><span data-stu-id="865af-166">(Optional.)</span></span>                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="865af-167">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="865af-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="865af-168">Origini supporti</span><span class="sxs-lookup"><span data-stu-id="865af-168">Media Sources</span></span>](media-sources.md)
</dt> </dl>

 

 



