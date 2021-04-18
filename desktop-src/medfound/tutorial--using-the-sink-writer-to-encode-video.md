---
description: Questa esercitazione usa il writer di sink per codificare un file video.
ms.assetid: 3E297366-0863-4E89-A0D5-438CD1FC5AF9
title: 'Esercitazione: uso del writer di sink per codificare video'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a3e6095355e18db6c8335cadcbc4afc56b35406
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310186"
---
# <a name="tutorial-using-the-sink-writer-to-encode-video"></a><span data-ttu-id="8e90b-103">Esercitazione: uso del writer di sink per codificare video</span><span class="sxs-lookup"><span data-stu-id="8e90b-103">Tutorial: Using the Sink Writer to Encode Video</span></span>

<span data-ttu-id="8e90b-104">Questa esercitazione usa il [writer di sink](sink-writer.md) per codificare un file video.</span><span class="sxs-lookup"><span data-stu-id="8e90b-104">This tutorial uses the [Sink Writer](sink-writer.md) to encode a video file.</span></span>

## <a name="define-the-video-format"></a><span data-ttu-id="8e90b-105">Definire il formato video</span><span class="sxs-lookup"><span data-stu-id="8e90b-105">Define the Video Format</span></span>

<span data-ttu-id="8e90b-106">Per semplicità, in questa esercitazione viene usato un formato video fisso, definito dalle costanti seguenti:</span><span class="sxs-lookup"><span data-stu-id="8e90b-106">For simplicity, this tutorial uses a fixed video format, defined by the following constants:</span></span>


```C++
// Format constants
const UINT32 VIDEO_WIDTH = 640;
const UINT32 VIDEO_HEIGHT = 480;
const UINT32 VIDEO_FPS = 30;
const UINT64 VIDEO_FRAME_DURATION = 10 * 1000 * 1000 / VIDEO_FPS;
const UINT32 VIDEO_BIT_RATE = 800000;
const GUID   VIDEO_ENCODING_FORMAT = MFVideoFormat_WMV3;
const GUID   VIDEO_INPUT_FORMAT = MFVideoFormat_RGB32;
const UINT32 VIDEO_PELS = VIDEO_WIDTH * VIDEO_HEIGHT;
const UINT32 VIDEO_FRAME_COUNT = 20 * VIDEO_FPS;
```



<span data-ttu-id="8e90b-107">Queste costanti specificano i parametri seguenti del formato video:</span><span class="sxs-lookup"><span data-stu-id="8e90b-107">These constants specify the following parameters of the video format:</span></span>

-   <span data-ttu-id="8e90b-108">Dimensioni fotogramma (larghezza e altezza)</span><span class="sxs-lookup"><span data-stu-id="8e90b-108">Frame size (width and height)</span></span>
-   <span data-ttu-id="8e90b-109">Fotogrammi al secondo.</span><span class="sxs-lookup"><span data-stu-id="8e90b-109">Frames per second.</span></span>
-   <span data-ttu-id="8e90b-110">Velocità in bit codificata.</span><span class="sxs-lookup"><span data-stu-id="8e90b-110">Encoded bit rate.</span></span>
-   <span data-ttu-id="8e90b-111">Formato di codifica, che è Windows Media Video 9 (**MFVideoFormat \_ WMV3**).</span><span class="sxs-lookup"><span data-stu-id="8e90b-111">Encoding format, which is Windows Media Video 9 (**MFVideoFormat\_WMV3**).</span></span>
-   <span data-ttu-id="8e90b-112">Formato di input, ovvero RGB a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="8e90b-112">Input format, which is 32-bit RGB.</span></span>
-   <span data-ttu-id="8e90b-113">Durata del file di output.</span><span class="sxs-lookup"><span data-stu-id="8e90b-113">Duration of the output file.</span></span>

<span data-ttu-id="8e90b-114">Il programma usa queste costanti per creare i tipi di supporto che descrivono il formato.</span><span class="sxs-lookup"><span data-stu-id="8e90b-114">The program uses these constants to create the media types that describe the format.</span></span> <span data-ttu-id="8e90b-115">In un'applicazione reale, in genere è supportato un intervallo di profili di codifica.</span><span class="sxs-lookup"><span data-stu-id="8e90b-115">In a real application, you would typically support a range of encoding profiles.</span></span>

## <a name="create-an-uncompressed-video-frame"></a><span data-ttu-id="8e90b-116">Creazione di un frame video non compresso</span><span class="sxs-lookup"><span data-stu-id="8e90b-116">Create an Uncompressed Video Frame</span></span>

<span data-ttu-id="8e90b-117">Inoltre, per semplicità, in questa esercitazione viene usato un frame video statico come input.</span><span class="sxs-lookup"><span data-stu-id="8e90b-117">Also for simplicity, this tutorial uses a static video frame as input.</span></span> <span data-ttu-id="8e90b-118">Il fotogramma video contiene un rettangolo verde a tinta unita e viene generato a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="8e90b-118">The video frame contains a solid green rectangle and is generated programmatically.</span></span> <span data-ttu-id="8e90b-119">Il fotogramma video viene archiviato in una variabile globale come una matrice di **DWORD** s:</span><span class="sxs-lookup"><span data-stu-id="8e90b-119">The video frame is stored in a global variable as an array of **DWORD** s:</span></span>


```C++
// Buffer to hold the video frame data.
DWORD videoFrameBuffer[VIDEO_PELS];
```



<span data-ttu-id="8e90b-120">Il codice seguente imposta ogni pixel del frame su verde:</span><span class="sxs-lookup"><span data-stu-id="8e90b-120">The following code sets every pixel in the frame to green:</span></span>


```C++
    // Set all pixels to green
    for (DWORD i = 0; i < VIDEO_PELS; ++i)
    {
        videoFrameBuffer[i] = 0x0000FF00;
    }
```



## <a name="initialize-the-sink-writer"></a><span data-ttu-id="8e90b-121">Inizializzare il writer di sink</span><span class="sxs-lookup"><span data-stu-id="8e90b-121">Initialize the Sink Writer</span></span>

<span data-ttu-id="8e90b-122">Per inizializzare il writer di sink, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="8e90b-122">To initialize the sink writer, perform the following steps.</span></span>

1.  <span data-ttu-id="8e90b-123">Chiamare [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) per creare una nuova istanza del writer del sink.</span><span class="sxs-lookup"><span data-stu-id="8e90b-123">Call [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) to create a new instance of the sink writer.</span></span>
2.  <span data-ttu-id="8e90b-124">Creare un tipo di supporto che descriva il video codificato.</span><span class="sxs-lookup"><span data-stu-id="8e90b-124">Create a media type that describes the encoded video.</span></span>
3.  <span data-ttu-id="8e90b-125">Passare questo tipo di supporto al metodo [**IMFSinkWriter:: AddStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-addstream) .</span><span class="sxs-lookup"><span data-stu-id="8e90b-125">Pass this media type to the [**IMFSinkWriter::AddStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-addstream) method.</span></span>
4.  <span data-ttu-id="8e90b-126">Creare un secondo tipo di supporto che descriva l'input non compresso.</span><span class="sxs-lookup"><span data-stu-id="8e90b-126">Create a second media type that describes the uncompressed input.</span></span>
5.  <span data-ttu-id="8e90b-127">Passare il tipo di supporto non compresso al metodo [**IMFSinkWriter:: SetInputMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-setinputmediatype) .</span><span class="sxs-lookup"><span data-stu-id="8e90b-127">Pass the uncompressed media type to the [**IMFSinkWriter::SetInputMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-setinputmediatype) method.</span></span>
6.  <span data-ttu-id="8e90b-128">Chiamare il metodo [**IMFSinkWriter:: BeginWriting**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-beginwriting) .</span><span class="sxs-lookup"><span data-stu-id="8e90b-128">Call the [**IMFSinkWriter::BeginWriting**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-beginwriting) method.</span></span>
7.  <span data-ttu-id="8e90b-129">Il writer di sink è ora pronto ad accettare gli esempi di input.</span><span class="sxs-lookup"><span data-stu-id="8e90b-129">The sink writer is now ready to accept input samples.</span></span>

<span data-ttu-id="8e90b-130">Nel codice seguente vengono illustrati questi passaggi.</span><span class="sxs-lookup"><span data-stu-id="8e90b-130">The following code shows these steps.</span></span>


```C++
HRESULT InitializeSinkWriter(IMFSinkWriter **ppWriter, DWORD *pStreamIndex)
{
    *ppWriter = NULL;
    *pStreamIndex = NULL;

    IMFSinkWriter   *pSinkWriter = NULL;
    IMFMediaType    *pMediaTypeOut = NULL;   
    IMFMediaType    *pMediaTypeIn = NULL;   
    DWORD           streamIndex;     

    HRESULT hr = MFCreateSinkWriterFromURL(L"output.wmv", NULL, NULL, &pSinkWriter);

    // Set the output media type.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMediaType(&pMediaTypeOut);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Video);     
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetGUID(MF_MT_SUBTYPE, VIDEO_ENCODING_FORMAT);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetUINT32(MF_MT_AVG_BITRATE, VIDEO_BIT_RATE);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetUINT32(MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeSize(pMediaTypeOut, MF_MT_FRAME_SIZE, VIDEO_WIDTH, VIDEO_HEIGHT);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeOut, MF_MT_FRAME_RATE, VIDEO_FPS, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeOut, MF_MT_PIXEL_ASPECT_RATIO, 1, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pSinkWriter->AddStream(pMediaTypeOut, &streamIndex);   
    }

    // Set the input media type.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMediaType(&pMediaTypeIn);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeIn->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Video);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeIn->SetGUID(MF_MT_SUBTYPE, VIDEO_INPUT_FORMAT);     
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeIn->SetUINT32(MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeSize(pMediaTypeIn, MF_MT_FRAME_SIZE, VIDEO_WIDTH, VIDEO_HEIGHT);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeIn, MF_MT_FRAME_RATE, VIDEO_FPS, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeIn, MF_MT_PIXEL_ASPECT_RATIO, 1, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pSinkWriter->SetInputMediaType(streamIndex, pMediaTypeIn, NULL);   
    }

    // Tell the sink writer to start accepting data.
    if (SUCCEEDED(hr))
    {
        hr = pSinkWriter->BeginWriting();
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppWriter = pSinkWriter;
        (*ppWriter)->AddRef();
        *pStreamIndex = streamIndex;
    }

    SafeRelease(&pSinkWriter);
    SafeRelease(&pMediaTypeOut);
    SafeRelease(&pMediaTypeIn);
    return hr;
}
```



<span data-ttu-id="8e90b-131">Nella maggior parte dei passaggi dell'esempio di codice precedente vengono impostate gli attributi del tipo di supporto per i due tipi di supporto.</span><span class="sxs-lookup"><span data-stu-id="8e90b-131">Most of the steps in previous code example are setting the media type attributes for the two media types.</span></span> <span data-ttu-id="8e90b-132">I dettagli dei tipi di supporto dipenderanno dal contenuto di origine e dal profilo di codifica desiderato.</span><span class="sxs-lookup"><span data-stu-id="8e90b-132">The details of the media types will depend on your source content and the desired encoding profile.</span></span>

## <a name="send-video-frames-to-the-sink-writer"></a><span data-ttu-id="8e90b-133">Inviare fotogrammi video al writer di sink</span><span class="sxs-lookup"><span data-stu-id="8e90b-133">Send Video Frames to the Sink Writer</span></span>

<span data-ttu-id="8e90b-134">Per inviare un frame video al writer di sink, chiamare il metodo [**IMFSinkWriter:: WriteSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) .</span><span class="sxs-lookup"><span data-stu-id="8e90b-134">To send a video frame to the sink writer, call the [**IMFSinkWriter::WriteSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) method.</span></span> <span data-ttu-id="8e90b-135">Il metodo **WriteSample** accetta un puntatore all'interfaccia [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , che rappresenta un oggetto di *esempio multimediale* .</span><span class="sxs-lookup"><span data-stu-id="8e90b-135">The **WriteSample** method takes a pointer to the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, which represents a *media sample* object.</span></span> <span data-ttu-id="8e90b-136">L'esempio multimediale contiene un oggetto *buffer multimediale* , che a sua volta contiene un puntatore al frame video.</span><span class="sxs-lookup"><span data-stu-id="8e90b-136">The media sample contains a *media buffer* object, which in turn contains a pointer to the video frame.</span></span> <span data-ttu-id="8e90b-137">Per ulteriori informazioni sugli esempi di supporti e sul buffer, vedere gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="8e90b-137">For more information about media samples and buffer, see the following topics.</span></span>

-   [<span data-ttu-id="8e90b-138">Esempi di supporti</span><span class="sxs-lookup"><span data-stu-id="8e90b-138">Media Samples</span></span>](media-samples.md)
-   [<span data-ttu-id="8e90b-139">Buffer multimediali</span><span class="sxs-lookup"><span data-stu-id="8e90b-139">Media Buffers</span></span>](media-buffers.md)

<span data-ttu-id="8e90b-140">A seconda dell'applicazione, è possibile ottenere gli esempi di supporti dal [lettore di origine](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="8e90b-140">Depending on your application, you might get the media samples from the [Source Reader](source-reader.md).</span></span> <span data-ttu-id="8e90b-141">In alternativa, è possibile creare gli esempi di supporti e modificare direttamente i dati nel buffer.</span><span class="sxs-lookup"><span data-stu-id="8e90b-141">Alternatively, you can create the media samples and directly manipulate the data in the buffer.</span></span> <span data-ttu-id="8e90b-142">Il codice seguente illustra il secondo approccio.</span><span class="sxs-lookup"><span data-stu-id="8e90b-142">The following code shows the second approach.</span></span> <span data-ttu-id="8e90b-143">Viene creato un buffer di memoria e viene scritto un singolo frame video nel buffer.</span><span class="sxs-lookup"><span data-stu-id="8e90b-143">It creates a memory buffer and writes a single video frame to the buffer.</span></span> <span data-ttu-id="8e90b-144">Aggiunge quindi il buffer a un esempio di supporto e invia l'esempio multimediale al writer del sink.</span><span class="sxs-lookup"><span data-stu-id="8e90b-144">Then it adds that buffer to a media sample, and sends the media sample to the sink writer.</span></span>


```C++
HRESULT WriteFrame(
    IMFSinkWriter *pWriter, 
    DWORD streamIndex, 
    const LONGLONG& rtStart        // Time stamp.
    )
{
    IMFSample *pSample = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    const LONG cbWidth = 4 * VIDEO_WIDTH;
    const DWORD cbBuffer = cbWidth * VIDEO_HEIGHT;

    BYTE *pData = NULL;

    // Create a new memory buffer.
    HRESULT hr = MFCreateMemoryBuffer(cbBuffer, &pBuffer);

    // Lock the buffer and copy the video frame to the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->Lock(&pData, NULL, NULL);
    }
    if (SUCCEEDED(hr))
    {
        hr = MFCopyImage(
            pData,                      // Destination buffer.
            cbWidth,                    // Destination stride.
            (BYTE*)videoFrameBuffer,    // First row in source image.
            cbWidth,                    // Source stride.
            cbWidth,                    // Image width in bytes.
            VIDEO_HEIGHT                // Image height in pixels.
            );
    }
    if (pBuffer)
    {
        pBuffer->Unlock();
    }

    // Set the data length of the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbBuffer);
    }

    // Create a media sample and add the buffer to the sample.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateSample(&pSample);
    }
    if (SUCCEEDED(hr))
    {
        hr = pSample->AddBuffer(pBuffer);
    }

    // Set the time stamp and the duration.
    if (SUCCEEDED(hr))
    {
        hr = pSample->SetSampleTime(rtStart);
    }
    if (SUCCEEDED(hr))
    {
        hr = pSample->SetSampleDuration(VIDEO_FRAME_DURATION);
    }

    // Send the sample to the Sink Writer.
    if (SUCCEEDED(hr))
    {
        hr = pWriter->WriteSample(streamIndex, pSample);
    }

    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}
```



<span data-ttu-id="8e90b-145">Questo codice esegue i passaggi seguenti.</span><span class="sxs-lookup"><span data-stu-id="8e90b-145">This code performs the following steps.</span></span>

1.  <span data-ttu-id="8e90b-146">Chiamare [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) per creare un oggetto buffer multimediale.</span><span class="sxs-lookup"><span data-stu-id="8e90b-146">Call [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) to create a media buffer object.</span></span> <span data-ttu-id="8e90b-147">Questa funzione alloca la memoria per il buffer.</span><span class="sxs-lookup"><span data-stu-id="8e90b-147">This function allocates the memory for the buffer.</span></span>
2.  <span data-ttu-id="8e90b-148">Chiamare [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) per bloccare il buffer e ottenere un puntatore alla memoria.</span><span class="sxs-lookup"><span data-stu-id="8e90b-148">Call [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) to lock the buffer and get a pointer to the memory.</span></span>
3.  <span data-ttu-id="8e90b-149">Chiamare [**MFCopyImage**](/windows/desktop/api/mfapi/nf-mfapi-mfcopyimage) per copiare il frame video nel buffer.</span><span class="sxs-lookup"><span data-stu-id="8e90b-149">Call [**MFCopyImage**](/windows/desktop/api/mfapi/nf-mfapi-mfcopyimage) to copy the video frame into the buffer.</span></span>
    > [!Note]  
    > <span data-ttu-id="8e90b-150">In questo particolare esempio l'uso di **memcpy** potrebbe funzionare anche in questo modo.</span><span class="sxs-lookup"><span data-stu-id="8e90b-150">In this particular example, using **memcpy** would work just as well.</span></span> <span data-ttu-id="8e90b-151">Tuttavia, la funzione [**MFCopyImage**](/windows/desktop/api/mfapi/nf-mfapi-mfcopyimage) gestisce correttamente il caso in cui lo stride dell'immagine di origine non corrisponde al buffer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8e90b-151">However, the [**MFCopyImage**](/windows/desktop/api/mfapi/nf-mfapi-mfcopyimage) function correctly handles the case where the stride of the source image does not match the target buffer.</span></span> <span data-ttu-id="8e90b-152">Per ulteriori informazioni, vedere [Image stride](image-stride.md).</span><span class="sxs-lookup"><span data-stu-id="8e90b-152">For more information, see [Image Stride](image-stride.md).</span></span>

     

4.  <span data-ttu-id="8e90b-153">Chiamare [**IMFMediaBuffer:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) per sbloccare il buffer.</span><span class="sxs-lookup"><span data-stu-id="8e90b-153">Call [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) to unlock the buffer.</span></span>
5.  <span data-ttu-id="8e90b-154">Chiamare [**IMFMediaBuffer:: SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength) per aggiornare la lunghezza dei dati validi nel buffer.</span><span class="sxs-lookup"><span data-stu-id="8e90b-154">Call [**IMFMediaBuffer::SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength) to update the length of the valid data in the buffer.</span></span> <span data-ttu-id="8e90b-155">In caso contrario, il valore predefinito è zero.</span><span class="sxs-lookup"><span data-stu-id="8e90b-155">(Otherwise, this value defaults to zero.)</span></span>
6.  <span data-ttu-id="8e90b-156">Chiamare [**MFCreateSample**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatesample) per creare un oggetto di esempio multimediale.</span><span class="sxs-lookup"><span data-stu-id="8e90b-156">Call [**MFCreateSample**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatesample) to create a media sample object.</span></span>
7.  <span data-ttu-id="8e90b-157">Chiamare [**IMFSample:: AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer) per aggiungere il buffer multimediale all'esempio multimediale.</span><span class="sxs-lookup"><span data-stu-id="8e90b-157">Call [**IMFSample::AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer) to add the media buffer to the media sample.</span></span>
8.  <span data-ttu-id="8e90b-158">Chiamare [**IMFSample:: SetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime) per impostare il timestamp per il frame del video.</span><span class="sxs-lookup"><span data-stu-id="8e90b-158">Call [**IMFSample::SetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime) to set the time stamp for the video frame.</span></span>
9.  <span data-ttu-id="8e90b-159">Chiamare [**IMFSample:: SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration) per impostare la durata del fotogramma video.</span><span class="sxs-lookup"><span data-stu-id="8e90b-159">Call [**IMFSample::SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration) to set the duration of the video frame.</span></span>
10. <span data-ttu-id="8e90b-160">Chiamare [**IMFSinkWriter:: WriteSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) per inviare l'esempio multimediale al writer del sink.</span><span class="sxs-lookup"><span data-stu-id="8e90b-160">Call [**IMFSinkWriter::WriteSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) to send the media sample to the sink writer.</span></span>

## <a name="write-the-main-function"></a><span data-ttu-id="8e90b-161">Scrivere la funzione Main</span><span class="sxs-lookup"><span data-stu-id="8e90b-161">Write the main Function</span></span>

<span data-ttu-id="8e90b-162">All'interno della `main` funzione, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="8e90b-162">Inside the `main` function, perform the following steps.</span></span>

1.  <span data-ttu-id="8e90b-163">Chiamare [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) per inizializzare la libreria com.</span><span class="sxs-lookup"><span data-stu-id="8e90b-163">Call [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) to initialize the COM library.</span></span>
2.  <span data-ttu-id="8e90b-164">Chiamare [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) per inizializzare Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="8e90b-164">Call [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) to initialize Microsoft Media Foundation.</span></span>
3.  <span data-ttu-id="8e90b-165">Creare il writer del sink.</span><span class="sxs-lookup"><span data-stu-id="8e90b-165">Create the sink writer.</span></span>
4.  <span data-ttu-id="8e90b-166">Inviare fotogrammi video al writer del sink.</span><span class="sxs-lookup"><span data-stu-id="8e90b-166">Send video frames to the sink writer.</span></span>
5.  <span data-ttu-id="8e90b-167">Chiamare [**IMFSinkWriter:: Finalize**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-finalize) per finalizzare il file di output.</span><span class="sxs-lookup"><span data-stu-id="8e90b-167">Call [**IMFSinkWriter::Finalize**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-finalize) to finalize the output file.</span></span>
6.  <span data-ttu-id="8e90b-168">Rilasciare il puntatore al writer del sink.</span><span class="sxs-lookup"><span data-stu-id="8e90b-168">Release the pointer to the sink writer.</span></span>
7.  <span data-ttu-id="8e90b-169">Chiamare [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span><span class="sxs-lookup"><span data-stu-id="8e90b-169">Call [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span></span>
8.  <span data-ttu-id="8e90b-170">Chiamare [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).</span><span class="sxs-lookup"><span data-stu-id="8e90b-170">Call [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).</span></span>


```C++
void main()
{
    // Set all pixels to green
    for (DWORD i = 0; i < VIDEO_PELS; ++i)
    {
        videoFrameBuffer[i] = 0x0000FF00;
    }

    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
    if (SUCCEEDED(hr))
    {
        hr = MFStartup(MF_VERSION);
        if (SUCCEEDED(hr))
        {
            IMFSinkWriter *pSinkWriter = NULL;
            DWORD stream;

            hr = InitializeSinkWriter(&pSinkWriter, &stream);
            if (SUCCEEDED(hr))
            {
                // Send frames to the sink writer.
                LONGLONG rtStart = 0;


                for (DWORD i = 0; i < VIDEO_FRAME_COUNT; ++i)
                {
                    hr = WriteFrame(pSinkWriter, stream, rtStart);
                    if (FAILED(hr))
                    {
                        break;
                    }
                    rtStart += VIDEO_FRAME_DURATION;
                }
            }
            if (SUCCEEDED(hr))
            {
                hr = pSinkWriter->Finalize();
            }
            SafeRelease(&pSinkWriter);
            MFShutdown();
        }
        CoUninitialize();
    }
}
```



## <a name="example-code"></a><span data-ttu-id="8e90b-171">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="8e90b-171">Example Code</span></span>

<span data-ttu-id="8e90b-172">Il codice seguente illustra il programma completo.</span><span class="sxs-lookup"><span data-stu-id="8e90b-172">The following code shows the complete program.</span></span>


```C++
#include <Windows.h>
#include <mfapi.h>
#include <mfidl.h>
#include <Mfreadwrite.h>
#include <mferror.h>

#pragma comment(lib, "mfreadwrite")
#pragma comment(lib, "mfplat")
#pragma comment(lib, "mfuuid")

template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}

// Format constants
const UINT32 VIDEO_WIDTH = 640;
const UINT32 VIDEO_HEIGHT = 480;
const UINT32 VIDEO_FPS = 30;
const UINT64 VIDEO_FRAME_DURATION = 10 * 1000 * 1000 / VIDEO_FPS;
const UINT32 VIDEO_BIT_RATE = 800000;
const GUID   VIDEO_ENCODING_FORMAT = MFVideoFormat_WMV3;
const GUID   VIDEO_INPUT_FORMAT = MFVideoFormat_RGB32;
const UINT32 VIDEO_PELS = VIDEO_WIDTH * VIDEO_HEIGHT;
const UINT32 VIDEO_FRAME_COUNT = 20 * VIDEO_FPS;

// Buffer to hold the video frame data.
DWORD videoFrameBuffer[VIDEO_PELS];

HRESULT InitializeSinkWriter(IMFSinkWriter **ppWriter, DWORD *pStreamIndex)
{
    *ppWriter = NULL;
    *pStreamIndex = NULL;

    IMFSinkWriter   *pSinkWriter = NULL;
    IMFMediaType    *pMediaTypeOut = NULL;   
    IMFMediaType    *pMediaTypeIn = NULL;   
    DWORD           streamIndex;     

    HRESULT hr = MFCreateSinkWriterFromURL(L"output.wmv", NULL, NULL, &pSinkWriter);

    // Set the output media type.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMediaType(&pMediaTypeOut);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Video);     
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetGUID(MF_MT_SUBTYPE, VIDEO_ENCODING_FORMAT);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetUINT32(MF_MT_AVG_BITRATE, VIDEO_BIT_RATE);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetUINT32(MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeSize(pMediaTypeOut, MF_MT_FRAME_SIZE, VIDEO_WIDTH, VIDEO_HEIGHT);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeOut, MF_MT_FRAME_RATE, VIDEO_FPS, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeOut, MF_MT_PIXEL_ASPECT_RATIO, 1, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pSinkWriter->AddStream(pMediaTypeOut, &streamIndex);   
    }

    // Set the input media type.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMediaType(&pMediaTypeIn);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeIn->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Video);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeIn->SetGUID(MF_MT_SUBTYPE, VIDEO_INPUT_FORMAT);     
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeIn->SetUINT32(MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeSize(pMediaTypeIn, MF_MT_FRAME_SIZE, VIDEO_WIDTH, VIDEO_HEIGHT);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeIn, MF_MT_FRAME_RATE, VIDEO_FPS, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeIn, MF_MT_PIXEL_ASPECT_RATIO, 1, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pSinkWriter->SetInputMediaType(streamIndex, pMediaTypeIn, NULL);   
    }

    // Tell the sink writer to start accepting data.
    if (SUCCEEDED(hr))
    {
        hr = pSinkWriter->BeginWriting();
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppWriter = pSinkWriter;
        (*ppWriter)->AddRef();
        *pStreamIndex = streamIndex;
    }

    SafeRelease(&pSinkWriter);
    SafeRelease(&pMediaTypeOut);
    SafeRelease(&pMediaTypeIn);
    return hr;
}

HRESULT WriteFrame(
    IMFSinkWriter *pWriter, 
    DWORD streamIndex, 
    const LONGLONG& rtStart        // Time stamp.
    )
{
    IMFSample *pSample = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    const LONG cbWidth = 4 * VIDEO_WIDTH;
    const DWORD cbBuffer = cbWidth * VIDEO_HEIGHT;

    BYTE *pData = NULL;

    // Create a new memory buffer.
    HRESULT hr = MFCreateMemoryBuffer(cbBuffer, &pBuffer);

    // Lock the buffer and copy the video frame to the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->Lock(&pData, NULL, NULL);
    }
    if (SUCCEEDED(hr))
    {
        hr = MFCopyImage(
            pData,                      // Destination buffer.
            cbWidth,                    // Destination stride.
            (BYTE*)videoFrameBuffer,    // First row in source image.
            cbWidth,                    // Source stride.
            cbWidth,                    // Image width in bytes.
            VIDEO_HEIGHT                // Image height in pixels.
            );
    }
    if (pBuffer)
    {
        pBuffer->Unlock();
    }

    // Set the data length of the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbBuffer);
    }

    // Create a media sample and add the buffer to the sample.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateSample(&pSample);
    }
    if (SUCCEEDED(hr))
    {
        hr = pSample->AddBuffer(pBuffer);
    }

    // Set the time stamp and the duration.
    if (SUCCEEDED(hr))
    {
        hr = pSample->SetSampleTime(rtStart);
    }
    if (SUCCEEDED(hr))
    {
        hr = pSample->SetSampleDuration(VIDEO_FRAME_DURATION);
    }

    // Send the sample to the Sink Writer.
    if (SUCCEEDED(hr))
    {
        hr = pWriter->WriteSample(streamIndex, pSample);
    }

    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}

void main()
{
    // Set all pixels to green
    for (DWORD i = 0; i < VIDEO_PELS; ++i)
    {
        videoFrameBuffer[i] = 0x0000FF00;
    }

    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
    if (SUCCEEDED(hr))
    {
        hr = MFStartup(MF_VERSION);
        if (SUCCEEDED(hr))
        {
            IMFSinkWriter *pSinkWriter = NULL;
            DWORD stream;

            hr = InitializeSinkWriter(&pSinkWriter, &stream);
            if (SUCCEEDED(hr))
            {
                // Send frames to the sink writer.
                LONGLONG rtStart = 0;


                for (DWORD i = 0; i < VIDEO_FRAME_COUNT; ++i)
                {
                    hr = WriteFrame(pSinkWriter, stream, rtStart);
                    if (FAILED(hr))
                    {
                        break;
                    }
                    rtStart += VIDEO_FRAME_DURATION;
                }
            }
            if (SUCCEEDED(hr))
            {
                hr = pSinkWriter->Finalize();
            }
            SafeRelease(&pSinkWriter);
            MFShutdown();
        }
        CoUninitialize();
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="8e90b-173">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8e90b-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e90b-174">Writer sink</span><span class="sxs-lookup"><span data-stu-id="8e90b-174">Sink Writer</span></span>](sink-writer.md)
</dt> </dl>

 

 
