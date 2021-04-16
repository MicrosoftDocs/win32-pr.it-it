---
description: Ogni volto in una mesh ha un vettore di unità perpendicolare normale, come illustrato nella figura seguente.
ms.assetid: 86e2a460-7b58-4612-8f72-5a4e864ceb58
title: Vettori normali per visi e vertici (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e0ef6fd8eba85b770cbfe71477655ddbafd8ee7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104550993"
---
# <a name="face-and-vertex-normal-vectors-direct3d-9"></a>Vettori normali per visi e vertici (Direct3D 9)

Ogni volto in una mesh ha un vettore di unità perpendicolare normale, come illustrato nella figura seguente. La direzione del vettore è determinata dall'ordine in cui sono definiti i vertici e dal fatto che il sistema di coordinate sia a destra o a sinistra. La normale faccia si allontana dal lato anteriore della faccia. In Direct3D, solo la parte anteriore di una faccia è visibile. Un front-end è quello in cui i vertici vengono definiti in ordine orario.

![illustrazione di un vettore normale per una faccia anteriore](images/nrmlvect.png)

Qualsiasi faccia che non sia un front-end è una faccia posteriore. In Direct3D non viene sempre eseguito il rendering dei visi. di conseguenza, i visi posteriori sono detti abbattuti. Se lo si desidera, è possibile modificare la modalità di eliminazione per eseguire il rendering delle facce. Per ulteriori informazioni, vedere [stato di eliminazione (Direct3D 9)](culling-state.md) .

Direct3D usa le normali unità Vertex per gli effetti di ombreggiatura, illuminazione e texturing di Gouraud. Nella figura seguente sono illustrate le normali di esempio.

![illustrazione delle normali dei vertici](images/vertnrml.png)

Quando si applica l'ombreggiatura Gouraud a un poligono, Direct3D usa le normali dei vertici per calcolare l'angolo tra la sorgente di luce e la superficie. Calcola i valori di colore e intensità per i vertici e li interpola per ogni punto in tutte le superfici della primitiva. Direct3D calcola il valore di intensità della luce usando l'angolo. Maggiore è l'angolo, minore è l'indicatore luminoso sulla superficie.

Se si sta creando un oggetto Flat, impostare le normali dei vertici in modo che punti perpendicolare alla superficie, come illustrato nella figura seguente.

![illustrazione di una superficie piatta costituita da due triangoli con le normali dei vertici](images/flatvert.png)

È più probabile, tuttavia, che l'oggetto sia costituito da strisce triangolari e che i triangoli non siano complanari. Un modo semplice per ottenere un'ombreggiatura uniforme in tutti i triangoli della striscia consiste nel calcolare innanzitutto il vettore normale della superficie per ogni volto poligonale a cui è associato il vertice. La normale del vertice può essere impostata in modo da creare un angolo uguale con ogni normale della superficie. Tuttavia, questo metodo potrebbe non essere sufficientemente efficiente per le primitive complesse.

Questo metodo è illustrato nel diagramma seguente, in cui sono illustrate due superfici, S1 e S2. I vettori normali per S1 e S2 sono visualizzati in blu. Il vettore di normalizzazione del vertice viene visualizzato in rosso. L'angolo che il vettore normale del vertice fa con la normale della superficie S1 è uguale all'angolo tra la normale del vertice e la normale della superficie di S2. Quando queste due superfici sono illuminate e ombreggiate con ombreggiatura Gouraud, il risultato è un bordo perfettamente ombreggiato e arrotondato tra di essi.

![diagramma di due superfici (S1 e S2) e dei relativi vettori normali e vettore del normale vertice](images/gvert.png)

Se la normale dei vertici si avvicina a una delle facce a cui è associata, causa l'aumento o la diminuzione dell'intensità della luce per i punti su tale superficie, a seconda dell'angolo che produce con la sorgente di luce. Il diagramma seguente illustra un esempio. Anche in questo caso, queste superfici vengono visualizzate in Edge. La normale del vertice si avvicina a S1, causando un angolo più piccolo con la sorgente di luce rispetto a quando la normale del vertice presenta angoli uguali con le normali della superficie.

![diagramma di due superfici (S1 e S2) con un vettore di normale vertice che si avvicina a una faccia](images/gvert2.png)

È possibile usare l'ombreggiatura Gouraud per visualizzare alcuni oggetti in una scena 3D con spigoli acuti. A tale scopo, duplicare i vettori normali dei vertici in qualsiasi intersezione di visi in cui è richiesto un bordo acuto, come illustrato nella figura seguente.

![illustrazione dei vettori normali dei vertici duplicati su bordi taglienti](images/shade1.png)

Se si usano i metodi DrawPrimitive per eseguire il rendering della scena, definire l'oggetto con spigoli acuti come un elenco di triangolo, anziché una striscia di triangolo. Quando si definisce un oggetto come striscia di triangolo, Direct3D lo considera come un singolo poligono composto da più facce triangolari. L'ombreggiatura Gouraud viene applicata sia in ogni faccia del poligono che tra i visi adiacenti. Il risultato è un oggetto che viene ombreggiato in modo uniforme dalla faccia alla faccia. Poiché un elenco di triangolo è un poligono composto da una serie di visi triangolari non contigui, Direct3D applica l'ombreggiatura Gouraud in ogni faccia del poligono. Non viene tuttavia applicato dalla faccia alla faccia. Se due o più triangoli di un elenco di triangolo sono adiacenti, sembrano avere un bordo affilato tra di essi.

Un'altra alternativa consiste nel passare a ombreggiatura piatta quando si esegue il rendering di oggetti con spigoli acuti. Questo è il metodo di calcolo più efficiente, ma può comportare la visualizzazione di oggetti nella scena che non vengono sottoposti a rendering in modo realistico come gli oggetti con ombreggiatura Gouraud.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sistemi di coordinate e geometria](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 



