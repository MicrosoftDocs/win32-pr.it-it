---
description: Questo argomento descrive come scrivere un gestore delle proprietà shell personalizzato per un'Microsoft Media Foundation multimediale.
ms.assetid: f8cf70ff-8324-4308-8adf-a145aa351ca9
title: Provider di metadati personalizzati per file multimediali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1951fd90265299cb53369d521193740b7d4d05e0f1650583965eb670ab375cc1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777601"
---
# <a name="custom-metadata-providers-for-media-files"></a>Provider di metadati personalizzati per file multimediali

Questo argomento descrive come scrivere un gestore delle proprietà shell personalizzato per un'Microsoft Media Foundation multimediale.

> [!Note]  
> Per informazioni di base sui provider di metadati in Media Foundation, vedere [Metadati multimediali.](media-metadata.md) In questo argomento vengono illustrati i gestori delle proprietà della shell. non descrive l'interfaccia dei metadati della versione 1, [**IMFMetadata.**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata)

 

I metadati sono strettamente collegati al formato del file. In Media Foundation i formati di file sono rappresentati da origini multimediali. Se si desidera supportare i metadati per un formato non supportato in modo nativo in Media Foundation, è necessario implementare un'origine multimediale personalizzata con un gestore delle proprietà. Il gestore delle proprietà consente al sistema di proprietà shell di leggere e scrivere metadati in modo efficiente.

Un gestore delle proprietà è un oggetto COM che implementa le interfacce seguenti:

-   [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream)
-   [**Ipropertystore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

Facoltativamente, può anche esporre l'interfaccia seguente:

-   [**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities)

Se il sistema di proprietà shell deve ottenere i metadati per un file, chiama [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per creare il gestore delle proprietà e quindi chiama i metodi di lettura e scrittura appropriati [**sull'interfaccia IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

La Media Foundation pipeline usa un meccanismo leggermente diverso, perché la pipeline ottiene il gestore delle proprietà direttamente dall'origine multimediale. Invece di chiamare [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per creare il gestore delle proprietà, la pipeline chiama [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) sull'origine multimediale, come descritto nell'argomento Provider di metadati [della shell](shell-metadata-providers.md).

Per creare un gestore di proprietà personalizzato, eseguire le operazioni seguenti:

-   Implementare [**l'interfaccia IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) per esporre [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore) Il GUID del servizio è **MF \_ PROPERTY HANDLER \_ \_ SERVICE**.
-   Se l'origine multimediale verrà usata in remoto, deve esporre anche l'interfaccia [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) tramite il metodo **QueryInterface** dell'origine multimediale, oltre a [**IMFGetService.**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   Per rendere il gestore delle proprietà disponibile per il sistema di proprietà della shell, registrare la DLL per il gestore delle proprietà come descritto in Registrazione e distribuzione [di gestori di proprietà.](../properties/prophand-reg-dist.md)
-   L'origine multimediale viene registrata separatamente, come descritto in [Scheme Handlers e Byte-Stream Handlers](scheme-handlers-and-byte-stream-handlers.md).

### <a name="implementation-tips"></a>Implementazione Suggerimenti

Per un elenco delle chiavi delle proprietà dei metadati, vedere [Proprietà dei metadati per i file multimediali.](metadata-properties-for-media-files.md)

I gestori di proprietà devono essere veloci. devono fornire un accesso efficiente in lettura e scrittura ai metadati. Si consideri che la shell può recuperare metadati da centinaia di file. Pertanto, non chiamare [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) dal gestore delle proprietà. La **funzione MFStartup** introduce la latenza di avvio, perché crea più thread della coda di lavoro e alloca memoria globale.

In un'implementazione tipica, il gestore della proprietà e l'origine multimediale condividono parte dello stesso codice di analisi. Tuttavia, un'origine multimediale usa chiamate [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) asincrone per L/O, mentre il gestore delle proprietà usa [**l'interfaccia IStream.**](/windows/win32/api/objidl/nn-objidl-istream) Media Foundation fornisce un oggetto helper che esegue il wrapping di un flusso basato su **IStream** e lo espone come **flusso IMFByteStream.** Per creare il wrapper, chiamare [**MFCreateMFByteStreamOnStream.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemfbytestreamonstream)

Quando si aggiornano i metadati, è consigliabile scrivere i dati direttamente nel flusso originale. Questa raccomandazione è diversa dal *comportamento di copia in* scrittura della maggior parte dei gestori di proprietà, in cui viene modificata una copia dei dati. I file multimediali possono essere molto grandi, quindi la copia in scrittura è in genere troppo lenta per un'implementazione efficiente. Per disabilitare la copia in scrittura, impostare l'impostazione **manualSafeSave** del Registro di sistema, come descritto in Registrazione e distribuzione [di gestori di proprietà.](../properties/prophand-reg-dist.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Metadati multimediali](media-metadata.md)
</dt> <dt>

[Origini multimediali](media-sources.md)
</dt> <dt>

[Scrittura di un'origine multimediale personalizzata](writing-a-custom-media-source.md)
</dt> </dl>

 

 
