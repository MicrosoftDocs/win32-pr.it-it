---
description: Direct3D consente a un'applicazione di aumentare il realismo delle sue scene eseguendo il rendering di oggetti poligonali segmentati, in particolare i caratteri, che hanno giunzioni perfettamente combinate.
ms.assetid: 190d5865-c45b-42ea-8a16-10a4f0bda743
title: Blending Geometry (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a19daa40f7d7d8193ae486640bc613dd7a666ec7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745383"
---
# <a name="geometry-blending-direct3d-9"></a>Blending Geometry (Direct3D 9)

Direct3D consente a un'applicazione di aumentare il realismo delle sue scene eseguendo il rendering di oggetti poligonali segmentati, in particolare i caratteri, che hanno giunzioni perfettamente combinate. Questi effetti sono spesso denominati Skin. Il sistema ottiene questo effetto applicando matrici di trasformazione globale aggiuntive a un singolo set di vertici per creare più risultati e quindi esegue una Blend lineare tra i vertici risultanti per creare un singolo set di geometria per il rendering. L'illustrazione seguente di una banana Mostra questo processo.

![illustrazione del processo di Unione di due oggetti con trama banana](images/geometry-blend.png)

L'illustrazione precedente Mostra come si può immaginare il processo di combinazione di geometria. In una singola chiamata di rendering, il sistema prende i vertici per la banana, li trasforma due volte, una volta senza modifiche e una volta con una semplice rotazione, e combina i risultati per creare una banana curva. Il sistema combina la posizione del vertice, nonché la normale dei vertici quando l'illuminazione è abilitata. Le applicazioni non sono limitate a due percorsi di fusione. Direct3D può unire la geometria tra le quattro matrici internazionali, inclusa la matrice mondiale standard, [**D3DTS \_ World**](d3dts-world.md).

> [!Note]
>
> Quando è abilitata l'illuminazione, le normali dei vertici vengono trasformate da una matrice di visualizzazione mondiale inversa corrispondente, ponderate in modo analogo ai calcoli della posizione del vertice. Il sistema normalizza il vettore normale risultante se lo \_ stato di rendering NORMALIZENORMALS di D3DRS è impostato su **true**.

 

Senza la fusione di geometria, spesso i modelli snodati dinamici vengono sottoposti a rendering in segmenti. Si consideri, ad esempio, un modello 3D del braccio umano. Nella visualizzazione più semplice, un ARM è costituito da due parti: il braccio superiore che si connette al corpo e il braccio inferiore, che si connette alla mano. I due sono connessi a gomito e il braccio inferiore ruota in corrispondenza di quel punto. Un'applicazione che esegue il rendering di un ARM potrebbe mantenere i dati dei vertici per il ARM superiore e inferiore, ognuno con una matrice di trasformazione globale separata. Questo aspetto è illustrato nell'esempio di codice seguente.


```
typedef struct _Arm
{
    VERTEX upper_arm_verts[200];
    D3DMATRIX matWorld_Upper;

    VERTEX lower_arm_verts[200];
    D3DMATRIX matWorld_Lower;
} ARM, *LPARM;

ARM MyArm; // This needs to be initialized.
```



Per eseguire il rendering del ARM, vengono effettuate due chiamate di rendering, come illustrato nel codice seguente.


```
// Render the upper arm.
d3dDevice->SetTransform( D3DTS_WORLD, &MyArm.matWorld_Upper );
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, numFaces );

// Render the lower arm, updating its world matrix to articulate
// the arm by pi/4 radians (45 degrees) at the elbow.
MyArm.matWorld_Lower = RotateMyArm(MyArm.matWorld, pi/4);
d3dDevice->SetTransform( D3DTS_WORLD, &MyArm.matWorld_Lower );
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, numFaces );
```



La figura seguente è una banana, modificata per usare questa tecnica.

![illustrazione di una banana con Blend senza fusione di geometria](images/noblend.png)

Le differenze tra la geometria mista e la geometria non mista sono ovvie. Questo esempio è piuttosto estremo. In un'applicazione reale, le giunzioni dei modelli segmentati sono progettate in modo che le giunzioni non siano evidenti. Tuttavia, le giunzioni sono visibili a volte, che presentano problemi costanti per le finestre di progettazione di modelli.

La fusione di geometria in Direct3D presenta un'alternativa allo scenario classico di modellazione segmentata. Tuttavia, la qualità visiva migliorata degli oggetti segmentati comporta il costo dei calcoli di fusione durante il rendering. Per ridurre al minimo l'impatto di queste operazioni aggiuntive, la pipeline di geometria Direct3D è ottimizzata per la geometria Blend con il minor sovraccarico possibile. Le applicazioni che usano in modo intelligente i servizi di Blend Geometry offerti da Direct3D possono migliorare il realismo dei loro caratteri evitando gravi ripercussioni sulle prestazioni.

## <a name="blending-transform-and-render-states"></a>Fusione degli Stati di trasformazione e rendering

Il metodo [**IDirect3DDevice9:: setransform**](/windows/desktop/api) riconosce le macro mondiali [**D3DTS \_**](d3dts-world.md) e [**D3DTS \_**](d3dts-worldn.md) , che corrispondono ai valori che possono essere definiti dalla macro [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) . Queste macro vengono usate per identificare le matrici tra le quali verrà fusa la geometria.

Il tipo enumerato [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) include lo \_ stato di rendering D3DRS VERTEXBLEND per abilitare e controllare la fusione geometrica. I valori validi per questo stato di rendering sono definiti dal tipo enumerato [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) . Se la fusione Geometry è abilitata, il formato del vertice deve includere il numero appropriato di pesi di fusione.

## <a name="blending-weights"></a>Pesi di fusione

Un peso di fusione, talvolta denominato peso beta, controlla la misura in cui una determinata matrice mondiale influisca su un vertice. I pesi di fusione sono valori a virgola mobile compresi tra 0,0 e 1,0, codificati in formato vertice, in cui il valore 0,0 indica che il vertice non è combinato con tale matrice e 1,0 indica che il vertice è interessato completamente dalla matrice.

I pesi per la fusione di geometria vengono codificati nel formato vertice, immediatamente dopo la posizione per ogni vertice, come descritto in [codici FVF a funzione fissa (Direct3D 9)](fixed-function-fvf-codes.md). Si comunica il numero di pesi di fusione nel formato vertice includendo una delle [costanti FVF](d3dfvf.md) nella descrizione del vertice fornita ai metodi di rendering.

Il sistema esegue una Blend lineare tra i risultati ponderati delle matrici di Blend. L'equazione seguente è la formula completa di fusione.

![equazione della fusione lineare, con matrici di trasformazione globale](images/vert-blend-formula.png)

Nell'equazione precedente, vBlend è il vertice di output, gli elementi v sono i vertici prodotti dalla matrice mondiale applicata ([**D3DTS \_ worldn**](d3dts-worldn.md)). Gli elementi W sono i valori di peso corrispondenti all'interno del formato del vertice. Un vertice con Blend tra n matrici può avere-1 Blend dei valori di peso, uno per ogni matrice di fusione, eccetto l'ultimo. Il sistema genera automaticamente il peso per l'ultima matrice globale in modo che la somma di tutti i pesi sia pari a 1,0, espressa in notazione Sigma. Questa formula può essere semplificata per ogni caso supportato da Direct3D, illustrato nelle equazioni seguenti.

![equazioni della fusione lineare per tre casi di fusione](images/vert-blend-formulas-simple.png)

Si tratta delle forme semplificate della formula di Blend completa per i due, tre e quattro case della matrice di Blend.

> [!Note]  
> Sebbene Direct3D includa descrittori FVF per definire i vertici contenenti fino a cinque pesi di fusione, solo tre possono essere utilizzati in questa versione di DirectX.

 

Informazioni aggiuntive sono contenute negli argomenti seguenti.

-   [Uso della combinazione di geometria (Direct3D 9)](using-geometry-blending.md)
-   [Fusione di vertici indicizzati (Direct3D 9)](indexed-vertex-blending.md)
-   [Interpolazione di vertici (Direct3D 9)](vertex-tweening.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pipeline Vertex](vertex-pipeline.md)
</dt> </dl>

 

 
