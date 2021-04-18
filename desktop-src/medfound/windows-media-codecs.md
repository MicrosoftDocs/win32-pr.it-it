---
description: I codec Windows Media Audio e video sono una raccolta di oggetti che è possibile usare per comprimere e decomprimere i dati multimediali digitali.
ms.assetid: 74de2e75-b1ee-436d-8d78-efe366ab7aa6
title: Codec Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ec98f98fbd0561b291dfc4cc18e4270bf363baf
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320801"
---
# <a name="windows-media-codecs"></a><span data-ttu-id="a3587-103">Codec Windows Media</span><span class="sxs-lookup"><span data-stu-id="a3587-103">Windows Media Codecs</span></span>

<span data-ttu-id="a3587-104">I codec Windows Media Audio e video sono una raccolta di oggetti che è possibile usare per comprimere e decomprimere i dati multimediali digitali.</span><span class="sxs-lookup"><span data-stu-id="a3587-104">The Windows Media Audio and Video codecs are a collection of objects that you can use to compress and decompress digital media data.</span></span> <span data-ttu-id="a3587-105">Ogni codec è costituito da due oggetti, un codificatore e un decodificatore.</span><span class="sxs-lookup"><span data-stu-id="a3587-105">Each codec consists of two objects, an encoder and a decoder.</span></span> <span data-ttu-id="a3587-106">In questa parte della documentazione viene descritto come utilizzare le funzionalità dei codec Windows Media Audio e video per produrre e utilizzare flussi di dati compressi.</span><span class="sxs-lookup"><span data-stu-id="a3587-106">This part of the documentation describes how to use the features of the Windows Media Audio and Video codecs to produce and consume compressed data streams.</span></span>

> [!Note]  
> <span data-ttu-id="a3587-107">Questa documentazione è destinata principalmente agli sviluppatori che desiderano utilizzare codec Windows Media nelle applicazioni multimediali basate su C++.</span><span class="sxs-lookup"><span data-stu-id="a3587-107">This documentation is primarily for developers who want to use Windows Media codecs in their C++-based media applications.</span></span> <span data-ttu-id="a3587-108">Per una panoramica tecnica delle funzionalità dei codec Windows Media, vedere [informazioni sui codec Windows Media](about-the-windows-media-codecs.md).</span><span class="sxs-lookup"><span data-stu-id="a3587-108">For a technical overview of the features of the Windows Media codecs, see [About the Windows Media Codecs](about-the-windows-media-codecs.md).</span></span>

 

<span data-ttu-id="a3587-109">Il termine *codec* è un amalgama dei termini compressore e decompressore.</span><span class="sxs-lookup"><span data-stu-id="a3587-109">The term *codec* is an amalgamation of the terms compressor and decompressor.</span></span> <span data-ttu-id="a3587-110">Un codec viene in genere implementato come una coppia di oggetti COM: uno per la codifica del contenuto e un altro per la decodifica del contenuto.</span><span class="sxs-lookup"><span data-stu-id="a3587-110">A codec is usually implemented as a pair of COM objects: one for encoding content, and another for decoding content.</span></span> <span data-ttu-id="a3587-111">In alcuni casi gli oggetti COM occupano la stessa libreria a collegamento dinamico (DLL).</span><span class="sxs-lookup"><span data-stu-id="a3587-111">In some cases the COM objects occupy the same dynamically linked library (DLL).</span></span>

<span data-ttu-id="a3587-112">Ogni oggetto codec implementa due interfacce separate ma simili:</span><span class="sxs-lookup"><span data-stu-id="a3587-112">Every codec object implements two separate but similar interfaces:</span></span>



| <span data-ttu-id="a3587-113">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="a3587-113">Interface</span></span>                              | <span data-ttu-id="a3587-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a3587-114">Description</span></span>                                 |
|----------------------------------------|---------------------------------------------|
| [<span data-ttu-id="a3587-115">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="a3587-115">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)   | <span data-ttu-id="a3587-116">Compatibile con Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="a3587-116">Compatible with Microsoft Media Foundation.</span></span> |
| [<span data-ttu-id="a3587-117">**IMediaObject**</span><span class="sxs-lookup"><span data-stu-id="a3587-117">**IMediaObject**</span></span>](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) | <span data-ttu-id="a3587-118">Compatibile con DirectShow.</span><span class="sxs-lookup"><span data-stu-id="a3587-118">Compatible with DirectShow.</span></span>                 |



 

<span data-ttu-id="a3587-119">Sono disponibili diversi codec per audio e video, ma anche codec diversi per diversi tipi di contenuto che possono essere inseriti in un file audio o video.</span><span class="sxs-lookup"><span data-stu-id="a3587-119">Not only are there different codecs for audio and for video, but also different codecs for different kinds of content that you might want to put into an audio or video file.</span></span> <span data-ttu-id="a3587-120">Gli algoritmi usati per comprimere e decomprimere i dati per le parole pronunciate differiscono dagli algoritmi usati per comprimere e decomprimere i dati di musica.</span><span class="sxs-lookup"><span data-stu-id="a3587-120">The algorithms used to compress and decompress data for spoken words differ from the algorithms used to compress and decompress music data.</span></span>

## <a name="codec-descriptions"></a><span data-ttu-id="a3587-121">Descrizioni codec</span><span class="sxs-lookup"><span data-stu-id="a3587-121">Codec Descriptions</span></span>

<span data-ttu-id="a3587-122">Nella tabella seguente vengono descritti gli utilizzi previsti dei codec Windows Media.</span><span class="sxs-lookup"><span data-stu-id="a3587-122">The following table describes the intended uses of the Windows Media codecs.</span></span>



| <span data-ttu-id="a3587-123">Codec</span><span class="sxs-lookup"><span data-stu-id="a3587-123">Codec</span></span>                                                                     | <span data-ttu-id="a3587-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a3587-124">Description</span></span>                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a3587-125">Windows Media Audio</span><span class="sxs-lookup"><span data-stu-id="a3587-125">Windows Media Audio</span></span>](windowsmediaaudioencoder.md)                       | <span data-ttu-id="a3587-126">Un codec audio che supporta tre categorie di contenuto codificato: standard, Professional e lossless.</span><span class="sxs-lookup"><span data-stu-id="a3587-126">An audio codec that supports three categories of encoded content: Standard, Professional, and Lossless.</span></span>                                                                                                                                                                                      |
| [<span data-ttu-id="a3587-127">Windows Media Audio Voice</span><span class="sxs-lookup"><span data-stu-id="a3587-127">Windows Media Audio Voice</span></span>](windowsmediaaudiovoiceencoder.md)            | <span data-ttu-id="a3587-128">Codec audio ottimizzato per la codifica della voce umana a rapporti di compressione elevati.</span><span class="sxs-lookup"><span data-stu-id="a3587-128">Audio codec optimized for encoding the human voice at high compression ratios.</span></span> <span data-ttu-id="a3587-129">Questo è il codec preferito per i flussi costituiti principalmente da parole vocali.</span><span class="sxs-lookup"><span data-stu-id="a3587-129">This is the preferred codec for streams consisting mostly of spoken words.</span></span> <span data-ttu-id="a3587-130">Per contenuti con musica mista e sintesi vocale, questo codec può modificare dinamicamente l'algoritmo di codifica usato per ottenere la qualità ottimale.</span><span class="sxs-lookup"><span data-stu-id="a3587-130">For content that is mixed music and speech, this codec can dynamically change the encoding algorithm used, to get optimal quality.</span></span> |
| [<span data-ttu-id="a3587-131">Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="a3587-131">Windows Media Video 9</span></span>](windowsmediavideo9encoder.md)                    | <span data-ttu-id="a3587-132">Un codec video che supporta quattro categorie di contenuto codificato: profilo semplice, profilo principale, profilo avanzato e immagine.</span><span class="sxs-lookup"><span data-stu-id="a3587-132">A video codec that supports four categories of encoded content: Simple Profile, Main Profile, Advanced Profile, and Image..</span></span>                                                                                                                                                                  |
| [<span data-ttu-id="a3587-133">Schermata Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="a3587-133">Windows Media Video 9 Screen</span></span>](usingthewindowsmediavideo9screencodec.md) | <span data-ttu-id="a3587-134">Codec video ottimizzato per la codifica di schermate sequenziali dai monitoraggi computer.</span><span class="sxs-lookup"><span data-stu-id="a3587-134">Video codec optimized for encoding sequential screen shots from computer monitors.</span></span> <span data-ttu-id="a3587-135">Questo codec viene spesso utilizzato per il training o il supporto software registrando le immagini di monitoraggio durante l'utilizzo delle applicazioni del computer.</span><span class="sxs-lookup"><span data-stu-id="a3587-135">This codec is often used for software training or support by recording monitor images while computer applications are being used.</span></span>                                                                         |



 

<span data-ttu-id="a3587-136">Le versioni più recenti degli oggetti codec consentono anche l'accesso ad alcuni codec legacy, tra cui Windows Media Video 7 e 8, Windows Media Screen 7, i precedenti codec Microsoft MPEG-4 e i codec MPEG-4 Microsoft ISO.</span><span class="sxs-lookup"><span data-stu-id="a3587-136">The most recent versions of the codec objects also enable access to some legacy codecs, including Windows Media Video 7 and 8, Windows Media Screen 7, the older Microsoft MPEG-4 codecs, and the Microsoft ISO MPEG-4 codecs.</span></span>

> [!Note]  
> <span data-ttu-id="a3587-137">Questa documentazione non copre questi codec legacy; vengono illustrate solo le versioni correnti dei codec.</span><span class="sxs-lookup"><span data-stu-id="a3587-137">This documentation does not cover these legacy codecs; it covers only the current versions of codecs.</span></span>

 

<span data-ttu-id="a3587-138">Per i codec precedenti, usare le stesse procedure di quando si usano i codec correnti; Tuttavia, tenere presente che non tutte le funzionalità sono supportate in tutti i codec.</span><span class="sxs-lookup"><span data-stu-id="a3587-138">For older codecs, use the same procedures as when using the current codecs; however, remember that not all features are supported in all codecs.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a3587-139">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="a3587-139">In this section</span></span>

-   [<span data-ttu-id="a3587-140">Informazioni sui codec Windows Media</span><span class="sxs-lookup"><span data-stu-id="a3587-140">About the Windows Media Codecs</span></span>](about-the-windows-media-codecs.md)
-   [<span data-ttu-id="a3587-141">Uso degli oggetti codec e DSP</span><span class="sxs-lookup"><span data-stu-id="a3587-141">Using the Codec and DSP Objects</span></span>](decidinghowtousethewindowsmediaaudioandvideocodecs.md)
-   [<span data-ttu-id="a3587-142">Metodi di codifica</span><span class="sxs-lookup"><span data-stu-id="a3587-142">Encoding Methods</span></span>](encodingmethods.md)
-   [<span data-ttu-id="a3587-143">Implementazione del codec</span><span class="sxs-lookup"><span data-stu-id="a3587-143">Codec Implementation</span></span>](codecimplementation.md)
-   [<span data-ttu-id="a3587-144">Modello di buffer di bucket a perdita</span><span class="sxs-lookup"><span data-stu-id="a3587-144">The Leaky Bucket Buffer Model</span></span>](the-leaky-bucket-buffer-model.md)
-   [<span data-ttu-id="a3587-145">Uso di codec DMOs</span><span class="sxs-lookup"><span data-stu-id="a3587-145">Working with Codec DMOs</span></span>](workingwithcodecdmos.md)
-   [<span data-ttu-id="a3587-146">Uso di codec MFTs</span><span class="sxs-lookup"><span data-stu-id="a3587-146">Working with Codec MFTs</span></span>](workingwithcodecmfts.md)
-   [<span data-ttu-id="a3587-147">Utilizzo di audio</span><span class="sxs-lookup"><span data-stu-id="a3587-147">Working with Audio</span></span>](workingwithaudio.md)
-   [<span data-ttu-id="a3587-148">Uso dei video</span><span class="sxs-lookup"><span data-stu-id="a3587-148">Working with Video</span></span>](workingwithvideo.md)
-   [<span data-ttu-id="a3587-149">Archiviazione di supporti compressi in file AVI</span><span class="sxs-lookup"><span data-stu-id="a3587-149">Storing Compressed Media in AVI Files</span></span>](storingcompressedmediainavifiles.md)
-   [<span data-ttu-id="a3587-150">Uso della codifica VBR</span><span class="sxs-lookup"><span data-stu-id="a3587-150">Using VBR Encoding</span></span>](usingvbrencoding.md)
-   [<span data-ttu-id="a3587-151">Uso della codifica Two-Pass</span><span class="sxs-lookup"><span data-stu-id="a3587-151">Using Two-Pass Encoding</span></span>](usingtwoencodingpasses.md)
-   [<span data-ttu-id="a3587-152">Recupero delle statistiche di codifica</span><span class="sxs-lookup"><span data-stu-id="a3587-152">Getting Encoding Statistics</span></span>](gettingencodingstatistics.md)
-   [<span data-ttu-id="a3587-153">Uso delle estensioni dell'unità dati</span><span class="sxs-lookup"><span data-stu-id="a3587-153">Using Data Unit Extensions</span></span>](usingdataunitextensions.md)
-   [<span data-ttu-id="a3587-154">Costanti IPropertyBag codec e DSP</span><span class="sxs-lookup"><span data-stu-id="a3587-154">Codec and DSP IPropertyBag Constants</span></span>](codecanddspproperties.md)
-   [<span data-ttu-id="a3587-155">Parser Sommario</span><span class="sxs-lookup"><span data-stu-id="a3587-155">Table of Contents Parser</span></span>](toc-parser.md)
-   [<span data-ttu-id="a3587-156">Domande frequenti sui codec di Windows Media</span><span class="sxs-lookup"><span data-stu-id="a3587-156">Windows Media Codec FAQ</span></span>](frequentlyaskedquestions.md)

## <a name="related-topics"></a><span data-ttu-id="a3587-157">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a3587-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3587-158">Guida alla programmazione di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a3587-158">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> <dt>

<span data-ttu-id="a3587-159">[Tecnologie multimediali per Windows](/previous-versions/bg125389(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="a3587-159">[Media Technologies for Windows](/previous-versions/bg125389(v=msdn.10))</span></span>
</dt> </dl>

 

 
