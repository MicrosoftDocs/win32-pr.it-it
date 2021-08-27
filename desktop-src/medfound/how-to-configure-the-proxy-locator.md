---
description: Come configurare il localizzatore di proxy
ms.assetid: ddc28add-ebf5-4a68-bdf4-dc5f33ab74da
title: Come configurare il localizzatore di proxy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51dcade0909159856c4286d9c2cd5d4851d10b6d2c5e56054545bdac312e21b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061541"
---
# <a name="how-to-configure-the-proxy-locator"></a>Come configurare il localizzatore di proxy

L'applicazione può modificare la configurazione predefinita del localizzatore proxy impostando la proprietà [MFNETSOURCE \_ PROXYLOCATORFACTORY](mfnetsource-proxylocatorfactory-property.md) sull'oggetto factory del localizzatore proxy implementato dall'applicazione. Quando l'applicazione chiama i metodi del resolver di origine per creare l'origine di rete, Media Foundation chiama la factory del localizzatore proxy. Questo oggetto crea il localizzatore proxy con configurazione personalizzata.

## <a name="to-change-the-default-configuration-setting-of-the-proxy-locator"></a>Per modificare l'impostazione di configurazione predefinita del localizzatore proxy

1.  Implementare [**l'interfaccia IMFNetProxyLocatorFactory.**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory)
2.  Nel metodo [**IMFNetProxyLocatorFactory::CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) eseguire le operazioni seguenti:
    1.  Creare un archivio delle proprietà.
    2.  Impostare le impostazioni di configurazione per il localizzatore proxy. Per informazioni su queste impostazioni, vedere [Proxy Locator Configuration Impostazioni](proxy-locator-configuration-settings.md).
    3.  Chiamare la [**funzione MFCreateProxyLocator.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) Passare l'archivio delle proprietà e il protocollo. Il protocollo è specificato nel *parametro pszProtocol* di [**CreateProxyLocator.**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator)
3.  Creare un'istanza della classe factory del localizzatore proxy e ottenere un puntatore alla relativa [**interfaccia IMFNetProxyLocatorFactory.**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory)
4.  Creare un altro archivio proprietà e impostare il valore della proprietà [**MFNETSOURCE \_ PROXYLOCATORFACTORY**](mfnetsource-proxylocatorfactory-property.md) uguale al puntatore [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) del passaggio 3.
5.  Quando si crea l'origine di rete, passare l'archivio delle proprietà nel parametro *pProps* dei metodi del resolver di origine, ad esempio [**IMFSourceResolver::BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl).

## <a name="example"></a>Esempio

L'esempio di codice seguente implementa [**l'interfaccia IMFNetProxyLocatorFactory.**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) Il [**metodo IMFNetProxyLocatorFactory::CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) crea un'istanza del localizzatore proxy predefinito e la configura per operare in modalità di rilevamento automatico.


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



L'esempio seguente illustra come passare il puntatore [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) all'origine di rete.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Supporto proxy per origini di rete](proxy-support-for-network-sources.md)
</dt> </dl>

 

 



