---
description: Il supporto per gli sprite di punti in Direct3D 9 Abilita il rendering a prestazioni elevate di punti (sistemi particellari). Gli sprite punto sono generalizzazioni di punti generici che consentono di eseguire il rendering di forme arbitrarie come definito dalle trame.
ms.assetid: a9046c7e-779c-4f33-b8ff-f189da3dcfc5
title: Sprite punto (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c988a104eb65b5e2d7e56ff2444e8d422c422df2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521706"
---
# <a name="point-sprites-direct3d-9"></a>Sprite punto (Direct3D 9)

Il supporto per gli sprite di punti in Direct3D 9 Abilita il rendering a prestazioni elevate di punti (sistemi particellari). Gli sprite punto sono generalizzazioni di punti generici che consentono di eseguire il rendering di forme arbitrarie come definito dalle trame.

-   [Controlli di rendering primitivi Point](#point-primitive-rendering-controls)
-   [Calcoli delle dimensioni del punto](#point-size-computations)
-   [Rendering di punti](#point-rendering)

## <a name="point-primitive-rendering-controls"></a>Controlli di rendering primitivi Point

Direct3D 9 supporta parametri aggiuntivi per controllare il rendering degli sprite punto (primitive di punti). Questi parametri consentono che i punti siano di dimensioni variabili e che venga applicata una mappa di trama completa. La dimensione di ogni punto è determinata dalle dimensioni specificate dall'applicazione combinate con una funzione basata sulla distanza calcolata da Direct3D. L'applicazione può specificare le dimensioni dei punti in base al vertice o impostando D3DRS \_ POINTSIZE, che si applica ai punti senza una dimensione per ogni vertice. Le dimensioni del punto sono espresse in unità di spazio della fotocamera, ad eccezione del caso in cui l'applicazione superi i vertici FVF (Flexible Vertex Format) post-trasformazione. In questo caso, la funzione basata sulla distanza non viene applicata e le dimensioni del punto sono espresse in unità di pixel sulla destinazione di rendering.

Le coordinate di trama calcolate e usate quando i punti di rendering dipendono dall'impostazione di D3DRS \_ POINTSPRITEENABLE. Quando questo valore è impostato su **true**, le coordinate di trama sono impostate in modo che ogni punto visualizzi la trama completa. In generale, questo è utile solo quando i punti sono significativamente più grandi di un pixel. Quando D3DRS \_ POINTSPRITEENABLE è impostato su **false**, per l'intero punto viene utilizzata la coordinata di trama del vertice di ogni punto.

## <a name="point-size-computations"></a>Calcoli delle dimensioni del punto

La dimensione del punto è determinata da D3DRS \_ POINTSCALEENABLE. Se questo valore è impostato su **false**, le dimensioni del punto specificate dall'applicazione vengono utilizzate come dimensioni dello spazio dello schermo (post-trasformazione). I vertici passati a Direct3D nello spazio dello schermo non hanno dimensioni dei punti calcolate. le dimensioni del punto specificate vengono interpretate come dimensioni dello spazio dello schermo.

Se D3DRS \_ POINTSCALEENABLE è **true**, Direct3D calcola le dimensioni dei punti dello spazio dello schermo in base alla formula seguente. Le dimensioni del punto specificate dall'applicazione sono espresse in unità di spazio fotocamera.

S = VH \* s <sub>i</sub> \* sqrt (1/(A + B \* D ₑ + C \* (D ₑ ²)))

In questa formula, le dimensioni del punto di input, S <sub>i</sub>, sono per vertice o il valore dello stato di \_ rendering POINTSIZE di D3DRS. I fattori di scala punto, D3DRS \_ POINTSCALE \_ A, D3DRS \_ POINTSCALE \_ B e D3DRS \_ POINTSCALE \_ c, sono rappresentati dai punti A, B e c. L'altezza del viewport, V h, è il membro di altezza della struttura [**D3DVIEWPORT9**](d3dviewport9.md) che rappresenta il viewport. D ₑ, la distanza dall'occhio alla posizione (occhio all'origine) viene calcolata prendendo la posizione dello spazio degli occhi del punto (X ₑ, Y ₑ, Z ₑ) ed eseguendo l'operazione seguente.

D ₑ = sqrt (X ₑ ² + Y ₑ ² + Z ₑ ²)

Le dimensioni massime del punto, PM ₐ ₓ, vengono determinate prendendo il minore del membro MaxPointSize della struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) o lo stato di \_ rendering D3DRS POINTSIZE \_ max. La dimensione minima del punto, P<sub>min</sub>, è determinata dall'esecuzione di una query sul valore di D3DRS \_ POINTSIZE \_ min. Pertanto, le dimensioni finali del punto dello spazio dello schermo, S, vengono determinate nel modo seguente.

-   Se SS > PM ₐ ₓ, S = P m ₐ ₓ
-   Se S < P<sub>min</sub>, s = p <sub>min</sub>
-   In caso contrario, S = S

## <a name="point-rendering"></a>Rendering di punti

Un punto dello spazio dello schermo, P = (X, Y, Z, W), della dimensione dello spazio dello schermo S viene rasterizzato come un quadrilatero dei quattro vertici seguenti.

((X + S/2, Y + S/2, Z, W), (X + S/2, Y-S/2, Z, W), (X-S/2, Y-S/2, Z, W), (X-S/2, Y + S/2, Z, W))

Gli attributi di colore dei vertici vengono duplicati in ogni vertice. Pertanto, ogni punto viene sempre sottoposto a rendering con colori costanti.

L'assegnazione degli indici di trama è controllata dall' \_ impostazione dello stato di rendering POINTSPRITEENABLE di D3DRS. Se D3DRS \_ POINTSPRITEENABLE è impostato su **false**, le coordinate di trama dei vertici vengono duplicate in corrispondenza di ogni vertice. Se D3DRS \_ POINTSPRITEENABLE è impostato su **true**, le coordinate di trama in corrispondenza dei quattro vertici vengono impostate sui valori seguenti.

(0. F, 0. F), (0. F, 1. F), (1. F, 0. F), (1. F, 1. F)

Vedere il diagramma seguente.

![diagramma di un quadrato con vertici con etichetta per i valori delle coordinate (u, v) e (x, y)](images/spritepoint.png)

Quando il ritaglio è abilitato, i punti vengono ritagliati nel modo seguente. Se il vertice supera l'intervallo di valori di profondità, MinZ e MaxZ della struttura [**D3DVIEWPORT9**](d3dviewport9.md) , in cui deve essere eseguito il rendering di una scena, il punto esiste al di fuori della vista tronco e non viene sottoposto a rendering. Se il punto, prendendo in considerazione le dimensioni del punto, è completamente esterno al viewport in X e Y, il punto non viene sottoposto a rendering; viene eseguito il rendering dei punti rimanenti. È possibile che la posizione del punto si trovi all'esterno del viewport in X o Y e sia ancora parzialmente visibile.

I punti possono essere ritagliati o meno correttamente nei piani di ritaglio definiti dall'utente. Se D3DPMISCCAPS \_ CLIPPLANESCALEDPOINTS non è impostato nel membro PrimitiveMiscCaps della struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) , i punti vengono ritagliati a piani di ritaglio definiti dall'utente basati solo sulla posizione del vertice, ignorando le dimensioni del punto. In questo caso, viene eseguito il rendering completo dei punti ridimensionati quando la posizione del vertice si trova all'interno dei piani di ritaglio ed eliminati quando la posizione del vertice si trova all'esterno di un piano di ritaglio. Le applicazioni possono impedire potenziali artefatti aggiungendo una geometria del bordo per ritagliare i piani di dimensioni massime delle dimensioni massime del punto.

Se \_ viene impostato il bit D3DPMISCCAPS CLIPPLANESCALEDPOINTS, i punti ridimensionati vengono ritagliati correttamente in piani di ritaglio definiti dall'utente.

L'elaborazione dei vertici hardware può supportare o meno le dimensioni dei punti. Se, ad esempio, viene creato un dispositivo con D3DCREATE \_ hardware \_ VERTEXPROCESSING in un dispositivo HAL (Hardware Abstraction Layer) \_ , D3DDEVTYPE Hal, che ha il membro MaxPointSize della struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) impostato su 1,0 o 0,0, tutti i punti sono un singolo pixel. Per eseguire il rendering degli sprite del punto pixel minori di 1,0, è necessario usare i vertici FVF TL (trasformati e illuminati) o l'elaborazione dei vertici software (D3DCREATE \_ software \_ VERTEXPROCESSING), nel qual caso il runtime di Direct3D emula il rendering Point sprite.

Un dispositivo hardware che esegue l'elaborazione dei vertici e supporta punti sprite-MaxPointSize impostato su un valore superiore a 1,0 f-è necessario per eseguire il calcolo delle dimensioni per gli sprite non trasformati ed è necessario per impostare correttamente il POINTSIZE POINTSIZED3DRS per vertice o D3DRS \_ \_ per i vertici TL.

Per informazioni sulle regole di rendering per punti, linee e triangoli, vedere [regole di rasterizzazione (Direct3D 9)](rasterization-rules.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pipeline Vertex](vertex-pipeline.md)
</dt> </dl>

 

 



