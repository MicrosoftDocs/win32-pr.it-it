---
description: La proprietà light type definisce il tipo di sorgente di luce in uso.
ms.assetid: 7718383a-6e49-4ad2-acc1-fc8fec0d4844
title: Tipi di luce (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd451fcf45e67f1d789b7481fcc1884282d2018db98ab26d27481bec5277031
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674417"
---
# <a name="light-types-direct3d-9"></a>Tipi di luce (Direct3D 9)

La proprietà light type definisce il tipo di sorgente di luce in uso. Il tipo di luce viene impostato usando un valore dell'enumerazione [**C++ D3DLIGHTTYPE**](./d3dlighttype.md) nel membro Type della struttura [**D3DLIGHT9 della**](d3dlight9.md) luce. In Direct3D sono disponibili tre tipi di luci: luci punto, in evidenza e luci direzionali. Ogni tipo illumina gli oggetti in una scena in modo diverso, con diversi livelli di overhead computazionale.

## <a name="point-light"></a>Point Light

Le luci punto hanno colore e posizione all'interno di una scena, ma nessuna direzione singola. Traslano luce ugualmente in tutte le direzioni, come illustrato nella figura seguente.

![illustrazione della luce del punto](images/ptlight.png)

Una lampadina è un buon esempio di luce punto. Le luci punto sono interessate dall'attenuazione e dall'intervallo e illuminano una mesh in base a vertici per vertice. Durante l'illuminazione, Direct3D usa la posizione della luce punto nello spazio mondiale e le coordinate del vertice acceso per derivare un vettore per la direzione della luce e la distanza percorsa dalla luce. Entrambi vengono usati, insieme alla normale del vertice, per calcolare il contributo della luce all'illuminazione della superficie.

## <a name="directional-light"></a>Luce direzionale

Le luci direzionali hanno solo colore e direzione, non posizione. Emettono luce parallela. Ciò significa che tutta la luce generata da luci direzionali attraversa una scena nella stessa direzione. Imagine una luce direzionale come sorgente di luce a distanza quasi infinita, ad esempio il sole. Le luci direzionali non sono interessate dall'attenuazione o dall'intervallo, quindi la direzione e il colore specificati sono gli unici fattori considerati quando Direct3D calcola i colori dei vertici. A causa del numero ridotto di fattori di illuminazione, questi sono i luci meno intensivi dal punto di vista computazionale da usare.

## <a name="spotlight"></a>Riflettori

I rifletti hanno colore, posizione e direzione in cui emettono luce. La luce emessa da un in evidenza è costituito da un cono interno chiaro e da un cono esterno più grande, con l'intensità della luce che diminuisce tra i due, come illustrato nella figura seguente.

![illustrazione di un in evidenza con un cono interno e un cono esterno](images/spotlt.png)

I dati in evidenza sono interessati da falloff, attenuazione e intervallo. Questi fattori, così come la distanza trasferta della luce a ogni vertice, si verificano quando si calcolano gli effetti di illuminazione per gli oggetti in una scena. Il calcolo di questi effetti per ogni vertice rende i riflettori il più dispendioso in termini di tempo di calcolo di tutte le luci in Direct3D.

La [**struttura C++ D3DLIGHT9**](d3dlight9.md) contiene tre membri che vengono usati solo dai spotlight. Questi membri, Falloff, Theta e Phi, controllano le dimensioni dei coni interni ed esterni di un oggetto in evidenza e la diminuzione della luce tra di essi.

Il valore di Theta è l'angolo radiante del cono interno del riflettore e il valore phi è l'angolo per il cono esterno della luce. Il valore Falloff controlla il modo in cui l'intensità della luce diminuisce tra il bordo esterno del cono interno e il bordo interno del cono esterno. La maggior parte delle applicazioni imposta Falloff su 1.0 per creare un falloff che si verifica in modo uniforme tra i due coni, ma è possibile impostare altri valori in base alle esigenze.

La figura seguente illustra la relazione tra i valori di questi membri e il modo in cui possono influire sui coni di luce interni ed esterni di un spotlight.

![illustrazione del modo in cui i valori phi e theta sono correlati ai coni in evidenza](images/spotlt2.png)

I riflettori generano un cono di luce che ha due parti: un cono interno chiaro e un cono esterno. La luce è più chiaro nel cono interno e non è presente all'esterno del cono esterno, con l'intensità della luce che si attenua tra le due aree. Questo tipo di attenuazione viene comunemente definito falloff.

La quantità di luce ricevuta da un vertice si basa sulla posizione del vertice nei coni interni o esterni. Direct3D calcola il prodotto punto del vettore di direzione (L) del punto in evidenza e il vettore dalla luce al vertice (D). Questo valore è uguale al coseno dell'angolo tra i due vettori e funge da indicatore della posizione del vertice che può essere confrontato con gli angoli del cono della luce per determinare dove potrebbe trovarsi il vertice nei coni interni o esterni. La figura seguente fornisce una rappresentazione grafica dell'associazione tra questi due vettori.

![illustrazione del vettore di direzione in evidenza e del vettore dal vertice al punto in evidenza](images/spotalg1.png)

Il sistema confronta questo valore con il coseno degli angoli del cono interno ed esterno del punto in evidenza. Nella struttura [**D3DLIGHT9**](d3dlight9.md) della luce, i membri Theta e Phi rappresentano gli angoli coni totali per i coni interni ed esterni. Poiché l'attenuazione si verifica quando il vertice diventa più distante dal centro dell'illuminazione (anziché dall'angolo totale del cono), il runtime divide questi angoli del cono a metà prima di calcolare le rispettive terminazioni.

Se il prodotto del punto dei vettori L e D è minore o uguale al coseno dell'angolo del cono esterno, il vertice si trova oltre il cono esterno e non riceve luce. Se il prodotto punto di L e D è maggiore del coseno dell'angolo del cono interno, il vertice si trova all'interno del cono interno e riceve la quantità massima di luce, considerando comunque l'attenuazione sulla distanza. Se il vertice si trova in un punto compreso tra le due aree, il falloff viene calcolato con l'equazione seguente.

![formula per l'intensità della luce al vertice, dopo il falloff](images/falloff.png)

Dove:

-   I <sub>f è</sub> intensità leggera dopo il falloff
-   Alfa è l'angolo tra i vettori L e D
-   Theta è l'angolo del cono interno
-   Phi è l'angolo del cono esterno
-   p è il falloff

Questa formula genera un valore compreso tra 0,0 e 1,0 che ridimensiona l'intensità della luce nel vertice per calcolare il falloff. Viene applicata anche l'attenuazione come fattore della distanza del vertice dalla luce. Il grafico seguente mostra in che modo i diversi valori di falloff possono influire sulla curva di falloff.

![grafico dell'intensità della luce rispetto alla distanza dei vertici dalla luce](images/fallgraf.png)

L'effetto dei vari valori di falloff sull'illuminazione effettiva è sottile e si incorre in una piccola diminuzione delle prestazioni modellando la curva di falloff con valori di falloff diversi da 1,0. Per questi motivi, questo valore è in genere impostato su 1.0.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Luci e materiali](lights-and-materials.md)
</dt> </dl>

 

 
