---
description: Origini supporti
ms.assetid: 65132e7d-22f6-4209-bc58-f5ea86ebd514
title: Origini supporti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbd69b63679ba73bc4049f37207b1d07940edada
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104234484"
---
# <a name="media-sources"></a><span data-ttu-id="cc623-103">Origini supporti</span><span class="sxs-lookup"><span data-stu-id="cc623-103">Media Sources</span></span>

<span data-ttu-id="cc623-104">Le *origini multimediali* sono oggetti che generano dati multimediali nella pipeline Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="cc623-104">*Media sources* are objects that generate media data in the Media Foundation pipeline.</span></span> <span data-ttu-id="cc623-105">In questa sezione vengono descritte in dettaglio le API di origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="cc623-105">This section describes the media source APIs in detail.</span></span> <span data-ttu-id="cc623-106">Leggere questa sezione se si sta implementando un'origine multimediale personalizzata o usando un'origine multimediale esterna alla pipeline Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="cc623-106">Read this section if you are implementing a custom media source, or using a media source outside of the Media Foundation pipeline.</span></span>

<span data-ttu-id="cc623-107">Se l'applicazione usa il livello di controllo, deve usare solo un subset limitato delle API di origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="cc623-107">If your application uses the control layer, it needs to use only a limited subset of the media source APIs.</span></span> <span data-ttu-id="cc623-108">Per informazioni, vedere l'argomento [uso di origini multimediali con la sessione multimediale](using-media-sources-with-the-media-session.md).</span><span class="sxs-lookup"><span data-stu-id="cc623-108">For information, see the topic [Using Media Sources with the Media Session](using-media-sources-with-the-media-session.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="cc623-109">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="cc623-109">In this section</span></span>



| <span data-ttu-id="cc623-110">Argomento</span><span class="sxs-lookup"><span data-stu-id="cc623-110">Topic</span></span>                                                                                                 | <span data-ttu-id="cc623-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cc623-111">Description</span></span>                                                                                                          |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cc623-112">Modello a oggetti di origine multimediale</span><span class="sxs-lookup"><span data-stu-id="cc623-112">Media Source Object Model</span></span>](media-source-object-model.md)<br/>                                 | <span data-ttu-id="cc623-113">Questo argomento descrive il modello a oggetti per le origini multimediali in Microsoft Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cc623-113">This topic describes the object model for media sources in Microsoft Media Foundation</span></span><br/>                     |
| [<span data-ttu-id="cc623-114">Descrittori di presentazione</span><span class="sxs-lookup"><span data-stu-id="cc623-114">Presentation Descriptors</span></span>](presentation-descriptors.md)<br/>                                   | <span data-ttu-id="cc623-115">Un *descrittore di presentazione* è un oggetto che contiene la descrizione di una particolare presentazione.</span><span class="sxs-lookup"><span data-stu-id="cc623-115">A *presentation descriptor* is an object that contains the description of a particular presentation.</span></span><br/>      |
| [<span data-ttu-id="cc623-116">Eventi di origine dei supporti</span><span class="sxs-lookup"><span data-stu-id="cc623-116">Media Source Events</span></span>](media-source-events.md)<br/>                                             | <span data-ttu-id="cc623-117">Questo argomento elenca gli eventi inviati da origini multimediali e flussi multimediali.</span><span class="sxs-lookup"><span data-stu-id="cc623-117">This topic lists the events that are sent by media sources and media streams.</span></span><br/>                             |
| [<span data-ttu-id="cc623-118">Scrittura di un'origine multimediale personalizzata</span><span class="sxs-lookup"><span data-stu-id="cc623-118">Writing a Custom Media Source</span></span>](writing-a-custom-media-source.md)<br/>                         | <span data-ttu-id="cc623-119">Questo argomento descrive come implementare un'origine multimediale personalizzata in Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="cc623-119">This topic describes how to implement a custom media source in Media Foundation.</span></span><br/>                          |
| [<span data-ttu-id="cc623-120">Case Study: origine supporto MPEG-1</span><span class="sxs-lookup"><span data-stu-id="cc623-120">Case Study: MPEG-1 Media Source</span></span>](tutorial--writing-a-custom-media-source.md)<br/>             | <span data-ttu-id="cc623-121">In questo argomento viene illustrata in dettaglio l'esempio [MPEG-1 media source](mpeg1source-sample.md) SDK.</span><span class="sxs-lookup"><span data-stu-id="cc623-121">This topic takes an in-depth look at the [MPEG-1 Media Source](mpeg1source-sample.md) SDK Sample.</span></span><br/>        |
| [<span data-ttu-id="cc623-122">Provider di metadati personalizzati per i file multimediali</span><span class="sxs-lookup"><span data-stu-id="cc623-122">Custom Metadata Providers for Media Files</span></span>](custom-metadata-providers-for-media-files.md)<br/> | <span data-ttu-id="cc623-123">In questo argomento viene descritto come scrivere un gestore di proprietà della shell personalizzato per un Media Foundation origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="cc623-123">This topic describes how to write a custom Shell property handler for a Media Foundation media source.</span></span><br/>    |
| [<span data-ttu-id="cc623-124">Resolver di origine</span><span class="sxs-lookup"><span data-stu-id="cc623-124">Source Resolver</span></span>](source-resolver.md)<br/>                                                     | <span data-ttu-id="cc623-125">Il resolver dell'origine accetta un URL o un flusso di byte e crea l'origine multimediale appropriata per il contenuto.</span><span class="sxs-lookup"><span data-stu-id="cc623-125">The source resolver takes a URL or byte stream and creates the appropriate media source for that content.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="cc623-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cc623-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc623-127">Pipeline Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cc623-127">Media Foundation Pipeline</span></span>](media-foundation-pipeline.md)
</dt> <dt>

[<span data-ttu-id="cc623-128">Provider di metadati personalizzati per i file multimediali</span><span class="sxs-lookup"><span data-stu-id="cc623-128">Custom Metadata Providers for Media Files</span></span>](custom-metadata-providers-for-media-files.md)
</dt> <dt>

[<span data-ttu-id="cc623-129">Architettura di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cc623-129">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> </dl>

 

 




