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
# <a name="media-foundation-and-com"></a><span data-ttu-id="439d5-103">Media Foundation e COM</span><span class="sxs-lookup"><span data-stu-id="439d5-103">Media Foundation and COM</span></span>

<span data-ttu-id="439d5-104">Microsoft Media Foundation usa una combinazione di costrutti COM, ma non è un'API completamente basata su COM.</span><span class="sxs-lookup"><span data-stu-id="439d5-104">Microsoft Media Foundation uses a mix of COM constructs, but is not a fully COM-based API.</span></span> <span data-ttu-id="439d5-105">In questo argomento viene descritta l'interazione tra COM e Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="439d5-105">This topic describes the interaction between COM and Media Foundation.</span></span> <span data-ttu-id="439d5-106">Vengono inoltre definite alcune procedure consigliate per lo sviluppo di Media Foundation componenti plug-in.</span><span class="sxs-lookup"><span data-stu-id="439d5-106">It also defines some best practices for developing Media Foundation plug-in components.</span></span> <span data-ttu-id="439d5-107">Seguendo queste procedure è possibile evitare alcuni errori di programmazione comuni ma minimi.</span><span class="sxs-lookup"><span data-stu-id="439d5-107">Following these practices can help you to avoid some common but subtle programming errors.</span></span>

-   [<span data-ttu-id="439d5-108">Procedure consigliate per le applicazioni</span><span class="sxs-lookup"><span data-stu-id="439d5-108">Best Practices for Applications</span></span>](#best-practices-for-applications)
-   [<span data-ttu-id="439d5-109">Procedure consigliate per i componenti di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="439d5-109">Best Practices for Media Foundation Components</span></span>](#best-practices-for-media-foundation-components)
-   [<span data-ttu-id="439d5-110">Summary</span><span class="sxs-lookup"><span data-stu-id="439d5-110">Summary</span></span>](#summary)
-   [<span data-ttu-id="439d5-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="439d5-111">Related topics</span></span>](#related-topics)

## <a name="best-practices-for-applications"></a><span data-ttu-id="439d5-112">Procedure consigliate per le applicazioni</span><span class="sxs-lookup"><span data-stu-id="439d5-112">Best Practices for Applications</span></span>

<span data-ttu-id="439d5-113">In Media Foundation, l'elaborazione asincrona e i callback vengono gestiti dalle [code di lavoro](work-queues.md).</span><span class="sxs-lookup"><span data-stu-id="439d5-113">In Media Foundation, asynchronous processing and callbacks are handled by [work queues](work-queues.md).</span></span> <span data-ttu-id="439d5-114">Le code di lavoro hanno sempre thread di Apartment a thread multipli (MTA), pertanto un'applicazione avrà un'implementazione più semplice se viene eseguita anche su un thread MTA.</span><span class="sxs-lookup"><span data-stu-id="439d5-114">Work queues always have multithreaded apartment (MTA) threads, so an application will have a simpler implementation if it runs on an MTA thread as well.</span></span> <span data-ttu-id="439d5-115">È quindi consigliabile chiamare [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) con il flag **COinit \_ multithreading** .</span><span class="sxs-lookup"><span data-stu-id="439d5-115">Therefore, it is recommended to call [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) with the **COINIT\_MULTITHREADED** flag.</span></span>

<span data-ttu-id="439d5-116">Media Foundation non esegue il marshalling di oggetti Apartment a thread singolo (STA) a thread della coda di lavoro.</span><span class="sxs-lookup"><span data-stu-id="439d5-116">Media Foundation does not marshal single-threaded apartment (STA) objects to work queue threads.</span></span> <span data-ttu-id="439d5-117">Né garantisce che vengano mantenute le invarianti.</span><span class="sxs-lookup"><span data-stu-id="439d5-117">Nor does it ensure that STA invariants are maintained.</span></span> <span data-ttu-id="439d5-118">Pertanto, un'applicazione STA deve prestare attenzione a non passare oggetti o proxy STA per Media Foundation API.</span><span class="sxs-lookup"><span data-stu-id="439d5-118">Therefore, an STA application must be careful to not pass STA objects or proxies to Media Foundation APIs.</span></span> <span data-ttu-id="439d5-119">Gli oggetti che sono solo sta non sono supportati in Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="439d5-119">Objects that are STA-only are not supported in Media Foundation.</span></span>

<span data-ttu-id="439d5-120">Se si dispone di un proxy STA per un MTA o di un oggetto a thread libero, è possibile effettuare il marshalling dell'oggetto in un proxy MTA usando un callback della coda di lavoro.</span><span class="sxs-lookup"><span data-stu-id="439d5-120">If you have an STA proxy to an MTA or free-threaded object, the object can be marshaled to an MTA proxy by using a work-queue callback.</span></span> <span data-ttu-id="439d5-121">La funzione [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) può restituire un puntatore non elaborato o un proxy sta, a seconda del modello a oggetti definito nel registro di sistema per il CLSID.</span><span class="sxs-lookup"><span data-stu-id="439d5-121">The [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function can return either a raw pointer or an STA proxy, depending on the object model defined in the registry for that CLSID.</span></span> <span data-ttu-id="439d5-122">Se viene restituito un proxy STA, non è necessario passare il puntatore a un'API Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="439d5-122">If an STA proxy is returned, you must not pass the pointer to a Media Foundation API.</span></span>

<span data-ttu-id="439d5-123">Si supponga, ad esempio, di voler passare un puntatore **IPropertyStore** al metodo [**IMFSourceResolver:: BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) .</span><span class="sxs-lookup"><span data-stu-id="439d5-123">For example, suppose that you want to pass an **IPropertyStore** pointer to the [**IMFSourceResolver::BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) method.</span></span> <span data-ttu-id="439d5-124">È possibile chiamare **PSCreateMemoryPropertyStore** per creare il puntatore **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="439d5-124">You might call **PSCreateMemoryPropertyStore** to create the **IPropertyStore** pointer.</span></span> <span data-ttu-id="439d5-125">Se si chiama da un STA, è necessario effettuare il marshalling del puntatore prima di passarlo a **BeginCreateObjectFromURL**.</span><span class="sxs-lookup"><span data-stu-id="439d5-125">If you are calling from an STA, you must marshal the pointer before passing it to **BeginCreateObjectFromURL**.</span></span>

<span data-ttu-id="439d5-126">Il codice seguente illustra come effettuare il marshalling di un proxy STA in un'API Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="439d5-126">The following code shows how to marshal an STA proxy to a Media Foundation API.</span></span>


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



<span data-ttu-id="439d5-127">Per ulteriori informazioni sulla tabella dell'interfaccia globale, vedere [**IGlobalInterfaceTable**](/windows/win32/api/objidl/nn-objidl-iglobalinterfacetable).</span><span class="sxs-lookup"><span data-stu-id="439d5-127">For more information about the global interface table, see [**IGlobalInterfaceTable**](/windows/win32/api/objidl/nn-objidl-iglobalinterfacetable).</span></span>

<span data-ttu-id="439d5-128">Se si usa Media Foundation in-process, gli oggetti restituiti da Media Foundation metodi e funzioni sono puntatori diretti all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="439d5-128">If you are using Media Foundation in-process, objects returned from Media Foundation methods and functions are direct pointers to the object.</span></span> <span data-ttu-id="439d5-129">Per Media Foundation tra processi, questi oggetti possono essere proxy MTA ed è necessario eseguirne il marshalling in un thread STA se necessario.</span><span class="sxs-lookup"><span data-stu-id="439d5-129">For cross-process Media Foundation, these objects may be MTA proxies, and should be marshaled into an STA thread if needed there.</span></span> <span data-ttu-id="439d5-130">Analogamente, gli oggetti ottenuti all'interno di un callback, ad esempio una topologia dall'evento [MESessionTopologyStatus](mesessiontopologystatus.md) , sono puntatori diretti quando Media Foundation viene usato in-process, ma sono proxy MTA quando Media Foundation viene usato tra processi.</span><span class="sxs-lookup"><span data-stu-id="439d5-130">Similarly, objects obtained inside a callback — for example, a topology from the [MESessionTopologyStatus](mesessiontopologystatus.md) event — are direct pointers when Media Foundation is used in-process, but are MTA proxies when Media Foundation is used cross-process.</span></span>

> [!Note]  
> <span data-ttu-id="439d5-131">Lo scenario più comune per l'uso di Media Foundation processo incrociato è con il [percorso multimediale protetto](protected-media-path.md) (PMP).</span><span class="sxs-lookup"><span data-stu-id="439d5-131">The most common scenario for using Media Foundation cross-process is with the [Protected Media Path](protected-media-path.md) (PMP).</span></span> <span data-ttu-id="439d5-132">Tuttavia, queste osservazioni si applicano a qualsiasi situazione in cui le API Media Foundation vengono usate tramite RPC.</span><span class="sxs-lookup"><span data-stu-id="439d5-132">However, these remarks apply to any situation when Media Foundation APIs are used through RPC.</span></span>

 

<span data-ttu-id="439d5-133">Tutte le implementazioni di [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) devono essere compatibili con MTA.</span><span class="sxs-lookup"><span data-stu-id="439d5-133">All implementations of [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) should be MTA-compatible.</span></span> <span data-ttu-id="439d5-134">Questi oggetti non devono necessariamente essere oggetti COM.</span><span class="sxs-lookup"><span data-stu-id="439d5-134">These objects do not need to be COM objects at all.</span></span> <span data-ttu-id="439d5-135">Tuttavia, in caso affermativo, non possono essere eseguiti nell'STA.</span><span class="sxs-lookup"><span data-stu-id="439d5-135">But if they are, they cannot run in the STA.</span></span> <span data-ttu-id="439d5-136">La funzione [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) verrà richiamata su un thread WorkQueue MTA e l'oggetto [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) fornito sarà un puntatore a oggetto diretto o un proxy MTA.</span><span class="sxs-lookup"><span data-stu-id="439d5-136">The [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) function will be invoked on an MTA workqueue thread, and the provided [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) object will be either a direct object pointer or an MTA proxy.</span></span>

## <a name="best-practices-for-media-foundation-components"></a><span data-ttu-id="439d5-137">Procedure consigliate per i componenti di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="439d5-137">Best Practices for Media Foundation Components</span></span>

<span data-ttu-id="439d5-138">Esistono due categorie di oggetti Media Foundation che devono essere interessati a COM.</span><span class="sxs-lookup"><span data-stu-id="439d5-138">There are two categories of Media Foundation objects that need to be concerned about COM.</span></span> <span data-ttu-id="439d5-139">Alcuni componenti, ad esempio le trasformazioni o i gestori del flusso di byte, sono oggetti COM completi creati da CLSID.</span><span class="sxs-lookup"><span data-stu-id="439d5-139">Some components, such as transforms or byte stream handlers, are full COM objects created by CLSID.</span></span> <span data-ttu-id="439d5-140">Questi oggetti devono rispettare le regole per gli apartment COM, sia per Media Foundation in-process che tra processi.</span><span class="sxs-lookup"><span data-stu-id="439d5-140">These objects must follow the rules for COM apartments, for both in-process and cross-process Media Foundation.</span></span> <span data-ttu-id="439d5-141">Altri componenti Media Foundation non sono oggetti COM completi, ma sono necessari proxy COM per la riproduzione tra processi.</span><span class="sxs-lookup"><span data-stu-id="439d5-141">Other Media Foundation components are not full COM objects, but do need COM proxies for cross-process playback.</span></span> <span data-ttu-id="439d5-142">Gli oggetti di questa categoria includono origini multimediali e oggetto attivazione.</span><span class="sxs-lookup"><span data-stu-id="439d5-142">Objects in this category include media sources and activation object.</span></span> <span data-ttu-id="439d5-143">Questi oggetti possono ignorare i problemi di Apartment se verranno utilizzati solo per Media Foundation in-process.</span><span class="sxs-lookup"><span data-stu-id="439d5-143">These objects can ignore apartment issues if they will be used only for in-process Media Foundation.</span></span>

<span data-ttu-id="439d5-144">Sebbene non tutti gli oggetti Media Foundation siano oggetti COM, tutte le interfacce Media Foundation derivano da [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span><span class="sxs-lookup"><span data-stu-id="439d5-144">Although not all Media Foundation objects are COM objects, all Media Foundation interfaces derive from [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span></span> <span data-ttu-id="439d5-145">Pertanto, tutti gli oggetti Media Foundation devono implementare **IUnknown** secondo le specifiche com, incluse le regole per il conteggio dei riferimenti e [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span><span class="sxs-lookup"><span data-stu-id="439d5-145">Therefore, all Media Foundation objects must implement **IUnknown** according to COM specifications, including the rules for reference counting and [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span></span> <span data-ttu-id="439d5-146">Tutti gli oggetti conteggiati a cui si fa riferimento devono inoltre garantire che [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow) non consenta lo scaricamento del modulo mentre gli oggetti rimangono persistenti.</span><span class="sxs-lookup"><span data-stu-id="439d5-146">All reference counted objects should also ensure that [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow) will not allow the module to be unloaded while the objects still persist.</span></span>

<span data-ttu-id="439d5-147">Media Foundation componenti non possono essere oggetti STA.</span><span class="sxs-lookup"><span data-stu-id="439d5-147">Media Foundation components cannot be STA objects.</span></span> <span data-ttu-id="439d5-148">Molti oggetti Media Foundation non devono necessariamente essere oggetti COM.</span><span class="sxs-lookup"><span data-stu-id="439d5-148">Many Media Foundation objects do not need to be COM objects at all.</span></span> <span data-ttu-id="439d5-149">Tuttavia, in caso affermativo, non possono essere eseguiti nell'STA.</span><span class="sxs-lookup"><span data-stu-id="439d5-149">But if they are, they cannot run in the STA.</span></span> <span data-ttu-id="439d5-150">Tutti i componenti Media Foundation devono essere thread-safe.</span><span class="sxs-lookup"><span data-stu-id="439d5-150">All Media Foundation components must be thread-safe.</span></span> <span data-ttu-id="439d5-151">Alcuni oggetti Media Foundation devono essere anche a thread libero o indipendente dall'Apartment.</span><span class="sxs-lookup"><span data-stu-id="439d5-151">Some Media Foundation objects must be free-threaded or apartment-neutral as well.</span></span> <span data-ttu-id="439d5-152">La tabella seguente specifica i requisiti per le implementazioni dell'interfaccia personalizzate:</span><span class="sxs-lookup"><span data-stu-id="439d5-152">The following table specifies the requirements for custom interface implementations:</span></span>



| <span data-ttu-id="439d5-153">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="439d5-153">Interface</span></span>                                                          | <span data-ttu-id="439d5-154">Category</span><span class="sxs-lookup"><span data-stu-id="439d5-154">Category</span></span>            | <span data-ttu-id="439d5-155">Apartment obbligatorio</span><span class="sxs-lookup"><span data-stu-id="439d5-155">Required apartment</span></span>       |
|--------------------------------------------------------------------|---------------------|--------------------------|
| [<span data-ttu-id="439d5-156">**IMFActivate**</span><span class="sxs-lookup"><span data-stu-id="439d5-156">**IMFActivate**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)                                 | <span data-ttu-id="439d5-157">Proxy tra processi</span><span class="sxs-lookup"><span data-stu-id="439d5-157">Cross-process proxy</span></span> | <span data-ttu-id="439d5-158">A thread libero o neutro</span><span class="sxs-lookup"><span data-stu-id="439d5-158">Free-threaded or neutral</span></span> |
| [<span data-ttu-id="439d5-159">**IMFByteStreamHandler**</span><span class="sxs-lookup"><span data-stu-id="439d5-159">**IMFByteStreamHandler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)               | <span data-ttu-id="439d5-160">Oggetto COM</span><span class="sxs-lookup"><span data-stu-id="439d5-160">COM object</span></span>          | <span data-ttu-id="439d5-161">MTA</span><span class="sxs-lookup"><span data-stu-id="439d5-161">MTA</span></span>                      |
| [<span data-ttu-id="439d5-162">**IMFContentProtectionManager**</span><span class="sxs-lookup"><span data-stu-id="439d5-162">**IMFContentProtectionManager**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) | <span data-ttu-id="439d5-163">Proxy tra processi</span><span class="sxs-lookup"><span data-stu-id="439d5-163">Cross-process proxy</span></span> | <span data-ttu-id="439d5-164">A thread libero o neutro</span><span class="sxs-lookup"><span data-stu-id="439d5-164">Free-threaded or neutral</span></span> |
| [<span data-ttu-id="439d5-165">**IMFQualityManager**</span><span class="sxs-lookup"><span data-stu-id="439d5-165">**IMFQualityManager**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager)                     | <span data-ttu-id="439d5-166">Oggetto COM</span><span class="sxs-lookup"><span data-stu-id="439d5-166">COM object</span></span>          | <span data-ttu-id="439d5-167">A thread libero o neutro</span><span class="sxs-lookup"><span data-stu-id="439d5-167">Free-threaded or neutral</span></span> |
| [<span data-ttu-id="439d5-168">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="439d5-168">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                           | <span data-ttu-id="439d5-169">Proxy tra processi</span><span class="sxs-lookup"><span data-stu-id="439d5-169">Cross-process proxy</span></span> | <span data-ttu-id="439d5-170">A thread libero o neutro</span><span class="sxs-lookup"><span data-stu-id="439d5-170">Free-threaded or neutral</span></span> |
| [<span data-ttu-id="439d5-171">**IMFSchemeHandler**</span><span class="sxs-lookup"><span data-stu-id="439d5-171">**IMFSchemeHandler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler)                       | <span data-ttu-id="439d5-172">Oggetto COM</span><span class="sxs-lookup"><span data-stu-id="439d5-172">COM object</span></span>          | <span data-ttu-id="439d5-173">MTA</span><span class="sxs-lookup"><span data-stu-id="439d5-173">MTA</span></span>                      |
| [<span data-ttu-id="439d5-174">**IMFTopoLoader**</span><span class="sxs-lookup"><span data-stu-id="439d5-174">**IMFTopoLoader**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)                             | <span data-ttu-id="439d5-175">Oggetto COM</span><span class="sxs-lookup"><span data-stu-id="439d5-175">COM object</span></span>          | <span data-ttu-id="439d5-176">A thread libero o neutro</span><span class="sxs-lookup"><span data-stu-id="439d5-176">Free-threaded or neutral</span></span> |
| [<span data-ttu-id="439d5-177">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="439d5-177">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)                               | <span data-ttu-id="439d5-178">Oggetto COM</span><span class="sxs-lookup"><span data-stu-id="439d5-178">COM object</span></span>          | <span data-ttu-id="439d5-179">MTA</span><span class="sxs-lookup"><span data-stu-id="439d5-179">MTA</span></span>                      |



 

<span data-ttu-id="439d5-180">Potrebbero essere necessari requisiti aggiuntivi a seconda dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="439d5-180">There may be additional requirements depending upon the implementation.</span></span> <span data-ttu-id="439d5-181">Se, ad esempio, un sink multimediale implementa un'altra interfaccia che consente all'applicazione di effettuare chiamate di funzione dirette al sink, il sink dovrà essere a thread libero o neutro, in modo da poter gestire le chiamate dirette tra processi.</span><span class="sxs-lookup"><span data-stu-id="439d5-181">For example, if a media sink implements another interface that enables the application to make direct function calls to the sink, the sink would need to be free-threaded or neutral, so that it could handle direct cross-process calls.</span></span> <span data-ttu-id="439d5-182">Qualsiasi oggetto può essere a thread libero. Questa tabella specifica i requisiti minimi.</span><span class="sxs-lookup"><span data-stu-id="439d5-182">Any object may be free-threaded; this table specifies the minimum requirements.</span></span>

<span data-ttu-id="439d5-183">Il metodo consigliato per implementare oggetti a thread libero o neutri consiste nell'aggregazione del gestore di marshalling a thread libero.</span><span class="sxs-lookup"><span data-stu-id="439d5-183">The recommended way to implement free-threaded or neutral objects is by aggregating the free-threaded marshaler.</span></span> <span data-ttu-id="439d5-184">Per ulteriori informazioni, vedere la documentazione MSDN su [**CoCreateFreeThreadedMarshaler**](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler).</span><span class="sxs-lookup"><span data-stu-id="439d5-184">For more details, see the MSDN documentation on [**CoCreateFreeThreadedMarshaler**](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler).</span></span> <span data-ttu-id="439d5-185">In conformità con la necessità di non passare gli oggetti o i proxy di STA a Media Foundation API, gli oggetti a thread libero non devono preoccuparsi di effettuare il marshalling dei puntatori di input STA nei componenti a thread libero.</span><span class="sxs-lookup"><span data-stu-id="439d5-185">In accordance with the requirement not to pass STA objects or proxies to Media Foundation APIs, free-threaded objects do not need to worry about marshaling STA input pointers in free-threaded components.</span></span>

<span data-ttu-id="439d5-186">I componenti che usano la coda di lavoro di funzione lunga (**\_ \_ \_ \_ funzione Long della coda di callback MFASYNC**) devono prestare maggiore attenzione.</span><span class="sxs-lookup"><span data-stu-id="439d5-186">Components that use the long-function work queue (**MFASYNC\_CALLBACK\_QUEUE\_LONG\_FUNCTION**) must exercise more care.</span></span> <span data-ttu-id="439d5-187">I thread nella funzione Long WorkQueue creano il proprio STA.</span><span class="sxs-lookup"><span data-stu-id="439d5-187">Threads in the long function workqueue create their own STA.</span></span> <span data-ttu-id="439d5-188">I componenti che usano la funzione Long WorkQueue per le richiamate devono evitare la creazione di oggetti COM su questi thread e devono prestare attenzione a eseguire il marshalling dei proxy in STA secondo necessità.</span><span class="sxs-lookup"><span data-stu-id="439d5-188">Components that use the long function workqueue for callbacks should avoid creating COM objects on these threads, and need to be careful to marshal proxies to the STA as necessary.</span></span>

## <a name="summary"></a><span data-ttu-id="439d5-189">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="439d5-189">Summary</span></span>

<span data-ttu-id="439d5-190">Se interagiscono con Media Foundation da un thread MTA, le applicazioni avranno un tempo più semplice, ma è possibile usare Media Foundation da un thread STA.</span><span class="sxs-lookup"><span data-stu-id="439d5-190">Applications will have an easier time if they interact with Media Foundation from an MTA thread, but it is possible with some care to use Media Foundation from an STA thread.</span></span> <span data-ttu-id="439d5-191">Media Foundation non gestisce i componenti STA e le applicazioni devono prestare attenzione a non passare oggetti STA alle API Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="439d5-191">Media Foundation does not handle STA components, and applications should be careful not to pass STA objects to Media Foundation APIs.</span></span> <span data-ttu-id="439d5-192">Alcuni oggetti presentano requisiti aggiuntivi, in particolare gli oggetti che vengono eseguiti in una situazione tra processi.</span><span class="sxs-lookup"><span data-stu-id="439d5-192">Some objects have additional requirements, especially objects that run in a cross-process situation.</span></span> <span data-ttu-id="439d5-193">Seguendo queste linee guida è possibile evitare errori COM, deadlock e ritardi imprevisti nell'elaborazione dei supporti.</span><span class="sxs-lookup"><span data-stu-id="439d5-193">Following these guidelines will help avoid COM errors, deadlocks, and unexpected delays in media processing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="439d5-194">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="439d5-194">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="439d5-195">API della piattaforma Media Foundation</span><span class="sxs-lookup"><span data-stu-id="439d5-195">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> <dt>

[<span data-ttu-id="439d5-196">Architettura di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="439d5-196">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> </dl>

 

 
