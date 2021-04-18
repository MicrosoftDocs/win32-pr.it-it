---
description: Uso del codec della schermata Windows Media Video 9
ms.assetid: d88d5f5e-0935-4bbe-8abf-72cc536f9b40
title: Uso del codec Windows Media Video 9 screen (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b825e053c4c732481c8d1ca5d4dc972f804f262a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320457"
---
# <a name="using-the-windows-media-video-9-screen-codec-microsoft-media-foundation"></a>Uso del codec Windows Media Video 9 screen (Microsoft Media Foundation)

Il codec Windows Media Video 9 screen è ottimizzato per comprimere il *video dell'applicazione*, che è costituito da screenshot consecutivi per lo schermo di un computer. Il codec sfrutta la semplicità tipica delle immagini (relativamente pochi colori, molte linee rette e così via) e la mancanza di movimento relativa per ottenere un rapporto di compressione molto elevato. Lo svantaggio di questa ottimizzazione è che il video non conforme alle caratteristiche previste del video dell'applicazione può essere difficile da comprimere con un livello di qualità accettabile.

Il codificatore di schermata Windows Media Video 9 è identificato dall'identificatore di classe CLSID \_ CMSSEncMediaObject2 e il decodificatore è identificato dall'identificatore di classe CLSID \_ CMSSDecMediaObject. Il valore di FOURCC per i tipi di supporto che usano questo codec è "MSS2".

## <a name="configuring-the-encoder"></a>Configurazione del codificatore

Il codificatore del codec Windows Media Video 9 screen viene configurato esattamente come il decoder video standard.

> [!Note]  
> Il codificatore dello schermo supporta solo la codifica con un solo passaggio. È possibile impostare la proprietà [MFPKEY \_ PASSESUSED](mfpkey-passesusedproperty.md) su 2 ed elaborare gli input due volte senza errori, ma non vi è alcun vantaggio. Si tratta di un problema noto che può essere corretto nelle versioni future.

 

## <a name="getting-the-best-results"></a>Ottenere risultati ottimali

Se si scopre che la qualità desiderata nel contenuto di acquisizione schermo richiede una velocità in bit superiore rispetto a quella che è possibile usare per lo scenario di distribuzione, è possibile provare le tecniche seguenti per ottenere maggiore efficienza dal codec:

-   Usare una risoluzione più piccola per l'acquisizione dello schermo. L'acquisizione di una risoluzione dello schermo superiore a quella necessaria può confondere il Visualizzatore presentando informazioni non necessarie.
-   Usare una frequenza di fotogrammi più lenta. Le acquisizioni di schermate possono spesso essere efficaci a frequenze di frame molto ridotte (a volte con un minimo di 4 o 5 fotogrammi al secondo).
-   Usare un minor numero di elementi grafici nell'acquisizione schermo. Il codec Windows Media Video 9 screen è ottimizzato per codificare primitive e testo di Windows con qualità elevata. In genere si verificano problemi a causa di immagini bitmap, che spesso contengono migliaia di colori singoli. Il minor numero di bitmap visualizzate sullo schermo quando si acquisisce, migliore sarà il risultato. Se non è possibile eliminare grafica dall'acquisizione schermo, esistono diversi modi per ridurre al minimo l'effetto di una bitmap sulla qualità dell'immagine:
    -   Ridurre le dimensioni dell'elemento grafico.
    -   Ridurre il numero di singoli elementi grafici visualizzati sullo schermo nello stesso momento.
    -   Ridurre la quantità di movimento del grafico. Se, ad esempio, l'immagine si trova in una finestra, conservarla nel modo più stazionale possibile.
    -   Evitare di spostare il puntatore del mouse sul grafico o di trascinare finestre o altri elementi sul grafico.

## <a name="decoding"></a>Decodifica

Non sono previsti requisiti speciali per la decodifica del video di acquisizione schermo. Tuttavia, come con tutti i Windows Media Video 9 codec, il decodificatore di acquisizione schermo non può decomprimere correttamente il contenuto codificato senza i dati privati del codec.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione della codifica video](configuringvideoencoding.md)
</dt> <dt>

[Uso di dati privati del codec video](usingvideocodecprivatedata.md)
</dt> <dt>

[Codificatore dello schermo Windows Media Video 9](windowsmediavideo9screenencoder.md)
</dt> <dt>

[Uso dei video](workingwithvideo.md)
</dt> </dl>

 

 



