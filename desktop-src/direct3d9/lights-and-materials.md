---
description: Le luci vengono usate per illuminare gli oggetti in una scena.
ms.assetid: 0751bb76-611a-41c4-aab2-aa6f68b61b0e
title: Luci e materiali (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a5ace2a80bb79d192fadc5376256eedf9229be9a36fa1d200341ccf28e961fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119277521"
---
# <a name="lights-and-materials-direct3d-9"></a>Luci e materiali (Direct3D 9)

Le luci vengono usate per illuminare gli oggetti in una scena. Quando l'illuminazione è abilitata, Direct3D calcola il colore di ogni vertice dell'oggetto in base a una combinazione di:

> [!Note]  
> Questa sezione è solo per la pipeline a funzione fissa. Gli shader programmabili eseguono tutte le operazioni di illuminazione in modo esplicito.

 

-   Colore del materiale corrente e texel in una mappa di trama associata.
-   Colori diffusi e speculari in corrispondenza del vertice, se specificato.
-   Colore e intensità della luce prodotta dalle sorgenti di luce nella scena o nel livello di luce ambientale della scena.

Quando si usano l'illuminazione e i materiali Direct3D, si consente a Direct3D di gestire automaticamente i dettagli dell'illuminazione. Gli utenti avanzati possono eseguire l'illuminazione da soli, se lo si desidera.

Il modo in cui si lavora con l'illuminazione e i materiali fa una grande differenza nell'aspetto della scena sottoposta a rendering. I materiali definiscono il modo in cui la luce si riflette su una superficie. I livelli di luce diretta e di luce ambientale definiscono la luce riflessa. È necessario usare i materiali per eseguire il rendering di una scena se l'illuminazione è abilitata. Le luci non sono necessarie per eseguire il rendering di una scena, ma i dettagli in una scena di cui viene eseguito il rendering senza luce non sono visibili. Nel migliore dei modi, il rendering di una scena non illuminata comporta un gruppo di oggetti nella scena. Questo non è un dettaglio sufficiente per la maggior parte degli scopi.

## <a name="direct-light-vs-ambient-light"></a>Confronto tra luce diretta e luce ambientale

Anche se la luce diretta e la luce ambientale illuminano gli oggetti in una scena, sono indipendenti l'uno dall'altro, hanno effetti molto diversi e richiedono di lavorare con essi in modi completamente diversi.

La luce diretta è esattamente questo: diretto. La luce diretta ha sempre la direzione e il colore ed è un fattore per gli algoritmi di ombreggiatura, ad esempio l'ombreggiatura Gouraud. Diversi tipi di luci emettono luce diretta in modi diversi, creando effetti di attenuazione speciali. È possibile creare un set di parametri di luce per la luce diretta chiamando il [**metodo IDirect3DDevice9::SetLight.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight)

La luce ambientale è in effetti ovunque in una scena. È possibile considerarlo come un livello generale di luce che riempie un'intera scena, indipendentemente dall'oggetto e dalle relative posizioni in tale scena. La luce ambientale non ha posizione o direzione, ma solo colore e intensità. Ogni luce aggiunge alla luce ambientale complessiva in una scena. Impostare il livello di luce ambientale con una chiamata al metodo [**IDirect3DDevice9::SetRenderState,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) specificando D3DRS AMBIENT come parametro State e il colore RGBA desiderato come parametro \_ Value. 

Il colore della luce ambientale assume la forma di un valore RGBA, dove ogni componente è un valore intero compreso tra 0 e 255. Questo è diverso dalla maggior parte dei valori di colore in Direct3D.

È possibile usare la macro [**D3DCOLOR \_ RGBA**](d3dcolor-rgba.md) per generare valori RGBA. I componenti rosso, verde e blu si combinano per ottenere il colore finale della luce ambientale. Il componente alfa controlla la trasparenza del colore. Quando si usa l'accelerazione hardware o l'emulazione RGB, il componente alfa viene ignorato.

## <a name="direct3d-light-model-vs-nature"></a>Confronto tra modello di luce Direct3D e natura

In natura, quando la luce viene emessa da una sorgente, viene riflessa da centinaia, se non migliaia o milioni di oggetti prima di raggiungere l'occhio dell'utente. Ogni volta che viene riflessa, una luce è invasa da una superficie, altre sono sparse in direzioni casuali e il resto passa a un'altra superficie o all'occhio dell'utente. Questo processo continua fino a quando la luce non viene ridotta a nulla o non viene percepita da un utente.

Ovviamente, i calcoli necessari per simulare perfettamente il comportamento naturale della luce sono troppo lunghi da usare per la grafica Direct3D in tempo reale. Di conseguenza, con la velocità, il modello di luce Direct3D approssima il funzionamento della luce nel mondo naturale. Direct3D descrive la luce in termini di componenti rosso, verde e blu che si combinano per creare un colore finale.

In Direct3D, quando la luce si riflette su una superficie, il colore chiaro interagisce matematicamente con la superficie stessa per creare il colore visualizzato sullo schermo. Per informazioni specifiche sugli algoritmi utilizzati da Direct3D, vedere [Matematica dell'illuminazione (Direct3D 9).](mathematics-of-lighting.md)

Il modello di luce Direct3D generalizza la luce in due tipi: luce ambientale e luce diretta. Ognuno ha attributi diversi e ognuno interagisce con il materiale di una superficie in modi diversi. La luce ambientale è una luce che è stata dispersa a tal punto che la direzione e la sorgente sono indeterminate: mantiene ovunque un basso livello di intensità. L'illuminazione indiretta usata dalle lucentine è un buon esempio di luce ambientale. La luce ambientale in Direct3D, come in natura, non ha alcuna direzione o sorgente reale, ma solo un colore e un'intensità. In realtà, il livello di luce ambientale è completamente indipendente da qualsiasi oggetto in una scena che genera luce. La luce ambientale non contribuisce alla reflection speculare.

La luce diretta è la luce generata da una sorgente all'interno di una scena; ha sempre colore e intensità e si sposta in una direzione specificata. La luce diretta interagisce con il materiale di una superficie per creare evidenziazioni speculari e la sua direzione viene usata come fattore negli algoritmi di ombreggiatura, inclusa l'ombreggiatura Gouraud. Quando la luce diretta viene riflessa, non contribuisce al livello di luce ambientale in una scena. Le origini in una scena che generano luce diretta hanno caratteristiche diverse che influiscono sul modo in cui illuminano una scena.

Inoltre, il materiale di un poligono ha proprietà che influiscono sul modo in cui tale poligono riflette la luce che riceve. Si imposta un singolo tratto di riflettenza che descrive il modo in cui il materiale riflette la luce ambientale e si impostano singoli tratti per determinare la riflettenza speculare e diffusa del materiale. Per altre informazioni, vedere [Materials (Direct3D 9)](materials.md).

## <a name="color-values-for-lights-and-materials"></a>Valori di colore per luci e materiali

Direct3D descrive il colore in termini di quattro componenti, rosso, verde, blu e alfa, che si combinano per creare un colore finale. La [**struttura C++ D3DCOLORVALUE**](d3dcolorvalue.md) è definita in modo da contenere valori per ogni componente. Ogni membro è un valore a virgola mobile che in genere è compreso tra 0,0 e 1,0 inclusi. Anche se le luci e i materiali usano la stessa struttura per descrivere il colore, i valori nella struttura vengono usati in modo leggermente diverso da ognuno.

I valori di colore per le sorgenti di luce rappresentano la quantità di un particolare componente chiaro che emette. Poiché le luci non usano un componente alfa, sono rilevanti solo i componenti rosso, verde e blu del colore. È possibile visualizzare i tre componenti come lenti rosse, verdi e blu su una proiezione tv. Ogni lente potrebbe essere disattivata (un valore 0,0 nel membro appropriato), potrebbe essere il più chiaro possibile (un valore 1,0) o potrebbe essere un livello compreso tra un membro e l'altro. I colori che passano attraverso le lenti si combinano per rendere il colore finale della luce. Una combinazione come R(1.0), G(1.0), B(1.0) crea una luce bianca, in cui R(0.0), G(0.0), B(0.0) non emette luce. È possibile creare una luce che emette un solo componente, generando una luce rossa, verde o blu pura; oppure la luce può usare combinazioni per emettere colori come il giallo o il viola. È anche possibile impostare valori negativi del componente colore per creare una "luce scura" che rimuove effettivamente la luce da una scena. In caso contrario, è possibile impostare i componenti su un valore maggiore di 1,0 per creare una luce estremamente luce.

Con i materiali, d'altra parte, i valori di colore rappresentano la quantità di un componente chiaro riflessa da una superficie di cui viene eseguito il rendering con tale materiale. Un materiale i cui componenti di colore sono R(1.0), G(1.0), B(1.0), A(1.0) riflette tutta la luce che si presenta. Analogamente, un materiale con R(0.0), G(1.0), B(0.0), A(1.0) riflette tutta la luce verde verso di esso. I materiali hanno più valori di riflettenza per creare vari tipi di effetti.

Altre informazioni sono contenute in: Tipi di luce [(Direct3D 9)](light-types.md)e [Proprietà luce (Direct3D 9).](light-properties.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Per iniziare](getting-started.md)
</dt> </dl>

 

 
