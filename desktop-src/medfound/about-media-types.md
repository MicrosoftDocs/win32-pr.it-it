---
description: Informazioni sui tipi di supporti in Microsoft Media Foundation. Un tipo di supporto descrive il formato di un flusso multimediale.
ms.assetid: 169cdb00-0c1a-4530-90b7-bc89c71d1d04
title: Informazioni sui tipi di supporti (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 263c2b473e378e6ae5dc75453b20d02dce61818f
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010904"
---
# <a name="about-media-types-microsoft-media-foundation"></a>Informazioni sui tipi di supporti (Microsoft Media Foundation)

Un *tipo di* supporto descrive il formato di un flusso multimediale. In Microsoft Media Foundation, i tipi di supporti sono rappresentati [**dall'interfaccia IMFMediaType.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) Questa interfaccia eredita [**l'interfaccia IMFAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) I dettagli di un tipo di supporto vengono specificati come attributi.

Per creare un nuovo tipo di supporto, chiamare la [**funzione MFCreateMediaType.**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) Questa funzione restituisce un puntatore [**all'interfaccia IMFMediaType.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) Il tipo di supporto inizialmente non ha attributi. Per impostare i dettagli del formato, impostare gli attributi pertinenti.

Per un elenco degli attributi del tipo di supporto, vedere [Attributi del tipo di supporto.](media-type-attributes.md)

## <a name="major-types-and-subtypes"></a>Tipi principali e sottotipi

Due informazioni importanti per qualsiasi tipo di supporto sono il tipo principale e il sottotipo.

-   Il *tipo principale* è un GUID che definisce la categoria complessiva dei dati in un flusso multimediale. I tipi principali includono video e audio. Per specificare il tipo principale, impostare [l'attributo \_ MF MT \_ MAJOR \_ TYPE.](mf-mt-major-type-attribute.md) Il [**metodo IMFMediaType::GetMajorType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype) restituisce il valore di questo attributo.
-   Il *sottotipo* definisce ulteriormente il formato. Ad esempio, all'interno del tipo principale video, sono presenti sottotipi per RGB-24, RGB-32, YUY2 e così via. All'interno dell'audio sono presenti audio PCM, audio a virgola mobile IEEE e altri. Il sottotipo fornisce più informazioni rispetto al tipo principale, ma non definisce tutti gli elementi relativi al formato. Ad esempio, i sottotipi video non definiscono le dimensioni dell'immagine o la frequenza dei fotogrammi. Per specificare il sottotipo, impostare [l'attributo \_ MF MT \_ SUBTYPE.](mf-mt-subtype-attribute.md)

Tutti i tipi di supporti devono avere un GUID di tipo principale e un GUID di sottotipo. Per un elenco di GUID di tipo principale e sottotipo, vedere [GUID del tipo di supporto.](media-type-guids.md)

## <a name="why-attributes"></a>Perché gli attributi?

Gli attributi presentano diversi vantaggi rispetto alle strutture di formato usate nelle tecnologie precedenti, ad esempio DirectShow e Windows Media Format SDK.

-   È più facile rappresentare valori "non so" o "non importa". Ad esempio, se si scrive una trasformazione video, è possibile sapere in anticipo quali formati RGB e YUV supportano la trasformazione, ma non le dimensioni del fotogramma video, fino a quando non vengono scaricati dall'origine video. Allo stesso modo, è possibile che non si sia a importare di alcuni dettagli, ad esempio le primarie video. Con una struttura di formato, ogni membro deve essere riempito con *un valore.* Di conseguenza, è diventato comune usare zero per indicare un valore sconosciuto o predefinito. Questa procedura può causare errori se un altro componente considera zero come valore legittimo. Con gli attributi è sufficiente omettere gli attributi sconosciuti o non rilevanti per il componente.

-   Quando i requisiti sono cambiati nel tempo, le strutture di formato sono state estese aggiungendo altri dati alla fine della struttura. Ad esempio, **WAVEFORMATEXTENSIBLE** estende la **struttura WAVEFORMATEX.** Questa procedura è increscita da errori, perché i componenti devono eseguire il cast dei puntatori di struttura ad altri tipi di struttura. Gli attributi possono essere estesi in modo sicuro.
-   Sono state definite strutture di formato reciprocamente incompatibili. Ad esempio, DirectShow definisce le **strutture VIDEOINFOHEADER** e **VIDEOINFOHEADER2.** Gli attributi vengono impostati indipendentemente l'uno dall'altro, pertanto questo problema non si verifica.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> <dt>

[Tipi di supporti](media-types.md)
</dt> </dl>

 

 



