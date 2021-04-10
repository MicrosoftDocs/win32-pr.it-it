---
description: Uso del resolver di origine
ms.assetid: 94e2a411-96b8-4506-8491-78f4f5f286ce
title: Uso del resolver di origine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e992199b097ff3f3337f92216b684d68e46bca13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226901"
---
# <a name="using-the-source-resolver"></a>Uso del resolver di origine

Il resolver dell'origine accetta un URL o un flusso di byte e crea l'origine multimediale appropriata per il contenuto. Per creare il resolver di origine, chiamare [**MFCreateSourceResolver**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver). Questa funzione restituisce un puntatore di interfaccia [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) .

Il resolver di origine include metodi sincroni e asincroni. Se si usa il resolver di origine dal thread dell'applicazione principale, i metodi asincroni rendono più reattiva l'interfaccia utente. I metodi sincroni possono bloccarsi per un periodo di tempo significativo, in particolare se il resolver di origine deve aprire una risorsa di rete.

I metodi sincroni sono:

-   [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl)
-   [**IMFSourceResolver::CreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream)

I metodi asincroni sono:

-   [**IMFSourceResolver::BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl)
-   [**IMFSourceResolver::BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream)

Per i metodi asincroni, ogni metodo dispone di un metodo **end..** . corrispondente per completare la richiesta asincrona e un metodo **Cancel...** per annullare una richiesta in sospeso. Per ulteriori informazioni sui metodi asincroni in Media Foundation, vedere [metodi di callback asincroni](asynchronous-callback-methods.md).

Nell'esempio di codice seguente viene creata un'origine multimediale da un URL. In questo esempio viene usato il metodo sincrono.


```C++
//  Create a media source from a URL.
HRESULT CreateMediaSource(PCWSTR sURL, IMFMediaSource **ppSource)
{
    MF_OBJECT_TYPE ObjectType = MF_OBJECT_INVALID;

    IMFSourceResolver* pSourceResolver = NULL;
    IUnknown* pSource = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pSourceResolver);
    if (FAILED(hr))
    {
        goto done;
    }

    // Use the source resolver to create the media source.

    // Note: For simplicity this sample uses the synchronous method to create 
    // the media source. However, creating a media source can take a noticeable
    // amount of time, especially for a network source. For a more responsive 
    // UI, use the asynchronous BeginCreateObjectFromURL method.

    hr = pSourceResolver->CreateObjectFromURL(
        sURL,                       // URL of the source.
        MF_RESOLUTION_MEDIASOURCE,  // Create a source object.
        NULL,                       // Optional property store.
        &ObjectType,        // Receives the created object type. 
        &pSource            // Receives a pointer to the media source.
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the IMFMediaSource interface from the media source.
    hr = pSource->QueryInterface(IID_PPV_ARGS(ppSource));

done:
    SafeRelease(&pSourceResolver);
    SafeRelease(&pSource);
    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Resolver di origine](source-resolver.md)
</dt> </dl>

 

 



