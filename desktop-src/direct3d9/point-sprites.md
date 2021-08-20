---
description: Il supporto per gli sprite di punti in Direct3D 9 consente il rendering ad alte prestazioni dei punti (sistemi di particelle). Gli sprite dei punti sono generalizzazioni di punti generici che consentono il rendering di forme arbitrarie in base a quanto definito dalle trame.
ms.assetid: a9046c7e-779c-4f33-b8ff-f189da3dcfc5
title: Sprite punto (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90abd21207d9b3866ff93bd6c73069b655056f1c28811689762b0ce669183793
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118520470"
---
# <a name="point-sprites-direct3d-9"></a>Sprite punto (Direct3D 9)

Il supporto per gli sprite di punti in Direct3D 9 consente il rendering ad alte prestazioni dei punti (sistemi di particelle). Gli sprite dei punti sono generalizzazioni di punti generici che consentono il rendering di forme arbitrarie in base a quanto definito dalle trame.

-   [Controlli per il rendering di primitive di punti](#point-primitive-rendering-controls)
-   [Calcoli delle dimensioni dei punti](#point-size-computations)
-   [Rendering dei punti](#point-rendering)

## <a name="point-primitive-rendering-controls"></a>Controlli per il rendering di primitive di punti

Direct3D 9 supporta parametri aggiuntivi per controllare il rendering degli sprite punto (primitive di punti). Questi parametri consentono ai punti di avere dimensioni variabili e di applicare una mappa di trama completa. Le dimensioni di ogni punto sono determinate da una dimensione specificata dall'applicazione combinata con una funzione basata sulla distanza calcolata da Direct3D. L'applicazione può specificare le dimensioni in punti in base al vertice o impostando D3DRS POINTSIZE, che si applica ai punti senza dimensioni \_ per vertice. Le dimensioni del punto sono espresse in unità di spazio della fotocamera, ad eccezione del caso in cui l'applicazione passa vertici FVF (Flexible Vertex Format) post-trasformati. In questo caso, la funzione basata sulla distanza non viene applicata e le dimensioni del punto sono espresse in unità di pixel sulla destinazione di rendering.

Le coordinate della trama calcolate e usate quando i punti di rendering dipendono dall'impostazione di D3DRS \_ POINTSPRITEENABLE. Quando questo valore è impostato su **TRUE,** le coordinate della trama vengono impostate in modo che ogni punto visualizzi la trama completa. In generale, ciò è utile solo quando i punti sono significativamente più grandi di un pixel. Quando D3DRS POINTSPRITEENABLE è impostato su FALSE, per l'intero punto viene usata la coordinata della trama dei vertici \_ di ogni punto. 

## <a name="point-size-computations"></a>Calcoli delle dimensioni dei punti

La dimensione del punto è determinata da D3DRS \_ POINTSCALEENABLE. Se questo valore è impostato su **FALSE,** le dimensioni del punto specificate dall'applicazione vengono usate come dimensioni dello spazio dello schermo (post-trasformazione). I vertici passati a Direct3D nello spazio dello schermo non hanno dimensioni in punti calcolate; le dimensioni in punti specificate vengono interpretate come dimensioni dello spazio dello schermo.

Se D3DRS \_ POINTSCALEENABLE è **TRUE,** Direct3D calcola le dimensioni del punto dello spazio dello schermo in base alla formula seguente. Le dimensioni del punto specificate dall'applicazione sono espresse in unità di spazio della fotocamera.

S s = Vh \* S <sub>i</sub> \* sqrt(1/(A + B \* D ₑ + C ( D \* ₑ² )))

In questa formula, la dimensione del punto di input, S <sub>i</sub>, è per vertice o il valore dello stato di rendering D3DRS \_ POINTSIZE. I fattori di scala dei punti, D3DRS \_ POINTSCALE \_ A, D3DRS POINTSCALE B e \_ \_ D3DRS \_ POINTSCALE C, sono rappresentati dai punti \_ A, B e C. L'altezza del viewport, V h, è il membro Height della struttura [**D3DVIEWPORT9**](d3dviewport9.md) che rappresenta il viewport. D ₑ, la distanza dall'occhio alla posizione (l'occhio all'origine) viene calcolata prendendo la posizione dello spazio visivo del punto (Xₑ, Yₑ, Zₑ) ed eseguendo l'operazione seguente.

D ₑ = sqrt (Xₑ² + Y ₑ² + Z ₑ²)

La dimensione massima del punto, Pmₐₓ, viene determinata prendendo il valore più piccolo del membro MaxPointSize della struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) o dello stato di rendering D3DRS \_ POINTSIZE \_ MAX. La dimensione minima in punti, P<sub>min</sub>, viene determinata tramite query sul valore di D3DRS \_ POINTSIZE \_ MIN. Di conseguenza, la dimensione finale del punto dello spazio dello schermo, S, viene determinata nel modo seguente.

-   Se Ss > Pmₐₓ, S = P mₐₓ
-   se S < P<sub>min</sub>, quindi S = P <sub>min</sub>
-   In caso contrario, S = S s

## <a name="point-rendering"></a>Rendering dei punti

Un punto dello spazio dello schermo, P = ( X, Y, Z, W), di dimensioni dello spazio dello schermo S viene rasterizzato come quadrilatero dei quattro vertici seguenti.

(( X + S/2, Y + S/2, Z, W), ( X + S/2, Y - S/2, Z, W), ( X - S/2, Y- S/2, Z, W), ( X - S/2, Y + S/2, Z, W))

Gli attributi di colore dei vertici vengono duplicati in ogni vertice. pertanto ogni punto viene sempre sottoposto a rendering con colori costanti.

L'assegnazione degli indici di trama è controllata dall'impostazione dello stato di rendering D3DRS \_ POINTSPRITEENABLE. Se D3DRS POINTSPRITEENABLE è impostato su FALSE, le coordinate della trama dei vertici vengono \_ duplicate in corrispondenza di ogni vertice.  Se D3DRS POINTSPRITEENABLE è impostato su TRUE, le coordinate della trama nei quattro \_ vertici vengono impostate sui valori seguenti. 

(0.F, 0.F), (0.F, 1.F), (1.F, 0.F), (1.F, 1.F)

Vedere il diagramma seguente.

![diagramma di un quadrato con vertici etichettati per i valori delle coordinate (u,v) e (x,y)](images/spritepoint.png)

Quando il ritaglio è abilitato, i punti vengono ritagliati nel modo seguente. Se il vertice supera l'intervallo di valori di profondità, MinZ e MaxZ della struttura [**D3DVIEWPORT9,**](d3dviewport9.md) in cui deve essere eseguito il rendering di una scena, il punto esiste all'esterno del frustum di visualizzazione e non ne viene eseguito il rendering. Se il punto, tenendo conto delle dimensioni del punto, si trova completamente all'esterno del viewport in X e Y, non viene eseguito il rendering del punto; viene eseguito il rendering dei punti rimanenti. È possibile che la posizione del punto sia esterna al viewport in X o Y e sia ancora parzialmente visibile.

I punti possono o meno essere ritagliati correttamente ai piani di ritaglio definiti dall'utente. Se D3DPMISCCAPS CLIPPLANESCALEDPOINTS non è impostato nel membro \_ PrimitiveMiscCaps della struttura [**D3DCAPS9,**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) i punti vengono ritagliati ai piani di ritaglio definiti dall'utente in base solo alla posizione del vertice, ignorando le dimensioni del punto. In questo caso, il rendering dei punti ridimensionati viene eseguito completamente quando la posizione del vertice si trova all'interno dei piani di ritaglio e viene eliminato quando la posizione del vertice si trova all'esterno di un piano di ritaglio. Le applicazioni possono impedire potenziali artefatti aggiungendo una geometria del bordo ai piani di ritaglio grandi quanto le dimensioni massime del punto.

Se il bit D3DPMISCCAPS CLIPPLANESCALEDPOINTS è impostato, i punti ridimensionati vengono ritagliati correttamente ai piani di \_ ritaglio definiti dall'utente.

L'elaborazione dei vertici hardware può supportare o meno le dimensioni in punti. Ad esempio, se un dispositivo viene creato con D3DCREATE HARDWARE VERTEXPROCESSING in un dispositivo HAL (Hardware Abstraction Layer) con il membro MaxPointSize della struttura \_ \_ \_ [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) impostato su 1.0 o 0.0, tutti i punti sono un singolo pixel. Per eseguire il rendering degli sprite dei punti pixel minori di 1,0, è necessario usare vertici FVF TL (trasformati e accesi) o elaborazione dei vertici software (D3DCREATE SOFTWARE VERTEXPROCESSING), nel qual caso il tempo di esecuzione \_ \_ Direct3D emula il rendering dello sprite del punto.

Un dispositivo hardware che esegue l'elaborazione dei vertici e supporta gli sprite di punti - MaxPointSize impostato su un valore maggiore di 1,0f - è necessario per eseguire il calcolo delle dimensioni per gli sprite non trasformati ed è necessario impostare correttamente il valore per vertice o D3DRS \_ POINTSIZED3DRS POINTSIZE per \_ i vertici TL.

Per informazioni sulle regole di rendering per punti, linee e triangoli, vedere [Regole di rasterizzazione (Direct3D 9).](rasterization-rules.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pipeline dei vertici](vertex-pipeline.md)
</dt> </dl>

 

 



