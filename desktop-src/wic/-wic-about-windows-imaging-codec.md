---
description: Windows Imaging Component (WIC) fornisce un framework estensibile per l'utilizzo di immagini e metadati di immagini.
ms.assetid: a05b496a-bd4c-4065-8060-df0f8930cde7
title: Panoramica del componente imaging Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 764260dd9375f1372c1936c7dbd776295eb34433
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231900"
---
# <a name="windows-imaging-component-overview"></a><span data-ttu-id="0e5be-103">Panoramica del componente imaging Windows</span><span class="sxs-lookup"><span data-stu-id="0e5be-103">Windows Imaging Component Overview</span></span>

<span data-ttu-id="0e5be-104">Windows Imaging Component (WIC) fornisce un framework estensibile per l'utilizzo di immagini e metadati di immagini.</span><span class="sxs-lookup"><span data-stu-id="0e5be-104">The Windows Imaging Component (WIC) provides an extensible framework for working with images and image metadata.</span></span> <span data-ttu-id="0e5be-105">WIC rende possibile i fornitori di software indipendenti (ISV) e i fornitori di hardware indipendenti (IHV) per sviluppare i propri codec di immagine e ottenere lo stesso supporto della piattaforma dei formati di immagine standard (ad esempio, TIFF, JPEG, PNG, GIF, BMP e HDPhoto).</span><span class="sxs-lookup"><span data-stu-id="0e5be-105">WIC makes it possible for independent software vendors (ISVs) and independent hardware vendors (IHVs) to develop their own image codecs and get the same platform support as standard image formats (for example, TIFF, JPEG, PNG, GIF, BMP, and HDPhoto).</span></span> <span data-ttu-id="0e5be-106">Un unico set coerente di interfacce viene usato per tutte le operazioni di elaborazione delle immagini, indipendentemente dal formato di immagine, quindi qualsiasi applicazione che usa WIC ottiene il supporto automatico per i nuovi formati di immagine non appena viene installato il codec.</span><span class="sxs-lookup"><span data-stu-id="0e5be-106">A single, consistent set of interfaces is used for all image processing, regardless of image format, so any application using the WIC gets automatic support for new image formats as soon as the codec is installed.</span></span> <span data-ttu-id="0e5be-107">Extensible Metadata Framework consente alle applicazioni di leggere e scrivere i propri metadati proprietari direttamente nei file di immagine, in modo che i metadati non vengano mai persi o separati dall'immagine.</span><span class="sxs-lookup"><span data-stu-id="0e5be-107">The extensible metadata framework makes it possible for applications to read and write their own proprietary metadata directly to image files, so the metadata never gets lost or separated from the image.</span></span>

<span data-ttu-id="0e5be-108">In questo argomento sono incluse le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="0e5be-108">This topic includes the following sections.</span></span>

-   [<span data-ttu-id="0e5be-109">Funzionalità del componente Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="0e5be-109">Windows Imaging Component Features</span></span>](#windows-imaging-component-features)
-   [<span data-ttu-id="0e5be-110">Codec nativi</span><span class="sxs-lookup"><span data-stu-id="0e5be-110">Native Codecs</span></span>](#native-codecs)
-   [<span data-ttu-id="0e5be-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0e5be-111">Related topics</span></span>](#related-topics)

## <a name="windows-imaging-component-features"></a><span data-ttu-id="0e5be-112">Funzionalità del componente Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="0e5be-112">Windows Imaging Component Features</span></span>

<span data-ttu-id="0e5be-113">Le funzionalità principali di WIC sono:</span><span class="sxs-lookup"><span data-stu-id="0e5be-113">The primary features of WIC are:</span></span>

-   <span data-ttu-id="0e5be-114">Consente agli sviluppatori di applicazioni di eseguire operazioni di elaborazione di immagini in qualsiasi formato di immagine tramite un unico set coerente di interfacce comuni, senza richiedere la conoscenza precedente di formati di immagine specifici.</span><span class="sxs-lookup"><span data-stu-id="0e5be-114">Enables application developers to perform image processing operations on any image format through a single, consistent set of common interfaces, without requiring prior knowledge of specific image formats.</span></span>
-   <span data-ttu-id="0e5be-115">Fornisce un'architettura "plug and Play" estendibile per codec di immagini, formati pixel e metadati, con l'individuazione automatica dei nuovi formati in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="0e5be-115">Provides an extensible "plug and play" architecture for image codecs, pixel formats, and metadata, with automatic run-time discovery of new formats.</span></span>
-   <span data-ttu-id="0e5be-116">Supporta la lettura e la scrittura di metadati arbitrari nei file di immagine, con la possibilità di mantenere i metadati non riconosciuti durante la modifica.</span><span class="sxs-lookup"><span data-stu-id="0e5be-116">Supports reading and writing of arbitrary metadata in image files, with the ability to preserve unrecognized metadata during editing.</span></span>
-   <span data-ttu-id="0e5be-117">Conserva i dati di immagini con profondità elevata, fino a 32 bit per canale, in tutta la pipeline di elaborazione delle immagini.</span><span class="sxs-lookup"><span data-stu-id="0e5be-117">Preserves high bit depth image data, up to 32 bits per channel, throughout the image processing pipeline.</span></span>
-   <span data-ttu-id="0e5be-118">Fornisce supporto incorporato per i formati di immagine più diffusi, i formati pixel e gli schemi di metadati.</span><span class="sxs-lookup"><span data-stu-id="0e5be-118">Provides built-in support for most popular image formats, pixel formats, and metadata schemas.</span></span>

## <a name="native-codecs"></a><span data-ttu-id="0e5be-119">Codec nativi</span><span class="sxs-lookup"><span data-stu-id="0e5be-119">Native Codecs</span></span>

<span data-ttu-id="0e5be-120">WIC include diversi codec predefiniti.</span><span class="sxs-lookup"><span data-stu-id="0e5be-120">WIC includes several built-in codecs.</span></span> <span data-ttu-id="0e5be-121">Con la piattaforma vengono forniti i codec standard seguenti.</span><span class="sxs-lookup"><span data-stu-id="0e5be-121">The following standard codecs are provided with the platform.</span></span> 

| <span data-ttu-id="0e5be-122">Codec</span><span class="sxs-lookup"><span data-stu-id="0e5be-122">Codec</span></span>                                                                                             | <span data-ttu-id="0e5be-123">Tipi MIME</span><span class="sxs-lookup"><span data-stu-id="0e5be-123">Mime Types</span></span>                       | <span data-ttu-id="0e5be-124">Decodificatori</span><span class="sxs-lookup"><span data-stu-id="0e5be-124">Decoders</span></span> | <span data-ttu-id="0e5be-125">Codificatori</span><span class="sxs-lookup"><span data-stu-id="0e5be-125">Encoders</span></span> |
|---------------------------------------------------------------------------------------------------|----------------------------------|----------|----------|
| <span data-ttu-id="0e5be-126">BMP (formato bitmap Windows), specifica BMP V5.</span><span class="sxs-lookup"><span data-stu-id="0e5be-126">BMP (Windows Bitmap Format), BMP Specification v5.</span></span>                                                | <span data-ttu-id="0e5be-127">image/bmp</span><span class="sxs-lookup"><span data-stu-id="0e5be-127">image/bmp</span></span>                        | <span data-ttu-id="0e5be-128">Sì</span><span class="sxs-lookup"><span data-stu-id="0e5be-128">Yes</span></span>      | <span data-ttu-id="0e5be-129">Sì</span><span class="sxs-lookup"><span data-stu-id="0e5be-129">Yes</span></span>      |
| <span data-ttu-id="0e5be-130">GIF (Graphics Interchange Format 89a), specifica GIF 89a/89m</span><span class="sxs-lookup"><span data-stu-id="0e5be-130">GIF (Graphics Interchange Format 89a), GIF Specification 89a/89m</span></span>                                  | <span data-ttu-id="0e5be-131">image/gif</span><span class="sxs-lookup"><span data-stu-id="0e5be-131">image/gif</span></span>                        | <span data-ttu-id="0e5be-132">Sì</span><span class="sxs-lookup"><span data-stu-id="0e5be-132">Yes</span></span>      | <span data-ttu-id="0e5be-133">Sì</span><span class="sxs-lookup"><span data-stu-id="0e5be-133">Yes</span></span>      |
| <span data-ttu-id="0e5be-134">ICO (formato icona)</span><span class="sxs-lookup"><span data-stu-id="0e5be-134">ICO (Icon Format)</span></span>                                                                                 | <span data-ttu-id="0e5be-135">immagine/ICO</span><span class="sxs-lookup"><span data-stu-id="0e5be-135">image/ico</span></span>                        | <span data-ttu-id="0e5be-136">Sì</span><span class="sxs-lookup"><span data-stu-id="0e5be-136">Yes</span></span>      | <span data-ttu-id="0e5be-137">No</span><span class="sxs-lookup"><span data-stu-id="0e5be-137">No</span></span>       |
| <span data-ttu-id="0e5be-138">JPEG (Joint Photographic Experts Group), specifica JFIF 1,02</span><span class="sxs-lookup"><span data-stu-id="0e5be-138">JPEG (Joint Photographic Experts Group), JFIF Specification 1.02</span></span>                                  | <span data-ttu-id="0e5be-139">image/jpeg, image/JPE, image/jpg</span><span class="sxs-lookup"><span data-stu-id="0e5be-139">image/jpeg, image/jpe, image/jpg</span></span> | <span data-ttu-id="0e5be-140">Sì</span><span class="sxs-lookup"><span data-stu-id="0e5be-140">Yes</span></span>      | <span data-ttu-id="0e5be-141">Sì</span><span class="sxs-lookup"><span data-stu-id="0e5be-141">Yes</span></span>      |
| <span data-ttu-id="0e5be-142">PNG (Portable Network Graphics), specifica PNG 1,2</span><span class="sxs-lookup"><span data-stu-id="0e5be-142">PNG (Portable Network Graphics), PNG Specification 1.2</span></span>                                            | <span data-ttu-id="0e5be-143">image/png</span><span class="sxs-lookup"><span data-stu-id="0e5be-143">image/png</span></span>                        | <span data-ttu-id="0e5be-144">Sì</span><span class="sxs-lookup"><span data-stu-id="0e5be-144">Yes</span></span>      | <span data-ttu-id="0e5be-145">Sì</span><span class="sxs-lookup"><span data-stu-id="0e5be-145">Yes</span></span>      |
| <span data-ttu-id="0e5be-146">TIFF (Tagged Image File Format), specifica TIFF 6,0</span><span class="sxs-lookup"><span data-stu-id="0e5be-146">TIFF (Tagged Image File Format), TIFF Specification 6.0</span></span>                                           | <span data-ttu-id="0e5be-147">image/TIFF, image/TIF</span><span class="sxs-lookup"><span data-stu-id="0e5be-147">image/tiff, image/tif</span></span>            | <span data-ttu-id="0e5be-148">Sì</span><span class="sxs-lookup"><span data-stu-id="0e5be-148">Yes</span></span>      | <span data-ttu-id="0e5be-149">Sì</span><span class="sxs-lookup"><span data-stu-id="0e5be-149">Yes</span></span>      |
| <span data-ttu-id="0e5be-150">Windows Media Photo, [specifiche foto HD 1,0](https://www.microsoft.com/whdc/xps/wmphoto.mspx)</span><span class="sxs-lookup"><span data-stu-id="0e5be-150">Windows Media Photo, [HD Photo Specification 1.0](https://www.microsoft.com/whdc/xps/wmphoto.mspx)</span></span> | <span data-ttu-id="0e5be-151">image/vnd. ms-phot</span><span class="sxs-lookup"><span data-stu-id="0e5be-151">image/vnd.ms-phot</span></span>                | <span data-ttu-id="0e5be-152">Sì</span><span class="sxs-lookup"><span data-stu-id="0e5be-152">Yes</span></span>      | <span data-ttu-id="0e5be-153">Sì</span><span class="sxs-lookup"><span data-stu-id="0e5be-153">Yes</span></span>      |
| <span data-ttu-id="0e5be-154">DDS (superficie DirectDraw)</span><span class="sxs-lookup"><span data-stu-id="0e5be-154">DDS (DirectDraw Surface)</span></span>                                                                          | <span data-ttu-id="0e5be-155">image/vnd. ms-DDS</span><span class="sxs-lookup"><span data-stu-id="0e5be-155">image/vnd.ms-dds</span></span>                 | <span data-ttu-id="0e5be-156">Sì</span><span class="sxs-lookup"><span data-stu-id="0e5be-156">Yes</span></span>      | <span data-ttu-id="0e5be-157">Sì</span><span class="sxs-lookup"><span data-stu-id="0e5be-157">Yes</span></span>      |



 

## <a name="related-topics"></a><span data-ttu-id="0e5be-158">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0e5be-158">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="0e5be-159">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="0e5be-159">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0e5be-160">Cenni preliminari sui metadati WIC</span><span class="sxs-lookup"><span data-stu-id="0e5be-160">WIC Metadata Overview</span></span>](-wic-about-metadata.md)
</dt> <dt>

<span data-ttu-id="0e5be-161">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="0e5be-161">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="0e5be-162">Come scrivere un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="0e5be-162">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

<span data-ttu-id="0e5be-163">[CODEC di esempio AITCodec](/previous-versions/dotnet/netframework-3.0/ms771770(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0e5be-163">[AITCodec Sample CODEC](/previous-versions/dotnet/netframework-3.0/ms771770(v=vs.85))</span></span>
</dt> </dl>

 

 
