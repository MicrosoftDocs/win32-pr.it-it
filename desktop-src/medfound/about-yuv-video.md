---
description: Informazioni su YUV Video
ms.assetid: 089f42f2-1e5b-4d4b-98a4-9ef0ca2823c1
title: Informazioni su YUV Video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3499a8adfe1a43a22fe9bdd9ff4e576b7a14c398a9dafc0b945647d7225ad581
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118744245"
---
# <a name="about-yuv-video"></a>Informazioni su YUV Video

I video digitali vengono spesso codificati in *formato YUV.* Questo articolo illustra i concetti generali del video YUV, insieme ad alcuni termini, senza entrare in profondità nella matematica dell'elaborazione video YUV.

Se si è lavorato con la grafica computer, probabilmente si ha familiarità con il colore RGB. Un colore RGB viene codificato usando tre valori: rosso, verde e blu. Questi valori corrispondono direttamente alle parti dello spettro visibile. I tre valori RGB formano un sistema di coordinate matematico, denominato *spazio colore*. Il componente rosso definisce un asse di questo sistema di coordinate, il blu definisce il secondo e il verde definisce il terzo, come illustrato nella figura seguente. Qualsiasi colore RGB valido rientra in un punto qualsiasi all'interno di questo spazio colore. Ad esempio, magenta puro è 100% blu, 100% rosso e 0% verde.

![diagramma che mostra lo spazio colore rgb](images/8ec60365-ed5c-41f7-9da9-be46aa82896a.gif)

Anche se RGB è un modo comune per rappresentare i colori, sono possibili altri sistemi di coordinate. Il termine *YUV si* riferisce a una famiglia di spazi colori, tutti i quali codificano le informazioni sulla luminosità separatamente dalle informazioni sui colori. Come RGB, YUV usa tre valori per rappresentare qualsiasi colore. Questi valori sono D', U e V. (in realtà, questo uso del termine "YUV" è tecnicamente impreciso. Nel video per computer, il termine YUV si riferisce quasi sempre a uno spazio colore specifico denominato Y'CbCr, descritto più avanti. Tuttavia, YUV viene spesso usato come termine generale per qualsiasi spazio colore che funziona in base ai principi di Y'CbCr.

Il componente Y,detto anche *luma,* rappresenta il valore di luminosità del colore. Il simbolo primo (') viene usato per distinguere luma da un valore strettamente correlato, *luminance*, definito Y. Luminance è derivato da valori *RGB* lineari, mentre luma è derivato da valori RGB *non* lineari (con correzione gamma). Luminance è una misura più vicina della luminosità reale, ma luma è più pratico da usare per motivi tecnici. Il simbolo primo viene spesso omesso, ma gli spazi colori YUV usano sempre luma, non la luminance.

Luma deriva da un colore RGB prendendo una media ponderata dei componenti rosso, verde e blu. Per la tv con definizione standard, viene usata la formula seguente:

`Y' = 0.299R + 0.587G + 0.114B`

Questa formula riflette il fatto che l'occhio umano è più sensibile a determinate lunghezze d'onda della luce rispetto ad altre, che influisce sulla luminosità percepita di un colore. La luce blu appare in grigio, il verde appare più chiaro e il rosso è in mezzo. Questa formula riflette anche le caratteristiche fisiche dei phosphor usati nelle prime tv. Una formula più recente, che prende in considerazione la moderna tecnologia tv, viene usata per la tv ad alta definizione:

`Y' = 0.2125R + 0.7154G + 0.0721B`

L'equazione luma per la tv con definizione standard è definita in una specifica denominata ITU-R BT.601. Per la tv ad alta definizione, la specifica pertinente è ITU-R BT.709.

I componenti you e V, detti  anche valori *chroma* o valori di differenza di colore, derivano sottraendo il valore Y dai componenti rosso e blu del colore RGB originale:

`U = B - Y'`

`V = R - Y'`

Insieme, questi valori contengono informazioni sufficienti per recuperare il valore RGB originale.

## <a name="benefits-of-yuv"></a>Vantaggi di YUV

La tv analoga usa YUV in parte per motivi cronologici. I segnali tv a colori analogici sono stati progettati per essere compatibili con le versioni precedenti dei tv in bianco e nero. Il segnale della tv a colori trasporta le informazioni sulla chroma (tu e V) sovrapposte al segnale luma. I tvi in bianco e nero ignorano la chroma e visualizzano il segnale combinato come immagine in scala di grigi. Il segnale è progettato in modo che la chroma non interferisca in modo significativo con il segnale luma. I tvi di colore possono estrarre la chroma e riconvertire il segnale in RGB.

YUV ha un altro vantaggio che è più rilevante al giorno d'oggi. L'occhio umano è meno sensibile ai cambiamenti di tonalità rispetto ai cambiamenti di luminosità. Di conseguenza, un'immagine può avere meno informazioni sulla croma rispetto alle informazioni di luma senza compromettere la qualità percepita dell'immagine. Ad esempio, è comune campionare i valori chroma a metà della risoluzione orizzontale dei campioni di luma. In altre parole, per ogni due campioni di luma in una riga di pixel, sono presenti un campione U e un campione V. Supponendo che vengono usati 8 bit per codificare ogni valore, sono necessari un totale di 4 byte per ogni due pixel (due Y', un U e un V), per una media di 16 bit per pixel o il 30% in meno rispetto alla codifica RGB a 24 bit equivalente.

YUV non è intrinsecamente più compatto di RGB. A meno che la chroma non venga sottocampionata, un pixel YUV ha le stesse dimensioni di un pixel RGB. Inoltre, la conversione da RGB a YUV non è una perdita. Se non è presente alcun sottocampionamento, un pixel YUV può essere convertito nuovamente in RGB senza perdita di informazioni. Il sottocampionamento rende più piccola un'immagine YUV e perde anche alcune informazioni sul colore. Se eseguita correttamente, tuttavia, la perdita non è percettivamente significativa.

## <a name="yuv-in-computer-video"></a>YUV in Computer Video

Le formule elencate in precedenza per YUV non sono le conversioni esatte usate nel video digitale. Il video digitale usa in genere una forma di YUV denominata Y'CbCr. In sostanza, Y'CbCr opera ridimensionando i componenti YUV agli intervalli seguenti:



| Componente | Intervallo                              |
|-----------|------------------------------------|
| Y'        | 16–235                             |
| Cb/Cr     | 16-240, con 128 che rappresenta zero |



 

Questi intervalli presuppongono 8 bit di precisione per i componenti Y'CbCr. Ecco la derivazione esatta di Y'CbCr, usando la definizione BT.601 di luma:

1.  Iniziare con valori RGB nell'intervallo \[ 0...1 \] . In altre parole, il nero puro è 0 e il bianco puro è 1. È importante notare che si tratta di valori RGB non lineari (con correzione gamma).
2.  Calcolare luma. Per BT.601, Y' = 0,299R + 0,587G + 0,114B, come descritto in precedenza.
3.  Calcolare i valori intermedi della differenza della croma (B - Y') e (R - Y'). Questi valori hanno un intervallo di +/- 0,886 per (B - Y') e +/- 0,701 per (R - Y').
4.  Ridimensionare i valori delle differenze di croma come indicato di seguito:

    Pb = (0,5 / (1 - 0,114)) × (B - Y')

    Pr = (0,5 / (1 - 0,299)) × (R - Y')

    Questi fattori di scala sono progettati per assegnare a entrambi i valori lo stesso intervallo numerico, +/- 0,5. Insieme, definiscono uno spazio colori YUV denominato Y'PbPr. Questo spazio colore viene usato nel video con componente analogico.

5.  Ridimensionare i valori Y'PbPr per ottenere i valori Y'CbCr finali:

    Y' = 16 + 219 × Y'

    Cb = 128 + 224 × Pb

    Cr = 128 + 224 × Pr

Questi ultimi fattori di scala producono l'intervallo di valori elencati nella tabella precedente. Naturalmente, è possibile convertire RGB direttamente in Y'CbCr senza archiviare i risultati intermedi. I passaggi sono elencati separatamente qui per illustrare in che modo Y'CbCr deriva dalle equazioni YUV originali fornite all'inizio di questo articolo.

La tabella seguente mostra i valori RGB e YCbCr per diversi colori, usando di nuovo la definizione BT.601 di luma.



| Color   | R   | G   | B   | Y'  | Cb  | Cr  |
|---------|-----|-----|-----|-----|-----|-----|
| Black   | 0   | 0   | 0   | 16  | 128 | 128 |
| Red     | 255 | 0   | 0   | 81  | 90  | 240 |
| Green   | 0   | 255 | 0   | 145 | 54  | 34  |
| Blu    | 0   | 0   | 255 | 41  | 240 | 110 |
| azzurro    | 0   | 255 | 255 | 170 | 166 | 16  |
| Fucsia | 255 | 0   | 255 | 106 | 202 | 222 |
| Giallo  | 255 | 255 | 0   | 210 | 16  | 146 |
| White   | 255 | 255 | 255 | 235 | 128 | 128 |



 

Come illustrato in questa tabella, Cb e Cr non corrispondono a idee intuitive sul colore. Ad esempio, il bianco puro e il nero puro contengono entrambi livelli neutri di Cb e Cr (128). I valori più alti e più bassi per Cb sono rispettivamente blu e giallo. Per Cr, i valori più alti e più bassi sono rosso e ciano.

## <a name="for-more-information"></a>Ulteriori informazioni

-   [Formati YUV a 8 bit consigliati per il rendering video](recommended-8-bit-yuv-formats-for-video-rendering.md)
-   Jack Jack. Video Demystified, Quinta edizione. Newnes, 2007.
-   Charles A. Poy pop. Introduzione tecnica al video digitale. Wiley, 1996.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di file multimediali video](video-media-types.md)
</dt> <dt>

[Tipi di supporti](media-types.md)
</dt> </dl>

 

 



