---
description: Tipi di supporto DMO
ms.assetid: 40958e12-09c7-4ce5-aa4d-5ed8b1f40aa3
title: Tipi di supporto DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1997abb1cc3c8eb10301778982ef7a46690855ed
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104530552"
---
# <a name="dmo-media-types"></a>Tipi di supporto DMO

Un tipo di supporto descrive il formato associato a un flusso di dati multimediali. Questo articolo descrive il modo in cui DMOs gestisce i tipi di supporto. È destinato principalmente agli sviluppatori che scrivono un DMOs personalizzato.

I tipi di supporto vengono definiti utilizzando la struttura del [**\_ \_ tipo di supporto DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) . Questa struttura include le informazioni seguenti:

-   Il *tipo principale* è un identificatore univoco globale (Guid) che definisce un'ampia categoria, ad esempio audio o video.
-   Il *sottotipo* è un GUID che definisce aspetti più specifici del tipo. Ad esempio, all'interno di video, i sottotipi includono RGB a 16 bit, RGB a 24 bit, UYVY, video con codifica DV e così via.
-   Il *blocco di formato* è una struttura secondaria che specifica completamente il formato. Il layout del blocco di formato dipende dal tipo di dati. Ad esempio, l'audio PCM usa la struttura **WAVEFORMATEX** . Il video usa diverse altre strutture, tra cui **VIDEOINFOHEADER** e **VIDEOINFOHEADER2**. Il layout del blocco di formato è identificato da un GUID di tipo di formato. Ad esempio, FORMAT \_ WAVEFORMATEX specifica una struttura **WAVEFORMATEX** .

Quando un DMO viene creato per la prima volta, i flussi non hanno un tipo di supporto. Prima che DMO possa elaborare i dati, il client deve impostare un tipo di supporto per ogni flusso. Questo processo viene descritto dal punto di vista del client nell' [impostazione dei tipi di supporto in un DMO](setting-media-types-on-a-dmo.md).

**Tipi di supporto nel registro di sistema**

Un DMO può aggiungere un elenco di tipi di supporti che supporta al registro di sistema, chiamando la funzione [**DMORegister**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoregister) . Un'applicazione può usare queste informazioni per cercare DMOs che corrispondano a un particolare formato. Le informazioni nel registro di sistema non sono destinate a essere complete. In genere, si includono solo i tipi principali supportati da DMO. La voce del registro di sistema ha chiavi separate per i tipi di input e di output, ma non distingue tra i singoli flussi.

La funzione **DMORegister** usa la [**struttura \_ \_ MEDIATYPE parziale DMO**](/previous-versions/windows/desktop/api/Dmoreg/ns-dmoreg-dmo_partial_mediatype) per descrivere i tipi di supporto. Questa struttura contiene un subset delle informazioni disponibili nella struttura del **\_ \_ tipo di supporto DMO** , ovvero il tipo principale e il sottotipo. Non include un blocco di formato perché il blocco di formato contiene in genere informazioni troppo granulari da includere nel registro di sistema, ad esempio l'altezza e la larghezza di un'immagine video.

**Tipi di supporti preferiti**

Dopo che l'applicazione ha creato un DMO, può eseguire una query su DMO per i tipi di supporto supportati. Per ogni flusso, DMO crea un elenco di tipi di supporti (possibilmente vuoti), classificati in ordine di preferenza. I metodi [**IMediaObject:: GetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputtype) e [**IMediaObject:: GetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputtype) enumerano i tipi preferiti. I tipi preferiti di un flusso possono cambiare in modo dinamico quando l'applicazione imposta i tipi di supporto su altri flussi. Ad esempio, l'elenco dei tipi di output preferiti può variare dopo l'impostazione del tipo di input o viceversa. Tuttavia, non è necessario che il DMO aggiorni i tipi preferiti in modo dinamico. L'applicazione non può presumere che tutti i tipi ricevuti siano validi. Per questo motivo, i metodi [**IMediaObject:: SetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setinputtype) e [**IMediaObject:: SetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setoutputtype) supportano un flag per il test di un tipo specifico.

I metodi **GetInputType** e **GetOutputType** restituiscono entrambi una struttura del **\_ \_ tipo di supporto DMO** . DMO può lasciare vuote alcune informazioni in questa struttura per indicare un intervallo di tipi. Il tipo o il sottotipo principale può essere \_ null GUID e il blocco di formato può essere vuoto (zero byte). Se il blocco di formato è vuoto, il tipo di formato deve essere GUID \_ null.

Dopo che l'applicazione ha impostato tutti i tipi di input DMO, in genere DMO deve restituire almeno un tipo completo per ogni flusso di output. Un tipo di output completo facilita i test e le applicazioni possono utilizzarlo come valore predefinito ragionevole. L'applicazione di test DMO si basa su questo comportamento. Vedere [utilizzo dell'applicazione DMOTest](using-the-dmotest-application.md).

**Impostazione dei tipi di supporto**

Le applicazioni utilizzano i metodi **SetInputType** e **SetOutputType** per testare, impostare o cancellare i tipi in un flusso specificato. L'applicazione deve specificare completamente il tipo. DMO verifica se può accettare il tipo proposto. La risposta può dipendere dai tipi impostati in altri flussi. Il \_ flag DMO set \_ TYPEF \_ Clear cancella il tipo di un flusso, in modo che l'applicazione possa "tornare indietro" e provare un'altra combinazione.

**Scenari di esempio**

Negli esempi seguenti vengono descritti alcuni scenari tipici, per illustrare i punti creati nelle sezioni precedenti.

-   **Decodificatori video.** In un decodificatore video tipico, il tipo di input determina in parte il tipo di output. Ad esempio, in genere entrambi i flussi devono avere la stessa frequenza dei fotogrammi e le stesse dimensioni di immagine. Una delle opzioni non è quella di definire i tipi di output preferiti fino a quando non viene impostato il tipo di input. Un'altra opzione consiste nell'enumerare un set di tipi incompleti, omettendo il blocco di formato. Usare il sottotipo per indicare i tipi non compressi supportati, ad esempio RGB a 16 bit, RGB a 24 bit e così via. Inoltre, i decodificatori video in genere non supportano l'impostazione del tipo di output prima del tipo di input. Il solito scenario consiste nel decodificare da un formato di input noto, quindi questa limitazione è ragionevole.
-   **Decodificatori audio.** Un decodificatore audio potrebbe supportare un set di formati di output fisso e limitato. In tal caso, potrebbe essere in grado di creare un elenco di formati di output preferiti prima che il formato di input sia noto.
-   **Compressori.** Nella maggior parte dei casi, un compressore video non può specificare completamente i formati di output preferiti fino a quando l'applicazione non imposta il formato di input e viceversa. Al contrario, DMO deve restituire un tipo incompleto senza blocco di formato. Per la compressione audio e video, in genere l'applicazione deve impostare diversi parametri di output, ad esempio la velocità in bit. Tuttavia, dopo aver impostato il tipo di input, il compressore deve restituire almeno un tipo di output completo per i motivi citati in precedenza.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scrittura di un DMO](writing-a-dmo.md)
</dt> </dl>

 

 



