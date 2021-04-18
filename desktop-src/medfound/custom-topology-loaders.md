---
description: Caricatori topologia personalizzati
ms.assetid: 3982b07e-3179-45c1-9f17-f2114363f53d
title: Caricatori topologia personalizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34a8f9e24b207d43620e7b2d09080d244b0a9e72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305459"
---
# <a name="custom-topology-loaders"></a><span data-ttu-id="9b284-103">Caricatori topologia personalizzati</span><span class="sxs-lookup"><span data-stu-id="9b284-103">Custom Topology Loaders</span></span>

<span data-ttu-id="9b284-104">Quando un'applicazione Accoda una topologia parziale nella sessione multimediale, la sessione multimediale usa un caricatore della topologia per risolvere la topologia.</span><span class="sxs-lookup"><span data-stu-id="9b284-104">When an application queues a partial topology on the Media Session, the Media Session uses a topology loader to resolve the topology.</span></span> <span data-ttu-id="9b284-105">Per impostazione predefinita, la sessione multimediale usa l'implementazione Media Foundation standard del caricatore della topologia, ma è anche possibile fornire un'implementazione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="9b284-105">By default, the Media Session uses the standard Media Foundation implementation of the topology loader, but you can also provide a custom implementation.</span></span> <span data-ttu-id="9b284-106">In questo modo si ottiene un maggiore controllo sulla topologia finale.</span><span class="sxs-lookup"><span data-stu-id="9b284-106">This gives you more control over the final topology.</span></span> <span data-ttu-id="9b284-107">Un caricatore di topologia personalizzato deve implementare l'interfaccia [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) .</span><span class="sxs-lookup"><span data-stu-id="9b284-107">A custom topology loader must implement the [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) interface.</span></span>

<span data-ttu-id="9b284-108">Per impostare un caricatore di topologia personalizzato nella sessione multimediale, eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="9b284-108">To set a custom topology loader on the Media Session, do the following:</span></span>

1.  <span data-ttu-id="9b284-109">Creare un archivio di attributi vuoto chiamando [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).</span><span class="sxs-lookup"><span data-stu-id="9b284-109">Create an empty attribute store by calling [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).</span></span>
2.  <span data-ttu-id="9b284-110">Impostare l' [**attributo \_ \_ TOPOLOADER della sessione MF**](mf-session-topoloader-attribute.md) nell'archivio di attributi.</span><span class="sxs-lookup"><span data-stu-id="9b284-110">Set the [**MF\_SESSION\_TOPOLOADER**](mf-session-topoloader-attribute.md) attribute on the attribute store.</span></span> <span data-ttu-id="9b284-111">Il valore dell'attributo è il CLSID del caricatore personalizzato.</span><span class="sxs-lookup"><span data-stu-id="9b284-111">The value of the attribute is the CLSID of your custom loader.</span></span>
3.  <span data-ttu-id="9b284-112">Chiamare [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) per creare la sessione multimediale per il contenuto non protetto oppure [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) per creare la sessione multimediale all'interno del percorso multimediale protetto (PMP).</span><span class="sxs-lookup"><span data-stu-id="9b284-112">Call [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) to create the Media Session for unprotected content, or [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) to create the Media Session inside the protected media path (PMP).</span></span>

> [!Note]  
> <span data-ttu-id="9b284-113">Per usare un caricatore di topologia personalizzato all'interno di PMP, il caricatore della topologia deve essere un componente attendibile.</span><span class="sxs-lookup"><span data-stu-id="9b284-113">To use a custom topology loader inside the PMP, the topology loader must be a trusted component.</span></span> <span data-ttu-id="9b284-114">Per altre informazioni, vedere [percorso multimediale protetto](protected-media-path.md).</span><span class="sxs-lookup"><span data-stu-id="9b284-114">For more information, see [Protected Media Path](protected-media-path.md).</span></span>

 

<span data-ttu-id="9b284-115">Il codice seguente illustra come impostare un caricatore di topologia personalizzato nella sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="9b284-115">The following code shows how to set a custom topology loader on the Media Session.</span></span>


```C++
HRESULT CreateSession_CustomTopoLoader(REFCLSID clsid, IMFMediaSession **ppSession)
{
    *ppSession = NULL;

    IMFMediaSession *pSession = NULL;
    IMFAttributes *pConfig = NULL;

    // Create an attribute store to configure the media session.
    HRESULT hr = MFCreateAttributes(&pConfig, 1);

    // Set the CLSID of the custom topology loader.
    if (SUCCEEDED(hr))
    {
        hr = pConfig->SetGUID(MF_SESSION_TOPOLOADER, clsid);
    }

    // Create the media session.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMediaSession(pConfig, &pSession);
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppSession = pSession;
        (*ppSession)->AddRef();
    }

    SafeRelease(&pSession);
    SafeRelease(&pConfig);

    return hr;
}
```



<span data-ttu-id="9b284-116">Non è necessario implementare l'intero algoritmo di caricamento della topologia nel caricatore della topologia.</span><span class="sxs-lookup"><span data-stu-id="9b284-116">It is not necessary to implement the entire topology-loading algorithm in your topology loader.</span></span> <span data-ttu-id="9b284-117">In alternativa, è possibile eseguire il wrapping del caricatore della topologia Media Foundation standard.</span><span class="sxs-lookup"><span data-stu-id="9b284-117">As an alternative, you can wrap the standard Media Foundation topology loader.</span></span> <span data-ttu-id="9b284-118">Nell'implementazione del metodo [**IMFTopoLoader:: Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) , modificare la topologia in base alle esigenze e passare la topologia modificata al caricatore della topologia standard.</span><span class="sxs-lookup"><span data-stu-id="9b284-118">In your implementation of the [**IMFTopoLoader::Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) method, modify the topology as needed and pass the modified topology to the standard topology loader.</span></span> <span data-ttu-id="9b284-119">Il caricatore della topologia standard completa quindi la topologia.</span><span class="sxs-lookup"><span data-stu-id="9b284-119">Then the standard topology loader completes the topology.</span></span> <span data-ttu-id="9b284-120">È anche possibile modificare la topologia completata prima di passarla di nuovo alla sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="9b284-120">You can also modify the completed topology before passing it back to the Media Session.</span></span>

<span data-ttu-id="9b284-121">Il codice seguente illustra la struttura generale di questo approccio.</span><span class="sxs-lookup"><span data-stu-id="9b284-121">The following code shows the general outline of this approach.</span></span> <span data-ttu-id="9b284-122">Non vengono visualizzati i dettagli del metodo [**Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) , perché questi dipendono dai requisiti specifici dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9b284-122">It does not show any details of the [**Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) method, because these will depend on the particular requirements of your application.</span></span>


```C++
class CTopoLoader : public IMFTopoLoader
{
public:

    static HRESULT CreateInstance(REFIID iid, void **ppv)
    {
        HRESULT hr = S_OK;

        CTopoLoader *pTopoLoader = new (std::nothrow) CTopoLoader(&hr);
        
        if (pTopoLoader == NULL)
        {
            return E_OUTOFMEMORY;
        }

        if (SUCCEEDED(hr))
        {
            hr = pTopoLoader->QueryInterface(iid, ppv);
        }

        SafeRelease(&pTopoLoader);
        return hr;
    }

    // IUnknown methods.
    STDMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CTopoLoader, IMFTopoLoader),
            { 0 },
        };
        return QISearch(this, qit, riid, ppv);
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        long cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        return cRef;
    }

    // IMTopoLoader methods.
    STDMETHODIMP Load(
        IMFTopology *pInput, 
        IMFTopology **ppOutput, 
        IMFTopology *pCurrent
        )
    {
        HRESULT hr = S_OK;

        // TODO: Add custom topology-building code here.
        //       Modify pInput as needed.

        if (SUCCEEDED(hr))
        {
            hr = m_pTopoLoader->Load(pInput, ppOutput, pCurrent);
        }

        // TODO: Add custom topology-building code here.
        //       Modify ppOutput as needed.

        return hr;
    }

private:
    CTopoLoader(HRESULT *phr) : m_cRef(1), m_pTopoLoader(NULL)
    {
        *phr = MFCreateTopoLoader(&m_pTopoLoader);
    }

    virtual ~CTopoLoader()
    {
        SafeRelease(&m_pTopoLoader);
    }

private:
    long            m_cRef;          // Reference count.
    IMFTopoLoader   *m_pTopoLoader;  // Standard topoloader.
};
```



## <a name="related-topics"></a><span data-ttu-id="9b284-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9b284-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b284-124">**MFCreateTopoLoader**</span><span class="sxs-lookup"><span data-stu-id="9b284-124">**MFCreateTopoLoader**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopoloader)
</dt> <dt>

[<span data-ttu-id="9b284-125">Compilazione avanzata della topologia</span><span class="sxs-lookup"><span data-stu-id="9b284-125">Advanced Topology Building</span></span>](advanced-topology-building.md)
</dt> </dl>

 

 



