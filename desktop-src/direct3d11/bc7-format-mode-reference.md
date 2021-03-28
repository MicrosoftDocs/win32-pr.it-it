---
title: Riferimento alla modalità di formattazione BC7
description: Questa documentazione contiene un elenco delle 8 modalità di blocco e delle allocazioni di bit per i blocchi di formato della compressione di trama BC7.
ms.assetid: B1CEB729-6694-49BF-ACB9-FD1EFAB0B0D1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 719a223e6ac057b949d5e1222582058f637ec526
ms.sourcegitcommit: 62e758931c610782807c7c9fad284921a6c56232
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/22/2020
ms.locfileid: "104398431"
---
# <a name="bc7-format-mode-reference"></a>Riferimento alla modalità di formattazione BC7

Questa documentazione contiene un elenco delle 8 modalità di blocco e delle allocazioni di bit per i blocchi di formato della compressione di trama BC7.

I colori per ogni subset in un blocco sono rappresentati da due colori dell'endpoint espliciti e da un set di colori interpolati tra di essi. A seconda della precisione dell'indice del blocco, ogni subset può avere 4, 8 o 16 colori possibili.

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

-   Solo componenti colore (nessun Alpha)
-   3 subset per blocco
-   RGBP 4.4.4.1 endpoint con un P-bit univoco per endpoint
-   indici a 3 bit
-   16 partizioni

![layout a 0 bit in modalità](images/bc7-mode0.png)

## <a name="mode-1"></a>Modalità 1

La modalità BC7 1 presenta le caratteristiche seguenti:

-   Solo componenti colore (nessun Alpha)
-   2 subset per blocco
-   RGBP 6.6.6.1 endpoint con un P-bit condiviso per subset)
-   indici a 3 bit
-   64 partizioni

![layout in modalità 1 bit](images/bc7-mode1.png)

## <a name="mode-2"></a>Modalità 2

La modalità BC7 2 presenta le caratteristiche seguenti:

-   Solo componenti colore (nessun Alpha)
-   3 subset per blocco
-   Endpoint 5.5.5 RGB
-   indici a 2 bit
-   64 partizioni

![layout in modalità a 2 bit](images/bc7-mode2.png)

## <a name="mode-3"></a>Modalità 3

La modalità BC7 3 presenta le caratteristiche seguenti:

-   Solo componenti colore (nessun Alpha)
-   2 subset per blocco
-   RGBP 7.7.7.1 endpoint con un P bit univoco per subset)
-   indici a 2 bit
-   64 partizioni

![layout in modalità a 3 bit](images/bc7-mode3.png)

## <a name="mode-4"></a>Modalità 4

La modalità BC7 4 presenta le caratteristiche seguenti:

-   Componenti colore con componente alfa separato
-   1 subset per blocco
-   Endpoint colori 5.5.5 RGB
-   endpoint alfa a 6 bit
-   indici a 2 bit a 16 x
-   indici a 3 bit a 16 bit
-   rotazione componente a 2 bit
-   selettore di indice a 1 bit (se vengono usati gli indici a 2 o 3 bit)

![layout in modalità a 4 bit](images/bc7-mode4.png)

## <a name="mode-5"></a>Modalità 5

La modalità BC7 5 presenta le caratteristiche seguenti:

-   Componenti colore con componente alfa separato
-   1 subset per blocco
-   Endpoint colori 7.7.7 RGB
-   endpoint alfa a 8 bit
-   indici di colore a 2 bit a 16 x
-   indici alfa a 2 bit a 16 x
-   rotazione componente a 2 bit

![layout in modalità a 5 bit](images/bc7-mode5.png)

## <a name="mode-6"></a>Modalità 6

La modalità BC7 6 presenta le caratteristiche seguenti:

-   Colori combinati e componenti alfa
-   Un subset per blocco
-   Endpoint RGBAP 7.7.7.7.1 Color (e Alpha) (Unique P-bit per endpoint)
-   indici a 4 bit a 16 bit

![layout in modalità a 6 bit](images/bc7-mode6.png)

## <a name="mode-7"></a>Modalità 7

La modalità BC7 7 presenta le caratteristiche seguenti:

-   Colori combinati e componenti alfa
-   2 subset per blocco
-   Endpoint RGBAP 5.5.5.5.1 Color (e Alpha) (Unique P-bit per endpoint)
-   indici a 2 bit
-   64 partizioni

![layout in modalità a 7 bit](images/bc7-mode7.png)

## <a name="remarks"></a>Commenti

Mode 8 (il byte meno significativo è impostato su 0x00) è riservato. Non usarlo nel codificatore. Se si passa questa modalità all'hardware, viene restituito un blocco inizializzato su tutti zeri.

In BC7 è possibile codificare il componente alfa in uno dei modi seguenti:

-   Tipi di blocco senza codifica esplicita del componente alfa. In questi blocchi, gli endpoint dei colori hanno una codifica solo RGB, con il componente alfa decodificato a 1,0 per tutti i Texel.
-   Tipi di blocco con componenti di colore e alfa combinati. In questi blocchi, i valori dei colori dell'endpoint vengono specificati nel formato RGBA e i valori del componente alfa vengono interpolati insieme ai valori dei colori.
-   Tipi di blocco con componenti di colore e alfa separati. In questi blocchi il colore e i valori alfa vengono specificati separatamente, ognuno con un proprio set di indici. Di conseguenza, hanno un vettore effettivo e un canale scalare codificato separatamente, in cui il vettore specifica in genere i canali di colore \[ R, G, B \] e il valore scalare specifica il canale alfa \[ a \] . Per supportare questo approccio, nella codifica viene fornito un campo a 2 bit separato, che consente di specificare la codifica del canale separata come valore scalare. Di conseguenza, il blocco può avere una delle quattro rappresentazioni seguenti di questa codifica alfa (come indicato dal campo a 2 bit):
    -   RGB \| A: canale alfa separato
    -   AGB \| R: canale colori "rosso" separato
    -   RAB \| G: canale colori "verde" separato
    -   RGA \| B: canale colori "blu" separato

    Il decodificatore Riordina nuovamente l'ordine del canale in RGBA dopo la decodifica, quindi il formato del blocco interno è invisibile per lo sviluppatore. I neri con componenti colore e alfa distinti hanno anche due set di dati di indice: uno per il set di canali vettoriale e uno per il canale scalare. (Nel caso della modalità 4, questi indici hanno larghezze diverse \[ 2 o 3 bit \] . La modalità 4 contiene inoltre un selettore a 1 bit che specifica se il vettore o il canale scalare utilizza gli indici a 3 bit.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Formato BC7](bc7-format.md)
</dt> </dl>

 

 




