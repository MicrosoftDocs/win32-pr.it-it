---
description: Questa sezione degli argomenti fornisce agli sviluppatori informazioni aggiuntive su come implementare i codec del formato di file di immagine che funzioneranno all'interno del Framework di Windows Imaging Component (WIC).
ms.assetid: 58f03dc2-cc31-4d76-b75a-f332da1f900f
title: Come scrivere un codec WIC-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee694d9a857781e97a31cb37f5ef18c518dae964
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882194"
---
# <a name="how-to-write-a-wic-enabled-codec"></a><span data-ttu-id="781c3-103">Come scrivere un codec WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="781c3-103">How to Write a WIC-Enabled Codec</span></span>

<span data-ttu-id="781c3-104">Questa sezione degli argomenti fornisce agli sviluppatori informazioni aggiuntive su come implementare i codec del formato di file di immagine che funzioneranno all'interno del Framework di Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="781c3-104">This section of topics provide developers with guidance on how to implement image file format codecs that will function within the Windows Imaging Component (WIC) framework.</span></span>

<dl>

[<span data-ttu-id="781c3-105">Introduzione</span><span class="sxs-lookup"><span data-stu-id="781c3-105">Introduction</span></span>](-wic-howtowriteacodec-intro.md)  
[<span data-ttu-id="781c3-106">Funzionamento di Windows Imaging Component (WIC)</span><span class="sxs-lookup"><span data-stu-id="781c3-106">How The Windows Imaging Component (WIC) Works</span></span>](-wic-howwicworks.md)  
<dl>

[<span data-ttu-id="781c3-107">Individuazione e arbitraggio</span><span class="sxs-lookup"><span data-stu-id="781c3-107">Discovery and Arbitration</span></span>](-wic-howwicworks.md)  
[<span data-ttu-id="781c3-108">Decodifica</span><span class="sxs-lookup"><span data-stu-id="781c3-108">Decoding</span></span>](-wic-howwicworks.md)  
[<span data-ttu-id="781c3-109">Encoding</span><span class="sxs-lookup"><span data-stu-id="781c3-109">Encoding</span></span>](-wic-howwicworks.md)  
[<span data-ttu-id="781c3-110">Durata di un codec</span><span class="sxs-lookup"><span data-stu-id="781c3-110">The Lifetime of a Codec</span></span>](-wic-howwicworks.md)  
[<span data-ttu-id="781c3-111">Come abilitare WIC per un codec</span><span class="sxs-lookup"><span data-stu-id="781c3-111">How to WIC-enable a Codec</span></span>](-wic-howwicworks.md)  
[<span data-ttu-id="781c3-112">Supporto di Apartment multithread in WIC</span><span class="sxs-lookup"><span data-stu-id="781c3-112">Multi-Threaded Apartment Support in WIC</span></span>](-wic-howwicworks.md)  
<span data-ttu-id="781c3-113"></dl> </dd> <a href="-wic-implementingwicdecoder.md">Implementazione di un decodificatore WIC-Enabled</a></span><span class="sxs-lookup"><span data-stu-id="781c3-113"></dl> </dd> <a href="-wic-implementingwicdecoder.md">Implementing a WIC-Enabled Decoder</a></span></span><dl>

[<span data-ttu-id="781c3-114">Interfacce del decodificatore</span><span class="sxs-lookup"><span data-stu-id="781c3-114">Decoder Interfaces</span></span>](-wic-decoderinterfaces.md)<dl>

[<span data-ttu-id="781c3-115">IWICBitmapDecoder</span><span class="sxs-lookup"><span data-stu-id="781c3-115">IWICBitmapDecoder</span></span>](-wic-imp-iwicbitmapdecoder.md)  
[<span data-ttu-id="781c3-116">IWICBitmapCodecProgressNotification</span><span class="sxs-lookup"><span data-stu-id="781c3-116">IWICBitmapCodecProgressNotification</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)  
[<span data-ttu-id="781c3-117">IWICBitmapSource</span><span class="sxs-lookup"><span data-stu-id="781c3-117">IWICBitmapSource</span></span>](-wic-imp-iwicbitmapsource.md)  
[<span data-ttu-id="781c3-118">IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="781c3-118">IWICBitmapFrameDecode</span></span>](-wic-imp-iwicbitmapframedecode.md)  
[<span data-ttu-id="781c3-119">IWICMetadataBlockReader</span><span class="sxs-lookup"><span data-stu-id="781c3-119">IWICMetadataBlockReader</span></span>](-wic-imp-iwicmetadatablockreader.md)  
[<span data-ttu-id="781c3-120">IWICBitmapSourceTransform</span><span class="sxs-lookup"><span data-stu-id="781c3-120">IWICBitmapSourceTransform</span></span>](-wic-imp-iwicbitmapsourcetransform.md)  
[<span data-ttu-id="781c3-121">IWICDevelopRaw</span><span class="sxs-lookup"><span data-stu-id="781c3-121">IWICDevelopRaw</span></span>](-wic-imp-iwicdevelopraw.md)  
<span data-ttu-id="781c3-122"></dl> </dd> </dl> </dd> <a href="-wic-implementingwicencoder.md">Implementazione di un codificatore di WIC-Enabled</a>  
</span><span class="sxs-lookup"><span data-stu-id="781c3-122"></dl> </dd> </dl> </dd> <a href="-wic-implementingwicencoder.md">Implementing a WIC-Enabled Encoder</a>  
</span></span><dl>

[<span data-ttu-id="781c3-123">Interfacce del codificatore</span><span class="sxs-lookup"><span data-stu-id="781c3-123">Encoder Interfaces</span></span>](-wic-encoderinterfaces.md)  
<dl>

[<span data-ttu-id="781c3-124">IWICBitmapEncoder</span><span class="sxs-lookup"><span data-stu-id="781c3-124">IWICBitmapEncoder</span></span>](-wic-imp-iwicbitmapencoder.md)  
[<span data-ttu-id="781c3-125">IWICBitmapCodecProgressNotification</span><span class="sxs-lookup"><span data-stu-id="781c3-125">IWICBitmapCodecProgressNotification</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md)  
[<span data-ttu-id="781c3-126">IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="781c3-126">IWICBitmapFrameEncode</span></span>](-wic-imp-iwicbitmapframeencode.md)  
[<span data-ttu-id="781c3-127">IWICMetadataBlockWriter</span><span class="sxs-lookup"><span data-stu-id="781c3-127">IWICMetadataBlockWriter</span></span>](-wic-imp-iwicmetadatablockwriter.md)  
<span data-ttu-id="781c3-128"></dl> </dd> </dl> </dd> <a href="-wic-codecinstallandreg.md">Installazione e registrazione di codec</a>  
</span><span class="sxs-lookup"><span data-stu-id="781c3-128"></dl> </dd> </dl> </dd> <a href="-wic-codecinstallandreg.md">Codec Installation and Registration</a>  
</span></span><dl>

[<span data-ttu-id="781c3-129">Registrazione di un codec</span><span class="sxs-lookup"><span data-stu-id="781c3-129">Registering a Codec</span></span>](-wic-codecinstallandreg.md)  
<dl>

[<span data-ttu-id="781c3-130">Voci di registro generali</span><span class="sxs-lookup"><span data-stu-id="781c3-130">General Register Entries</span></span>](-wic-generalregentries.md)  
[<span data-ttu-id="781c3-131">Voci del registro di sistema specifiche del codificatore</span><span class="sxs-lookup"><span data-stu-id="781c3-131">Encoder-Specific Registry Entries</span></span>](-wic-encoderregentries.md)  
<dl>

[<span data-ttu-id="781c3-132">Registrazione di un formato contenitore con writer di metadati</span><span class="sxs-lookup"><span data-stu-id="781c3-132">Registering a Container Format with Metadata Writers</span></span>](-wic-encoderregentries.md)  
<span data-ttu-id="781c3-133"></dl> </dd> <a href="-wic-decoderregentries.md">Voci del registro di sistema specifiche del codificatore</a>  
</span><span class="sxs-lookup"><span data-stu-id="781c3-133"></dl> </dd> <a href="-wic-decoderregentries.md">Encoder-Specific Registry Entries</a>  
</span></span><dl>

[<span data-ttu-id="781c3-134">Registrazione di un nuovo formato del contenitore con i lettori di metadati</span><span class="sxs-lookup"><span data-stu-id="781c3-134">Registering a New Container Format with Metadata Readers</span></span>](-wic-decoderregentries.md)  
<span data-ttu-id="781c3-135"></dl> </dd> <a href="-wic-integrationregentries.md">Integrazione con la PhotoGallery di Windows Vista ed Esplora risorse</a>  
</span><span class="sxs-lookup"><span data-stu-id="781c3-135"></dl> </dd> <a href="-wic-integrationregentries.md">Integration with Windows Vista PhotoGallery and Explorer</a>  
</span></span><dl>

[<span data-ttu-id="781c3-136">Archivio delle proprietà di Windows</span><span class="sxs-lookup"><span data-stu-id="781c3-136">Windows Property Store</span></span>](-wic-integrationregentries.md)  
[<span data-ttu-id="781c3-137">Raccolta foto di Windows Vista</span><span class="sxs-lookup"><span data-stu-id="781c3-137">Windows Vista Photo Gallery</span></span>](-wic-integrationregentries.md)  
[<span data-ttu-id="781c3-138">Cache anteprime di Windows Vista</span><span class="sxs-lookup"><span data-stu-id="781c3-138">Windows Vista Thumbnail Cache</span></span>](-wic-integrationregentries.md)  
<span data-ttu-id="781c3-139"></dl> </dd> </dl> </dd> <a href="-wic-codecinstallandreg.md">Aggiornamento della cache delle anteprime durante l'installazione di un codec</a> [rendere disponibile il codec WIC-Enabled per gli utenti](-wic-codecinstallandreg.md) </dl> </dd> <a href="-wic-howtowriteacodec-conclusion.md"></a>  
</span><span class="sxs-lookup"><span data-stu-id="781c3-139"></dl> </dd> </dl> </dd> <a href="-wic-codecinstallandreg.md">Updating the Thumbnail Cache when Installing a Codec</a> [Making Your WIC-Enabled Codec Available to Users](-wic-codecinstallandreg.md) </dl> </dd> <a href="-wic-howtowriteacodec-conclusion.md">Conclusion</a>  
</span></span></dl>

## <a name="related-topics"></a><span data-ttu-id="781c3-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="781c3-140">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="781c3-141">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="781c3-141">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="781c3-142">Introduzione (come scrivere un CODEC WIC-Enabled)</span><span class="sxs-lookup"><span data-stu-id="781c3-142">Introduction (How to Write a WIC-Enabled CODEC)</span></span>](-wic-howtowriteacodec-intro.md)
</dt> <dt>

[<span data-ttu-id="781c3-143">Panoramica del componente imaging Windows</span><span class="sxs-lookup"><span data-stu-id="781c3-143">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



