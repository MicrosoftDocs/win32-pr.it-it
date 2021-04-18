---
description: In questo argomento viene descritto come scrivere un gestore di proprietà della shell personalizzato per un Microsoft Media Foundation origine multimediale.
ms.assetid: f8cf70ff-8324-4308-8adf-a145aa351ca9
title: Provider di metadati personalizzati per i file multimediali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2ded77492d03f7b802f6b2f9c25e1009ef97f50
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320725"
---
# <a name="custom-metadata-providers-for-media-files"></a>Provider di metadati personalizzati per i file multimediali

In questo argomento viene descritto come scrivere un gestore di proprietà della shell personalizzato per un Microsoft Media Foundation origine multimediale.

> [!Note]  
> Per informazioni generali sui provider di metadati in Media Foundation, vedere [metadati del supporto](media-metadata.md). In questo argomento vengono illustrati i gestori delle proprietà della shell. non descrive l'interfaccia dei metadati della versione 1, [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata).

 

I metadati sono strettamente legati al formato del file. In Media Foundation i formati di file sono rappresentati da origini multimediali. Se si desidera supportare i metadati per un formato non supportato in modo nativo in Media Foundation, è necessario implementare un'origine multimediale personalizzata con un gestore proprietà. Il gestore proprietà consente al sistema di proprietà della shell di leggere e scrivere i metadati in modo efficiente.

Un gestore proprietà è un oggetto COM che implementa le interfacce seguenti:

-   [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream)
-   [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

Facoltativamente, può anche esporre l'interfaccia seguente:

-   [**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities)

Se il sistema di proprietà della shell deve ottenere i metadati per un file, chiama [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per creare il gestore della proprietà, quindi chiama i metodi di lettura e scrittura appropriati sull'interfaccia [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .

La pipeline Media Foundation usa un meccanismo leggermente diverso, perché la pipeline ottiene il gestore della proprietà direttamente dall'origine multimediale. Anziché chiamare [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per creare il gestore della proprietà, la pipeline chiama [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) nell'origine del supporto, come descritto nell'argomento [provider di metadati della shell](shell-metadata-providers.md).

Per creare un gestore di proprietà personalizzato, eseguire le operazioni seguenti:

-   Implementare l'interfaccia [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) per esporre [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore). Il GUID del servizio è il **\_ servizio del \_ gestore \_ delle proprietà MF**.
-   Se l'origine supporto verrà usata in modalità remota, deve anche esporre l'interfaccia [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) tramite il metodo **QueryInterface** dell'origine multimediale, oltre a [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice).
-   Per rendere disponibile il gestore delle proprietà per il sistema di proprietà della shell, registrare la DLL per il gestore della proprietà come descritto in [registrazione e distribuzione dei gestori di proprietà](../properties/prophand-reg-dist.md).
-   L'origine multimediale viene registrata separatamente, come descritto in [gestori di schemi e gestori di Byte-Stream](scheme-handlers-and-byte-stream-handlers.md).

### <a name="implementation-tips"></a>Suggerimenti per l'implementazione

Per un elenco di chiavi di proprietà dei metadati, vedere [proprietà dei metadati per i file multimediali](metadata-properties-for-media-files.md).

I gestori di proprietà devono essere veloci; devono fornire un accesso in lettura e scrittura efficiente ai metadati. (Si consideri che la shell può recuperare i metadati da centinaia di file). Pertanto, non chiamare [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) dal gestore della proprietà. La funzione **MFStartup** introduce la latenza di avvio, perché crea più thread della coda di lavoro e alloca memoria globale.

In un'implementazione tipica, il gestore della proprietà e l'origine multimediale condividono parte dello stesso codice di analisi. Tuttavia, un'origine multimediale usa le chiamate [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) asincrone per i/O, mentre il gestore delle proprietà usa l'interfaccia [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) . Media Foundation fornisce un oggetto helper che esegue il wrapping di un flusso basato su **IStream** e lo espone come flusso **IMFByteStream** . Per creare il wrapper, chiamare [**MFCreateMFByteStreamOnStream**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemfbytestreamonstream).

Quando si aggiornano i metadati, è consigliabile scrivere i dati direttamente nel flusso originale. Questa raccomandazione differisce dal comportamento di *copia su scrittura* della maggior parte dei gestori di proprietà, in cui una copia dei dati viene modificata. I file multimediali possono essere molto grandi, quindi la copia in scrittura è in genere troppo lenta per un'implementazione efficiente. Per disabilitare la copia in scrittura, impostare l'impostazione del registro di sistema **ManualSafeSave** , come descritto in [registrazione e distribuzione di gestori di proprietà](../properties/prophand-reg-dist.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Metadati del supporto](media-metadata.md)
</dt> <dt>

[Origini supporti](media-sources.md)
</dt> <dt>

[Scrittura di un'origine multimediale personalizzata](writing-a-custom-media-source.md)
</dt> </dl>

 

 
