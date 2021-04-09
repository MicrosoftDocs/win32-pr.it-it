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
# <a name="using-the-source-reader-in-asynchronous-mode"></a><span data-ttu-id="6269a-103">Utilizzo del lettore di origine in modalità asincrona</span><span class="sxs-lookup"><span data-stu-id="6269a-103">Using the Source Reader in Asynchronous Mode</span></span>

<span data-ttu-id="6269a-104">In questo argomento viene descritto come utilizzare il [lettore di origine](source-reader.md) in modalità asincrona.</span><span class="sxs-lookup"><span data-stu-id="6269a-104">This topic describes how to use the [Source Reader](source-reader.md) in asynchronous mode.</span></span> <span data-ttu-id="6269a-105">In modalità asincrona, l'applicazione fornisce un'interfaccia di callback, che viene usata per notificare all'applicazione che i dati sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="6269a-105">In asynchronous mode, the application provides a callback interface, which is used to notify the application that data is available.</span></span>

<span data-ttu-id="6269a-106">In questo argomento si presuppone che l'utente abbia già letto l'argomento [utilizzo del lettore di origine per l'elaborazione dei dati multimediali](processing-media-data-with-the-source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="6269a-106">This topic assumes that you have already read the topic [Using the Source Reader to Process Media Data](processing-media-data-with-the-source-reader.md).</span></span>

## <a name="using-asynchronous-mode"></a><span data-ttu-id="6269a-107">Uso della modalità asincrona</span><span class="sxs-lookup"><span data-stu-id="6269a-107">Using Asynchronous Mode</span></span>

<span data-ttu-id="6269a-108">Il lettore di origine funziona in modalità sincrona o asincrona.</span><span class="sxs-lookup"><span data-stu-id="6269a-108">The Source Reader operates either in synchronous mode or asynchronous mode.</span></span> <span data-ttu-id="6269a-109">Nell'esempio di codice illustrato nella sezione precedente si presuppone che il lettore di origine usi la modalità sincrona, che è l'impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="6269a-109">The code example shown in the previous section assumes that the Source Reader is using synchronous mode, which is the default.</span></span> <span data-ttu-id="6269a-110">In modalità sincrona, il metodo [**IMFSourceReader:: ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) si blocca mentre l'origine multimediale produce l'esempio successivo.</span><span class="sxs-lookup"><span data-stu-id="6269a-110">In synchronous mode, the [**IMFSourceReader::ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) method blocks while the media source produces the next sample.</span></span> <span data-ttu-id="6269a-111">Un'origine multimediale acquisisce in genere i dati da un'origine esterna, ad esempio un file locale o una connessione di rete, in modo che il metodo possa bloccare il thread chiamante per un periodo di tempo significativo.</span><span class="sxs-lookup"><span data-stu-id="6269a-111">A media source typically acquires data from some external source (such as a local file or a network connection), so the method can block the calling thread for a noticeable amount of time.</span></span>

<span data-ttu-id="6269a-112">In modalità asincrona, il [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) viene restituito immediatamente e il lavoro viene eseguito in un altro thread.</span><span class="sxs-lookup"><span data-stu-id="6269a-112">In asynchronous mode, the [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) returns immediately and the work is performed on another thread.</span></span> <span data-ttu-id="6269a-113">Al termine dell'operazione, il lettore di origine chiama l'applicazione tramite l'interfaccia di callback [**IMFSourceReaderCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback) .</span><span class="sxs-lookup"><span data-stu-id="6269a-113">After the operation is complete, the Source Reader calls the application through the [**IMFSourceReaderCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback) callback interface.</span></span> <span data-ttu-id="6269a-114">Per usare la modalità asincrona, è necessario fornire un puntatore di callback quando si crea per la prima volta il lettore di origine, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="6269a-114">To use asynchronous mode, you must provide a callback pointer when you first create the Source Reader, as follows:</span></span>

1.  <span data-ttu-id="6269a-115">Creare un archivio di attributi chiamando la funzione [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) .</span><span class="sxs-lookup"><span data-stu-id="6269a-115">Create an attribute store by calling the [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) function.</span></span>
2.  <span data-ttu-id="6269a-116">Impostare l'attributo di [ \_ \_ \_ \_ callback asincrono di MF source Reader](mf-source-reader-async-callback.md) nell'archivio di attributi.</span><span class="sxs-lookup"><span data-stu-id="6269a-116">Set the [MF\_SOURCE\_READER\_ASYNC\_CALLBACK](mf-source-reader-async-callback.md) attribute on the attribute store.</span></span> <span data-ttu-id="6269a-117">Il valore dell'attributo è un puntatore all'oggetto callback.</span><span class="sxs-lookup"><span data-stu-id="6269a-117">The attribute value is a pointer to your callback object.</span></span>
3.  <span data-ttu-id="6269a-118">Quando si crea il lettore di origine, passare l'archivio attributi alla funzione di creazione nel parametro *pAttributes* .</span><span class="sxs-lookup"><span data-stu-id="6269a-118">When you create the Source Reader, pass the attribute store to the creation function in the *pAttributes* parameter.</span></span> <span data-ttu-id="6269a-119">Tutte le funzioni per la creazione del lettore di origine dispongono di questo parametro.</span><span class="sxs-lookup"><span data-stu-id="6269a-119">All of the functions to create the Source Reader have this parameter.</span></span>

<span data-ttu-id="6269a-120">Nell'esempio seguente sono illustrati i passaggi per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="6269a-120">The following example shows these steps.</span></span>


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



<span data-ttu-id="6269a-121">Dopo aver creato il lettore di origine, non è possibile passare da una modalità all'altra sincrona a una asincrona.</span><span class="sxs-lookup"><span data-stu-id="6269a-121">After you create the Source Reader, you cannot switch modes between synchronous and asynchronous.</span></span>

<span data-ttu-id="6269a-122">Per ottenere i dati in modalità asincrona, chiamare il metodo [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) , ma impostare gli ultimi quattro parametri su **null**, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="6269a-122">To get data in asynchronous mode, call the [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) method but set the last four parameters to **NULL**, as shown in the following example.</span></span>


```C++
    // Request the first sample.
    hr = pReader->ReadSample(MF_SOURCE_READER_FIRST_VIDEO_STREAM, 
        0, NULL, NULL, NULL, NULL);
```



<span data-ttu-id="6269a-123">Quando il metodo [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) viene completato in modo asincrono, il lettore di origine chiama il metodo [**IMFSourceReaderCallback:: OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) .</span><span class="sxs-lookup"><span data-stu-id="6269a-123">When the [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) method completes asynchronously, the Source Reader calls your [**IMFSourceReaderCallback::OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) method.</span></span> <span data-ttu-id="6269a-124">Questo metodo ha cinque parametri:</span><span class="sxs-lookup"><span data-stu-id="6269a-124">This method has five parameters:</span></span>

-   <span data-ttu-id="6269a-125">*hrStatus*: contiene un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6269a-125">*hrStatus*: Contains an **HRESULT** value.</span></span> <span data-ttu-id="6269a-126">Si tratta dello stesso valore restituito da [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) in modalità sincrona.</span><span class="sxs-lookup"><span data-stu-id="6269a-126">This is the same value that [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) would return in synchronous mode.</span></span> <span data-ttu-id="6269a-127">Se *hrStatus* contiene un codice di errore, è possibile ignorare i parametri rimanenti.</span><span class="sxs-lookup"><span data-stu-id="6269a-127">If *hrStatus* contains an error code, you can ignore the remaining parameters.</span></span>
-   <span data-ttu-id="6269a-128">*dwStreamIndex*, *dwStreamFlags*, llTimestamp e *pSample*: questi tre parametri sono equivalenti agli ultimi tre parametri in [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample).</span><span class="sxs-lookup"><span data-stu-id="6269a-128">*dwStreamIndex*, *dwStreamFlags*, llTimestamp, and *pSample*: These three parameters are equivalent to the last three parameters in [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample).</span></span> <span data-ttu-id="6269a-129">Contengono rispettivamente il numero di flusso, i flag di stato e il puntatore [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) .</span><span class="sxs-lookup"><span data-stu-id="6269a-129">They contain the stream number, status flags, and [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) pointer, respectively.</span></span>


```C++
    STDMETHODIMP OnReadSample(HRESULT hrStatus, DWORD dwStreamIndex,
        DWORD dwStreamFlags, LONGLONG llTimestamp, IMFSample *pSample);
```



<span data-ttu-id="6269a-130">Inoltre, l'interfaccia di callback definisce altri due metodi:</span><span class="sxs-lookup"><span data-stu-id="6269a-130">In addition, the callback interface defines two other methods:</span></span>

-   <span data-ttu-id="6269a-131">[**OnEvent**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onevent).</span><span class="sxs-lookup"><span data-stu-id="6269a-131">[**OnEvent**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onevent).</span></span> <span data-ttu-id="6269a-132">Invia una notifica all'applicazione quando si verificano determinati eventi nell'origine multimediale, ad esempio gli eventi di connessione di rete o di buffering.</span><span class="sxs-lookup"><span data-stu-id="6269a-132">Notifies the application when certain events occur in media source, such as buffering or network connection events.</span></span>
-   <span data-ttu-id="6269a-133">[**OnFlush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onflush).</span><span class="sxs-lookup"><span data-stu-id="6269a-133">[**OnFlush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onflush).</span></span> <span data-ttu-id="6269a-134">Chiamato quando il metodo [**Flush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-flush) viene completato.</span><span class="sxs-lookup"><span data-stu-id="6269a-134">Called when the [**Flush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-flush) method completes.</span></span>

## <a name="implementing-the-callback-interface"></a><span data-ttu-id="6269a-135">Implementazione dell'interfaccia di callback</span><span class="sxs-lookup"><span data-stu-id="6269a-135">Implementing the Callback Interface</span></span>

<span data-ttu-id="6269a-136">L'interfaccia di callback deve essere thread-safe, perché [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) e gli altri metodi di callback vengono chiamati dai thread di lavoro.</span><span class="sxs-lookup"><span data-stu-id="6269a-136">The callback interface must be thread-safe, because [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) and the other callback methods are called from worker threads.</span></span>

<span data-ttu-id="6269a-137">Quando si implementa il callback, è possibile adottare diversi approcci.</span><span class="sxs-lookup"><span data-stu-id="6269a-137">There are several different approaches you can take when you implement the callback.</span></span> <span data-ttu-id="6269a-138">Ad esempio, è possibile eseguire tutte le operazioni all'interno del callback oppure è possibile usare il callback per inviare una notifica all'applicazione, ad esempio segnalando un handle di evento, quindi eseguire operazioni dal thread dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6269a-138">For example, you can do all of the work inside the callback, or you can use the callback to notify the application (for example, by signaling an event handle) and then do work from the application thread.</span></span>

<span data-ttu-id="6269a-139">Il metodo [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) verrà chiamato una volta per ogni chiamata eseguita al metodo [**IMFSourceReader:: ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) .</span><span class="sxs-lookup"><span data-stu-id="6269a-139">The [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) method will be called once for every call that you make to the [**IMFSourceReader::ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) method.</span></span> <span data-ttu-id="6269a-140">Per ottenere l'esempio successivo, chiamare di nuovo **ReadSample** .</span><span class="sxs-lookup"><span data-stu-id="6269a-140">To get the next sample, call **ReadSample** again.</span></span> <span data-ttu-id="6269a-141">Se si verifica un errore, viene chiamato **OnReadSample** con un codice di errore per il parametro *hrStatus* .</span><span class="sxs-lookup"><span data-stu-id="6269a-141">If an error occurs, **OnReadSample** is called with an error code for the *hrStatus* parameter.</span></span>

<span data-ttu-id="6269a-142">Nell'esempio seguente viene illustrata un'implementazione minima dell'interfaccia di callback.</span><span class="sxs-lookup"><span data-stu-id="6269a-142">The following example shows a minimal implementation of the callback interface.</span></span> <span data-ttu-id="6269a-143">In primo luogo, di seguito è illustrata la dichiarazione di una classe che implementa l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6269a-143">First, here is the declaration of a class that implements the interface.</span></span>


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



<span data-ttu-id="6269a-144">In questo esempio non sono interessati ai metodi [**OnEvent**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onevent) e [**OnFlush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onflush) , quindi semplicemente restituiscono **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6269a-144">In this example, we are not interested in the [**OnEvent**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onevent) and [**OnFlush**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onflush) methods, so they simply return **S\_OK**.</span></span> <span data-ttu-id="6269a-145">La classe usa un handle di evento per segnalare l'applicazione; Questo handle viene fornito tramite il costruttore.</span><span class="sxs-lookup"><span data-stu-id="6269a-145">The class uses an event handle to signal the application; this handle is provided through the constructor.</span></span>

<span data-ttu-id="6269a-146">In questo esempio minimo il metodo [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) stampa semplicemente il timestamp nella finestra della console.</span><span class="sxs-lookup"><span data-stu-id="6269a-146">In this minimal example, the [**OnReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereadercallback-onreadsample) method just prints the time stamp to the console window.</span></span> <span data-ttu-id="6269a-147">Archivia quindi il codice di stato e il flag di fine del flusso e segnala l'handle dell'evento:</span><span class="sxs-lookup"><span data-stu-id="6269a-147">Then it stores the status code and the end-of-stream flag, and signals the event handle:</span></span>


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



<span data-ttu-id="6269a-148">Il codice seguente mostra che l'applicazione userà questa classe di callback per leggere tutti i fotogrammi video da un file multimediale:</span><span class="sxs-lookup"><span data-stu-id="6269a-148">The following code shows the application would use this callback class to read all of the video frames from a media file:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="6269a-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6269a-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6269a-150">Lettore di origine</span><span class="sxs-lookup"><span data-stu-id="6269a-150">Source Reader</span></span>](source-reader.md)
</dt> </dl>

 

 



