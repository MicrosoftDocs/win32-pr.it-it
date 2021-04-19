---
description: Nell'esempio seguente viene illustrato come codificare nuovamente un'immagine e i relativi metadati in un nuovo file con lo stesso formato.
ms.assetid: a7cfaa6d-e17d-458a-ae63-72963615bef8
title: "Procedura: codificare nuovamente un'immagine JPEG con i metadati"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c023defb760faeab2bc6ea92232fcc916ef15126
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/20/2021
ms.locfileid: "106323892"
---
# <a name="how-to-re-encode-a-jpeg-image-with-metadata"></a><span data-ttu-id="9c264-103">Procedura: codificare nuovamente un'immagine JPEG con i metadati</span><span class="sxs-lookup"><span data-stu-id="9c264-103">How-to re-encode a JPEG image with metadata</span></span>

<span data-ttu-id="9c264-104">Nell'esempio seguente viene illustrato come codificare nuovamente un'immagine e i relativi metadati in un nuovo file con lo stesso formato.</span><span class="sxs-lookup"><span data-stu-id="9c264-104">The following example demonstrates how to re-encode an image and its metadata to a new file of the same format.</span></span> <span data-ttu-id="9c264-105">In questo esempio vengono inoltre aggiunti metadati per illustrare un'espressione a elemento singolo utilizzata da un writer di query.</span><span class="sxs-lookup"><span data-stu-id="9c264-105">In addition, this example adds metadata to demonstrate a single-item expression used by a query writer.</span></span>

<span data-ttu-id="9c264-106">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="9c264-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="9c264-107">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="9c264-107">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="9c264-108">Parte 1: decodificare un'immagine</span><span class="sxs-lookup"><span data-stu-id="9c264-108">Part 1: Decode an Image</span></span>](#part-1-decode-an-image)
-   [<span data-ttu-id="9c264-109">Parte 2: creare e inizializzare il codificatore di immagini</span><span class="sxs-lookup"><span data-stu-id="9c264-109">Part 2: Create and Initialize the Image Encoder</span></span>](#part-2-create-and-initialize-the-image-encoder)
-   [<span data-ttu-id="9c264-110">Parte 3: copiare le informazioni sul frame decodificato</span><span class="sxs-lookup"><span data-stu-id="9c264-110">Part 3: Copy Decoded Frame Information</span></span>](#part-3-copy-decoded-frame-information)
-   [<span data-ttu-id="9c264-111">Parte 4: copiare i metadati</span><span class="sxs-lookup"><span data-stu-id="9c264-111">Part 4: Copy the Metadata</span></span>](#part-4-copy-the-metadata)
-   [<span data-ttu-id="9c264-112">Parte 5: aggiungere metadati aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="9c264-112">Part 5: Add Additional Metadata</span></span>](#part-5-add-additional-metadata)
-   [<span data-ttu-id="9c264-113">Parte 6: finalizzare l'immagine codificata</span><span class="sxs-lookup"><span data-stu-id="9c264-113">Part 6: Finalize the Encoded Image</span></span>](#part-6-finalize-the-encoded-image)
-   [<span data-ttu-id="9c264-114">Codice di esempio di ricodifica JPEG</span><span class="sxs-lookup"><span data-stu-id="9c264-114">JPEG Re-encode Example Code</span></span>](#jpeg-re-encode-example-code)
-   [<span data-ttu-id="9c264-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9c264-115">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="9c264-116">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="9c264-116">Prerequisites</span></span>

<span data-ttu-id="9c264-117">Per comprendere questo argomento, è necessario avere familiarità con il sistema di metadati di Windows Imaging Component (WIC), come descritto in [Panoramica dei metadati di WIC](-wic-about-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="9c264-117">To understand this topic, you should be familiar with the Windows Imaging Component (WIC) metadata system as described in the [WIC Metadata Overview](-wic-about-metadata.md).</span></span> <span data-ttu-id="9c264-118">È anche necessario avere familiarità con i componenti del codec WIC come descritto in Panoramica dei componenti di [Windows Imaging](-wic-about-windows-imaging-codec.md).</span><span class="sxs-lookup"><span data-stu-id="9c264-118">You should also be familiar with the WIC codec components as described in the [Windows Imaging Component Overview](-wic-about-windows-imaging-codec.md).</span></span>

## <a name="part-1-decode-an-image"></a><span data-ttu-id="9c264-119">Parte 1: decodificare un'immagine</span><span class="sxs-lookup"><span data-stu-id="9c264-119">Part 1: Decode an Image</span></span>

<span data-ttu-id="9c264-120">Prima di poter copiare i dati o i metadati delle immagini in un nuovo file di immagine, è necessario creare prima un decodificatore per l'immagine esistente che si vuole ricodificare.</span><span class="sxs-lookup"><span data-stu-id="9c264-120">Before you can copy image data or metadata to a new image file, you must first create a decoder for the existing image that you want to re-encode.</span></span> <span data-ttu-id="9c264-121">Nel codice seguente viene illustrato come creare un decodificatore WIC per il file di immagine test.jpg.</span><span class="sxs-lookup"><span data-stu-id="9c264-121">The following code demonstrates how to create a WIC decoder for the image file test.jpg.</span></span>


```C++
    // Initialize COM.
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);

    IWICImagingFactory *piFactory = NULL;
    IWICBitmapDecoder *piDecoder = NULL;

    // Create the COM imaging factory.
    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(CLSID_WICImagingFactory,
        NULL, CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&piFactory));
    }

    // Create the decoder.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateDecoderFromFilename(L"test.jpg", NULL, GENERIC_READ,
            WICDecodeMetadataCacheOnDemand, //For JPEG lossless decoding/encoding.
            &piDecoder);
    }
```



<span data-ttu-id="9c264-122">La chiamata a **CreateDecoderFromFilename** ha usato il valore WICDecodeMetadataCacheOnDemand dall'enumerazione [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) come quarto parametro.</span><span class="sxs-lookup"><span data-stu-id="9c264-122">The call to **CreateDecoderFromFilename** used the value WICDecodeMetadataCacheOnDemand from the [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) enumeration as the fourth parameter.</span></span> <span data-ttu-id="9c264-123">Ciò indica al decodificatore di memorizzare nella cache i metadati quando i metadati sono necessari, ottenendo un lettore di query o utilizzando il lettore di metadati sottostante.</span><span class="sxs-lookup"><span data-stu-id="9c264-123">This tells the decoder to cache the metadata when the metadata is needed, either by obtaining a query reader or by using the underlying metadata reader.</span></span> <span data-ttu-id="9c264-124">L'utilizzo di questa opzione consente di mantenere il flusso ai metadati, che è necessario per l'esecuzione di una codifica rapida dei metadati e consente la decodifica e la codifica senza perdita di immagini JPEG.</span><span class="sxs-lookup"><span data-stu-id="9c264-124">Using this option enables you to retain the stream to the metadata, which is required for performing fast metadata encoding and enables lossless decoding and encoding of JPEG images.</span></span> <span data-ttu-id="9c264-125">In alternativa, è possibile usare l'altro valore di **WICDecodeOptions** , WICDecodeMetadataCacheOnLoad, che memorizza nella cache i metadati dell'immagine incorporata non appena l'immagine viene caricata.</span><span class="sxs-lookup"><span data-stu-id="9c264-125">Alternatively, you could use the other **WICDecodeOptions** value, WICDecodeMetadataCacheOnLoad, which caches the embedded image metadata as soon as the image is loaded.</span></span>

## <a name="part-2-create-and-initialize-the-image-encoder"></a><span data-ttu-id="9c264-126">Parte 2: creare e inizializzare il codificatore di immagini</span><span class="sxs-lookup"><span data-stu-id="9c264-126">Part 2: Create and Initialize the Image Encoder</span></span>

<span data-ttu-id="9c264-127">Il codice seguente illustra la creazione del codificatore che verrà usato per codificare l'immagine precedentemente decodificata.</span><span class="sxs-lookup"><span data-stu-id="9c264-127">The following code demonstrates the creation of the encoder you will use to encode the image you previously decoded.</span></span>


```C++
    // Variables used for encoding.
    IWICStream *piFileStream = NULL;
    IWICBitmapEncoder *piEncoder = NULL;
    IWICMetadataBlockWriter *piBlockWriter = NULL;
    IWICMetadataBlockReader *piBlockReader = NULL;

    WICPixelFormatGUID pixelFormat = { 0 };
    UINT count = 0;
    double dpiX, dpiY = 0.0;
    UINT width, height = 0;

    // Create a file stream.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateStream(&piFileStream);
    }

    // Initialize our new file stream.
    if (SUCCEEDED(hr))
    {
        hr = piFileStream->InitializeFromFilename(L"test2.jpg", GENERIC_WRITE);
    }

    // Create the encoder.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateEncoder(GUID_ContainerFormatJpeg, NULL, &piEncoder);
    }
    // Initialize the encoder
    if (SUCCEEDED(hr))
    {
        hr = piEncoder->Initialize(piFileStream,WICBitmapEncoderNoCache);
    }
```



<span data-ttu-id="9c264-128">Un flusso di file WIC piFileStream viene creato e inizializzato per la scrittura nel file di immagine "test2.jpg".</span><span class="sxs-lookup"><span data-stu-id="9c264-128">A WIC file stream piFileStream is created and initialized for writing to the image file "test2.jpg".</span></span> <span data-ttu-id="9c264-129">piFileStream viene quindi utilizzato per inizializzare il codificatore, in modo da informare il codificatore dove scrivere i bit dell'immagine al termine della codifica.</span><span class="sxs-lookup"><span data-stu-id="9c264-129">piFileStream is then used to initialize the encoder, informing the encoder where to write the image bits when the encoding is complete.</span></span>

## <a name="part-3-copy-decoded-frame-information"></a><span data-ttu-id="9c264-130">Parte 3: copiare le informazioni sul frame decodificato</span><span class="sxs-lookup"><span data-stu-id="9c264-130">Part 3: Copy Decoded Frame Information</span></span>

<span data-ttu-id="9c264-131">Il codice seguente copia ogni frame di un'immagine in un nuovo frame del codificatore.</span><span class="sxs-lookup"><span data-stu-id="9c264-131">The following code copies each frame of an image to a new frame of the encoder.</span></span> <span data-ttu-id="9c264-132">Questa copia include le dimensioni, la risoluzione e il formato pixel; Tutti questi sono necessari per creare un frame valido.</span><span class="sxs-lookup"><span data-stu-id="9c264-132">This copy includes size, resolution, and pixel format; all of which are necessary to create a valid frame.</span></span>

> [!Note]  
> <span data-ttu-id="9c264-133">Le immagini JPEG avranno un solo frame e il ciclo seguente non è tecnicamente necessario, ma è incluso per illustrare l'utilizzo di più frame per i formati che lo supportano.</span><span class="sxs-lookup"><span data-stu-id="9c264-133">JPEG images will only have one frame and the loop below is not technically necessary but is included to demonstrate multi-frame usage for formats that support it.</span></span>

 


```C++
    if (SUCCEEDED(hr))
    {
        hr = piDecoder->GetFrameCount(&count);
    }

    if (SUCCEEDED(hr))
    {
        // Process each frame of the image.
        for (UINT i=0; i<count && SUCCEEDED(hr); i++)
        {
            // Frame variables.
            IWICBitmapFrameDecode *piFrameDecode = NULL;
            IWICBitmapFrameEncode *piFrameEncode = NULL;
            IWICMetadataQueryReader *piFrameQReader = NULL;
            IWICMetadataQueryWriter *piFrameQWriter = NULL;

            // Get and create the image frame.
            if (SUCCEEDED(hr))
            {
                hr = piDecoder->GetFrame(i, &piFrameDecode);
            }
            if (SUCCEEDED(hr))
            {
                hr = piEncoder->CreateNewFrame(&piFrameEncode, NULL);
            }

            // Initialize the encoder.
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->Initialize(NULL);
            }
            // Get and set the size.
            if (SUCCEEDED(hr))
            {
                hr = piFrameDecode->GetSize(&width, &height);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetSize(width, height);
            }
            // Get and set the resolution.
            if (SUCCEEDED(hr))
            {
                piFrameDecode->GetResolution(&dpiX, &dpiY);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetResolution(dpiX, dpiY);
            }
            // Set the pixel format.
            if (SUCCEEDED(hr))
            {
                piFrameDecode->GetPixelFormat(&pixelFormat);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetPixelFormat(&pixelFormat);
            }
```



<span data-ttu-id="9c264-134">Il codice seguente esegue un controllo rapido per determinare se i formati di immagine di origine e di destinazione sono uguali.</span><span class="sxs-lookup"><span data-stu-id="9c264-134">The following code performs a quick check to determine whether the source and destination image formats are the same.</span></span> <span data-ttu-id="9c264-135">Questa operazione è necessaria come parte 4 che mostra un'operazione supportata solo quando il formato di origine e di destinazione è lo stesso.</span><span class="sxs-lookup"><span data-stu-id="9c264-135">This is needed as Part 4 shows an operation that is only supported when the source and destination format are the same.</span></span>


```C++
            // Check that the destination format and source formats are the same.
            bool formatsEqual = FALSE;
            if (SUCCEEDED(hr))
            {
                GUID srcFormat;
                GUID destFormat;

                hr = piDecoder->GetContainerFormat(&srcFormat);
                if (SUCCEEDED(hr))
                {
                    hr = piEncoder->GetContainerFormat(&destFormat);
                }
                if (SUCCEEDED(hr))
                {
                    if (srcFormat == destFormat)
                        formatsEqual = true;
                    else
                        formatsEqual = false;
                }
            }
```



## <a name="part-4-copy-the-metadata"></a><span data-ttu-id="9c264-136">Parte 4: copiare i metadati</span><span class="sxs-lookup"><span data-stu-id="9c264-136">Part 4: Copy the Metadata</span></span>

> [!Note]  
> <span data-ttu-id="9c264-137">Il codice contenuto in questa sezione è valido solo se i formati di immagine di origine e di destinazione sono uguali.</span><span class="sxs-lookup"><span data-stu-id="9c264-137">The code in this section is valid only when the source and destination image formats are the same.</span></span> <span data-ttu-id="9c264-138">Non è possibile copiare tutti i metadati di un'immagine in un'unica operazione quando si esegue la codifica in un formato di immagine diverso.</span><span class="sxs-lookup"><span data-stu-id="9c264-138">You cannot copy all of an image's metadata in a single operation when encoding to a different image format.</span></span>

 

<span data-ttu-id="9c264-139">Per mantenere i metadati durante la ricodifica di un'immagine nello stesso formato di immagine, sono disponibili metodi per la copia di tutti i metadati in un'unica operazione.</span><span class="sxs-lookup"><span data-stu-id="9c264-139">To preserve metadata while re-encoding an image to the same image format, there are methods available for copying all the metadata in a single operation.</span></span> <span data-ttu-id="9c264-140">Ognuna di queste operazioni segue un modello simile. ogni imposta i metadati del frame decodificato direttamente nel nuovo frame da codificare.</span><span class="sxs-lookup"><span data-stu-id="9c264-140">Each of these operations follows a similar pattern; each sets the decoded frame's metadata directly into the new frame being encoded.</span></span> <span data-ttu-id="9c264-141">Si noti che questa operazione viene eseguita per ogni singolo frame di immagine.</span><span class="sxs-lookup"><span data-stu-id="9c264-141">Note that this is done for each individual image frame.</span></span>

<span data-ttu-id="9c264-142">Il metodo preferito per la copia dei metadati consiste nell'inizializzare il writer del blocco del nuovo frame con il lettore di blocco del frame decodificato.</span><span class="sxs-lookup"><span data-stu-id="9c264-142">The preferred method for copying metadata is to initialize the new frame's block writer with the decoded frame's block reader.</span></span> <span data-ttu-id="9c264-143">Il codice seguente illustra questo metodo.</span><span class="sxs-lookup"><span data-stu-id="9c264-143">The following code demonstrates this method.</span></span>


```C++
            if (SUCCEEDED(hr) && formatsEqual)
            {
                // Copy metadata using metadata block reader/writer.
                if (SUCCEEDED(hr))
                {
                    piFrameDecode->QueryInterface(IID_PPV_ARGS(&piBlockReader));
                }
                if (SUCCEEDED(hr))
                {
                    piFrameEncode->QueryInterface(IID_PPV_ARGS(&piBlockWriter));
                }
                if (SUCCEEDED(hr))
                {
                    piBlockWriter->InitializeFromBlockReader(piBlockReader);
                }
            }
```



<span data-ttu-id="9c264-144">In questo esempio si ottengono semplicemente il Reader di blocco e il writer del blocco rispettivamente dal frame di origine e dal frame di destinazione.</span><span class="sxs-lookup"><span data-stu-id="9c264-144">In this example, you simply obtain the block reader and block writer from the source frame and destination frame, respectively.</span></span> <span data-ttu-id="9c264-145">Il writer di blocco viene quindi inizializzato dal lettore del blocco.</span><span class="sxs-lookup"><span data-stu-id="9c264-145">The block writer is then initialized from the block reader.</span></span> <span data-ttu-id="9c264-146">Viene così inizializzato il writer del blocco con i metadati pre-popolati del lettore di blocchi.</span><span class="sxs-lookup"><span data-stu-id="9c264-146">This initializes the block writer with the pre-populated metadata of the block reader.</span></span> <span data-ttu-id="9c264-147">Per ulteriori metodi per la copia dei metadati, vedere la sezione relativa alla scrittura dei metadati nella [Panoramica della lettura e scrittura dei metadati delle immagini](-wic-codec-readingwritingmetadata.md).</span><span class="sxs-lookup"><span data-stu-id="9c264-147">To learn additional methods for copying metadata, see the Writing Metadata section in the [Overview of Reading and Writing Image Metadata](-wic-codec-readingwritingmetadata.md).</span></span>

<span data-ttu-id="9c264-148">Anche in questo caso, questa operazione funziona solo se le immagini di origine e di destinazione hanno lo stesso formato.</span><span class="sxs-lookup"><span data-stu-id="9c264-148">Again, this operation works only when the source and destination images have the same format.</span></span> <span data-ttu-id="9c264-149">Questo è dovuto al fatto che i diversi formati di immagine archiviano i blocchi di metadati in posizioni diverse.</span><span class="sxs-lookup"><span data-stu-id="9c264-149">This is because different image formats store the metadata blocks in different locations.</span></span> <span data-ttu-id="9c264-150">Ad esempio, JPEG e Tagged Image File Format (TIFF) supportano i blocchi di metadati di Extensible Metadata Platform (XMP).</span><span class="sxs-lookup"><span data-stu-id="9c264-150">For instance, both JPEG and Tagged Image File Format (TIFF) support Extensible Metadata Platform (XMP) metadata blocks.</span></span> <span data-ttu-id="9c264-151">Nelle immagini JPEG il blocco XMP si trova nel blocco di metadati radice, come illustrato nella [Panoramica dei metadati di WIC](-wic-about-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="9c264-151">In JPEG images, the XMP block is at the root metadata block as illustrated in the [WIC Metadata Overview](-wic-about-metadata.md).</span></span> <span data-ttu-id="9c264-152">Tuttavia, in un'immagine TIFF, il blocco XMP è incorporato nel blocco IFD radice.</span><span class="sxs-lookup"><span data-stu-id="9c264-152">However, in a TIFF image, the XMP block is embedded in the root IFD block.</span></span>

## <a name="part-5-add-additional-metadata"></a><span data-ttu-id="9c264-153">Parte 5: aggiungere metadati aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="9c264-153">Part 5: Add Additional Metadata</span></span>

<span data-ttu-id="9c264-154">Nell'esempio seguente viene illustrato come aggiungere metadati all'immagine di destinazione.</span><span class="sxs-lookup"><span data-stu-id="9c264-154">The following example demonstrates how to add metadata to the destination image.</span></span> <span data-ttu-id="9c264-155">Questa operazione viene eseguita chiamando il metodo **SetMetadataByName** del writer di query utilizzando un'espressione di query e i dati archiviati in un [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).</span><span class="sxs-lookup"><span data-stu-id="9c264-155">This is done by calling the query writer's **SetMetadataByName** method using a query expression and the data stored in a [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).</span></span>


```C++
            if(SUCCEEDED(hr))
            {
                hr = piFrameEncode->GetMetadataQueryWriter(&piFrameQWriter);
            }
            if (SUCCEEDED(hr))
            {
                // Add additional metadata.
                PROPVARIANT    value;
                value.vt = VT_LPWSTR;
                value.pwszVal= L"Metadata Test Image.";
                hr = piFrameQWriter->SetMetadataByName(L"/xmp/dc:title", &value);
            }
```



<span data-ttu-id="9c264-156">Per ulteriori informazioni sull'espressione di query, vedere [Cenni preliminari sul linguaggio di query dei metadati](-wic-codec-metadataquerylanguage.md).</span><span class="sxs-lookup"><span data-stu-id="9c264-156">For more information on the query expression, see the [Metadata Query Language Overview](-wic-codec-metadataquerylanguage.md).</span></span>

## <a name="part-6-finalize-the-encoded-image"></a><span data-ttu-id="9c264-157">Parte 6: finalizzare l'immagine codificata</span><span class="sxs-lookup"><span data-stu-id="9c264-157">Part 6: Finalize the Encoded Image</span></span>

<span data-ttu-id="9c264-158">I passaggi finali per la copia dell'immagine sono la scrittura dei dati pixel per il frame, il commit del frame nel codificatore e il commit del codificatore.</span><span class="sxs-lookup"><span data-stu-id="9c264-158">The final steps for copying the image are to write the pixel data for the frame, commit the frame to the encoder, and commit the encoder.</span></span> <span data-ttu-id="9c264-159">Il commit del codificatore scrive il flusso dell'immagine nel file.</span><span class="sxs-lookup"><span data-stu-id="9c264-159">Committing the encoder writes the image stream to the file.</span></span>


```C++
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->WriteSource(
                    static_cast<IWICBitmapSource*> (piFrameDecode),
                    NULL); // Using NULL enables JPEG loss-less encoding.
            }

            // Commit the frame.
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->Commit();
            }

            if (piFrameDecode)
            {
                piFrameDecode->Release();
            }

            if (piFrameEncode)
            {
                piFrameEncode->Release();
            }

            if (piFrameQReader)
            {
                piFrameQReader->Release();
            }

            if (piFrameQWriter)
            {
                piFrameQWriter->Release();
            }
        }
    }

    if (SUCCEEDED(hr))
    {
        piEncoder->Commit();
    }

    if (SUCCEEDED(hr))
    {
        piFileStream->Commit(STGC_DEFAULT);
    }

    if (piFileStream)
    {
        piFileStream->Release();
    }
    if (piEncoder)
    {
        piEncoder->Release();
    }
    if (piBlockWriter)
    {
        piBlockWriter->Release();
    }
    if (piBlockReader)
    {
        piBlockReader->Release();
    }
```



<span data-ttu-id="9c264-160">Il metodo **WriteSource** del frame viene usato per scrivere i dati pixel per l'immagine.</span><span class="sxs-lookup"><span data-stu-id="9c264-160">The frame's **WriteSource** method is used to write the pixel data for the image.</span></span> <span data-ttu-id="9c264-161">Si noti che questa operazione viene eseguita dopo la scrittura dei metadati.</span><span class="sxs-lookup"><span data-stu-id="9c264-161">Note that this is done after the metadata has been written.</span></span> <span data-ttu-id="9c264-162">Questa operazione è necessaria per garantire che i metadati dispongano di spazio sufficiente all'interno del file di immagine.</span><span class="sxs-lookup"><span data-stu-id="9c264-162">This is necessary to ensure that the metadata has enough space within the image file.</span></span> <span data-ttu-id="9c264-163">Una volta scritti i dati pixel, il frame viene scritto nel flusso usando il metodo **commit** del frame.</span><span class="sxs-lookup"><span data-stu-id="9c264-163">After the pixel data is written, the frame is written to the stream using the frame's **Commit** method.</span></span> <span data-ttu-id="9c264-164">Dopo l'elaborazione di tutti i frame, il codificatore (e quindi l'immagine) viene finalizzato usando il metodo **commit** del codificatore.</span><span class="sxs-lookup"><span data-stu-id="9c264-164">After all frames have been processed, the encoder (and thus the image) is finalized using the encoder's **Commit** method.</span></span>

<span data-ttu-id="9c264-165">Dopo aver eseguito il commit del frame, è necessario rilasciare gli oggetti COM creati nel ciclo.</span><span class="sxs-lookup"><span data-stu-id="9c264-165">Once you commit the frame, you must release the COM objects created in the loop.</span></span>

## <a name="jpeg-re-encode-example-code"></a><span data-ttu-id="9c264-166">Codice di esempio di ricodifica JPEG</span><span class="sxs-lookup"><span data-stu-id="9c264-166">JPEG Re-encode Example Code</span></span>

<span data-ttu-id="9c264-167">Di seguito è riportato il codice delle parti da 1 a 6 in un blocco conveniente.</span><span class="sxs-lookup"><span data-stu-id="9c264-167">The following is the code from Parts 1 through 6 in one convienient block.</span></span>


```C++
#include <Windows.h>
#include <Wincodecsdk.h>

int main()
{
    // Initialize COM.
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);

    IWICImagingFactory *piFactory = NULL;
    IWICBitmapDecoder *piDecoder = NULL;

    // Create the COM imaging factory.
    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(CLSID_WICImagingFactory,
        NULL, CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&piFactory));
    }

    // Create the decoder.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateDecoderFromFilename(L"test.jpg", NULL, GENERIC_READ,
            WICDecodeMetadataCacheOnDemand, //For JPEG lossless decoding/encoding.
            &piDecoder);
    }

    // Variables used for encoding.
    IWICStream *piFileStream = NULL;
    IWICBitmapEncoder *piEncoder = NULL;
    IWICMetadataBlockWriter *piBlockWriter = NULL;
    IWICMetadataBlockReader *piBlockReader = NULL;

    WICPixelFormatGUID pixelFormat = { 0 };
    UINT count = 0;
    double dpiX, dpiY = 0.0;
    UINT width, height = 0;

    // Create a file stream.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateStream(&piFileStream);
    }

    // Initialize our new file stream.
    if (SUCCEEDED(hr))
    {
        hr = piFileStream->InitializeFromFilename(L"test2.jpg", GENERIC_WRITE);
    }

    // Create the encoder.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateEncoder(GUID_ContainerFormatJpeg, NULL, &piEncoder);
    }
    // Initialize the encoder
    if (SUCCEEDED(hr))
    {
        hr = piEncoder->Initialize(piFileStream,WICBitmapEncoderNoCache);
    }

    if (SUCCEEDED(hr))
    {
        hr = piDecoder->GetFrameCount(&count);
    }

    if (SUCCEEDED(hr))
    {
        // Process each frame of the image.
        for (UINT i=0; i<count && SUCCEEDED(hr); i++)
        {
            // Frame variables.
            IWICBitmapFrameDecode *piFrameDecode = NULL;
            IWICBitmapFrameEncode *piFrameEncode = NULL;
            IWICMetadataQueryReader *piFrameQReader = NULL;
            IWICMetadataQueryWriter *piFrameQWriter = NULL;

            // Get and create the image frame.
            if (SUCCEEDED(hr))
            {
                hr = piDecoder->GetFrame(i, &piFrameDecode);
            }
            if (SUCCEEDED(hr))
            {
                hr = piEncoder->CreateNewFrame(&piFrameEncode, NULL);
            }

            // Initialize the encoder.
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->Initialize(NULL);
            }
            // Get and set the size.
            if (SUCCEEDED(hr))
            {
                hr = piFrameDecode->GetSize(&width, &height);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetSize(width, height);
            }
            // Get and set the resolution.
            if (SUCCEEDED(hr))
            {
                piFrameDecode->GetResolution(&dpiX, &dpiY);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetResolution(dpiX, dpiY);
            }
            // Set the pixel format.
            if (SUCCEEDED(hr))
            {
                piFrameDecode->GetPixelFormat(&pixelFormat);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetPixelFormat(&pixelFormat);
            }

            // Check that the destination format and source formats are the same.
            bool formatsEqual = FALSE;
            if (SUCCEEDED(hr))
            {
                GUID srcFormat;
                GUID destFormat;

                hr = piDecoder->GetContainerFormat(&srcFormat);
                if (SUCCEEDED(hr))
                {
                    hr = piEncoder->GetContainerFormat(&destFormat);
                }
                if (SUCCEEDED(hr))
                {
                    if (srcFormat == destFormat)
                        formatsEqual = true;
                    else
                        formatsEqual = false;
                }
            }

            if (SUCCEEDED(hr) && formatsEqual)
            {
                // Copy metadata using metadata block reader/writer.
                if (SUCCEEDED(hr))
                {
                    piFrameDecode->QueryInterface(IID_PPV_ARGS(&piBlockReader));
                }
                if (SUCCEEDED(hr))
                {
                    piFrameEncode->QueryInterface(IID_PPV_ARGS(&piBlockWriter));
                }
                if (SUCCEEDED(hr))
                {
                    piBlockWriter->InitializeFromBlockReader(piBlockReader);
                }
            }

            if(SUCCEEDED(hr))
            {
                hr = piFrameEncode->GetMetadataQueryWriter(&piFrameQWriter);
            }
            if (SUCCEEDED(hr))
            {
                // Add additional metadata.
                PROPVARIANT    value;
                value.vt = VT_LPWSTR;
                value.pwszVal= L"Metadata Test Image.";
                hr = piFrameQWriter->SetMetadataByName(L"/xmp/dc:title", &value);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->WriteSource(
                    static_cast<IWICBitmapSource*> (piFrameDecode),
                    NULL); // Using NULL enables JPEG loss-less encoding.
            }

            // Commit the frame.
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->Commit();
            }

            if (piFrameDecode)
            {
                piFrameDecode->Release();
            }

            if (piFrameEncode)
            {
                piFrameEncode->Release();
            }

            if (piFrameQReader)
            {
                piFrameQReader->Release();
            }

            if (piFrameQWriter)
            {
                piFrameQWriter->Release();
            }
        }
    }

    if (SUCCEEDED(hr))
    {
        piEncoder->Commit();
    }

    if (SUCCEEDED(hr))
    {
        piFileStream->Commit(STGC_DEFAULT);
    }

    if (piFileStream)
    {
        piFileStream->Release();
    }
    if (piEncoder)
    {
        piEncoder->Release();
    }
    if (piBlockWriter)
    {
        piBlockWriter->Release();
    }
    if (piBlockReader)
    {
        piBlockReader->Release();
    }
    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="9c264-168">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9c264-168">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="9c264-169">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="9c264-169">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9c264-170">Cenni preliminari sui metadati WIC</span><span class="sxs-lookup"><span data-stu-id="9c264-170">WIC Metadata Overview</span></span>](-wic-about-metadata.md)
</dt> <dt>

[<span data-ttu-id="9c264-171">Cenni preliminari sul linguaggio di query dei metadati</span><span class="sxs-lookup"><span data-stu-id="9c264-171">Metadata Query Language Overview</span></span>](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[<span data-ttu-id="9c264-172">Panoramica della lettura e della scrittura dei metadati delle immagini</span><span class="sxs-lookup"><span data-stu-id="9c264-172">Overview of Reading and Writing Image Metadata</span></span>](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[<span data-ttu-id="9c264-173">Panoramica dell'estendibilità dei metadati</span><span class="sxs-lookup"><span data-stu-id="9c264-173">Metadata Extensibility Overview</span></span>](-wic-codec-metadatahandlers.md)
</dt> </dl>

 

 
