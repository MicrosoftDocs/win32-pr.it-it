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
# <a name="user-clip-planes-on-feature-level-9-hardware"></a><span data-ttu-id="41d35-103">Piani di ritaglio utente su hardware di livello funzionalità 9</span><span class="sxs-lookup"><span data-stu-id="41d35-103">User clip planes on feature level 9 hardware</span></span>

<span data-ttu-id="41d35-104">A partire da Windows 8, Microsoft High Level Shader Language (HLSL) supporta una sintassi che è possibile usare con l'API Microsoft Direct3D 11 per specificare i piani di ritaglio utente sul [livello di funzionalità](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="41d35-104">Starting with Windows 8, Microsoft High Level Shader Language (HLSL) supports a syntax that you can use with the Microsoft Direct3D 11 API to specify user clip planes on [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x and higher.</span></span> <span data-ttu-id="41d35-105">È possibile usare questa sintassi di clip-Plane per scrivere uno shader e quindi usare tale oggetto shader con l'API Direct3D 11 per l'esecuzione in tutti i livelli di funzionalità Direct3D.</span><span class="sxs-lookup"><span data-stu-id="41d35-105">You can use this clip-planes syntax to write a shader, and then use that shader object with the Direct3D 11 API to run on all Direct3D feature levels.</span></span>

-   [<span data-ttu-id="41d35-106">Background</span><span class="sxs-lookup"><span data-stu-id="41d35-106">Background</span></span>](#background-reading)
-   [<span data-ttu-id="41d35-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="41d35-107">Syntax</span></span>](#syntax)
-   [<span data-ttu-id="41d35-108">Creazione di piani di ritaglio nello spazio di ritaglio sul livello di funzionalità 9 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="41d35-108">Creating clip planes in clip space on feature level 9 and higher</span></span>](#creating-clip-planes-in-clip-space-on-feature-level-9-and-higher)
    -   [<span data-ttu-id="41d35-109">Lettura in background</span><span class="sxs-lookup"><span data-stu-id="41d35-109">Background reading</span></span>](#background-reading)
    -   [<span data-ttu-id="41d35-110">livelli di funzionalità di 10Level9</span><span class="sxs-lookup"><span data-stu-id="41d35-110">10Level9 feature levels</span></span>](#10level9-feature-levels)
    -   [<span data-ttu-id="41d35-111">Ritagliare la matematica del piano</span><span class="sxs-lookup"><span data-stu-id="41d35-111">Clip plane math</span></span>](#clip-plane-math)
    -   [<span data-ttu-id="41d35-112">Ritaglio nello spazio di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="41d35-112">Clipping in view space</span></span>](#clipping-in-view-space)
    -   [<span data-ttu-id="41d35-113">Matrice di proiezione</span><span class="sxs-lookup"><span data-stu-id="41d35-113">Projection matrix</span></span>](#projection-matrix)
    -   [<span data-ttu-id="41d35-114">Taglia piano clip spazio</span><span class="sxs-lookup"><span data-stu-id="41d35-114">Clip space clip plane</span></span>](#clip-space-clip-plane)
-   [<span data-ttu-id="41d35-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="41d35-115">Related topics</span></span>](#related-topics)

## <a name="background"></a><span data-ttu-id="41d35-116">Sfondo</span><span class="sxs-lookup"><span data-stu-id="41d35-116">Background</span></span>

<span data-ttu-id="41d35-117">È possibile accedere ai piani di ritaglio utente nell'API Microsoft Direct3D 9 tramite i metodi [**IDirect3DDevice9:: SetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane) e [**IDirect3DDevice9:: GetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getclipplane) .</span><span class="sxs-lookup"><span data-stu-id="41d35-117">You can access user clip planes in the Microsoft Direct3D 9 API via [**IDirect3DDevice9::SetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane) and [**IDirect3DDevice9::GetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getclipplane) methods.</span></span> <span data-ttu-id="41d35-118">In Microsoft Direct3D 10 e versioni successive, è possibile accedere ai piani di ritaglio utente tramite la semantica [SV \_ Clipdistance](dx-graphics-hlsl-semantics.md) .</span><span class="sxs-lookup"><span data-stu-id="41d35-118">In Microsoft Direct3D 10 and later, you can access user clip planes through the [SV\_ClipDistance](dx-graphics-hlsl-semantics.md) semantic.</span></span> <span data-ttu-id="41d35-119">Ma prima di Windows 8, SV \_ Clipdistance non era disponibile per l'hardware di [livello funzionalità](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x nelle API Direct3D 10 o Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="41d35-119">But before Windows 8, SV\_ClipDistance was not available for [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x hardware in the Direct3D 10 or Direct3D 11 APIs.</span></span> <span data-ttu-id="41d35-120">Quindi, prima di Windows 8, l'unico modo per accedere ai piani di clip utente con hardware a livello di funzionalità 9 \_ x era tramite l'API Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="41d35-120">So, before Windows 8, the only way to access user clip planes with feature level 9\_x hardware was through the Direct3D 9 API.</span></span> <span data-ttu-id="41d35-121">Le app di Windows Store Direct3D non possono usare l'API Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="41d35-121">Direct3D Windows Store apps can't use the Direct3D 9 API.</span></span> <span data-ttu-id="41d35-122">Qui viene descritta la sintassi che è possibile usare per accedere ai piani di ritaglio utente tramite l'API Direct3D 11 a livello di funzionalità 9 \_ x e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="41d35-122">Here we describe the syntax that you can use to access user clip planes through the Direct3D 11 API on feature level 9\_x and higher.</span></span>

<span data-ttu-id="41d35-123">Le app usano i piani di ritaglio per definire un set di piani invisibili all'interno del mondo 3D che ritagliano (eliminate) tutte le primitive disegnate.</span><span class="sxs-lookup"><span data-stu-id="41d35-123">Apps use clip planes to define a set of invisible planes within the 3D world that clip (throw away) all drawn primitives.</span></span> <span data-ttu-id="41d35-124">Windows non rilascerà alcun pixel che si trova sul lato negativo di tutti i piani di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="41d35-124">Windows won't draw any pixel that is on the negative side of any clip planes.</span></span> <span data-ttu-id="41d35-125">Le app possono quindi usare i piani di ritaglio per il rendering di riflessi planari.</span><span class="sxs-lookup"><span data-stu-id="41d35-125">Apps can then use clip planes to render planar reflections.</span></span>

## <a name="syntax"></a><span data-ttu-id="41d35-126">Sintassi</span><span class="sxs-lookup"><span data-stu-id="41d35-126">Syntax</span></span>

<span data-ttu-id="41d35-127">Usare questa sintassi per dichiarare i piani di ritaglio come attributi di funzione in una [dichiarazione di funzione](dx-graphics-hlsl-function-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="41d35-127">Use this syntax to declare clip planes as function attributes in a [function declaration](dx-graphics-hlsl-function-syntax.md).</span></span> <span data-ttu-id="41d35-128">Qui, ad esempio, si usa la sintassi in un frammento vertex shader:</span><span class="sxs-lookup"><span data-stu-id="41d35-128">For example, here we use the syntax on a vertex shader fragment:</span></span>

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

<span data-ttu-id="41d35-129">Questo esempio per un frammento vertex shader denota due piani di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="41d35-129">This example for a vertex shader fragment denotes two clip planes.</span></span> <span data-ttu-id="41d35-130">Indica che è necessario inserire il nuovo attributo **clipplanes** tra parentesi quadre immediatamente prima del valore restituito del vertex shader.</span><span class="sxs-lookup"><span data-stu-id="41d35-130">It shows that you need to place the new **clipplanes** attribute within square brackets immediately before the return value of the vertex shader.</span></span> <span data-ttu-id="41d35-131">Tra parentesi dopo l'attributo **clipplanes** , viene fornito un elenco di un massimo di 6 costanti **float4** che definiscono i coefficienti dei piani per ogni piano di ritaglio attivo.</span><span class="sxs-lookup"><span data-stu-id="41d35-131">Within parentheses after the **clipplanes** attribute, you provide a list of up to 6 **float4** constants that define the plane coefficients for each active clip plane.</span></span> <span data-ttu-id="41d35-132">Nell'esempio viene inoltre illustrato che è necessario fare in modo che i coefficienti di ogni piano risiedano in un buffer costante.</span><span class="sxs-lookup"><span data-stu-id="41d35-132">The example also shows that you need to make the coefficients of each plane reside in a constant buffer.</span></span>

> [!Note]  
> <span data-ttu-id="41d35-133">Non sono disponibili sintassi per la disabilitazione dinamica di un piano di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="41d35-133">There is no syntax available to disable a clip plane dynamically.</span></span> <span data-ttu-id="41d35-134">È necessario ricompilare uno shader altrimenti identico senza attributo **clipplanes** oppure l'app può impostare i coefficienti nel buffer costante su zero, in modo che il piano non influisca più sulla geometria.</span><span class="sxs-lookup"><span data-stu-id="41d35-134">You must either recompile an otherwise identical shader with no **clipplanes** attribute, or your app can set the coefficients in your constant buffer to zero so that the plane no longer affects any geometry.</span></span>

 

<span data-ttu-id="41d35-135">Questa sintassi è disponibile per qualsiasi destinazione Vertex Shader 4,0 o successiva, che include vs \_ 4 \_ 0 \_ level \_ 9 \_ 1 e vs \_ 4 \_ 0 \_ level \_ 9 \_ 3.</span><span class="sxs-lookup"><span data-stu-id="41d35-135">This syntax is available for any 4.0 or later vertex shader target, which includes vs\_4\_0\_level\_9\_1 and vs\_4\_0\_level\_9\_3.</span></span>

## <a name="creating-clip-planes-in-clip-space-on-feature-level-9-and-higher"></a><span data-ttu-id="41d35-136">Creazione di piani di ritaglio nello spazio di ritaglio sul livello di funzionalità 9 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="41d35-136">Creating clip planes in clip space on feature level 9 and higher</span></span>

<span data-ttu-id="41d35-137">Qui viene illustrato come creare i piani di ritaglio nello spazio di ritaglio a [livello di funzionalità](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="41d35-137">Here we show how to create clip planes in clip space on [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x and higher.</span></span>

### <a name="background-reading"></a><span data-ttu-id="41d35-138">Lettura in background</span><span class="sxs-lookup"><span data-stu-id="41d35-138">Background reading</span></span>

<span data-ttu-id="41d35-139">"Introduzione alla programmazione di giochi 3D con DirectX 10" di Frank D. Luna spiega lo sfondo matematico della grafica (capitoli 1, 2 e 3) che ti servono e le varie trasformazioni di spazi e spazi che si verificano nel vertex shader (sezioni 5,6 e 5,8).</span><span class="sxs-lookup"><span data-stu-id="41d35-139">"Introduction to 3D Game Programming with DirectX 10" by Frank D. Luna explains the graphics math background (chapters 1, 2 and 3) you need, and the various spaces and space transformations that occur in the vertex shader (sections 5.6 and 5.8).</span></span>

### <a name="10level9-feature-levels"></a><span data-ttu-id="41d35-140">livelli di funzionalità di 10Level9</span><span class="sxs-lookup"><span data-stu-id="41d35-140">10Level9 feature levels</span></span>

<span data-ttu-id="41d35-141">In Direct3D 10 e versioni successive è possibile ritagliare in qualsiasi spazio che abbia senso, spesso nello spazio globale o nello spazio di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="41d35-141">In Direct3D 10 and later, you can clip in any space that makes sense, often in world space or view space.</span></span> <span data-ttu-id="41d35-142">Tuttavia, Direct3D 9 USA lo spazio di ritaglio, ovvero lo spazio di proiezione della divisione pre-prospettiva.</span><span class="sxs-lookup"><span data-stu-id="41d35-142">But Direct3D 9 uses clip space, which is pre perspective divide projection space.</span></span> <span data-ttu-id="41d35-143">I vettori si trovano nello spazio di ritaglio quando il vertex shader li passa alle fasi che seguono nella [pipeline grafica](/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline).</span><span class="sxs-lookup"><span data-stu-id="41d35-143">Vectors are in clip space when the vertex shader passes them to stages that follow in the [graphics pipeline](/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline).</span></span>

<span data-ttu-id="41d35-144">Quando si scrive un'app di Windows Store, è necessario usare i livelli di funzionalità di 10Level9 ([livello di funzionalità](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x), in modo che l'app possa essere eseguita su hardware a livello di funzionalità 9 \_ x e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="41d35-144">When you write a Windows Store app, you must use 10Level9 feature levels ([feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x) so the app can run on feature level 9\_x and higher hardware.</span></span> <span data-ttu-id="41d35-145">Poiché l'app supporta il livello di funzionalità 9 \_ x e versioni successive, è necessario usare anche la funzionalità comune di applicazione dei piani di ritaglio nello spazio di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="41d35-145">Because your app supports feature level 9\_x and higher, you must also use the common capability of applying clip planes in clip space.</span></span>

<span data-ttu-id="41d35-146">Quando si compila un vertex shader con Visual Studio \_ 4 \_ 0 \_ livello \_ 9 \_ 1 o versione successiva, tale vertex shader può usare l'attributo **clipplanes** .</span><span class="sxs-lookup"><span data-stu-id="41d35-146">When you compile a vertex shader with vs\_4\_0\_level\_9\_1 or later, that vertex shader can use the **clipplanes** attribute.</span></span> <span data-ttu-id="41d35-147">Un oggetto Direct3D 10 o versione successiva ha un prodotto punto del vertice emesso che contiene ciascuna delle costanti globali **float4** specificate nell'attributo.</span><span class="sxs-lookup"><span data-stu-id="41d35-147">A Direct3D 10 or later object has a dot product of the emitted vertex that contains each of the **float4** global constants specified in the attribute.</span></span> <span data-ttu-id="41d35-148">L'oggetto Direct3D 9 dispone di metadati sufficienti per fare in modo che il runtime 10Level9 riporti le chiamate appropriate a [**IDirect3DDevice9:: SetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane).</span><span class="sxs-lookup"><span data-stu-id="41d35-148">The Direct3D 9 object has enough meta data to cause the 10Level9 runtime to issue the appropriate calls to [**IDirect3DDevice9::SetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane).</span></span>

### <a name="clip-plane-math"></a><span data-ttu-id="41d35-149">Ritagliare la matematica del piano</span><span class="sxs-lookup"><span data-stu-id="41d35-149">Clip plane math</span></span>

<span data-ttu-id="41d35-150">Un piano di ritaglio viene definito da un vettore con 4 componenti.</span><span class="sxs-lookup"><span data-stu-id="41d35-150">A clip plane is defined by a vector with 4 components.</span></span> <span data-ttu-id="41d35-151">I primi tre componenti definiscono un vettore x, y, z che emana dall'origine nello spazio che si vuole ritagliare.</span><span class="sxs-lookup"><span data-stu-id="41d35-151">The first three components define an x, y, z vector that emanates from the origin in the space we want to clip.</span></span> <span data-ttu-id="41d35-152">Questo vettore implica un piano, perpendicolare al vettore e in esecuzione nell'origine.</span><span class="sxs-lookup"><span data-stu-id="41d35-152">This vector implies a plane, perpendicular to the vector and running through the origin.</span></span> <span data-ttu-id="41d35-153">Windows mantiene tutti i pixel sul lato vettoriale del piano e taglia tutti i pixel dietro il piano.</span><span class="sxs-lookup"><span data-stu-id="41d35-153">Windows keeps all pixels on the vector side of the plane and clips all pixels behind the plane.</span></span> <span data-ttu-id="41d35-154">Il componente Forth w esegue il push del piano e fa in modo che Windows ritaglia un valore minore (un w negativo causa la ritaglio di Windows) lungo la linea vettoriale.</span><span class="sxs-lookup"><span data-stu-id="41d35-154">The forth w component pushes the plane back and causes Windows to clip less (a negative w causes Windows to clip more) along the vector line.</span></span> <span data-ttu-id="41d35-155">Se i componenti x, y, z costituiscono un vettore di unità (normalizzato), w esegue il push delle unità w del piano.</span><span class="sxs-lookup"><span data-stu-id="41d35-155">If the x, y, z components compose a unit (normalized) vector, w pushes the plane w units back.</span></span>

<span data-ttu-id="41d35-156">Il matematico eseguito dall'unità di elaborazione grafica (GPU) per determinare il ritaglio è un semplice prodotto punto tra il vettore di vertice (x, y, z, 1) e il vettore del piano di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="41d35-156">The math that the graphics processing unit (GPU) performs to determine clipping is a simple dot product between the vertex vector (x, y, z, 1) and the clipping plane vector.</span></span> <span data-ttu-id="41d35-157">Questa operazione matematica crea una lunghezza di proiezione sul vettore del piano di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="41d35-157">This math operation creates a projection length on the clip plane vector.</span></span> <span data-ttu-id="41d35-158">Un prodotto a virgola negativo indica che il vertice si trova sul lato troncato del piano.</span><span class="sxs-lookup"><span data-stu-id="41d35-158">A negative dot product shows the vertex to be on the clipped side of the plane.</span></span>

### <a name="clipping-in-view-space"></a><span data-ttu-id="41d35-159">Ritaglio nello spazio di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="41d35-159">Clipping in view space</span></span>

<span data-ttu-id="41d35-160">Ecco il nostro vertice nello spazio di visualizzazione:</span><span class="sxs-lookup"><span data-stu-id="41d35-160">Here is our vertex in view space:</span></span>

![vertice nello spazio di visualizzazione](images/vertex-clip.png)

<span data-ttu-id="41d35-162">Ecco il nostro piano di ritaglio nello spazio di visualizzazione:</span><span class="sxs-lookup"><span data-stu-id="41d35-162">Here is our clip plane in view space:</span></span>

![ritaglio del piano nello spazio di visualizzazione](images/clip-plane-view.png)

<span data-ttu-id="41d35-164">Di seguito è riportato il prodotto scalare del piano vertice e della clip nello spazio di visualizzazione:</span><span class="sxs-lookup"><span data-stu-id="41d35-164">Here is the dot product of vertex and clip plane in view space:</span></span>

<span data-ttu-id="41d35-165">ClipDistance = **v** · **C**  =  *v* ₓ *c* ₓ +*v*<sub>y</sub>*c*<sub>y</sub>  +  *v*<sub>z</sub>*c*<sub>z</sub>  +  *C*<sub>w</sub></span><span class="sxs-lookup"><span data-stu-id="41d35-165">ClipDistance = **v** · **C** = *v* ₓ *C* ₓ +*v*<sub>y</sub>*C*<sub>y</sub> + *v*<sub>z</sub>*C*<sub>z</sub> + *C*<sub>w</sub></span></span>

<span data-ttu-id="41d35-166">Questa operazione matematica funziona per un oggetto Direct3D 10 o versione successiva ma non funzionerà per un oggetto Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="41d35-166">This math operation works for a Direct3D 10 or later object but won't work for a Direct3D 9 object.</span></span> <span data-ttu-id="41d35-167">Per Direct3D 9, dobbiamo prima di tutto passare attraverso la trasformazione proiezione nello spazio di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="41d35-167">For Direct3D 9, we must first get through our projection transform into clip space.</span></span>

### <a name="projection-matrix"></a><span data-ttu-id="41d35-168">Matrice di proiezione</span><span class="sxs-lookup"><span data-stu-id="41d35-168">Projection matrix</span></span>

<span data-ttu-id="41d35-169">Una matrice di proiezione trasforma un vertice dallo spazio di visualizzazione (dove l'origine è l'occhio del visualizzatore, + x è a destra, + y è attivo e + z è dritto) nello spazio di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="41d35-169">A projection matrix transforms a vertex from view space (where the origin is the viewer's eye, +x is to the right, +y is up, and +z is straight ahead) into clip space.</span></span> <span data-ttu-id="41d35-170">La matrice di proiezione legge il vertice per il ritaglio hardware e la [fase di rasterizzazione](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage).</span><span class="sxs-lookup"><span data-stu-id="41d35-170">The projection matrix readies the vertex for hardware clipping and the [rasterization stage](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage).</span></span> <span data-ttu-id="41d35-171">Ecco una matrice di prospettive standard (altre proiezioni richiedono una matematica diversa):</span><span class="sxs-lookup"><span data-stu-id="41d35-171">Here is a standard perspective matrix (other projections require different math):</span></span>

<dl> <span data-ttu-id="41d35-172">rapporto *r*   della larghezza/altezza della finestra</span><span class="sxs-lookup"><span data-stu-id="41d35-172">*r*  ratio of window width/height</span></span>  
<span data-ttu-id="41d35-173">   angolo di visualizzazione α</span><span class="sxs-lookup"><span data-stu-id="41d35-173">*α*  viewing angle</span></span>  
<span data-ttu-id="41d35-174">*f*   distanza dal visualizzatore al piano lontano</span><span class="sxs-lookup"><span data-stu-id="41d35-174">*f*  distance from the viewer to the far plane</span></span>  
<span data-ttu-id="41d35-175">*n*   distanza dal visualizzatore al piano vicino</span><span class="sxs-lookup"><span data-stu-id="41d35-175">*n*  distance from the viewer to the near plane</span></span>
</dl><span data-ttu-id="41d35-176">![matrice di proiezione](images/projection-matrix.png)</span><span class="sxs-lookup"><span data-stu-id="41d35-176">![projection matrix](images/projection-matrix.png)</span></span>

<span data-ttu-id="41d35-177">La matrice successiva è una versione semplificata della matrice precedente.</span><span class="sxs-lookup"><span data-stu-id="41d35-177">The next matrix is a simplified version of the previous matrix.</span></span> <span data-ttu-id="41d35-178">Viene visualizzata la matrice semplificata per poterla usare più avanti nell'operazione di moltiplicazione della matrice.</span><span class="sxs-lookup"><span data-stu-id="41d35-178">We show the matrix simplified so we can use it later in the matrix multiply operation.</span></span>

![matrice di proiezione semplificata](images/projection-matrix2.png)

<span data-ttu-id="41d35-180">A questo punto, il vertice dello spazio di visualizzazione viene trasformato nello spazio di ritaglio con una matrice Multiply:</span><span class="sxs-lookup"><span data-stu-id="41d35-180">Now we transform our view space vertex into clip space with a matrix multiply:</span></span>

![moltiplicazione matrice](images/matrix-multiply.png)

<span data-ttu-id="41d35-182">Nell'operazione di moltiplicazione della matrice, i componenti x e y sono solo leggermente regolati, ma i componenti z e w sono piuttosto alterati.</span><span class="sxs-lookup"><span data-stu-id="41d35-182">In our matrix multiply operation, our x and y components are only slightly adjusted, but our z and w components are quite mangled.</span></span> <span data-ttu-id="41d35-183">Il nostro piano di ritaglio non ci fornirà ciò che vogliamo.</span><span class="sxs-lookup"><span data-stu-id="41d35-183">Our clip plane won't give us what we want any more.</span></span>

### <a name="clip-space-clip-plane"></a><span data-ttu-id="41d35-184">Taglia piano clip spazio</span><span class="sxs-lookup"><span data-stu-id="41d35-184">Clip space clip plane</span></span>

<span data-ttu-id="41d35-185">Qui si vuole creare un piano di ritaglio dello spazio di ritaglio il cui prodotto a punti con il vertice dello spazio di ritaglio restituisce lo stesso valore di **v · C** nel [ritaglio nella sezione spazio di visualizzazione](#clipping-in-view-space) .</span><span class="sxs-lookup"><span data-stu-id="41d35-185">Here we want to create a clip space clip plane whose dot product with our clip space vertex gives us the same value as **v · C** in the [Clipping in view space](#clipping-in-view-space) section.</span></span>

![taglia piano](images/clip-space-clip-plane.png)

<span data-ttu-id="41d35-187">**v** · **C**  =  **v P** · **C**<sub>P</sub></span><span class="sxs-lookup"><span data-stu-id="41d35-187">**v** · **C** = **v P** · **C**<sub>P</sub></span></span>

<span data-ttu-id="41d35-188">*v* ₓ *c* ₓ +*v*<sub>y</sub>*c*<sub>y</sub>  +  *v*<sub>z</sub>*c*<sub>z</sub>  +  *c*<sub>w</sub>  =  *v* ₓ *p* ₓ *C*<sub>p ₓ</sub>  + *v*<sub>y</sub>*p*<sub>y</sub>*c*<sub>p <sub></sub></sub>y  +  *v*<sub>z</sub>*A*<sub>y</sub>*c*<sub>p <sub></sub></sub>z  +  *BC*<sub>p <sub>z</sub></sub>  +  *v*<sub>z</sub>*c*<sub>p <sub>w</sub></sub></span><span class="sxs-lookup"><span data-stu-id="41d35-188">*v* ₓ *C* ₓ +*v*<sub>y</sub>*C*<sub>y</sub> + *v*<sub>z</sub>*C*<sub>z</sub> + *C*<sub>w</sub> = *v* ₓ *P* ₓ *C*<sub>Pₓ</sub> +*v*<sub>y</sub>*P*<sub>y</sub>*C*<sub>P <sub>y</sub></sub> + *v*<sub>z</sub>*A*<sub>y</sub>*C*<sub>P <sub>z</sub></sub> + *BC*<sub>P <sub>z</sub></sub> + *v*<sub>z</sub>*C*<sub>P<sub>w</sub></sub></span></span>

<span data-ttu-id="41d35-189">Ora è possibile suddividere l'operazione matematica precedente per componente Vertex in quattro equazioni separate:</span><span class="sxs-lookup"><span data-stu-id="41d35-189">Now we can break the preceding math operation up by vertex component into four separate equations:</span></span>

![componente x vertice del prodotto del piano di ritaglio](images/clip-space-clip-plane-equ1.png)

![componente vertice y del prodotto del piano di ritaglio](images/clip-space-clip-plane-equ2.png)

![componente Vertex w del prodotto del piano di ritaglio](images/clip-space-clip-plane-equ3.png)

![componente vertice z del prodotto del piano di ritaglio](images/clip-space-clip-plane-equ4.png)

<span data-ttu-id="41d35-194">Il piano di ritaglio dello spazio di visualizzazione e la matrice di proiezione derivano e forniscono il piano di ritaglio dello spazio di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="41d35-194">Our view space clip plane and our projection matrix derive and give us our clip space clip plane.</span></span>

![taglia piano clip spazio](images/clip-space-clip-plane-matrix.png)

## <a name="related-topics"></a><span data-ttu-id="41d35-196">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="41d35-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41d35-197">Guida alla programmazione per HLSL</span><span class="sxs-lookup"><span data-stu-id="41d35-197">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> <dt>

[<span data-ttu-id="41d35-198">Sintassi di dichiarazione di funzione</span><span class="sxs-lookup"><span data-stu-id="41d35-198">Function Declaration Syntax</span></span>](dx-graphics-hlsl-function-syntax.md)
</dt> </dl>

 

 