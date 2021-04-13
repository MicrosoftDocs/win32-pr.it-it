---
description: Modello a oggetti di origine multimediale
ms.assetid: 88373028-8a34-4bf1-8300-d1a7e4c7dd75
title: Modello a oggetti di origine multimediale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0d05cc9d5341bff433d6276b5ee67505361b78f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351531"
---
# <a name="media-source-object-model"></a><span data-ttu-id="ee7f2-103">Modello a oggetti di origine multimediale</span><span class="sxs-lookup"><span data-stu-id="ee7f2-103">Media Source Object Model</span></span>

<span data-ttu-id="ee7f2-104">Questo argomento descrive il modello a oggetti per le origini multimediali in Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="ee7f2-104">This topic describes the object model for media sources in Microsoft Media Foundation.</span></span> <span data-ttu-id="ee7f2-105">Un'origine multimediale deve implementare due oggetti:</span><span class="sxs-lookup"><span data-stu-id="ee7f2-105">A media source must implement two objects:</span></span>

-   <span data-ttu-id="ee7f2-106">Descrittore di presentazione che descrive il contenuto dell'origine, inclusi il numero di flussi e il formato di ogni flusso.</span><span class="sxs-lookup"><span data-stu-id="ee7f2-106">A presentation descriptor, which describes the contents of the source, including the number of streams and the format of each stream.</span></span> <span data-ttu-id="ee7f2-107">Per ulteriori informazioni sui descrittori di presentazione, vedere [descrittori di presentazione](presentation-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="ee7f2-107">For more information about presentation descriptors, see [Presentation Descriptors](presentation-descriptors.md).</span></span>
-   <span data-ttu-id="ee7f2-108">Uno o più flussi multimediali, che generano i dati di origine.</span><span class="sxs-lookup"><span data-stu-id="ee7f2-108">One or more media streams, which generate the source data.</span></span>

<span data-ttu-id="ee7f2-109">L'origine non crea i flussi fino a quando non viene avviata la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="ee7f2-109">The source does not create the streams until playback starts.</span></span>

## <a name="media-source-interfaces"></a><span data-ttu-id="ee7f2-110">Interfacce di origine dei supporti</span><span class="sxs-lookup"><span data-stu-id="ee7f2-110">Media Source Interfaces</span></span>

<span data-ttu-id="ee7f2-111">Un'origine multimediale deve esporre le interfacce seguenti tramite **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="ee7f2-111">A media source must expose the following interfaces through **QueryInterface**.</span></span>



| <span data-ttu-id="ee7f2-112">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="ee7f2-112">Interface</span></span>                                                | <span data-ttu-id="ee7f2-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee7f2-113">Description</span></span>                                                                                                     |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ee7f2-114">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="ee7f2-114">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                 | <span data-ttu-id="ee7f2-115">Obbligatorio per tutte le origini supporti.</span><span class="sxs-lookup"><span data-stu-id="ee7f2-115">Required for all media sources.</span></span>                                                                                 |
| [<span data-ttu-id="ee7f2-116">**IMFMediaEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="ee7f2-116">**IMFMediaEventGenerator**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) | <span data-ttu-id="ee7f2-117">Obbligatorio per tutte le origini supporti.</span><span class="sxs-lookup"><span data-stu-id="ee7f2-117">Required for all media sources.</span></span> <span data-ttu-id="ee7f2-118">L'interfaccia [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) eredita questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="ee7f2-118">The [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface inherits this interface.</span></span> |



 

<span data-ttu-id="ee7f2-119">Facoltativamente, un'origine multimediale può implementare l'interfaccia [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) e implementare una delle interfacce seguenti come servizi:</span><span class="sxs-lookup"><span data-stu-id="ee7f2-119">Optionally, a media source can implement the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface and implement any of the following interfaces as services:</span></span>



| <span data-ttu-id="ee7f2-120">Interfaccia del servizio</span><span class="sxs-lookup"><span data-stu-id="ee7f2-120">Service interface</span></span>                                  | <span data-ttu-id="ee7f2-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee7f2-121">Description</span></span>                                                       |
|----------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="ee7f2-122">**IMFRateControl**</span><span class="sxs-lookup"><span data-stu-id="ee7f2-122">**IMFRateControl**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)           | <span data-ttu-id="ee7f2-123">Controlla la velocità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="ee7f2-123">Controls the playback rate.</span></span>                                       |
| [<span data-ttu-id="ee7f2-124">**IMFRateSupport**</span><span class="sxs-lookup"><span data-stu-id="ee7f2-124">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)           | <span data-ttu-id="ee7f2-125">Segnala l'intervallo di frequenze di riproduzione supportate.</span><span class="sxs-lookup"><span data-stu-id="ee7f2-125">Reports the range of playback rates that are supported.</span></span>           |
| [<span data-ttu-id="ee7f2-126">**IMFQualityAdvise**</span><span class="sxs-lookup"><span data-stu-id="ee7f2-126">**IMFQualityAdvise**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)       | <span data-ttu-id="ee7f2-127">Consente al gestore della qualità di regolare la qualità audio o video.</span><span class="sxs-lookup"><span data-stu-id="ee7f2-127">Enables the quality manager to adjust the audio or video quality.</span></span> |
| [<span data-ttu-id="ee7f2-128">**IMFMetadataProvider**</span><span class="sxs-lookup"><span data-stu-id="ee7f2-128">**IMFMetadataProvider**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) | <span data-ttu-id="ee7f2-129">Fornisce i metadati.</span><span class="sxs-lookup"><span data-stu-id="ee7f2-129">Provides metadata.</span></span>                                                |



 

<span data-ttu-id="ee7f2-130">Se l'origine supporto può essere riprodotto a frequenze diverse dalla velocità normale (1,0), deve esporre il servizio di controllo della velocità ([**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) e [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)).</span><span class="sxs-lookup"><span data-stu-id="ee7f2-130">If the media source can play at rates other than normal speed (1.0), it should expose the rate control service ([**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) and [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)).</span></span> <span data-ttu-id="ee7f2-131">In caso contrario, si presuppone che l'origine supporti solo la riproduzione alla velocità normale.</span><span class="sxs-lookup"><span data-stu-id="ee7f2-131">Otherwise, it is assumed that the source only supports playback at normal speed.</span></span> <span data-ttu-id="ee7f2-132">Per ulteriori informazioni, vedere [implementazione del controllo della frequenza](implementing-rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="ee7f2-132">For more information, see [Implementing Rate Control](implementing-rate-control.md).</span></span>

<span data-ttu-id="ee7f2-133">Per ulteriori informazioni sulle interfacce del servizio e [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice), vedere [interfacce di servizio](service-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="ee7f2-133">For more information about service interfaces and [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice), see [Service Interfaces](service-interfaces.md).</span></span>

## <a name="media-stream-interfaces"></a><span data-ttu-id="ee7f2-134">Interfacce del flusso multimediale</span><span class="sxs-lookup"><span data-stu-id="ee7f2-134">Media Stream Interfaces</span></span>

<span data-ttu-id="ee7f2-135">I flussi multimediali devono implementare le interfacce seguenti.</span><span class="sxs-lookup"><span data-stu-id="ee7f2-135">Media streams must implement the following interfaces.</span></span>



| <span data-ttu-id="ee7f2-136">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="ee7f2-136">Interface</span></span>                                                | <span data-ttu-id="ee7f2-137">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee7f2-137">Description</span></span>                                                                                                     |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ee7f2-138">**IMFMediaStream**</span><span class="sxs-lookup"><span data-stu-id="ee7f2-138">**IMFMediaStream**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)                 | <span data-ttu-id="ee7f2-139">Obbligatorio per tutti i flussi multimediali.</span><span class="sxs-lookup"><span data-stu-id="ee7f2-139">Required for all media streams.</span></span>                                                                                 |
| [<span data-ttu-id="ee7f2-140">**IMFMediaEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="ee7f2-140">**IMFMediaEventGenerator**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) | <span data-ttu-id="ee7f2-141">Obbligatorio per tutti i flussi multimediali.</span><span class="sxs-lookup"><span data-stu-id="ee7f2-141">Required for all media streams.</span></span> <span data-ttu-id="ee7f2-142">L'interfaccia [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) eredita questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="ee7f2-142">The [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) interface inherits this interface.</span></span> |



 

<span data-ttu-id="ee7f2-143">Attualmente non sono definite interfacce del servizio per flussi multimediali.</span><span class="sxs-lookup"><span data-stu-id="ee7f2-143">Currently no service interfaces are defined for media streams.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ee7f2-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ee7f2-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee7f2-145">Origini supporti</span><span class="sxs-lookup"><span data-stu-id="ee7f2-145">Media Sources</span></span>](media-sources.md)
</dt> </dl>

 

 



