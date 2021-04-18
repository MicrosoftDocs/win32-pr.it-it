---
description: In questa sezione viene descritta la progettazione generale di Microsoft Media Foundation. Per informazioni sull'utilizzo di Media Foundation per attività di programmazione specifiche, vedere Guida alla programmazione di Media Foundation.
ms.assetid: 33820c6a-859d-4df6-a605-4e0f64f45c5b
title: Architettura di Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c0914b0f4c43966edcdc6d30efa7c9dbdbbd4e8
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320771"
---
# <a name="media-foundation-architecture"></a><span data-ttu-id="08043-104">Architettura di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="08043-104">Media Foundation Architecture</span></span>

<span data-ttu-id="08043-105">In questa sezione viene descritta la progettazione generale di Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="08043-105">This section describes the general design of Microsoft Media Foundation.</span></span> <span data-ttu-id="08043-106">Per informazioni sull'utilizzo di Media Foundation per attività di programmazione specifiche, vedere [Guida alla programmazione di Media Foundation](media-foundation-programming-guide.md).</span><span class="sxs-lookup"><span data-stu-id="08043-106">For information about using Media Foundation for specific programming tasks, see [Media Foundation Programming Guide](media-foundation-programming-guide.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="08043-107">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="08043-107">In this section</span></span>



| <span data-ttu-id="08043-108">Argomento</span><span class="sxs-lookup"><span data-stu-id="08043-108">Topic</span></span>                                                                                                         | <span data-ttu-id="08043-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="08043-109">Description</span></span>                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="08043-110">Panoramica dell'architettura Media Foundation</span><span class="sxs-lookup"><span data-stu-id="08043-110">Overview of the Media Foundation Architecture</span></span>](overview-of-the-media-foundation-architecture.md)<br/> | <span data-ttu-id="08043-111">Fornisce una panoramica di alto livello dell'architettura Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="08043-111">Gives a high-level overview of the Media Foundation architecture.</span></span><br/>                                                                                                                                                                                                               |
| [<span data-ttu-id="08043-112">Primitive Media Foundation</span><span class="sxs-lookup"><span data-stu-id="08043-112">Media Foundation Primitives</span></span>](media-foundation-primitives.md)<br/>                                     | <span data-ttu-id="08043-113">Vengono descritte alcune interfacce di base utilizzate in Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="08043-113">Describes some basic interfaces that are used throughout Media Foundation.</span></span><br/> <span data-ttu-id="08043-114">Quasi tutte le applicazioni Media Foundation utilizzeranno tali interfacce.</span><span class="sxs-lookup"><span data-stu-id="08043-114">Almost all Media Foundation applications will use these interfaces.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="08043-115">API della piattaforma Media Foundation</span><span class="sxs-lookup"><span data-stu-id="08043-115">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)<br/>                               | <span data-ttu-id="08043-116">Descrive le funzioni di base Media Foundation, ad esempio callback asincroni e code di lavoro.</span><span class="sxs-lookup"><span data-stu-id="08043-116">Describes core Media Foundation functions, such as asynchronous callbacks and work queues.</span></span><br/> <span data-ttu-id="08043-117">Alcune applicazioni possono utilizzare interfacce a livello di piattaforma.</span><span class="sxs-lookup"><span data-stu-id="08043-117">Some applications might use platform-level interfaces.</span></span> <span data-ttu-id="08043-118">Inoltre, i plug-in personalizzati, ad esempio le origini supporti e MFTs, usano queste interfacce.</span><span class="sxs-lookup"><span data-stu-id="08043-118">Also, custom plug-ins, such as media sources and MFTs, use these interfaces.</span></span><br/>                                       |
| [<span data-ttu-id="08043-119">Pipeline Media Foundation</span><span class="sxs-lookup"><span data-stu-id="08043-119">Media Foundation Pipeline</span></span>](media-foundation-pipeline.md)<br/>                                         | <span data-ttu-id="08043-120">Il Media Foundation livello della pipeline è costituito da origini supporti, MFTs e sink multimediali.</span><span class="sxs-lookup"><span data-stu-id="08043-120">The Media Foundation pipeline layer consists of media sources, MFTs, and media sinks.</span></span> <span data-ttu-id="08043-121">La maggior parte delle applicazioni non chiama i metodi direttamente sul livello della pipeline.</span><span class="sxs-lookup"><span data-stu-id="08043-121">Most applications do not call methods directly on the pipeline layer.</span></span> <span data-ttu-id="08043-122">Al contrario, le applicazioni utilizzano uno dei livelli più elevati, ad esempio la sessione multimediale o l'Reader di origine e il writer del sink.</span><span class="sxs-lookup"><span data-stu-id="08043-122">Instead, applications use one of the higher layers, such as the Media Session or the Source Reader and Sink Writer.</span></span><br/> |
| [<span data-ttu-id="08043-123">Sessione multimediale</span><span class="sxs-lookup"><span data-stu-id="08043-123">Media Session</span></span>](media-session.md)<br/>                                                                 | <span data-ttu-id="08043-124">La sessione multimediale gestisce il flusso di dati nella pipeline Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="08043-124">The Media Session manages data flow in the Media Foundation pipeline.</span></span><br/>                                                                                                                                                                                                           |
| [<span data-ttu-id="08043-125">Lettore di origine</span><span class="sxs-lookup"><span data-stu-id="08043-125">Source Reader</span></span>](source-reader.md)<br/>                                                                 | <span data-ttu-id="08043-126">Il lettore di origine consente a un'applicazione di recuperare i dati da un'origine multimediale, senza che il applicating debba chiamare direttamente le API di origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="08043-126">The Source Reader enables an application to get data from a media source, without the applicating needing to call the media source APIs directly.</span></span> <span data-ttu-id="08043-127">Il lettore di origine può inoltre eseguire la decodifica dei flussi compressi.</span><span class="sxs-lookup"><span data-stu-id="08043-127">The Source Reader can also perform decoding of compressed streams.</span></span><br/>                                                            |
| [<span data-ttu-id="08043-128">Percorso supporto protetto</span><span class="sxs-lookup"><span data-stu-id="08043-128">Protected Media Path</span></span>](protected-media-path.md)<br/>                                                   | <span data-ttu-id="08043-129">Il percorso multimediale protetto (PMP) fornisce un ambiente protetto per la riproduzione di contenuti video Premium.</span><span class="sxs-lookup"><span data-stu-id="08043-129">The protected media path (PMP) provides a protected environment for playing premium video content.</span></span> <span data-ttu-id="08043-130">Non è necessario usare PMP quando si scrive un'applicazione Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="08043-130">It is not necessary to use the PMP when writing a Media Foundation application.</span></span> <br/>                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="08043-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="08043-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08043-132">Informazioni su Media Foundation</span><span class="sxs-lookup"><span data-stu-id="08043-132">About Media Foundation</span></span>](about-the-media-foundation-sdk.md)
</dt> <dt>

[<span data-ttu-id="08043-133">Media Foundation: concetti essenziali</span><span class="sxs-lookup"><span data-stu-id="08043-133">Media Foundation: Essential Concepts</span></span>](media-foundation-programming--essential-concepts.md)
</dt> <dt>

[<span data-ttu-id="08043-134">Media Foundation e COM</span><span class="sxs-lookup"><span data-stu-id="08043-134">Media Foundation and COM</span></span>](media-foundation-and-com.md)
</dt> <dt>

[<span data-ttu-id="08043-135">Guida alla programmazione di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="08043-135">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> </dl>

 

 




