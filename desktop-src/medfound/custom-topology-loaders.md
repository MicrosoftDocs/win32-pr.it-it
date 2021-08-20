---
description: Caricatori di topologia personalizzati
ms.assetid: 3982b07e-3179-45c1-9f17-f2114363f53d
title: Caricatori di topologia personalizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02ca9cf393b83693199cea984183bf88186f74322ed816352e3c43d19a6e880b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117880386"
---
# <a name="custom-topology-loaders"></a>Caricatori di topologia personalizzati

Quando un'applicazione accoda una topologia parziale nella sessione multimediale, la sessione multimediale usa un caricatore di topologia per risolvere la topologia. Per impostazione predefinita, la sessione multimediale usa l'implementazione Media Foundation standard del caricatore della topologia, ma è anche possibile fornire un'implementazione personalizzata. In questo modo si ha maggiore controllo sulla topologia finale. Un caricatore di topologia personalizzato deve implementare [**l'interfaccia IMFTopoLoader.**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)

Per impostare un caricatore di topologia personalizzato nella sessione multimediale, eseguire le operazioni seguenti:

1.  Creare un archivio attributi vuoto chiamando [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).
2.  Impostare [**l'attributo \_ MF SESSION \_ TOPOLOADER**](mf-session-topoloader-attribute.md) nell'archivio attributi. Il valore dell'attributo è il CLSID del caricatore personalizzato.
3.  Chiamare [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) per creare la sessione multimediale per il contenuto non protetto oppure [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) per creare la sessione multimediale all'interno del percorso del supporto protetto (PMP).

> [!Note]  
> Per usare un caricatore di topologia personalizzato all'interno del PMP, il caricatore di topologia deve essere un componente attendibile. Per altre informazioni, vedere [Percorso del supporto protetto.](protected-media-path.md)

 

Il codice seguente illustra come impostare un caricatore di topologia personalizzato nella sessione multimediale.


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



Non è necessario implementare l'intero algoritmo di caricamento della topologia nel caricatore della topologia. In alternativa, è possibile eseguire il wrapping del caricatore Media Foundation topologia standard. Nell'implementazione del [**metodo IMFTopoLoader::Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) modificare la topologia in base alle esigenze e passare la topologia modificata al caricatore della topologia standard. Il caricatore della topologia standard completa quindi la topologia. È anche possibile modificare la topologia completata prima di passarla nuovamente alla sessione multimediale.

Il codice seguente illustra la struttura generale di questo approccio. Non vengono visualizzati dettagli del metodo [**Load,**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) perché dipendono dai requisiti specifici dell'applicazione.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**MFCreateTopoLoader**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopoloader)
</dt> <dt>

[Compilazione avanzata della topologia](advanced-topology-building.md)
</dt> </dl>

 

 



