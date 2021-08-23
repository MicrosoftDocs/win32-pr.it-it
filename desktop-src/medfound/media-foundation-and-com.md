---
description: Microsoft Media Foundation usa una combinazione di costrutti COM, ma non è un'API completamente basata su COM.
ms.assetid: d58ca46f-8f3a-4a12-b948-1ea7ab568788
title: Media Foundation e COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb43fa29063da453a17275fca0b5c441e89f75aab8016a1abcf1702f5433fd71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974214"
---
# <a name="media-foundation-and-com"></a>Media Foundation e COM

Microsoft Media Foundation usa una combinazione di costrutti COM, ma non è un'API completamente basata su COM. Questo argomento descrive l'interazione tra COM e Media Foundation. Definisce anche alcune procedure consigliate per lo sviluppo di Media Foundation componenti plug-in. Seguendo queste procedure è possibile evitare alcuni errori di programmazione comuni ma sottili.

-   [Procedure consigliate per le applicazioni](#best-practices-for-applications)
-   [Procedure consigliate per Media Foundation componenti](#best-practices-for-media-foundation-components)
-   [Summary](#summary)
-   [Argomenti correlati](#related-topics)

## <a name="best-practices-for-applications"></a>Procedure consigliate per le applicazioni

In Media Foundation, l'elaborazione asincrona e i callback vengono gestiti dalle [code di lavoro](work-queues.md). Le code di lavoro hanno sempre thread apartment multithreading (MTA), quindi un'applicazione avrà un'implementazione più semplice se viene eseguita anche in un thread MTA. È pertanto consigliabile chiamare [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) con il flag **COINIT \_ MULTITHREADED.**

Media Foundation esegue il marshalling di oggetti apartment a thread singolo (STA) ai thread della coda di lavoro. Né garantisce che le invarianti STA siano mantenute. Pertanto, un'applicazione STA deve prestare attenzione a non passare oggetti o proxy STA Media Foundation API. Gli oggetti che sono solo STA non sono supportati in Media Foundation.

Se si dispone di un proxy STA per un MTA o un oggetto a thread libero, è possibile effettuare il marshalling dell'oggetto a un proxy MTA usando un callback della coda di lavoro. La [**funzione CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) può restituire un puntatore non elaborato o un proxy STA, a seconda del modello a oggetti definito nel Registro di sistema per tale CLSID. Se viene restituito un proxy STA, non è necessario passare il puntatore a un Media Foundation API.

Si supponga, ad esempio, di voler passare un **puntatore IPropertyStore** al [**metodo IMFSourceResolver::BeginCreateObjectFromURL.**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) È possibile chiamare **PSCreateMemoryPropertyStore per** creare il **puntatore IPropertyStore.** Se si chiama da sta, è necessario effettuare il marshalling del puntatore prima di passarlo a **BeginCreateObjectFromURL.**

Il codice seguente illustra come effettuare il marshalling di un proxy STA a un'API Media Foundation.


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



Per altre informazioni sulla tabella dell'interfaccia globale, vedere [**IGlobalInterfaceTable**](/windows/win32/api/objidl/nn-objidl-iglobalinterfacetable).

Se si usa Media Foundation in-process, gli oggetti restituiti da Media Foundation metodi e funzioni sono puntatori diretti all'oggetto. Per i processi Media Foundation, questi oggetti possono essere proxy MTA e devono essere sottoposti a marshalling in un thread STA, se necessario. Analogamente, gli oggetti ottenuti all'interno di un callback, ad esempio una topologia dall'evento [MESessionTopologyStatus,](mesessiontopologystatus.md) sono puntatori diretti quando Media Foundation viene usato in-process, ma sono proxy MTA quando Media Foundation viene usato tra processi.

> [!Note]  
> Lo scenario più comune per l'Media Foundation cross-process è con [il percorso](protected-media-path.md) del supporto protetto (PMP). Tuttavia, queste osservazioni si applicano a qualsiasi situazione in cui Media Foundation API vengono usate tramite RPC.

 

Tutte le implementazioni [**di IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) devono essere compatibili con MTA. Questi oggetti non devono essere affatto oggetti COM. In caso contrario, non possono essere eseguiti in STA. La [**funzione IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) verrà richiamata in un thread della coda di lavoro MTA e l'oggetto [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) fornito sarà un puntatore a oggetto diretto o un proxy MTA.

## <a name="best-practices-for-media-foundation-components"></a>Procedure consigliate per Media Foundation componenti

Esistono due categorie di Media Foundation che devono preoccuparsi di COM. Alcuni componenti, ad esempio trasformazioni o gestori di flussi di byte, sono oggetti COM completi creati da CLSID. Questi oggetti devono seguire le regole per gli apartment COM, sia in-process che cross-process Media Foundation. Altri Media Foundation non sono oggetti COM completi, ma sono necessari proxy COM per la riproduzione cross-process. Gli oggetti in questa categoria includono origini multimediali e oggetti di attivazione. Questi oggetti possono ignorare i problemi relativi all'apartment se verranno usati solo per i processi Media Foundation.

Anche se non tutti Media Foundation sono oggetti COM, tutte Media Foundation interfacce derivano da [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown). Pertanto, tutti Media Foundation devono implementare **IUnknown** in base alle specifiche COM, incluse le regole per il conteggio dei riferimenti [**e QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)). Tutti gli oggetti con conteggio dei riferimenti devono inoltre garantire che [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow) non consenta lo scaricamento del modulo mentre gli oggetti sono ancora persistenti.

Media Foundation componenti non possono essere oggetti STA. Molti Media Foundation non devono essere affatto oggetti COM. In caso contrario, non possono essere eseguiti in STA. Tutti Media Foundation componenti devono essere thread-safe. Alcuni Media Foundation devono essere a thread libero o indipendenti dall'apartment. La tabella seguente specifica i requisiti per le implementazioni di interfacce personalizzate:



| Interfaccia                                                          | Category            | Apartment obbligatorio       |
|--------------------------------------------------------------------|---------------------|--------------------------|
| [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)                                 | Proxy tra processi | Thread libero o neutro |
| [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)               | Oggetto COM          | MTA                      |
| [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) | Proxy tra processi | Thread libero o neutro |
| [**IMFQualityManager**](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager)                     | Oggetto COM          | Thread libero o neutro |
| [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                           | Proxy tra processi | Thread libero o neutro |
| [**IMFSchemeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler)                       | Oggetto COM          | MTA                      |
| [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)                             | Oggetto COM          | Thread libero o neutro |
| [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)                               | Oggetto COM          | MTA                      |



 

Potrebbero esserci requisiti aggiuntivi a seconda dell'implementazione. Ad esempio, se un sink multimediale implementa un'altra interfaccia che consente all'applicazione di effettuare chiamate di funzione dirette al sink, il sink deve essere a thread libero o neutro, in modo che possa gestire chiamate cross-process dirette. Qualsiasi oggetto può essere a thread libero. questa tabella specifica i requisiti minimi.

Il modo consigliato per implementare oggetti a thread libero o neutro è aggregando il gestore di marshalling a thread libero. Per altre informazioni, vedere la documentazione MSDN in [**CoCreateFreeThreadedMarshaler**](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler). In conformità al requisito di non passare oggetti o proxy STA alle API Media Foundation, gli oggetti a thread libero non devono preoccuparsi del marshalling dei puntatori di input STA nei componenti a thread libero.

I componenti che usano la coda di lavoro a funzione lunga (**MFASYNC \_ CALLBACK QUEUE LONG \_ \_ \_ FUNCTION**) devono prestare maggiore attenzione. I thread nella coda di lavoro delle funzioni lunghe creano il proprio STA. I componenti che usano la coda di lavoro delle funzioni lunghe per i callback devono evitare la creazione di oggetti COM in questi thread e devono prestare attenzione a effettuare il marshalling dei proxy a STA in base alle esigenze.

## <a name="summary"></a>Riepilogo

Le applicazioni avranno un tempo più semplice se interagiscono con Media Foundation da un thread MTA, ma è possibile usare Media Foundation da un thread STA. Media Foundation non gestisce i componenti STA e le applicazioni devono prestare attenzione a non passare oggetti STA Media Foundation API. Alcuni oggetti hanno requisiti aggiuntivi, in particolare gli oggetti eseguiti in una situazione multi-processo. Seguendo queste linee guida è possibile evitare errori COM, deadlock e ritardi imprevisti nell'elaborazione dei supporti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Media Foundation API della piattaforma](media-foundation-platform-apis.md)
</dt> <dt>

[Architettura di Media Foundation](media-foundation-architecture.md)
</dt> </dl>

 

 
