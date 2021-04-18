---
description: Come configurare il localizzatore proxy
ms.assetid: ddc28add-ebf5-4a68-bdf4-dc5f33ab74da
title: Come configurare il localizzatore proxy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a6b383dda9ac78b2c62aa8481a09cc5c0d7b3ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308766"
---
# <a name="how-to-configure-the-proxy-locator"></a><span data-ttu-id="7e58d-103">Come configurare il localizzatore proxy</span><span class="sxs-lookup"><span data-stu-id="7e58d-103">How to Configure the Proxy Locator</span></span>

<span data-ttu-id="7e58d-104">L'applicazione può modificare la configurazione predefinita del localizzatore proxy impostando la proprietà [MFNETSOURCE \_ PROXYLOCATORFACTORY](mfnetsource-proxylocatorfactory-property.md) sull'oggetto factory del localizzatore proxy implementato dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7e58d-104">The application can change the default configuration of the proxy locator by setting the [MFNETSOURCE\_PROXYLOCATORFACTORY](mfnetsource-proxylocatorfactory-property.md) property to the proxy locator factory object that is implemented by the application.</span></span> <span data-ttu-id="7e58d-105">Quando l'applicazione chiama i metodi del resolver di origine per creare l'origine di rete, Media Foundation chiama la factory del localizzatore proxy.</span><span class="sxs-lookup"><span data-stu-id="7e58d-105">When the application calls source resolver methods to create the network source, Media Foundation calls the proxy locator factory.</span></span> <span data-ttu-id="7e58d-106">Questo oggetto crea il localizzatore proxy con la configurazione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="7e58d-106">This object creates the proxy locator with custom configuration.</span></span>

## <a name="to-change-the-default-configuration-setting-of-the-proxy-locator"></a><span data-ttu-id="7e58d-107">Per modificare l'impostazione di configurazione predefinita del localizzatore proxy</span><span class="sxs-lookup"><span data-stu-id="7e58d-107">To change the default configuration setting of the proxy locator</span></span>

1.  <span data-ttu-id="7e58d-108">Implementare l'interfaccia [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) .</span><span class="sxs-lookup"><span data-stu-id="7e58d-108">Implement the [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) interface.</span></span>
2.  <span data-ttu-id="7e58d-109">Nel metodo [**IMFNetProxyLocatorFactory:: CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="7e58d-109">In the [**IMFNetProxyLocatorFactory::CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) method, do the following:</span></span>
    1.  <span data-ttu-id="7e58d-110">Creare un archivio delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="7e58d-110">Create a property store.</span></span>
    2.  <span data-ttu-id="7e58d-111">Impostare le impostazioni di configurazione per il localizzatore proxy.</span><span class="sxs-lookup"><span data-stu-id="7e58d-111">Set the configuration settings for the proxy locator.</span></span> <span data-ttu-id="7e58d-112">Per informazioni su queste impostazioni, vedere [impostazioni di configurazione del localizzatore proxy](proxy-locator-configuration-settings.md).</span><span class="sxs-lookup"><span data-stu-id="7e58d-112">For information about these settings, see [Proxy Locator Configuration Settings](proxy-locator-configuration-settings.md).</span></span>
    3.  <span data-ttu-id="7e58d-113">Chiamare la funzione [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) .</span><span class="sxs-lookup"><span data-stu-id="7e58d-113">Call the [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) function.</span></span> <span data-ttu-id="7e58d-114">Passare l'archivio delle proprietà e il protocollo.</span><span class="sxs-lookup"><span data-stu-id="7e58d-114">Pass in the property store and the protocol.</span></span> <span data-ttu-id="7e58d-115">Il protocollo viene specificato nel parametro *pszProtocol* di [**CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator).</span><span class="sxs-lookup"><span data-stu-id="7e58d-115">The protocol is specified in the *pszProtocol* parameter of [**CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator).</span></span>
3.  <span data-ttu-id="7e58d-116">Creare un'istanza della classe factory del localizzatore proxy e ottenere un puntatore alla relativa interfaccia [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) .</span><span class="sxs-lookup"><span data-stu-id="7e58d-116">Create an instance of your proxy locator factory class and get a pointer to its [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) interface.</span></span>
4.  <span data-ttu-id="7e58d-117">Creare un altro archivio di proprietà e impostare il valore della proprietà [**MFNETSOURCE \_ PROXYLOCATORFACTORY**](mfnetsource-proxylocatorfactory-property.md) uguale al puntatore [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) del passaggio 3.</span><span class="sxs-lookup"><span data-stu-id="7e58d-117">Create another property store and set the value of the [**MFNETSOURCE\_PROXYLOCATORFACTORY**](mfnetsource-proxylocatorfactory-property.md) property equal to the [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) pointer from step 3.</span></span>
5.  <span data-ttu-id="7e58d-118">Quando si crea l'origine di rete, passare l'archivio delle proprietà nel parametro *pProps* dei metodi del resolver di origine, ad esempio [**IMFSourceResolver:: BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl).</span><span class="sxs-lookup"><span data-stu-id="7e58d-118">When you create the network source, pass the property store in the *pProps* parameter of the source resolver methods such as [**IMFSourceResolver::BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl).</span></span>

## <a name="example"></a><span data-ttu-id="7e58d-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="7e58d-119">Example</span></span>

<span data-ttu-id="7e58d-120">Nell'esempio di codice seguente viene implementata l'interfaccia [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) .</span><span class="sxs-lookup"><span data-stu-id="7e58d-120">The following code example implements the [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) interface.</span></span> <span data-ttu-id="7e58d-121">Il metodo [**IMFNetProxyLocatorFactory:: CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) crea un'istanza del localizzatore proxy predefinito e la configura per operare in modalità di rilevamento automatico.</span><span class="sxs-lookup"><span data-stu-id="7e58d-121">The [**IMFNetProxyLocatorFactory::CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) method creates an instance of the default proxy locator, and configures it to operate in auto-detect mode.</span></span>


```C++
class CProxyLocatorFactory : public IMFNetProxyLocatorFactory 
{
    LONG m_cRef;

public:

    CProxyLocatorFactory() : m_cRef(1)
    {
    }

    STDMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CProxyLocatorFactory, IMFNetProxyLocatorFactory),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        return cRef;
    }

    STDMETHODIMP CreateProxyLocator(
        LPCWSTR pszProtocol, 
        IMFNetProxyLocator **ppProxyLocator
        )
    {
        *ppProxyLocator = NULL;

        //Create the property store object
        IPropertyStore *pProp = NULL;

        HRESULT hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pProp));

        if(SUCCEEDED(hr))
        {
            // Property key for proxy settings.
            PROPERTYKEY key;
            key.fmtid = MFNETSOURCE_PROXYSETTINGS;        
            key.pid = 0;

            // Proxy settings
            PROPVARIANT var;
            var.vt = VT_I4;
            var.lVal = MFNET_PROXYSETTING_AUTO;

            hr = pProp->SetValue(key, var);
        }

        //Create the default proxy locator.

        if(SUCCEEDED(hr))
        {
            hr = MFCreateProxyLocator(pszProtocol, pProp, ppProxyLocator);
        }

        SafeRelease(&pProp);
        return hr;
    }
};
```



<span data-ttu-id="7e58d-122">Nell'esempio seguente viene illustrato come passare il puntatore [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) all'origine di rete.</span><span class="sxs-lookup"><span data-stu-id="7e58d-122">The next example shows how to pass the [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) pointer to the network source.</span></span>


```C++
// Creates a media source from a URL.
//
// This example demonstrates how to set a proxy locator on the network source.

HRESULT CreateMediaSourceWithProxyLocator(
    PCWSTR pszURL, 
    IMFMediaSource **ppSource
    )
{
    IPropertyStore *pConfig = NULL;

    IMFNetProxyLocatorFactory *pFactory = new (std::nothrow) CProxyLocatorFactory();

    if (pFactory == NULL)
    {
        return E_OUTOFMEMORY;
    }

    // Configure the property store.
    HRESULT hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pConfig));

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid =  MFNETSOURCE_PROXYLOCATORFACTORY;
        key.pid = 0;

        PROPVARIANT var;
        var.vt = VT_UNKNOWN;
        var.punkVal = pFactory;

        hr = pConfig->SetValue(key, var);
    }

    // Create the source media source.
    if (SUCCEEDED(hr))
    {
        hr = CreateMediaSource(pszURL, pConfig, ppSource);
    }

    SafeRelease(&pConfig);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="7e58d-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7e58d-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e58d-124">Supporto del proxy per le origini di rete</span><span class="sxs-lookup"><span data-stu-id="7e58d-124">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 



