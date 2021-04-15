---
description: Attributi dell'evento
ms.assetid: 25e77ee1-cffc-4f8b-ac07-b5607a125fc7
title: Attributi evento (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 633e8f3857582422fe4a2d65ba34e68be483e7aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524530"
---
# <a name="event-attributes-microsoft-media-foundation"></a><span data-ttu-id="8cac4-103">Attributi evento (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="8cac4-103">Event Attributes (Microsoft Media Foundation)</span></span>

<span data-ttu-id="8cac4-104">Gli attributi seguenti si applicano agli eventi.</span><span class="sxs-lookup"><span data-stu-id="8cac4-104">The following attributes apply to events.</span></span>



| <span data-ttu-id="8cac4-105">Attributo</span><span class="sxs-lookup"><span data-stu-id="8cac4-105">Attribute</span></span>                                                                                                        | <span data-ttu-id="8cac4-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8cac4-106">Description</span></span>                                                                                                           |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8cac4-107">**MF \_ evento \_ do \_ assottigliamento**</span><span class="sxs-lookup"><span data-stu-id="8cac4-107">**MF\_EVENT\_DO\_THINNING**</span></span>](mf-event-do-thinning-attribute.md)                                                | <span data-ttu-id="8cac4-108">Quando un'origine multimediale richiede una nuova velocità di riproduzione, specifica se l'origine richiede anche l'assottigliamento.</span><span class="sxs-lookup"><span data-stu-id="8cac4-108">When a media source requests a new playback rate, specifies whether the source also requests thinning.</span></span>                |
| [<span data-ttu-id="8cac4-109">**\_nodo di \_ output \_ evento MF**</span><span class="sxs-lookup"><span data-stu-id="8cac4-109">**MF\_EVENT\_OUTPUT\_NODE**</span></span>](mf-event-output-node-attribute.md)                                                | <span data-ttu-id="8cac4-110">Identifica il nodo della topologia per un sink di flusso.</span><span class="sxs-lookup"><span data-stu-id="8cac4-110">Identifies the topology node for a stream sink.</span></span>                                                                       |
| [<span data-ttu-id="8cac4-111">**\_ \_ \_ offset ora presentazione evento \_ MF**</span><span class="sxs-lookup"><span data-stu-id="8cac4-111">**MF\_EVENT\_PRESENTATION\_TIME\_OFFSET**</span></span>](mf-event-presentation-time-offset-attribute.md)                     | <span data-ttu-id="8cac4-112">Offset tra l'ora di presentazione e i timestamp dell'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="8cac4-112">Offset between the presentation time and the media source's time stamps.</span></span>                                              |
| [<span data-ttu-id="8cac4-113">**\_tempo di \_ SCRUBSAMPLE \_ evento MF**</span><span class="sxs-lookup"><span data-stu-id="8cac4-113">**MF\_EVENT\_SCRUBSAMPLE\_TIME**</span></span>](mf-event-scrubsample-time-attribute.md)                                      | <span data-ttu-id="8cac4-114">Tempo di presentazione per un esempio di cui è stato eseguito il rendering durante lo scrubbing.</span><span class="sxs-lookup"><span data-stu-id="8cac4-114">Presentation time for a sample that was rendered while scrubbing.</span></span>                                                     |
| [<span data-ttu-id="8cac4-115">**\_SESSIONCAPS evento \_ MF**</span><span class="sxs-lookup"><span data-stu-id="8cac4-115">**MF\_EVENT\_SESSIONCAPS**</span></span>](mf-event-sessioncaps-attribute.md)                                                 | <span data-ttu-id="8cac4-116">Contiene i flag che definiscono le funzionalità della sessione multimediale in base alla presentazione corrente.</span><span class="sxs-lookup"><span data-stu-id="8cac4-116">Contains flags that define the capabilities of the Media Session, based on the current presentation.</span></span>                  |
| [<span data-ttu-id="8cac4-117">**\_ \_ Delta SESSIONCAPS evento \_ MF**</span><span class="sxs-lookup"><span data-stu-id="8cac4-117">**MF\_EVENT\_SESSIONCAPS\_DELTA**</span></span>](mf-event-sessioncaps-delta-attribute.md)                                    | <span data-ttu-id="8cac4-118">Contiene flag che indicano quali funzionalità sono state modificate nella sessione multimediale, in base alla presentazione corrente.</span><span class="sxs-lookup"><span data-stu-id="8cac4-118">Contains flags that indicate which capabilities have changed in the Media Session, based on the current presentation.</span></span> |
| [<span data-ttu-id="8cac4-119">**\_ \_ \_ inizio effettivo origine evento \_ MF**</span><span class="sxs-lookup"><span data-stu-id="8cac4-119">**MF\_EVENT\_SOURCE\_ACTUAL\_START**</span></span>](mf-event-source-actual-start-attribute.md)                               | <span data-ttu-id="8cac4-120">Contiene l'ora di inizio del riavvio di un'origine multimediale dalla posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="8cac4-120">Contains the start time when a media source restarts from its current position.</span></span>                                       |
| [<span data-ttu-id="8cac4-121">**\_caratteristiche dell' \_ origine \_ evento MF**</span><span class="sxs-lookup"><span data-stu-id="8cac4-121">**MF\_EVENT\_SOURCE\_CHARACTERISTICS**</span></span>](mf-event-source-characteristics-attribute.md)                          | <span data-ttu-id="8cac4-122">Specifica le caratteristiche correnti dell'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="8cac4-122">Specifies the current characteristics of the media source.</span></span>                                                            |
| [<span data-ttu-id="8cac4-123">**\_ \_ caratteristiche origine evento \_ MF \_ obsolete**</span><span class="sxs-lookup"><span data-stu-id="8cac4-123">**MF\_EVENT\_SOURCE\_CHARACTERISTICS\_OLD**</span></span>](mf-event-source-characteristics-old-attribute.md)                 | <span data-ttu-id="8cac4-124">Specifica le caratteristiche precedenti dell'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="8cac4-124">Specifies the previous characteristics of the media source.</span></span>                                                           |
| [<span data-ttu-id="8cac4-125">**\_ \_ \_ inizio Fake origine evento \_ MF**</span><span class="sxs-lookup"><span data-stu-id="8cac4-125">**MF\_EVENT\_SOURCE\_FAKE\_START**</span></span>](mf-event-source-fake-start-attribute.md)                                   | <span data-ttu-id="8cac4-126">Specifica se la topologia del segmento corrente è vuota.</span><span class="sxs-lookup"><span data-stu-id="8cac4-126">Specifies whether the current segment topology is empty.</span></span>                                                              |
| [<span data-ttu-id="8cac4-127">**\_origine evento \_ MF \_ PROJECTSTART**</span><span class="sxs-lookup"><span data-stu-id="8cac4-127">**MF\_EVENT\_SOURCE\_PROJECTSTART**</span></span>](mf-event-source-projectstart-attribute.md)                                | <span data-ttu-id="8cac4-128">Specifica l'ora di inizio per una topologia di segmento.</span><span class="sxs-lookup"><span data-stu-id="8cac4-128">Specifies the start time for a segment topology.</span></span>                                                                      |
| [<span data-ttu-id="8cac4-129">**\_ \_ topologia di origine evento MF \_ \_ annullata**</span><span class="sxs-lookup"><span data-stu-id="8cac4-129">**MF\_EVENT\_SOURCE\_TOPOLOGY\_CANCELED**</span></span>](mf-event-source-topology-canceled-attribute.md)                     | <span data-ttu-id="8cac4-130">Specifica se l'origine del sequencer ha annullato una topologia.</span><span class="sxs-lookup"><span data-stu-id="8cac4-130">Specifies whether the sequencer source canceled a topology.</span></span>                                                           |
| [<span data-ttu-id="8cac4-131">**\_ora di \_ presentazione di inizio evento \_ MF \_**</span><span class="sxs-lookup"><span data-stu-id="8cac4-131">**MF\_EVENT\_START\_PRESENTATION\_TIME**</span></span>](mf-event-start-presentation-time-attribute.md)                       | <span data-ttu-id="8cac4-132">Ora di inizio per la presentazione, in unità di 100 nanosecondi, misurata dal clock di presentazione.</span><span class="sxs-lookup"><span data-stu-id="8cac4-132">The starting time for the presentation, in 100-nanosecond units, as measured by the presentation clock.</span></span>               |
| [<span data-ttu-id="8cac4-133">**\_ \_ \_ \_ ora di presentazione dell'avvio \_ dell'evento MF nell' \_ output**</span><span class="sxs-lookup"><span data-stu-id="8cac4-133">**MF\_EVENT\_START\_PRESENTATION\_TIME\_AT\_OUTPUT**</span></span>](mf-event-start-presentation-time-at-output-attribute.md) | <span data-ttu-id="8cac4-134">Ora di presentazione in cui i sink dei supporti eseguiranno il rendering del primo campione della nuova topologia.</span><span class="sxs-lookup"><span data-stu-id="8cac4-134">The presentation time at which the media sinks will render the first sample of the new topology.</span></span>                      |
| [<span data-ttu-id="8cac4-135">**\_ \_ stato topologia evento MF \_**</span><span class="sxs-lookup"><span data-stu-id="8cac4-135">**MF\_EVENT\_TOPOLOGY\_STATUS**</span></span>](mf-event-topology-status-attribute.md)                                        | <span data-ttu-id="8cac4-136">Specifica lo stato di una topologia durante la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="8cac4-136">Specifies the status of a topology during playback.</span></span>                                                                   |
| [<span data-ttu-id="8cac4-137">**\_tempo di \_ \_ \_ ricorrenza \_ evento MF Session approx**</span><span class="sxs-lookup"><span data-stu-id="8cac4-137">**MF\_SESSION\_APPROX\_EVENT\_OCCURRENCE\_TIME**</span></span>](mf-session-approx-event-occurrence-time-attribute.md)        | <span data-ttu-id="8cac4-138">Ora approssimativa in cui la sessione multimediale ha generato un evento.</span><span class="sxs-lookup"><span data-stu-id="8cac4-138">The approximate time when the Media Session raised an event.</span></span>                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="8cac4-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8cac4-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8cac4-140">**IMFMediaEvent**</span><span class="sxs-lookup"><span data-stu-id="8cac4-140">**IMFMediaEvent**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)
</dt> <dt>

[<span data-ttu-id="8cac4-141">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8cac4-141">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="8cac4-142">Attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8cac4-142">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 



