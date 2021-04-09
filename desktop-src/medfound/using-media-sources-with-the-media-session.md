---
description: Uso di origini multimediali con la sessione multimediale
ms.assetid: b50d3d6e-728b-4ba5-9b79-413d2108ade1
title: Uso di origini multimediali con la sessione multimediale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf08edf1d68ea11b05e8f8db83e247bc844cd85c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103968890"
---
# <a name="using-media-sources-with-the-media-session"></a><span data-ttu-id="c1269-103">Uso di origini multimediali con la sessione multimediale</span><span class="sxs-lookup"><span data-stu-id="c1269-103">Using Media Sources with the Media Session</span></span>

<span data-ttu-id="c1269-104">Se si usa la sessione multimediale per controllare la riproduzione, il set di metodi che è necessario chiamare su un'origine multimediale è limitato.</span><span class="sxs-lookup"><span data-stu-id="c1269-104">If you are using the Media Session to control playback, the set of methods that you should call on a media source is restricted.</span></span> <span data-ttu-id="c1269-105">Questa sezione descrive come usare l'origine dei supporti insieme alla sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="c1269-105">This section describes how to use media source in conjunction with the Media Session.</span></span>

<span data-ttu-id="c1269-106">Ecco i passaggi di base che verranno eseguiti dall'applicazione:</span><span class="sxs-lookup"><span data-stu-id="c1269-106">Here are the basic steps your application will perform:</span></span>

1.  <span data-ttu-id="c1269-107">Creare l'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="c1269-107">Create the media source.</span></span> <span data-ttu-id="c1269-108">Per creare un'origine multimediale, usare il resolver di origine.</span><span class="sxs-lookup"><span data-stu-id="c1269-108">To create a media source, use the source resolver.</span></span> <span data-ttu-id="c1269-109">Per ulteriori informazioni, vedere [resolver di origine](source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="c1269-109">For more information, see [Source Resolver](source-resolver.md).</span></span> <span data-ttu-id="c1269-110">Il resolver di origine restituisce un puntatore all'interfaccia [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) dell'origine.</span><span class="sxs-lookup"><span data-stu-id="c1269-110">The source resolver returns a pointer to the source's [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface.</span></span> <span data-ttu-id="c1269-111">Se è stata scritta un'origine multimediale personalizzata, è possibile specificare invece un metodo di creazione personalizzato.</span><span class="sxs-lookup"><span data-stu-id="c1269-111">(If you have written a custom media source, you can provide a custom creation method instead.)</span></span>

2.  <span data-ttu-id="c1269-112">Configurare la presentazione.</span><span class="sxs-lookup"><span data-stu-id="c1269-112">Configure the presentation.</span></span> <span data-ttu-id="c1269-113">Per configurare la presentazione dell'origine, chiamare [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="c1269-113">To configure the source's presentation, call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span> <span data-ttu-id="c1269-114">È possibile modificare questa copia, ma le modifiche non diventano attive fino a quando non viene avviata la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="c1269-114">You can modify this copy, but the changes do not become active until the playback starts.</span></span> <span data-ttu-id="c1269-115">Non modificare il descrittore della presentazione durante la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="c1269-115">Do not modify the presentation descriptor during playback.</span></span> <span data-ttu-id="c1269-116">Per ulteriori informazioni, vedere [descrittori di presentazione](presentation-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="c1269-116">For more information, see [Presentation Descriptors](presentation-descriptors.md).</span></span>

3.  <span data-ttu-id="c1269-117">Creare una topologia che contenga l'origine del supporto.</span><span class="sxs-lookup"><span data-stu-id="c1269-117">Create a topology that contains the media source.</span></span> <span data-ttu-id="c1269-118">Per ulteriori informazioni, vedere [topologie](topologies.md).</span><span class="sxs-lookup"><span data-stu-id="c1269-118">For more information, see [Topologies](topologies.md).</span></span>

4.  <span data-ttu-id="c1269-119">Usare la sessione multimediale per controllare la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="c1269-119">Use the Media Session to control playback.</span></span> <span data-ttu-id="c1269-120">La sessione multimediale chiama i metodi sull'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="c1269-120">The Media Session calls methods on the media source.</span></span> <span data-ttu-id="c1269-121">Al momento l'applicazione non deve chiamare alcun metodo sull'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="c1269-121">The application should not call any methods on the media source at this time.</span></span>

5.  <span data-ttu-id="c1269-122">Prima di rilasciare l'origine del supporto, chiamare [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) per arrestare l'origine.</span><span class="sxs-lookup"><span data-stu-id="c1269-122">Before releasing the media source, call [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) to shut down the source.</span></span>

    > [!Note]  
    > <span data-ttu-id="c1269-123">Se si utilizza l'origine sequencer, l'origine del sequencer gestisce la chiusura delle origini del segmento.</span><span class="sxs-lookup"><span data-stu-id="c1269-123">If you are using the sequencer source, the sequencer source handles shutting down the segment sources.</span></span> <span data-ttu-id="c1269-124">Per ulteriori informazioni, vedere [sequencer source](sequencer-source.md).</span><span class="sxs-lookup"><span data-stu-id="c1269-124">For more information, see [Sequencer Source](sequencer-source.md).</span></span>

     

<span data-ttu-id="c1269-125">Se si usa la sessione multimediale, gli unici metodi che è necessario chiamare sull'origine del supporto sono [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor), [**getcaratteristiche**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-getcharacteristics)e [**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span><span class="sxs-lookup"><span data-stu-id="c1269-125">If you use the Media Session, the only methods that you should call on the media source are [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor), [**GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-getcharacteristics), and [**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span></span> <span data-ttu-id="c1269-126">In particolare:</span><span class="sxs-lookup"><span data-stu-id="c1269-126">In particular:</span></span>

-   <span data-ttu-id="c1269-127">Non chiamare [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start), [**pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause)o [**Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop); questi metodi devono essere chiamati solo dalla sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="c1269-127">Do not call [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start), [**Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause), or [**Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop); these methods should be called only by the Media Session.</span></span>

-   <span data-ttu-id="c1269-128">Non chiamare alcun metodo [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) .</span><span class="sxs-lookup"><span data-stu-id="c1269-128">Do not call any [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) methods.</span></span>

-   <span data-ttu-id="c1269-129">Non recuperare gli eventi direttamente dall'origine supporto o da uno dei flussi.</span><span class="sxs-lookup"><span data-stu-id="c1269-129">Do not retrieve events directly from the media source or any of the streams.</span></span> <span data-ttu-id="c1269-130">Per il corretto funzionamento della pipeline, la sessione multimediale deve ricevere questi eventi.</span><span class="sxs-lookup"><span data-stu-id="c1269-130">The Media Session must receive these events for the pipeline to function correctly.</span></span> <span data-ttu-id="c1269-131">La sessione multimediale trasmette tutti gli eventi necessari per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c1269-131">The Media Session forwards any events that are needed by the application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c1269-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c1269-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1269-133">Sessione multimediale</span><span class="sxs-lookup"><span data-stu-id="c1269-133">Media Session</span></span>](media-session.md)
</dt> </dl>

 

 



