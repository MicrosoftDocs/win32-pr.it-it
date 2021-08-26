---
title: Piani di ritaglio utente nell'hardware di livello funzionalità 9
description: A partire da Windows 8, Microsoft High Level Shader Language (HLSL) supporta una sintassi che è possibile usare con l'API Microsoft Direct3D 11 per specificare i piani di ritaglio utente a livello di funzionalità 9 x e \_ successive.
ms.assetid: C51FB0E5-94C3-4E7F-AC33-E5F0F26EDC11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd6ffd624e688dbe5e3591e10ee5c005a9d4564dc5a536e9c89cfcee50067c2a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948971"
---
# <a name="user-clip-planes-on-feature-level-9-hardware"></a>Piani di ritaglio utente nell'hardware di livello funzionalità 9

A partire da Windows 8, Microsoft High Level Shader Language (HLSL) supporta una sintassi che è possibile usare con l'API Microsoft Direct3D 11 per specificare i piani di ritaglio utente a livello di funzionalità [9](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) x e \_ successive. È possibile usare questa sintassi dei piani di ritaglio per scrivere uno shader e quindi usare tale oggetto shader con l'API Direct3D 11 per l'esecuzione su tutti i livelli di funzionalità Direct3D.

-   [Background](#background-reading)
-   [Sintassi](#syntax)
-   [Creazione di piani di ritaglio nello spazio clip nel livello di funzionalità 9 e versioni successive](#creating-clip-planes-in-clip-space-on-feature-level-9-and-higher)
    -   [Lettura in background](#background-reading)
    -   [Livelli di funzionalità 10Level9](#10level9-feature-levels)
    -   [Calcolo matematico del piano di ritaglio](#clip-plane-math)
    -   [Ritaglio nello spazio di visualizzazione](#clipping-in-view-space)
    -   [Matrice di proiezione](#projection-matrix)
    -   [Piano di ritaglio dello spazio di ritaglio](#clip-space-clip-plane)
-   [Argomenti correlati](#related-topics)

## <a name="background"></a>Sfondo

È possibile accedere ai piani di ritaglio utente nell'API Microsoft Direct3D 9 tramite i metodi [**IDirect3DDevice9::SetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane) e [**IDirect3DDevice9::GetClipPlane.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getclipplane) In Microsoft Direct3D 10 e versioni successive è possibile accedere ai piani di ritaglio utente tramite la [semantica SV \_ ClipDistance.](dx-graphics-hlsl-semantics.md) Ma prima Windows 8, SV ClipDistance non era disponibile per l'hardware con livello di funzionalità 9 x nelle API \_ [](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) \_ Direct3D 10 o Direct3D 11. Quindi, prima Windows 8, l'unico modo per accedere ai piani di ritaglio utente con hardware con livello di funzionalità 9 x era tramite \_ l'API Direct3D 9. Le app Direct3D Windows Store non possono usare l'API Direct3D 9. Di seguito viene descritta la sintassi che è possibile usare per accedere ai piani di ritaglio utente tramite l'API Direct3D 11 a livello di funzionalità 9 \_ x e successive.

Le app usano i piani di ritaglio per definire un set di piani invisibili all'interno del mondo 3D che ritagliano (buttano) tutte le primitive disegnate. Windows disegna alcun pixel che si trova sul lato negativo dei piani di ritaglio. Le app possono quindi usare i piani di ritaglio per eseguire il rendering dei riflessi planari.

## <a name="syntax"></a>Sintassi

Usare questa sintassi per dichiarare i piani di ritaglio come attributi di funzione in una [dichiarazione di funzione](dx-graphics-hlsl-function-syntax.md). Ad esempio, qui si usa la sintassi su un frammento di vertex shader:

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

Questo esempio per un frammento vertex shader indica due piani di ritaglio. Indica che è necessario inserire il nuovo attributo **clipplanes** tra parentesi quadre immediatamente prima del valore restituito del vertex shader. Tra parentesi dopo l'attributo **clipplanes** viene fornito un elenco di fino a 6 costanti **float4** che definiscono i coefficienti del piano per ogni piano di clip attivo. L'esempio mostra anche che è necessario fare in modo che i coefficienti di ogni piano risiedano in un buffer costante.

> [!Note]  
> Non è disponibile alcuna sintassi per disabilitare dinamicamente un piano di ritaglio. È necessario ricompilare uno shader altrimenti identico senza alcun attributo **clipplanes** oppure l'app può impostare i coefficienti nel buffer costante su zero in modo che il piano non influisca più sulla geometria.

 

Questa sintassi è disponibile per qualsiasi destinazione vertex shader 4.0 o successiva, che include vs \_ 4 \_ 0 \_ livello \_ 9 \_ 1 e vs \_ 4 \_ 0 \_ livello \_ 9 \_ 3.

## <a name="creating-clip-planes-in-clip-space-on-feature-level-9-and-higher"></a>Creazione di piani di ritaglio nello spazio clip nel livello di funzionalità 9 e versioni successive

Di seguito viene illustrato come creare piani di ritaglio nello spazio di ritaglio a livello [di funzionalità](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 x e \_ versioni successive.

### <a name="background-reading"></a>Lettura in background

"Introduction to 3D Game Programming with DirectX 10" (Introduzione alla programmazione di giochi 3D con DirectX 10) di Frank D. Luna illustra lo sfondo matematico della grafica (capitoli 1, 2 e 3) necessari e i vari spazi e trasformazioni dello spazio che si verificano nel vertex shader (sezioni 5.6 e 5.8).

### <a name="10level9-feature-levels"></a>10Level9 - Livelli di funzionalità

In Direct3D 10 e versioni successive è possibile ritagliare qualsiasi spazio utile, spesso nello spazio del mondo o nello spazio di visualizzazione. Direct3D 9 usa tuttavia lo spazio di ritaglio, ovvero lo spazio di proiezione di divisione pre-prospettiva. I vettori sono nello spazio di ritaglio quando il vertex shader li passa alle fasi che seguono nella [pipeline grafica.](/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline)

Quando si scrive un'app Windows Store, è necessario usare i livelli di funzionalità 10Level9[(livello](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) di funzionalità 9 x) in modo che l'app possa essere eseguita sul livello di funzionalità 9 x e hardware \_ \_ superiore. Poiché l'app supporta il livello di funzionalità 9 x e versioni successive, è necessario usare anche la funzionalità comune di applicazione dei piani \_ di ritaglio nello spazio clip.

Quando si compila un vertex shader con un livello 4 0 9 1 o versione successiva, tale vertex shader può \_ usare \_ l'attributo \_ \_ \_ **clipplanes.** Un oggetto Direct3D 10 o versione successiva ha un prodotto punto del vertice generato che contiene ognuna delle **costanti globali float4** specificate nell'attributo . L'oggetto Direct3D 9 ha metadati sufficienti per determinare il runtime 10Level9 per eseguire le chiamate appropriate a [**IDirect3DDevice9::SetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane).

### <a name="clip-plane-math"></a>Calcolo matematico del piano di ritaglio

Un piano di ritaglio è definito da un vettore con 4 componenti. I primi tre componenti definiscono un vettore x, y, z che emana dall'origine nello spazio che si vuole ritagliare. Questo vettore implica un piano, perpendicolare al vettore e che attraversa l'origine. Windows tutti i pixel sul lato vettore del piano e ritaglia tutti i pixel dietro il piano. Il componente forth w fa tornare indietro il piano e fa sì che Windows clip meno (un valore w negativo Windows di ritagliare di più) lungo la linea vettoriale. Se i componenti x, y, z compongono un vettore di unità (normalizzato), w fa tornare indietro il piano w unità.

La matematica eseguita dall'unità di elaborazione grafica (GPU) per determinare il ritaglio è un semplice prodotto punto tra il vettore vertice (x, y, z, 1) e il vettore del piano di ritaglio. Questa operazione matematica crea una lunghezza di proiezione sul vettore del piano di ritaglio. Un prodotto punto negativo mostra il vertice sul lato ritagliato del piano.

### <a name="clipping-in-view-space"></a>Ritaglio nello spazio di visualizzazione

Ecco il vertice nello spazio di visualizzazione:

![vertice nello spazio di visualizzazione](images/vertex-clip.png)

Ecco il piano di ritaglio nello spazio di visualizzazione:

![Piano di ritaglio nello spazio di visualizzazione](images/clip-plane-view.png)

Ecco il prodotto punto del vertice e del piano di ritaglio nello spazio di visualizzazione:

ClipDistance = **v** · **C**  =  *v* ₓ *C* ₓ +*v*<sub>y</sub>*C*<sub>y</sub>  +  *v*<sub>z</sub>*C*<sub>z</sub>C  +  *w*<sub></sub>

Questa operazione matematica funziona per un oggetto Direct3D 10 o versione successiva, ma non per un oggetto Direct3D 9. Per Direct3D 9, è prima necessario passare alla trasformazione della proiezione in spazio clip.

### <a name="projection-matrix"></a>Matrice di proiezione

Una matrice di proiezione trasforma un vertice dallo spazio di visualizzazione (dove l'origine è l'occhio del visualizzatore, +x è a destra, +y è verso l'alto e +z è direttamente in avanti) nello spazio di ritaglio. La matrice di proiezione legge il vertice per il ritaglio hardware e la fase [di rasterizzazione.](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage) Ecco una matrice prospettica standard (altre proiezioni richiedono calcoli matematici diversi):

<dl> *rapporto r*   di larghezza/altezza della finestra  
*α'angolo*   di visualizzazione  
*f*   distanza dal visualizzatore al piano lontano  
*n*   distanza dal visualizzatore al piano vicino
</dl>![matrice di proiezione](images/projection-matrix.png)

La matrice successiva è una versione semplificata della matrice precedente. Viene illustrata la matrice semplificata in modo da poterla usare in un secondo momento nell'operazione di moltiplicazione della matrice.

![matrice di proiezione semplificata](images/projection-matrix2.png)

Ora si trasforma il vertice dello spazio di visualizzazione in uno spazio di ritaglio con una moltiplicazione di matrice:

![moltiplicazione matrice](images/matrix-multiply.png)

Nell'operazione di moltiplicazione della matrice, i componenti x e y sono solo leggermente modificati, ma i componenti z e w sono piuttosto mangled. Il piano di ritaglio non offrirà più ciò che si vuole.

### <a name="clip-space-clip-plane"></a>Piano di ritaglio dello spazio di ritaglio

In questo caso si vuole creare un piano clip space clip il cui prodotto punto con il vertice dello spazio clip offre lo stesso valore **di v · C** nella [sezione Ritaglio nello spazio di](#clipping-in-view-space) visualizzazione.

![piano di ritaglio](images/clip-space-clip-plane.png)

**v** · **C**  =  **v P** · **C**<sub>P</sub>

*v* ₓ *C* ₓ +*v*<sub>y</sub>*C*<sub>y</sub>  +  *v*<sub></sub>*z C*<sub>c</sub>  +  <sub>w</sub>  =  *v* ₓ *P* ₓ *C*<sub>Pₓ</sub>  + *v*<sub>y</sub>*P*<sub></sub>y *C*<sub>P <sub>y</sub></sub>  +  *v*<sub>A</sub><sub>y</sub>*C* P <sub><sub>z</sub></sub>  +  *BC* P <sub><sub>z</sub></sub>  +  *v*<sub>z</sub>*C* P <sub><sub>w</sub></sub>

Ora è possibile suddividere l'operazione matematica precedente per componente vertice in quattro equazioni separate:

![Componente x vertice del prodotto del piano di ritaglio](images/clip-space-clip-plane-equ1.png)

![Componente vertice y del prodotto del piano di ritaglio](images/clip-space-clip-plane-equ2.png)

![w componente vertice del prodotto del piano di ritaglio](images/clip-space-clip-plane-equ3.png)

![Componente vertice z del prodotto del piano di ritaglio](images/clip-space-clip-plane-equ4.png)

Il piano di ritaglio dello spazio di visualizzazione e la matrice di proiezione derivano e forniscono il piano di ritaglio dello spazio clip.

![Clip Space Clip Plane](images/clip-space-clip-plane-matrix.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida alla programmazione per HLSL](dx-graphics-hlsl-pguide.md)
</dt> <dt>

[Sintassi di dichiarazione di funzione](dx-graphics-hlsl-function-syntax.md)
</dt> </dl>

 

 