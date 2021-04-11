---
title: Ottenere risultati soddisfacenti con il codec della schermata Windows Media Video 9
description: Ottenere risultati soddisfacenti con il codec della schermata Windows Media Video 9
ms.assetid: c5b080d3-2934-4af7-8f01-9ab0829db05d
keywords:
- Windows Media Format SDK, Windows Media Video 9 codec dello schermo
- Formato Advanced Systems Format (ASF), Windows Media Video 9 screen codec
- ASF (Advanced Systems Format), Windows Media Video 9 codec dello schermo
- codec, schermata Windows Media Video 9
- Windows Media Video 9 codec dello schermo, risultati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a297638c7c50a6380fd4c43ea1d4b9971d44db5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103956206"
---
# <a name="getting-good-results-with-the-windows-media-video-9-screen-codec"></a>Ottenere risultati soddisfacenti con il codec della schermata Windows Media Video 9

Il codec Windows Media Video 9 screen è progettato per produrre video altamente compressi per l'acquisizione schermo. Poiché la maggior parte delle esigenze di acquisizione schermo implica immagini piuttosto semplici e statiche, i livelli elevati di compressione ottenuti non implicano in genere un grande sacrificio nella qualità dell'immagine. Tuttavia, ogni acquisizione della schermata è diversa e la qualità dell'immagine risultante può variare notevolmente in base alle circostanze.

Il modo migliore per determinare le impostazioni del profilo per una sessione di codec della schermata consiste nel codificare un file di test usando un flusso di velocità in bit variabile basato sulla qualità. Impostare la qualità sul valore desiderato e codificare un'acquisizione schermo come se si stesse registrando il file finale. Quando il file viene scritto, viene riprodotto utilizzando l'oggetto Reader asincrono, effettuando chiamate regolari a [**IWMReaderAdvanced:: GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics). Monitorando il valore del membro **dwBandwidth** della struttura delle [**\_ \_ statistiche di WM Reader**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics) per ogni chiamata, è possibile determinare la velocità in bit approssimativa necessaria per ottenere la qualità desiderata. È quindi possibile usare tale velocità in bit per la codifica della velocità in bit costante.

Se si rileva che la qualità desiderata richiede una velocità in bit superiore a quella che è possibile usare per lo scenario di distribuzione, è possibile provare le tecniche seguenti per ottenere maggiore efficienza dal codec.

-   Usare una risoluzione più piccola per l'acquisizione dello schermo. L'acquisizione di una risoluzione dello schermo maggiore di quella necessaria può anche creare confusione per il Visualizzatore presentando più informazioni del necessario.
-   Usare un minor numero di elementi grafici nell'acquisizione schermo. Il codec Windows Media Video 9 screen è ottimizzato per codificare primitive e testo di Windows con qualità elevata. In genere si verificano problemi a causa di immagini bitmap, che spesso contengono migliaia di colori singoli. Il minor numero di bitmap visualizzate sullo schermo quando si acquisisce, migliore sarà il risultato. Se non è possibile eliminare grafica dall'acquisizione schermo, esistono diversi modi per ridurre al minimo l'effetto di una bitmap sulla qualità dell'immagine:
    -   Ridurre le dimensioni dell'elemento grafico.
    -   Ridurre il numero di singoli elementi grafici visualizzati contemporaneamente sullo schermo.
    -   Ridurre la quantità di movimento del grafico. Se, ad esempio, l'immagine si trova in una finestra, conservarla nel modo più stazionale possibile.
    -   Evitare di spostare il puntatore del mouse sul grafico o di trascinare finestre o altri elementi sul grafico.
-   Usare una frequenza di [*fotogrammi*](wmformat-glossary.md)più lenta. Le acquisizioni di schermate possono spesso essere efficaci a frequenze di frame molto ridotte (a volte con un minimo di 4 o 5 fotogrammi al secondo).
-   Ridurre la velocità in bit dell'audio associato.

Inoltre, il codec non supporta il ridimensionamento del rettangolo video. In altre parole, se si tenta di usare il codec per codificare una schermata 800 x 600 fino a un rettangolo video 640 x 480, il video risultante avrà artefatti significativi che potrebbero rendere illeggibili gran parte del testo sullo schermo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Configurazione di flussi di acquisizione schermo**](configuring-screen-capture-streams.md)
</dt> <dt>

[**Configurazione di flussi**](configuring-streams.md)
</dt> </dl>

 

 




