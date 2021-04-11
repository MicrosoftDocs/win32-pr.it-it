---
description: Le proprietà della luce descrivono il tipo e il colore di una sorgente di luce.
ms.assetid: b39f1287-c67b-4cbb-b599-4a1b2f4981ac
title: Proprietà Light (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63239024109327e483ff93c2ee29fe42fc22c922
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124011"
---
# <a name="light-properties-direct3d-9"></a>Proprietà Light (Direct3D 9)

Le proprietà della luce descrivono il tipo e il colore di una sorgente di luce. A seconda del tipo di luce utilizzata, una luce può includere proprietà per l'attenuazione e l'intervallo oppure per gli effetti Spotlight. Tuttavia, non tutti i tipi di luci utilizzano tutte le proprietà. Direct3D usa la struttura [**D3DLIGHT9**](d3dlight9.md) per includere informazioni sulle proprietà di luce per tutti i tipi di fonti di luce. Questa sezione contiene informazioni per tutte le proprietà chiare. Le informazioni sono divise nei gruppi seguenti.

Le proprietà posizione, intervallo e attenuazione definiscono la posizione di una luce nello spazio globale e il modo in cui la luce che emette si comporta sulla distanza. Come per tutte le proprietà di luce usate in C++, queste sono contenute nella struttura [**D3DLIGHT9**](d3dlight9.md) di una luce.

-   [Attenuazione chiara](#light-attenuation)
-   [Colore chiaro](#light-color)
-   [Direzione luce](#light-direction)
-   [Posizione luce](#light-position)
-   [Intervallo chiaro](#light-range)

## <a name="light-attenuation"></a>Attenuazione chiara

Attenuazione controlla il modo in cui l'intensità di una luce diminuisce verso la distanza massima specificata dalla proprietà Range. Tre membri della struttura [**D3DLIGHT9**](d3dlight9.md) rappresentano un'attenuazione chiara: Attenuation0, Attenuation1 e Attenuation2. Questi membri contengono valori a virgola mobile compresi tra 0,0 e infinito, che controllano l'attenuazione di una luce. Alcune applicazioni impostano il membro Attenuation1 su 1,0 e gli altri a 0,0, ottenendo un'intensità chiara che cambia come 1/D, dove D è la distanza tra la sorgente di luce e il vertice. L'intensità massima della luce è nell'origine, diminuendo a 1/(intervallo chiaro) nell'intervallo della luce. In genere, un'applicazione imposta Attenuation0 su 0,0, Attenuation1 su un valore costante e Attenuation2 su 0,0.

È possibile combinare i valori di attenuazione per ottenere effetti di attenuazione più complessi. In alternativa, è possibile impostarli su valori non compresi nell'intervallo normale per creare effetti di attenuazione ancora più strani. Tuttavia, i valori di attenuazione negativi non sono consentiti. Vedere [attenuazione e fattore di Spotlight (Direct3D 9)](attenuation-and-spotlight-factor.md).

## <a name="light-color"></a>Colore chiaro

Le luci in Direct3D emettono tre colori che vengono usati in modo indipendente nei calcoli di illuminazione del sistema: un colore diffuso, un colore di ambiente e un colore speculare. Ogni viene incorporato dal modulo di illuminazione Direct3D, interagendo con una controparte dal materiale corrente, per produrre un colore finale usato per il rendering. Il colore diffuso interagisce con la proprietà Diffusion Reflector del materiale corrente, il colore speculare con la proprietà di Reflection speculare del materiale e così via. Per informazioni dettagliate sull'applicazione di questi colori a Direct3D, vedere [matematica dell'illuminazione (Direct3D 9)](mathematics-of-lighting.md).

In un'applicazione C++ la struttura [**D3DLIGHT9**](d3dlight9.md) include tre membri per questi colori: diffusa, ambiente e speculare, ognuno dei quali è una struttura [**D3DCOLORVALUE**](d3dcolorvalue.md) che definisce il colore emesso.

Il tipo di colore che si applica più spesso ai calcoli del sistema è il colore diffuso. Il colore più comune diffuso è bianco (R:1.0 G:1.0 B:1.0), ma è possibile creare i colori necessari per ottenere gli effetti desiderati. Ad esempio, è possibile utilizzare la luce rossa per un caminetto oppure utilizzare la luce verde per un segnale di traffico impostato su "Vai".

In genere, i componenti di colore chiaro vengono impostati su valori compresi tra 0,0 e 1,0, inclusi, ma questo non è un requisito. Ad esempio, è possibile impostare tutti i componenti su 2,0, creando una luce più luminosa del bianco. Questo tipo di impostazione può essere particolarmente utile quando si usano impostazioni di attenuazione diverse da Constant.

Si noti che, sebbene Direct3D usi i valori RGBA per le luci, il componente colore alfa non viene usato.

Per l'illuminazione vengono in genere usati i colori di materiale. Tuttavia, è possibile specificare che i colori del materiale-emissivo, ambient, diffuse e speculari devono essere sottoposti a override da colori dei vertici diffusi o speculari. Questa operazione viene eseguita chiamando [**SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) e impostando le variabili di stato del dispositivo elencate nella tabella seguente.



| Variabile di stato del dispositivo         | Significato                                       | Type                   | Predefinito          |
|-------------------------------|-----------------------------------------------|------------------------|------------------|
| \_AMBIENTMATERIALSOURCE D3DRS  | Definisce dove ottenere il colore del materiale di ambiente.  | D3DMATERIALCOLORSOURCE | \_Materiale D3DMCS |
| \_DIFFUSEMATERIALSOURCE D3DRS  | Definisce dove ottenere il colore del materiale diffuso.  | D3DMATERIALCOLORSOURCE | \_COLOR1 D3DMCS   |
| \_SPECULARMATERIALSOURCE D3DRS | Definisce dove ottenere il colore del materiale speculare. | D3DMATERIALCOLORSOURCE | \_Color2 D3DMCS   |
| \_EMISSIVEMATERIALSOURCE D3DRS | Definisce dove ottenere il colore del materiale emissivo. | D3DMATERIALCOLORSOURCE | \_Materiale D3DMCS |
| \_COLORVERTEX D3DRS            | Disabilita o Abilita l'uso dei colori vertici.     | BOOL                   | true             |



 

Il valore di Alpha/Transparency viene sempre visualizzato solo dal canale alfa del colore diffuso.

Il valore di nebbia viene sempre visualizzato solo dal canale alfa del colore speculare.

D3DMATERIALCOLORSOURCE può avere i valori seguenti.

-   \_Materiale D3DMCS: il colore del materiale viene usato come origine.
-   \_Il colore del vertice D3DMCS COLOR1-Diffusion viene usato come origine.
-   D3DMCS \_ color2-colore del vertice speculare viene usato come origine.

## <a name="light-direction"></a>Direzione luce

Una proprietà di direzione della luce determina la direzione di spostamento della luce emessa dall'oggetto, nello spazio globale. Direction viene usato solo da luci direzionali e Spotlight ed è descritto con un vettore.

Imposta la direzione della luce nel membro della direzione della struttura [**D3DLIGHT9**](d3dlight9.md) della luce. Il membro Direction è di tipo [**D3DVECTOR**](d3dvector.md). I vettori di direzione vengono descritti come Distanze da un'origine logica, indipendentemente dalla posizione della luce in una scena. Pertanto, un oggetto Spotlight che punta direttamente a una scena, lungo l'asse z positivo, ha un vettore di direzione di <0, 0, 1> indipendentemente dalla posizione in cui è definita. Analogamente, è possibile simulare la luce solare direttamente su una scena usando una luce direzionale la cui direzione è <0,-1, 0>. Ovviamente, non è necessario creare luci che splendano lungo gli assi delle coordinate. è possibile combinare e abbinare i valori per creare luci che risplendano a angoli più interessanti.

> [!Note]  
> Anche se non è necessario normalizzare il vettore di direzione di una luce, assicurarsi sempre che disponga di magnitude. In altre parole, non usare un <0, 0, 0> vettore di direzione.

 

## <a name="light-position"></a>Posizione luce

La posizione chiara viene descritta usando una struttura [**D3DVECTOR**](d3dvector.md) nel membro position della struttura [**D3DLIGHT9**](d3dlight9.md) . Si presuppone che le coordinate x, y e z si trovino nello spazio globale. Le luci direzionali sono l'unico tipo di luce che non usa la proprietà Position.

## <a name="light-range"></a>Intervallo chiaro

Una proprietà di intervallo della luce determina la distanza, nello spazio globale, in cui le mesh in una scena non ricevono più la luce emessa da tale oggetto. Il membro dell'intervallo contiene un valore a virgola mobile che rappresenta l'intervallo massimo della luce nello spazio globale. Le luci direzionali non usano la proprietà Range.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Luci e materiali](lights-and-materials.md)
</dt> </dl>

 

 
