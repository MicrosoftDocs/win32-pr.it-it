---
title: Ottenere buoni risultati con il codec dello schermo Windows Media Video 9
description: Ottenere buoni risultati con il codec dello schermo Windows Media Video 9
ms.assetid: c5b080d3-2934-4af7-8f01-9ab0829db05d
keywords:
- Windows Media Format SDK,Windows codec dello schermo Media Video 9
- Advanced Systems Format (ASF), Windows codec dello schermo Video multimediale 9
- ASF (Advanced Systems Format), Windows codec dello schermo Video multimediale 9
- codec, Windows Video multimediale 9
- Windows Codec dello schermo Media Video 9,risultati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657cde745f6bfbabe00fe123b493e2eae2afb20ddf40206f781822770a4386f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110431"
---
# <a name="getting-good-results-with-the-windows-media-video-9-screen-codec"></a>Ottenere buoni risultati con il codec dello schermo Windows Media Video 9

Il codec Windows media video 9 è progettato per produrre video altamente compresso per l'acquisizione dello schermo. Poiché la maggior parte delle necessità di acquisizione dello schermo prevede immagini piuttosto semplici e statiche, gli elevati livelli di compressione ottenuta non comportano in genere un grande sacrificio nella qualità delle immagini. Tuttavia, ogni acquisizione dello schermo è diversa e la qualità dell'immagine risultante può variare notevolmente a seconda delle circostanze.

Il modo migliore per determinare le impostazioni del profilo per una sessione di codec dello schermo è codificare un file di test usando un flusso di velocità in bit variabile basato sulla qualità. Impostare la qualità sul valore desiderato e codificare un'acquisizione schermo come se si registrava il file finale. Quando il file viene scritto, riprodurlo usando l'oggetto lettore asincrono, effettuando chiamate regolari a [**IWMReaderAdvanced::GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics). Monitorando il valore del membro **dwBandwidth** della struttura [**WM READER \_ \_ STATISTICS**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics) per ogni chiamata, è possibile determinare la velocità in bit approssimativa necessaria per ottenere la qualità desiderata. È quindi possibile usare tale velocità in bit per la codifica a velocità in bit costante.

Se si scopre che la qualità desiderata richiede una velocità in bit più elevata rispetto a quella che è possibile usare per lo scenario di distribuzione, è possibile provare le tecniche seguenti per ottenere maggiore efficienza dal codec.

-   Usare una risoluzione più piccola per l'acquisizione dello schermo. L'acquisizione di una risoluzione dello schermo più grande del necessario può anche creare confusione per il visualizzatore presentando più informazioni di quelle necessarie.
-   Usare un minor numero di elementi grafici nell'acquisizione dello schermo. Il codec Windows Media Video 9 Screen è ottimizzato per codificare Windows primitive e testo con alta qualità. In genere si verificano problemi a causa della grafica bitmap, che spesso contiene migliaia di singoli colori. Minore è il numero di bitmap visualizzate sullo schermo durante l'acquisizione, migliori saranno i risultati. Se non è possibile eliminare la grafica dall'acquisizione dello schermo, esistono diversi modi per ridurre al minimo l'impatto di una bitmap sulla qualità dell'immagine:
    -   Ridurre le dimensioni dell'immagine.
    -   Ridurre il numero di singoli elementi grafici visualizzati contemporaneamente sullo schermo.
    -   Ridurre la quantità di movimento dell'immagine. Ad esempio, se l'elemento grafico si trova in una finestra, mantenere la finestra il più stazionaria possibile.
    -   Evitare di spostare il puntatore del mouse sull'elemento grafico o di trascinare finestre o altri elementi sull'elemento grafico.
-   Usare una frequenza [*fotogrammi più lenta.*](wmformat-glossary.md) Le acquisizioni dello schermo possono spesso essere efficaci a frequenze di fotogrammi molto basse (talvolta fino a 4 o 5 fotogrammi al secondo).
-   Ridurre la velocità in bit dell'audio che lo accompagna.

Inoltre, il codec non supporta il ridimensionamento del rettangolo video. In altre parole, se si prova a usare il codec per codificare uno schermo 800 x 600 verso il basso in un rettangolo video 640 x 480, il video risultante avrà artefatti significativi che potrebbero rendere illeggibile gran parte del testo sullo schermo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Configurazione dell'acquisizione schermo Flussi**](configuring-screen-capture-streams.md)
</dt> <dt>

[**Configurazione di Flussi**](configuring-streams.md)
</dt> </dl>

 

 




