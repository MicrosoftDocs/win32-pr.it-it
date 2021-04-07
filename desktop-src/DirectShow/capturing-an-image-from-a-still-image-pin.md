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
# <a name="capturing-an-image-from-a-still-image-pin"></a><span data-ttu-id="83bef-103">Acquisizione di un'immagine da un PIN dell'immagine ancora</span><span class="sxs-lookup"><span data-stu-id="83bef-103">Capturing an Image From a Still Image Pin</span></span>

<span data-ttu-id="83bef-104">Alcune fotocamere possono produrre un'immagine ancora separata dal flusso di acquisizione e spesso l'immagine ancora è di qualità superiore rispetto alle immagini prodotte dal flusso di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="83bef-104">Some cameras can produce a still image separate from the capture stream, and often the still image is of higher quality than the images produced by the capture stream.</span></span> <span data-ttu-id="83bef-105">La fotocamera potrebbe avere un pulsante che funge da trigger hardware oppure può supportare l'attivazione del software.</span><span class="sxs-lookup"><span data-stu-id="83bef-105">The camera may have a button that acts as a hardware trigger, or it may support software triggering.</span></span> <span data-ttu-id="83bef-106">Una fotocamera che supporta le immagini ancora esporrà un PIN dell'immagine ancora, che è ancora una categoria pin della categoria pin \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="83bef-106">A camera that supports still images will expose a still image pin, which is pin category PIN\_CATEGORY\_STILL.</span></span>

<span data-ttu-id="83bef-107">Il modo consigliato per ottenere immagini ancora dal dispositivo consiste nell'usare le API di acquisizione immagini Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="83bef-107">The recommended way to get still images from the device is to use the Windows Image Acquisition (WIA) APIs.</span></span> <span data-ttu-id="83bef-108">Per ulteriori informazioni, vedere la sezione relativa all'acquisizione di immagini Windows nella documentazione di Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="83bef-108">For more information, see "Windows Image Acquisition" in the Platform SDK documentation.</span></span> <span data-ttu-id="83bef-109">Tuttavia, è anche possibile usare DirectShow per acquisire un'immagine.</span><span class="sxs-lookup"><span data-stu-id="83bef-109">However, you can also use DirectShow to capture an image.</span></span>

<span data-ttu-id="83bef-110">Per attivare il pin ancora, usare il metodo [**IAMVideoControl:: semode**](/windows/desktop/api/Strmif/nf-strmif-iamvideocontrol-setmode) quando il grafico è in esecuzione, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="83bef-110">To trigger the still pin, use the [**IAMVideoControl::SetMode**](/windows/desktop/api/Strmif/nf-strmif-iamvideocontrol-setmode) method when the graph is running, as follows:</span></span>


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



<span data-ttu-id="83bef-111">Eseguire una query sul filtro di acquisizione per [**IAMVideoControl**](/windows/desktop/api/Strmif/nn-strmif-iamvideocontrol).</span><span class="sxs-lookup"><span data-stu-id="83bef-111">Query the capture filter for [**IAMVideoControl**](/windows/desktop/api/Strmif/nn-strmif-iamvideocontrol).</span></span> <span data-ttu-id="83bef-112">Se l'interfaccia è supportata, ottenere un puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN ancora chiamando il metodo [**ICaptureGraphBuilder2:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) , come illustrato nell'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="83bef-112">If the interface is supported, get a pointer to the still pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface by calling the [**ICaptureGraphBuilder2::FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) method, as shown in the previous example.</span></span> <span data-ttu-id="83bef-113">Chiamare quindi [**IAMVideoControl:: semode**](/windows/desktop/api/Strmif/nf-strmif-iamvideocontrol-setmode) con il puntatore **Ipin** e il \_ flag di attivazione VideoControlFlag.</span><span class="sxs-lookup"><span data-stu-id="83bef-113">Then call [**IAMVideoControl::SetMode**](/windows/desktop/api/Strmif/nf-strmif-iamvideocontrol-setmode) with the **IPin** pointer and the VideoControlFlag\_Trigger flag.</span></span>

> [!Note]  
> <span data-ttu-id="83bef-114">A seconda della fotocamera, potrebbe essere necessario eseguire il rendering del PIN di acquisizione ( \_ acquisizione della categoria pin \_ ) prima che il pin ancora si connetta.</span><span class="sxs-lookup"><span data-stu-id="83bef-114">Depending on the camera, you might need to render the capture pin (PIN\_CATEGORY\_CAPTURE) before the still pin will connect.</span></span>

 

### <a name="example-using-the-sample-grabber-filter"></a><span data-ttu-id="83bef-115">Esempio: uso del filtro Grabber di esempio</span><span class="sxs-lookup"><span data-stu-id="83bef-115">Example: Using the Sample Grabber Filter</span></span>

<span data-ttu-id="83bef-116">Un modo per acquisire l'immagine è con il filtro [**grabber di esempio**](sample-grabber-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="83bef-116">One way to capture the image is with the [**Sample Grabber**](sample-grabber-filter.md) filter.</span></span> <span data-ttu-id="83bef-117">Il grabber di esempio usa una funzione di callback definita dall'applicazione per elaborare l'immagine.</span><span class="sxs-lookup"><span data-stu-id="83bef-117">The Sample Grabber uses an application-defined callback function to process the image.</span></span> <span data-ttu-id="83bef-118">Per altre informazioni sul filtro Grabber di esempio, vedere [uso del grabber di esempio](using-the-sample-grabber.md).</span><span class="sxs-lookup"><span data-stu-id="83bef-118">For more information about the Sample Grabber filter, see [Using the Sample Grabber](using-the-sample-grabber.md).</span></span>

<span data-ttu-id="83bef-119">Nell'esempio seguente si presuppone che il Pin Still fornisca un'immagine RGB non compressa.</span><span class="sxs-lookup"><span data-stu-id="83bef-119">The following example assumes that the still pin delivers an uncompressed RGB image.</span></span> <span data-ttu-id="83bef-120">In primo luogo, definire una classe che implementerà l'interfaccia di callback del grabber di esempio, [**ISampleGrabberCB**](isamplegrabbercb.md):</span><span class="sxs-lookup"><span data-stu-id="83bef-120">First, define a class that will implement the Sample Grabber's callback interface, [**ISampleGrabberCB**](isamplegrabbercb.md):</span></span>


```C++
// Class to hold the callback function for the Sample Grabber filter.
class SampleGrabberCallback : public ISampleGrabberCB
{
    // Implementation is described later.
}

// Global instance of the class.
SampleGrabberCallback g_StillCapCB;
```



<span data-ttu-id="83bef-121">L'implementazione della classe verrà descritta a breve.</span><span class="sxs-lookup"><span data-stu-id="83bef-121">The implementation of the class is described shortly.</span></span>

<span data-ttu-id="83bef-122">A questo punto, connettere il Pin Still al grabber di esempio e connettere il grabber di esempio al filtro [**renderer null**](null-renderer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="83bef-122">Next, connect the still pin to the Sample Grabber, and connect the Sample Grabber to the [**Null Renderer**](null-renderer-filter.md) filter.</span></span> <span data-ttu-id="83bef-123">Il renderer NULL elimina semplicemente gli esempi di supporti ricevuti; il lavoro effettivo verrà eseguito all'interno del callback.</span><span class="sxs-lookup"><span data-stu-id="83bef-123">The Null Renderer simply discards media samples that it receives; the actual work will be done within the callback.</span></span> <span data-ttu-id="83bef-124">(L'unico motivo per cui il renderer null consiste nel connettere il pin di output di Sample Grabber a un elemento). Chiamare [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) per creare i filtri di esempio grabber e renderer null e chiamare [**IFilterGraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) per aggiungere entrambi i filtri al grafo:</span><span class="sxs-lookup"><span data-stu-id="83bef-124">(The only reason for the Null Renderer is to connect the Sample Grabber's output pin to something.) Call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) to create the Sample Grabber and Null Renderer filters, and call [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) to add both filters to the graph:</span></span>


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



<span data-ttu-id="83bef-125">È possibile usare il metodo [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) per connettere tutti e tre i filtri in una chiamata al metodo, passando dal pin continuo al grabber di esempio e dal grabber di esempio al renderer null:</span><span class="sxs-lookup"><span data-stu-id="83bef-125">You can use the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method to connect all three filters in one method call, going from the still pin to the Sample Grabber, and from the Sample Grabber to the Null Renderer:</span></span>


```C++
hr = pBuild->RenderStream(
    &PIN_CATEGORY_STILL, // Connect this pin ...
    &MEDIATYPE_Video,    // with this media type ...
    pCap,                // on this filter ...
    pSG_Filter,          // to the Sample Grabber ...
    pNull);              // ... and finally to the Null Renderer.
```



<span data-ttu-id="83bef-126">Usare ora l'interfaccia [**ISampleGrabber**](isamplegrabber.md) per configurare il grabber di esempio in modo da memorizzare nel buffer gli esempi:</span><span class="sxs-lookup"><span data-stu-id="83bef-126">Now use the [**ISampleGrabber**](isamplegrabber.md) interface to configure the Sample Grabber so that it buffers samples:</span></span>


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



<span data-ttu-id="83bef-127">Impostare l'interfaccia di callback con un puntatore all'oggetto callback:</span><span class="sxs-lookup"><span data-stu-id="83bef-127">Set the callback interface with a pointer to your callback object:</span></span>


```C++
hr = pSG->SetCallback(&g_StillCapCB, 0); // 0 = Use the SampleCB callback method.
```



<span data-ttu-id="83bef-128">Ottenere il tipo di supporto usato dal pin per connettersi con il grabber di esempio:</span><span class="sxs-lookup"><span data-stu-id="83bef-128">Get the media type that the still pin used to connect with the Sample Grabber:</span></span>


```C++
// Store the media type for later use.
AM_MEDIA_TYPE g_StillMediaType;

hr = pSG->GetConnectedMediaType(&g_StillMediaType);
pSG->Release();
```



<span data-ttu-id="83bef-129">Questo tipo di supporto conterrà la struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) che definisce il formato dell'immagine ancora.</span><span class="sxs-lookup"><span data-stu-id="83bef-129">This media type will contain the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure that defines the format of the still image.</span></span> <span data-ttu-id="83bef-130">Liberare il tipo di supporto prima della chiusura dell'applicazione:</span><span class="sxs-lookup"><span data-stu-id="83bef-130">Free the media type before the application exits:</span></span>


```C++
// On exit, remember to release the media type.
FreeMediaType(g_StillMediaType);
```



<span data-ttu-id="83bef-131">Di seguito è riportato un esempio della classe di callback.</span><span class="sxs-lookup"><span data-stu-id="83bef-131">What follows is an example of the callback class.</span></span> <span data-ttu-id="83bef-132">Si noti che la classe implementa **IUnknown**, che eredita tramite l'interfaccia [**ISampleGrabber**](isamplegrabber.md) , ma non mantiene un conteggio dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="83bef-132">Note that the class implements **IUnknown**, which it inherits through the [**ISampleGrabber**](isamplegrabber.md) interface, but it does not keep a reference count.</span></span> <span data-ttu-id="83bef-133">Questo è sicuro perché l'applicazione crea l'oggetto nello stack e l'oggetto rimane nell'ambito per tutta la durata del grafico di filtro.</span><span class="sxs-lookup"><span data-stu-id="83bef-133">This is safe because the application creates the object on the stack, and the object remains in scope throughout the lifetime of the filter graph.</span></span>

<span data-ttu-id="83bef-134">Tutto il lavoro si verifica nel metodo [**BufferCB**](isamplegrabbercb-buffercb.md) , che viene chiamato dal grabber di esempio ogni volta che viene ottenuto un nuovo esempio.</span><span class="sxs-lookup"><span data-stu-id="83bef-134">All of the work happens in the [**BufferCB**](isamplegrabbercb-buffercb.md) method, which is called by the Sample Grabber whenever it gets a new sample.</span></span> <span data-ttu-id="83bef-135">Nell'esempio seguente il metodo scrive la bitmap in un file:</span><span class="sxs-lookup"><span data-stu-id="83bef-135">In the following example, the method writes the bitmap to a file:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="83bef-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="83bef-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83bef-137">Attività di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="83bef-137">Video Capture Tasks</span></span>](video-capture-tasks.md)
</dt> </dl>

 

 
