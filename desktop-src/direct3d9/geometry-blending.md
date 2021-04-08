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
# <a name="geometry-blending-direct3d-9"></a><span data-ttu-id="b70e4-103">Blending Geometry (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b70e4-103">Geometry Blending (Direct3D 9)</span></span>

<span data-ttu-id="b70e4-104">Direct3D consente a un'applicazione di aumentare il realismo delle sue scene eseguendo il rendering di oggetti poligonali segmentati, in particolare i caratteri, che hanno giunzioni perfettamente combinate.</span><span class="sxs-lookup"><span data-stu-id="b70e4-104">Direct3D enables an application to increase the realism of its scenes by rendering segmented polygonal objects - especially characters - that have smoothly blended joints.</span></span> <span data-ttu-id="b70e4-105">Questi effetti sono spesso denominati Skin.</span><span class="sxs-lookup"><span data-stu-id="b70e4-105">These effects are often referred to as skinning.</span></span> <span data-ttu-id="b70e4-106">Il sistema ottiene questo effetto applicando matrici di trasformazione globale aggiuntive a un singolo set di vertici per creare più risultati e quindi esegue una Blend lineare tra i vertici risultanti per creare un singolo set di geometria per il rendering.</span><span class="sxs-lookup"><span data-stu-id="b70e4-106">The system achieves this effect by applying additional world transformation matrices to a single set of vertices to create multiple results, and then performing a linear blend between the resultant vertices to create a single set of geometry for rendering.</span></span> <span data-ttu-id="b70e4-107">L'illustrazione seguente di una banana Mostra questo processo.</span><span class="sxs-lookup"><span data-stu-id="b70e4-107">The following illustration of a banana shows this process.</span></span>

![illustrazione del processo di Unione di due oggetti con trama banana](images/geometry-blend.png)

<span data-ttu-id="b70e4-109">L'illustrazione precedente Mostra come si può immaginare il processo di combinazione di geometria.</span><span class="sxs-lookup"><span data-stu-id="b70e4-109">The preceding illustration shows how you might imagine the geometry-blending process.</span></span> <span data-ttu-id="b70e4-110">In una singola chiamata di rendering, il sistema prende i vertici per la banana, li trasforma due volte, una volta senza modifiche e una volta con una semplice rotazione, e combina i risultati per creare una banana curva.</span><span class="sxs-lookup"><span data-stu-id="b70e4-110">In a single rendering call, the system takes the vertices for the banana, transforms them twice - once without modification, and once with a simple rotation - and blends the results to create a bent banana.</span></span> <span data-ttu-id="b70e4-111">Il sistema combina la posizione del vertice, nonché la normale dei vertici quando l'illuminazione è abilitata.</span><span class="sxs-lookup"><span data-stu-id="b70e4-111">The system blends the vertex position, as well as the vertex normal when lighting is enabled.</span></span> <span data-ttu-id="b70e4-112">Le applicazioni non sono limitate a due percorsi di fusione. Direct3D può unire la geometria tra le quattro matrici internazionali, inclusa la matrice mondiale standard, [**D3DTS \_ World**](d3dts-world.md).</span><span class="sxs-lookup"><span data-stu-id="b70e4-112">Applications are not limited to two blending paths; Direct3D can blend geometry between as many as four world matrices, including the standard world matrix, [**D3DTS\_WORLD**](d3dts-world.md).</span></span>

> [!Note]
>
> <span data-ttu-id="b70e4-113">Quando è abilitata l'illuminazione, le normali dei vertici vengono trasformate da una matrice di visualizzazione mondiale inversa corrispondente, ponderate in modo analogo ai calcoli della posizione del vertice.</span><span class="sxs-lookup"><span data-stu-id="b70e4-113">When lighting is enabled, vertex normals are transformed by a corresponding inverse world-view matrix, weighted in the same way as the vertex position computations.</span></span> <span data-ttu-id="b70e4-114">Il sistema normalizza il vettore normale risultante se lo \_ stato di rendering NORMALIZENORMALS di D3DRS è impostato su **true**.</span><span class="sxs-lookup"><span data-stu-id="b70e4-114">The system normalizes the resulting normal vector if the D3DRS\_NORMALIZENORMALS render state is set to **TRUE**.</span></span>

 

<span data-ttu-id="b70e4-115">Senza la fusione di geometria, spesso i modelli snodati dinamici vengono sottoposti a rendering in segmenti.</span><span class="sxs-lookup"><span data-stu-id="b70e4-115">Without geometry blending, dynamic articulated models are often rendered in segments.</span></span> <span data-ttu-id="b70e4-116">Si consideri, ad esempio, un modello 3D del braccio umano.</span><span class="sxs-lookup"><span data-stu-id="b70e4-116">For instance, consider a 3D model of the human arm.</span></span> <span data-ttu-id="b70e4-117">Nella visualizzazione più semplice, un ARM è costituito da due parti: il braccio superiore che si connette al corpo e il braccio inferiore, che si connette alla mano.</span><span class="sxs-lookup"><span data-stu-id="b70e4-117">In the simplest view, an arm has two parts: the upper arm which connects to the body, and the lower arm, which connects to the hand.</span></span> <span data-ttu-id="b70e4-118">I due sono connessi a gomito e il braccio inferiore ruota in corrispondenza di quel punto.</span><span class="sxs-lookup"><span data-stu-id="b70e4-118">The two are connected at the elbow, and the lower arm rotates at that point.</span></span> <span data-ttu-id="b70e4-119">Un'applicazione che esegue il rendering di un ARM potrebbe mantenere i dati dei vertici per il ARM superiore e inferiore, ognuno con una matrice di trasformazione globale separata.</span><span class="sxs-lookup"><span data-stu-id="b70e4-119">An application that renders an arm might retain vertex data for the upper and lower arm, each with a separate world transformation matrix.</span></span> <span data-ttu-id="b70e4-120">Questo aspetto è illustrato nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="b70e4-120">The following code example illustrates this.</span></span>


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



<span data-ttu-id="b70e4-121">Per eseguire il rendering del ARM, vengono effettuate due chiamate di rendering, come illustrato nel codice seguente.</span><span class="sxs-lookup"><span data-stu-id="b70e4-121">To render the arm, two rendering calls are made, as shown in the following code.</span></span>


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



<span data-ttu-id="b70e4-122">La figura seguente è una banana, modificata per usare questa tecnica.</span><span class="sxs-lookup"><span data-stu-id="b70e4-122">The following illustration is a banana, modified to use this technique.</span></span>

![illustrazione di una banana con Blend senza fusione di geometria](images/noblend.png)

<span data-ttu-id="b70e4-124">Le differenze tra la geometria mista e la geometria non mista sono ovvie.</span><span class="sxs-lookup"><span data-stu-id="b70e4-124">The differences between the blended geometry and the nonblended geometry are obvious.</span></span> <span data-ttu-id="b70e4-125">Questo esempio è piuttosto estremo.</span><span class="sxs-lookup"><span data-stu-id="b70e4-125">This example is somewhat extreme.</span></span> <span data-ttu-id="b70e4-126">In un'applicazione reale, le giunzioni dei modelli segmentati sono progettate in modo che le giunzioni non siano evidenti.</span><span class="sxs-lookup"><span data-stu-id="b70e4-126">In a real-world application, the joints of segmented models are designed so that seams are not as obvious.</span></span> <span data-ttu-id="b70e4-127">Tuttavia, le giunzioni sono visibili a volte, che presentano problemi costanti per le finestre di progettazione di modelli.</span><span class="sxs-lookup"><span data-stu-id="b70e4-127">However, seams are visible at times, which presents constant challenges for model designers.</span></span>

<span data-ttu-id="b70e4-128">La fusione di geometria in Direct3D presenta un'alternativa allo scenario classico di modellazione segmentata.</span><span class="sxs-lookup"><span data-stu-id="b70e4-128">Geometry blending in Direct3D presents an alternative to the classic segmented-modeling scenario.</span></span> <span data-ttu-id="b70e4-129">Tuttavia, la qualità visiva migliorata degli oggetti segmentati comporta il costo dei calcoli di fusione durante il rendering.</span><span class="sxs-lookup"><span data-stu-id="b70e4-129">However, the improved visual quality of segmented objects comes at the cost of the blending computations during rendering.</span></span> <span data-ttu-id="b70e4-130">Per ridurre al minimo l'impatto di queste operazioni aggiuntive, la pipeline di geometria Direct3D è ottimizzata per la geometria Blend con il minor sovraccarico possibile.</span><span class="sxs-lookup"><span data-stu-id="b70e4-130">To minimize the impact of these additional operations, the Direct3D geometry pipeline is optimized to blend geometry with the least possible overhead.</span></span> <span data-ttu-id="b70e4-131">Le applicazioni che usano in modo intelligente i servizi di Blend Geometry offerti da Direct3D possono migliorare il realismo dei loro caratteri evitando gravi ripercussioni sulle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="b70e4-131">Applications that intelligently use the geometry blending services offered by Direct3D can improve the realism of their characters while avoiding serious performance repercussions.</span></span>

## <a name="blending-transform-and-render-states"></a><span data-ttu-id="b70e4-132">Fusione degli Stati di trasformazione e rendering</span><span class="sxs-lookup"><span data-stu-id="b70e4-132">Blending Transform and Render States</span></span>

<span data-ttu-id="b70e4-133">Il metodo [**IDirect3DDevice9:: setransform**](/windows/desktop/api) riconosce le macro mondiali [**D3DTS \_**](d3dts-world.md) e [**D3DTS \_**](d3dts-worldn.md) , che corrispondono ai valori che possono essere definiti dalla macro [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="b70e4-133">The [**IDirect3DDevice9::SetTransform**](/windows/desktop/api) method recognizes the [**D3DTS\_WORLD**](d3dts-world.md) and [**D3DTS\_WORLDn**](d3dts-worldn.md) macros, which correspond to values that can be defined by the [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) macro.</span></span> <span data-ttu-id="b70e4-134">Queste macro vengono usate per identificare le matrici tra le quali verrà fusa la geometria.</span><span class="sxs-lookup"><span data-stu-id="b70e4-134">These macros are used to identify the matrices between which geometry will be blended.</span></span>

<span data-ttu-id="b70e4-135">Il tipo enumerato [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) include lo \_ stato di rendering D3DRS VERTEXBLEND per abilitare e controllare la fusione geometrica.</span><span class="sxs-lookup"><span data-stu-id="b70e4-135">The [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) enumerated type includes the D3DRS\_VERTEXBLEND render state to enable and control geometry blending.</span></span> <span data-ttu-id="b70e4-136">I valori validi per questo stato di rendering sono definiti dal tipo enumerato [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) .</span><span class="sxs-lookup"><span data-stu-id="b70e4-136">Valid values for this render state are defined by the [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) enumerated type.</span></span> <span data-ttu-id="b70e4-137">Se la fusione Geometry è abilitata, il formato del vertice deve includere il numero appropriato di pesi di fusione.</span><span class="sxs-lookup"><span data-stu-id="b70e4-137">If geometry blending is enabled, the vertex format must include the appropriate number of blending weights.</span></span>

## <a name="blending-weights"></a><span data-ttu-id="b70e4-138">Pesi di fusione</span><span class="sxs-lookup"><span data-stu-id="b70e4-138">Blending Weights</span></span>

<span data-ttu-id="b70e4-139">Un peso di fusione, talvolta denominato peso beta, controlla la misura in cui una determinata matrice mondiale influisca su un vertice.</span><span class="sxs-lookup"><span data-stu-id="b70e4-139">A blending weight, sometimes called a beta weight, controls the extent to which a given world matrix affects a vertex.</span></span> <span data-ttu-id="b70e4-140">I pesi di fusione sono valori a virgola mobile compresi tra 0,0 e 1,0, codificati in formato vertice, in cui il valore 0,0 indica che il vertice non è combinato con tale matrice e 1,0 indica che il vertice è interessato completamente dalla matrice.</span><span class="sxs-lookup"><span data-stu-id="b70e4-140">Blending weights are floating-point values that range from 0.0 to 1.0, encoded in the vertex format, where a value of 0.0 means the vertex is not blended with that matrix, and 1.0 means that the vertex is affected in full by the matrix.</span></span>

<span data-ttu-id="b70e4-141">I pesi per la fusione di geometria vengono codificati nel formato vertice, immediatamente dopo la posizione per ogni vertice, come descritto in [codici FVF a funzione fissa (Direct3D 9)](fixed-function-fvf-codes.md).</span><span class="sxs-lookup"><span data-stu-id="b70e4-141">Geometry blending weights are encoded in the vertex format, appearing immediately after the position for each vertex, as described in [Fixed Function FVF Codes (Direct3D 9)](fixed-function-fvf-codes.md).</span></span> <span data-ttu-id="b70e4-142">Si comunica il numero di pesi di fusione nel formato vertice includendo una delle [costanti FVF](d3dfvf.md) nella descrizione del vertice fornita ai metodi di rendering.</span><span class="sxs-lookup"><span data-stu-id="b70e4-142">You communicate the number of blending weights in the vertex format by including one of the [FVF constants](d3dfvf.md) in the vertex description that you provide to the rendering methods.</span></span>

<span data-ttu-id="b70e4-143">Il sistema esegue una Blend lineare tra i risultati ponderati delle matrici di Blend.</span><span class="sxs-lookup"><span data-stu-id="b70e4-143">The system performs a linear blend between the weighted results of the blend matrices.</span></span> <span data-ttu-id="b70e4-144">L'equazione seguente è la formula completa di fusione.</span><span class="sxs-lookup"><span data-stu-id="b70e4-144">The following equation is the complete blending formula.</span></span>

![equazione della fusione lineare, con matrici di trasformazione globale](images/vert-blend-formula.png)

<span data-ttu-id="b70e4-146">Nell'equazione precedente, vBlend è il vertice di output, gli elementi v sono i vertici prodotti dalla matrice mondiale applicata ([**D3DTS \_ worldn**](d3dts-worldn.md)).</span><span class="sxs-lookup"><span data-stu-id="b70e4-146">In the preceding equation, vBlend is the output vertex, the v-elements are the vertices produced by the applied world matrix ([**D3DTS\_WORLDn**](d3dts-worldn.md)).</span></span> <span data-ttu-id="b70e4-147">Gli elementi W sono i valori di peso corrispondenti all'interno del formato del vertice.</span><span class="sxs-lookup"><span data-stu-id="b70e4-147">The W elements are the corresponding weight values within the vertex format.</span></span> <span data-ttu-id="b70e4-148">Un vertice con Blend tra n matrici può avere-1 Blend dei valori di peso, uno per ogni matrice di fusione, eccetto l'ultimo.</span><span class="sxs-lookup"><span data-stu-id="b70e4-148">A vertex blended between n matrices can have - 1 blending weight values, one for each blending matrix, except the last.</span></span> <span data-ttu-id="b70e4-149">Il sistema genera automaticamente il peso per l'ultima matrice globale in modo che la somma di tutti i pesi sia pari a 1,0, espressa in notazione Sigma.</span><span class="sxs-lookup"><span data-stu-id="b70e4-149">The system automatically generates the weight for the last world matrix so that the sum of all weights is 1.0, expressed in sigma notation here.</span></span> <span data-ttu-id="b70e4-150">Questa formula può essere semplificata per ogni caso supportato da Direct3D, illustrato nelle equazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="b70e4-150">This formula can be simplified for each of the cases supported by Direct3D, which is shown in the following equations.</span></span>

![equazioni della fusione lineare per tre casi di fusione](images/vert-blend-formulas-simple.png)

<span data-ttu-id="b70e4-152">Si tratta delle forme semplificate della formula di Blend completa per i due, tre e quattro case della matrice di Blend.</span><span class="sxs-lookup"><span data-stu-id="b70e4-152">These are the simplified forms of the complete blending formula for the two, three, and four blend matrix cases.</span></span>

> [!Note]  
> <span data-ttu-id="b70e4-153">Sebbene Direct3D includa descrittori FVF per definire i vertici contenenti fino a cinque pesi di fusione, solo tre possono essere utilizzati in questa versione di DirectX.</span><span class="sxs-lookup"><span data-stu-id="b70e4-153">Although Direct3D includes FVF descriptors to define vertices that contain up to five blending weights, only three can be used in this release of DirectX.</span></span>

 

<span data-ttu-id="b70e4-154">Informazioni aggiuntive sono contenute negli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="b70e4-154">Additional information is contained in the following topics.</span></span>

-   [<span data-ttu-id="b70e4-155">Uso della combinazione di geometria (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b70e4-155">Using Geometry Blending (Direct3D 9)</span></span>](using-geometry-blending.md)
-   [<span data-ttu-id="b70e4-156">Fusione di vertici indicizzati (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b70e4-156">Indexed Vertex Blending (Direct3D 9)</span></span>](indexed-vertex-blending.md)
-   [<span data-ttu-id="b70e4-157">Interpolazione di vertici (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b70e4-157">Vertex Tweening (Direct3D 9)</span></span>](vertex-tweening.md)

## <a name="related-topics"></a><span data-ttu-id="b70e4-158">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b70e4-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b70e4-159">Pipeline Vertex</span><span class="sxs-lookup"><span data-stu-id="b70e4-159">Vertex Pipeline</span></span>](vertex-pipeline.md)
</dt> </dl>

 

 
