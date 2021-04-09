---
description: Codifica video interlacciata
ms.assetid: 7695d4e3-4a75-4972-ab02-bc532d6a4dce
title: Codifica video interlacciata (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fafacb56f29964e81b040c59cdb75d8ebb35830b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968342"
---
# <a name="interlaced-video-encoding-microsoft-media-foundation"></a>Codifica video interlacciata (Microsoft Media Foundation)

I dati video destinati all'uso con i computer sono in genere *progressivi*, vale a dire che ogni frame è codificato come una singola immagine. Alcuni dispositivi, come le televisioni, non visualizzano un frame in una sola volta, ma come due immagini. Una delle immagini, o campi, contiene tutte le righe numerate pari. L'altro campo contiene i dati per tutte le righe dispari. Il video codificato con più di un campo per frame viene chiamato interlacciato, perché viene sottoposto a rendering passando tra il campo even e il campo dispari.

In passato, il contenuto video interlacciato veniva sempre deinterlacciato prima della codifica con il codec Windows Media Video. A partire da Windows Media 9 Series, tuttavia, il codificatore video supporta la compressione di contenuto interlacciato senza prima convertirlo in progressivo. La gestione dell'interlacciamento in un file codificato è importante se il rendering del contenuto viene eseguito su una visualizzazione interlacciata, ad esempio un televisore. Questa funzionalità è sempre più importante, in quanto il supporto per le distribuzioni di contenuto basato su Windows Media in lettori DVD, set-top box e altri componenti elettronici domestici.

Il modo più semplice per codificare e distribuire video interlacciato consiste nello sviluppare l'applicazione usando Windows Media Format SDK e archiviando il contenuto nei file ASF. Le informazioni interlacciate sui frame vengono passate al codec usando le estensioni dell'unità dati, che funzionano bene per il contenuto ASF, ma sono leggermente più complicate per il supporto in altri contenitori. Per ulteriori informazioni sulle estensioni dell'unità dati, vedere [Using Data Unit Extensions](usingdataunitextensions.md).

Per supportare la codifica interlacciata è necessario eseguire due passaggi principali: ottenere le informazioni sul frame nel codificatore e recapitano le informazioni all'applicazione di rendering. Questi passaggi sono descritti nei paragrafi seguenti.

## <a name="interlaced-video-and-the-encoder"></a>Video interlacciato e codificatore

Il primo passaggio nella codifica del video con l'interlacciamento mantenuto consiste nel configurare il codificatore per codificare i campi interlacciati. A tale scopo, impostare la proprietà [MFPKEY \_ INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md) su **true**. In questo modo si prepara il codificatore a ricevere esempi interlacciati. Ogni esempio di input deve contenere entrambi i campi.

Ogni esempio elaborato con il codificatore dopo l'attivazione della codifica interlacciata deve avere un'estensione di unità dati collegata. Si presuppone che gli esempi senza l'estensione dell'unità dati prevista siano progressivi. Il GUID che identifica l'estensione è D590DC20-07BC-436C-9CF7-F3BBFBF1A4DC. I valori passati dagli oggetti di Windows Media Format SDK sono definiti nella tabella seguente.



| Valore      | Descrizione                                                                                                                              |
|------------|------------------------------------------------------------------------------------------------------------------------------------------|
| 0x00000020 | Specifica che l'esempio è codificato prima con il campo inferiore. Questo valore è significativo solo se combinato con il valore interlacciato. |
| 0x00000040 | Specifica che l'esempio è codificato prima con il campo superiore. Questo valore è significativo solo se combinato con il valore interlacciato.    |
| 0x00000080 | Specifica che l'esempio è interlacciato. Si tratta dell'unico valore significativo per il codec DMOs.                                    |



 

Uno dei primi due valori viene sempre combinato con 0x80 utilizzando **un operatore OR** bit per bit prima di essere impostato nell'esempio. Tuttavia, il codificatore controlla solo 0x80 e ignora il resto dell'estensione. Se l'estensione identifica l'esempio come interlacciato, il codificatore gestisce l'interlacciamento di esempio nel flusso compresso e incorpora un flag di indicazione nel flusso, in modo che il decodificatore possa identificare i frame interlacciati. Ogni campione interlacciato è contrassegnato, in modo che il contenuto di origine costituito da una combinazione di progressivo e interlacciato possa essere codificato in un flusso insieme.

L'oggetto writer di Windows Media Format SDK include le estensioni dell'unità dati del tipo di contenuto negli esempi che scrive nella sezione dati del contenitore ASF da usare al momento del rendering.

## <a name="reading-and-rendering-interlaced-video"></a>Lettura e rendering di video interlacciati

Il decodificatore identifica gli esempi interlacciati in base al flag impostato nel flusso dal codificatore. Come impostazione predefinita, il decodificatore Deinterlaccia gli esempi e recapita output progressivi. L'applicazione Player può configurare il decodificatore per elaborare gli output con interlacciamento gestito impostando la proprietà [ \_ \_ deinterlacciamento del decodificatore MFPKEY](mfpkey-decoder-deinterlacingproperty.md) .

La difficoltà nella riproduzione video interlacciata si verifica dopo che il decodificatore fornisce gli esempi. Il renderer (scheda video o chip in un dispositivo) non è in grado di visualizzare correttamente il contenuto del video senza conoscere il campo. Nelle applicazioni che usano Windows Media Format SDK, l'estensione dell'unità dati del tipo di contenuto viene recuperata dagli esempi non compressi e può essere passata al dispositivo.

Quando si usano direttamente gli oggetti codec, nessuno di questi trasferimenti di dati è automatico. È necessario implementare il supporto dell'estensione dell'unità dati, sia negli oggetti buffer che nel contenitore usato per il contenuto codificato. I tipi più comuni di contenitori multimediali (ad esempio AVI) non supportano i metadati a livello di esempio. È possibile implementare il proprio sistema per archiviare i dati nel file e associarli a singoli esempi, ma solo un lettore personalizzato può recuperarlo.

> [!Note]  
> Impostando la proprietà [MFPKEY \_ INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md) su **true** e non inviando alcun campione con l'estensione dell'unità dati Content-Type collegata, il codificatore potrebbe arrestarsi in modo anomalo. Impostare il codificatore per la codifica interlacciata solo se sono presenti esempi interlacciati per il recapito.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dei video](workingwithvideo.md)
</dt> </dl>

 

 



