---
description: Il filtro Sample Grabber è un filtro di trasformazione che può essere usato per acquisire campioni multimediali da un flusso mentre passano attraverso il grafico dei filtri.
ms.assetid: ec0e367e-9ef9-4de6-9132-b462c233bc98
title: Uso del grabber di esempio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47318b7bd4dbbad57fb82bec11e0a1293a0284c906c78fc7175d8a758ad477f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083561"
---
# <a name="using-the-sample-grabber"></a>Uso del grabber di esempio

\[Questa API non è supportata e potrebbe essere modificata o non disponibile in futuro.\]

Il [**filtro Sample Grabber**](sample-grabber-filter.md) è un filtro di trasformazione che può essere usato per acquisire campioni multimediali da un flusso mentre passano attraverso il grafico dei filtri.

Se si vuole semplicemente acquisire una bitmap da un file video, è più facile usare l'oggetto [Media Detector (MediaDet).](media-detector--mediadet.md) Per [informazioni dettagliate, vedere Grabbing a Poster Frame](grabbing-a-poster-frame.md) (Afferrare una cornice poster). Il grabber di esempio è tuttavia più flessibile, perché funziona con quasi tutti i tipi di supporti (vedere [**ISampleGrabber::SetMediaType**](isamplegrabber-setmediatype.md) per le poche eccezioni) e offre maggiore controllo all'applicazione.

-   [Creare la gestione Graph filtri](#create-the-filter-graph-manager)
-   [Aggiungere Sample Grabber al filtro Graph](#add-the-sample-grabber-to-the-filter-graph)
-   [Impostare il tipo di supporto](#set-the-media-type)
-   [Compilare il Graph](#build-the-filter-graph)
-   [Eseguire il Graph](#run-the-graph)
-   [Afferrare l'esempio](#grab-the-sample)
-   [Codice di esempio](#example-code)
-   [Argomenti correlati](#related-topics)

## <a name="create-the-filter-graph-manager"></a>Creare la gestione Graph filtri

Per iniziare, creare [filter Graph Manager](filter-graph-manager.md) ed eseguire una query per le interfacce [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) e [**IMediaEventEx.**](/windows/desktop/api/Control/nn-control-imediaeventex)


```C++
    IGraphBuilder *pGraph = NULL;
    IMediaControl *pControl = NULL;
    IMediaEventEx *pEvent = NULL;


    HRESULT hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
        CLSCTX_INPROC_SERVER,IID_PPV_ARGS(&pGraph));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->QueryInterface(IID_PPV_ARGS(&pControl));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->QueryInterface(IID_PPV_ARGS(&pEvent));
    if (FAILED(hr))
    {
        goto done;
    }
```





## <a name="add-the-sample-grabber-to-the-filter-graph"></a>Aggiungere Sample Grabber al filtro Graph

Creare un'istanza del filtro Sample Grabber e aggiungerla al grafico dei filtri. Eseguire una query sul filtro Grabber di esempio per [**l'interfaccia ISampleGrabber.**](isamplegrabber.md)


```C++
    IBaseFilter *pGrabberF = NULL;
    ISampleGrabber *pGrabber = NULL;


    // Create the Sample Grabber filter.
    hr = CoCreateInstance(CLSID_SampleGrabber, NULL, CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&pGrabberF));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pGrabberF, L&quot;Sample Grabber&quot;);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabberF->QueryInterface(IID_PPV_ARGS(&pGrabber));
    if (FAILED(hr))
    {
        goto done;
    }
```





## <a name="set-the-media-type"></a>Impostare il tipo di supporto

Quando si crea per la prima volta Sample Grabber, non ha un tipo di supporto preferito. Ciò significa che è possibile connettersi a quasi tutti i filtri nel grafico, ma non si avrebbe alcun controllo sul tipo di dati ricevuti. Prima di compilare il resto del grafico, è quindi necessario impostare un tipo di supporto per Sample Grabber chiamando il metodo [**ISampleGrabber::SetMediaType.**](isamplegrabber-setmediatype.md)

Quando il grabber di esempio si connette, confronta questo tipo di supporto con il tipo di supporto offerto dall'altro filtro. Gli unici campi che controlla sono il tipo principale, il sottotipo e il tipo di formato. Per uno di questi valori, il valore GUID \_ NULL significa "accettare qualsiasi valore". Nella maggior parte dei casi è necessario impostare il tipo principale e il sottotipo. Ad esempio, il codice seguente specifica un video RGB a 24 bit non compresso:


```C++
    AM_MEDIA_TYPE mt;
    ZeroMemory(&mt, sizeof(mt));
    mt.majortype = MEDIATYPE_Video;
    mt.subtype = MEDIASUBTYPE_RGB24;

    hr = pGrabber->SetMediaType(&mt);
    if (FAILED(hr))
    {
        goto done;
    }
```



## <a name="build-the-filter-graph"></a>Compilare l'Graph

A questo punto è possibile compilare il resto del grafico dei filtri. [Poiché](intelligent-connect.md) Il grabber di esempio si connetterà solo usando il tipo di supporto specificato, ciò consente di sfruttare i meccanismi di Connessione intelligenti di Filter Graph Manager quando si compila il grafo.

Ad esempio, se è stato specificato un video non compresso, è possibile connettere un filtro di origine a Sample Grabber e Filter Graph Manager aggiungerà automaticamente il parser di file e il decodificatore. L'esempio seguente usa la funzione helper ConnectFilters, elencata Connessione [due filtri](connect-two-filters.md):


```C++
    IBaseFilter *pSourceF = NULL;
    IEnumPins *pEnum = NULL;
    IPin *pPin = NULL;


    hr = pGraph->AddSourceFilter(pszVideoFile, L&quot;Source&quot;, &pSourceF);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSourceF->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        goto done;
    }

    while (S_OK == pEnum->Next(1, &pPin, NULL))
    {
        hr = ConnectFilters(pGraph, pPin, pGrabberF);
        SafeRelease(&pPin);
        if (SUCCEEDED(hr))
        {
            break;
        }
    }

    if (FAILED(hr))
    {
        goto done;
    }
```





Sample Grabber è un filtro di trasformazione, quindi il pin di output deve essere connesso a un altro filtro. Spesso, è possibile rimuovere semplicemente gli esempi dopo averli utilizzati. In tal caso, connettere Sample Grabber al filtro [**renderer Null,**](null-renderer-filter.md)che elimina i dati ricevuti.

L'esempio seguente connette Sample Grabber al filtro Del renderer Null:


```C++
    IBaseFilter *pNullF = NULL;


    hr = CoCreateInstance(CLSID_NullRenderer, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pNullF));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pNullF, L&quot;Null Filter&quot;);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = ConnectFilters(pGraph, pGrabberF, pNullF);
    if (FAILED(hr))
    {
        goto done;
    }
```





Tenere presente che il posizionamento di Sample Grabber tra un decodificatore video e il renderer video può danneggiare significativamente le prestazioni di rendering. Sample Grabber è un filtro trans-in-place, il che significa che il buffer di output è lo stesso del buffer di input. Per il rendering video, è probabile che il buffer di output si trovi nella scheda grafica, dove le operazioni di lettura sono molto più lente rispetto alle operazioni di lettura nella memoria principale.

## <a name="run-the-graph"></a>Eseguire il Graph

Sample Grabber funziona in una delle due modalità seguenti:

-   La modalità di memorizzazione nel buffer crea una copia di ogni campione prima di recapitare l'esempio a valle.
-   La modalità di callback richiama una funzione di callback definita dall'applicazione in ogni esempio.

Questo articolo descrive la modalità di memorizzazione nel buffer. Prima di usare la modalità di callback, tenere presente che la funzione di callback deve essere piuttosto limitata. In caso contrario, può ridurre drasticamente le prestazioni o persino causare deadlock. Per altre informazioni, vedere [**ISampleGrabber::SetCallback.**](isamplegrabber-setcallback.md) Per attivare la modalità di memorizzazione nel buffer, chiamare il metodo [**ISampleGrabber::SetBufferSamples**](isamplegrabber-setbuffersamples.md) con il valore **TRUE.**

Facoltativamente, chiamare il [**metodo ISampleGrabber::SetOneShot**](isamplegrabber-setoneshot.md) con il valore **TRUE.** Ciò causa l'arresto di Sample Grabber dopo la ricezione del primo campione multimediale, che è utile se si vuole afferrare un singolo fotogramma dal flusso. Cercare l'ora desiderata, eseguire il grafico e attendere [**l'evento EC \_ COMPLETE.**](ec-complete.md) Si noti che il livello di accuratezza dei fotogrammi dipende dall'origine. Ad esempio, la ricerca di un file MPEG spesso non è precisa per i frame.

Per eseguire il grafico il più rapidamente possibile, ruotare l'orologio del grafo come descritto in [Impostazione dell'Graph clock](setting-the-graph-clock.md).

L'esempio seguente abilita la modalità one-shot e la modalità di buffering, esegue il grafico dei filtri e attende il completamento.


```C++
    hr = pGrabber->SetOneShot(TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabber->SetBufferSamples(TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pControl->Run();
    if (FAILED(hr))
    {
        goto done;
    }

    long evCode;
    hr = pEvent->WaitForCompletion(INFINITE, &evCode);
```



## <a name="grab-the-sample"></a>Afferrare l'esempio

In modalità di buffering, Sample Grabber archivia una copia di ogni esempio. Il [**metodo ISampleGrabber::GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md) copia il buffer in una matrice allocata dal chiamante. Per determinare le dimensioni della matrice necessarie, chiamare prima **GetCurrentBuffer** con un **puntatore NULL** per l'indirizzo della matrice. Allocare quindi la matrice e chiamare il metodo una seconda volta per copiare il buffer. Nell'esempio seguente sono illustrati i passaggi per l'operazione.


```C++
    // Find the required buffer size.
    long cbBuffer;
    hr = pGrabber->GetCurrentBuffer(&cbBuffer, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    pBuffer = (BYTE*)CoTaskMemAlloc(cbBuffer);
    if (!pBuffer) 
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    hr = pGrabber->GetCurrentBuffer(&cbBuffer, (long*)pBuffer);
    if (FAILED(hr))
    {
        goto done;
    }
```



Sarà necessario conoscere il formato esatto dei dati nel buffer. Per ottenere queste informazioni, chiamare il [**metodo ISampleGrabber::GetConnectedMediaType.**](isamplegrabber-getconnectedmediatype.md) Questo metodo inserisce in una [**struttura AM \_ MEDIA \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) il formato .

Per un flusso video non compresso, le informazioni sul formato sono contenute in una [**struttura VIDEOINFOHEADER.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) L'esempio seguente illustra come ottenere le informazioni sul formato per un flusso video non compresso.


```C++
    // Examine the format block.
    if ((mt.formattype == FORMAT_VideoInfo) && 
        (mt.cbFormat >= sizeof(VIDEOINFOHEADER)) &&
        (mt.pbFormat != NULL)) 
    {
        VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)mt.pbFormat;

        hr = WriteBitmap(pszBitmapFile, &pVih->bmiHeader, 
            mt.cbFormat - SIZE_PREHEADER, pBuffer, cbBuffer);
    }
    else 
    {
        // Invalid format.
        hr = VFW_E_INVALIDMEDIATYPE; 
    }
```



> [!Note]  
> Il grabber di esempio non supporta [**VIDEOINFOHEADER2.**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)

 

## <a name="example-code"></a>Codice di esempio

Ecco il codice completo per gli esempi precedenti.

> [!Note]  
> Questo esempio usa la [funzione SafeRelease](../medfound/saferelease.md) per rilasciare i puntatori a interfaccia.

 


```C++
#include <windows.h>
#include <dshow.h>
#include "qedit.h"

template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}



HRESULT WriteBitmap(PCWSTR, BITMAPINFOHEADER*, size_t, BYTE*, size_t);

HRESULT GrabVideoBitmap(PCWSTR pszVideoFile, PCWSTR pszBitmapFile)
{
    IGraphBuilder *pGraph = NULL;
    IMediaControl *pControl = NULL;
    IMediaEventEx *pEvent = NULL;
    IBaseFilter *pGrabberF = NULL;
    ISampleGrabber *pGrabber = NULL;
    IBaseFilter *pSourceF = NULL;
    IEnumPins *pEnum = NULL;
    IPin *pPin = NULL;
    IBaseFilter *pNullF = NULL;

    BYTE *pBuffer = NULL;

    HRESULT hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
        CLSCTX_INPROC_SERVER,IID_PPV_ARGS(&pGraph));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->QueryInterface(IID_PPV_ARGS(&pControl));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->QueryInterface(IID_PPV_ARGS(&pEvent));
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the Sample Grabber filter.
    hr = CoCreateInstance(CLSID_SampleGrabber, NULL, CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&pGrabberF));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pGrabberF, L&quot;Sample Grabber&quot;);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabberF->QueryInterface(IID_PPV_ARGS(&pGrabber));
    if (FAILED(hr))
    {
        goto done;
    }

    AM_MEDIA_TYPE mt;
    ZeroMemory(&mt, sizeof(mt));
    mt.majortype = MEDIATYPE_Video;
    mt.subtype = MEDIASUBTYPE_RGB24;

    hr = pGrabber->SetMediaType(&mt);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddSourceFilter(pszVideoFile, L&quot;Source&quot;, &pSourceF);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSourceF->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        goto done;
    }

    while (S_OK == pEnum->Next(1, &pPin, NULL))
    {
        hr = ConnectFilters(pGraph, pPin, pGrabberF);
        SafeRelease(&pPin);
        if (SUCCEEDED(hr))
        {
            break;
        }
    }

    if (FAILED(hr))
    {
        goto done;
    }

    hr = CoCreateInstance(CLSID_NullRenderer, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pNullF));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pNullF, L&quot;Null Filter&quot;);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = ConnectFilters(pGraph, pGrabberF, pNullF);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabber->SetOneShot(TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabber->SetBufferSamples(TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pControl->Run();
    if (FAILED(hr))
    {
        goto done;
    }

    long evCode;
    hr = pEvent->WaitForCompletion(INFINITE, &evCode);

    // Find the required buffer size.
    long cbBuffer;
    hr = pGrabber->GetCurrentBuffer(&cbBuffer, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    pBuffer = (BYTE*)CoTaskMemAlloc(cbBuffer);
    if (!pBuffer) 
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    hr = pGrabber->GetCurrentBuffer(&cbBuffer, (long*)pBuffer);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabber->GetConnectedMediaType(&mt);
    if (FAILED(hr))
    {
        goto done;
    }

    // Examine the format block.
    if ((mt.formattype == FORMAT_VideoInfo) && 
        (mt.cbFormat >= sizeof(VIDEOINFOHEADER)) &&
        (mt.pbFormat != NULL)) 
    {
        VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)mt.pbFormat;

        hr = WriteBitmap(pszBitmapFile, &pVih->bmiHeader, 
            mt.cbFormat - SIZE_PREHEADER, pBuffer, cbBuffer);
    }
    else 
    {
        // Invalid format.
        hr = VFW_E_INVALIDMEDIATYPE; 
    }

    FreeMediaType(mt);

done:
    CoTaskMemFree(pBuffer);
    SafeRelease(&pPin);
    SafeRelease(&pEnum);
    SafeRelease(&pNullF);
    SafeRelease(&pSourceF);
    SafeRelease(&pGrabber);
    SafeRelease(&pGrabberF);
    SafeRelease(&pControl);
    SafeRelease(&pEvent);
    SafeRelease(&pGraph);
    return hr;
};

// Writes a bitmap file
//  pszFileName:  Output file name.
//  pBMI:         Bitmap format information (including pallete).
//  cbBMI:        Size of the BITMAPINFOHEADER, including palette, if present.
//  pData:        Pointer to the bitmap bits.
//  cbData        Size of the bitmap, in bytes.

HRESULT WriteBitmap(PCWSTR pszFileName, BITMAPINFOHEADER *pBMI, size_t cbBMI,
    BYTE *pData, size_t cbData)
{
    HANDLE hFile = CreateFile(pszFileName, GENERIC_WRITE, 0, NULL, 
        CREATE_ALWAYS, 0, NULL);
    if (hFile == NULL)
    {
        return HRESULT_FROM_WIN32(GetLastError());
    }

    BITMAPFILEHEADER bmf = { };

    bmf.bfType = &#39;MB&#39;;
    bmf.bfSize = cbBMI+ cbData + sizeof(bmf); 
    bmf.bfOffBits = sizeof(bmf) + cbBMI; 

    DWORD cbWritten = 0;
    BOOL result = WriteFile(hFile, &bmf, sizeof(bmf), &cbWritten, NULL);
    if (result)
    {
        result = WriteFile(hFile, pBMI, cbBMI, &cbWritten, NULL);
    }
    if (result)
    {
        result = WriteFile(hFile, pData, cbData, &cbWritten, NULL);
    }

    HRESULT hr = result ? S_OK : HRESULT_FROM_WIN32(GetLastError());

    CloseHandle(hFile);

    return hr;
}
```





## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di DirectShow di modifica](using-directshow-editing-services.md)
</dt> </dl>

 

 
