---
description: Video su YUV
ms.assetid: 089f42f2-1e5b-4d4b-98a4-9ef0ca2823c1
title: Video su YUV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b57b4a453870af34c221683bdaf613b5038081d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526011"
---
# <a name="about-yuv-video"></a>Video su YUV

Il video digitale è spesso codificato in formato *YUV* . Questo articolo illustra i concetti generali di video YUV, oltre a una terminologia, senza approfondire la matematica dell'elaborazione di video YUV.

Se si è lavorato con la grafica del computer, probabilmente si ha familiarità con il colore RGB. Un colore RGB viene codificato utilizzando tre valori: rosso, verde e blu. Questi valori corrispondono direttamente alle parti dello spettro visibile. I tre valori RGB formano un sistema di coordinate matematiche, denominato *spazio colore*. Il componente rosso definisce un asse del sistema di coordinate, il blu definisce il secondo e il verde definisce il terzo, come illustrato nella figura seguente. Qualsiasi colore RGB valido cade in un punto qualsiasi all'interno di questo spazio colore. Ad esempio, il magenta pure è 100% Blue, 100% Red e 0% verde.

![diagramma che mostra lo spazio colore RGB](images/8ec60365-ed5c-41f7-9da9-be46aa82896a.gif)

Sebbene RGB sia un modo comune per rappresentare i colori, sono possibili altri sistemi di coordinate. Il termine *YUV* fa riferimento a una famiglia di spazi dei colori, che codificano le informazioni sulla luminosità separatamente dalle informazioni sui colori. Come RGB, YUV usa tre valori per rappresentare qualsiasi colore. Questi valori sono definiti Y, U e V. l'uso del termine "YUV", infatti, è tecnicamente non accurato. Nel computer video il termine YUV si riferisce quasi sempre a un particolare spazio dei colori denominato CbCr, illustrato più avanti. Tuttavia, YUV viene spesso usato come termine generale per qualsiasi spazio di colore che funziona con gli stessi principi di CbCr.

Il componente Y, denominato anche *Luma*, rappresenta il valore di luminosità del colore. Il simbolo principale (') viene usato per distinguere la Luma da un valore strettamente correlato, *luminanza*, che è designato come Y. luminanza deriva da valori RGB *lineari* , mentre Luma deriva da valori RGB *non lineari* (con correzione a gamma). La luminanza è una misura più stretta della luminosità reale, ma la luminanza è più pratica da usare per motivi tecnici. Il simbolo principale viene spesso omesso, ma gli spazi dei colori YUV utilizzano sempre luma, non la luminanza.

Luma deriva da un colore RGB prendendo una media ponderata dei componenti rosso, verde e blu. Per la televisione con definizione standard, viene utilizzata la formula seguente:

`Y' = 0.299R + 0.587G + 0.114B`

Questa formula riflette il fatto che l'occhio umano è più sensibile a determinate lunghezze di luce rispetto ad altre, che influiscono sulla luminosità percepita di un colore. La luce blu appare in grigio, il verde appare più chiaro e il rosso è in un punto compreso tra. Questa formula riflette anche le caratteristiche fisiche dei fosfor usati nei primi televisori. Una formula più recente, prendendo in considerazione la moderna tecnologia per la televisione, viene usata per la televisione ad alta definizione:

`Y' = 0.2125R + 0.7154G + 0.0721B`

L'equazione Luma per la televisione con definizione standard è definita in una specifica denominata ITU-R BT. 601. Per la televisione ad alta definizione, la specifica pertinente è ITU-R BT. 709.

I componenti utente e V, denominati anche valori *cromatici* o valori di *differenza colore* , vengono derivati sottraendo il valore Y dai componenti rosso e blu del colore RGB originale:

`U = B - Y'`

`V = R - Y'`

Insieme, questi valori contengono informazioni sufficienti per recuperare il valore RGB originale.

## <a name="benefits-of-yuv"></a>Vantaggi di YUV

La televisione analoga USA YUV in parte per motivi cronologici. I segnali televisivi analoghi sono stati progettati per essere compatibili con le versioni precedenti con la televisione nera e bianca. Il segnale della televisione dei colori contiene le informazioni sul Chroma (u e V) sovrapposte al segnale luma. I televisori neri e bianchi ignorano il Chroma e visualizzano il segnale combinato come immagine in scala di grigi. Il segnale è progettato in modo che il Chroma non interferisca significativamente con il segnale luma. I televisore a colori possono estrarre il Chroma e riconvertire il segnale in RGB.

YUV offre un altro vantaggio più rilevante oggi. L'occhio umano è meno sensibile alle modifiche di Hue rispetto alle modifiche della luminosità. Di conseguenza, un'immagine può avere meno informazioni sulla crominanza rispetto alle informazioni Luma senza sacrificare la qualità percepita dell'immagine. Ad esempio, è comune campionare i valori Chroma a metà della risoluzione orizzontale degli esempi Luma. In altre parole, per ogni due campioni luma in una riga di pixel, è presente un campione U e un campione V. Supponendo che vengano usati 8 bit per codificare ogni valore, sono necessari un totale di 4 byte per ogni due pixel (due Y, uno U e uno V), per una media di 16 bit per pixel o il 30% inferiore rispetto alla codifica RGB equivalente a 24 bit.

YUV non è intrinsecamente più compatto di RGB. A meno che la croma non sia downsampling, un pixel YUV ha le stesse dimensioni di un pixel RGB. Inoltre, la conversione da RGB a YUV non è una perdita di perdite. Se non è presente alcun sottocampionando, un pixel YUV può essere convertito di nuovo in RGB senza perdita di informazioni. Sottocampionando rende un'immagine YUV più piccola e perde anche alcune informazioni sul colore. Se viene eseguita correttamente, tuttavia, la perdita non è percettivamente significativa.

## <a name="yuv-in-computer-video"></a>YUV nel video del computer

Le formule elencate in precedenza per YUV non sono le conversioni esatte usate nei video digitali. Il video digitale usa in genere una forma di YUV denominata CbCr. Essenzialmente, CbCr funziona scalando i componenti YUV agli intervalli seguenti:



| Componente | Range                              |
|-----------|------------------------------------|
| Y        | 16 – 235                             |
| CB/CR     | 16-240, con 128 che rappresenta zero |



 

Questi intervalli presuppongono 8 bit di precisione per i componenti CbCr. Di seguito è illustrata l'esatta derivazione di CbCr, con la definizione di Luma BT. 601:

1.  Iniziare con i valori RGB nell'intervallo \[ 0... 1 \] . In altre parole, il nero puro è 0 e il bianco puro è 1. In particolare, si tratta di valori RGB non lineari (con correzione gamma).
2.  Calcolo della luminanza. Per BT. 601, Y ' = 0.299 R + 0.587 G + 0.114 B, come descritto in precedenza.
3.  Calcolare i valori di differenza croma intermedia (B-Y ') e (R-Y '). Questi valori hanno un intervallo di +/-0,886 per (B-Y ') e +/-0,701 per (R-Y ').
4.  Ridimensionare i valori di differenza croma come indicato di seguito:

    PB = (0,5/(1-0,114)) × (B-Y ')

    PR = (0,5/(1-0,299)) × (R-Y ')

    Questi fattori di scala sono progettati per assegnare a entrambi i valori lo stesso intervallo numerico, +/-0,5. Insieme definiscono uno spazio di colore YUV denominato Y'PbPr. Questo spazio di colore viene usato nel video dei componenti analoghi.

5.  Ridimensionare i valori di Y'PbPr per ottenere i valori CbCr finali:

    Y ' = 16 + 219 × Y '

    CB = 128 + 224 × PB

    CR = 128 + 224 × PR

Questi ultimi fattori di scalabilità generano l'intervallo di valori elencati nella tabella precedente. Naturalmente, è possibile convertire RGB direttamente in CbCr senza archiviare i risultati intermedi. I passaggi sono elencati separatamente qui per illustrare il modo in cui CbCr deriva dalle equazioni YUV originali fornite all'inizio di questo articolo.

La tabella seguente mostra i valori RGB e YCbCr per vari colori, usando di nuovo la definizione BT. 601 di Luma.



| Colore   | R   | G   | B   | Y  | CB  | Cr  |
|---------|-----|-----|-----|-----|-----|-----|
| Black   | 0   | 0   | 0   | 16  | 128 | 128 |
| Red     | 255 | 0   | 0   | 81  | 90  | 240 |
| Green   | 0   | 255 | 0   | 145 | 54  | 34  |
| Blu    | 0   | 0   | 255 | 41  | 240 | 110 |
| azzurro    | 0   | 255 | 255 | 170 | 166 | 16  |
| Fucsia | 255 | 0   | 255 | 106 | 202 | 222 |
| Giallo  | 255 | 255 | 0   | 210 | 16  | 146 |
| White   | 255 | 255 | 255 | 235 | 128 | 128 |



 

Come illustrato nella tabella, CB e CR non corrispondono a idee intuitive sui colori. Ad esempio, pure bianco e puro nero contengono entrambi livelli neutri di CB e CR (128). I valori massimo e minimo per CB sono rispettivamente blu e giallo. Per CR, i valori massimo e minimo sono Red e cyan.

## <a name="for-more-information"></a>Ulteriori informazioni

-   [Formati YUV a 8 bit consigliati per il rendering video](recommended-8-bit-yuv-formats-for-video-rendering.md)
-   Keith Jack. Video demistificato, quinta edizione. Newnes, 2007.
-   Carlo A. Poynton. Introduzione tecnica ai video digitali. Wiley, 1996.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di supporti video](video-media-types.md)
</dt> <dt>

[Tipi di supporto](media-types.md)
</dt> </dl>

 

 



