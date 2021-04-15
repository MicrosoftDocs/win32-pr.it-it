---
description: In questo argomento viene descritto come utilizzare i profili ASF in Microsoft Media Foundation.
ms.assetid: 03a0981b-29c3-450d-aa58-bc56a76e6cb6
title: Profilo ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 616670e7de68fd73c168c474544fc6236f1586e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524658"
---
# <a name="asf-profile"></a><span data-ttu-id="1a196-103">Profilo ASF</span><span class="sxs-lookup"><span data-stu-id="1a196-103">ASF Profile</span></span>

<span data-ttu-id="1a196-104">In questo argomento viene descritto come utilizzare i profili ASF in Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="1a196-104">This topic describes how to work with ASF profiles in Microsoft Media Foundation.</span></span>

<span data-ttu-id="1a196-105">Un file di formato di sistema avanzato (ASF) contiene uno o più flussi.</span><span class="sxs-lookup"><span data-stu-id="1a196-105">An Advanced Systems Format (ASF) file contains one or more streams.</span></span> <span data-ttu-id="1a196-106">Per ogni flusso, l'intestazione ASF contiene un'intestazione di proprietà del flusso che descrive il flusso.</span><span class="sxs-lookup"><span data-stu-id="1a196-106">For each stream, the ASF header contains a Stream Properties Header that describes the stream.</span></span> <span data-ttu-id="1a196-107">A livello di [WMContainer](wmcontainer-asf-components.md) , per impostare o leggere le proprietà dei flussi ASF vengono usati gli oggetti seguenti:</span><span class="sxs-lookup"><span data-stu-id="1a196-107">At the [WMContainer](wmcontainer-asf-components.md) layer, the following objects are used to set or read the properties of the ASF streams:</span></span>

-   <span data-ttu-id="1a196-108">Oggetto *profilo ASF* : descrive i flussi e le relazioni tra di essi.</span><span class="sxs-lookup"><span data-stu-id="1a196-108">*ASF profile* object: Describes the streams and their relationships with each other.</span></span> <span data-ttu-id="1a196-109">L'oggetto profilo ASF espone l'interfaccia [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) .</span><span class="sxs-lookup"><span data-stu-id="1a196-109">The ASF profile object exposes the [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) interface.</span></span>
-   <span data-ttu-id="1a196-110">Oggetto di *configurazione del flusso* : descrive un flusso.</span><span class="sxs-lookup"><span data-stu-id="1a196-110">*Stream configuration* object: Describes one stream.</span></span> <span data-ttu-id="1a196-111">L'oggetto di configurazione del flusso contiene un tipo di supporto che descrive il formato del flusso.</span><span class="sxs-lookup"><span data-stu-id="1a196-111">The stream configuration object contains a media type that describes the format of the stream.</span></span> <span data-ttu-id="1a196-112">Per i flussi audio e video, il tipo di supporto descrive esattamente il modo in cui il flusso viene configurato e viene usato dai codec che codificano o decodificano il flusso.</span><span class="sxs-lookup"><span data-stu-id="1a196-112">For audio and video streams, the media type describes exactly how the stream is configured, and is used by codecs that encode or decode the stream.</span></span> <span data-ttu-id="1a196-113">L'oggetto di configurazione del flusso espone l'interfaccia [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) .</span><span class="sxs-lookup"><span data-stu-id="1a196-113">The stream configuration object exposes the [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface.</span></span> <span data-ttu-id="1a196-114">Un profilo ASF valido contiene almeno un oggetto di configurazione del flusso.</span><span class="sxs-lookup"><span data-stu-id="1a196-114">A valid ASF profile contains at least one stream configuration object.</span></span>
-   <span data-ttu-id="1a196-115">Oggetto di *esclusione reciproca* : descrive più flussi che non sono previsti per la lettura simultanea.</span><span class="sxs-lookup"><span data-stu-id="1a196-115">*Mutual exclusion* object: Describes multiple streams that are not intended be read concurrently.</span></span> <span data-ttu-id="1a196-116">Un oggetto di esclusione reciproca espone l'interfaccia [**IMFASFMutualExclusion**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion) .</span><span class="sxs-lookup"><span data-stu-id="1a196-116">A mutual exclusion object exposes the [**IMFASFMutualExclusion**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion) interface.</span></span> <span data-ttu-id="1a196-117">Un profilo ASF contiene zero o più oggetti di esclusione reciproca.</span><span class="sxs-lookup"><span data-stu-id="1a196-117">An ASF profile contains zero or more mutual exclusion objects.</span></span>

<span data-ttu-id="1a196-118">Nel diagramma seguente viene illustrata la relazione tra il profilo ASF e gli oggetti contenuti nel profilo.</span><span class="sxs-lookup"><span data-stu-id="1a196-118">The following diagram shows the relationship between the ASF profile and the objects that are contained in the profile.</span></span>

![diagramma dell'albero di un nodo del profilo ASF con nodi figlio di configurazione del flusso; il primo punto per il tipo di supporto, i successivi due ad esclusione reciproca](images/asf-components02.png)

<span data-ttu-id="1a196-120">Per la riproduzione, il profilo ASF viene usato per enumerare i flussi e trovare i formati dei flussi.</span><span class="sxs-lookup"><span data-stu-id="1a196-120">For playback, the ASF profile is used to enumerate the streams and find the stream formats.</span></span> <span data-ttu-id="1a196-121">Per la codifica, il profilo ASF viene usato per configurare i flussi nel file di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1a196-121">For encoding, the ASF profile is used to configure the streams in the destination file.</span></span>

<span data-ttu-id="1a196-122">Il profilo ASF viene utilizzato anche per configurare il [sink multimediale ASF](asf-media-sinks.md).</span><span class="sxs-lookup"><span data-stu-id="1a196-122">The ASF profile is also used to configure the [ASF Media Sink](asf-media-sinks.md).</span></span> <span data-ttu-id="1a196-123">Per ogni flusso nel profilo ASF, il sink multimediale ASF crea un sink di flusso corrispondente.</span><span class="sxs-lookup"><span data-stu-id="1a196-123">For each stream in the ASF profile, the ASF media sink creates a corresponding stream sink.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1a196-124">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="1a196-124">In this section</span></span>



| <span data-ttu-id="1a196-125">Argomento</span><span class="sxs-lookup"><span data-stu-id="1a196-125">Topic</span></span>                                                                                           | <span data-ttu-id="1a196-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a196-126">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="1a196-127">Creazione di un profilo ASF</span><span class="sxs-lookup"><span data-stu-id="1a196-127">Creating an ASF Profile</span></span>](creating-an-asf-profile.md)<br/>                               | <span data-ttu-id="1a196-128">Viene descritto come creare un oggetto profilo ASF.</span><span class="sxs-lookup"><span data-stu-id="1a196-128">Describes how to create an ASF profile object.</span></span><br/>          |
| [<span data-ttu-id="1a196-129">Creazione e configurazione di flussi ASF</span><span class="sxs-lookup"><span data-stu-id="1a196-129">Creating and Configuring ASF Streams</span></span>](creating-and-configuring-asf-streams.md)<br/>     | <span data-ttu-id="1a196-130">Viene descritto come aggiungere flussi a un profilo ASF.</span><span class="sxs-lookup"><span data-stu-id="1a196-130">Describes how to add streams to an ASF profile.</span></span><br/>         |
| [<span data-ttu-id="1a196-131">Uso dell'esclusione reciproca per i flussi ASF</span><span class="sxs-lookup"><span data-stu-id="1a196-131">Using Mutual Exclusion for ASF Streams</span></span>](using-mutual-exclusion-for-asf-streams.md)<br/> | <span data-ttu-id="1a196-132">Viene descritto come aggiungere esclusioni reciproche ai flussi ASF.</span><span class="sxs-lookup"><span data-stu-id="1a196-132">Describes how to add mutual exclusions to ASF streams.</span></span> <br/> |



 

## <a name="related-topics"></a><span data-ttu-id="1a196-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1a196-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a196-134">Tipi di supporto</span><span class="sxs-lookup"><span data-stu-id="1a196-134">Media Types</span></span>](media-types.md)
</dt> <dt>

[<span data-ttu-id="1a196-135">Esercitazione: codifica Windows Media da 1 passaggio</span><span class="sxs-lookup"><span data-stu-id="1a196-135">Tutorial: 1-Pass Windows Media Encoding</span></span>](tutorial--1-pass-windows-media-encoding.md)
</dt> <dt>

[<span data-ttu-id="1a196-136">Esercitazione: scrittura di un file WMA usando la codifica CBR</span><span class="sxs-lookup"><span data-stu-id="1a196-136">Tutorial: Writing a WMA File by Using CBR Encoding</span></span>](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> <dt>

[<span data-ttu-id="1a196-137">Componenti ASF WMContainer</span><span class="sxs-lookup"><span data-stu-id="1a196-137">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> </dl>

 

 




