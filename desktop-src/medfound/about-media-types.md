---
description: Informazioni sui tipi di supporto
ms.assetid: 169cdb00-0c1a-4530-90b7-bc89c71d1d04
title: Informazioni sui tipi di supporto (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca1ee75979c5c382e7e4ea458655efb83435a22d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103968847"
---
# <a name="about-media-types-microsoft-media-foundation"></a>Informazioni sui tipi di supporto (Microsoft Media Foundation)

Un *tipo di supporto* descrive il formato di un flusso multimediale. In Microsoft Media Foundation i tipi di supporto sono rappresentati dall'interfaccia [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) . Questa interfaccia eredita l'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) . I dettagli di un tipo di supporto vengono specificati come attributi.

Per creare un nuovo tipo di supporto, chiamare la funzione [**MFCreateMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) . Questa funzione restituisce un puntatore all'interfaccia [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) . Il tipo di supporto inizialmente non ha attributi. Per impostare i dettagli del formato, impostare gli attributi pertinenti.

Per un elenco degli attributi del tipo di supporto, vedere [attributi del tipo di supporto](media-type-attributes.md).

## <a name="major-types-and-subtypes"></a>Tipi e sottotipi principali

Due informazioni importanti per qualsiasi tipo di supporto sono il tipo principale e il sottotipo.

-   Il *tipo principale* è un GUID che definisce la categoria complessiva dei dati in un flusso multimediale. I tipi principali includono video e audio. Per specificare il tipo principale, impostare l'attributo di [ \_ \_ \_ tipo principale MF mt](mf-mt-major-type-attribute.md) . Il metodo [**IMFMediaType:: GetMajorType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype) restituisce il valore di questo attributo.
-   Il *sottotipo* definisce ulteriormente il formato. Ad esempio, all'interno del tipo principale video sono presenti sottotipi per RGB-24, RGB-32, YUY2 e così via. All'interno dell'audio sono disponibili audio PCM, audio a virgola mobile IEEE e altri. Il sottotipo fornisce più informazioni rispetto al tipo principale, ma non definisce tutti gli elementi del formato. Ad esempio, i sottotipi video non definiscono le dimensioni dell'immagine o la frequenza dei fotogrammi. Per specificare il sottotipo, impostare l'attributo del [ \_ \_ sottotipo MF mt](mf-mt-subtype-attribute.md) .

Tutti i tipi di supporto devono avere un GUID di tipo principale e un GUID del sottotipo. Per un elenco di GUID di tipo e sottotipo principale, vedere [GUID di tipo di supporto](media-type-guids.md).

## <a name="why-attributes"></a>Perché attributi?

Gli attributi presentano diversi vantaggi rispetto alle strutture di formato usate nelle tecnologie precedenti, ad esempio DirectShow e Windows Media Format SDK.

-   È più semplice rappresentare i valori "Don ' t know" o "not care". Se, ad esempio, si scrive una trasformazione video, è possibile che si sappia in anticipo quali formati RGB e YUV sono supportati dalla trasformazione, ma non le dimensioni del frame video, fino a quando non vengono recuperati dall'origine video. Analogamente, è possibile che non si sia interessati a determinati dettagli, ad esempio le primarie video. Con una struttura di formato, ogni membro deve essere riempito con *un valore.* Di conseguenza, è diventato comune usare zero per indicare un valore sconosciuto o predefinito. Questa procedura può causare errori se un altro componente considera zero come valore legittimo. Con gli attributi è sufficiente omettere gli attributi sconosciuti o non rilevanti per il componente.

-   Poiché i requisiti sono stati modificati nel tempo, le strutture di formato sono state estese aggiungendo dati aggiuntivi alla fine della struttura. **WAVEFORMATEXTENSIBLE** , ad esempio, estende la struttura **WAVEFORMATEX** . Questa pratica è soggetta a errori, perché i componenti devono eseguire il cast dei puntatori alla struttura ad altri tipi di struttura. Gli attributi possono essere estesi in modo sicuro.
-   Sono state definite strutture di formato incompatibili a vicenda. Ad esempio, DirectShow definisce le strutture **VIDEOINFOHEADER** e **VIDEOINFOHEADER2** . Gli attributi vengono impostati indipendentemente l'uno dall'altro, quindi questo problema non si verifica.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> <dt>

[Tipi di supporto](media-types.md)
</dt> </dl>

 

 



