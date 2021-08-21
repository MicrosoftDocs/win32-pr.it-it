---
description: Direct3D consente a un'applicazione di aumentare il realistico delle scene tramite il rendering di oggetti poligonali segmentati, in particolare i caratteri, che hanno giunzioni uniformi.
ms.assetid: 190d5865-c45b-42ea-8a16-10a4f0bda743
title: Fusione geometry (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c71bb449b592c69ae2cf41487aef229718149eb4c1465d90f8b358d30458b69c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122177"
---
# <a name="geometry-blending-direct3d-9"></a>Fusione geometry (Direct3D 9)

Direct3D consente a un'applicazione di aumentare il realistico delle scene tramite il rendering di oggetti poligonali segmentati, in particolare i caratteri, che hanno giunzioni uniformi. Questi effetti sono spesso definiti skinning. Il sistema ottiene questo effetto applicando matrici di trasformazione del mondo aggiuntive a un singolo set di vertici per creare più risultati e quindi eseguendo una fusione lineare tra i vertici risultanti per creare un singolo set di geometria per il rendering. L'illustrazione seguente di una torta di banane mostra questo processo.

![Illustrazione del processo di fusione di due oggetti con trama di banano](images/geometry-blend.png)

La figura precedente mostra come si potrebbe immaginare il processo di fusione della geometria. In una singola chiamata di rendering, il sistema accetta i vertici per la banana, li trasforma due volte, una volta senza modifiche e una volta con una semplice rotazione, e combina i risultati per creare una banane chinta. Il sistema unisce la posizione del vertice e la normale del vertice quando l'illuminazione è abilitata. Le applicazioni non sono limitate a due percorsi di fusione. Direct3D può unire la geometria tra fino a quattro matrici del mondo, tra cui la matrice globale [**standard, D3DTS \_ WORLD.**](d3dts-world.md)

> [!Note]
>
> Quando l'illuminazione è abilitata, le normali dei vertici vengono trasformate da una matrice di visualizzazione globale inversa corrispondente, ponderata allo stesso modo dei calcoli della posizione dei vertici. Il sistema normalizza il vettore normale risultante se lo stato di rendering D3DRS \_ NORMALIZENORMALS è impostato su **TRUE.**

 

Senza la fusione geometrica, il rendering dei modelli articolati dinamici viene spesso eseguito in segmenti. Si consideri ad esempio un modello 3D del braccio umano. Nella visualizzazione più semplice, un braccio ha due parti: il braccio superiore che si connette al corpo e il braccio inferiore, che si connette alla mano. I due sono collegati al gomito e il braccio inferiore ruota in quel punto. Un'applicazione che esegue il rendering di un arm potrebbe conservare i dati dei vertici per il braccio superiore e inferiore, ognuno con una matrice di trasformazione globale separata. Questo aspetto è illustrato nell'esempio di codice seguente.


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



Per eseguire il rendering del arm, vengono effettuate due chiamate di rendering, come illustrato nel codice seguente.


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

![illustrazione di una blended banana senza fusione geometrica](images/noblend.png)

Le differenze tra la geometria blended e la geometria nonblended sono ovvie. Questo esempio è piuttosto estremo. In un'applicazione reale, le giunzioni dei modelli segmentati sono progettate in modo che le giunzioni non siano così ovvie. Tuttavia, le seams sono visibili a volte, il che presenta problemi costanti per i progettisti di modelli.

La fusione delle geometrie in Direct3D rappresenta un'alternativa allo scenario di modellazione segmentata classico. Tuttavia, la qualità visiva migliorata degli oggetti segmentati ha il costo dei calcoli di fusione durante il rendering. Per ridurre al minimo l'impatto di queste operazioni aggiuntive, la pipeline geometry Direct3D è ottimizzata per unire la geometria con il minor sovraccarico possibile. Le applicazioni che usano in modo intelligente i servizi di fusione della geometria offerti da Direct3D possono migliorare il realistico dei caratteri evitando gravi ripercussioni sulle prestazioni.

## <a name="blending-transform-and-render-states"></a>Fusione degli stati di trasformazione e rendering

Il metodo [**IDirect3DDevice9::SetTransform**](/windows/desktop/api) riconosce le macro [**D3DTS \_ WORLD**](d3dts-world.md) e [**D3DTS \_ WORLDn,**](d3dts-worldn.md) che corrispondono ai valori che possono essere definiti dalla macro [**D3DTS \_ WORLDMATRIX.**](d3dts-worldmatrix.md) Queste macro vengono usate per identificare le matrici tra cui verrà eseguita la fusione della geometria.

Il [**tipo enumerato D3DRENDERSTATETYPE**](./d3drenderstatetype.md) include lo stato di rendering VERTEXBLEND D3DRS per abilitare e controllare la \_ fusione della geometria. I valori validi per questo stato di rendering sono definiti dal [**tipo enumerato D3DVERTEXBLENDFLAGS.**](./d3dvertexblendflags.md) Se la fusione geometrica è abilitata, il formato dei vertici deve includere il numero appropriato di pesi di fusione.

## <a name="blending-weights"></a>Blending Weights

Un peso di fusione, talvolta denominato peso beta, controlla la misura in cui una determinata matrice globale influisce su un vertice. I pesi di fusione sono valori a virgola mobile che vanno da 0,0 a 1,0, codificati nel formato vertice, dove un valore pari a 0,0 indica che il vertice non viene sfumato con tale matrice e 1,0 indica che il vertice è interessato completamente dalla matrice.

I pesi di fusione della geometria vengono codificati nel formato vertice, che viene visualizzato immediatamente dopo la posizione per ogni vertice, come descritto in [Codici FVF a funzione fissa (Direct3D 9).](fixed-function-fvf-codes.md) È possibile comunicare il numero di pesi di fusione nel formato vertice includendo una delle costanti [FVF](d3dfvf.md) nella descrizione dei vertici fornita ai metodi di rendering.

Il sistema esegue una fusione lineare tra i risultati ponderati delle matrici di blend. L'equazione seguente è la formula di fusione completa.

![equazione della fusione lineare, usando matrici di trasformazione globale](images/vert-blend-formula.png)

Nell'equazione precedente vBlend è il vertice di output, gli elementi v sono i vertici prodotti dalla matrice globale applicata ([**D3DTS \_ WORLDn**](d3dts-worldn.md)). Gli elementi W sono i valori di peso corrispondenti all'interno del formato dei vertici. Un vertice misto tra n matrici può avere 1 valore di peso di fusione, uno per ogni matrice di fusione, ad eccezione dell'ultima. Il sistema genera automaticamente il peso per l'ultima matrice globale in modo che la somma di tutti i pesi sia 1,0, espressa nella notazione sigma qui. Questa formula può essere semplificata per ognuno dei case supportati da Direct3D, come illustrato nelle equazioni seguenti.

![equazioni di fusione lineare per tre case di fusione](images/vert-blend-formulas-simple.png)

Queste sono le forme semplificate della formula di fusione completa per i due, tre e quattro case della matrice di blend.

> [!Note]  
> Anche se Direct3D include descrittori FVF per definire vertici che contengono fino a cinque pesi di fusione, in questa versione di DirectX è possibile usare solo tre.

 

Altre informazioni sono contenute negli argomenti seguenti.

-   [Uso della fusione geometrica (Direct3D 9)](using-geometry-blending.md)
-   [Fusione di vertici indicizzati (Direct3D 9)](indexed-vertex-blending.md)
-   [Tweening vertice (Direct3D 9)](vertex-tweening.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pipeline vertice](vertex-pipeline.md)
</dt> </dl>

 

 
