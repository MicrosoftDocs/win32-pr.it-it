---
title: Piani di ritaglio utente su hardware di livello funzionalità 9
description: A partire da Windows 8, Microsoft High Level Shader Language (HLSL) supporta una sintassi che è possibile usare con l'API Microsoft Direct3D 11 per specificare i piani di ritaglio utente sul livello di funzionalità 9 \_ x e versioni successive.
ms.assetid: C51FB0E5-94C3-4E7F-AC33-E5F0F26EDC11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 968831ca39f2501a44b00f202fd8dfda1f92d1e7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338055"
---
# <a name="user-clip-planes-on-feature-level-9-hardware"></a>Piani di ritaglio utente su hardware di livello funzionalità 9

A partire da Windows 8, Microsoft High Level Shader Language (HLSL) supporta una sintassi che è possibile usare con l'API Microsoft Direct3D 11 per specificare i piani di ritaglio utente sul [livello di funzionalità](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x e versioni successive. È possibile usare questa sintassi di clip-Plane per scrivere uno shader e quindi usare tale oggetto shader con l'API Direct3D 11 per l'esecuzione in tutti i livelli di funzionalità Direct3D.

-   [Background](#background-reading)
-   [Sintassi](#syntax)
-   [Creazione di piani di ritaglio nello spazio di ritaglio sul livello di funzionalità 9 e versioni successive](#creating-clip-planes-in-clip-space-on-feature-level-9-and-higher)
    -   [Lettura in background](#background-reading)
    -   [livelli di funzionalità di 10Level9](#10level9-feature-levels)
    -   [Ritagliare la matematica del piano](#clip-plane-math)
    -   [Ritaglio nello spazio di visualizzazione](#clipping-in-view-space)
    -   [Matrice di proiezione](#projection-matrix)
    -   [Taglia piano clip spazio](#clip-space-clip-plane)
-   [Argomenti correlati](#related-topics)

## <a name="background"></a>Sfondo

È possibile accedere ai piani di ritaglio utente nell'API Microsoft Direct3D 9 tramite i metodi [**IDirect3DDevice9:: SetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane) e [**IDirect3DDevice9:: GetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getclipplane) . In Microsoft Direct3D 10 e versioni successive, è possibile accedere ai piani di ritaglio utente tramite la semantica [SV \_ Clipdistance](dx-graphics-hlsl-semantics.md) . Ma prima di Windows 8, SV \_ Clipdistance non era disponibile per l'hardware di [livello funzionalità](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x nelle API Direct3D 10 o Direct3D 11. Quindi, prima di Windows 8, l'unico modo per accedere ai piani di clip utente con hardware a livello di funzionalità 9 \_ x era tramite l'API Direct3D 9. Le app di Windows Store Direct3D non possono usare l'API Direct3D 9. Qui viene descritta la sintassi che è possibile usare per accedere ai piani di ritaglio utente tramite l'API Direct3D 11 a livello di funzionalità 9 \_ x e versioni successive.

Le app usano i piani di ritaglio per definire un set di piani invisibili all'interno del mondo 3D che ritagliano (eliminate) tutte le primitive disegnate. Windows non rilascerà alcun pixel che si trova sul lato negativo di tutti i piani di ritaglio. Le app possono quindi usare i piani di ritaglio per il rendering di riflessi planari.

## <a name="syntax"></a>Sintassi

Usare questa sintassi per dichiarare i piani di ritaglio come attributi di funzione in una [dichiarazione di funzione](dx-graphics-hlsl-function-syntax.md). Qui, ad esempio, si usa la sintassi in un frammento vertex shader:

``` syntax
cbuffer ClipPlaneConstantBuffer 
{
       float4 clipPlane1;
       float4 clipPlane2;
};

[clipplanes(clipPlane1,clipPlane2)]
VertexShaderOutput main(VertexShaderInput input)
{
       // the rest of the vertex shader doesn't refer to the clip plane
 
       …
 
       return output;
}
```

Questo esempio per un frammento vertex shader denota due piani di ritaglio. Indica che è necessario inserire il nuovo attributo **clipplanes** tra parentesi quadre immediatamente prima del valore restituito del vertex shader. Tra parentesi dopo l'attributo **clipplanes** , viene fornito un elenco di un massimo di 6 costanti **float4** che definiscono i coefficienti dei piani per ogni piano di ritaglio attivo. Nell'esempio viene inoltre illustrato che è necessario fare in modo che i coefficienti di ogni piano risiedano in un buffer costante.

> [!Note]  
> Non sono disponibili sintassi per la disabilitazione dinamica di un piano di ritaglio. È necessario ricompilare uno shader altrimenti identico senza attributo **clipplanes** oppure l'app può impostare i coefficienti nel buffer costante su zero, in modo che il piano non influisca più sulla geometria.

 

Questa sintassi è disponibile per qualsiasi destinazione Vertex Shader 4,0 o successiva, che include vs \_ 4 \_ 0 \_ level \_ 9 \_ 1 e vs \_ 4 \_ 0 \_ level \_ 9 \_ 3.

## <a name="creating-clip-planes-in-clip-space-on-feature-level-9-and-higher"></a>Creazione di piani di ritaglio nello spazio di ritaglio sul livello di funzionalità 9 e versioni successive

Qui viene illustrato come creare i piani di ritaglio nello spazio di ritaglio a [livello di funzionalità](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x e versioni successive.

### <a name="background-reading"></a>Lettura in background

"Introduzione alla programmazione di giochi 3D con DirectX 10" di Frank D. Luna spiega lo sfondo matematico della grafica (capitoli 1, 2 e 3) che ti servono e le varie trasformazioni di spazi e spazi che si verificano nel vertex shader (sezioni 5,6 e 5,8).

### <a name="10level9-feature-levels"></a>livelli di funzionalità di 10Level9

In Direct3D 10 e versioni successive è possibile ritagliare in qualsiasi spazio che abbia senso, spesso nello spazio globale o nello spazio di visualizzazione. Tuttavia, Direct3D 9 USA lo spazio di ritaglio, ovvero lo spazio di proiezione della divisione pre-prospettiva. I vettori si trovano nello spazio di ritaglio quando il vertex shader li passa alle fasi che seguono nella [pipeline grafica](/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline).

Quando si scrive un'app di Windows Store, è necessario usare i livelli di funzionalità di 10Level9 ([livello di funzionalità](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x), in modo che l'app possa essere eseguita su hardware a livello di funzionalità 9 \_ x e versioni successive. Poiché l'app supporta il livello di funzionalità 9 \_ x e versioni successive, è necessario usare anche la funzionalità comune di applicazione dei piani di ritaglio nello spazio di ritaglio.

Quando si compila un vertex shader con Visual Studio \_ 4 \_ 0 \_ livello \_ 9 \_ 1 o versione successiva, tale vertex shader può usare l'attributo **clipplanes** . Un oggetto Direct3D 10 o versione successiva ha un prodotto punto del vertice emesso che contiene ciascuna delle costanti globali **float4** specificate nell'attributo. L'oggetto Direct3D 9 dispone di metadati sufficienti per fare in modo che il runtime 10Level9 riporti le chiamate appropriate a [**IDirect3DDevice9:: SetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane).

### <a name="clip-plane-math"></a>Ritagliare la matematica del piano

Un piano di ritaglio viene definito da un vettore con 4 componenti. I primi tre componenti definiscono un vettore x, y, z che emana dall'origine nello spazio che si vuole ritagliare. Questo vettore implica un piano, perpendicolare al vettore e in esecuzione nell'origine. Windows mantiene tutti i pixel sul lato vettoriale del piano e taglia tutti i pixel dietro il piano. Il componente Forth w esegue il push del piano e fa in modo che Windows ritaglia un valore minore (un w negativo causa la ritaglio di Windows) lungo la linea vettoriale. Se i componenti x, y, z costituiscono un vettore di unità (normalizzato), w esegue il push delle unità w del piano.

Il matematico eseguito dall'unità di elaborazione grafica (GPU) per determinare il ritaglio è un semplice prodotto punto tra il vettore di vertice (x, y, z, 1) e il vettore del piano di ritaglio. Questa operazione matematica crea una lunghezza di proiezione sul vettore del piano di ritaglio. Un prodotto a virgola negativo indica che il vertice si trova sul lato troncato del piano.

### <a name="clipping-in-view-space"></a>Ritaglio nello spazio di visualizzazione

Ecco il nostro vertice nello spazio di visualizzazione:

![vertice nello spazio di visualizzazione](images/vertex-clip.png)

Ecco il nostro piano di ritaglio nello spazio di visualizzazione:

![ritaglio del piano nello spazio di visualizzazione](images/clip-plane-view.png)

Di seguito è riportato il prodotto scalare del piano vertice e della clip nello spazio di visualizzazione:

ClipDistance = **v** · **C**  =  *v* ₓ *c* ₓ +*v*<sub>y</sub>*c*<sub>y</sub>  +  *v*<sub>z</sub>*c*<sub>z</sub>  +  *C*<sub>w</sub>

Questa operazione matematica funziona per un oggetto Direct3D 10 o versione successiva ma non funzionerà per un oggetto Direct3D 9. Per Direct3D 9, dobbiamo prima di tutto passare attraverso la trasformazione proiezione nello spazio di ritaglio.

### <a name="projection-matrix"></a>Matrice di proiezione

Una matrice di proiezione trasforma un vertice dallo spazio di visualizzazione (dove l'origine è l'occhio del visualizzatore, + x è a destra, + y è attivo e + z è dritto) nello spazio di ritaglio. La matrice di proiezione legge il vertice per il ritaglio hardware e la [fase di rasterizzazione](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage). Ecco una matrice di prospettive standard (altre proiezioni richiedono una matematica diversa):

<dl> rapporto *r*   della larghezza/altezza della finestra  
   angolo di visualizzazione α  
*f*   distanza dal visualizzatore al piano lontano  
*n*   distanza dal visualizzatore al piano vicino
</dl>![matrice di proiezione](images/projection-matrix.png)

La matrice successiva è una versione semplificata della matrice precedente. Viene visualizzata la matrice semplificata per poterla usare più avanti nell'operazione di moltiplicazione della matrice.

![matrice di proiezione semplificata](images/projection-matrix2.png)

A questo punto, il vertice dello spazio di visualizzazione viene trasformato nello spazio di ritaglio con una matrice Multiply:

![moltiplicazione matrice](images/matrix-multiply.png)

Nell'operazione di moltiplicazione della matrice, i componenti x e y sono solo leggermente regolati, ma i componenti z e w sono piuttosto alterati. Il nostro piano di ritaglio non ci fornirà ciò che vogliamo.

### <a name="clip-space-clip-plane"></a>Taglia piano clip spazio

Qui si vuole creare un piano di ritaglio dello spazio di ritaglio il cui prodotto a punti con il vertice dello spazio di ritaglio restituisce lo stesso valore di **v · C** nel [ritaglio nella sezione spazio di visualizzazione](#clipping-in-view-space) .

![taglia piano](images/clip-space-clip-plane.png)

**v** · **C**  =  **v P** · **C**<sub>P</sub>

*v* ₓ *c* ₓ +*v*<sub>y</sub>*c*<sub>y</sub>  +  *v*<sub>z</sub>*c*<sub>z</sub>  +  *c*<sub>w</sub>  =  *v* ₓ *p* ₓ *C*<sub>p ₓ</sub>  + *v*<sub>y</sub>*p*<sub>y</sub>*c*<sub>p <sub></sub></sub>y  +  *v*<sub>z</sub>*A*<sub>y</sub>*c*<sub>p <sub></sub></sub>z  +  *BC*<sub>p <sub>z</sub></sub>  +  *v*<sub>z</sub>*c*<sub>p <sub>w</sub></sub>

Ora è possibile suddividere l'operazione matematica precedente per componente Vertex in quattro equazioni separate:

![componente x vertice del prodotto del piano di ritaglio](images/clip-space-clip-plane-equ1.png)

![componente vertice y del prodotto del piano di ritaglio](images/clip-space-clip-plane-equ2.png)

![componente Vertex w del prodotto del piano di ritaglio](images/clip-space-clip-plane-equ3.png)

![componente vertice z del prodotto del piano di ritaglio](images/clip-space-clip-plane-equ4.png)

Il piano di ritaglio dello spazio di visualizzazione e la matrice di proiezione derivano e forniscono il piano di ritaglio dello spazio di ritaglio.

![taglia piano clip spazio](images/clip-space-clip-plane-matrix.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida alla programmazione per HLSL](dx-graphics-hlsl-pguide.md)
</dt> <dt>

[Sintassi di dichiarazione di funzione](dx-graphics-hlsl-function-syntax.md)
</dt> </dl>

 

 