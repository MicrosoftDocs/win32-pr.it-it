---
description: In questo argomento viene introdotto il decodificatore bitmap, un componente di base del codec Windows Imaging Component (WIC) utilizzato per decodificare i file di immagine da un flusso.
ms.assetid: 9dc8d2ec-5cc5-45fa-8a4d-5bdc3072c90c
title: Panoramica della decodifica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a15e6a9c914cfa220e1aad5bff4badeb8fc8cc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349871"
---
# <a name="decoding-overview"></a><span data-ttu-id="e5348-103">Panoramica della decodifica</span><span class="sxs-lookup"><span data-stu-id="e5348-103">Decoding Overview</span></span>

<span data-ttu-id="e5348-104">In questo argomento viene introdotto il decodificatore bitmap, un componente di base del codec Windows Imaging Component (WIC) utilizzato per decodificare i file di immagine da un flusso.</span><span class="sxs-lookup"><span data-stu-id="e5348-104">The topic introduces the bitmap decoder, a core Windows Imaging Component (WIC) codec component used to decode image files from a stream.</span></span>

<span data-ttu-id="e5348-105">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="e5348-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="e5348-106">Introduzione</span><span class="sxs-lookup"><span data-stu-id="e5348-106">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="e5348-107">Decodificatori bitmap nativi</span><span class="sxs-lookup"><span data-stu-id="e5348-107">Native Bitmap Decoders</span></span>](#native-bitmap-decoders)
-   [<span data-ttu-id="e5348-108">Creazione di un decodificatore bitmap</span><span class="sxs-lookup"><span data-stu-id="e5348-108">Creating a Bitmap Decoder</span></span>](#creating-a-bitmap-decoder)
-   [<span data-ttu-id="e5348-109">Estensibilità del decodificatore</span><span class="sxs-lookup"><span data-stu-id="e5348-109">Decoder Extensibility</span></span>](#decoder-extensibility)
-   [<span data-ttu-id="e5348-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e5348-110">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="e5348-111">Introduzione</span><span class="sxs-lookup"><span data-stu-id="e5348-111">Introduction</span></span>

<span data-ttu-id="e5348-112">I decodificatori di bitmap possono essere visualizzati come contenitore esterno di un'immagine digitale e forniscono l'accesso alle proprietà globali e ai frame di immagine.</span><span class="sxs-lookup"><span data-stu-id="e5348-112">Bitmap decoders can be viewed as the outer container of a digital image and provides access to global properties and image frames.</span></span> <span data-ttu-id="e5348-113">Alcuni formati di immagine supportano anteprime globali, anteprime, contesti di colore o metadati, mentre altri forniscono tali proprietà solo a livello di frame.</span><span class="sxs-lookup"><span data-stu-id="e5348-113">Some image formats support global thumbnails, previews, color contexts, or metadata, while others provide these properties only at the frame level.</span></span> <span data-ttu-id="e5348-114">Si noti tuttavia che molti dei formati di immagine standard non supportano queste proprietà globali.</span><span class="sxs-lookup"><span data-stu-id="e5348-114">Note, however, many of the standard image formats do not support these global properties.</span></span> <span data-ttu-id="e5348-115">Di conseguenza, molte delle implementazioni di codec native fornite da WIC non supportano la maggior parte di queste proprietà globali.</span><span class="sxs-lookup"><span data-stu-id="e5348-115">As such, many of the native codec implementations provided by WIC do not support the majority of these global properties.</span></span> <span data-ttu-id="e5348-116">Per informazioni sul supporto delle proprietà globali, vedere la tabella nella sezione decodificatori bitmap nativi di questo argomento.</span><span class="sxs-lookup"><span data-stu-id="e5348-116">See the table in the Native Bitmap Decoders section of this topic for information about global property support.</span></span>

<span data-ttu-id="e5348-117">In WIC i decodificatori di bitmap sono rappresentati dall'interfaccia [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) e forniscono l'accesso a queste proprietà globali della bitmap e, più importante, i frame in esso contenuti.</span><span class="sxs-lookup"><span data-stu-id="e5348-117">In WIC, bitmap decoders are represented by the [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) interface and provides access to these global properties of the bitmap and, more importantly, the frames it contains.</span></span> <span data-ttu-id="e5348-118">L'interfaccia [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) rappresenta un singolo frame bitmap ed è descritta in dettaglio nella [Panoramica delle origini bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="e5348-118">The [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) interface represents an individual bitmap frame and is discussed in detail in the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

## <a name="native-bitmap-decoders"></a><span data-ttu-id="e5348-119">Decodificatori bitmap nativi</span><span class="sxs-lookup"><span data-stu-id="e5348-119">Native Bitmap Decoders</span></span>

<span data-ttu-id="e5348-120">WIC fornisce diverse implementazioni native dell'interfaccia [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) per i formati di immagine Web standard e il formato di foto HD con intervallo dinamico elevato.</span><span class="sxs-lookup"><span data-stu-id="e5348-120">WIC provides several native implementations of the [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) interface for the standard web image formats and the high dynamic range HD Photo format.</span></span> <span data-ttu-id="e5348-121">Nella tabella seguente sono elencati i decodificatori nativi disponibili, il nome dell'identificatore di classe e il supporto per le proprietà globali.</span><span class="sxs-lookup"><span data-stu-id="e5348-121">The following table lists the available native decoders, class identifier name, and support for global properties.</span></span> <span data-ttu-id="e5348-122">Anche se una funzionalità potrebbe non supportare una proprietà, ad esempio anteprime a livello globale, il formato dell'immagine può supportare tali proprietà a livello di singolo frame.</span><span class="sxs-lookup"><span data-stu-id="e5348-122">Though a feature may not support a property such as thumbnails at the global level, the image format may support such properties at the individual frame level.</span></span>



| <span data-ttu-id="e5348-123">Formato immagine</span><span class="sxs-lookup"><span data-stu-id="e5348-123">Image Format</span></span> | <span data-ttu-id="e5348-124">Nome CLSID</span><span class="sxs-lookup"><span data-stu-id="e5348-124">CLSID Name</span></span>            | <span data-ttu-id="e5348-125">Anteprime</span><span class="sxs-lookup"><span data-stu-id="e5348-125">Thumbnails</span></span> | <span data-ttu-id="e5348-126">Anteprime</span><span class="sxs-lookup"><span data-stu-id="e5348-126">Previews</span></span> | <span data-ttu-id="e5348-127">Contesti colori</span><span class="sxs-lookup"><span data-stu-id="e5348-127">Color Contexts</span></span> | <span data-ttu-id="e5348-128">Metadati</span><span class="sxs-lookup"><span data-stu-id="e5348-128">Metadata</span></span> |
|--------------|-----------------------|------------|----------|----------------|----------|
| <span data-ttu-id="e5348-129">BMP</span><span class="sxs-lookup"><span data-stu-id="e5348-129">BMP</span></span>          | <span data-ttu-id="e5348-130">\_WICBMPDECODER CLSID</span><span class="sxs-lookup"><span data-stu-id="e5348-130">CLSID\_WICBmpDecoder</span></span>  | <span data-ttu-id="e5348-131">No</span><span class="sxs-lookup"><span data-stu-id="e5348-131">No</span></span>         | <span data-ttu-id="e5348-132">No</span><span class="sxs-lookup"><span data-stu-id="e5348-132">No</span></span>       | <span data-ttu-id="e5348-133">No</span><span class="sxs-lookup"><span data-stu-id="e5348-133">No</span></span>             | <span data-ttu-id="e5348-134">No</span><span class="sxs-lookup"><span data-stu-id="e5348-134">No</span></span>       |
| <span data-ttu-id="e5348-135">GIF</span><span class="sxs-lookup"><span data-stu-id="e5348-135">GIF</span></span>          | <span data-ttu-id="e5348-136">\_WICGIFDECODER CLSID</span><span class="sxs-lookup"><span data-stu-id="e5348-136">CLSID\_WICGifDecoder</span></span>  | <span data-ttu-id="e5348-137">No</span><span class="sxs-lookup"><span data-stu-id="e5348-137">No</span></span>         | <span data-ttu-id="e5348-138">No</span><span class="sxs-lookup"><span data-stu-id="e5348-138">No</span></span>       | <span data-ttu-id="e5348-139">No</span><span class="sxs-lookup"><span data-stu-id="e5348-139">No</span></span>             | <span data-ttu-id="e5348-140">Sì</span><span class="sxs-lookup"><span data-stu-id="e5348-140">Yes</span></span>      |
| <span data-ttu-id="e5348-141">ICO</span><span class="sxs-lookup"><span data-stu-id="e5348-141">ICO</span></span>          | <span data-ttu-id="e5348-142">\_WICICODECODER CLSID</span><span class="sxs-lookup"><span data-stu-id="e5348-142">CLSID\_WICIcoDecoder</span></span>  | <span data-ttu-id="e5348-143">No</span><span class="sxs-lookup"><span data-stu-id="e5348-143">No</span></span>         | <span data-ttu-id="e5348-144">No</span><span class="sxs-lookup"><span data-stu-id="e5348-144">No</span></span>       | <span data-ttu-id="e5348-145">No</span><span class="sxs-lookup"><span data-stu-id="e5348-145">No</span></span>             | <span data-ttu-id="e5348-146">No</span><span class="sxs-lookup"><span data-stu-id="e5348-146">No</span></span>       |
| <span data-ttu-id="e5348-147">JPEG</span><span class="sxs-lookup"><span data-stu-id="e5348-147">JPEG</span></span>         | <span data-ttu-id="e5348-148">\_WICJPEGDECODER CLSID</span><span class="sxs-lookup"><span data-stu-id="e5348-148">CLSID\_WICJpegDecoder</span></span> | <span data-ttu-id="e5348-149">No</span><span class="sxs-lookup"><span data-stu-id="e5348-149">No</span></span>         | <span data-ttu-id="e5348-150">No</span><span class="sxs-lookup"><span data-stu-id="e5348-150">No</span></span>       | <span data-ttu-id="e5348-151">No</span><span class="sxs-lookup"><span data-stu-id="e5348-151">No</span></span>             | <span data-ttu-id="e5348-152">No</span><span class="sxs-lookup"><span data-stu-id="e5348-152">No</span></span>       |
| <span data-ttu-id="e5348-153">PNG</span><span class="sxs-lookup"><span data-stu-id="e5348-153">PNG</span></span>          | <span data-ttu-id="e5348-154">\_WICPNGDECODER CLSID</span><span class="sxs-lookup"><span data-stu-id="e5348-154">CLSID\_WICPngDecoder</span></span>  | <span data-ttu-id="e5348-155">No</span><span class="sxs-lookup"><span data-stu-id="e5348-155">No</span></span>         | <span data-ttu-id="e5348-156">No</span><span class="sxs-lookup"><span data-stu-id="e5348-156">No</span></span>       | <span data-ttu-id="e5348-157">No</span><span class="sxs-lookup"><span data-stu-id="e5348-157">No</span></span>             | <span data-ttu-id="e5348-158">No</span><span class="sxs-lookup"><span data-stu-id="e5348-158">No</span></span>       |
| <span data-ttu-id="e5348-159">TIFF</span><span class="sxs-lookup"><span data-stu-id="e5348-159">TIFF</span></span>         | <span data-ttu-id="e5348-160">\_WICTIFFDECODER CLSID</span><span class="sxs-lookup"><span data-stu-id="e5348-160">CLSID\_WICTiffDecoder</span></span> | <span data-ttu-id="e5348-161">No</span><span class="sxs-lookup"><span data-stu-id="e5348-161">No</span></span>         | <span data-ttu-id="e5348-162">No</span><span class="sxs-lookup"><span data-stu-id="e5348-162">No</span></span>       | <span data-ttu-id="e5348-163">No</span><span class="sxs-lookup"><span data-stu-id="e5348-163">No</span></span>             | <span data-ttu-id="e5348-164">No</span><span class="sxs-lookup"><span data-stu-id="e5348-164">No</span></span>       |
| <span data-ttu-id="e5348-165">Foto HD</span><span class="sxs-lookup"><span data-stu-id="e5348-165">HD Photo</span></span>     | <span data-ttu-id="e5348-166">\_WICWMPDECODER CLSID</span><span class="sxs-lookup"><span data-stu-id="e5348-166">CLSID\_WICWmpDecoder</span></span>  | <span data-ttu-id="e5348-167">No</span><span class="sxs-lookup"><span data-stu-id="e5348-167">No</span></span>         | <span data-ttu-id="e5348-168">Sì</span><span class="sxs-lookup"><span data-stu-id="e5348-168">Yes</span></span>      | <span data-ttu-id="e5348-169">No</span><span class="sxs-lookup"><span data-stu-id="e5348-169">No</span></span>             | <span data-ttu-id="e5348-170">No</span><span class="sxs-lookup"><span data-stu-id="e5348-170">No</span></span>       |



 

## <a name="creating-a-bitmap-decoder"></a><span data-ttu-id="e5348-171">Creazione di un decodificatore bitmap</span><span class="sxs-lookup"><span data-stu-id="e5348-171">Creating a Bitmap Decoder</span></span>

<span data-ttu-id="e5348-172">Per decodificare un'immagine usando WIC, è prima di tutto necessario creare un'istanza di [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) per il formato di immagine di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e5348-172">To decode an image using WIC, you first need to create an instance of the [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) for the targeted image format.</span></span> <span data-ttu-id="e5348-173">L'istanza del decodificatore consente di accedere alle proprietà e ai metadati globali, se supportati, nonché ai frame dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="e5348-173">The decoder instance enables you to access the global properties and metadata, if supported, as well as the image frames.</span></span> <span data-ttu-id="e5348-174">WIC Imaging Factory, [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory), fornisce diversi metodi per la creazione di decodificatori di bitmap.</span><span class="sxs-lookup"><span data-stu-id="e5348-174">The WIC imaging factory, [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory), provides several methods for creating bitmap decoders.</span></span> <span data-ttu-id="e5348-175">Per creare i decodificatori di bitmap, vengono forniti i metodi factory seguenti.</span><span class="sxs-lookup"><span data-stu-id="e5348-175">The following factory methods are provided to create bitmap decoders.</span></span>

-   [<span data-ttu-id="e5348-176">**CreateDecoder**</span><span class="sxs-lookup"><span data-stu-id="e5348-176">**CreateDecoder**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoder)
-   [<span data-ttu-id="e5348-177">**CreateDecoderFromFileHandle**</span><span class="sxs-lookup"><span data-stu-id="e5348-177">**CreateDecoderFromFileHandle**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilehandle)
-   [<span data-ttu-id="e5348-178">**CreateDecoderFromFilename**</span><span class="sxs-lookup"><span data-stu-id="e5348-178">**CreateDecoderFromFilename**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename)
-   [<span data-ttu-id="e5348-179">**CreateDecoderFromStream**</span><span class="sxs-lookup"><span data-stu-id="e5348-179">**CreateDecoderFromStream**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream)

<span data-ttu-id="e5348-180">Il codice seguente illustra come creare un decodificatore bitmap usando un nome file di immagine e recuperare il primo frame dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="e5348-180">The following code demonstrates the how to create a bitmap decoder using an image filename and retrieve the first frame of the image.</span></span>


```C++
   // Create a decoder
   IWICBitmapDecoder *pDecoder = NULL;

   hr = m_pIWICFactory->CreateDecoderFromFilename(
       szFileName,                      // Image to be decoded
       NULL,                            // Do not prefer a particular vendor
       GENERIC_READ,                    // Desired read access to the file
       WICDecodeMetadataCacheOnDemand,  // Cache metadata when needed
       &pDecoder                        // Pointer to the decoder
       );

   // Retrieve the first frame of the image from the decoder
   IWICBitmapFrameDecode *pFrame = NULL;

   if (SUCCEEDED(hr))
   {
       hr = pDecoder->GetFrame(0, &pFrame);
   }
```



## <a name="decoder-extensibility"></a><span data-ttu-id="e5348-181">Estensibilità del decodificatore</span><span class="sxs-lookup"><span data-stu-id="e5348-181">Decoder Extensibility</span></span>

<span data-ttu-id="e5348-182">Una delle funzionalità principali di WIC è un Framework di estendibilità che consente agli sviluppatori di codec di sviluppare i propri codec di immagine e ottenere lo stesso supporto della piattaforma delle implementazioni native dei codec di immagine.</span><span class="sxs-lookup"><span data-stu-id="e5348-182">One of the core features of WIC is an extensibility framework that enables codec developers to develop their own image codecs and get the same platform support as the native implementations of image codecs.</span></span> <span data-ttu-id="e5348-183">Un unico set coerente di interfacce viene usato per l'elaborazione di tutte le immagini, indipendentemente dal formato di immagine.</span><span class="sxs-lookup"><span data-stu-id="e5348-183">A single, consistent set of interfaces is used for all image processing, regardless of image format.</span></span> <span data-ttu-id="e5348-184">Qualsiasi applicazione che utilizza WIC ottiene il supporto automatico per i nuovi formati di immagine non appena viene installato il codec.</span><span class="sxs-lookup"><span data-stu-id="e5348-184">Any application using WIC gets automatic support for new image formats as soon as the codec is installed.</span></span> <span data-ttu-id="e5348-185">Per ulteriori informazioni sullo sviluppo di codec, vedere gli argomenti relativi [allo sviluppo di componenti](-wic-component-development.md).</span><span class="sxs-lookup"><span data-stu-id="e5348-185">For more information on codec development, see the topics in [Component Development](-wic-component-development.md).</span></span> <span data-ttu-id="e5348-186">Per ulteriori informazioni sullo sviluppo di decodificatori, vedere [implementazione di un Decodificatore WIC-Enabled](-wic-implementingwicdecoder.md).</span><span class="sxs-lookup"><span data-stu-id="e5348-186">For more information on decoder development, see [Implementing a WIC-Enabled Decoder](-wic-implementingwicdecoder.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5348-187">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e5348-187">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="e5348-188">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="e5348-188">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e5348-189">Panoramica del componente imaging Windows</span><span class="sxs-lookup"><span data-stu-id="e5348-189">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="e5348-190">Panoramica della codifica</span><span class="sxs-lookup"><span data-stu-id="e5348-190">Encoding Overview</span></span>](-wic-creating-encoder.md)
</dt> <dt>

[<span data-ttu-id="e5348-191">Sviluppo di componenti</span><span class="sxs-lookup"><span data-stu-id="e5348-191">Component Development</span></span>](-wic-component-development.md)
</dt> </dl>

 

 



