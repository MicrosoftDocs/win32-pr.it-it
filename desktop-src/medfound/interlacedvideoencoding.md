---
description: Codifica video interlacciata
ms.assetid: 7695d4e3-4a75-4972-ab02-bc532d6a4dce
title: Codifica video interlacciata (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15269aca3f2878504fef56c62b1a1d70ecd89295c237164ba864b15aaae371d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119724391"
---
# <a name="interlaced-video-encoding-microsoft-media-foundation"></a>Codifica video interlacciata (Microsoft Media Foundation)

I dati video destinati all'uso con i computer sono in genere *progressivi,* vale a dire che ogni fotogramma è codificato come singola immagine. Alcuni dispositivi, come i tvi, non visualizzano una cornice contemporaneamente, ma come due immagini. Una delle immagini, o campi, contiene tutte le righe numerate pari. L'altro campo contiene i dati per tutte le righe dispari. Il video codificato con più di un campo per fotogramma viene chiamato interlacciato, perché ne viene eseguito il rendering passando dal campo pari al campo dispari.

In passato, il contenuto video interlacciato era sempre de-interlacciato prima della codifica con il codec Windows Media Video. A partire Windows Media 9 Series, tuttavia, il codificatore video supporta la compressione del contenuto interlacciato senza prima convertirlo in progressivo. La gestione dell'interlacciamento in un file codificato è importante se il rendering del contenuto viene eseguito su uno schermo interlacciato, ad esempio una tv. Questa funzionalità è di importanza crescente, poiché il supporto per Windows contenuto basato su supporti viene distribuito a lettori DVD, set-top box e altri componenti elettronici per la casa.

Il modo più semplice per codificare e distribuire video interlacciati è sviluppare l'applicazione usando Windows Media Format SDK e archiviare il contenuto in file ASF. Le informazioni interlacciate sui frame vengono passate al codec usando estensioni di unità dati, che funzionano bene per il contenuto asf, ma sono un po' più difficili da supportare in altri contenitori. Per altre informazioni sulle estensioni per unità dati, vedere [Using Data Unit Extensions](usingdataunitextensions.md).

Per supportare la codifica interlacciata sono necessari due passaggi principali: ottenere le informazioni sui frame nel codificatore e recapitare le informazioni all'applicazione per il rendering. Questi passaggi sono descritti nei paragrafi seguenti.

## <a name="interlaced-video-and-the-encoder"></a>Video interlacciato e codificatore

Il primo passaggio per codificare i video con interlacciamento mantenuto consiste nel configurare il codificatore per codificare i campi interlacciati. A tale scopo, impostare la [proprietà MFPKEY \_ INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md) su **TRUE.** In questo modo il codificatore viene preparato per la ricezione di campioni interlacciati. Ogni esempio di input deve contenere entrambi i campi.

A ogni esempio che si elabora con il codificatore dopo l'attivazione della codifica interlacciata deve essere collegata un'estensione per unità dati. Si presuppone che gli esempi senza l'estensione per unità dati prevista siano progressivi. Il GUID che identifica l'estensione è D590DC20-07BC-436C-9CF7-F3BBFBF1A4DC. I valori passati dagli oggetti di Windows Media Format SDK sono definiti nella tabella seguente.



| Valore      | Descrizione                                                                                                                              |
|------------|------------------------------------------------------------------------------------------------------------------------------------------|
| 0x00000020 | Specifica che l'esempio viene codificato prima con il campo inferiore. Questo valore è significativo solo se combinato con il valore interlacciato. |
| 0x00000040 | Specifica che l'esempio viene codificato con il primo campo. Questo valore è significativo solo se combinato con il valore interlacciato.    |
| 0x00000080 | Specifica che l'esempio è interlacciato. Questo è l'unico valore significativo per gli oggetti DMO del codec.                                    |



 

Uno dei primi due valori viene sempre combinato con 0x80 usando un **OR** bit per bit prima di essere impostato sull'esempio. Tuttavia, il codificatore controlla solo la 0x80 e ignora il resto dell'estensione. Se l'estensione identifica il campione come interlacciato, il codificatore mantiene l'interlacciamento del campione nel flusso compresso e incorpora un flag di indicazione nel flusso in modo che il decodificatore possa identificare i fotogrammi interlacciati. Ogni campione interlacciato è contrassegnato, in modo che il contenuto di origine che è una combinazione di progressivo e interlacciato possa essere codificato insieme in un flusso.

L'oggetto writer di Windows Media Format SDK include le estensioni dell'unità dati del tipo di contenuto negli esempi scritti nella sezione data del contenitore ASF per l'uso al momento del rendering.

## <a name="reading-and-rendering-interlaced-video"></a>Lettura e rendering di video interlacciati

Il decodificatore identifica i campioni interlacciati in base al flag impostato nel flusso dal codificatore. Come impostazione predefinita, il decodificatore deinterlace gli esempi e fornisce output progressivi. L'applicazione lettore può configurare il decodificatore per elaborare gli output con l'interlacciamento mantenuto impostando la proprietà [MFPKEY \_ DECODER \_ DEINTERLACING.](mfpkey-decoder-deinterlacingproperty.md)

La difficoltà nella riproduzione di video interlacciati si verifica dopo che il decodificatore ha fornito i campioni. Il renderer (scheda video o chip in un dispositivo) non può visualizzare correttamente il contenuto video senza sapere quale campo è. Nelle applicazioni che usano Windows Media Format SDK, l'estensione dell'unità dati del tipo di contenuto viene recuperata dagli esempi non compressi e può essere passata al dispositivo.

Quando si usano direttamente gli oggetti codec, nessuno di questi dati viene trasferito automaticamente. È necessario implementare il supporto di data-unit-extension, sia negli oggetti buffer che nel contenitore utilizzato per il contenuto codificato. I tipi più comuni di contenitori multimediali (ad esempio AVI) non supportano i metadati a livello di campione. È possibile implementare un sistema personalizzato per archiviare i dati nel file e associarli a singoli esempi, ma solo un lettore personalizzato sarà in grado di recuperarlo.

> [!Note]  
> Se si imposta la proprietà [MFPKEY \_ INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md) su **TRUE** e quindi non si inviano esempi con l'estensione dell'unità dati del tipo di contenuto collegata, è possibile che il codificatore si arresti in modo anomalo. Impostare il codificatore per la codifica interlacciata solo se sono disponibili campioni interlacciati da distribuire.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dei video](workingwithvideo.md)
</dt> </dl>

 

 



