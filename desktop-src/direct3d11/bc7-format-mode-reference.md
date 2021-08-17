---
title: Informazioni di riferimento sulla modalità formato BC7
description: Questa documentazione contiene un elenco delle modalità a 8 blocchi e delle allocazioni di bit per i blocchi di formato di compressione trame BC7.
ms.assetid: B1CEB729-6694-49BF-ACB9-FD1EFAB0B0D1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f96bfd9c90697b47587048684239ecf084dd43a76e0ef76b9717fe09d3b3630
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119126166"
---
# <a name="bc7-format-mode-reference"></a>Informazioni di riferimento sulla modalità formato BC7

Questa documentazione contiene un elenco delle modalità a 8 blocchi e delle allocazioni di bit per i blocchi di formato di compressione trame BC7.

I colori per ogni subset all'interno di un blocco sono rappresentati da due colori endpoint espliciti e da un set di colori interpolati tra di essi. A seconda della precisione dell'indice del blocco, ogni subset può avere 4, 8 o 16 colori possibili.

-   [Modalità 0](#mode-0)
-   [Modalità 1](#mode-1)
-   [Modalità 2](#mode-2)
-   [Modalità 3](#mode-3)
-   [Modalità 4](#mode-4)
-   [Modalità 5](#mode-5)
-   [Modalità 6](#mode-6)
-   [Modalità 7](#mode-7)
-   [Osservazioni:](#remarks)
-   [Argomenti correlati](#related-topics)

## <a name="mode-0"></a>Modalità 0

La modalità BC7 0 presenta le caratteristiche seguenti:

-   Solo componenti a colori (senza alfa)
-   3 subset per blocco
-   Endpoint RGBP 4.4.4.1 con un bit P univoco per ogni endpoint
-   Indici a 3 bit
-   16 partizioni

![modalità layout a 0 bit](images/bc7-mode0.png)

## <a name="mode-1"></a>Modalità 1

La modalità BC7 1 presenta le caratteristiche seguenti:

-   Solo componenti a colori (senza alfa)
-   2 subset per blocco
-   Endpoint RGBP 6.6.6.1 con un bit P condiviso per subset)
-   Indici a 3 bit
-   64 partizioni

![modalità layout a 1 bit](images/bc7-mode1.png)

## <a name="mode-2"></a>Modalità 2

La modalità BC7 2 presenta le caratteristiche seguenti:

-   Solo componenti a colori (senza alfa)
-   3 subset per blocco
-   Endpoint RGB 5.5.5
-   Indici a 2 bit
-   64 partizioni

![modalità layout a 2 bit](images/bc7-mode2.png)

## <a name="mode-3"></a>Modalità 3

La modalità BC7 3 presenta le caratteristiche seguenti:

-   Solo componenti a colori (senza alfa)
-   2 subset per blocco
-   Endpoint RGBP 7.7.7.1 con un bit P univoco per subset)
-   Indici a 2 bit
-   64 partizioni

![modalità layout a 3 bit](images/bc7-mode3.png)

## <a name="mode-4"></a>Modalità 4

La modalità BC7 4 presenta le caratteristiche seguenti:

-   Componenti a colori con componente alfa separato
-   1 subset per blocco
-   Endpoint a colori RGB 5.5.5
-   Endpoint alfa a 6 bit
-   Indici a 16 x 2 bit
-   Indici a 16 x 3 bit
-   Rotazione dei componenti a 2 bit
-   Selettore di indice a 1 bit (se vengono usati gli indici a 2 o 3 bit)

![modalità layout a 4 bit](images/bc7-mode4.png)

## <a name="mode-5"></a>Modalità 5

La modalità BC7 5 presenta le caratteristiche seguenti:

-   Componenti a colori con componente alfa separato
-   1 subset per blocco
-   Endpoint a colori RGB 7.7.7
-   Endpoint alfa a 8 bit
-   Indici di colore a 16 x 2 bit
-   Indici alfa a 16 x 2 bit
-   Rotazione dei componenti a 2 bit

![modalità layout a 5 bit](images/bc7-mode5.png)

## <a name="mode-6"></a>Modalità 6

La modalità BC7 6 presenta le caratteristiche seguenti:

-   Componenti combinati di colore e alfa
-   Un subset per blocco
-   Endpoint RGBAP 7.7.7.7.1 a colori (e alfa) (bit P univoco per endpoint)
-   Indici a 16 x 4 bit

![modalità layout a 6 bit](images/bc7-mode6.png)

## <a name="mode-7"></a>Modalità 7

La modalità BC7 7 presenta le caratteristiche seguenti:

-   Componenti combinati di colore e alfa
-   2 subset per blocco
-   Endpoint RGBAP 5.5.5.5.1 a colori (e alfa) (bit P univoco per endpoint)
-   Indici a 2 bit
-   64 partizioni

![modalità layout a 7 bit](images/bc7-mode7.png)

## <a name="remarks"></a>Commenti

La modalità 8 (il byte meno significativo è impostato su 0x00) è riservata. Non usarlo nel codificatore. Se si passa questa modalità all'hardware, viene restituito un blocco inizializzato su tutti gli zeri.

In BC7 è possibile codificare il componente alfa in uno dei modi seguenti:

-   Blocca i tipi senza codifica esplicita del componente alfa. In questi blocchi, gli endpoint di colore hanno una codifica solo RGB, con il componente alfa decodificato a 1.0 per tutti i texel.
-   Tipi a blocchi con componenti di colore e alfa combinati. In questi blocchi, i valori dei colori dell'endpoint vengono specificati nel formato RGBA e i valori dei componenti alfa vengono interpolati insieme ai valori di colore.
-   Tipi a blocchi con componenti di colore e alfa separati. In questi blocchi il colore e i valori alfa vengono specificati separatamente, ognuno con il proprio set di indici. Di conseguenza, hanno un vettore effettivo e un canale scalare codificati separatamente, in cui il vettore specifica in genere i canali di colore R, G, B e scalare specifica il canale alfa \[ \] A \[ \] . Per supportare questo approccio, nella codifica viene fornito un campo separato a 2 bit, che consente la specifica della codifica del canale separata come valore scalare. Di conseguenza, il blocco può avere una delle quattro diverse rappresentazioni seguenti di questa codifica alfa (come indicato dal campo a 2 bit):
    -   RGB \| A: canale alfa separato
    -   AGB R: canale di \| colore "rosso" separato
    -   RAB \| G: canale di colore "verde" separato
    -   RGA B: canale a \| colori "blu" separato

    Il decodificatore riordina l'ordine dei canali a RGBA dopo la decodifica, in modo che il formato del blocco interno non sia visibile allo sviluppatore. I blocchi con componenti alfa e di colore separati hanno anche due set di dati di indice: uno per il set vettoriale di canali e uno per il canale scalare. Nel caso della modalità 4, questi indici hanno larghezze diverse di 2 o \[ 3 \] bit. La modalità 4 contiene anche un selettore a 1 bit che specifica se il vettore o il canale scalare usa gli indici a 3 bit.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Formato BC7](bc7-format.md)
</dt> </dl>

 

 




