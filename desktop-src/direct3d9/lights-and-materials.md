---
description: Le luci vengono usate per illuminare gli oggetti in una scena.
ms.assetid: 0751bb76-611a-41c4-aab2-aa6f68b61b0e
title: Luci e materiali (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6f44a12c1be1e7a14f7bfe176d7f391901d2dac
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401061"
---
# <a name="lights-and-materials-direct3d-9"></a>Luci e materiali (Direct3D 9)

Le luci vengono usate per illuminare gli oggetti in una scena. Quando l'illuminazione è abilitata, Direct3D calcola il colore di ogni vertice dell'oggetto in base a una combinazione di:

> [!Note]  
> Questa sezione è destinata solo alla pipeline a funzione fissa. Gli shader programmabili eseguono tutte le operazioni di illuminazione in modo esplicito.

 

-   Il colore del materiale corrente e i Texel in una mappa di trama associata.
-   Colori con riflessione diffusa e speculare nel vertice, se specificato.
-   Il colore e l'intensità della luce prodotta dalle fonti di luce nella scena o dal livello di luce ambientale della scena.

Quando si usa l'illuminazione e i materiali Direct3D, si consente a Direct3D di gestire i dettagli dell'illuminazione. Se necessario, gli utenti avanzati possono eseguire l'illuminazione autonomamente.

La modalità di utilizzo di illuminazione e materiali fa una grande differenza nell'aspetto della scena di cui è stato eseguito il rendering. I materiali definiscono il modo in cui la luce riflette una superficie. I livelli di luce diretta e ambientale definiscono la luce che viene riflessa. Se l'illuminazione è abilitata, è necessario utilizzare i materiali per eseguire il rendering di una scena. Non sono necessarie luci per eseguire il rendering di una scena, ma i dettagli in una scena sottoposta a rendering senza luce non sono visibili. Al meglio, il rendering di una scena spenta genera una silhouette degli oggetti nella scena. Questo non è un dettaglio sufficiente per la maggior parte degli scopi.

## <a name="direct-light-vs-ambient-light"></a>Luce diretta e luce ambiente

Sebbene sia la luce diretta che quella di ambiente illuminano gli oggetti in una scena, sono indipendenti l'uno dall'altro, hanno effetti molto diversi e richiedono l'uso in modi completamente diversi.

La luce diretta è semplicemente: diretto. La luce diretta ha sempre la direzione e il colore ed è un fattore per gli algoritmi di ombreggiatura, ad esempio l'ombreggiatura Gouraud. Tipi diversi di luci emettono luce diretta in modi diversi, creando effetti speciali di attenuazione. Per creare un set di parametri luce per la luce diretta, chiamare il metodo [**IDirect3DDevice9:: selight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight) .

Ambiente chiaro è in realtà ovunque in una scena. È possibile considerarlo come un livello generale di luce che riempie un'intera scena, indipendentemente dagli oggetti e dalle rispettive posizioni nella scena. La luce di ambiente non ha posizione o direzione, ma solo il colore e l'intensità. Ogni luce si aggiunge alla luce di ambiente complessiva in una scena. Impostare il livello di luce di ambiente con una chiamata al metodo [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) , specificando D3DRS \_ ambiente come parametro di *stato* e il colore RGBA desiderato come parametro del valore.

Il colore della luce ambientale assume il formato di un valore RGBA, in cui ogni componente è un valore intero compreso tra 0 e 255. Questo è diverso dalla maggior parte dei valori di colore in Direct3D.

È possibile usare la macro [**D3DCOLOR \_ RGBA**](d3dcolor-rgba.md) per generare valori RGBA. I componenti rosso, verde e blu si combinano per rendere il colore finale della luce dell'ambiente. Il componente alfa controlla la trasparenza del colore. Quando si usa l'accelerazione hardware o l'emulazione RGB, il componente alfa viene ignorato.

## <a name="direct3d-light-model-vs-nature"></a>Confronto tra modello leggero Direct3D e natura

Per natura, quando la luce viene emessa da un'origine, viene riflessa da centinaia, se non da migliaia o milioni di oggetti prima di raggiungere l'occhio dell'utente. Ogni volta che viene riflessa, una luce viene assorbita da una superficie, altre è suddivisa in direzioni casuali e il resto passa a un'altra superficie o all'occhio dell'utente. Questo processo continua fino a quando la luce non viene ridotta a niente o un utente percepisce la luce.

Ovviamente, i calcoli necessari per simulare perfettamente il comportamento naturale della luce sono troppo lunghi da usare per la grafica Direct3D in tempo reale. Pertanto, con la massima rapidità, il modello Direct3D Light si avvicina al modo in cui Light funziona nel mondo naturale. Direct3D descrive la luce in termini di componenti rosso, verde e blu che si combinano per creare un colore finale.

In Direct3D, quando la luce riflette una superficie, il colore chiaro interagisce matematicamente con la superficie stessa per creare il colore visualizzato sullo schermo. Per informazioni specifiche sugli algoritmi usati da Direct3D, vedere [matematica dell'illuminazione (Direct3D 9)](mathematics-of-lighting.md).

Il modello della luce Direct3D generalizza la luce in due tipi: luce ambientale e luce diretta. Ognuno ha attributi diversi e ognuno interagisce con il materiale di una superficie in modi diversi. L'ambiente chiaro è chiaro che è stato sparso così tanto che la direzione e l'origine sono indeterminate: mantiene un basso livello di intensità ovunque. L'illuminazione indiretta usata dai fotografi è un valido esempio di luce ambientale. La luce ambientale in Direct3D, come per natura, non ha alcuna direzione o origine reale, bensì solo un colore e un'intensità. Infatti, il livello di luce di ambiente è completamente indipendente dagli oggetti in una scena che generano luce. Ambiente chiaro non contribuisce alla reflection speculare.

La luce diretta è la luce generata da un'origine all'interno di una scena; ha sempre il colore e l'intensità e viaggia in una direzione specificata. La luce diretta interagisce con il materiale di una superficie per creare evidenziazioni speculari e la direzione viene utilizzata come fattore per gli algoritmi di ombreggiatura, inclusa l'ombreggiatura Gouraud. Quando la luce diretta viene riflessa, non contribuisce al livello di luce di ambiente in una scena. Le origini in una scena che generano luce diretta hanno caratteristiche diverse che influiscono sul modo in cui illuminano una scena.

Inoltre, il materiale di un poligono ha proprietà che influiscono sulla modalità con cui il poligono riflette la luce che riceve. Si imposta un tratto di Reflection singolo che descrive il modo in cui il materiale riflette la luce ambientale e si impostano i singoli tratti per determinare la reflection speculare e diffusa del materiale. Per ulteriori informazioni, vedere [Materials (Direct3D 9)](materials.md).

## <a name="color-values-for-lights-and-materials"></a>Valori di colore per luci e materiali

Direct3D descrive il colore in termini di quattro componenti: rosso, verde, blu e alfa, combinati per creare un colore finale. La struttura C++ [**D3DCOLORVALUE**](d3dcolorvalue.md) è definita per contenere valori per ogni componente. Ogni membro è un valore a virgola mobile che in genere è compreso tra 0,0 e 1,0 inclusi. Sebbene sia le luci che i materiali usino la stessa struttura per descrivere il colore, i valori della struttura vengono usati in modo leggermente diverso da ciascuno.

I valori dei colori per le origini chiare rappresentano la quantità di un particolare componente chiaro emesso. Poiché le luci non usano un componente alfa, sono rilevanti solo i componenti rosso, verde e blu del colore. È possibile visualizzare i tre componenti come le lenti rosse, verdi e blu in un televisore di proiezione. Ogni lente può essere disattivata (un valore 0,0 nel membro appropriato), potrebbe essere il più chiaro possibile (un valore 1,0) o un certo livello di tempo compreso tra. I colori che passano attraverso le lenti si uniscono per rendere il colore finale della luce. Una combinazione come R (1.0), G (1.0), B (1.0) crea una luce bianca, dove R (0,0), G (0,0), B (0,0) non emette la luce. È possibile creare una luce che emette solo un componente, ottenendo una luce pura, verde o blu; in alternativa, la luce potrebbe usare combinazioni per emettere colori come giallo o viola. È anche possibile impostare valori negativi per i componenti di colore per creare una "luce scura" che rimuove effettivamente la luce da una scena. In alternativa, è possibile impostare i componenti su un valore maggiore di 1,0 per creare una luce estremamente luminosa.

Con i materiali, d'altra parte, i valori dei colori rappresentano la quantità di un componente leggero riflesso da una superficie di cui viene eseguito il rendering con tale materiale. Un materiale i cui componenti di colore sono R (1.0), G (1.0), B (1.0), A (1.0) riflette tutta la luce che è in arrivo. Analogamente, un materiale con R (0,0), G (1.0), B (0,0), A (1.0) riflette tutta la luce verde che viene indirizzata. I materiali hanno più valori di reflection per creare vari tipi di effetti.

Informazioni aggiuntive sono contenute in: [tipi leggeri (Direct3D 9)](light-types.md)e [Proprietà Light (Direct3D 9)](light-properties.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Per iniziare](getting-started.md)
</dt> </dl>

 

 
