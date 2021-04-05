---
description: In questo argomento viene fornita una panoramica di come è possibile utilizzare le API di Windows Imaging Component (WIC) per la lettura e la scrittura di metadati incorporati nei file di immagine.
ms.assetid: b1e0b936-a13a-42dd-8470-957ba1d90423
title: Panoramica della lettura e della scrittura dei metadati delle immagini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 484d562b71184c20adf054f1de2a4203878da9b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967695"
---
# <a name="overview-of-reading-and-writing-image-metadata"></a><span data-ttu-id="25e56-103">Panoramica della lettura e della scrittura dei metadati delle immagini</span><span class="sxs-lookup"><span data-stu-id="25e56-103">Overview of Reading and Writing Image Metadata</span></span>

<span data-ttu-id="25e56-104">In questo argomento viene fornita una panoramica di come è possibile utilizzare le API di Windows Imaging Component (WIC) per la lettura e la scrittura di metadati incorporati nei file di immagine.</span><span class="sxs-lookup"><span data-stu-id="25e56-104">This topic provides an overview of how you can use the Windows Imaging Component (WIC) APIs to read and write metadata that is embedded in image files.</span></span>

<span data-ttu-id="25e56-105">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="25e56-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="25e56-106">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="25e56-106">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="25e56-107">Introduzione</span><span class="sxs-lookup"><span data-stu-id="25e56-107">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="25e56-108">Lettura di Metadadata tramite un lettore di query</span><span class="sxs-lookup"><span data-stu-id="25e56-108">Reading Metadadata Using a Query Reader</span></span>](#reading-metadadata-using-a-query-reader)
    -   [<span data-ttu-id="25e56-109">Recupero di un lettore di query</span><span class="sxs-lookup"><span data-stu-id="25e56-109">Obtaining a Query Reader</span></span>](#obtaining-a-query-reader)
    -   [<span data-ttu-id="25e56-110">Lettura dei metadati</span><span class="sxs-lookup"><span data-stu-id="25e56-110">Reading Metadata</span></span>](#reading-metadata)
    -   [<span data-ttu-id="25e56-111">Metodi di lettura query aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="25e56-111">Additional Query Reader Methods</span></span>](#additional-query-reader-methods)
-   [<span data-ttu-id="25e56-112">Scrittura di metadati tramite un writer di query</span><span class="sxs-lookup"><span data-stu-id="25e56-112">Writing Metadata Using a Query Writer</span></span>](#writing-metadata-using-a-query-writer)
    -   [<span data-ttu-id="25e56-113">Recupero di un writer di query</span><span class="sxs-lookup"><span data-stu-id="25e56-113">Obtaining a Query Writer</span></span>](#obtaining-a-query-writer)
    -   [<span data-ttu-id="25e56-114">Aggiunta di metadati</span><span class="sxs-lookup"><span data-stu-id="25e56-114">Adding Metadata</span></span>](#adding-metadata)
    -   [<span data-ttu-id="25e56-115">Rimozione di metadati</span><span class="sxs-lookup"><span data-stu-id="25e56-115">Removing Metadata</span></span>](#removing-metadata)
    -   [<span data-ttu-id="25e56-116">Copia dei metadati per la ricodifica</span><span class="sxs-lookup"><span data-stu-id="25e56-116">Copying Metadata for Re-encoding</span></span>](#copying-metadata-for-re-encoding)
-   [<span data-ttu-id="25e56-117">Codifica rapida dei metadati</span><span class="sxs-lookup"><span data-stu-id="25e56-117">Fast Metadata Encoding</span></span>](#fast-metadata-encoding)
    -   [<span data-ttu-id="25e56-118">Aggiunta di spaziatura interna ai blocchi di metadati</span><span class="sxs-lookup"><span data-stu-id="25e56-118">Adding Padding to Metadata Blocks</span></span>](#adding-padding-to-metadata-blocks)
    -   [<span data-ttu-id="25e56-119">Acquisizione di un codificatore di metadati rapido</span><span class="sxs-lookup"><span data-stu-id="25e56-119">Obtaining a Fast Metadata Encoder</span></span>](#obtaining-a-fast-metadata-encoder)
    -   [<span data-ttu-id="25e56-120">Uso del codificatore di metadati veloci</span><span class="sxs-lookup"><span data-stu-id="25e56-120">Using the Fast Metadata Encoder</span></span>](#using-the-fast-metadata-encoder)
-   [<span data-ttu-id="25e56-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="25e56-121">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="25e56-122">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="25e56-122">Prerequisites</span></span>

<span data-ttu-id="25e56-123">Per comprendere questo argomento, è necessario avere familiarità con il sistema di metadati WIC, come descritto in [Panoramica dei metadati di WIC](-wic-about-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="25e56-123">To understand this topic, you should be familiar with the WIC metadata system as described in the [WIC Metadata Overview](-wic-about-metadata.md).</span></span> <span data-ttu-id="25e56-124">È anche necessario conoscere il linguaggio di query usato per leggere e scrivere i metadati, come descritto in [Cenni preliminari sul linguaggio di query dei metadati](-wic-codec-metadataquerylanguage.md).</span><span class="sxs-lookup"><span data-stu-id="25e56-124">You should also be familiar with the query language used to read and write metadata, as described in [Metadata Query Language Overview](-wic-codec-metadataquerylanguage.md).</span></span>

## <a name="introduction"></a><span data-ttu-id="25e56-125">Introduzione</span><span class="sxs-lookup"><span data-stu-id="25e56-125">Introduction</span></span>

<span data-ttu-id="25e56-126">WIC fornisce agli sviluppatori di applicazioni i componenti Component Object Model (COM) per la lettura e la scrittura dei metadati incorporati nei file di immagine.</span><span class="sxs-lookup"><span data-stu-id="25e56-126">WIC provides application developers with Component Object Model (COM) components to read and write metadata embedded in image files.</span></span> <span data-ttu-id="25e56-127">Esistono due modi per leggere e scrivere i metadati:</span><span class="sxs-lookup"><span data-stu-id="25e56-127">There are two ways to read and write metadata:</span></span>

-   <span data-ttu-id="25e56-128">Utilizzo di una query Reader/Writer e di un'espressione di query per eseguire query sui blocchi di metadati per blocchi annidati o metadati specifici all'interno di un blocco.</span><span class="sxs-lookup"><span data-stu-id="25e56-128">Using a query reader/writer and a query expression to query metadata blocks for nested blocks or specific metadata within a block.</span></span>
-   <span data-ttu-id="25e56-129">Utilizzo di un gestore di metadati (un lettore di metadati o un writer di metadati) per accedere ai blocchi di metadati annidati o a metadati specifici all'interno dei blocchi di metadati.</span><span class="sxs-lookup"><span data-stu-id="25e56-129">Using a metadata handler (a metadata reader or a metadata writer) to access the nested metadata blocks or specific metadata within the metadata blocks.</span></span>

<span data-ttu-id="25e56-130">Il più semplice consiste nell'usare un reader/writer di query e un'espressione di query per accedere ai metadati.</span><span class="sxs-lookup"><span data-stu-id="25e56-130">The easiest of these is to use a query reader/writer and a query expression to access the metadata.</span></span> <span data-ttu-id="25e56-131">Un lettore di query ([**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)) viene utilizzato per leggere i metadati mentre per la scrittura dei metadati viene utilizzato un writer di query ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)).</span><span class="sxs-lookup"><span data-stu-id="25e56-131">A query reader ([**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)) is used to read metadata while a query writer ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)) is used to write metadata.</span></span> <span data-ttu-id="25e56-132">Entrambi usano un'espressione di query per leggere o scrivere i metadati desiderati.</span><span class="sxs-lookup"><span data-stu-id="25e56-132">Both of these use a query expression to read or write the desired metadata.</span></span> <span data-ttu-id="25e56-133">Dietro le quinte, un lettore di query (e un writer) usa un gestore di metadati per accedere ai metadati descritti dall'espressione di query.</span><span class="sxs-lookup"><span data-stu-id="25e56-133">Behind the scenes, a query reader (and writer) uses a metadata handler to access the metadata described by the query expression.</span></span>

<span data-ttu-id="25e56-134">Il metodo più avanzato consiste nell'accedere direttamente ai gestori di metadati.</span><span class="sxs-lookup"><span data-stu-id="25e56-134">The more advanced method is to directly access the metadata handlers.</span></span> <span data-ttu-id="25e56-135">Un gestore di metadati viene ottenuto dai singoli frame utilizzando un reader di blocco ([**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)) o un writer di blocco ([**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)).</span><span class="sxs-lookup"><span data-stu-id="25e56-135">A metadata handler is obtained from the individual frames using a block reader ([**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)) or a block writer ([**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)).</span></span> <span data-ttu-id="25e56-136">I due tipi di gestori di metadati disponibili sono il lettore di metadati ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) e il writer dei metadati ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)).</span><span class="sxs-lookup"><span data-stu-id="25e56-136">The two types of metadata handlers available are the metadata reader ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) and the metadata writer ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)).</span></span>

<span data-ttu-id="25e56-137">Il diagramma seguente del contenuto di un file di immagine JPEG viene usato in tutti gli esempi di questo argomento.</span><span class="sxs-lookup"><span data-stu-id="25e56-137">The following diagram of the contents of a JPEG image file is used throughout the examples in this topic.</span></span> <span data-ttu-id="25e56-138">L'immagine rappresentata dal diagramma è stata creata tramite Microsoft Paint; i metadati della classificazione sono stati aggiunti utilizzando la funzionalità raccolta foto di Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="25e56-138">The image represented by this diagram was created by using Microsoft Paint; the rating metadata was added by using the Photo Gallery feature of Windows Vista.</span></span>

![illustrazione dell'immagine JPEG con i metadati di classificazione](graphics/jpeg.png)

## <a name="reading-metadadata-using-a-query-reader"></a><span data-ttu-id="25e56-140">Lettura di Metadadata tramite un lettore di query</span><span class="sxs-lookup"><span data-stu-id="25e56-140">Reading Metadadata Using a Query Reader</span></span>

<span data-ttu-id="25e56-141">Il modo più semplice per leggere i metadati consiste nell'usare l'interfaccia di lettura query, [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader).</span><span class="sxs-lookup"><span data-stu-id="25e56-141">The easiest way to read metadata is to use the query reader interface, [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader).</span></span> <span data-ttu-id="25e56-142">Il lettore di query consente di leggere i blocchi di metadati e gli elementi all'interno di blocchi di metadati usando un'espressione di query.</span><span class="sxs-lookup"><span data-stu-id="25e56-142">The query reader enables you to read metadata blocks and items within metadata blocks using a query expression.</span></span>

<span data-ttu-id="25e56-143">È possibile ottenere un lettore di query in tre modi: tramite un decodificatore bitmap ([**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)), tramite i singoli frame ([**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)) o tramite un writer di query ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)).</span><span class="sxs-lookup"><span data-stu-id="25e56-143">There are three ways to obtain a query reader: through a bitmap decoder ([**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)), through its individual frames ([**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)), or through a query writer ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)).</span></span>

### <a name="obtaining-a-query-reader"></a><span data-ttu-id="25e56-144">Recupero di un lettore di query</span><span class="sxs-lookup"><span data-stu-id="25e56-144">Obtaining a Query Reader</span></span>

<span data-ttu-id="25e56-145">Il codice di esempio seguente illustra come ottenere un decodificatore bitmap dalla factory di imaging e come recuperare un singolo frame bitmap.</span><span class="sxs-lookup"><span data-stu-id="25e56-145">The following example code shows how to obtain a bitmap decoder from the imaging factory and retrieve an individual bitmap frame.</span></span> <span data-ttu-id="25e56-146">Questo codice esegue anche le operazioni di installazione necessarie per ottenere un lettore di query da un frame decodificato.</span><span class="sxs-lookup"><span data-stu-id="25e56-146">This code also performs setup work needed to obtain a query reader from a decoded frame.</span></span>


```
IWICImagingFactory *pFactory = NULL;
IWICBitmapDecoder *pDecoder = NULL;
IWICBitmapFrameDecode *pFrameDecode = NULL;
IWICMetadataQueryReader *pQueryReader = NULL;
IWICMetadataQueryReader *pEmbedReader = NULL;
PROPVARIANT value;

// Initialize COM
CoInitialize(NULL);

// Initialize PROPVARIANT
PropVariantInit(&value);

//Create the COM imaging factory
HRESULT hr = CoCreateInstance(
    CLSID_WICImagingFactory,
    NULL,
    CLSCTX_INPROC_SERVER,
    IID_IWICImagingFactory,
    (LPVOID*)&pFactory);

// Create the decoder
if (SUCCEEDED(hr))
{
    hr = pFactory->CreateDecoderFromFilename(
        L"test.jpg",
        NULL,
        GENERIC_READ,
        WICDecodeMetadataCacheOnDemand,
        &pDecoder);
}

// Get a single frame from the image
if (SUCCEEDED(hr))
{
    hr = pDecoder->GetFrame(
         0,  //JPEG has only one frame.
         &pFrameDecode); 
}
```



<span data-ttu-id="25e56-147">Il decodificatore bitmap per il file di test.jpg viene ottenuto usando il metodo **CreateDecoderFromFilename** della factory di imaging.</span><span class="sxs-lookup"><span data-stu-id="25e56-147">The bitmap decoder for the test.jpg file is obtained by using the **CreateDecoderFromFilename** method of the imaging factory.</span></span> <span data-ttu-id="25e56-148">In questo metodo, il quarto parametro è impostato sul valore WICDecodeMetadataCacheOnDemand dall'enumerazione [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) .</span><span class="sxs-lookup"><span data-stu-id="25e56-148">In this method, the fourth parameter is set to the value WICDecodeMetadataCacheOnDemand from the [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) enumeration.</span></span> <span data-ttu-id="25e56-149">Ciò indica al decodificatore di memorizzare nella cache i metadati quando sono necessari i metadati; ottenendo un lettore di query o il lettore di metadati sottostante.</span><span class="sxs-lookup"><span data-stu-id="25e56-149">This tells the decoder to cache the metadata when the metadata is needed; either by obtaining a query reader or the underlying metadata reader.</span></span> <span data-ttu-id="25e56-150">L'uso di questa opzione consente di mantenere il flusso ai metadati necessari per la codifica rapida dei metadati e consente la decodifica senza perdita di codice dell'immagine JPEG.</span><span class="sxs-lookup"><span data-stu-id="25e56-150">Using this option enables you to retain the stream to the metadata required for fast metadata encoding and enables lossless decoding of the JPEG image.</span></span> <span data-ttu-id="25e56-151">In alternativa, è possibile usare l'altro valore di **WICDecodeOptions** , WICDecodeMetadataCacheOnLoad, che memorizza nella cache i metadati dell'immagine incorporata non appena l'immagine viene caricata.</span><span class="sxs-lookup"><span data-stu-id="25e56-151">Alternatively, you could use the other **WICDecodeOptions** value, WICDecodeMetadataCacheOnLoad, which caches the embedded image metadata as soon as the image is loaded.</span></span>

<span data-ttu-id="25e56-152">Per ottenere il lettore di query del frame, effettuare una semplice chiamata al metodo **GetMetadataQueryReader** del frame.</span><span class="sxs-lookup"><span data-stu-id="25e56-152">To obtain the frame's query reader, make a simple call to the frame's **GetMetadataQueryReader** method.</span></span> <span data-ttu-id="25e56-153">Il codice seguente illustra questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="25e56-153">The following code demonstrates this call.</span></span>


```
// Get the query reader
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}
```



<span data-ttu-id="25e56-154">Analogamente, è possibile ottenere un lettore di query anche a livello di decodificatore.</span><span class="sxs-lookup"><span data-stu-id="25e56-154">Similarly, a query reader can also be obtained at the decoder level.</span></span> <span data-ttu-id="25e56-155">Una semplice chiamata al metodo **GetMetadataQueryReader** del decodificatore ottiene il lettore di query del decodificatore.</span><span class="sxs-lookup"><span data-stu-id="25e56-155">A simple call to the decoder's **GetMetadataQueryReader** method gets the decoder's query reader.</span></span> <span data-ttu-id="25e56-156">Il lettore di query di un decodificatore, a differenza del lettore di query di un frame, legge i metadati per un'immagine che si trova all'esterno dei singoli frame.</span><span class="sxs-lookup"><span data-stu-id="25e56-156">An decoder's query reader, unlike a frame's query reader, reads metadata for an image that is outside of the individual frames.</span></span> <span data-ttu-id="25e56-157">Tuttavia, questo scenario non è comune e i formati di immagini native non supportano questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="25e56-157">However, this scenario is not common, and the native image formats do not support this capability.</span></span> <span data-ttu-id="25e56-158">I CODEC di immagini native forniti da WIC leggono e scrivono i metadati a livello di frame anche per i formati a singolo frame, ad esempio JPEG.</span><span class="sxs-lookup"><span data-stu-id="25e56-158">The native image CODECS provided by WIC read and write metadata at the frame level even for single-frame formats such as JPEG.</span></span>

### <a name="reading-metadata"></a><span data-ttu-id="25e56-159">Lettura dei metadati</span><span class="sxs-lookup"><span data-stu-id="25e56-159">Reading Metadata</span></span>

<span data-ttu-id="25e56-160">Prima di passare alla lettura effettiva dei metadati, esaminare il diagramma seguente di un file JPEG che include blocchi di metadati incorporati e dati effettivi da recuperare.</span><span class="sxs-lookup"><span data-stu-id="25e56-160">Before you move on to actually reading metadata, look at the following diagram of a JPEG file that includes embedded metadata blocks and actual data to retrieve.</span></span> <span data-ttu-id="25e56-161">Questo diagramma fornisce callout a blocchi di metadati e elementi specifici all'interno dell'immagine fornendo l'espressione di query dei metadati a ogni blocco o elemento.</span><span class="sxs-lookup"><span data-stu-id="25e56-161">This diagram provides callouts to specific metadata blocks and items within the image providing the metadata query expression to each block or item.</span></span>

![illustrazione dell'immagine JPEG con callout di metadati](graphics/jpegwithcallouts.png)

<span data-ttu-id="25e56-163">Per eseguire una query per i blocchi di metadati incorporati o per elementi specifici in base al nome, chiamare il metodo **GetMetadataByName** .</span><span class="sxs-lookup"><span data-stu-id="25e56-163">To query for embedded metadata blocks or specific items by name, call the **GetMetadataByName** method.</span></span> <span data-ttu-id="25e56-164">Questo metodo accetta un'espressione di query e un [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) in cui viene restituito l'elemento dei metadati.</span><span class="sxs-lookup"><span data-stu-id="25e56-164">This method takes a query expression and a [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) in which the metadata item is returned.</span></span> <span data-ttu-id="25e56-165">Il codice seguente esegue una query per un blocco di metadati annidato e converte il componente [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) fornito dal valore PROPVARIANT in un lettore di query, se trovato.</span><span class="sxs-lookup"><span data-stu-id="25e56-165">The following code queries for a nested metadata block and converts the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) component provided by the PROPVARIANT value to a query reader if found.</span></span>


```
if (SUCCEEDED(hr))
{
    // Get the nested IFD reader
    hr = pQueryReader->GetMetadataByName(L"/app1/ifd", &value);
    if (value.vt == VT_UNKNOWN)
    {
        hr = value.punkVal->QueryInterface(IID_IWICMetadataQueryReader, (void **)&pEmbedReader);
    }
    PropVariantClear(&value); // Clear value for new query
}
```



<span data-ttu-id="25e56-166">L'espressione di query "/app1/IFD" sta eseguendo una query per il blocco IFD annidato nel blocco App1.</span><span class="sxs-lookup"><span data-stu-id="25e56-166">The query expression "/app1/ifd" is querying for the IFD block nested in the App1 block.</span></span> <span data-ttu-id="25e56-167">Il file di immagine JPEG contiene il blocco di metadati annidati IFD, in modo che [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) venga restituito con un tipo di variabile (VT) `VT_UNKNOWN` e un puntatore a un'interfaccia [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) (punkVal).</span><span class="sxs-lookup"><span data-stu-id="25e56-167">The JPEG image file contains the IFD nested metadata block, so the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) is returned with a variable type (vt) of `VT_UNKNOWN` and a pointer to an [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface (punkVal).</span></span> <span data-ttu-id="25e56-168">Viene quindi eseguita una query sull'interfaccia IUnknown per un lettore di query.</span><span class="sxs-lookup"><span data-stu-id="25e56-168">You then query the IUnknown interface for a query reader.</span></span>

<span data-ttu-id="25e56-169">Nel codice seguente viene illustrata una nuova query basata sul nuovo Reader di query relativo al blocco IFD annidato.</span><span class="sxs-lookup"><span data-stu-id="25e56-169">The following code demonstrates a new query based on the new query reader relative to the nested IFD block.</span></span>


```
if (SUCCEEDED(hr))
{
    hr = pEmbedReader->GetMetadataByName(L"/{ushort=18249}", &value);
    PropVariantClear(&value); // Clear value for new query
}
```



<span data-ttu-id="25e56-170">L'espressione di query "/{ushort = 18249}" esegue una query sul blocco IFD per la classificazione MicrosoftPhoto incorporata nel tag 18249.</span><span class="sxs-lookup"><span data-stu-id="25e56-170">The query expression "/{ushort=18249}" queries the IFD block for the MicrosoftPhoto rating embedded under tag 18249.</span></span> <span data-ttu-id="25e56-171">Il valore [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) conterrà ora un tipo di valore `VT_UI2` e un valore di dati di 50.</span><span class="sxs-lookup"><span data-stu-id="25e56-171">The [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) value will now contain a value type of `VT_UI2` and a data value of 50.</span></span>

<span data-ttu-id="25e56-172">Tuttavia, non è necessario ottenere un blocco annidato prima di eseguire query per valori di dati specifici.</span><span class="sxs-lookup"><span data-stu-id="25e56-172">However, it is not necessary to obtain a nested block before querying for specific data values.</span></span> <span data-ttu-id="25e56-173">Ad esempio, anziché eseguire una query per il IFD annidato e quindi per la classificazione MicrosoftPhoto, è possibile usare invece il blocco di metadati radice e la query illustrata nel codice seguente per ottenere le stesse informazioni.</span><span class="sxs-lookup"><span data-stu-id="25e56-173">For instance, instead of querying for the nested IFD and then for the MicrosoftPhoto rating, you can instead use the root metadata block and the query shown in the following code to obtain the same information.</span></span>


```
if (SUCCEEDED(hr))
{
    hr = pQueryReader->GetMetadataByName(L"/app1/ifd/{ushort=18249}", &value);
    PropVariantClear(&value);
}
```



<span data-ttu-id="25e56-174">Oltre a eseguire query per elementi di metadati specifici in un blocco di metadati, è anche possibile enumerare tutti gli elementi di metadati in un blocco di metadati (esclusi gli elementi di metadati nei blocchi di metadati annidati).</span><span class="sxs-lookup"><span data-stu-id="25e56-174">In addition to querying for specific metadata items in a metadata block, you can also enumerate all the metadata items in a metadata block (not including metadata items in nested metadata blocks).</span></span> <span data-ttu-id="25e56-175">Per enumerare gli elementi di metadati nel blocco corrente, viene usato il metodo **GetEnumeration** del Visualizzatore di query.</span><span class="sxs-lookup"><span data-stu-id="25e56-175">To enumerate the metadata items in the current block, the query reader's **GetEnumeration** method is used.</span></span> <span data-ttu-id="25e56-176">Questo metodo ottiene un'interfaccia **IEnumString** popolata con gli elementi di metadati nel blocco corrente.</span><span class="sxs-lookup"><span data-stu-id="25e56-176">This method obtains an **IEnumString** interface populated with the metadata items in the current block.</span></span> <span data-ttu-id="25e56-177">Il codice seguente, ad esempio, enumera la classificazione XMP e la classificazione MicrosoftPhoto per il blocco IFD annidato ottenuto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="25e56-177">For example, the following code enumerates the XMP rating and MicrosoftPhoto rating for the nested IFD block that was obtained earlier.</span></span>


```
IEnumString *metadataItems = NULL;

if (SUCCEEDED(hr))
{
    hr = pEmbedReader->GetEnumerator(&metadataItems);
}
```



<span data-ttu-id="25e56-178">Per altre informazioni sull'identificazione dei tag appropriati per diversi formati di immagine e formati di metadati, vedere [query di metadati del formato di immagine nativo](-wic-native-image-format-metadata-queries.md).</span><span class="sxs-lookup"><span data-stu-id="25e56-178">For more information on identifying appropriate tags for various image formats and metadata formats, see [Native Image Format Metadata Queries](-wic-native-image-format-metadata-queries.md).</span></span>

### <a name="additional-query-reader-methods"></a><span data-ttu-id="25e56-179">Metodi di lettura query aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="25e56-179">Additional Query Reader Methods</span></span>

<span data-ttu-id="25e56-180">Oltre a leggere i metadati, è anche possibile ottenere informazioni aggiuntive sull'Reader di query e ottenere i metadati tramite altri metodi.</span><span class="sxs-lookup"><span data-stu-id="25e56-180">In addition to reading metadata, you can also obtain additional information about the query reader and obtain metadata through other means.</span></span> <span data-ttu-id="25e56-181">In query Reader sono disponibili due metodi che forniscono informazioni su query Reader, **GetContainerFormat** e **getLocation**.</span><span class="sxs-lookup"><span data-stu-id="25e56-181">The query reader provides two methods that provide information about the query reader, **GetContainerFormat** and **GetLocation**.</span></span>

<span data-ttu-id="25e56-182">Con il lettore di query incorporato è possibile utilizzare **GetContainerFormat** per determinare il tipo di blocco di metadati ed è possibile chiamare **getLocation** per ottenere il percorso relativo al blocco di metadati radice.</span><span class="sxs-lookup"><span data-stu-id="25e56-182">With the embedded query reader, you can use **GetContainerFormat** to determine the type of metadata block, and you can call **GetLocation** to obtain the path relative to the root metadata block.</span></span> <span data-ttu-id="25e56-183">Nel codice seguente viene eseguita una query sul lettore di query incorporato per la relativa posizione.</span><span class="sxs-lookup"><span data-stu-id="25e56-183">The following code queries the embedded query reader for its location.</span></span>


```
// Determine the metadata block format

if (SUCCEEDED(hr))
{
    hr = pEmbedReader->GetContainerFormat(&containerGUID);
}

// Determine the query reader's location
if (SUCCEEDED(hr))
{
    UINT length;
    WCHAR readerNamespace[100];
    hr = pEmbedReader->GetLocation(100, readerNamespace, &length);
}
```



<span data-ttu-id="25e56-184">La chiamata a **GetContainerFormat** per il lettore di query incorporato restituisce il GUID del formato dei metadati IFD.</span><span class="sxs-lookup"><span data-stu-id="25e56-184">The call to **GetContainerFormat** for the embedded query reader returns the IFD metadata format GUID.</span></span> <span data-ttu-id="25e56-185">La chiamata a **getLocation** restituisce uno spazio dei nomi "/app1/IFD"; fornisce il percorso relativo da cui verranno eseguite le successive query al nuovo Reader di query.</span><span class="sxs-lookup"><span data-stu-id="25e56-185">The call to **GetLocation** returns a namespace of "/app1/ifd"; providing you with the relative path from which subsequent queries to the new query reader will be executed.</span></span> <span data-ttu-id="25e56-186">Naturalmente, il codice precedente non è molto utile, ma illustra come usare il metodo **getLocation** per trovare i blocchi di metadati annidati.</span><span class="sxs-lookup"><span data-stu-id="25e56-186">Of course, the preceding code isn't very useful, but it does demonstrate how to use the **GetLocation** method for finding nested metadata blocks.</span></span>

## <a name="writing-metadata-using-a-query-writer"></a><span data-ttu-id="25e56-187">Scrittura di metadati tramite un writer di query</span><span class="sxs-lookup"><span data-stu-id="25e56-187">Writing Metadata Using a Query Writer</span></span>

> [!Note]  
> <span data-ttu-id="25e56-188">Alcuni esempi di codice forniti in questa sezione non vengono visualizzati nel contesto dei passaggi effettivi necessari per la scrittura dei metadati.</span><span class="sxs-lookup"><span data-stu-id="25e56-188">Some of the code examples provided in this section are not shown in the context of the actual steps required to write metadata.</span></span> <span data-ttu-id="25e56-189">Per visualizzare gli esempi di codice nel contesto di un esempio funzionante, vedere l'esercitazione Procedura: ricodificare un'immagine con metadati.</span><span class="sxs-lookup"><span data-stu-id="25e56-189">To view the code examples in the context of a working sample, see the How-to: Re-encode an Image with Metadata tutorial.</span></span>

 

<span data-ttu-id="25e56-190">Il componente principale per la scrittura dei metadati è il writer di query ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)).</span><span class="sxs-lookup"><span data-stu-id="25e56-190">The main component for writing metadata is the query writer ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)).</span></span> <span data-ttu-id="25e56-191">Il writer di query consente di impostare e rimuovere i blocchi di metadati e gli elementi all'interno di un blocco di metadati.</span><span class="sxs-lookup"><span data-stu-id="25e56-191">The query writer enables you to set and remove metadata blocks and items within a metadata block.</span></span>

<span data-ttu-id="25e56-192">Come il lettore di query, è possibile ottenere un writer di query in tre modi: tramite un codificatore di bitmap ([**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)), tramite i singoli frame ([**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)) o tramite un codificatore di metadati rapido ([**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)).</span><span class="sxs-lookup"><span data-stu-id="25e56-192">Like the query reader, there are three ways to obtain a query writer: through a bitmap encoder ([**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)), through its individual frames ([**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)), or through a fast metadata encoder ([**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)).</span></span>

### <a name="obtaining-a-query-writer"></a><span data-ttu-id="25e56-193">Recupero di un writer di query</span><span class="sxs-lookup"><span data-stu-id="25e56-193">Obtaining a Query Writer</span></span>

<span data-ttu-id="25e56-194">Il writer di query più comune è per un singolo frame di una bitmap.</span><span class="sxs-lookup"><span data-stu-id="25e56-194">The most common query writer is for an individual frame of a bitmap.</span></span> <span data-ttu-id="25e56-195">Questo writer di query imposta e rimuove i blocchi di metadati e gli elementi di un frame di immagini.</span><span class="sxs-lookup"><span data-stu-id="25e56-195">This query writer sets and removes an image frame's metadata blocks and items.</span></span> <span data-ttu-id="25e56-196">Per ottenere un writer di query del fotogramma immagine, chiamare il metodo **GetMetadataQueryWriter** del frame.</span><span class="sxs-lookup"><span data-stu-id="25e56-196">To obtain an image frame's query writer, call the frame's **GetMetadataQueryWriter** method.</span></span> <span data-ttu-id="25e56-197">Il codice seguente illustra la chiamata al metodo semplice per ottenere il writer di query di un frame.</span><span class="sxs-lookup"><span data-stu-id="25e56-197">The following code demonstrates the simple method call to obtain a frame's query writer.</span></span>


```
IWICMetadataQueryWriter &pFrameQWriter = NULL;

//Obtain a query writer from the frame.
hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
```



<span data-ttu-id="25e56-198">Analogamente, è possibile ottenere un writer di query anche per il livello del codificatore.</span><span class="sxs-lookup"><span data-stu-id="25e56-198">Similarly, a query writer can also be obtained for the encoder level.</span></span> <span data-ttu-id="25e56-199">Una semplice chiamata al metodo **GetMetadataQueryWriter** del codificatore ottiene il writer di query del codificatore.</span><span class="sxs-lookup"><span data-stu-id="25e56-199">A simple call to the encoder's **GetMetadataQueryWriter** method gets the encoder's query writer.</span></span> <span data-ttu-id="25e56-200">Un writer di query del codificatore, a differenza del writer di query di un frame, scrive i metadati per un'immagine all'esterno del singolo frame.</span><span class="sxs-lookup"><span data-stu-id="25e56-200">An encoder's query writer, unlike a frame's query writer, writes metadata for an image outside of the individual frame.</span></span> <span data-ttu-id="25e56-201">Tuttavia, questo scenario non è comune e i formati di immagini native non supportano questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="25e56-201">However, this scenario is not common, and the native image formats do not support this capability.</span></span> <span data-ttu-id="25e56-202">I codec di immagini native forniti da WIC leggono e scrivono i metadati a livello di frame anche per i formati a singolo frame, ad esempio JPEG.</span><span class="sxs-lookup"><span data-stu-id="25e56-202">The native image codecs provided by WIC read and write metadata at the frame level even for single-frame formats such as JPEG.</span></span>

<span data-ttu-id="25e56-203">È anche possibile ottenere un writer di query direttamente dalla factory di imaging ([**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)).</span><span class="sxs-lookup"><span data-stu-id="25e56-203">You can also obtain a query writer directly from the imaging factory ([**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)).</span></span> <span data-ttu-id="25e56-204">Esistono due metodi di creazione di immagini che restituiscono un writer di query: **CreateQueryWriter** e **CreateQueryWriterFromReader**.</span><span class="sxs-lookup"><span data-stu-id="25e56-204">There are two imaging factory methods that return a query writer: **CreateQueryWriter** and **CreateQueryWriterFromReader**.</span></span>

<span data-ttu-id="25e56-205">**CreateQueryWriter** crea un writer di query per il formato di metadati e il fornitore specificati.</span><span class="sxs-lookup"><span data-stu-id="25e56-205">**CreateQueryWriter** creates a query writer for the specified metadata format and vendor.</span></span> <span data-ttu-id="25e56-206">Questo writer di query consente di scrivere metadati per un formato di metadati specifico e di aggiungerli all'immagine.</span><span class="sxs-lookup"><span data-stu-id="25e56-206">This query writer enables you to write metadata for a specific metadata format and add it to the image.</span></span> <span data-ttu-id="25e56-207">Il codice seguente illustra una chiamata **CreateQueryWriter** per creare un writer di query XMP.</span><span class="sxs-lookup"><span data-stu-id="25e56-207">The following code demonstrates a **CreateQueryWriter** call to create an XMP query writer.</span></span>


```
IWICMetadataQueryWriter *pXMPWriter = NULL;

// Create XMP block
GUID vendor = GUID_VendorMicrosoft;
hr = pFactory->CreateQueryWriter(
        GUID_MetadataFormatXMP,
        &vendor,
        &pXMPWriter);
```



<span data-ttu-id="25e56-208">In questo esempio, il nome descrittivo `GUID_MetadataFormatXMP` viene usato come parametro *guidMetadataFormat* .</span><span class="sxs-lookup"><span data-stu-id="25e56-208">In this example, the friendly name `GUID_MetadataFormatXMP` is used as the *guidMetadataFormat* parameter.</span></span> <span data-ttu-id="25e56-209">Rappresenta il GUID del formato dei metadati XMP e il fornitore rappresenta il gestore creato da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="25e56-209">It represents the XMP metadata format GUID, and vendor represents the Microsoft created handler.</span></span> <span data-ttu-id="25e56-210">In alternativa, è possibile passare **null** come parametro *pguidVendor* con gli stessi risultati se non esiste alcun altro gestore XMP.</span><span class="sxs-lookup"><span data-stu-id="25e56-210">Alternatively, **NULL** can be passed as the *pguidVendor* parameter with the same results if no other XMP handler exists.</span></span> <span data-ttu-id="25e56-211">Se insieme al gestore XMP nativo viene installato un gestore XMP personalizzato, il passaggio di un **valore null** per il fornitore comporterà la restituzione del GUID più basso.</span><span class="sxs-lookup"><span data-stu-id="25e56-211">If a custom XMP handler is installed alongside the native XMP handler, passing **NULL** for the vendor will result in the query writer with the lowest GUID being returned.</span></span>

<span data-ttu-id="25e56-212">**CreateQueryWriterFromReader** è simile al metodo **CreateQueryWriter** con la differenza che il nuovo writer di query viene prepopolato con i dati forniti dal lettore di query.</span><span class="sxs-lookup"><span data-stu-id="25e56-212">**CreateQueryWriterFromReader** is similar to the **CreateQueryWriter** method except that it prepopulates the new query writer with the data provided by the query reader.</span></span> <span data-ttu-id="25e56-213">Questa operazione è utile per ricodificare un'immagine mantenendo i metadati esistenti o per rimuovere i metadati indesiderati.</span><span class="sxs-lookup"><span data-stu-id="25e56-213">This is useful for re-encoding an image while maintaining the existing metadata, or for removing unwanted metadata.</span></span> <span data-ttu-id="25e56-214">Il codice seguente illustra una chiamata **CreateQueryWriterFromReader** .</span><span class="sxs-lookup"><span data-stu-id="25e56-214">The following code demonstrates a **CreateQueryWriterFromReader** call.</span></span>


```
hr = pFrameDecode->GetMetadataQueryReader(&pFrameQReader);

// Copy metadata using query readers
if(SUCCEEDED(hr) && pFrameQReader)
{
    IWICMetadataQueryWriter *pNewWriter = NULL;

    GUID vendor = GUID_VendorMicrosoft;
    hr = pFactory->CreateQueryWriterFromReader(
        pFrameQReader,
        &vendor,
        &pNewWriter);
```



### <a name="adding-metadata"></a><span data-ttu-id="25e56-215">Aggiunta di metadati</span><span class="sxs-lookup"><span data-stu-id="25e56-215">Adding Metadata</span></span>

<span data-ttu-id="25e56-216">Dopo aver ottenuto un writer di query, è possibile usarlo per aggiungere blocchi ed elementi di metadati.</span><span class="sxs-lookup"><span data-stu-id="25e56-216">After you obtain a query writer, you can use it to add metadata blocks and items.</span></span> <span data-ttu-id="25e56-217">Per scrivere i metadati, utilizzare il metodo **SetMetadataByName** del writer di query.</span><span class="sxs-lookup"><span data-stu-id="25e56-217">To write metadata, you use the query writer's **SetMetadataByName** method.</span></span> <span data-ttu-id="25e56-218">**SetMetadataByName** accetta due parametri: un'espressione di query (*wzName*) e un puntatore a un [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) (*pvarValue*).</span><span class="sxs-lookup"><span data-stu-id="25e56-218">**SetMetadataByName** takes two parameters: a query expression (*wzName*) and a pointer to a [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) (*pvarValue*).</span></span> <span data-ttu-id="25e56-219">L'espressione di query definisce il blocco o l'elemento da impostare mentre PROPVARIANT fornisce il valore di dati effettivo da impostare.</span><span class="sxs-lookup"><span data-stu-id="25e56-219">The query expression defines the block or item to set while the PROPVARIANT provides the actual data value to set.</span></span>

<span data-ttu-id="25e56-220">Nell'esempio seguente viene illustrato come aggiungere un titolo utilizzando il writer di query XMP ottenuto in precedenza tramite il metodo **CreateQueryWriter** .</span><span class="sxs-lookup"><span data-stu-id="25e56-220">The following example demonstrates how to add a title by using the XMP query writer previously obtained by using the **CreateQueryWriter** method.</span></span>


```
// Write metadata to the XMP writer
if (SUCCEEDED(hr))
{
    PROPVARIANT value;
    PropVariantInit(&value);

    value.vt = VT_LPWSTR;
    value.pwszVal = L"Metadata Test Image.";
   
    hr = pXMPWriter->SetMetadataByName(L"/dc:title", &value);

    PropVariantClear(&value);
}
```



<span data-ttu-id="25e56-221">In questo esempio, il tipo del valore (VT) viene impostato su `VT_LPWSTR` , a indicare che verrà utilizzata una stringa come valore di dati.</span><span class="sxs-lookup"><span data-stu-id="25e56-221">In this example, value's type (vt) is set to `VT_LPWSTR`, indicating that a string will be used as the data value.</span></span> <span data-ttu-id="25e56-222">Poiché il tipo del *valore* è una stringa, *pwszVal* viene usato per impostare il titolo da usare.</span><span class="sxs-lookup"><span data-stu-id="25e56-222">Because *value*'s type is a string, *pwszVal* is used to set the title to use.</span></span> <span data-ttu-id="25e56-223">**SetMetadataByName** viene quindi chiamato usando l'espressione di query "/DC: title" e il nuovo set [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).</span><span class="sxs-lookup"><span data-stu-id="25e56-223">**SetMetadataByName** is then called using the query expression "/dc:title" and the newly set [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).</span></span> <span data-ttu-id="25e56-224">L'espressione di query utilizzata indica che è necessario impostare la proprietà title nello schema della fotocamera digitale (DC).</span><span class="sxs-lookup"><span data-stu-id="25e56-224">The query expression used indicates that the title property in the digital camera (dc) schema should be set.</span></span> <span data-ttu-id="25e56-225">Si noti che l'espressione non è "/XMP/DC: title"; Questo perché il writer di query è già specifico di XMP e non contiene un blocco XMP incorporato, che verrà suggerito da "/XMP/DC: title".</span><span class="sxs-lookup"><span data-stu-id="25e56-225">Note that the expression is not "/xmp/dc:title"; this is because the query writer is already specific to XMP and does not contain an embedded XMP block, which "/xmp/dc:title" would suggest.</span></span>

<span data-ttu-id="25e56-226">Fino a questo punto non sono stati effettivamente aggiunti metadati a un frame di immagine.</span><span class="sxs-lookup"><span data-stu-id="25e56-226">Up to this point you haven't actually added any metadata to an image frame.</span></span> <span data-ttu-id="25e56-227">È stato semplicemente popolato un writer di query con i dati.</span><span class="sxs-lookup"><span data-stu-id="25e56-227">You've simply populated a query writer with data.</span></span> <span data-ttu-id="25e56-228">Per aggiungere a un frame un blocco di metadati rappresentato dal writer di query, è necessario chiamare di nuovo **SetMetadataByName** usando il writer di query come valore di [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).</span><span class="sxs-lookup"><span data-stu-id="25e56-228">To add to a frame a metadata block represented by the query writer, you again call **SetMetadataByName** using the query writer as the value of the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).</span></span> <span data-ttu-id="25e56-229">In questo modo i metadati del writer di query vengono copiati nel frame dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="25e56-229">This effectively copies the metadata in the query writer to the image frame.</span></span> <span data-ttu-id="25e56-230">Il codice seguente illustra come aggiungere i metadati nel writer di query XMP precedentemente ottenuto al blocco di metadati radice di un frame.</span><span class="sxs-lookup"><span data-stu-id="25e56-230">The following code demonstrates how to add the metadata in the XMP query writer previously obtained to a frame's root metadata block.</span></span>


```
// Get the frame's query writer and write the XMP query writer to it
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);

    // Copy the metadata in the XMP query writer to the frame
    if (SUCCEEDED(hr))
    {
        PROPVARIANT value;

        PropVariantInit(&value);
        value.vt = VT_UNKNOWN;
        value.punkVal = pXMPWriter;
        value.punkVal->AddRef();

        hr = pFrameQWriter->SetMetadataByName(L"/", &value);

        PropVariantClear(&value);
    }
}
```



<span data-ttu-id="25e56-231">In questo esempio viene usato un tipo di valore (VT), `VT_UNKOWN` che indica un tipo di valore dell'interfaccia com.</span><span class="sxs-lookup"><span data-stu-id="25e56-231">In this example, a value type (vt) of `VT_UNKOWN` is used; indicating a COM interface value type.</span></span> <span data-ttu-id="25e56-232">Il writer di query XMP (piXMPWriter) viene quindi usato come valore di [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant), aggiungendovi un riferimento usando il metodo AddRef.</span><span class="sxs-lookup"><span data-stu-id="25e56-232">The XMP query writer (piXMPWriter) is then used as the value of the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant), adding a reference to it by using the AddRef method.</span></span> <span data-ttu-id="25e56-233">Infine, il writer di query XMP viene impostato chiamando il metodo **SetMetadataByName** del frame e passando l'espressione di query "/", indicando il blocco radice e il PROPVARIANT appena impostato.</span><span class="sxs-lookup"><span data-stu-id="25e56-233">Finally, the XMP query writer is set by calling the frame's **SetMetadataByName** method and passing the query expression "/", indicating the root block, and the newly set PROPVARIANT.</span></span>

> [!Note]  
> <span data-ttu-id="25e56-234">Se il frame contiene già il blocco di metadati che si sta tentando di aggiungere, i metadati che si aggiungono verranno aggiunti e i metadati esistenti verranno sovrascritti.</span><span class="sxs-lookup"><span data-stu-id="25e56-234">If the frame already contains the metadata block you are trying to add, the metadata you are adding will be added and existing metadata overwritten.</span></span>

 

### <a name="removing-metadata"></a><span data-ttu-id="25e56-235">Rimozione di metadati</span><span class="sxs-lookup"><span data-stu-id="25e56-235">Removing Metadata</span></span>

<span data-ttu-id="25e56-236">Un writer di query consente inoltre di rimuovere i metadati chiamando il metodo **RemoveMetadataByName** .</span><span class="sxs-lookup"><span data-stu-id="25e56-236">A query writer also enables you to remove metadata by calling the **RemoveMetadataByName** method.</span></span> <span data-ttu-id="25e56-237">**RemoveMetadataByName** accetta un'espressione di query e rimuove il blocco o l'elemento di metadati, se esistente.</span><span class="sxs-lookup"><span data-stu-id="25e56-237">**RemoveMetadataByName** takes a query expression and removes the metadata block or item if it exists.</span></span> <span data-ttu-id="25e56-238">Il codice seguente illustra come rimuovere il titolo aggiunto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="25e56-238">The following code demonstrates how to remove the title that was previously added.</span></span>


```
if (SUCCEEDED(hr))
{
    hr = pFrameQWriter->RemoveMetadataByName(L"/xmp/dc:title");
}
```



<span data-ttu-id="25e56-239">Il codice seguente illustra come rimuovere l'intero blocco di metadati XMP.</span><span class="sxs-lookup"><span data-stu-id="25e56-239">The following code demonstrates how to remove the entire XMP metadata block.</span></span>


```
if (SUCCEEDED(hr))
{
    hr = pFrameQWriter->RemoveMetadataByName(L"/xmp");
}
```



### <a name="copying-metadata-for-re-encoding"></a><span data-ttu-id="25e56-240">Copia dei metadati per la ricodifica</span><span class="sxs-lookup"><span data-stu-id="25e56-240">Copying Metadata for Re-encoding</span></span>

> [!Note]  
> <span data-ttu-id="25e56-241">Il codice contenuto in questa sezione è valido solo se i formati di immagine di origine e di destinazione sono uguali.</span><span class="sxs-lookup"><span data-stu-id="25e56-241">The code in this section is valid only when the source and destination image formats are the same.</span></span> <span data-ttu-id="25e56-242">Non è possibile copiare tutti i metadati di un'immagine in un'unica operazione quando si esegue la codifica in un formato di immagine diverso.</span><span class="sxs-lookup"><span data-stu-id="25e56-242">You cannot copy all of an image's metadata in a single operation when encoding to a different image format.</span></span>

 

<span data-ttu-id="25e56-243">Per mantenere i metadati durante la ricodifica di un'immagine nello stesso formato di immagine, sono disponibili metodi per la copia di tutti i metadati in un'unica operazione.</span><span class="sxs-lookup"><span data-stu-id="25e56-243">To preserve metadata while re-encoding an image to the same image format, there are methods available for copying all the metadata in a single operation.</span></span> <span data-ttu-id="25e56-244">Ognuna di queste operazioni segue un modello simile. ogni imposta i metadati del frame decodificato direttamente nel nuovo frame da codificare.</span><span class="sxs-lookup"><span data-stu-id="25e56-244">Each of these operations follows a similar pattern; each sets the decoded frame's metadata directly into the new frame being encoded.</span></span>

<span data-ttu-id="25e56-245">Il metodo preferito per la copia dei metadati consiste nell'inizializzare il writer del blocco del nuovo frame con il lettore di blocco del frame decodificato.</span><span class="sxs-lookup"><span data-stu-id="25e56-245">The preferred method to copy metadata is to initialize the new frame's block writer with the decoded frame's block reader.</span></span> <span data-ttu-id="25e56-246">Il codice seguente illustra questo metodo.</span><span class="sxs-lookup"><span data-stu-id="25e56-246">The following code demonstrates this method.</span></span>


```
if (SUCCEEDED(hr) && formatsEqual)
{
    // Copy metadata using metadata block reader/writer
    if (SUCCEEDED(hr))
    {
        pFrameDecode->QueryInterface(
            IID_IWICMetadataBlockReader,
            (void**)&pBlockReader);
    }
    if (SUCCEEDED(hr))
    {
        pFrameEncode->QueryInterface(
            IID_IWICMetadataBlockWriter,
            (void**)&pBlockWriter);
    }
    if (SUCCEEDED(hr))
    {
        pBlockWriter->InitializeFromBlockReader(pBlockReader);
    }
}
```



<span data-ttu-id="25e56-247">In questo esempio, il Reader di blocco e il writer del blocco vengono ottenuti rispettivamente dal fotogramma di origine e dal frame di destinazione.</span><span class="sxs-lookup"><span data-stu-id="25e56-247">In this example, the block reader and the block writer are obtained from the source frame and destination frame, respectively.</span></span> <span data-ttu-id="25e56-248">Il writer di blocco viene quindi inizializzato dal lettore del blocco.</span><span class="sxs-lookup"><span data-stu-id="25e56-248">The block writer is then initialized from the block reader.</span></span> <span data-ttu-id="25e56-249">Viene così inizializzato il reader del blocco con i metadati precompilati del lettore di blocchi.</span><span class="sxs-lookup"><span data-stu-id="25e56-249">This initializes the block reader with the pre-populated metadata of the block reader.</span></span>

<span data-ttu-id="25e56-250">Un altro metodo per copiare i metadati consiste nel scrivere il blocco di metadati a cui fa riferimento il lettore di query utilizzando il writer di query del codificatore.</span><span class="sxs-lookup"><span data-stu-id="25e56-250">Another method to copy metadata is to write the metadata block referenced by the query reader using the encoder's query writer.</span></span> <span data-ttu-id="25e56-251">Il codice seguente illustra questo metodo.</span><span class="sxs-lookup"><span data-stu-id="25e56-251">The following code demonstrates this method.</span></span>


```
if (SUCCEEDED(hr) && formatsEqual)
{
    hr = pFrameDecode->GetMetadataQueryReader(&pFrameQReader);

    // Copy metadata using query readers
    if(SUCCEEDED(hr))
    {
        hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
        if (SUCCEEDED(hr))
        {
            PropVariantClear(&value);
            value.vt=VT_UNKNOWN;
            value.punkVal=pFrameQReader;
            value.punkVal->AddRef();
            hr = pFrameQWriter->SetMetadataByName(L"/", &value);
            PropVariantClear(&value);
        }
    }
}
```



<span data-ttu-id="25e56-252">In questo caso, un lettore di query viene ottenuto dal fotogramma decodificato e quindi usato come valore della proprietà di [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) con un tipo di valore impostato su VT \_ Unknown.</span><span class="sxs-lookup"><span data-stu-id="25e56-252">Here, a query reader is obtained from the decoded frame and then used as the property value of the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) with a value type set to VT\_UNKNOWN.</span></span> <span data-ttu-id="25e56-253">Viene ottenuto il writer di query per il codificatore e l'espressione di query "/" viene utilizzata per impostare i metadati nel percorso di navigazione radice.</span><span class="sxs-lookup"><span data-stu-id="25e56-253">The query writer for the encoder is obtained and the query expression "/" is used to set the metadata at the root navigation path.</span></span> <span data-ttu-id="25e56-254">È inoltre possibile utilizzare questo metodo quando si impostano blocchi di metadati annidati, modificando l'espressione di query nella posizione desiderata.</span><span class="sxs-lookup"><span data-stu-id="25e56-254">You can also use this method when setting nested metadata blocks, by adjusting the query expression to the desired location.</span></span>

<span data-ttu-id="25e56-255">Analogamente, è possibile creare un writer di query basato sul lettore di query del frame decodificato usando il metodo **CreateQueryWriterFromReader** della factory di imaging.</span><span class="sxs-lookup"><span data-stu-id="25e56-255">Similarly, you can create a query writer based on the decoded frame's query reader by using the imaging factory's **CreateQueryWriterFromReader** method.</span></span> <span data-ttu-id="25e56-256">Il writer di query creato in questa operazione verrà prepopolato con i metadati dall'Reader di query e potrà essere impostato nel frame.</span><span class="sxs-lookup"><span data-stu-id="25e56-256">The query writer created in this operation will be prepopulated with the metadata from the query reader and can then be set in the frame.</span></span> <span data-ttu-id="25e56-257">Il codice seguente illustra l'operazione di copia **CreateQueryWriterFromReader** .</span><span class="sxs-lookup"><span data-stu-id="25e56-257">The following code demonstrates the **CreateQueryWriterFromReader** copy operation.</span></span>


```
IWICMetadataQueryWriter *pNewWriter = NULL;

GUID vendor = GUID_VendorMicrosoft;
hr = pFactory->CreateQueryWriterFromReader(
    pFrameQReader,
    &vendor,
    &pNewWriter);

if (SUCCEEDED(hr))
{
    // Get the frame's query writer
    hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
}

// Set the query writer to the frame.
if (SUCCEEDED(hr))
{
    PROPVARIANT value;

    PropVariantInit(&value);
    value.vt = VT_UNKNOWN;
    value.punkVal = pNewWriter;
    value.punkVal->AddRef();
    hr = pFrameQWriter->SetMetadataByName(L"/",&value);
}
```



<span data-ttu-id="25e56-258">Questo metodo utilizza un writer di query separato basato sui dati del lettore di query.</span><span class="sxs-lookup"><span data-stu-id="25e56-258">This method uses a separate query writer is created that is based on the data of the query reader.</span></span> <span data-ttu-id="25e56-259">Questo nuovo writer di query viene quindi impostato nel frame.</span><span class="sxs-lookup"><span data-stu-id="25e56-259">This new query writer then set in the frame.</span></span>

<span data-ttu-id="25e56-260">Anche in questo caso, queste operazioni per la copia dei metadati funzionano solo quando le immagini di origine e di destinazione hanno lo stesso formato.</span><span class="sxs-lookup"><span data-stu-id="25e56-260">Again, these operations to copy metadata only work when the source and destination images have the same format.</span></span> <span data-ttu-id="25e56-261">Questo è dovuto al fatto che i diversi formati di immagine archiviano i blocchi di metadati in posizioni diverse.</span><span class="sxs-lookup"><span data-stu-id="25e56-261">This is because different image formats store the metadata blocks in different locations.</span></span> <span data-ttu-id="25e56-262">Ad esempio, JPEG e TIFF supportano i blocchi di metadati XMP.</span><span class="sxs-lookup"><span data-stu-id="25e56-262">For instance, both JPEG and TIFF support XMP metadata blocks.</span></span> <span data-ttu-id="25e56-263">Nelle immagini JPEG il blocco XMP si trova nel blocco di metadati radice, come illustrato nella [Panoramica dei metadati di WIC](-wic-about-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="25e56-263">In JPEG images, the XMP block is at the root metadata block as illustrated in the [WIC Metadata Overview](-wic-about-metadata.md).</span></span> <span data-ttu-id="25e56-264">Tuttavia, in un'immagine TIFF, il blocco XMP è annidato in un blocco IFD radice.</span><span class="sxs-lookup"><span data-stu-id="25e56-264">However, in a TIFF image, the XMP block is nested in a root IFD block.</span></span> <span data-ttu-id="25e56-265">Il diagramma seguente illustra le differenze tra un'immagine JPEG e un'immagine TIFF con gli stessi metadati di valutazione.</span><span class="sxs-lookup"><span data-stu-id="25e56-265">The following diagram illustrates the differences between a JPEG image and a TIFF image with the same rating metadata.</span></span>

![confronto tra JPEG e TIFF.](graphics/jpgvstiff.png)

## <a name="fast-metadata-encoding"></a><span data-ttu-id="25e56-267">Codifica rapida dei metadati</span><span class="sxs-lookup"><span data-stu-id="25e56-267">Fast Metadata Encoding</span></span>

<span data-ttu-id="25e56-268">Non è sempre necessario codificare nuovamente un'immagine per scrivervi nuovi metadati.</span><span class="sxs-lookup"><span data-stu-id="25e56-268">It is not always necessary to re-encode an image to write new metadata to it.</span></span> <span data-ttu-id="25e56-269">I metadati possono anche essere scritti usando un codificatore di metadati rapido.</span><span class="sxs-lookup"><span data-stu-id="25e56-269">Metadata can also be written by using a fast metadata encoder.</span></span> <span data-ttu-id="25e56-270">Un codificatore di metadati veloce può scrivere una quantità limitata di metadati in un'immagine senza ricodificare l'immagine.</span><span class="sxs-lookup"><span data-stu-id="25e56-270">A fast metadata encoder can write a limited amount of metadata to an image without re-encoding the image.</span></span> <span data-ttu-id="25e56-271">Questa operazione viene eseguita scrivendo i nuovi metadati all'interno della spaziatura interna vuota fornita da alcuni formati di metadati.</span><span class="sxs-lookup"><span data-stu-id="25e56-271">This is accomplished by writing the new metadata within the empty padding provided by some metadata formats.</span></span> <span data-ttu-id="25e56-272">I formati di metadati nativi che supportano la spaziatura dei metadati sono EXIF, IFD, GPS e XMP.</span><span class="sxs-lookup"><span data-stu-id="25e56-272">The native metadata formats that support metadata padding are Exif, IFD, GPS and XMP.</span></span>

### <a name="adding-padding-to-metadata-blocks"></a><span data-ttu-id="25e56-273">Aggiunta di spaziatura interna ai blocchi di metadati</span><span class="sxs-lookup"><span data-stu-id="25e56-273">Adding Padding to Metadata Blocks</span></span>

<span data-ttu-id="25e56-274">Prima di poter eseguire la codifica rapida dei metadati, è necessario che nel blocco di metadati sia disponibile spazio per la scrittura di più metadati.</span><span class="sxs-lookup"><span data-stu-id="25e56-274">Before you can perform fast metadata encoding, there must be room within the metadata block to write more metadata.</span></span> <span data-ttu-id="25e56-275">Se lo spazio disponibile nella spaziatura interna esistente non è sufficiente per la scrittura dei nuovi metadati, la codifica rapida dei metadati avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="25e56-275">If there is not enough room within the existing padding to write the new metadata, the fast metadata encoding will fail.</span></span> <span data-ttu-id="25e56-276">Per aggiungere la spaziatura dei metadati a un'immagine, l'immagine deve essere codificata nuovamente.</span><span class="sxs-lookup"><span data-stu-id="25e56-276">To add metadata padding to an image, the image must be re-encoded.</span></span> <span data-ttu-id="25e56-277">È possibile aggiungere spaziatura interna nello stesso modo in cui si aggiungono altri elementi di metadati, usando un'espressione di query, se il blocco di metadati che si sta riempiendo lo supporta.</span><span class="sxs-lookup"><span data-stu-id="25e56-277">You can add padding the same way you would add any other metadata item, by using a query expression, if the metadata block you are padding supports it.</span></span> <span data-ttu-id="25e56-278">Nell'esempio seguente viene illustrato come aggiungere spaziatura interna a un blocco IFD incorporato in un blocco App1.</span><span class="sxs-lookup"><span data-stu-id="25e56-278">The following example demonstrates how to add padding to an IFD block embedded in an App1 block.</span></span>


```
if (SUCCEEDED(hr))
{
    // Add metadata padding
    PROPVARIANT padding;

    PropVariantInit(&padding);
    padding.vt = VT_UI4;
    padding.uiVal = 4096; // 4KB

    hr = pFrameQWriter->SetMetadataByName(L"/app1/ifd/PaddingSchema:padding", &padding);

    PropVariantClear(&padding);
}
```



<span data-ttu-id="25e56-279">Per aggiungere spaziatura interna, creare un PROPVARIANT di tipo VT \_ UI4 e un valore corrispondente al numero di byte di spaziatura interna da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="25e56-279">To add padding, create a PROPVARIANT of type VT\_UI4 and a value corresponding to the number of bytes of padding to add.</span></span> <span data-ttu-id="25e56-280">Un valore tipico è 4096 byte.</span><span class="sxs-lookup"><span data-stu-id="25e56-280">A typical value is 4096 bytes.</span></span> <span data-ttu-id="25e56-281">Le query sui metadati per JPEG, TIFF e JPEG-XR sono disponibili in questa tabella.</span><span class="sxs-lookup"><span data-stu-id="25e56-281">The metadata queries for JPEG, TIFF, and JPEG-XR are in this table.</span></span>



| <span data-ttu-id="25e56-282">Formato metadati</span><span class="sxs-lookup"><span data-stu-id="25e56-282">Metadata format</span></span> | <span data-ttu-id="25e56-283">Query di metadati JPEG</span><span class="sxs-lookup"><span data-stu-id="25e56-283">JPEG metadata query</span></span>                  | <span data-ttu-id="25e56-284">Query di metadati TIFF, JPEG-XR</span><span class="sxs-lookup"><span data-stu-id="25e56-284">TIFF, JPEG-XR metadata query</span></span>    |
|-----------------|--------------------------------------|---------------------------------|
| <span data-ttu-id="25e56-285">IFD</span><span class="sxs-lookup"><span data-stu-id="25e56-285">IFD</span></span>             | <span data-ttu-id="25e56-286">/app1/ifd/PaddingSchema: riempimento</span><span class="sxs-lookup"><span data-stu-id="25e56-286">/app1/ifd/PaddingSchema:Padding</span></span>      | <span data-ttu-id="25e56-287">/ifd/PaddingSchema: riempimento</span><span class="sxs-lookup"><span data-stu-id="25e56-287">/ifd/PaddingSchema:Padding</span></span>      |
| <span data-ttu-id="25e56-288">EXIF</span><span class="sxs-lookup"><span data-stu-id="25e56-288">EXIF</span></span>            | <span data-ttu-id="25e56-289">/app1/ifd/exif/PaddingSchema: riempimento</span><span class="sxs-lookup"><span data-stu-id="25e56-289">/app1/ifd/exif/PaddingSchema:Padding</span></span> | <span data-ttu-id="25e56-290">/ifd/exif/PaddingSchema: riempimento</span><span class="sxs-lookup"><span data-stu-id="25e56-290">/ifd/exif/PaddingSchema:Padding</span></span> |
| <span data-ttu-id="25e56-291">XMP</span><span class="sxs-lookup"><span data-stu-id="25e56-291">XMP</span></span>             | <span data-ttu-id="25e56-292">/xmp/PaddingSchema: riempimento</span><span class="sxs-lookup"><span data-stu-id="25e56-292">/xmp/PaddingSchema:Padding</span></span>           | <span data-ttu-id="25e56-293">/ifd/xmp/PaddingSchema: riempimento</span><span class="sxs-lookup"><span data-stu-id="25e56-293">/ifd/xmp/PaddingSchema:Padding</span></span>  |
| <span data-ttu-id="25e56-294">GPS</span><span class="sxs-lookup"><span data-stu-id="25e56-294">GPS</span></span>             | <span data-ttu-id="25e56-295">/app1/ifd/gps/PaddingSchema: riempimento</span><span class="sxs-lookup"><span data-stu-id="25e56-295">/app1/ifd/gps/PaddingSchema:Padding</span></span>  | <span data-ttu-id="25e56-296">/ifd/gps/PaddingSchema: riempimento</span><span class="sxs-lookup"><span data-stu-id="25e56-296">/ifd/gps/PaddingSchema:Padding</span></span>  |



 

### <a name="obtaining-a-fast-metadata-encoder"></a><span data-ttu-id="25e56-297">Acquisizione di un codificatore di metadati rapido</span><span class="sxs-lookup"><span data-stu-id="25e56-297">Obtaining a Fast Metadata Encoder</span></span>

<span data-ttu-id="25e56-298">Quando si dispone di un'immagine con riempimento dei metadati, è possibile ottenere un codificatore di metadati rapido usando i metodi **CreateFastMetadataEncoderFromDecoder** e **CreateFastMetadataEncoderFromFrameDecode** di imaging Factory.</span><span class="sxs-lookup"><span data-stu-id="25e56-298">When you have an image with metadata padding, a fast metadata encoder can be obtained by using the imaging factory methods **CreateFastMetadataEncoderFromDecoder** and **CreateFastMetadataEncoderFromFrameDecode**.</span></span>

<span data-ttu-id="25e56-299">Come suggerisce il nome, **CreateFastMetadataEncoderFromDecoder** crea un codificatore di metadati rapido per i metadati a livello di decodificatore.</span><span class="sxs-lookup"><span data-stu-id="25e56-299">As the name implies, **CreateFastMetadataEncoderFromDecoder** creates a fast metadata encoder for decoder-level metadata.</span></span> <span data-ttu-id="25e56-300">I formati di immagine nativi forniti da WIC non supportano i metadati a livello di decodificatore, ma questo metodo viene fornito nel caso in cui tale formato di immagine venga sviluppato in futuro.</span><span class="sxs-lookup"><span data-stu-id="25e56-300">The native image formats provided by WIC do not support decoder-level metadata but this method is provided in case such an image format is developed in the future.</span></span>

<span data-ttu-id="25e56-301">Lo scenario più comune consiste nell'ottenere un codificatore di metadati veloce da un frame di immagini usando **CreateFastMetadataEncoderFromFrameDecode**.</span><span class="sxs-lookup"><span data-stu-id="25e56-301">The more common scenario is to obtain a fast metadata encoder from an image frame by using **CreateFastMetadataEncoderFromFrameDecode**.</span></span> <span data-ttu-id="25e56-302">Il codice seguente ottiene un codificatore di metadati Fast del frame decodificato e modifica il valore della classificazione nel blocco App1.</span><span class="sxs-lookup"><span data-stu-id="25e56-302">The following code obtains a decoded frame's fast metadata encoder and changes the rating value in the App1 block.</span></span>


```
if (SUCCEEDED(hr))
{
    IWICFastMetadataEncoder *pFME = NULL;
    IWICMetadataQueryWriter *pFMEQW = NULL;

    hr = pFactory->CreateFastMetadataEncoderFromFrameDecode(
        pFrameDecode, 
        &pFME);
}
```



### <a name="using-the-fast-metadata-encoder"></a><span data-ttu-id="25e56-303">Uso del codificatore di metadati veloci</span><span class="sxs-lookup"><span data-stu-id="25e56-303">Using the Fast Metadata Encoder</span></span>

<span data-ttu-id="25e56-304">Dal codificatore di metadati rapido, è possibile ottenere un writer di query.</span><span class="sxs-lookup"><span data-stu-id="25e56-304">From the fast metadata encoder, you can obtain a query writer.</span></span> <span data-ttu-id="25e56-305">Questo consente di scrivere i metadati usando un'espressione di query, come illustrato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="25e56-305">This enables you to write metadata by using a query expression as previously demonstrated.</span></span> <span data-ttu-id="25e56-306">Dopo aver impostato i metadati nel writer di query, eseguire il commit del codificatore di metadati rapido per finalizzare l'aggiornamento dei metadati.</span><span class="sxs-lookup"><span data-stu-id="25e56-306">After metadata has been set in the query writer, commit the fast metadata encoder to finalize the metadata update.</span></span> <span data-ttu-id="25e56-307">Il codice seguente illustra l'impostazione e il commit delle modifiche dei metadati</span><span class="sxs-lookup"><span data-stu-id="25e56-307">The following code demonstrates setting and committing the metadata changes</span></span>


```
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



<span data-ttu-id="25e56-308">Se il **commit** ha esito negativo per qualsiasi motivo, è necessario codificare nuovamente l'immagine per assicurarsi che i nuovi metadati vengano aggiunti all'immagine.</span><span class="sxs-lookup"><span data-stu-id="25e56-308">If **Commit** fails for any reason, you will need to re-encode the image to ensure the new metadata is added to the image.</span></span>

## <a name="related-topics"></a><span data-ttu-id="25e56-309">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="25e56-309">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="25e56-310">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="25e56-310">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="25e56-311">Panoramica del componente imaging Windows</span><span class="sxs-lookup"><span data-stu-id="25e56-311">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="25e56-312">Cenni preliminari sui metadati WIC</span><span class="sxs-lookup"><span data-stu-id="25e56-312">WIC Metadata Overview</span></span>](-wic-about-metadata.md)
</dt> <dt>

[<span data-ttu-id="25e56-313">Cenni preliminari sul linguaggio di query dei metadati</span><span class="sxs-lookup"><span data-stu-id="25e56-313">Metadata Query Language Overview</span></span>](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[<span data-ttu-id="25e56-314">Panoramica dell'estendibilità dei metadati</span><span class="sxs-lookup"><span data-stu-id="25e56-314">Metadata Extensibility Overview</span></span>](-wic-codec-metadatahandlers.md)
</dt> <dt>

[<span data-ttu-id="25e56-315">Procedura: ricodificare un'immagine JPEG con i metadati</span><span class="sxs-lookup"><span data-stu-id="25e56-315">How-to: Re-encode a JPEG Image with Metadata</span></span>](-wic-codec-jpegmetadataencoding.md)
</dt> </dl>

 

 
