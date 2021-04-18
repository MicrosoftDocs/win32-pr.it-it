---
description: Il filtro Grabber di esempio è un filtro di trasformazione che può essere usato per estrarre gli esempi di supporti da un flusso mentre passano attraverso il grafico dei filtri.
ms.assetid: ec0e367e-9ef9-4de6-9132-b462c233bc98
title: Uso del grabber di esempio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4886c796691e83e02b58ddea129d60d5004c9f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314384"
---
# <a name="using-the-sample-grabber"></a>Uso del grabber di esempio

\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]

Il filtro [**grabber di esempio**](sample-grabber-filter.md) è un filtro di trasformazione che può essere usato per estrarre gli esempi di supporti da un flusso mentre passano attraverso il grafico dei filtri.

Se si vuole semplicemente estrarre una bitmap da un file video, è più semplice usare l'oggetto [mediadet (Media Detector)](media-detector--mediadet.md) . Per informazioni dettagliate, vedere [acquisizione di un frame di poster](grabbing-a-poster-frame.md) . Il grabber di esempio è più flessibile, tuttavia, perché funziona con quasi tutti i tipi di supporto (vedere [**ISampleGrabber:: SetMediaType**](isamplegrabber-setmediatype.md) per le poche eccezioni) e offre un maggiore controllo per l'applicazione.

-   [Creare il gestore del grafico del filtro](#create-the-filter-graph-manager)
-   [Aggiungere il grabber di esempio al grafico di filtro](#add-the-sample-grabber-to-the-filter-graph)
-   [Imposta il tipo di supporto](#set-the-media-type)
-   [Creare il grafico di filtro](#build-the-filter-graph)
-   [Eseguire il grafo](#run-the-graph)
-   [Acquisire l'esempio](#grab-the-sample)
-   [Codice di esempio](#example-code)
-   [Argomenti correlati](#related-topics)

## <a name="create-the-filter-graph-manager"></a>Creare il gestore del grafico del filtro

Per iniziare, creare la [gestione del grafo del filtro](filter-graph-manager.md) e la query per le interfacce [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) e [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) .


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





## <a name="add-the-sample-grabber-to-the-filter-graph"></a>Aggiungere il grabber di esempio al grafico di filtro

Creare un'istanza del filtro Grabber di esempio e addit al grafico dei filtri. Eseguire una query sul filtro Grabber di esempio per l'interfaccia [**ISampleGrabber**](isamplegrabber.md) .


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





## <a name="set-the-media-type"></a>Imposta il tipo di supporto

Quando si crea il grabber di esempio per la prima volta, non è disponibile alcun tipo di supporto preferito. Ciò significa che è possibile connettersi praticamente a qualsiasi filtro nel grafico, ma non si avrà alcun controllo sul tipo di dati ricevuti. Prima di creare il resto del grafo, è necessario impostare un tipo di supporto per il grabber di esempio, chiamando il metodo [**ISampleGrabber:: SetMediaType**](isamplegrabber-setmediatype.md) .

Quando si connette il grabber di esempio, questo tipo di supporto viene confrontato con il tipo di supporto offerto dall'altro filtro. Gli unici campi che controlla sono il tipo principale, il sottotipo e il tipo di formato. Per uno di questi valori, il valore \_ null del GUID indica che "accetta qualsiasi valore". Nella maggior parte dei casi, è preferibile impostare il tipo e il sottotipo principali. Il codice seguente, ad esempio, specifica un video RGB a 24 bit non compresso:


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



## <a name="build-the-filter-graph"></a>Creare il grafico di filtro

A questo punto è possibile compilare il resto del grafico del filtro. Poiché il grabber di esempio si connetterà solo usando il tipo di supporto specificato, questo consente di sfruttare i meccanismi di [connessione intelligente](intelligent-connect.md) del gestore del grafico dei filtri quando si compila il grafo.

Se, ad esempio, è stato specificato un video non compresso, è possibile connettere un filtro di origine al grabber di esempio e il componente di gestione del filtro del grafico aggiungerà automaticamente il parser di file e il decodificatore. Nell'esempio seguente viene usata la funzione helper ConnectFilters, elencata in [Connect Two filters](connect-two-filters.md):


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





Il grabber di esempio è un filtro di trasformazione, quindi il pin di output deve essere connesso a un altro filtro. Spesso è possibile semplicemente rimuovere gli esempi una volta completata l'operazione. In tal caso, connettere il grabber di esempio al [**filtro renderer null**](null-renderer-filter.md), che elimina i dati ricevuti.

Nell'esempio seguente viene connesso il grabber di esempio al filtro renderer null:


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





Tenere presente che l'inserimento del grabber di esempio tra un decodificatore video e il renderer video può danneggiare significativamente le prestazioni di rendering. Il grabber di esempio è un filtro Trans-on-Place, che indica che il buffer di output è uguale al buffer di input. Per il rendering video, è probabile che il buffer di output si trovi nella scheda grafica, in cui le operazioni di lettura sono molto più lente, rispetto alle operazioni di lettura nella memoria principale.

## <a name="run-the-graph"></a>Eseguire il grafo

Il grabber di esempio opera in una delle due modalità seguenti:

-   La modalità di buffering esegue una copia di ogni esempio prima di consegnare l'esempio downstream.
-   La modalità di callback richiama una funzione di callback definita dall'applicazione su ogni esempio.

Questo articolo descrive la modalità di buffering. Prima di utilizzare la modalità di callback, tenere presente che la funzione di callback deve essere piuttosto limitata. In caso contrario, può ridurre drasticamente le prestazioni o anche causare deadlock. Per ulteriori informazioni, vedere [**ISampleGrabber:: secallback**](isamplegrabber-setcallback.md). Per attivare la modalità di buffering, chiamare il metodo [**ISampleGrabber:: SetBufferSamples**](isamplegrabber-setbuffersamples.md) con il valore **true**.

Facoltativamente, chiamare il metodo [**ISampleGrabber:: SetOneShot**](isamplegrabber-setoneshot.md) con il valore **true**. In questo modo, l'grabber di esempio si arresta dopo la ricezione del primo esempio multimediale, che risulta utile se si desidera acquisire un singolo frame dal flusso. Cercare l'ora desiderata, eseguire il grafo e attendere l'evento di [**\_ completamento della EC**](ec-complete.md) . Si noti che il livello di accuratezza del frame dipende dall'origine. Ad esempio, la ricerca di un file MPEG spesso non è accurata per i frame.

Per eseguire il grafico il più rapidamente possibile, attivare il clock del grafico come descritto in [impostazione del clock del grafico](setting-the-graph-clock.md).

Nell'esempio seguente viene abilitata la modalità monofase e la modalità di memorizzazione nel buffer, viene eseguito il grafico del filtro e viene atteso il completamento.


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



## <a name="grab-the-sample"></a>Acquisire l'esempio

In modalità di memorizzazione nel buffer, il grabber di esempio archivia una copia di ogni esempio. Il metodo [**ISampleGrabber:: GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md) copia il buffer in una matrice allocata dal chiamante. Per determinare le dimensioni della matrice necessaria, chiamare prima **GetCurrentBuffer** con un puntatore **null** per l'indirizzo di matrice. Quindi allocare la matrice e chiamare il metodo una seconda volta per copiare il buffer. Nell'esempio seguente sono illustrati i passaggi per l'operazione.


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



È necessario avere a disposizione il formato esatto dei dati nel buffer. Per ottenere queste informazioni, chiamare il metodo [**ISampleGrabber:: GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md) . Questo metodo compila una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) con il formato.

Per un flusso video non compresso, le informazioni sul formato sono contenute in una struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) . Nell'esempio seguente viene illustrato come ottenere le informazioni sul formato per un flusso video non compresso.


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
> Il grabber di esempio non supporta [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).

 

## <a name="example-code"></a>Codice di esempio

Ecco il codice completo per gli esempi precedenti.

> [!Note]  
> Questo esempio usa la funzione [SafeRelease](../medfound/saferelease.md) per rilasciare i puntatori a interfaccia.

 


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

[Uso dei servizi di modifica DirectShow](using-directshow-editing-services.md)
</dt> </dl>

 

 
