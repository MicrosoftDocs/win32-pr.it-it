---
description: Questa esercitazione usa Sink Writer per codificare un file video.
ms.assetid: 3E297366-0863-4E89-A0D5-438CD1FC5AF9
title: 'Esercitazione: Uso del sink writer per codificare il video'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5347a82fd40355c8006b15492a59543018ae5868cb02fcefeeb1812bd26930c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972780"
---
# <a name="tutorial-using-the-sink-writer-to-encode-video"></a>Esercitazione: Uso del sink writer per codificare il video

Questa esercitazione usa [Sink Writer per](sink-writer.md) codificare un file video.

## <a name="define-the-video-format"></a>Definire il formato video

Per semplicità, questa esercitazione usa un formato video fisso, definito dalle costanti seguenti:


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



Queste costanti specificano i parametri seguenti del formato video:

-   Dimensioni del frame (larghezza e altezza)
-   Fotogrammi al secondo.
-   Velocità in bit codificata.
-   Formato di codifica, che Windows Media Video 9 (**MFVideoFormat \_ WMV3**).
-   Formato di input, ovvero RGB a 32 bit.
-   Durata del file di output.

Il programma usa queste costanti per creare i tipi di supporti che descrivono il formato. In un'applicazione reale si supporterebbe in genere una gamma di profili di codifica.

## <a name="create-an-uncompressed-video-frame"></a>Creare un fotogramma video non compresso

Anche per semplicità, questa esercitazione usa un frame video statico come input. Il fotogramma video contiene un rettangolo verde a tinta unita e viene generato a livello di codice. Il fotogramma video viene archiviato in una variabile globale come matrice **di DWORD:**


```C++
// Buffer to hold the video frame data.
DWORD videoFrameBuffer[VIDEO_PELS];
```



Il codice seguente imposta ogni pixel del frame su verde:


```C++
    // Set all pixels to green
    for (DWORD i = 0; i < VIDEO_PELS; ++i)
    {
        videoFrameBuffer[i] = 0x0000FF00;
    }
```



## <a name="initialize-the-sink-writer"></a>Inizializzare il writer di sink

Per inizializzare il writer di sink, seguire questa procedura.

1.  Chiamare [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) per creare una nuova istanza del writer di sink.
2.  Creare un tipo di supporto che descrive il video codificato.
3.  Passare questo tipo di supporto al [**metodo IMFSinkWriter::AddStream.**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-addstream)
4.  Creare un secondo tipo di supporto che descrive l'input non compresso.
5.  Passare il tipo di supporto non compresso al [**metodo IMFSinkWriter::SetInputMediaType.**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-setinputmediatype)
6.  Chiamare il [**metodo IMFSinkWriter::BeginWriting.**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-beginwriting)
7.  Il writer di sink è ora pronto per accettare esempi di input.

Il codice seguente illustra questi passaggi.


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



La maggior parte dei passaggi nell'esempio di codice precedente è l'impostazione degli attributi del tipo di supporto per i due tipi di supporti. I dettagli dei tipi di supporti dipendono dal contenuto di origine e dal profilo di codifica desiderato.

## <a name="send-video-frames-to-the-sink-writer"></a>Inviare fotogrammi video al sink writer

Per inviare un fotogramma video al writer di sink, chiamare il [**metodo IMFSinkWriter::WriteSample.**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) Il **metodo WriteSample** accetta un puntatore all'interfaccia [**IMFSample,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) che rappresenta un *oggetto di esempio multimediale.* L'esempio multimediale contiene *un oggetto buffer* multimediale, che a sua volta contiene un puntatore al fotogramma video. Per altre informazioni sugli esempi di supporti e sul buffer, vedere gli argomenti seguenti.

-   [Esempi di supporti](media-samples.md)
-   [Buffer multimediali](media-buffers.md)

A seconda dell'applicazione, è possibile ottenere gli esempi di supporti da [Source Reader.](source-reader.md) In alternativa, è possibile creare gli esempi di supporti e modificare direttamente i dati nel buffer. Il codice seguente illustra il secondo approccio. Crea un buffer di memoria e scrive un singolo fotogramma video nel buffer. Quindi aggiunge il buffer a un campione di supporti e invia l'esempio multimediale al writer di sink.


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



Questo codice esegue i passaggi seguenti.

1.  Chiamare [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) per creare un oggetto buffer multimediale. Questa funzione alloca la memoria per il buffer.
2.  Chiamare [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) per bloccare il buffer e ottenere un puntatore alla memoria.
3.  Chiamare [**MFCopyImage**](/windows/desktop/api/mfapi/nf-mfapi-mfcopyimage) per copiare il fotogramma video nel buffer.
    > [!Note]  
    > In questo esempio specifico, anche **l'uso di memcpy** funziona. Tuttavia, la [**funzione MFCopyImage**](/windows/desktop/api/mfapi/nf-mfapi-mfcopyimage) gestisce correttamente il caso in cui lo stride dell'immagine di origine non corrisponde al buffer di destinazione. Per altre informazioni, vedere [Image Stride](image-stride.md).

     

4.  Chiamare [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) per sbloccare il buffer.
5.  Chiamare [**IMFMediaBuffer::SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength) per aggiornare la lunghezza dei dati validi nel buffer. In caso contrario, il valore predefinito è zero.
6.  Chiamare [**MFCreateSample**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatesample) per creare un oggetto di esempio multimediale.
7.  Chiamare [**IMFSample::AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer) per aggiungere il buffer multimediale all'esempio multimediale.
8.  Chiamare [**IMFSample::SetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime) per impostare il timestamp per il fotogramma video.
9.  Chiamare [**IMFSample::SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration) per impostare la durata del fotogramma video.
10. Chiamare [**IMFSinkWriter::WriteSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) per inviare l'esempio multimediale al writer di sink.

## <a name="write-the-main-function"></a>Scrivere la funzione main

`main`All'interno della funzione seguire questa procedura.

1.  Chiamare [**CoInitializeEx per**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) inizializzare la libreria COM.
2.  Chiamare [**MFStartup per**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) inizializzare Microsoft Media Foundation.
3.  Creare il writer di sink.
4.  Inviare fotogrammi video al writer di sink.
5.  Chiamare [**IMFSinkWriter::Finalize per**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-finalize) finalizzare il file di output.
6.  Rilasciare il puntatore al writer di sink.
7.  Chiamare [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).
8.  Chiamare [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).


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



## <a name="example-code"></a>Codice di esempio

Il codice seguente illustra il programma completo.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sink Writer](sink-writer.md)
</dt> </dl>

 

 
