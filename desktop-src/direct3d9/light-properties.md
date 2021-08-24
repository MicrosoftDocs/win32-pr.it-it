---
description: Le proprietà della luce descrivono il tipo e il colore di una sorgente di luce.
ms.assetid: b39f1287-c67b-4cbb-b599-4a1b2f4981ac
title: Proprietà light (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14c3e815401fe0b35c7409dec783515de5c3422ac92d6aed6fd4adebf09f8c18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747001"
---
# <a name="light-properties-direct3d-9"></a>Proprietà light (Direct3D 9)

Le proprietà della luce descrivono il tipo e il colore di una sorgente di luce. A seconda del tipo di luce in uso, una luce può avere proprietà per l'attenuazione e l'intervallo o per gli effetti in evidenza. Tuttavia, non tutti i tipi di luci usano tutte le proprietà. Direct3D usa la [**struttura D3DLIGHT9**](d3dlight9.md) per portare informazioni sulle proprietà della luce per tutti i tipi di sorgenti di luce. Questa sezione contiene informazioni per tutte le proprietà light. Le informazioni sono suddivise nei gruppi seguenti.

Le proprietà di posizione, intervallo e attenuazione definiscono la posizione di una luce nello spazio mondiale e il comportamento della luce emette sulla distanza. Come per tutte le proprietà di luce usate in C++, queste sono contenute nella struttura [**D3DLIGHT9 di una**](d3dlight9.md) luce.

-   [Attenuazione della luce](#light-attenuation)
-   [Colore chiaro](#light-color)
-   [Direzione luce](#light-direction)
-   [Posizione della luce](#light-position)
-   [Intervallo di luce](#light-range)

## <a name="light-attenuation"></a>Attenuazione della luce

L'attenuazione controlla il modo in cui l'intensità di una luce diminuisce verso la distanza massima specificata dalla proprietà range. Tre [**membri della struttura D3DLIGHT9**](d3dlight9.md) rappresentano l'attenuazione della luce: Attenuation0, Attenuation1 e Attenuation2. Questi membri contengono valori a virgola mobile compresi tra 0,0 e infinito, controllando l'attenuazione di una luce. Alcune applicazioni impostano il membro Attenuation1 su 1.0 e le altre su 0.0, con conseguente intensità della luce che cambia come 1/D, dove D è la distanza dalla sorgente di luce al vertice. L'intensità massima della luce è alla sorgente, riducendo a 1/ (intervallo di luce) all'intervallo della luce. In genere, un'applicazione imposta Attenuation0 su 0.0, Attenuation1 su un valore costante e Attenuation2 su 0.0.

È possibile combinare i valori di attenuazione per ottenere effetti di attenuazione più complessi. In caso contrario, è possibile impostarli su valori non compreso nell'intervallo normale per creare effetti di attenuazione uniforme. I valori di attenuazione negativi, tuttavia, non sono consentiti. Vedere [Attenuazione e fattore spotlight (Direct3D 9).](attenuation-and-spotlight-factor.md)

## <a name="light-color"></a>Colore chiaro

Le luci in Direct3D generano tre colori che vengono usati in modo indipendente nei calcoli di illuminazione del sistema: un colore diffuso, un colore ambientale e un colore speculare. Ognuno è incorporato dal modulo di illuminazione Direct3D, che interagisce con una controparte del materiale corrente, per produrre un colore finale usato nel rendering. Il colore diffuso interagisce con la proprietà di riflessione diffusa del materiale corrente, il colore speculare con la proprietà di riflettore speculare del materiale e così via. Per informazioni specifiche su come Direct3D applica questi colori, vedere [Matematica dell'illuminazione (Direct3D 9).](mathematics-of-lighting.md)

In un'applicazione C++ la struttura [**D3DLIGHT9**](d3dlight9.md) include tre membri per questi colori, Diffuse, Ambient e Specular, ognuno dei quali è una [**struttura D3DCOLORVALUE**](d3dcolorvalue.md) che definisce il colore generato.

Il tipo di colore che si applica maggiormente ai calcoli del sistema è il colore diffuso. Il colore diffuso più comune è il bianco (R:1.0 G:1.0 B:1.0), ma è possibile creare i colori in base alle esigenze per ottenere gli effetti desiderati. Ad esempio, è possibile usare la luce rossa per un viaggio oppure la luce verde per un segnale di traffico impostato su "Go".

In genere, i componenti di colore chiaro vengono impostati su valori compresi tra 0,0 e 1,0 inclusi, ma questo non è un requisito. Ad esempio, è possibile impostare tutti i componenti su 2.0, creando una luce "più chiaro del bianco". Questo tipo di impostazione può essere particolarmente utile quando si usano impostazioni di attenuazione diverse dalla costante.

Si noti che anche se Direct3D usa i valori RGBA per le luci, il componente di colore alfa non viene usato.

I colori dei materiali vengono in genere usati per l'illuminazione. È tuttavia possibile specificare che i colori dei materiali emissivi, ambientali, diffusi e speculari devono essere sostituiti dai colori dei vertici diffusi o speculari. Questa operazione viene eseguita chiamando [**SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) e impostando le variabili di stato del dispositivo elencate nella tabella seguente.



| Variabile di stato del dispositivo         | Significato                                       | Type                   | Predefinito          |
|-------------------------------|-----------------------------------------------|------------------------|------------------|
| D3DRS \_ AMBIENTMATERIALSOURCE  | Definisce dove ottenere il colore del materiale di ambiente.  | D3DMATERIALCOLORSOURCE | MATERIALE D3DMCS \_ |
| D3DRS \_ DIFFUSEMATERIALSOURCE  | Definisce dove ottenere il colore del materiale diffuso.  | D3DMATERIALCOLORSOURCE | COLORE 1 DI D3DMCS \_   |
| D3DRS \_ SPECULARMATERIALSOURCE | Definisce dove ottenere il colore del materiale speculare. | D3DMATERIALCOLORSOURCE | D3DMCS \_ COLOR2   |
| D3DRS \_ EMISSIVEMATERIALSOURCE | Definisce dove ottenere il colore del materiale emissivo. | D3DMATERIALCOLORSOURCE | MATERIALE D3DMCS \_ |
| D3DRS \_ COLORVERTEX            | Disabilita o abilita l'uso dei colori dei vertici.     | BOOL                   | true             |



 

Il valore alfa/trasparenza proviene sempre solo dal canale alfa del colore diffuso.

Il valore del colore blu proviene sempre solo dal canale alfa del colore speculare.

D3DMATERIALCOLORSOURCE può avere i valori seguenti.

-   MATERIALE D3DMCS: \_ il colore del materiale viene usato come origine.
-   D3DMCS COLOR1: come origine viene usato il colore del vertice \_ diffuso.
-   D3DMCS COLOR2 : come origine viene usato il \_ colore del vertice speculare.

## <a name="light-direction"></a>Direzione luce

La proprietà direction di una luce determina la direzione della luce emessa dall'oggetto, nello spazio del mondo. La direzione viene usata solo da luci direzionali e in evidenza e viene descritta con un vettore.

Impostare la direzione della luce nel membro Direction della struttura [**D3DLIGHT9 della**](d3dlight9.md) luce. Il membro direction è di tipo [**D3DVECTOR.**](d3dvector.md) I vettori di direzione sono descritti come distanze da un'origine logica, indipendentemente dalla posizione della luce in una scena. Pertanto, un elemento spotlight che punta direttamente in una scena, lungo l'asse z positivo, ha un vettore di direzione di <0,0,1> indipendentemente dalla posizione in cui è definita. Analogamente, è possibile simulare i ghiai di luce direttamente su una scena usando una luce direzionale la cui direzione è <0,-1,0>. Ovviamente, non è necessario creare luci che risplendono lungo gli assi delle coordinate. È possibile combinare e associare valori per creare luci che si distallano da angoli più interessanti.

> [!Note]  
> Anche se non è necessario normalizzare il vettore di direzione di una luce, assicurarsi sempre che abbia grandezza. In altre parole, non usare un vettore <0,0,0> direzione.

 

## <a name="light-position"></a>Posizione della luce

La posizione della luce viene [**descritta usando una struttura D3DVECTOR**](d3dvector.md) nel membro Position della struttura [**D3DLIGHT9.**](d3dlight9.md) Si presuppone che le coordinate x, y e z siano nello spazio mondiale. Le luci direzionali sono l'unico tipo di luce che non usa la proprietà position.

## <a name="light-range"></a>Intervallo di luce

La proprietà range di una luce determina la distanza, nello spazio del mondo, in cui le mesh in una scena non ricevono più la luce emessa da tale oggetto. Il membro Range contiene un valore a virgola mobile che rappresenta l'intervallo massimo della luce, nello spazio mondiale. Le luci direzionali non usano la proprietà range.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Luci e materiali](lights-and-materials.md)
</dt> </dl>

 

 
