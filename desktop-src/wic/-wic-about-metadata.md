---
description: In questo argomento viene illustrato il supporto dei metadati di imaging fornito da Windows Imaging Component (WIC).
ms.assetid: 35727810-3c4c-4c11-a4a2-3ae2cf3b8142
title: Cenni preliminari sui metadati WIC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f00e3a77eb74a3fb4a00db05ef9e00028f02ecf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104563732"
---
# <a name="wic-metadata-overview"></a><span data-ttu-id="f3cf1-103">Cenni preliminari sui metadati WIC</span><span class="sxs-lookup"><span data-stu-id="f3cf1-103">WIC Metadata Overview</span></span>

<span data-ttu-id="f3cf1-104">In questo argomento viene illustrato il supporto dei metadati di imaging fornito da Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="f3cf1-104">This topic introduces the imaging metadata support provided by the Windows Imaging Component (WIC).</span></span> <span data-ttu-id="f3cf1-105">Viene fornita un'introduzione alla lettura e alla scrittura dei metadati delle immagini, del linguaggio di query dei metadati e dell'estensibilità del gestore di metadati.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-105">It provides an introduction to reading and writing image metadata, the metadata query language, and metadata handler extensibility.</span></span>

<span data-ttu-id="f3cf1-106">I metadati delle immagini sono dati incorporati all'interno di un file di immagine che fornisce informazioni aggiuntive sull'immagine, ad esempio il dispositivo usato per acquisire l'immagine o le dimensioni dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-106">Image metadata is data embedded inside an image file that provides additional information about the image, such as the device used to capture the image or the dimensions of the image.</span></span> <span data-ttu-id="f3cf1-107">Sebbene sia contenuto all'interno del file di immagine, questi metadati non fanno parte dei dati di rendering.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-107">Although it is contained within the image file itself, this metadata is not part of the rendering data.</span></span> <span data-ttu-id="f3cf1-108">WIC fornisce interfacce che consentono di leggere e scrivere questi metadati per diversi formati di metadati comuni, tra cui Extensible Metadata Platform (XMP), Scambioable image file (EXIF) e dati testuali png (testo).</span><span class="sxs-lookup"><span data-stu-id="f3cf1-108">WIC provides interfaces that enable you to read and write this metadata for several common metadata formats including Extensible Metadata Platform (XMP), Exchangeable Image File (EXIF), and Png Textual Data (tEXt).</span></span>

<span data-ttu-id="f3cf1-109">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-109">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="f3cf1-110">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="f3cf1-110">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="f3cf1-111">Introduzione</span><span class="sxs-lookup"><span data-stu-id="f3cf1-111">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="f3cf1-112">Lettura dei metadati delle immagini</span><span class="sxs-lookup"><span data-stu-id="f3cf1-112">Reading Image Metadata</span></span>](#reading-image-metadata)
-   [<span data-ttu-id="f3cf1-113">Scrittura dei metadati delle immagini</span><span class="sxs-lookup"><span data-stu-id="f3cf1-113">Writing Image Metadata</span></span>](#writing-image-metadata)
-   [<span data-ttu-id="f3cf1-114">Estensibilità dei metadati</span><span class="sxs-lookup"><span data-stu-id="f3cf1-114">Metadata Extensibility</span></span>](#metadata-extensibility)
-   [<span data-ttu-id="f3cf1-115">Formati di metadati supportati</span><span class="sxs-lookup"><span data-stu-id="f3cf1-115">Supported Metadata Formats</span></span>](#supported-metadata-formats)
-   [<span data-ttu-id="f3cf1-116">Riepilogo componenti metadati</span><span class="sxs-lookup"><span data-stu-id="f3cf1-116">Metadata Component Summary</span></span>](#metadata-component-summary)
-   [<span data-ttu-id="f3cf1-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f3cf1-117">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="f3cf1-118">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="f3cf1-118">Prerequisites</span></span>

<span data-ttu-id="f3cf1-119">Per comprendere questo argomento, è necessario conoscere le interfacce del codificatore e del decodificatore WIC e i relativi componenti COM (Component Object Model), come descritto in [Panoramica dei componenti di Windows Imaging](-wic-about-windows-imaging-codec.md).</span><span class="sxs-lookup"><span data-stu-id="f3cf1-119">To understand this topic, you should be familiar with the WIC encoder and decoder interfaces and their related Component Object Model (COM) components, as described in the [Windows Imaging Component Overview](-wic-about-windows-imaging-codec.md).</span></span> <span data-ttu-id="f3cf1-120">Consente inoltre di avere una certa familiarità con alcuni formati di metadati di imaging attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-120">It also helps to have a general familiarity with some of the imaging metadata formats in use today.</span></span>

## <a name="introduction"></a><span data-ttu-id="f3cf1-121">Introduzione</span><span class="sxs-lookup"><span data-stu-id="f3cf1-121">Introduction</span></span>

<span data-ttu-id="f3cf1-122">I metadati forniscono informazioni estese su un'immagine.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-122">Metadata provides extended information about an image.</span></span> <span data-ttu-id="f3cf1-123">Queste informazioni possono essere usate in diversi modi.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-123">This information can be used in several ways.</span></span> <span data-ttu-id="f3cf1-124">Un'immagine potrebbe contenere metadati, ad esempio una descrizione, una classificazione, tag di categoria e informazioni sul copyright.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-124">An image might contain metadata such as a description, rating, category tags, and copyright information.</span></span> <span data-ttu-id="f3cf1-125">L'accesso ai metadati rende più semplice eseguire attività quali la gestione delle risorse, il percorso del file o la determinazione delle informazioni sul copyright.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-125">Accessing the metadata makes it easier to perform tasks such as asset management, file location, or determining copyright information.</span></span> <span data-ttu-id="f3cf1-126">La raccolta foto di Windows in Windows Vista, ad esempio, consente di aggiungere descrizioni e tag di categoria alle immagini.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-126">For example, the Windows Photo Gallery in Windows Vista enables you to add descriptions and category tags to images.</span></span> <span data-ttu-id="f3cf1-127">Questo consente una migliore individuabilità delle immagini e un modo pratico per suddividere in categorie le immagini.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-127">This allows for better discoverability of images and a convenient way to categorize images.</span></span> <span data-ttu-id="f3cf1-128">Utilizzando le API WIC e i formati di metadati comuni, le applicazioni possono scrivere o leggere facilmente questo tipo di metadati in o da immagini.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-128">Using the WIC APIs and common metadata formats, applications can easily write or read this type of metadata to or from images.</span></span>

<span data-ttu-id="f3cf1-129">Il diagramma seguente illustra il contenuto di un file JPEG che include i blocchi di metadati incorporati e gli elementi di metadati.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-129">The following diagram illustrates the contents of a JPEG file that includes embedded metadata blocks and metadata items.</span></span>

![immagine JPEG con metadati di classificazione](graphics/jpeg.png)

<span data-ttu-id="f3cf1-131">In questa immagine di esempio, i metadati sono incorporati nel file di immagine in un frame di immagine.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-131">In this example image, the metadata is embedded in the image file within an image frame.</span></span> <span data-ttu-id="f3cf1-132">Il formato JPEG non supporta più frame immagine, quindi i metadati vengono associati concettualmente a questo singolo frame.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-132">The JPEG format does not support multiple image frames, so the metadata is conceptually attached to this single frame.</span></span> <span data-ttu-id="f3cf1-133">I formati che supportano più frame, ad esempio TIFF, possono avere metadati collegati a ogni fotogramma immagine come illustrato nel diagramma.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-133">Formats that support multiple frames, such as TIFF, may have metadata attached to each image frame as this diagram shows.</span></span> <span data-ttu-id="f3cf1-134">Sebbene non sia attualmente comune e non supportato dai codec di immagini native, alcuni formati di immagine possono supportare anche i metadati all'esterno di un frame di immagine.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-134">Though not common today and not supported by the native image codecs, some image formats may also support metadata outside of an image frame.</span></span> <span data-ttu-id="f3cf1-135">WIC è sufficientemente flessibile per gestire metadati a livello di frame e metadati al di fuori del singolo frame di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-135">WIC is flexible enough to handle both frame-level metadata and metadata outside of an image's individual frame.</span></span>

## <a name="reading-image-metadata"></a><span data-ttu-id="f3cf1-136">Lettura dei metadati delle immagini</span><span class="sxs-lookup"><span data-stu-id="f3cf1-136">Reading Image Metadata</span></span>

<span data-ttu-id="f3cf1-137">Le API WIC forniscono componenti COM che semplificano la lettura e la scrittura dei metadati delle immagini da parte delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-137">The WIC APIs provide COM components that make it easy for applications to read and write image metadata.</span></span>

<span data-ttu-id="f3cf1-138">Il modo principale per leggere i metadati consiste nell'usare un lettore di query di metadati ([**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)) per accedere a elementi di metadati specifici.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-138">The primary way to read metadata is to use a metadata query reader ([**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)) to access specific metadata items.</span></span> <span data-ttu-id="f3cf1-139">Il componente lettore di query dei metadati viene implementato dal codec ed è accessibile a livello di decodificatore o con singoli fotogrammi immagine, che è il metodo più comune.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-139">The metadata query reader component is implemented by the codec and can be accessed at the decoder level or through individual image frames, which is the more common method.</span></span> <span data-ttu-id="f3cf1-140">Il codice seguente illustra come accedere a un lettore di query per un singolo frame usando il metodo **GetMetadataQueryReader** del lettore di query.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-140">The following code demonstrates how to access a query reader for an individual frame by using the query reader's **GetMetadataQueryReader** method.</span></span>


```
// Get the query reader
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}
```



<span data-ttu-id="f3cf1-141">Un lettore di query fornisce metodi per ottenere informazioni su metadati specifici e un metodo per specificare un elemento di metadati da recuperare.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-141">A query reader provides methods to obtain information about specific metadata, and a means to specify a metadata item to retrieve.</span></span> <span data-ttu-id="f3cf1-142">Nel codice seguente viene usata un'espressione di query per richiedere un elemento di metadati specifico all'interno del blocco IFD (App1 nested image file directory).</span><span class="sxs-lookup"><span data-stu-id="f3cf1-142">The following code uses a query expression to request a specific metadata item within the App1 nested image file directory (IFD) block.</span></span> <span data-ttu-id="f3cf1-143">Questa operazione viene eseguita usando il metodo **GetMetadataByName** del lettore di query.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-143">This is done by using the query reader's **GetMetadataByName** method.</span></span> <span data-ttu-id="f3cf1-144">Nel codice seguente viene illustrato l'utilizzo di query Reader per ottenere il valore della classificazione MicrosoftPhoto.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-144">The following code demonstrates using the query reader to obtain the MicrosoftPhoto rating value.</span></span>


```
PROPVARIANT value;
PropVariantInit(&value);

LPCWSTR pwzRatingQuery = L"/app1/ifd/{ushort=18249}";

if (SUCCEEDED(hr))
{
    hr = pQueryReader->GetMetadataByName(pwzRatingQuery, &value);
}
```



<span data-ttu-id="f3cf1-145">La variabile pwzRatingQuery nell'esempio precedente è la stringa di query per accedere alla classificazione MicrosoftPhoto dell'elemento dei metadati.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-145">The pwzRatingQuery variable in the preceding example is the query string to access the metadata item MicrosoftPhoto rating.</span></span> <span data-ttu-id="f3cf1-146">Questa stringa viene creata utilizzando il linguaggio di query dei metadati.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-146">This string is created by using the metadata query language.</span></span> <span data-ttu-id="f3cf1-147">Per creare questa stringa, è necessario conoscere il formato dei metadati e il linguaggio di query dei metadati per recuperare singoli elementi di metadati.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-147">To create this string, knowledge of the metadata format and the metadata query language is needed to retrieve individual metadata items.</span></span> <span data-ttu-id="f3cf1-148">Per ulteriori informazioni sul linguaggio di query dei metadati, vedere [Cenni preliminari sul linguaggio di query dei metadati](-wic-codec-metadataquerylanguage.md).</span><span class="sxs-lookup"><span data-stu-id="f3cf1-148">For more information about the metadata query language, see the [Metadata Query Language Overview](-wic-codec-metadataquerylanguage.md).</span></span>

<span data-ttu-id="f3cf1-149">Dietro le quinte, un lettore di query usa un lettore di metadati ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) per accedere ai metadati descritti dall'espressione di query.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-149">Behind the scenes, a query reader uses a metadata reader ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) to access the metadata described by the query expression.</span></span> <span data-ttu-id="f3cf1-150">Oltre a usare un lettore di query, è anche possibile accedere direttamente a un lettore di metadati per leggere i metadati.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-150">In addition to using a query reader, you can also access a metadata reader directly to read metadata.</span></span> <span data-ttu-id="f3cf1-151">È possibile ottenere un lettore di metadati dal decodificatore o da singoli frame eseguendo una query per un'interfaccia di lettura a blocchi ([**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)).</span><span class="sxs-lookup"><span data-stu-id="f3cf1-151">You can obtain a metadata reader from the decoder or individual frames by querying for a block reader ([**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)) interface.</span></span>

## <a name="writing-image-metadata"></a><span data-ttu-id="f3cf1-152">Scrittura dei metadati delle immagini</span><span class="sxs-lookup"><span data-stu-id="f3cf1-152">Writing Image Metadata</span></span>

<span data-ttu-id="f3cf1-153">Il processo di scrittura dei metadati è simile al modo in cui viene letto, ad eccezione del fatto che viene utilizzato un writer di query di metadati ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)).</span><span class="sxs-lookup"><span data-stu-id="f3cf1-153">The process of writing metadata is similar to the way it is read except that a metadata query writer ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)) is used.</span></span> <span data-ttu-id="f3cf1-154">L'interfaccia del writer di query è implementata dal codificatore di immagini e, come nel lettore di query, si accede ai metadati sia nel codificatore che nei singoli frame, a seconda del supporto del formato di immagine.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-154">The query writer interface is implemented by the image encoder and, as in the query reader, metadata is accessed both on the encoder and on individual frames (depending on image format support).</span></span>

<span data-ttu-id="f3cf1-155">Nel codice seguente viene illustrato come ottenere un writer di query da un frame del codificatore e rimuovere il valore della classificazione precedentemente letto.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-155">The following code demonstrates how to obtain a query writer from an encoder frame and remove the rating value that was previously read.</span></span>


```
// Get the frame's query writer
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
}

if (SUCCEEDED(hr))
{
    hr = pFrameQWriter->RemoveMetadataByName(L"/app1/ifd/{ushort=18249}");
}
```



<span data-ttu-id="f3cf1-156">Un altro modo per scrivere i metadati consiste nell'eseguire aggiornamenti rapidi dei metadati.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-156">Another way to write metadata is through fast metadata updates.</span></span> <span data-ttu-id="f3cf1-157">La codifica rapida dei metadati è un modo per scrivere i metadati delle immagini senza dover codificare nuovamente un file di immagine.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-157">Fast metadata encoding is a way to write image metadata without having to re-encode an image file.</span></span> <span data-ttu-id="f3cf1-158">Questa operazione viene eseguita scrivendo nuove informazioni sui metadati in un'area imbottita del formato dei metadati.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-158">This is done by writing new metadata information to a padded region of the metadata format.</span></span> <span data-ttu-id="f3cf1-159">Il codificatore di metadati rapido ([**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)) viene ottenuto dalla factory del componente, in base al decodificatore di immagini.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-159">The fast metadata encoder ([**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)) is obtained from the component factory, based on the image decoder.</span></span> <span data-ttu-id="f3cf1-160">Il codificatore di metadati veloci ottiene quindi un writer di query usato per scrivere i metadati.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-160">The fast metadata encoder then obtains a query writer that is used to write the metadata.</span></span> <span data-ttu-id="f3cf1-161">Infine, il codificatore Fast conferma la modifica.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-161">Finally, the fast encoder commits the change.</span></span>

<span data-ttu-id="f3cf1-162">Il codice seguente illustra come ottenere un codificatore di metadati rapido e usarlo per scrivere il valore MicrosoftRating.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-162">The following code demonstrates how to obtain a fast metadata encoder and use it to write the MicrosoftRating value.</span></span>


```
if (SUCCEEDED(hr))
{
    IWICFastMetadataEncoder *pFME = NULL;
    IWICMetadataQueryWriter *pFMEQW = NULL;

    hr = pFactory->CreateFastMetadataEncoderFromFrameDecode(
        pFrameDecode,
        &pFME);

    if (SUCCEEDED(hr))
    {
        hr = pFME->GetMetadataQueryWriter(&pFMEQW);
    }

    if (SUCCEEDED(hr))
    {
        // Add additional metadata
        PROPVARIANT value;

        PropVariantInit(&value);

        value.vt = VT_UI4;
        value.uiVal = 99;
        hr = pFMEQW->SetMetadataByName(L"/app1/ifd/{ushort=18249}", &value);

        PropVariantClear(&value);
    }

    if (SUCCEEDED(hr))
    {
        hr = pFME->Commit();
    }
}
```



<span data-ttu-id="f3cf1-163">Non tutti i formati di metadati supportano metadati veloci.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-163">Not all metadata formats support fast metadata.</span></span> <span data-ttu-id="f3cf1-164">Per vedere quali formati supportati in modo nativo supportano la codifica dei metadati veloce, vedere la tabella nella sezione [formati di metadati supportati](#supported-metadata-formats) più avanti in questo documento.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-164">To see which natively supported formats support fast metadata encoding, see the table in the [Supported Metadata Formats](#supported-metadata-formats) section later in this document.</span></span>

<span data-ttu-id="f3cf1-165">Dietro le quinte, un writer di query utilizza un writer di metadati ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)) per scrivere i metadati descritti dall'espressione di query.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-165">Behind the scenes, a query writer uses a metadata writer ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)) to write the metadata described by the query expression.</span></span> <span data-ttu-id="f3cf1-166">Oltre a usare un lettore di query, è anche possibile accedere direttamente a un writer di metadati per la scrittura dei metadati.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-166">In addition to using a query reader, you can also access a metadata writer directly to write metadata.</span></span> <span data-ttu-id="f3cf1-167">È possibile ottenere un writer di metadati dal decodificatore o da singoli frame usando l'esecuzione di query per un'interfaccia di writer di blocco ([**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)).</span><span class="sxs-lookup"><span data-stu-id="f3cf1-167">You can obtain a metadata writer from the decoder or individual frames using querying for a block writer ([**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)) interface.</span></span>

## <a name="metadata-extensibility"></a><span data-ttu-id="f3cf1-168">Estensibilità dei metadati</span><span class="sxs-lookup"><span data-stu-id="f3cf1-168">Metadata Extensibility</span></span>

<span data-ttu-id="f3cf1-169">Come indicato in precedenza, WIC fornisce diversi gestori di metadati per la lettura e la scrittura dei metadati per i formati di metadati comuni.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-169">As mentioned previously, WIC provides several metadata handlers to read and write metadata for common metadata formats.</span></span> <span data-ttu-id="f3cf1-170">Tuttavia, esistono alcuni formati di metadati che non sono supportati in modo nativo.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-170">However, there are some metadata formats that are not natively supported.</span></span> <span data-ttu-id="f3cf1-171">WIC fornisce pertanto le API per la creazione di gestori di metadati aggiuntivi che possono estendere il supporto dei metadati ad altri formati.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-171">Therefore, WIC provides APIs for creating additional metadata handlers that can extend metadata support to other formats.</span></span>

<span data-ttu-id="f3cf1-172">Per supportare completamente altri formati di metadati, è necessario sviluppare due tipi di gestori, ovvero un lettore di metadati per leggere i metadati e un writer di metadati per la scrittura dei metadati.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-172">To fully support other metadata formats, two types of handlers must be developed — a metadata reader to read metadata and a metadata writer to write metadata.</span></span> <span data-ttu-id="f3cf1-173">Sebbene questi due gestori vengono in genere implementati in coppie per un formato specifico, questo non è un requisito.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-173">Although these two handlers are usually implemented in pairs for a specific format, that is not a requirement.</span></span> <span data-ttu-id="f3cf1-174">Potrebbero esserci alcuni casi in cui è necessaria solo la capacità di lettura o solo la funzionalità di scrittura.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-174">There might be some cases in which only the read ability or only the write ability is needed.</span></span>

<span data-ttu-id="f3cf1-175">Per ulteriori informazioni sull'estendibilità dei metadati mediante le API WIC, vedere [Cenni preliminari sull'estendibilità dei metadati](-wic-codec-metadatahandlers.md).</span><span class="sxs-lookup"><span data-stu-id="f3cf1-175">For more information on metadata extensibility using the WIC APIs, see the [Metadata Extensibility Overview](-wic-codec-metadatahandlers.md).</span></span>

## <a name="supported-metadata-formats"></a><span data-ttu-id="f3cf1-176">Formati di metadati supportati</span><span class="sxs-lookup"><span data-stu-id="f3cf1-176">Supported Metadata Formats</span></span>

<span data-ttu-id="f3cf1-177">WIC fornisce supporto per diversi formati di metadati comuni.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-177">WIC provides support for several common metadata formats.</span></span> <span data-ttu-id="f3cf1-178">Nella tabella seguente sono elencati i formati di metadati supportati, le relative versioni, i formati di immagine che supportano il formato dei metadati e se il formato dei metadati supporta la codifica rapida dei metadati.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-178">The following table lists the supported metadata formats, their versions, the image formats that support the metadata format, and whether the metadata format supports fast metadata encoding.</span></span> <span data-ttu-id="f3cf1-179">Per ulteriori informazioni sulla codifica rapida dei metadati, vedere la sezione [scrittura dei metadati delle immagini](#writing-image-metadata) più indietro in questo documento.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-179">For more information about fast metadata encoding, see the [Writing Image Metadata](#writing-image-metadata) section earlier in this document.</span></span>



| <span data-ttu-id="f3cf1-180">Formati di metadati supportati</span><span class="sxs-lookup"><span data-stu-id="f3cf1-180">Supported metadata formats</span></span> | <span data-ttu-id="f3cf1-181">Versione della specifica dei metadati</span><span class="sxs-lookup"><span data-stu-id="f3cf1-181">Metadata specification version</span></span> | <span data-ttu-id="f3cf1-182">Supporto del formato immagine</span><span class="sxs-lookup"><span data-stu-id="f3cf1-182">Image format support</span></span> | <span data-ttu-id="f3cf1-183">Supporta la codifica rapida dei metadati</span><span class="sxs-lookup"><span data-stu-id="f3cf1-183">Supports fast metadata encoding</span></span> |
|----------------------------|--------------------------------|----------------------|---------------------------------|
| <span data-ttu-id="f3cf1-184">App0</span><span class="sxs-lookup"><span data-stu-id="f3cf1-184">App0</span></span>                       | <span data-ttu-id="f3cf1-185">JFIF 1,02</span><span class="sxs-lookup"><span data-stu-id="f3cf1-185">JFIF 1.02</span></span>                      | <span data-ttu-id="f3cf1-186">JPEG</span><span class="sxs-lookup"><span data-stu-id="f3cf1-186">JPEG</span></span>                 | <span data-ttu-id="f3cf1-187">No</span><span class="sxs-lookup"><span data-stu-id="f3cf1-187">No</span></span>                              |
| <span data-ttu-id="f3cf1-188">App1</span><span class="sxs-lookup"><span data-stu-id="f3cf1-188">App1</span></span>                       | <span data-ttu-id="f3cf1-189">JFIF 1,02</span><span class="sxs-lookup"><span data-stu-id="f3cf1-189">JFIF 1.02</span></span>                      | <span data-ttu-id="f3cf1-190">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="f3cf1-190">JPEG, TIFF</span></span>           | <span data-ttu-id="f3cf1-191">No</span><span class="sxs-lookup"><span data-stu-id="f3cf1-191">No</span></span>                              |
| <span data-ttu-id="f3cf1-192">App13</span><span class="sxs-lookup"><span data-stu-id="f3cf1-192">App13</span></span>                      | <span data-ttu-id="f3cf1-193">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="f3cf1-193">Unknown</span></span>                        | <span data-ttu-id="f3cf1-194">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="f3cf1-194">JPEG, TIFF</span></span>           | <span data-ttu-id="f3cf1-195">No</span><span class="sxs-lookup"><span data-stu-id="f3cf1-195">No</span></span>                              |
| <span data-ttu-id="f3cf1-196">IFD</span><span class="sxs-lookup"><span data-stu-id="f3cf1-196">IFD</span></span>                        | <span data-ttu-id="f3cf1-197">TIFF 6,0</span><span class="sxs-lookup"><span data-stu-id="f3cf1-197">TIFF 6.0</span></span>                       | <span data-ttu-id="f3cf1-198">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="f3cf1-198">JPEG, TIFF</span></span>           | <span data-ttu-id="f3cf1-199">Sì</span><span class="sxs-lookup"><span data-stu-id="f3cf1-199">Yes</span></span>                             |
| <span data-ttu-id="f3cf1-200">IRB</span><span class="sxs-lookup"><span data-stu-id="f3cf1-200">IRB</span></span>                        | <span data-ttu-id="f3cf1-201">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="f3cf1-201">Unknown</span></span>                        | <span data-ttu-id="f3cf1-202">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="f3cf1-202">JPEG, TIFF</span></span>           | <span data-ttu-id="f3cf1-203">No</span><span class="sxs-lookup"><span data-stu-id="f3cf1-203">No</span></span>                              |
| <span data-ttu-id="f3cf1-204">Exif</span><span class="sxs-lookup"><span data-stu-id="f3cf1-204">Exif</span></span>                       | <span data-ttu-id="f3cf1-205">EXIF 2,2</span><span class="sxs-lookup"><span data-stu-id="f3cf1-205">Exif 2.2</span></span>                       | <span data-ttu-id="f3cf1-206">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="f3cf1-206">JPEG, TIFF</span></span>           | <span data-ttu-id="f3cf1-207">Sì</span><span class="sxs-lookup"><span data-stu-id="f3cf1-207">Yes</span></span>                             |
| <span data-ttu-id="f3cf1-208">XMP</span><span class="sxs-lookup"><span data-stu-id="f3cf1-208">XMP</span></span>                        | <span data-ttu-id="f3cf1-209">XMP 1,0 (settembre 2005)</span><span class="sxs-lookup"><span data-stu-id="f3cf1-209">XMP 1.0 (Sept 2005)</span></span>            | <span data-ttu-id="f3cf1-210">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="f3cf1-210">JPEG, TIFF</span></span>           | <span data-ttu-id="f3cf1-211">Sì</span><span class="sxs-lookup"><span data-stu-id="f3cf1-211">Yes</span></span>                             |
| <span data-ttu-id="f3cf1-212">GPS</span><span class="sxs-lookup"><span data-stu-id="f3cf1-212">GPS</span></span>                        | <span data-ttu-id="f3cf1-213">EXIF 2,2</span><span class="sxs-lookup"><span data-stu-id="f3cf1-213">Exif 2.2</span></span>                       | <span data-ttu-id="f3cf1-214">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="f3cf1-214">JPEG, TIFF</span></span>           | <span data-ttu-id="f3cf1-215">Sì</span><span class="sxs-lookup"><span data-stu-id="f3cf1-215">Yes</span></span>                             |
| <span data-ttu-id="f3cf1-216">IPTC</span><span class="sxs-lookup"><span data-stu-id="f3cf1-216">IPTC</span></span>                       | <span data-ttu-id="f3cf1-217">IPTC 4,0</span><span class="sxs-lookup"><span data-stu-id="f3cf1-217">IPTC 4.0</span></span>                       | <span data-ttu-id="f3cf1-218">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="f3cf1-218">JPEG, TIFF</span></span>           | <span data-ttu-id="f3cf1-219">Sì</span><span class="sxs-lookup"><span data-stu-id="f3cf1-219">Yes</span></span>                             |
| <span data-ttu-id="f3cf1-220">Testo</span><span class="sxs-lookup"><span data-stu-id="f3cf1-220">tEXt</span></span>                       | <span data-ttu-id="f3cf1-221">PNG 1,2</span><span class="sxs-lookup"><span data-stu-id="f3cf1-221">PNG 1.2</span></span>                        | <span data-ttu-id="f3cf1-222">PNG</span><span class="sxs-lookup"><span data-stu-id="f3cf1-222">PNG</span></span>                  | <span data-ttu-id="f3cf1-223">No</span><span class="sxs-lookup"><span data-stu-id="f3cf1-223">No</span></span>                              |



 

> [!Note]  
> <span data-ttu-id="f3cf1-224">IPTC supporta solo FME se le dimensioni dei blocchi aumentano, perché IPTC non supporta la spaziatura interna.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-224">IPTC only supports FME if the blocks grow in size, as IPTC does not support padding.</span></span>

 

## <a name="metadata-component-summary"></a><span data-ttu-id="f3cf1-225">Riepilogo componenti metadati</span><span class="sxs-lookup"><span data-stu-id="f3cf1-225">Metadata Component Summary</span></span>

<span data-ttu-id="f3cf1-226">Nella tabella seguente vengono descritte le interfacce WIC che supportano i metadati e i relativi componenti.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-226">The following table describes the WIC interfaces that support metadata, and their corresponding components.</span></span> <span data-ttu-id="f3cf1-227">Questi componenti forniscono l'accesso ai metadati di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-227">These components provide the access to an image's metadata.</span></span> <span data-ttu-id="f3cf1-228">Per ulteriori informazioni su questi componenti, vedere [Cenni preliminari sul componente Windows Imaging](-wic-about-windows-imaging-codec.md).</span><span class="sxs-lookup"><span data-stu-id="f3cf1-228">For more information about these components, see the [Windows Imaging Component Overview](-wic-about-windows-imaging-codec.md).</span></span> 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f3cf1-229">Componente</span><span class="sxs-lookup"><span data-stu-id="f3cf1-229">Component</span></span></th>
<th><span data-ttu-id="f3cf1-230">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f3cf1-230">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f3cf1-231">Decodificatore bitmap (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder"><strong>IWICBitmapDecoder</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="f3cf1-231">Bitmap Decoder (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder"><strong>IWICBitmapDecoder</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="f3cf1-232">Legge un flusso di immagini e produce un'origine bitmap utilizzabile.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-232">Reads an image stream and produces a usable bitmap source.</span></span> <span data-ttu-id="f3cf1-233">Associato a un formato di contenitore, ad esempio Tagged Image File Format (TIFF) o Joint Photographic Experts Group (JPEG).</span><span class="sxs-lookup"><span data-stu-id="f3cf1-233">Associated with a container format such as Tagged Image File Format (TIFF) or Joint Photographic Experts Group (JPEG).</span></span></li>
<li><span data-ttu-id="f3cf1-234">Implementa un'interfaccia <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a> per enumerare tutti i blocchi di metadati nel flusso di dati del decodificatore che non si trovano all'interno di un frame.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-234">Implements an <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a> interface to enumerate all of the metadata blocks in the decoder's data stream that are not inside a frame.</span></span></li>
<li><span data-ttu-id="f3cf1-235">Espone un lettore di query per leggere i metadati associati all'immagine che non si trova all'interno di un frame.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-235">Exposes a query reader to read the metadata associated with the image that is not inside a frame.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3cf1-236">Bitmap frame Decode (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode"><strong>IWICBitmapFrameDecode</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="f3cf1-236">Bitmap Frame Decode (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode"><strong>IWICBitmapFrameDecode</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="f3cf1-237">Accede a singoli frame dal flusso di immagini utilizzato dal decodificatore.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-237">Accesses individual frames from the image stream held by the decoder.</span></span></li>
<li><span data-ttu-id="f3cf1-238">Implementa un'interfaccia <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a> per enumerare tutti i blocchi di metadati nel flusso di dati del frame.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-238">Implements an <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a> interface to enumerate all of the metadata blocks in the frame's data stream.</span></span></li>
<li><span data-ttu-id="f3cf1-239">Espone un lettore di query per leggere i metadati associati al frame, usando espressioni di query.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-239">Exposes a query reader to read the metadata associated with the frame, using query expressions.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f3cf1-240">Codificatore bitmap (<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder"><strong>IWICBitmapEncoder</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="f3cf1-240">Bitmap Encoder (<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder"><strong>IWICBitmapEncoder</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="f3cf1-241">Scrive un'origine bitmap in un flusso di immagini.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-241">Writes a bitmap source to an image stream.</span></span> <span data-ttu-id="f3cf1-242">Associato a un formato di contenitore, ad esempio TIFF o JPEG.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-242">Associated with a container format such as TIFF or JPEG.</span></span></li>
<li><span data-ttu-id="f3cf1-243">Implementa un'interfaccia <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a> per creare un elenco di blocchi di metadati da scrivere nel flusso di dati del codificatore.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-243">Implements an <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a> interface to build up a list of metadata blocks to write into the data stream of the encoder.</span></span></li>
<li><span data-ttu-id="f3cf1-244">Espone un writer di query per scrivere i metadati associati all'immagine, usando espressioni di query.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-244">Exposes a query writer to write the metadata associated with the image, using query expressions.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3cf1-245">Bitma frame Encode (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode"><strong>IWICBitmapFrameEncode</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="f3cf1-245">Bitma Frame Encode (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode"><strong>IWICBitmapFrameEncode</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="f3cf1-246">Crea un frame che verrà codificato nel flusso utilizzato dal codificatore.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-246">Creates a frame that will be encoded into the stream held by the encoder.</span></span></li>
<li><span data-ttu-id="f3cf1-247">Implementa un'interfaccia <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a> per creare un elenco di blocchi di metadati da scrivere nel flusso di dati del frame.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-247">Implements an <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a> interface to build up a list of metadata blocks to write into the frame's data stream.</span></span></li>
<li><span data-ttu-id="f3cf1-248">Espone un writer di query per scrivere i metadati associati al frame, usando espressioni di query.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-248">Exposes a query writer to write the metadata associated with the frame, using query expressions.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="f3cf1-249">Nella tabella seguente vengono descritti i componenti dei metadati WIC.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-249">The following table describes the WIC metadata components.</span></span> <span data-ttu-id="f3cf1-250">Questi componenti consentono di leggere e scrivere i metadati in un'immagine esposta dai componenti elencati nella tabella precedente.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-250">These components enable you to read and write the metadata in an image exposed by the components listed in the previous table.</span></span> 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f3cf1-251">Componente</span><span class="sxs-lookup"><span data-stu-id="f3cf1-251">Component</span></span></th>
<th><span data-ttu-id="f3cf1-252">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f3cf1-252">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f3cf1-253">Lettore di query dei metadati (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader"><strong>IWICMetadataQueryReader</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="f3cf1-253">Metadata Query Reader (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader"><strong>IWICMetadataQueryReader</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="f3cf1-254">Accetta una stringa di query e sposta la gerarchia dei metadati sottostante per ottenere i metadati.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-254">Takes a query string and navigates the underlying metadata hierarchy to get metadata.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3cf1-255">Writer di query dei metadati (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter"><strong>IWICMetadataQueryWriter</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="f3cf1-255">Metadata Query Writer (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter"><strong>IWICMetadataQueryWriter</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="f3cf1-256">Accetta una stringa di query e sposta la gerarchia dei metadati sottostante per ottenere, impostare e rimuovere i metadati.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-256">Takes a query string and navigates the underlying metadata hierarchy to get, set, and remove metadata.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f3cf1-257">Lettore di blocchi di metadati (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="f3cf1-257">Metadata Block Reader (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="f3cf1-258">Gestisce una raccolta di sola lettura di oggetti <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader"><strong>IWICMetadataReader</strong></a> all'inizio della gerarchia dei metadati e Abilita l'enumerazione di tutti i blocchi di metadati.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-258">Manages a read-only collection of <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader"><strong>IWICMetadataReader</strong></a> objects at the top of the metadata hierarchy and enables enumeration of all metadata blocks.</span></span></li>
<li><span data-ttu-id="f3cf1-259">Implementata da un decodificatore bitmap e da un frame bitmap decodificato.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-259">Implemented by a bitmap decoder and a decoded bitmap frame.</span></span></li>
<li><span data-ttu-id="f3cf1-260">Implementato da sviluppatori di componenti di terze parti per codec personalizzati.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-260">Implemented by third-party component developers for custom codecs.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3cf1-261">Writer del blocco di metadati (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="f3cf1-261">Metadata Block Writer (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="f3cf1-262">Gestisce una raccolta di lettura e scrittura di oggetti <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter"><strong>IWICMetadataWriter</strong></a> all'inizio della gerarchia dei metadati.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-262">Manages a read and write collection of <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter"><strong>IWICMetadataWriter</strong></a> objects at the top of the metadata hierarchy.</span></span></li>
<li><span data-ttu-id="f3cf1-263">Implementata da un codificatore bitmap e da una codifica di frame bitmap.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-263">Implemented by a bitmap encoder and a bitmap frame encode.</span></span></li>
<li><span data-ttu-id="f3cf1-264">Implementato da sviluppatori di componenti di terze parti per codec personalizzati.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-264">Implemented by third-party component developers for custom codecs.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f3cf1-265">Lettore di metadati (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader"><strong>IWICMetadataReader</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="f3cf1-265">Metadata Reader (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader"><strong>IWICMetadataReader</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="f3cf1-266">Analizza un flusso di metadati e gestisce una raccolta di sola lettura degli elementi di metadati.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-266">Parses a stream of metadata and manages a read-only collection of the metadata items.</span></span> <span data-ttu-id="f3cf1-267">Associato a un formato di metadati, ad esempio EXIF, IFD e XMP.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-267">Associated with a metadata format such as EXIF, IFD, and XMP.</span></span></li>
<li><span data-ttu-id="f3cf1-268">Funge da dizionario, restituendo un valore quando viene fornita una coppia di formato e ID.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-268">Acts as a dictionary, returning a value when given a format and ID pair.</span></span></li>
<li><span data-ttu-id="f3cf1-269">Implementato da sviluppatori di componenti di terze parti per i tipi di metadati personalizzati.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-269">Implemented by third-party component developers for custom metadata types.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f3cf1-270">Writer di metadati (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter"><strong>IWICMetadataWriter</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="f3cf1-270">Metadata Writer (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter"><strong>IWICMetadataWriter</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="f3cf1-271">Analizza e serializza un flusso di metadati e gestisce una raccolta di lettura/scrittura di elementi di metadati.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-271">Parses and serializes a stream of metadata and manages a read/write collection of metadata items.</span></span></li>
<li><span data-ttu-id="f3cf1-272">Implementato da sviluppatori di componenti di terze parti per i tipi di metadati personalizzati.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-272">Implemented by third-party component developers for custom metadata types.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f3cf1-273">Fast Metadata encoder<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder"><strong>IWICFastMetadataEncoder</strong></a></span><span class="sxs-lookup"><span data-stu-id="f3cf1-273">Fast Metadata Encoder<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder"><strong>IWICFastMetadataEncoder</strong></a></span></span></td>
<td><ul>
<li><span data-ttu-id="f3cf1-274">Espone la semantica per la scrittura in una gerarchia di metadati che aggiornerà i metadati senza ricodificare l'immagine.</span><span class="sxs-lookup"><span data-stu-id="f3cf1-274">Exposes semantics for writing on a metadata hierarchy that will update metadata in place without re-encoding the image.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="f3cf1-275">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f3cf1-275">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="f3cf1-276">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="f3cf1-276">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f3cf1-277">Panoramica del componente imaging Windows</span><span class="sxs-lookup"><span data-stu-id="f3cf1-277">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="f3cf1-278">Cenni preliminari sul linguaggio di query dei metadati</span><span class="sxs-lookup"><span data-stu-id="f3cf1-278">Metadata Query Language Overview</span></span>](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[<span data-ttu-id="f3cf1-279">Panoramica della lettura e della scrittura dei metadati delle immagini</span><span class="sxs-lookup"><span data-stu-id="f3cf1-279">Overview of Reading and Writing Image Metadata</span></span>](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[<span data-ttu-id="f3cf1-280">Panoramica dell'estendibilità dei metadati</span><span class="sxs-lookup"><span data-stu-id="f3cf1-280">Metadata Extensibility Overview</span></span>](-wic-codec-metadatahandlers.md)
</dt> <dt>

[<span data-ttu-id="f3cf1-281">Procedura: ricodificare un'immagine JPEG con i metadati</span><span class="sxs-lookup"><span data-stu-id="f3cf1-281">How-to: Re-encode a JPEG Image with Metadata</span></span>](-wic-codec-jpegmetadataencoding.md)
</dt> </dl>

 

 



