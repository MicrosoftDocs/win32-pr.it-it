---
description: Impostazione di una gestione credenziali
ms.assetid: a20c2e6c-e9d9-438f-a57a-e3080587c11c
title: Impostazione di una gestione credenziali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c98d9d9572438a63f93f916a0084f8a33a7bca5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309000"
---
# <a name="setting-a-credential-manager"></a>Impostazione di una gestione credenziali

Un'applicazione che fornisce le credenziali per l'origine di rete deve eseguire le operazioni seguenti:

1.  Implementare un oggetto di gestione delle credenziali che espone l'interfaccia [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) .
2.  Prima di creare l'origine di rete, creare un nuovo archivio delle proprietà.
3.  Impostare la proprietà [**MFNETSOURCE \_ Credential \_ Manager**](mfnetsource-credential-manager-property.md) nell'archivio delle proprietà. Il valore della proprietà è un puntatore all'interfaccia [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) .
4.  Passare un puntatore all'archivio delle proprietà al resolver di origine, come descritto in [configurazione di un'origine multimediale](configuring-a-media-source.md).

Le origini di rete usano Gestione credenziali per ottenere le credenziali utente. Se l'origine di rete richiede credenziali per accedere a una risorsa di rete, viene chiamato il metodo [**IMFNetCredentialManager:: BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) dell'applicazione. Questa chiamata avvia una richiesta asincrona per ottenere le credenziali dell'utente. Il metodo **BeginGetCredentials** può ottenere le credenziali dalla cache delle credenziali o dall'utente. Le credenziali vengono archiviate in un *oggetto credenziale*. Al termine dell'operazione, l'applicazione richiama l'interfaccia di callback per notificare all'origine di rete. L'origine di rete chiama [**IMFNetCredentialManager:: EndGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) per completare l'operazione asincrona.

Poiché si tratta di un'operazione asincrona, l'applicazione deve inviare il callback alla fine dell'operazione. Per istruzioni dettagliate sulla scrittura di un metodo asincrono, vedere [scrittura di un metodo asincrono](writing-an-asynchronous-method.md).

Nell'esempio seguente viene illustrato come impostare la proprietà [**MFNETSOURCE \_ Credential \_ Manager**](mfnetsource-credential-manager-property.md) nell'origine di rete.


```C++
// Creates a media source from a URL.
//
// Demonstrates how to set a credential manager on the network source.

HRESULT CreateMediaSourceWithCredentialManager(
    PCWSTR pszURL, 
    IMFMediaSource **ppSource
    )
{
    IPropertyStore *pConfig = NULL;

    CCredentialManager *pCredentials = new (std::nothrow) CCredentialManager();

    if (pCredentials == NULL)
    {
        return E_OUTOFMEMORY;
    }

    // Configure the property store.
    HRESULT hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pConfig));

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid =  MFNETSOURCE_CREDENTIAL_MANAGER;
        key.pid = 0;

        PROPVARIANT var;
        var.vt = VT_UNKNOWN;
        pCredentials->QueryInterface(IID_PPV_ARGS(&var.punkVal));

        hr = pConfig->SetValue(key, var);

        PropVariantClear(&var);
    }

    // Create the source media source.
    if (SUCCEEDED(hr))
    {
        hr = CreateMediaSource(pszURL, pConfig, ppSource);
    }

    SafeRelease(&pConfig);
    SafeRelease(&pCredentials);

    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Autenticazione origine rete](network-source-authentication.md)
</dt> </dl>

 

 



