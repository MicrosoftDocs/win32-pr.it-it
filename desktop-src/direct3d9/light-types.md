---
description: La proprietà tipo di luce definisce il tipo di origine di luce che si sta usando.
ms.assetid: 7718383a-6e49-4ad2-acc1-fc8fec0d4844
title: Tipi leggeri (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39ae2c7fd5380b0f604181f36d784afe3f3fc3ff
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104048868"
---
# <a name="light-types-direct3d-9"></a>Tipi leggeri (Direct3D 9)

La proprietà tipo di luce definisce il tipo di origine di luce che si sta usando. Il tipo di luce viene impostato usando un valore dell'enumerazione C++ [**D3DLIGHTTYPE**](./d3dlighttype.md) nel membro del tipo della struttura [**D3DLIGHT9**](d3dlight9.md) della luce. Sono disponibili tre tipi di luci nelle luci del punto Direct3D, nei faretti e nelle luci direzionali. Ogni tipo illumina gli oggetti in una scena in modo diverso, con diversi livelli di overhead computazionale.

## <a name="point-light"></a>Luce puntiforme

Le luci puntiformi hanno il colore e la posizione all'interno di una scena, ma nessuna direzione singola. Forniscono ugualmente la luce in tutte le direzioni, come illustrato nella figura seguente.

![illustrazione della luce del punto](images/ptlight.png)

Una lampadina è un valido esempio di luce puntiforme. Le luci puntiformi sono interessate dall'attenuazione e dall'intervallo e illuminano una mesh in base ai vertici. Durante l'illuminazione, Direct3D usa la posizione della luce del punto nello spazio globale e le coordinate del vertice da illuminare per derivare un vettore per la direzione della luce e la distanza con cui è stata spostata la luce. Entrambi vengono utilizzati, insieme alla normale del vertice, per calcolare il contributo della luce sull'illuminazione della superficie.

## <a name="directional-light"></a>Luce direzionale

Le luci direzionali hanno solo il colore e la direzione, non la posizione. Emettono luce parallela. Ciò significa che tutta la luce generata da luci direzionali attraversa una scena nella stessa direzione. Immaginate una luce direzionale come una sorgente di luce a distanza quasi infinita, ad esempio il sole. Le luci direzionali non vengono influenzate dall'attenuazione o dall'intervallo, quindi la direzione e il colore specificati sono gli unici fattori considerati quando Direct3D calcola i colori dei vertici. A causa del numero ridotto di fattori di illuminazione, si tratta delle spie meno complesse da usare.

## <a name="spotlight"></a>Riflettori

I riflettori hanno il colore, la posizione e la direzione in cui emettono la luce. La luce emessa da un riflettore è costituita da un cono interno luminoso e da un cono esterno più grande, con l'intensità di luce che diminuisce tra i due, come illustrato nella figura seguente.

![illustrazione di un oggetto Spotlight con un cono interno e un cono esterno](images/spotlt.png)

I Spotlight sono interessati da decadimento, attenuazione e intervallo. Questi fattori, oltre alla luce della distanza per ogni vertice, vengono calcolati quando si calcolano gli effetti di illuminazione per gli oggetti in una scena. Il calcolo di questi effetti per ogni vertice rende Spotlight la maggior parte del tempo di calcolo di tutte le luci in Direct3D.

La struttura C++ [**D3DLIGHT9**](d3dlight9.md) contiene tre membri che vengono usati solo da Spotlight. Questi membri, ovvero decadimento, theta e Phi, controllano la dimensione o i coni interni ed esterni di un oggetto Spotlight e il modo in cui la luce diminuisce tra di essi.

Il valore theta è l'angolo radiante del cono interno del faretto e il valore Phi è l'angolo per il cono esterno della luce. Il valore di interruzione controlla il modo in cui l'intensità di luminosità diminuisce tra il bordo esterno del cono interno e il bordo interno del cono esterno. Per la maggior parte delle applicazioni è stato impostato il decadimento su 1,0 per creare un'interruzione che si verifica uniformemente tra i due coni, ma è possibile impostare altri valori in base alle esigenze.

Nella figura seguente viene illustrata la relazione tra i valori di questi membri e il modo in cui possono influenzare i coni di luce interni ed esterni di Spotlight.

![illustrazione del modo in cui i valori Phi e teta sono correlati ai coni Spotlight](images/spotlt2.png)

I riflettori emettono un cono di luce con due parti: un cono interno chiaro e un cono esterno. La luce è più luminosa nel cono interno e non è presente all'esterno del cono esterno, con una lieve intensità di attenuazione tra le due aree. Questo tipo di attenuazione è comunemente noto come interruzione.

La quantità di luce ricevuta da un vertice è basata sulla posizione del vertice nei coni interni o esterni. Direct3D calcola il prodotto scalare del vettore di direzione di Spotlight (L) e il vettore dalla luce al vertice (D). Questo valore è uguale al coseno dell'angolo tra i due vettori e funge da indicatore della posizione del vertice che può essere confrontato con gli angoli conici della luce per determinare il punto in cui il vertice potrebbe trovarsi nei coni interni o esterni. Nell'illustrazione seguente viene fornita una rappresentazione grafica dell'associazione tra i due vettori.

![illustrazione del vettore di direzione Spotlight e del vettore dal vertice al primo piano](images/spotalg1.png)

Il sistema confronta questo valore con il coseno degli angoli dei coni interni ed esterni del faretto. Nella struttura [**D3DLIGHT9**](d3dlight9.md) della luce i membri theta e Phi rappresentano gli angoli conici totali per i coni interni ed esterni. Poiché l'attenuazione si verifica quando il vertice diventa più distante dal centro dell'illuminazione (invece che dall'angolo del cono totale), il runtime divide la metà di questi angoli del cono prima di calcolare i loro coseni.

Se il prodotto punto dei vettori L e D è minore o uguale al coseno dell'angolo del cono esterno, il vertice si trova oltre il cono esterno e non riceve luce. Se il prodotto punto di L e D è maggiore del coseno dell'angolo del cono interno, il vertice si trova all'interno del cono interno e riceve la quantità massima di luce, continuando a considerare l'attenuazione rispetto alla distanza. Se il vertice si trova in un punto qualsiasi tra le due aree, il decadimento viene calcolato con la seguente equazione.

![formula per l'intensità di luce al vertice, dopo l'interruzione](images/falloff.png)

Dove:

-   I <sub>f</sub> sono intensità di luce dopo il decadimento
-   Alfa è l'angolo tra i vettori L e D
-   Theta è l'angolo del cono interno
-   Phi è l'angolo del cono esterno
-   p è il decadimento

Questa formula genera un valore compreso tra 0,0 e 1,0 che consente di ridimensionare l'intensità della luce nel vertice per tenere conto del decadimento. Viene applicata anche l'attenuazione come fattore della distanza del vertice dalla luce. Il grafico seguente mostra in che modo i valori di interruzione diversi possono influenzare la curva di decadimento.

![grafico dell'intensità chiara rispetto alla distanza del vertice dalla luce](images/fallgraf.png)

L'effetto dei diversi valori di interruzione sull'illuminazione effettiva è ridotto e si verifica una lieve riduzione delle prestazioni mediante la definizione della curva di interruzione con valori di interruzione diversi da 1,0. Per questi motivi, questo valore viene in genere impostato su 1,0.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Luci e materiali](lights-and-materials.md)
</dt> </dl>

 

 
