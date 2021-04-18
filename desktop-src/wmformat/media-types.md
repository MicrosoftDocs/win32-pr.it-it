---
title: Tipi di supporto per Windows Media Format SDK
description: Informazioni sui tipi di supporto che possono essere usati da Windows Media Format SDK. I tipi di supporto sono valori GUID assegnati alle costanti nell'SDK.
ms.assetid: 00dcbb20-09ed-44c5-992c-20f3d17ad47c
keywords:
- Windows Media Format SDK, tipi di supporto
- Formati di sistemi avanzati (ASF), tipi di supporto
- ASF (formato di sistemi avanzati), tipi di supporto
- tipi di supporto, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d6d15255ab311c67562a6c9dde83650240b0803
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/02/2021
ms.locfileid: "106334336"
---
# <a name="media-types-for-windows-media-format-sdk"></a><span data-ttu-id="58718-108">Tipi di supporto per Windows Media Format SDK</span><span class="sxs-lookup"><span data-stu-id="58718-108">Media Types for Windows Media Format SDK</span></span>

<span data-ttu-id="58718-109">I tipi di supporto identificano i diversi tipi di supporti che possono essere usati da Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="58718-109">Media types identify the different types of media that can be used by the Windows Media Format SDK.</span></span> <span data-ttu-id="58718-110">Tutti i tipi di supporto sono valori GUID che sono stati assegnati alle costanti nell'SDK.</span><span class="sxs-lookup"><span data-stu-id="58718-110">All media types are GUID values that have been assigned to constants in the SDK.</span></span> <span data-ttu-id="58718-111">I valori GUID rappresentati dalle costanti elencate in questa sezione sono elencati nella sezione [identificatori del tipo di supporto](media-type-identifiers.md) di questo riferimento.</span><span class="sxs-lookup"><span data-stu-id="58718-111">The GUID values represented by the constants listed in this section are listed in the [Media Type Identifiers](media-type-identifiers.md) section of this reference.</span></span>

<span data-ttu-id="58718-112">La tabella seguente elenca i principali tipi di supporti.</span><span class="sxs-lookup"><span data-stu-id="58718-112">The following table lists major media types.</span></span> <span data-ttu-id="58718-113">Queste costanti definiscono la classificazione di alto livello del supporto digitale supportato da Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="58718-113">These constants define the high level classification of digital media supported by the Windows Media Format SDK.</span></span>



| <span data-ttu-id="58718-114">Tipo principale</span><span class="sxs-lookup"><span data-stu-id="58718-114">Major type</span></span>                | <span data-ttu-id="58718-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="58718-115">Description</span></span>                                                                                             |
|---------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58718-116">Video di WMMEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="58718-116">WMMEDIATYPE\_Video</span></span>        | <span data-ttu-id="58718-117">Flusso video.</span><span class="sxs-lookup"><span data-stu-id="58718-117">A video stream.</span></span>                                                                                         |
| <span data-ttu-id="58718-118">\_Audio WMMEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="58718-118">WMMEDIATYPE\_Audio</span></span>        | <span data-ttu-id="58718-119">Flusso audio.</span><span class="sxs-lookup"><span data-stu-id="58718-119">An audio stream.</span></span>                                                                                        |
| <span data-ttu-id="58718-120">\_Script WMMEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="58718-120">WMMEDIATYPE\_Script</span></span>       | <span data-ttu-id="58718-121">Flusso di script.</span><span class="sxs-lookup"><span data-stu-id="58718-121">A script stream.</span></span>                                                                                        |
| <span data-ttu-id="58718-122">WMMEDIATYPE \_ filetransfer</span><span class="sxs-lookup"><span data-stu-id="58718-122">WMMEDIATYPE\_FileTransfer</span></span> | <span data-ttu-id="58718-123">Flusso contenente file di dati.</span><span class="sxs-lookup"><span data-stu-id="58718-123">A stream that contains data files.</span></span> <span data-ttu-id="58718-124">I flussi Web, che sono costituiti da file HTML, hanno anche questo tipo principale.</span><span class="sxs-lookup"><span data-stu-id="58718-124">Web streams, which consist of HTML files, also have this major type.</span></span> |
| <span data-ttu-id="58718-125">Immagine di WMMEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="58718-125">WMMEDIATYPE\_Image</span></span>        | <span data-ttu-id="58718-126">Un flusso di immagini JPEG per un file audio illustrato (come in una presentazione).</span><span class="sxs-lookup"><span data-stu-id="58718-126">A JPEG image stream for an illustrated audio file (as in a slide show).</span></span>                                 |
| <span data-ttu-id="58718-127">\_Testo WMMEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="58718-127">WMMEDIATYPE\_Text</span></span>         | <span data-ttu-id="58718-128">Flusso di testo.</span><span class="sxs-lookup"><span data-stu-id="58718-128">A text stream.</span></span>                                                                                          |



 

<span data-ttu-id="58718-129">Oltre ai tipi di supporti principali supportati in modo esplicito, è possibile creare tipi di dati arbitrari.</span><span class="sxs-lookup"><span data-stu-id="58718-129">In addition to the explicitly supported major media types, you can create your own arbitrary data types.</span></span> <span data-ttu-id="58718-130">Per i tipi di dati arbitrari personalizzati, è necessario assicurarsi che il GUID utilizzato non corrisponda a un tipo principale esistente.</span><span class="sxs-lookup"><span data-stu-id="58718-130">For custom arbitrary data types, you must ensure that the GUID you use does not match an existing major type.</span></span>

<span data-ttu-id="58718-131">Un flusso multimediale avrà spesso un sottotipo oltre al tipo principale.</span><span class="sxs-lookup"><span data-stu-id="58718-131">A media stream will often have a subtype in addition to its major type.</span></span> <span data-ttu-id="58718-132">Nelle sezioni seguenti sono elencati i sottotipi supportati.</span><span class="sxs-lookup"><span data-stu-id="58718-132">The following sections list the supported subtypes.</span></span>



| <span data-ttu-id="58718-133">Sezione</span><span class="sxs-lookup"><span data-stu-id="58718-133">Section</span></span>                                                        | <span data-ttu-id="58718-134">Descrizione</span><span class="sxs-lookup"><span data-stu-id="58718-134">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="58718-135">Sottotipi di supporti non compressi</span><span class="sxs-lookup"><span data-stu-id="58718-135">Uncompressed Media Subtypes</span></span>](uncompressed-media-subtypes.md) | <span data-ttu-id="58718-136">Descrive i sottotipi disponibili per i supporti non compressi.</span><span class="sxs-lookup"><span data-stu-id="58718-136">Describes the subtypes available for uncompressed media.</span></span> <span data-ttu-id="58718-137">Questi sono i tipi generalmente associati al supporto di input o di output.</span><span class="sxs-lookup"><span data-stu-id="58718-137">These are the types typically associated with input or output media.</span></span>              |
| [<span data-ttu-id="58718-138">Sottotipi di supporti compressi</span><span class="sxs-lookup"><span data-stu-id="58718-138">Compressed Media Subtypes</span></span>](compressed-media-subtypes.md)     | <span data-ttu-id="58718-139">Descrive i sottotipi disponibili per i supporti compressi.</span><span class="sxs-lookup"><span data-stu-id="58718-139">Describes the subtypes available for compressed media.</span></span> <span data-ttu-id="58718-140">Questi sono i tipi in genere associati ai supporti in un flusso all'interno di un file ASF.</span><span class="sxs-lookup"><span data-stu-id="58718-140">These are the types typically associated with media in a stream within an ASF file.</span></span> |
| [<span data-ttu-id="58718-141">Formati di input video</span><span class="sxs-lookup"><span data-stu-id="58718-141">Video Input Formats</span></span>](video-input-formats.md)                 | <span data-ttu-id="58718-142">Elenca i formati video accettati come input per il codec Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="58718-142">Lists the video formats accepted as inputs for the Windows Media Video 9 codec.</span></span>                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="58718-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="58718-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58718-144">**Identificatori del tipo di supporto**</span><span class="sxs-lookup"><span data-stu-id="58718-144">**Media Type Identifiers**</span></span>](media-type-identifiers.md)
</dt> <dt>

[<span data-ttu-id="58718-145">**Guida di riferimento alla programmazione**</span><span class="sxs-lookup"><span data-stu-id="58718-145">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 




