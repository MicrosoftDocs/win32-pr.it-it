---
description: Tipi di supporto
ms.assetid: 690fda6e-dcbd-44dc-968d-cc949126da81
title: Tipi di supporto (Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8acbfb1b637eef6acb664d3d95a0488f155c6916
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351621"
---
# <a name="media-types-media-foundation"></a><span data-ttu-id="23c8c-103">Tipi di supporto (Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="23c8c-103">Media Types (Media Foundation)</span></span>

<span data-ttu-id="23c8c-104">Un *tipo di supporto* è un modo per descrivere il formato di un flusso multimediale.</span><span class="sxs-lookup"><span data-stu-id="23c8c-104">A *media type* is a way to describe the format of a media stream.</span></span> <span data-ttu-id="23c8c-105">In Media Foundation i tipi di supporto sono rappresentati dall'interfaccia [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) .</span><span class="sxs-lookup"><span data-stu-id="23c8c-105">In Media Foundation, media types are represented by the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface.</span></span> <span data-ttu-id="23c8c-106">Le applicazioni utilizzano i tipi di supporto per individuare il formato di un file multimediale o di un flusso multimediale.</span><span class="sxs-lookup"><span data-stu-id="23c8c-106">Applications use media types to discover the format of a media file or media stream.</span></span> <span data-ttu-id="23c8c-107">Gli oggetti nella pipeline Media Foundation utilizzano i tipi di supporto per negoziare i formati che verranno recapitati o ricevuti.</span><span class="sxs-lookup"><span data-stu-id="23c8c-107">Objects in the Media Foundation pipeline use media types to negotiate the formats they will deliver or receive.</span></span>

<span data-ttu-id="23c8c-108">In questa sezione vengono trattati gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="23c8c-108">This section contains the following topics.</span></span>



| <span data-ttu-id="23c8c-109">Argomento</span><span class="sxs-lookup"><span data-stu-id="23c8c-109">Topic</span></span>                                                                    | <span data-ttu-id="23c8c-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="23c8c-110">Description</span></span>                                                                      |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="23c8c-111">Informazioni sui tipi di supporto</span><span class="sxs-lookup"><span data-stu-id="23c8c-111">About Media Types</span></span>](about-media-types.md)                               | <span data-ttu-id="23c8c-112">Panoramica generale dei tipi di supporto in Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="23c8c-112">General overview of media types in Media Foundation.</span></span>                             |
| [<span data-ttu-id="23c8c-113">GUID di tipo multimediale</span><span class="sxs-lookup"><span data-stu-id="23c8c-113">Media Type GUIDs</span></span>](media-type-guids.md)                                 | <span data-ttu-id="23c8c-114">Elenca i GUID definiti per i tipi e i sottotipi principali.</span><span class="sxs-lookup"><span data-stu-id="23c8c-114">Lists the defined GUIDs for major types and subtypes.</span></span>                            |
| [<span data-ttu-id="23c8c-115">Tipi di supporti audio</span><span class="sxs-lookup"><span data-stu-id="23c8c-115">Audio Media Types</span></span>](audio-media-types.md)                               | <span data-ttu-id="23c8c-116">Come creare i tipi di supporto per i formati audio.</span><span class="sxs-lookup"><span data-stu-id="23c8c-116">How to create media types for audio formats.</span></span>                                     |
| [<span data-ttu-id="23c8c-117">Tipi di supporti video</span><span class="sxs-lookup"><span data-stu-id="23c8c-117">Video Media Types</span></span>](video-media-types.md)                               | <span data-ttu-id="23c8c-118">Come creare i tipi di supporto per i formati video.</span><span class="sxs-lookup"><span data-stu-id="23c8c-118">How to create media types for video formats.</span></span>                                     |
| [<span data-ttu-id="23c8c-119">Tipi di supporti completi e parziali</span><span class="sxs-lookup"><span data-stu-id="23c8c-119">Complete and Partial Media Types</span></span>](complete-and-partial-media-types.md) | <span data-ttu-id="23c8c-120">Descrive la differenza tra i tipi di supporto completi e i tipi di supporti parziali.</span><span class="sxs-lookup"><span data-stu-id="23c8c-120">Describes the difference between complete media types and partial media types.</span></span>   |
| [<span data-ttu-id="23c8c-121">Conversioni di tipi di supporto</span><span class="sxs-lookup"><span data-stu-id="23c8c-121">Media Type Conversions</span></span>](media-type-conversions.md)                     | <span data-ttu-id="23c8c-122">Come eseguire la conversione tra Media Foundation tipi di supporto e le strutture di formato precedenti.</span><span class="sxs-lookup"><span data-stu-id="23c8c-122">How to convert between Media Foundation media types and older format structures.</span></span> |
| [<span data-ttu-id="23c8c-123">Funzioni helper del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="23c8c-123">Media Type Helper Functions</span></span>](media-type-helper-functions.md)           | <span data-ttu-id="23c8c-124">Elenco di funzioni che modificano o ottengono informazioni da un tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="23c8c-124">A list of functions that manipulate or get information from a media type.</span></span>        |
| [<span data-ttu-id="23c8c-125">Codice di debug del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="23c8c-125">Media Type Debugging Code</span></span>](media-type-debugging-code.md)               | <span data-ttu-id="23c8c-126">Codice di esempio che illustra come visualizzare un tipo di supporto durante il debug.</span><span class="sxs-lookup"><span data-stu-id="23c8c-126">Example code that shows how to view a media type while debugging.</span></span>                |



 

## <a name="related-topics"></a><span data-ttu-id="23c8c-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="23c8c-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23c8c-128">Primitive Media Foundation</span><span class="sxs-lookup"><span data-stu-id="23c8c-128">Media Foundation Primitives</span></span>](media-foundation-primitives.md)
</dt> <dt>

[<span data-ttu-id="23c8c-129">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="23c8c-129">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 



