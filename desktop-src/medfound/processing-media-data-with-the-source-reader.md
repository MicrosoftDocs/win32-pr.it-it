---
description: In questo argomento viene descritto come utilizzare il lettore di origine per elaborare i dati multimediali.
ms.assetid: 583f5736-f767-47c5-8fdc-b3645aed59f6
title: Utilizzo del lettore di origine per l'elaborazione dei dati multimediali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b19bce4d83298693825037aef92a220d78ed7c7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351181"
---
# <a name="using-the-source-reader-to-process-media-data"></a>Utilizzo del lettore di origine per l'elaborazione dei dati multimediali

In questo argomento viene descritto come utilizzare il [lettore di origine](source-reader.md) per elaborare i dati multimediali.

Per usare il lettore di origine, seguire questa procedura di base:

1.  Creare un'istanza del lettore di origine.
2.  Enumerare i formati di output possibili.
3.  Imposta il formato di output effettivo per ogni flusso.
4.  Elaborare i dati dall'origine.

Nella parte restante di questo argomento vengono descritti in dettaglio questi passaggi.

-   [Creazione del lettore di origine](#creating-the-source-reader)
-   [Enumerazione dei formati di output](#enumerating-output-formats)
-   [Impostazione di formati di output](#setting-output-formats)
-   [Elaborazione dei dati multimediali](#using-the-source-reader-to-process-media-data)
-   [Svuotamento della pipeline di dati](#draining-the-data-pipeline)
-   [Recupero della durata del file](#getting-the-file-duration)
-   [La ricerca](#seeking)
-   [Velocità di riproduzione](#playback-rate)
-   [Accelerazione hardware](#hardware-acceleration)
-   [Argomenti correlati](#related-topics)

## <a name="creating-the-source-reader"></a>Creazione del lettore di origine

Per creare un'istanza del lettore di origine, chiamare una delle funzioni seguenti:



| Funzione                                                                                                                                                                                                                                                        | Descrizione                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFCreateSourceReaderFromURL"></span><span id="mfcreatesourcereaderfromurl"></span><span id="MFCREATESOURCEREADERFROMURL"></span>[**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)<br/>                                         | Accetta un URL come input. Questa funzione usa il [resolver di origine](source-resolver.md) per creare un'origine multimediale dall'URL.<br/>                                                                       |
| <span id="MFCreateSourceReaderFromByteStream"></span><span id="mfcreatesourcereaderfrombytestream"></span><span id="MFCREATESOURCEREADERFROMBYTESTREAM"></span>[**MFCreateSourceReaderFromByteStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)<br/>      | Accetta un puntatore a un flusso di byte. Questa funzione usa anche il resolver di origine per creare l'origine multimediale.<br/>                                                                                        |
| <span id="MFCreateSourceReaderFromMediaSource"></span><span id="mfcreatesourcereaderfrommediasource"></span><span id="MFCREATESOURCEREADERFROMMEDIASOURCE"></span>[**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)<br/> | Accetta un puntatore a un'origine multimediale che è già stata creata. Questa funzione è utile per le origini multimediali che il resolver di origine non è in grado di creare, ad esempio dispositivi di acquisizione o origini multimediali personalizzate.<br/> |



 

In genere, per i file multimediali, usare [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl). Per i dispositivi, ad esempio le webcam, usare [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource). Per ulteriori informazioni sui dispositivi di acquisizione in Microsoft Media Foundation, vedere [acquisizione audio/video](audio-video-capture.md).

Ognuna di queste funzioni accetta un puntatore [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) facoltativo, che viene usato per impostare diverse opzioni nel lettore di origine, come descritto negli argomenti di riferimento per queste funzioni. Per ottenere il comportamento predefinito, impostare questo parametro su **null**. Ogni funzione restituisce un puntatore [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) come parametro di output. Prima di chiamare una di queste funzioni, è necessario chiamare la funzione **CoInitialize (ex)** e [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) .

Il codice seguente crea il lettore di origine da un URL.


```C++
int __cdecl wmain(int argc, __in_ecount(argc) PCWSTR* argv)
{
    if (argc < 2)
    {
        return 1;
    }

    const WCHAR *pszURL = argv[1];

    // Initialize the COM runtime.
    HRESULT hr = CoInitializeEx(0, COINIT_MULTITHREADED);
    if (SUCCEEDED(hr))
    {
        // Initialize the Media Foundation platform.
        hr = MFStartup(MF_VERSION);
        if (SUCCEEDED(hr))
        {
            // Create the source reader.
            IMFSourceReader *pReader;
            hr = MFCreateSourceReaderFromURL(pszURL, NULL, &pReader);
            if (SUCCEEDED(hr))
            {
                ReadMediaFile(pReader);
                pReader->Release();
            }
            // Shut down Media Foundation.
            MFShutdown();
        }
        CoUninitialize();
    }
}
```



## <a name="enumerating-output-formats"></a>Enumerazione dei formati di output

Ogni origine multimediale ha almeno un flusso. Ad esempio, un file video può contenere un flusso video e un flusso audio. Il formato di ogni flusso viene descritto usando un tipo di supporto, rappresentato dall'interfaccia [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) . Per ulteriori informazioni sui tipi di supporto, vedere [tipi di supporti](media-types.md). È necessario esaminare il tipo di supporto per comprendere il formato dei dati che si ottengono dal lettore di origine.

Inizialmente, ogni flusso ha un formato predefinito, che è possibile trovare chiamando il metodo [**IMFSourceReader:: GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) :

Per ogni flusso, l'origine multimediale offre un elenco di tipi di supporti possibili per quel flusso. Il numero di tipi dipende dall'origine. Se l'origine rappresenta un file multimediale, in genere è presente un solo tipo per ogni flusso. Una webcam, d'altra parte, potrebbe essere in grado di trasmettere video in formati diversi. In tal caso, l'applicazione può selezionare il formato da usare dall'elenco dei tipi di supporto.

Per ottenere uno dei tipi di supporto per un flusso, chiamare il metodo [**IMFSourceReader:: GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype) . Questo metodo accetta due parametri di indice, ovvero l'indice del flusso e un indice nell'elenco dei tipi di supporto per il flusso. Per enumerare tutti i tipi per un flusso, incrementare l'indice dell'elenco mantenendo la costante dell'indice del flusso. Quando l'indice dell'elenco non rientra nei limiti, **GetNativeMediaType** restituisce **MF \_ E \_ non \_ più \_ tipi**.


```C++
HRESULT EnumerateTypesForStream(IMFSourceReader *pReader, DWORD dwStreamIndex)
{
    HRESULT hr = S_OK;
    DWORD dwMediaTypeIndex = 0;

    while (SUCCEEDED(hr))
    {
        IMFMediaType *pType = NULL;
        hr = pReader->GetNativeMediaType(dwStreamIndex, dwMediaTypeIndex, &pType);
        if (hr == MF_E_NO_MORE_TYPES)
        {
            hr = S_OK;
            break;
        }
        else if (SUCCEEDED(hr))
        {
            // Examine the media type. (Not shown.)

            pType->Release();
        }
        ++dwMediaTypeIndex;
    }
    return hr;
}
```



Per enumerare i tipi di supporto per ogni flusso, incrementare l'indice del flusso. Quando l'indice del flusso non rientra nei limiti, [**GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype) restituisce **MF \_ E \_ INVALIDSTREAMNUMBER**.


```C++
HRESULT EnumerateTypesForStream(IMFSourceReader *pReader, DWORD dwStreamIndex)
{
    HRESULT hr = S_OK;
    DWORD dwMediaTypeIndex = 0;

    while (SUCCEEDED(hr))
    {
        IMFMediaType *pType = NULL;
        hr = pReader->GetNativeMediaType(dwStreamIndex, dwMediaTypeIndex, &pType);
        if (hr == MF_E_NO_MORE_TYPES)
        {
            hr = S_OK;
            break;
        }
        else if (SUCCEEDED(hr))
        {
            // Examine the media type. (Not shown.)

            pType->Release();
        }
        ++dwMediaTypeIndex;
    }
    return hr;
}
```



## <a name="setting-output-formats"></a>Impostazione di formati di output

Per modificare il formato di output, chiamare il metodo [**IMFSourceReader:: SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype) . Questo metodo accetta l'indice del flusso e un tipo di supporto:

``` syntax
hr = pReader->SetCurrentMediaType(dwStreamIndex, pMediaType);
```

Per il tipo di supporto, dipende dal fatto che si desideri inserire un decodificatore.

-   Per ottenere i dati direttamente dall'origine senza decodificarli, usare uno dei tipi restituiti da [**GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype).
-   Per decodificare il flusso, creare un nuovo tipo di supporto che descriva il formato non compresso desiderato.

Nel caso del decodificatore, creare il tipo di supporto come segue:

1.  Chiamare [**MFCreateMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) per creare un nuovo tipo di supporto.
2.  Impostare l'attributo di [**\_ \_ \_ tipo principale MF mt**](mf-mt-major-type-attribute.md) per specificare audio o video.
3.  Impostare l'attributo del [**\_ \_ sottotipo MF mt**](mf-mt-subtype-attribute.md) per specificare il sottotipo del formato di decodifica. (Vedere [GUID del sottotipo audio](audio-subtype-guids.md) e [GUID del sottotipo video](video-subtype-guids.md)).
4.  Chiamare [**IMFSourceReader:: SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype).

Il lettore di origine caricherà automaticamente il decodificatore. Per ottenere i dettagli completi del formato decodificato, chiamare [**IMFSourceReader:: GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) dopo la chiamata a [**SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype)

Il codice seguente configura il flusso video per RGB-32 e il flusso audio per l'audio PCM.


```C++
HRESULT ConfigureDecoder(IMFSourceReader *pReader, DWORD dwStreamIndex)
{
    IMFMediaType *pNativeType = NULL;
    IMFMediaType *pType = NULL;

    // Find the native format of the stream.
    HRESULT hr = pReader->GetNativeMediaType(dwStreamIndex, 0, &pNativeType);
    if (FAILED(hr))
    {
        return hr;
    }

    GUID majorType, subtype;

    // Find the major type.
    hr = pNativeType->GetGUID(MF_MT_MAJOR_TYPE, &majorType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Define the output type.
    hr = MFCreateMediaType(&pType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetGUID(MF_MT_MAJOR_TYPE, majorType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Select a subtype.
    if (majorType == MFMediaType_Video)
    {
        subtype= MFVideoFormat_RGB32;
    }
    else if (majorType == MFMediaType_Audio)
    {
        subtype = MFAudioFormat_PCM;
    }
    else
    {
        // Unrecognized type. Skip.
        goto done;
    }

    hr = pType->SetGUID(MF_MT_SUBTYPE, subtype);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the uncompressed format.
    hr = pReader->SetCurrentMediaType(dwStreamIndex, NULL, pType);
    if (FAILED(hr))
    {
        goto done;
    }

done:
    SafeRelease(&pNativeType);
    SafeRelease(&pType);
    return hr;
}
```



## <a name="processing-media-data"></a>Elaborazione dei dati multimediali

Per ottenere i dati multimediali dall'origine, chiamare il metodo [**IMFSourceReader:: ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) , come illustrato nel codice seguente.


```C++
        DWORD streamIndex, flags;
        LONGLONG llTimeStamp;

        hr = pReader->ReadSample(
            MF_SOURCE_READER_ANY_STREAM,    // Stream index.
            0,                              // Flags.
            &streamIndex,                   // Receives the actual stream index. 
            &flags,                         // Receives status flags.
            &llTimeStamp,                   // Receives the time stamp.
            &pSample                        // Receives the sample or NULL.
            );
```



Il primo parametro è l'indice del flusso per il quale si desidera ottenere i dati. È anche possibile specificare **MF \_ source \_ Reader \_ Any \_ Stream** per ottenere i dati disponibili successivi da qualsiasi flusso. Il secondo parametro contiene flag facoltativi. per un elenco di questi, vedere il [**flag di controllo del \_ lettore di origine \_ \_ \_ MF**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_control_flag) . Il terzo parametro riceve l'indice del flusso che produce effettivamente i dati. Queste informazioni sono necessarie se si imposta il primo parametro su **MF \_ source \_ Reader \_ Any \_ Stream**. Il quarto parametro riceve i flag di stato, che indicano vari eventi che possono verificarsi durante la lettura dei dati, ad esempio le modifiche al formato nel flusso. Per un elenco di flag di stato, [**vedere \_ \_ \_ flag di lettura origine MF**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_flag).

Se l'origine del supporto è in grado di produrre dati per il flusso richiesto, l'ultimo parametro di [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) riceve un puntatore all'interfaccia [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) di un oggetto di esempio multimediale. Usare l'esempio di supporto per:

-   Ottenere un puntatore ai dati multimediali.
-   Ottenere l'ora di presentazione e la durata del campione.
-   Ottiene gli attributi che descrivono l'interlacciamento, la dominanza dei campi e altri aspetti dell'esempio.

Il contenuto dei dati multimediali dipende dal formato del flusso. Per un flusso video non compresso, ogni esempio multimediale contiene un singolo frame video. Per un flusso audio non compresso, ogni esempio di supporto contiene una sequenza di frame audio.

Il metodo [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) può restituire **S \_ OK** e non restituisce ancora un esempio multimediale nel parametro *pSample* . Ad esempio, quando si raggiunge la fine del file, **ReadSample** imposta il flag **MF \_ source \_ READERF \_ ENDOFSTREAM** in *dwFlags* e imposta *pSample* su **null**. In questo caso, il metodo **ReadSample** restituisce **S \_ OK** perché non si è verificato alcun errore, anche se il parametro *pSample* è impostato su **null**. Quindi, controllare sempre il valore di *pSample* prima di dereferenziarlo.

Il codice seguente illustra come chiamare [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) in un ciclo e controllare le informazioni restituite dal metodo, fino a quando non viene raggiunta la fine del file multimediale.


```C++
HRESULT ProcessSamples(IMFSourceReader *pReader)
{
    HRESULT hr = S_OK;
    IMFSample *pSample = NULL;
    size_t  cSamples = 0;

    bool quit = false;
    while (!quit)
    {
        DWORD streamIndex, flags;
        LONGLONG llTimeStamp;

        hr = pReader->ReadSample(
            MF_SOURCE_READER_ANY_STREAM,    // Stream index.
            0,                              // Flags.
            &streamIndex,                   // Receives the actual stream index. 
            &flags,                         // Receives status flags.
            &llTimeStamp,                   // Receives the time stamp.
            &pSample                        // Receives the sample or NULL.
            );

        if (FAILED(hr))
        {
            break;
        }

        wprintf(L"Stream %d (%I64d)\n", streamIndex, llTimeStamp);
        if (flags & MF_SOURCE_READERF_ENDOFSTREAM)
        {
            wprintf(L"\tEnd of stream\n");
            quit = true;
        }
        if (flags & MF_SOURCE_READERF_NEWSTREAM)
        {
            wprintf(L"\tNew stream\n");
        }
        if (flags & MF_SOURCE_READERF_NATIVEMEDIATYPECHANGED)
        {
            wprintf(L"\tNative type changed\n");
        }
        if (flags & MF_SOURCE_READERF_CURRENTMEDIATYPECHANGED)
        {
            wprintf(L"\tCurrent type changed\n");
        }
        if (flags & MF_SOURCE_READERF_STREAMTICK)
        {
            wprintf(L"\tStream tick\n");
        }

        if (flags & MF_SOURCE_READERF_NATIVEMEDIATYPECHANGED)
        {
            // The format changed. Reconfigure the decoder.
            hr = ConfigureDecoder(pReader, streamIndex);
            if (FAILED(hr))
            {
                break;
            }
        }

        if (pSample)
        {
            ++cSamples;
        }

        SafeRelease(&pSample);
    }

    if (FAILED(hr))
    {
        wprintf(L"ProcessSamples FAILED, hr = 0x%x\n", hr);
    }
    else
    {
        wprintf(L"Processed %d samples\n", cSamples);
    }
    SafeRelease(&pSample);
    return hr;
}
```



## <a name="draining-the-data-pipeline"></a>Svuotamento della pipeline di dati

Durante l'elaborazione dei dati, un decodificatore o un'altra trasformazione può memorizzare nel buffer esempi di input. Nel diagramma seguente l'applicazione chiama [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) e riceve un campione con un'ora di presentazione uguale a *T1*. Il decodificatore contiene esempi per *T2* e *T3*.

![illustrazione che mostra il buffering in un decodificatore.](images/sourcereader02.png)

Alla successiva chiamata a [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample), il lettore di origine potrebbe assegnare *T4* al decodificatore e restituire *T2* all'applicazione.

Se si desidera decodificare tutti gli esempi attualmente memorizzati nel buffer nel decodificatore, senza passare i nuovi esempi al decodificatore, impostare il flag di **\_ \_ \_ \_ svuotamento CONTROLF di MF source Reader** nel parametro *dwControlFlags* di [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample). Continuare a eseguire questa operazione in un ciclo fino a quando **ReadSample** non restituisce un puntatore di esempio **null** . A seconda del modo in cui il decodificatore memorizza nel buffer gli esempi, questo potrebbe verificarsi immediatamente o dopo diverse chiamate a **ReadSample**.

## <a name="getting-the-file-duration"></a>Recupero della durata del file

Per ottenere la durata di un file multimediale, chiamare il metodo [**IMFSourceReader:: GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) e richiedere l'attributo [**MF \_ PD \_ Duration**](mf-pd-duration-attribute.md) , come illustrato nel codice seguente.


```C++
HRESULT GetDuration(IMFSourceReader *pReader, LONGLONG *phnsDuration)
{
    PROPVARIANT var;
    HRESULT hr = pReader->GetPresentationAttribute(MF_SOURCE_READER_MEDIASOURCE, 
        MF_PD_DURATION, &var);
    if (SUCCEEDED(hr))
    {
        hr = PropVariantToInt64(var, phnsDuration);
        PropVariantClear(&var);
    }
    return hr;
}
```



La funzione illustrata di seguito consente di ottenere la durata in unità di 100 nanosecondi. Dividere per 10 milioni per ottenere la durata in secondi.

## <a name="seeking"></a>La ricerca

Un'origine multimediale che ottiene dati da un file locale può in genere eseguire ricerche in posizioni arbitrarie nel file. I dispositivi di acquisizione, ad esempio le webcam, in genere non possono eseguire ricerche, perché i dati sono Live. Un'origine che trasmette i dati in una rete potrebbe essere in grado di eseguire ricerche, a seconda del protocollo di streaming di rete.

Per determinare se un'origine multimediale può eseguire ricerche, chiamare [**IMFSourceReader:: GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) e richiedere l'attributo delle [ \_ \_ \_ \_ caratteristiche di lettura origine (MF](mf-source-reader-mediasource-characteristics.md) ), come illustrato nel codice seguente:


```C++
HRESULT GetSourceFlags(IMFSourceReader *pReader, ULONG *pulFlags)
{
    ULONG flags = 0;

    PROPVARIANT var;
    PropVariantInit(&var);

    HRESULT hr = pReader->GetPresentationAttribute(
        MF_SOURCE_READER_MEDIASOURCE, 
        MF_SOURCE_READER_MEDIASOURCE_CHARACTERISTICS, 
        &var);

    if (SUCCEEDED(hr))
    {
        hr = PropVariantToUInt32(var, &flags);
    }
    if (SUCCEEDED(hr))
    {
        *pulFlags = flags;
    }

    PropVariantClear(&var);
    return hr;
}
```



Questa funzione ottiene un set di flag di funzionalità dall'origine. Questi flag sono definiti nell'enumerazione [**delle \_ caratteristiche MFMEDIASOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) . Due flag sono correlati alla ricerca:



| Flag                                                                                                                                      | Descrizione                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFMEDIASOURCE_CAN_SEEK"></span><span id="mfmediasource_can_seek"></span>**MFMEDIASOURCE \_ può \_ cercare**<br/>                 | L'origine è in grado di cercare.<br/>                                                                                                                                                                            |
| <span id="MFMEDIASOURCE_HAS_SLOW_SEEK"></span><span id="mfmediasource_has_slow_seek"></span>**MFMEDIASOURCE \_ con \_ \_ ricerca lenta**<br/> | Il completamento della ricerca potrebbe richiedere molto tempo. Ad esempio, l'origine potrebbe dover scaricare l'intero file prima che possa essere cercato. Non esistono criteri severi per l'origine per restituire questo flag.<br/> |



 

I test di codice seguenti per **MFMEDIASOURCE \_ possono \_ cercare** flag.


```C++
BOOL SourceCanSeek(IMFSourceReader *pReader)
{
    BOOL bCanSeek = FALSE;
    ULONG flags;
    if (SUCCEEDED(GetSourceFlags(pReader, &flags)))
    {
        bCanSeek = ((flags & MFMEDIASOURCE_CAN_SEEK) == MFMEDIASOURCE_CAN_SEEK);
    }
    return bCanSeek;
}
```



Per eseguire la ricerca, chiamare il metodo [**IMFSourceReader:: SetCurrentPosition**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentposition) , come illustrato nel codice seguente.


```C++
HRESULT SetPosition(IMFSourceReader *pReader, const LONGLONG& hnsPosition)
{
    PROPVARIANT var;
    HRESULT hr = InitPropVariantFromInt64(hnsPosition, &var);
    if (SUCCEEDED(hr))
    {
        hr = pReader->SetCurrentPosition(GUID_NULL, var);
        PropVariantClear(&var);
    }
    return hr;
}
```



Il primo parametro fornisce il formato di ora utilizzato per specificare la posizione di ricerca. Tutte le origini multimediali in Media Foundation sono necessarie per supportare unità 100-nanosecondi, indicate dal valore **\_ null GUID**. Il secondo parametro è un **PROPVARIANT** che contiene la posizione di ricerca. Per le unità di tempo di 100 nanosecondi, il tipo di dati è **LONGLONG**.

Tenere presente che non tutte le origini supporti forniscono la ricerca con precisione del frame. L'accuratezza della ricerca dipende da diversi fattori, ad esempio l'intervallo del fotogramma chiave, se il file multimediale contiene un indice e se i dati hanno una velocità in bit costante o variabile. Pertanto, dopo la ricerca in una posizione in un file, non esiste alcuna garanzia che il timestamp del campione successivo corrisponda esattamente alla posizione richiesta. In genere, la posizione effettiva non sarà successiva alla posizione richiesta, pertanto è possibile rimuovere gli esempi fino a raggiungere il punto desiderato nel flusso.

## <a name="playback-rate"></a>Velocità di riproduzione

Sebbene sia possibile impostare la velocità di riproduzione usando il lettore di origine, l'operazione non è in genere molto utile per i motivi seguenti:

-   Il lettore di origine non supporta la riproduzione inversa, anche se l'origine multimediale lo esegue.
-   L'applicazione controlla i tempi di presentazione, in modo che l'applicazione possa implementare una riproduzione veloce o lenta senza impostare la frequenza nell'origine.
-   Alcune origini supporti supportano la modalità di *assottigliamento* , in cui l'origine fornisce un minor numero di campioni, in genere solo i fotogrammi chiave. Tuttavia, se si desidera eliminare i fotogrammi non chiave, è possibile controllare ogni esempio per l' [attributo \_ CleanPoint di MFSampleExtension](mfsampleextension-cleanpoint-attribute.md) .

Per impostare la velocità di riproduzione usando il lettore di origine, chiamare il metodo [**IMFSourceReader:: GetServiceForStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getserviceforstream) per ottenere le interfacce [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) e [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) dall'origine multimediale.

## <a name="hardware-acceleration"></a>Accelerazione hardware

Il lettore di origine è compatibile con Microsoft DirectX Video Acceleration (DXVA) 2,0 per la decodifica video con accelerazione hardware. Per usare DXVA con il lettore di origine, seguire questa procedura.

1.  Creare un dispositivo Microsoft Direct3D.
2.  Chiamare la funzione [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9) per creare la gestione dispositivi Direct3D. Questa funzione ottiene un puntatore all'interfaccia [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) .
3.  Chiamare il metodo [**IDirect3DDeviceManager9:: ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) con un puntatore al dispositivo Direct3D.
4.  Creare un archivio di attributi chiamando la funzione [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) .
5.  Creare il lettore di origine. Passare l'archivio di attributi nel parametro *pAttributes* della funzione di creazione.

Quando si fornisce un dispositivo Direct3D, il lettore di origine alloca gli esempi video compatibili con l'API DXVA video processor. È possibile usare l'elaborazione video DXVA per eseguire la deinterlacciamento hardware o la combinazione di video. Per ulteriori informazioni, vedere [DXVA video processing](dxva-video-processing.md). Inoltre, se il decodificatore supporta DXVA 2,0, utilizzerà il dispositivo Direct3D per eseguire la decodifica con accelerazione hardware.

> [!IMPORTANT]
> A partire da Windows 8, è possibile usare [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) invece di [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9). Per le app di Windows Store, è necessario usare **IMFDXGIDeviceManager**. Per altre informazioni, vedere le [API video di Direct3D 11](direct3d-11-video-apis.md).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Lettore di origine](source-reader.md)
</dt> </dl>

 

 




