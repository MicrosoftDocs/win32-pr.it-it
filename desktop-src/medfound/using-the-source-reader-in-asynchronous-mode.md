---
description: In questo argomento viene descritto come utilizzare il lettore di origine in modalità asincrona.
ms.assetid: 9D3C2780-D7DB-4151-8474-9A19EC94F6BE
title: Utilizzo del lettore di origine in modalità asincrona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 357d0405cb3e594d059b7c93e793250e0be88562
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049655"
---
# <a name="using-the-source-reader-in-asynchronous-mode"></a>Utilizzo del lettore di origine in modalità asincrona

In questo argomento viene descritto come utilizzare il [lettore di origine](source-reader.md) in modalità asincrona. In modalità asincrona, l'applicazione fornisce un'interfaccia di callback, che viene usata per notificare all'applicazione che i dati sono disponibili.

In questo argomento si presuppone che l'utente abbia già letto l'argomento [utilizzo del lettore di origine per l'elaborazione dei dati multimediali](processing-media-data-with-the-source-reader.md).

## <a name="using-asynchronous-mode"></a>Uso della modalità asincrona

Il lettore di origine funziona in modalità sincrona o asincrona. Nell'esempio di codice illustrato nella sezione precedente si presuppone che il lettore di origine usi la modalità sincrona, che è l'impostazione predefinita. In modalità sincrona, il metodo [**IMFSourceReader:: ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) si blocca mentre l'origine multimediale produce l'esempio successivo. Un'origine multimediale acquisisce in genere i dati da un'origine esterna, ad esempio un file locale o una connessione di rete, in modo che il metodo possa bloccare il thread chiamante per un periodo di tempo significativo.

In modalità asincrona, il [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) viene restituito immediatamente e il lavoro viene eseguito in un altro thread. Al termine dell'operazione, il lettore di origine chiama l'applicazione tramite l'interfaccia di callback [**IMFSourceReaderCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback) . Per usare la modalità asincrona, è necessario fornire un puntatore di callback quando si crea per la prima volta il lettore di origine, come indicato di seguito:

1.  Creare un archivio di attributi chiamando la funzione [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) .
2.  Impostare l'attributo di [ \_ \_ \_ \_ callback asincrono di MF source Reader](mf-source-reader-async-callback.md) nell'archivio di attributi. Il valore dell'attributo è un puntatore all'oggetto callback.
3.  Quando si crea il lettore di origine, passare l'archivio attributi alla funzione di creazione nel parametro *pAttributes* . Tutte le funzioni per la creazione del lettore di origine dispongono di questo parametro.

Nell'esempio seguente sono illustrati i passaggi per l'operazione.


```C++
HRESULT CreateSourceReaderAsync(
    PCWSTR pszURL, 
    IMFSourceReaderCallback *pCallback, 
    IMFSourceReader **ppReader)
{
    HRESULT hr = S_OK;
    IMFAttributes *pAttributes = NULL;

    hr = MFCreateAttributes(&pAttributes, 1);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAttributes->SetUnknown(MF_SOURCE_READER_ASYNC_CALLBACK, pCallback);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFCreateSourceReaderFromURL(pszURL, pAttributes, ppReader);

done:
    SafeRelease(&pAttributes);
    return hr;
}
```



Dopo aver creato il lettore di origine, non è possibile passare da una modalità all'altra sincrona a una asincrona.

Per ottenere i dati in modalità asincrona, chiamare il metodo [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) , ma impostare gli ultimi quattro parametri su **null**, come illustrato nell'esempio seguente.


```C++
    // Request the first sample.
    hr = pReader->ReadSample(MF_SOURCE_READER_FIRST_VIDEO_STREAM, 
        0, NULL, NULL, NULL, NULL);
```



Quando il metodo [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) viene completato in modo asincrono, il lettore di origine chiama il metodo [**IMFSourceReaderCallback:: OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) . Questo metodo ha cinque parametri:

-   *hrStatus*: contiene un valore **HRESULT** . Si tratta dello stesso valore restituito da [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) in modalità sincrona. Se *hrStatus* contiene un codice di errore, è possibile ignorare i parametri rimanenti.
-   *dwStreamIndex*, *dwStreamFlags*, llTimestamp e *pSample*: questi tre parametri sono equivalenti agli ultimi tre parametri in [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample). Contengono rispettivamente il numero di flusso, i flag di stato e il puntatore [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) .


```C++
    STDMETHODIMP OnReadSample(HRESULT hrStatus, DWORD dwStreamIndex,
        DWORD dwStreamFlags, LONGLONG llTimestamp, IMFSample *pSample);
```



Inoltre, l'interfaccia di callback definisce altri due metodi:

-   [**OnEvent**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onevent). Invia una notifica all'applicazione quando si verificano determinati eventi nell'origine multimediale, ad esempio gli eventi di connessione di rete o di buffering.
-   [**OnFlush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onflush). Chiamato quando il metodo [**Flush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-flush) viene completato.

## <a name="implementing-the-callback-interface"></a>Implementazione dell'interfaccia di callback

L'interfaccia di callback deve essere thread-safe, perché [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) e gli altri metodi di callback vengono chiamati dai thread di lavoro.

Quando si implementa il callback, è possibile adottare diversi approcci. Ad esempio, è possibile eseguire tutte le operazioni all'interno del callback oppure è possibile usare il callback per inviare una notifica all'applicazione, ad esempio segnalando un handle di evento, quindi eseguire operazioni dal thread dell'applicazione.

Il metodo [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) verrà chiamato una volta per ogni chiamata eseguita al metodo [**IMFSourceReader:: ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) . Per ottenere l'esempio successivo, chiamare di nuovo **ReadSample** . Se si verifica un errore, viene chiamato **OnReadSample** con un codice di errore per il parametro *hrStatus* .

Nell'esempio seguente viene illustrata un'implementazione minima dell'interfaccia di callback. In primo luogo, di seguito è illustrata la dichiarazione di una classe che implementa l'interfaccia.


```C++
#include <shlwapi.h>

class SourceReaderCB : public IMFSourceReaderCallback
{
public:
    SourceReaderCB(HANDLE hEvent) : 
      m_nRefCount(1), m_hEvent(hEvent), m_bEOS(FALSE), m_hrStatus(S_OK)
    {
        InitializeCriticalSection(&m_critsec);
    }

    // IUnknown methods
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv)
    {
        static const QITAB qit[] =
        {
            QITABENT(SourceReaderCB, IMFSourceReaderCallback),
            { 0 },
        };
        return QISearch(this, qit, iid, ppv);
    }
    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_nRefCount);
    }
    STDMETHODIMP_(ULONG) Release()
    {
        ULONG uCount = InterlockedDecrement(&m_nRefCount);
        if (uCount == 0)
        {
            delete this;
        }
        return uCount;
    }

    // IMFSourceReaderCallback methods
    STDMETHODIMP OnReadSample(HRESULT hrStatus, DWORD dwStreamIndex,
        DWORD dwStreamFlags, LONGLONG llTimestamp, IMFSample *pSample);

    STDMETHODIMP OnEvent(DWORD, IMFMediaEvent *)
    {
        return S_OK;
    }

    STDMETHODIMP OnFlush(DWORD)
    {
        return S_OK;
    }

public:
    HRESULT Wait(DWORD dwMilliseconds, BOOL *pbEOS)
    {
        *pbEOS = FALSE;

        DWORD dwResult = WaitForSingleObject(m_hEvent, dwMilliseconds);
        if (dwResult == WAIT_TIMEOUT)
        {
            return E_PENDING;
        }
        else if (dwResult != WAIT_OBJECT_0)
        {
            return HRESULT_FROM_WIN32(GetLastError());
        }

        *pbEOS = m_bEOS;
        return m_hrStatus;
    }
    
private:
    
    // Destructor is private. Caller should call Release.
    virtual ~SourceReaderCB() 
    {
    }

    void NotifyError(HRESULT hr)
    {
        wprintf(L"Source Reader error: 0x%X\n", hr);
    }

private:
    long                m_nRefCount;        // Reference count.
    CRITICAL_SECTION    m_critsec;
    HANDLE              m_hEvent;
    BOOL                m_bEOS;
    HRESULT             m_hrStatus;

};
```



In questo esempio non sono interessati ai metodi [**OnEvent**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onevent) e [**OnFlush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onflush) , quindi semplicemente restituiscono **S \_ OK**. La classe usa un handle di evento per segnalare l'applicazione; Questo handle viene fornito tramite il costruttore.

In questo esempio minimo il metodo [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) stampa semplicemente il timestamp nella finestra della console. Archivia quindi il codice di stato e il flag di fine del flusso e segnala l'handle dell'evento:


```C++
HRESULT SourceReaderCB::OnReadSample(
    HRESULT hrStatus,
    DWORD /* dwStreamIndex */,
    DWORD dwStreamFlags,
    LONGLONG llTimestamp,
    IMFSample *pSample      // Can be NULL
    )
{
    EnterCriticalSection(&m_critsec);

    if (SUCCEEDED(hrStatus))
    {
        if (pSample)
        {
            // Do something with the sample.
            wprintf(L"Frame @ %I64d\n", llTimestamp);
        }
    }
    else
    {
        // Streaming error.
        NotifyError(hrStatus);
    }

    if (MF_SOURCE_READERF_ENDOFSTREAM & dwStreamFlags)
    {
        // Reached the end of the stream.
        m_bEOS = TRUE;
    }
    m_hrStatus = hrStatus;

    LeaveCriticalSection(&m_critsec);
    SetEvent(m_hEvent);
    return S_OK;
}
```



Il codice seguente mostra che l'applicazione userà questa classe di callback per leggere tutti i fotogrammi video da un file multimediale:


```C++
HRESULT ReadMediaFile(PCWSTR pszURL)
{
    HRESULT hr = S_OK;

    IMFSourceReader *pReader = NULL;
    SourceReaderCB *pCallback = NULL;

    HANDLE hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
    if (hEvent == NULL)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        goto done;
    }

    // Create an instance of the callback object.
    pCallback = new (std::nothrow) SourceReaderCB(hEvent);
    if (pCallback == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    // Create the Source Reader.
    hr = CreateSourceReaderAsync(pszURL, pCallback, &pReader);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = ConfigureDecoder(pReader, MF_SOURCE_READER_FIRST_VIDEO_STREAM);
    if (FAILED(hr))
    {
        goto done;
    }

    // Request the first sample.
    hr = pReader->ReadSample(MF_SOURCE_READER_FIRST_VIDEO_STREAM, 
        0, NULL, NULL, NULL, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    while (SUCCEEDED(hr))
    {
        BOOL bEOS;
        hr = pCallback->Wait(INFINITE, &bEOS);
        if (FAILED(hr) || bEOS)
        {
            break;
        }
        hr = pReader->ReadSample(MF_SOURCE_READER_FIRST_VIDEO_STREAM,
            0, NULL, NULL, NULL, NULL);
    }

done:
    SafeRelease(&pReader);
    SafeRelease(&pCallback);
    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Lettore di origine](source-reader.md)
</dt> </dl>

 

 



