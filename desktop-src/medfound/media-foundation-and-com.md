---
description: Microsoft Media Foundation usa una combinazione di costrutti COM, ma non è un'API completamente basata su COM.
ms.assetid: d58ca46f-8f3a-4a12-b948-1ea7ab568788
title: Media Foundation e COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdb7d05bac6a3f4deef2c004c6980ef1351c3823
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320772"
---
# <a name="media-foundation-and-com"></a>Media Foundation e COM

Microsoft Media Foundation usa una combinazione di costrutti COM, ma non è un'API completamente basata su COM. In questo argomento viene descritta l'interazione tra COM e Media Foundation. Vengono inoltre definite alcune procedure consigliate per lo sviluppo di Media Foundation componenti plug-in. Seguendo queste procedure è possibile evitare alcuni errori di programmazione comuni ma minimi.

-   [Procedure consigliate per le applicazioni](#best-practices-for-applications)
-   [Procedure consigliate per i componenti di Media Foundation](#best-practices-for-media-foundation-components)
-   [Summary](#summary)
-   [Argomenti correlati](#related-topics)

## <a name="best-practices-for-applications"></a>Procedure consigliate per le applicazioni

In Media Foundation, l'elaborazione asincrona e i callback vengono gestiti dalle [code di lavoro](work-queues.md). Le code di lavoro hanno sempre thread di Apartment a thread multipli (MTA), pertanto un'applicazione avrà un'implementazione più semplice se viene eseguita anche su un thread MTA. È quindi consigliabile chiamare [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) con il flag **COinit \_ multithreading** .

Media Foundation non esegue il marshalling di oggetti Apartment a thread singolo (STA) a thread della coda di lavoro. Né garantisce che vengano mantenute le invarianti. Pertanto, un'applicazione STA deve prestare attenzione a non passare oggetti o proxy STA per Media Foundation API. Gli oggetti che sono solo sta non sono supportati in Media Foundation.

Se si dispone di un proxy STA per un MTA o di un oggetto a thread libero, è possibile effettuare il marshalling dell'oggetto in un proxy MTA usando un callback della coda di lavoro. La funzione [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) può restituire un puntatore non elaborato o un proxy sta, a seconda del modello a oggetti definito nel registro di sistema per il CLSID. Se viene restituito un proxy STA, non è necessario passare il puntatore a un'API Media Foundation.

Si supponga, ad esempio, di voler passare un puntatore **IPropertyStore** al metodo [**IMFSourceResolver:: BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) . È possibile chiamare **PSCreateMemoryPropertyStore** per creare il puntatore **IPropertyStore** . Se si chiama da un STA, è necessario effettuare il marshalling del puntatore prima di passarlo a **BeginCreateObjectFromURL**.

Il codice seguente illustra come effettuare il marshalling di un proxy STA in un'API Media Foundation.


```C++
class CCreateSourceMarshalCallback
    : public IMFAsyncCallback
{
public:
    CCreateSourceMarshalCallback(
        LPCWSTR szURL, 
        IMFSourceResolver* pResolver, 
        IPropertyStore* pSourceProps, 
        IMFAsyncCallback* pCompletionCallback, 
        HRESULT& hr
        )
        : m_szURL(szURL), 
          m_pResolver(pResolver), 
          m_pCompletionCallback(pCompletionCallback),
          m_pGIT(NULL),
          m_cRef(1)
    {
        hr = CoCreateInstance(CLSID_StdGlobalInterfaceTable, NULL, 
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&m_pGIT));

        if(SUCCEEDED(hr))
        {
            hr = m_pGIT->RegisterInterfaceInGlobal(
                pSourceProps, IID_IPropertyStore, &m_dwInterfaceCookie);
        }
    }
    ~CCreateSourceMarshalCallback()
    {
        SafeRelease(&m_pResolver);
        SafeRelease(&m_pCompletionCallback);
        SafeRelease(&m_pGIT);
    }


    STDMETHOD_(ULONG, AddRef)()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHOD_(ULONG, Release)()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (0 == cRef)
        {
            delete this;
        }
        return cRef;
    }

    STDMETHOD(QueryInterface)(REFIID riid, LPVOID* ppvObject)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CCreateSourceMarshalCallback, IMFAsyncCallback),
            { 0 }
        };
        return QISearch(this, qit, riid, ppvObject);

    }

    STDMETHOD(GetParameters)(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        return E_NOTIMPL;
    }

    STDMETHOD(Invoke)(IMFAsyncResult* pResult)
    {
        IPropertyStore *pSourceProps = NULL;

        HRESULT hr = m_pGIT->GetInterfaceFromGlobal(
            m_dwInterfaceCookie, 
            IID_PPV_ARGS(&pSourceProps)
            );

        if(SUCCEEDED(hr))
        {
            hr = m_pResolver->BeginCreateObjectFromURL(
                m_szURL, MF_RESOLUTION_MEDIASOURCE, pSourceProps, NULL, 
                m_pCompletionCallback, NULL);
        }

        SafeRelease(&pSourceProps);
        return hr;
    }

private:
    LPCWSTR m_szURL;
    IMFSourceResolver *m_pResolver;
    IMFAsyncCallback *m_pCompletionCallback;
    IGlobalInterfaceTable *m_pGIT;
    DWORD m_dwInterfaceCookie;
    LONG m_cRef;
};
```



Per ulteriori informazioni sulla tabella dell'interfaccia globale, vedere [**IGlobalInterfaceTable**](/windows/win32/api/objidl/nn-objidl-iglobalinterfacetable).

Se si usa Media Foundation in-process, gli oggetti restituiti da Media Foundation metodi e funzioni sono puntatori diretti all'oggetto. Per Media Foundation tra processi, questi oggetti possono essere proxy MTA ed è necessario eseguirne il marshalling in un thread STA se necessario. Analogamente, gli oggetti ottenuti all'interno di un callback, ad esempio una topologia dall'evento [MESessionTopologyStatus](mesessiontopologystatus.md) , sono puntatori diretti quando Media Foundation viene usato in-process, ma sono proxy MTA quando Media Foundation viene usato tra processi.

> [!Note]  
> Lo scenario più comune per l'uso di Media Foundation processo incrociato è con il [percorso multimediale protetto](protected-media-path.md) (PMP). Tuttavia, queste osservazioni si applicano a qualsiasi situazione in cui le API Media Foundation vengono usate tramite RPC.

 

Tutte le implementazioni di [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) devono essere compatibili con MTA. Questi oggetti non devono necessariamente essere oggetti COM. Tuttavia, in caso affermativo, non possono essere eseguiti nell'STA. La funzione [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) verrà richiamata su un thread WorkQueue MTA e l'oggetto [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) fornito sarà un puntatore a oggetto diretto o un proxy MTA.

## <a name="best-practices-for-media-foundation-components"></a>Procedure consigliate per i componenti di Media Foundation

Esistono due categorie di oggetti Media Foundation che devono essere interessati a COM. Alcuni componenti, ad esempio le trasformazioni o i gestori del flusso di byte, sono oggetti COM completi creati da CLSID. Questi oggetti devono rispettare le regole per gli apartment COM, sia per Media Foundation in-process che tra processi. Altri componenti Media Foundation non sono oggetti COM completi, ma sono necessari proxy COM per la riproduzione tra processi. Gli oggetti di questa categoria includono origini multimediali e oggetto attivazione. Questi oggetti possono ignorare i problemi di Apartment se verranno utilizzati solo per Media Foundation in-process.

Sebbene non tutti gli oggetti Media Foundation siano oggetti COM, tutte le interfacce Media Foundation derivano da [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown). Pertanto, tutti gli oggetti Media Foundation devono implementare **IUnknown** secondo le specifiche com, incluse le regole per il conteggio dei riferimenti e [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)). Tutti gli oggetti conteggiati a cui si fa riferimento devono inoltre garantire che [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow) non consenta lo scaricamento del modulo mentre gli oggetti rimangono persistenti.

Media Foundation componenti non possono essere oggetti STA. Molti oggetti Media Foundation non devono necessariamente essere oggetti COM. Tuttavia, in caso affermativo, non possono essere eseguiti nell'STA. Tutti i componenti Media Foundation devono essere thread-safe. Alcuni oggetti Media Foundation devono essere anche a thread libero o indipendente dall'Apartment. La tabella seguente specifica i requisiti per le implementazioni dell'interfaccia personalizzate:



| Interfaccia                                                          | Category            | Apartment obbligatorio       |
|--------------------------------------------------------------------|---------------------|--------------------------|
| [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)                                 | Proxy tra processi | A thread libero o neutro |
| [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)               | Oggetto COM          | MTA                      |
| [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) | Proxy tra processi | A thread libero o neutro |
| [**IMFQualityManager**](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager)                     | Oggetto COM          | A thread libero o neutro |
| [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                           | Proxy tra processi | A thread libero o neutro |
| [**IMFSchemeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler)                       | Oggetto COM          | MTA                      |
| [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)                             | Oggetto COM          | A thread libero o neutro |
| [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)                               | Oggetto COM          | MTA                      |



 

Potrebbero essere necessari requisiti aggiuntivi a seconda dell'implementazione. Se, ad esempio, un sink multimediale implementa un'altra interfaccia che consente all'applicazione di effettuare chiamate di funzione dirette al sink, il sink dovrà essere a thread libero o neutro, in modo da poter gestire le chiamate dirette tra processi. Qualsiasi oggetto può essere a thread libero. Questa tabella specifica i requisiti minimi.

Il metodo consigliato per implementare oggetti a thread libero o neutri consiste nell'aggregazione del gestore di marshalling a thread libero. Per ulteriori informazioni, vedere la documentazione MSDN su [**CoCreateFreeThreadedMarshaler**](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler). In conformità con la necessità di non passare gli oggetti o i proxy di STA a Media Foundation API, gli oggetti a thread libero non devono preoccuparsi di effettuare il marshalling dei puntatori di input STA nei componenti a thread libero.

I componenti che usano la coda di lavoro di funzione lunga (**\_ \_ \_ \_ funzione Long della coda di callback MFASYNC**) devono prestare maggiore attenzione. I thread nella funzione Long WorkQueue creano il proprio STA. I componenti che usano la funzione Long WorkQueue per le richiamate devono evitare la creazione di oggetti COM su questi thread e devono prestare attenzione a eseguire il marshalling dei proxy in STA secondo necessità.

## <a name="summary"></a>Riepilogo

Se interagiscono con Media Foundation da un thread MTA, le applicazioni avranno un tempo più semplice, ma è possibile usare Media Foundation da un thread STA. Media Foundation non gestisce i componenti STA e le applicazioni devono prestare attenzione a non passare oggetti STA alle API Media Foundation. Alcuni oggetti presentano requisiti aggiuntivi, in particolare gli oggetti che vengono eseguiti in una situazione tra processi. Seguendo queste linee guida è possibile evitare errori COM, deadlock e ritardi imprevisti nell'elaborazione dei supporti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[API della piattaforma Media Foundation](media-foundation-platform-apis.md)
</dt> <dt>

[Architettura di Media Foundation](media-foundation-architecture.md)
</dt> </dl>

 

 
