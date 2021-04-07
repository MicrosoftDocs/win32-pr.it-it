---
description: Acquisizione di un'immagine da un PIN dell'immagine ancora
ms.assetid: cbcb4d6d-dc85-4ae2-b0a8-110f15092733
title: Acquisizione di un'immagine da un PIN dell'immagine ancora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3510f318f3107dd698dc753704d6c09d70ddd308
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746087"
---
# <a name="capturing-an-image-from-a-still-image-pin"></a>Acquisizione di un'immagine da un PIN dell'immagine ancora

Alcune fotocamere possono produrre un'immagine ancora separata dal flusso di acquisizione e spesso l'immagine ancora è di qualità superiore rispetto alle immagini prodotte dal flusso di acquisizione. La fotocamera potrebbe avere un pulsante che funge da trigger hardware oppure può supportare l'attivazione del software. Una fotocamera che supporta le immagini ancora esporrà un PIN dell'immagine ancora, che è ancora una categoria pin della categoria pin \_ \_ .

Il modo consigliato per ottenere immagini ancora dal dispositivo consiste nell'usare le API di acquisizione immagini Windows (WIA). Per ulteriori informazioni, vedere la sezione relativa all'acquisizione di immagini Windows nella documentazione di Platform SDK. Tuttavia, è anche possibile usare DirectShow per acquisire un'immagine.

Per attivare il pin ancora, usare il metodo [**IAMVideoControl:: semode**](/windows/desktop/api/Strmif/nf-strmif-iamvideocontrol-setmode) quando il grafico è in esecuzione, come indicato di seguito:


```C++
IAMVideoControl *pAMVidControl = NULL;

hr = pControl->Run(); // Run the graph.
if (FAILED(hr))
{
    // Handle error.
}

hr = pCap->QueryInterface(IID_IAMVideoControl, (void**)&pAMVidControl);

if (SUCCEEDED(hr))
{
    // Find the still pin.
    IPin *pPin = NULL;

    // pBuild is an ICaptureGraphBuilder2 pointer.

    hr = pBuild->FindPin(
        pCap,                  // Filter.
        PINDIR_OUTPUT,         // Look for an output pin.
        &PIN_CATEGORY_STILL,   // Pin category.
        NULL,                  // Media type (don't care).
        FALSE,                 // Pin must be unconnected.
        0,                     // Get the 0'th pin.
        &pPin                  // Receives a pointer to thepin.
        );

    if (SUCCEEDED(hr))
    {
        hr = pAMVidControl->SetMode(pPin, VideoControlFlag_Trigger);
        pPin->Release();
    }
    pAMVidControl->Release();
}
```



Eseguire una query sul filtro di acquisizione per [**IAMVideoControl**](/windows/desktop/api/Strmif/nn-strmif-iamvideocontrol). Se l'interfaccia è supportata, ottenere un puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN ancora chiamando il metodo [**ICaptureGraphBuilder2:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) , come illustrato nell'esempio precedente. Chiamare quindi [**IAMVideoControl:: semode**](/windows/desktop/api/Strmif/nf-strmif-iamvideocontrol-setmode) con il puntatore **Ipin** e il \_ flag di attivazione VideoControlFlag.

> [!Note]  
> A seconda della fotocamera, potrebbe essere necessario eseguire il rendering del PIN di acquisizione ( \_ acquisizione della categoria pin \_ ) prima che il pin ancora si connetta.

 

### <a name="example-using-the-sample-grabber-filter"></a>Esempio: uso del filtro Grabber di esempio

Un modo per acquisire l'immagine è con il filtro [**grabber di esempio**](sample-grabber-filter.md) . Il grabber di esempio usa una funzione di callback definita dall'applicazione per elaborare l'immagine. Per altre informazioni sul filtro Grabber di esempio, vedere [uso del grabber di esempio](using-the-sample-grabber.md).

Nell'esempio seguente si presuppone che il Pin Still fornisca un'immagine RGB non compressa. In primo luogo, definire una classe che implementerà l'interfaccia di callback del grabber di esempio, [**ISampleGrabberCB**](isamplegrabbercb.md):


```C++
// Class to hold the callback function for the Sample Grabber filter.
class SampleGrabberCallback : public ISampleGrabberCB
{
    // Implementation is described later.
}

// Global instance of the class.
SampleGrabberCallback g_StillCapCB;
```



L'implementazione della classe verrà descritta a breve.

A questo punto, connettere il Pin Still al grabber di esempio e connettere il grabber di esempio al filtro [**renderer null**](null-renderer-filter.md) . Il renderer NULL elimina semplicemente gli esempi di supporti ricevuti; il lavoro effettivo verrà eseguito all'interno del callback. (L'unico motivo per cui il renderer null consiste nel connettere il pin di output di Sample Grabber a un elemento). Chiamare [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) per creare i filtri di esempio grabber e renderer null e chiamare [**IFilterGraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) per aggiungere entrambi i filtri al grafo:


```C++
// Add the Sample Grabber filter to the graph.
IBaseFilter *pSG_Filter;
hr = CoCreateInstance(
    CLSID_SampleGrabber, 
    NULL, 
    CLSCTX_INPROC_SERVER,
    IID_IBaseFilter, 
    (void**)&pSG_Filter
    );

hr = pGraph->AddFilter(pSG_Filter, L"SampleGrab");

// Add the Null Renderer filter to the graph.
IBaseFilter *pNull;

hr = CoCreateInstance(
    CLSID_NullRenderer, 
    NULL, 
    CLSCTX_INPROC_SERVER,
    IID_IBaseFilter, 
    (void**)&pNull
    );

hr = pGraph->AddFilter(pNull, L"NullRender");
```



È possibile usare il metodo [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) per connettere tutti e tre i filtri in una chiamata al metodo, passando dal pin continuo al grabber di esempio e dal grabber di esempio al renderer null:


```C++
hr = pBuild->RenderStream(
    &PIN_CATEGORY_STILL, // Connect this pin ...
    &MEDIATYPE_Video,    // with this media type ...
    pCap,                // on this filter ...
    pSG_Filter,          // to the Sample Grabber ...
    pNull);              // ... and finally to the Null Renderer.
```



Usare ora l'interfaccia [**ISampleGrabber**](isamplegrabber.md) per configurare il grabber di esempio in modo da memorizzare nel buffer gli esempi:


```C++
// Configure the Sample Grabber.
ISampleGrabber *pSG = NULL;

hr = pSG_Filter->QueryInterface(IID_ISampleGrabber, (void**)&pSG);
if (SUCCEEDED(hr))
{
    hr = pSG->SetOneShot(FALSE);
    hr = pSG->SetBufferSamples(TRUE);

    ...
```



Impostare l'interfaccia di callback con un puntatore all'oggetto callback:


```C++
hr = pSG->SetCallback(&g_StillCapCB, 0); // 0 = Use the SampleCB callback method.
```



Ottenere il tipo di supporto usato dal pin per connettersi con il grabber di esempio:


```C++
// Store the media type for later use.
AM_MEDIA_TYPE g_StillMediaType;

hr = pSG->GetConnectedMediaType(&g_StillMediaType);
pSG->Release();
```



Questo tipo di supporto conterrà la struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) che definisce il formato dell'immagine ancora. Liberare il tipo di supporto prima della chiusura dell'applicazione:


```C++
// On exit, remember to release the media type.
FreeMediaType(g_StillMediaType);
```



Di seguito è riportato un esempio della classe di callback. Si noti che la classe implementa **IUnknown**, che eredita tramite l'interfaccia [**ISampleGrabber**](isamplegrabber.md) , ma non mantiene un conteggio dei riferimenti. Questo è sicuro perché l'applicazione crea l'oggetto nello stack e l'oggetto rimane nell'ambito per tutta la durata del grafico di filtro.

Tutto il lavoro si verifica nel metodo [**BufferCB**](isamplegrabbercb-buffercb.md) , che viene chiamato dal grabber di esempio ogni volta che viene ottenuto un nuovo esempio. Nell'esempio seguente il metodo scrive la bitmap in un file:


```C++
class SampleGrabberCallback : public ISampleGrabberCB
{
public:
    // Fake referance counting.
    STDMETHODIMP_(ULONG) AddRef() { return 1; }
    STDMETHODIMP_(ULONG) Release() { return 2; }

    STDMETHODIMP QueryInterface(REFIID riid, void **ppvObject)
    {
        if (NULL == ppvObject) return E_POINTER;
        if (riid == __uuidof(IUnknown))
        {
            *ppvObject = static_cast<IUnknown*>(this);
             return S_OK;
        }
        if (riid == __uuidof(ISampleGrabberCB))
        {
            *ppvObject = static_cast<ISampleGrabberCB*>(this);
             return S_OK;
        }
        return E_NOTIMPL;
    }

    STDMETHODIMP SampleCB(double Time, IMediaSample *pSample)
    {
        return E_NOTIMPL;
    }

    STDMETHODIMP BufferCB(double Time, BYTE *pBuffer, long BufferLen)
    {
        if ((g_StillMediaType.majortype != MEDIATYPE_Video) ||
            (g_StillMediaType.formattype != FORMAT_VideoInfo) ||
            (g_StillMediaType.cbFormat < sizeof(VIDEOINFOHEADER)) ||
            (g_StillMediaType.pbFormat == NULL))
        {
            return VFW_E_INVALIDMEDIATYPE;
        }
        HANDLE hf = CreateFile("C:\\Example.bmp", GENERIC_WRITE, 
        FILE_SHARE_WRITE, NULL, CREATE_ALWAYS, 0, NULL);
        if (hf == INVALID_HANDLE_VALUE)
        {
            return E_FAIL;
        }
        long cbBitmapInfoSize = g_StillMediaType.cbFormat - SIZE_PREHEADER;
        VIDEOINFOHEADER *pVideoHeader =
           (VIDEOINFOHEADER*)g_StillMediaType.pbFormat;

        BITMAPFILEHEADER bfh;
        ZeroMemory(&bfh, sizeof(bfh));
        bfh.bfType = 'MB';  // Little-endian for "BM".
        bfh.bfSize = sizeof( bfh ) + BufferLen + cbBitmapInfoSize;
        bfh.bfOffBits = sizeof( BITMAPFILEHEADER ) + cbBitmapInfoSize;
        
        // Write the file header.
        DWORD dwWritten = 0;
        WriteFile( hf, &bfh, sizeof( bfh ), &dwWritten, NULL );
        WriteFile(hf, HEADER(pVideoHeader), cbBitmapInfoSize, &dwWritten, NULL);        
        WriteFile( hf, pBuffer, BufferLen, &dwWritten, NULL );
        CloseHandle( hf );
        return S_OK;

    }
};
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività di acquisizione video](video-capture-tasks.md)
</dt> </dl>

 

 
