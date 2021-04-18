---
description: Sblocco di Windows Media Format SDK
ms.assetid: 7ede8bda-3b26-452d-8ce9-cd2410ffd9f4
title: Sblocco di Windows Media Format SDK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e9807794dc7e42c563f2f7d45dcb0b1b684aad1
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320722"
---
# <a name="unlocking-the-windows-media-format-sdk"></a>Sblocco di Windows Media Format SDK

Per accedere alla versione 7 o 7,1 di Windows Media Format SDK, un'applicazione deve fornire un certificato software, detto anche chiave, in fase di esecuzione. Questa chiave è contenuta in una libreria statica denominata wmstub. lib a cui si collega l'applicazione in fase di compilazione. Una chiave individualizzata è necessaria solo per la creazione o la lettura di file protetti da DRM. È possibile creare file non DRM usando la libreria statica fornita con Windows Media Format SDK. Per informazioni dettagliate su come ottenere la chiave DRM, vedere Windows Media Format SDK. Un'applicazione DirectShow fornisce il certificato al writer ASF WM quando viene aggiunto al grafico dei filtri. L'applicazione deve essere registrata come provider chiave utilizzando le interfacce COM **IServiceProvider** e **IObjectWithSite** . Utilizzando questa tecnica, l'applicazione implementa una classe del provider di chiavi derivata da **IServiceProvider**. Questa classe implementa i tre metodi COM standard,**AddRef**, **QueryInterface** e **Release**, insieme a un altro metodo, **QueryService**, che viene chiamato da Filter Graph Manager. **QueryService** chiama il metodo SDK di Windows Media Format [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85)) e torna al gestore del grafico del filtro un puntatore al certificato creato. Se il certificato è valido, il gestore del grafico dei filtri consente di continuare il processo di compilazione del grafico.

> [!Note]  
> Per compilare un'applicazione, includere Wmsdkidl. h per il prototipo per [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85))e collegarsi alla libreria Wmstub. lib.

 

Nell'esempio di codice riportato di seguito vengono illustrati i passaggi di base di questo processo:


```C++
// Declare and implement a key provider class derived from IServiceProvider.

class CKeyProvider : public IServiceProvider {
public:
    // IUnknown interface
    STDMETHODIMP QueryInterface(REFIID riid, void ** ppv);
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();

    CKeyProvider();

    // IServiceProvider
    STDMETHODIMP QueryService(REFIID siid, REFIID riid, void **ppv);
    
private:
    ULONG m_cRef;
};

CKeyProvider::CKeyProvider() : m_cRef(0)
{
}

// IUnknown methods
ULONG CKeyProvider::AddRef()
{
    return InterlockedIncrement(&m_cRef);
}

ULONG CKeyProvider::Release()
{
    ASSERT(m_cRef > 0);

    ULONG lCount = InterlockedDecrement(&m_cRef);
    if (m_cRef == 0) 
    {
        delete this;
        return (ULONG)0;
    }
    return (ULONG)lCount;
}

// We only support IUnknown and IServiceProvider.
HRESULT CKeyProvider::QueryInterface(REFIID riid, void ** ppv)
{
    if (!ppv) return E_POINTER;

    if (riid == IID_IUnknown) 
    {
        *ppv = (void *) static_cast<IUnknown *>(this);
        AddRef();
        return S_OK;
    }
    if (riid == IID_IServiceProvider) 
    {
        *ppv = (void *) static_cast<IServiceProvider *>(this);
        AddRef();
        return S_OK;
    }

    return E_NOINTERFACE;
}

STDMETHODIMP CKeyProvider::QueryService(REFIID siid, REFIID riid, void **ppv)
{
    if (!ppv) return E_POINTER;

    if (siid == __uuidof(IWMReader) && riid == IID_IUnknown) 
    {
        IUnknown *punkCert;
        HRESULT hr = WMCreateCertificate(&punkCert);
        if (SUCCEEDED(hr)) 
        {
            *ppv = (void *) punkCert;
        }
        return hr;
    }
    return E_NOINTERFACE;
}

////////////////////////////////////////////////////////////////////
//
// These examples illustrate the sequence of method calls
// in your application. Error checking is omitted for brevity.
//
///////////////////////////////////////////////////////////////////

// Create the filter graph manager, but don't add any filters.
IGraphBuilder *pGraph;
hr = CreateFilterGraph(&pGraph);

...

// Instantiate the key provider class, and AddRef it
// so that COM doesn't try to free our static object.

CKeyProvider prov;
prov.AddRef();  // Don't let COM try to free our static object.

// Give the graph an IObjectWithSite pointer for callbacks and QueryService.
IObjectWithSite* pObjectWithSite = NULL;

hr = pGraph->QueryInterface(IID_IObjectWithSite, (void**)&pObjectWithSite);
if (SUCCEEDED(hr))
{
    // Use the IObjectWithSite pointer to specify our key provider object.
    // The filter graph manager will use this pointer to call
    // QueryService to do the unlocking.
    // If the unlocking succeeds, then we can build our graph.

    pObjectWithSite->SetSite((IUnknown *) (IServiceProvider *) &prov);
    pObjectWithSite->Release();
}

// Now build the graph.
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di file ASF in DirectShow](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 
