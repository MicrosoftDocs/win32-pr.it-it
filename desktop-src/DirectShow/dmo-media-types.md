---
description: DMO Tipi di supporti
ms.assetid: 40958e12-09c7-4ce5-aa4d-5ed8b1f40aa3
title: DMO Tipi di supporti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0d67be6775163695189c2dc2c2742f65bcd0181032d9935b2a2a3ce2df2e900
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016129"
---
# <a name="dmo-media-types"></a>DMO Tipi di supporti

Un tipo di supporto descrive il formato associato a un flusso di dati multimediali. Questo articolo descrive come le DMO gestiscono i tipi di supporti. È destinato principalmente agli sviluppatori che scrivono dmo personalizzati.

I tipi di supporti vengono definiti usando la [**DMO \_ MEDIA \_ TYPE.**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) Questa struttura include le informazioni seguenti:

-   Il *tipo principale* è un identificatore univoco globale (GUID) che definisce una categoria generale, ad esempio audio o video.
-   Il *sottotipo* è un GUID che definisce aspetti più specifici del tipo. Ad esempio, all'interno del video, i sottotipi includono RGB a 16 bit, RGB a 24 bit, UYVY, video con codifica DV e così via.
-   Il *blocco di* formato è una struttura secondaria che specifica completamente il formato. Il layout del blocco di formato dipende dal tipo di dati. Ad esempio, l'audio PCM usa la **struttura WAVEFORMATEX.** Video usa varie altre strutture, tra cui **VIDEOINFOHEADER** e **VIDEOINFOHEADER2**. Il layout del blocco di formato è identificato da un GUID del tipo di formato. Ad esempio, FORMAT \_ WaveFormatEx specifica una **struttura WAVEFORMATEX.**

Quando un DMO viene creato per la prima volta, i flussi non hanno un tipo di supporto. Prima che il DMO possa elaborare dati, il client deve impostare un tipo di supporto per ogni flusso. Questo processo viene descritto dal punto di vista del client in Impostazione dei tipi di supporti [in un DMO](setting-media-types-on-a-dmo.md).

**Tipi di supporti nel Registro di sistema**

Un DMO può aggiungere un elenco di tipi di supporti supportati al Registro di sistema chiamando la [**funzione DMORegister.**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoregister) Un'applicazione può usare queste informazioni per cercare DMO che corrispondono a un formato specifico. Le informazioni nel Registro di sistema non sono destinate a essere complete. In genere, si includono solo i tipi principali supportati dal DMO. La voce del Registro di sistema ha chiavi separate per i tipi di input e output, ma non distingue tra i singoli flussi.

La **funzione DMORegister** usa la [**struttura DMO PARTIAL \_ \_ MEDIATYPE**](/previous-versions/windows/desktop/api/Dmoreg/ns-dmoreg-dmo_partial_mediatype) per descrivere i tipi di supporti. Questa struttura contiene un subset delle informazioni disponibili nella **DMO \_ MEDIA \_ TYPE,** ovvero il tipo principale e il sottotipo. Non include un blocco di formato, perché il blocco di formato contiene in genere informazioni troppo granulari da includere nel Registro di sistema, ad esempio l'altezza e la larghezza di un'immagine video.

**Tipi di supporti preferiti**

Dopo che l'applicazione ha creato un DMO, può eseguire una query sul DMO per i tipi di supporti supportati. Per ogni flusso, il DMO crea un elenco di tipi di supporti (possibilmente vuoti), classificati in ordine di preferenza. I [**metodi IMediaObject::GetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputtype) e [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputtype) enumerano i tipi preferiti. I tipi preferiti di un flusso possono cambiare in modo dinamico quando l'applicazione imposta tipi di supporti in altri flussi. Ad esempio, l'elenco dei tipi di output preferiti potrebbe cambiare dopo l'impostazione del tipo di input o viceversa. Tuttavia, la DMO non è necessaria per aggiornare i tipi preferiti in modo dinamico. L'applicazione non può presupporre che ogni tipo ricevuto sia valido. Per questo motivo, i metodi [**IMediaObject::SetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setinputtype) e [**IMediaObject::SetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setoutputtype) supportano un flag per il test di un tipo specifico.

Entrambi **i metodi GetInputType** **e GetOutputType** restituiscono una **DMO MEDIA \_ \_ TYPE.** Il DMO può lasciare vuote alcune informazioni in questa struttura, per indicare un intervallo di tipi. Il tipo o il sottotipo principale può essere GUID \_ NULL e il blocco di formato può essere vuoto (zero byte). Se il blocco di formato è vuoto, il tipo di formato deve essere GUID \_ NULL.

Dopo che l'applicazione ha impostato tutti i DMO di input di un DMO, in genere deve restituire almeno un tipo completo per ogni flusso di output. Un tipo di output completo facilita i test e le applicazioni possono usarlo come impostazione predefinita ragionevole. L DMO di test si basa su questo comportamento. Vedere [Uso dell'applicazione DMOTest.](using-the-dmotest-application.md)

**Impostazione dei tipi di supporti**

Le applicazioni usano **i metodi SetInputType** **e SetOutputType** per testare, impostare o cancellare i tipi in un flusso specificato. L'applicazione deve specificare completamente il tipo. Il DMO verifica se può accettare il tipo proposto. La risposta può dipendere dai tipi impostati in altri flussi. Il DMO SET TYPEF CLEAR cancella il tipo di un flusso, in modo che \_ \_ l'applicazione possa eseguire il \_ back-out e provare un'altra combinazione.

**Scenari di esempio**

Gli esempi seguenti descrivono alcuni scenari tipici, per illustrare i punti illustrati nelle sezioni precedenti.

-   **Decodificatori video.** In un decodificatore video tipico, il tipo di input determina in parte il tipo di output. Ad esempio, in genere entrambi i flussi devono avere la stessa frequenza dei fotogrammi e le stesse dimensioni dell'immagine. Un'opzione è definire i tipi di output preferiti solo dopo l'impostazione del tipo di input. Un'altra opzione è enumerare un set di tipi incompleti, omettendo il blocco di formato. Usare il sottotipo per indicare i tipi non compressi supportati, ad esempio RGB a 16 bit, RGB a 24 bit e così via. Inoltre, i decodificatori video in genere non supportano l'impostazione del tipo di output prima del tipo di input. Lo scenario consueto consiste nel decodificare da un formato di input noto, quindi questa limitazione è ragionevole.
-   **Decodificatori audio.** Un decodificatore audio potrebbe supportare un set limitato e fisso di formati di output. In tal caso, potrebbe essere possibile creare un elenco di formati di output preferiti prima che il formato di input sia noto.
-   **Compressori.** Nella maggior parte dei casi, un videocontenitorio non può specificare completamente i formati di output preferiti finché l'applicazione non imposta il formato di input e viceversa. Al contrario, il DMO deve restituire un tipo incompleto senza blocco di formato. Per la compressione audio e video, l'applicazione deve in genere impostare vari parametri di output, ad esempio la velocità in bit. Tuttavia, dopo aver impostato il tipo di input, il compressore deve restituire almeno un tipo di output completo, per i motivi indicati in precedenza.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scrittura di un DMO](writing-a-dmo.md)
</dt> </dl>

 

 



