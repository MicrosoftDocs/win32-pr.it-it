---
description: Trasferimento Radiance pre-calcolato (Direct3D 9)
ms.assetid: 2a233d23-9a9e-4774-9be0-f3bfe0369b21
title: Trasferimento Radiance pre-calcolato (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94829a2559888c61ae795309bac5d1ab699d7f27
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104554736"
---
# <a name="precomputed-radiance-transfer-direct3d-9"></a><span data-ttu-id="d5fc9-103">Trasferimento Radiance pre-calcolato (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d5fc9-103">Precomputed Radiance Transfer (Direct3D 9)</span></span>

## <a name="using-precomputed-radiance-transfer"></a><span data-ttu-id="d5fc9-104">Uso del trasferimento Radiance pre-calcolato</span><span class="sxs-lookup"><span data-stu-id="d5fc9-104">Using Precomputed Radiance Transfer</span></span>

<span data-ttu-id="d5fc9-105">Negli scenari interessanti sono presenti diverse forme di complessità, tra cui il modo in cui l'ambiente di illuminazione è modellato (ovvero i modelli di illuminazione ad area rispetto ai punti/direzionali) e il tipo di effetti globali che vengono modellati (ad esempio, ombre, interriflettenze, scattering di sottosuperficie). Le tecniche di rendering interattive tradizionali modellano una quantità limitata di questa complessità.</span><span class="sxs-lookup"><span data-stu-id="d5fc9-105">There are several forms of complexity present in interesting scenes, including how the lighting environment is modeled (that is, area lighting models versus point/directional ones) and what kind of global effects are modeled (for example, shadows, interreflections, subsurface scattering.) Traditional interactive rendering techniques model a limited amount of this complexity.</span></span> <span data-ttu-id="d5fc9-106">Il PRT Abilita questi effetti con alcune restrizioni significative:</span><span class="sxs-lookup"><span data-stu-id="d5fc9-106">PRT enables these effects with some significant restrictions:</span></span>

-   <span data-ttu-id="d5fc9-107">Si presuppone che gli oggetti siano rigidi (ovvero nessuna deformazione).</span><span class="sxs-lookup"><span data-stu-id="d5fc9-107">Objects are assumed to be rigid (that is, no deformations).</span></span>
-   <span data-ttu-id="d5fc9-108">Si tratta di un approccio incentrato sugli oggetti (a meno che gli oggetti non vengano spostati insieme, questi effetti globali non vengono mantenuti tra di essi).</span><span class="sxs-lookup"><span data-stu-id="d5fc9-108">It is an object-centric approach (unless objects are moved together, these global effects are not maintained between them).</span></span>
-   <span data-ttu-id="d5fc9-109">Viene modellata solo l'illuminazione a bassa frequenza (che produce ombre morbide). Per le luci ad alta frequenza (ombre acute), è necessario utilizzare tecniche tradizionali.</span><span class="sxs-lookup"><span data-stu-id="d5fc9-109">Only low-frequency lighting is modeled (resulting in soft shadows.) For high-frequency lights (sharp shadows), traditional techniques would have to be employed.</span></span>

<span data-ttu-id="d5fc9-110">Per PRT è necessario uno dei seguenti, ma non entrambi:</span><span class="sxs-lookup"><span data-stu-id="d5fc9-110">PRT requires either of the following, but not both:</span></span>

-   <span data-ttu-id="d5fc9-111">modelli altamente tassellati e vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="d5fc9-111">highly-tessellated models and vs\_1\_1</span></span>
-   <span data-ttu-id="d5fc9-112">PS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d5fc9-112">ps\_2\_0</span></span>

### <a name="standard-diffuse-lighting-versus-prt"></a><span data-ttu-id="d5fc9-113">Illuminazione standard diffusa rispetto a PRT</span><span class="sxs-lookup"><span data-stu-id="d5fc9-113">Standard Diffuse Lighting versus PRT</span></span>

<span data-ttu-id="d5fc9-114">Viene eseguito il rendering dell'illustrazione seguente usando il modello di illuminazione tradizionale (n · l).</span><span class="sxs-lookup"><span data-stu-id="d5fc9-114">The following illustration is rendered using the traditional (n · l) lighting model.</span></span> <span data-ttu-id="d5fc9-115">È possibile abilitare le ombreggiature nitide usando un altro passaggio e una forma di tecnica di ombreggiatura (mappe di profondità ombreggiatura o volumi shadow).</span><span class="sxs-lookup"><span data-stu-id="d5fc9-115">Sharp shadows could be enabled using another pass and some form of shadowing technique (shadow depth maps or shadow volumes).</span></span> <span data-ttu-id="d5fc9-116">L'aggiunta di più luci richiederebbe più passaggi (se è necessario usare le ombreggiature) o più shader complessi con tecniche tradizionali.</span><span class="sxs-lookup"><span data-stu-id="d5fc9-116">Adding multiple lights would require either multiple passes (if shadows are to be used) or more complex shaders with traditional techniques.</span></span>

![Screenshot di un'illustrazione sottoposta a rendering usando il modello di illuminazione tradizionale](images/prt-diffuse-cropped.png)

<span data-ttu-id="d5fc9-118">L'illustrazione successiva viene sottoposta a rendering con PRT usando la migliore approssimazione di una singola luce direzionale che può risolvere.</span><span class="sxs-lookup"><span data-stu-id="d5fc9-118">The next illustration is rendered with PRT using the best approximation of a single directional light that it can resolve.</span></span> <span data-ttu-id="d5fc9-119">In questo modo si otterrà un'ombreggiatura soft che sarebbe difficile da produrre con le tecniche tradizionali.</span><span class="sxs-lookup"><span data-stu-id="d5fc9-119">This results in soft shadows that would be difficult to produce with traditional techniques.</span></span> <span data-ttu-id="d5fc9-120">Poiché PRT modella sempre gli ambienti di illuminazione completi che aggiungono più luci o usando una mappa dell'ambiente, è possibile modificare solo i valori (ma non il numero) delle costanti usate dallo shader.</span><span class="sxs-lookup"><span data-stu-id="d5fc9-120">Because PRT always models complete lighting environments adding multiple lights or using an environment map, you would only change the values (but not the number) of constants used by the shader.</span></span>

![Screenshot di un'illustrazione sottoposta a rendering usando PRT](images/prt-diffuseshadows-cropped.png)

### <a name="prt-with-interreflections"></a><span data-ttu-id="d5fc9-122">PRT con interriflettenze</span><span class="sxs-lookup"><span data-stu-id="d5fc9-122">PRT with Interreflections</span></span>

<span data-ttu-id="d5fc9-123">L'illuminazione diretta raggiunge la superficie direttamente dalla luce.</span><span class="sxs-lookup"><span data-stu-id="d5fc9-123">Direct lighting reaches the surface directly from the light.</span></span> <span data-ttu-id="d5fc9-124">Le interriflettenze sono chiare che raggiungono la superficie dopo il rimbalzo di un'altra superficie per un certo numero di volte.</span><span class="sxs-lookup"><span data-stu-id="d5fc9-124">Interreflections are light reaching the surface after bouncing off some other surface some number of times.</span></span> <span data-ttu-id="d5fc9-125">Il PRT può modellare questo comportamento senza modificare le prestazioni in fase di esecuzione eseguendo semplicemente il simulatore con parametri diversi.</span><span class="sxs-lookup"><span data-stu-id="d5fc9-125">PRT can model this behavior without changing the performance at run time by simply running the simulator with different parameters.</span></span>

<span data-ttu-id="d5fc9-126">La figura seguente viene creata usando solo il PRT diretto (0 rimbalzi senza interriflettenze).</span><span class="sxs-lookup"><span data-stu-id="d5fc9-126">The following illustration is created using direct PRT only (0 bounces with no interreflections).</span></span>

![Screenshot di un'illustrazione di cui è stato eseguito il rendering usando solo la PRT diretta](images/prt-nointerreflections.png)

<span data-ttu-id="d5fc9-128">La figura seguente viene creata usando PRT con le interspecchiazioni (2 rimbalzi con le interdipendenze).</span><span class="sxs-lookup"><span data-stu-id="d5fc9-128">The following illustration is created using PRT with interreflections (2 bounces with interreflections).</span></span>

![Screenshot di un'illustrazione sottoposta a rendering usando PRT con interriflettenze](images/prt-interreflections.png)

### <a name="prt-with-subsurface-scattering"></a><span data-ttu-id="d5fc9-130">PRT con scattering della sottosuperficie</span><span class="sxs-lookup"><span data-stu-id="d5fc9-130">PRT with Subsurface Scattering</span></span>

<span data-ttu-id="d5fc9-131">La dispersione della sottosuperficie è una tecnica che modella il modo in cui la luce passa attraverso determinati materiali.</span><span class="sxs-lookup"><span data-stu-id="d5fc9-131">Subsurface scattering is a technique that models how light passes through certain materials.</span></span> <span data-ttu-id="d5fc9-132">Ad esempio, premere una torcia accesa sul Palm della mano.</span><span class="sxs-lookup"><span data-stu-id="d5fc9-132">As an example, press a lit flashlight against the palm of your hand.</span></span> <span data-ttu-id="d5fc9-133">La luce della torcia passa attraverso la mano, rimbalza (cambiando colore nel processo) ed esce dall'altra parte della mano.</span><span class="sxs-lookup"><span data-stu-id="d5fc9-133">The light from the flashlight passes through your hand, bounces around (changing color in the process), and exits from the other side of your hand.</span></span> <span data-ttu-id="d5fc9-134">Questo può essere modellato anche con semplici modifiche al simulatore e nessuna modifica al runtime.</span><span class="sxs-lookup"><span data-stu-id="d5fc9-134">This can also be modeled with simple changes to the simulator and no changes to the runtime.</span></span>

<span data-ttu-id="d5fc9-135">Nella figura seguente viene illustrato PRT con la dispersione della sottosuperficie.</span><span class="sxs-lookup"><span data-stu-id="d5fc9-135">The following illustration demonstrates PRT with subsurface scattering.</span></span>

![Screenshot di un'illustrazione sottoposta a rendering usando PRT con scattering della sottosuperficie](images/prt-subsurface.png)

## <a name="how-prt-works"></a><span data-ttu-id="d5fc9-137">Funzionamento di PRT</span><span class="sxs-lookup"><span data-stu-id="d5fc9-137">How PRT Works</span></span>

<span data-ttu-id="d5fc9-138">I termini seguenti sono utili per comprendere il funzionamento di PRT, come illustrato nel diagramma seguente.</span><span class="sxs-lookup"><span data-stu-id="d5fc9-138">The following terms are useful for understanding how PRT works, as illustrated in the following diagram.</span></span>

<span data-ttu-id="d5fc9-139">Radiance di origine: la luminosità di origine rappresenta l'ambiente di illuminazione nel suo complesso.</span><span class="sxs-lookup"><span data-stu-id="d5fc9-139">Source Radiance: The source radiance represents the lighting environment as a whole.</span></span> <span data-ttu-id="d5fc9-140">In PRT un ambiente arbitrario viene approssimato usando la base armonica sferica. questa illuminazione si presuppone che sia distante rispetto all'oggetto (lo stesso presupposto per le mappe dell'ambiente).</span><span class="sxs-lookup"><span data-stu-id="d5fc9-140">In PRT an arbitrary environment is approximated using the spherical harmonic basis - this lighting is assumed to be distant relative to the object (the same assumption that is made with environment maps.)</span></span>

<span data-ttu-id="d5fc9-141">Radiance di uscita: l'uscita Radiance è la luce che esce da un punto sulla superficie da qualsiasi origine possibile (Radiance riflesso, scattering di sottosuperficie, emissione).</span><span class="sxs-lookup"><span data-stu-id="d5fc9-141">Exit Radiance: Exit radiance is the light leaving from a point on the surface from any possible source (reflected radiance, subsurface scattering, emission).</span></span>

<span data-ttu-id="d5fc9-142">Transfer vectors: i vettori di trasferimento eseguono il mapping della luminosità del codice sorgente al radiatore di uscita e vengono precalcolati offline usando una simulazione di trasporto leggero complessa.</span><span class="sxs-lookup"><span data-stu-id="d5fc9-142">Transfer Vectors: Transfer vectors map Source Radiance into exit radiance and are precomputed offline using a complex light transport simulation.</span></span>

![diagramma del funzionamento di PRT](images/prt-lightingpicture.png)

<span data-ttu-id="d5fc9-144">PRT determina il processo di rendering in due fasi, come illustrato nel diagramma seguente:</span><span class="sxs-lookup"><span data-stu-id="d5fc9-144">PRT factors the rendering process into two stages, as shown in the following diagram:</span></span>

1.  <span data-ttu-id="d5fc9-145">Una simulazione di trasporto leggero costosa Precalcola i coefficienti di trasferimento che possono essere usati in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="d5fc9-145">An expensive light transport simulation precomputes transfer coefficients that can be used at run time.</span></span>
2.  <span data-ttu-id="d5fc9-146">Una fase di runtime relativamente leggera approssimatamente si avvicina all'ambiente di illuminazione usando la base armonica sferica, quindi usa questi coefficienti di illuminazione e i coefficienti di trasferimento pre-calcolati (dalla fase 1) con uno shader semplice, con conseguente uscita Radiance (luce che esce dall'oggetto).</span><span class="sxs-lookup"><span data-stu-id="d5fc9-146">A relatively lightweight run-time stage first approximates the lighting environment using the spherical harmonic basis, then uses these lighting coefficients and the precomputed transfer coefficients (from stage 1) with a simple shader, resulting in exit radiance (the light leaving the object).</span></span>

![diagramma del flusso di dati PRT](images/prt-dataflow.png)

### <a name="how-to-use-the-prt-api"></a><span data-ttu-id="d5fc9-148">Come usare l'API PRT</span><span class="sxs-lookup"><span data-stu-id="d5fc9-148">How to Use the PRT API</span></span>

1.  <span data-ttu-id="d5fc9-149">Calcola i vettori di trasferimento con una delle risorse di calcolo... metodi di [**ID3DXPRTEngine**](id3dxprtengine.md).</span><span class="sxs-lookup"><span data-stu-id="d5fc9-149">Compute the transfer vectors with one of the Compute... methods of [**ID3DXPRTEngine**](id3dxprtengine.md).</span></span>

    <span data-ttu-id="d5fc9-150">La gestione diretta di questi vettori di trasferimento richiede una quantità significativa di calcolo della memoria e dello shader.</span><span class="sxs-lookup"><span data-stu-id="d5fc9-150">Directly dealing with these transfer vectors requires a significant amount of memory and shader computation.</span></span> <span data-ttu-id="d5fc9-151">La compressione riduce significativamente la quantità di memoria e il calcolo dello shader necessari.</span><span class="sxs-lookup"><span data-stu-id="d5fc9-151">Compression significantly reduces the amount of memory and shader computation required.</span></span>

    <span data-ttu-id="d5fc9-152">I valori di illuminazione finali vengono calcolati in un vertex shader che implementa la seguente equazione di rendering compresso.</span><span class="sxs-lookup"><span data-stu-id="d5fc9-152">The final lighting values are calculated in a vertex shader that implements the following compressed rendering equation.</span></span>

    ![equazione di rendering PRT](images/prt-shaderequation.png)

    <span data-ttu-id="d5fc9-154">Dove:</span><span class="sxs-lookup"><span data-stu-id="d5fc9-154">Where:</span></span>

    

    | <span data-ttu-id="d5fc9-155">Parametro</span><span class="sxs-lookup"><span data-stu-id="d5fc9-155">Parameter</span></span>      | <span data-ttu-id="d5fc9-156">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d5fc9-156">Description</span></span>                                                                                                     |
    |----------------|-----------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="d5fc9-157">RP</span><span class="sxs-lookup"><span data-stu-id="d5fc9-157">Rₚ</span></span>             | <span data-ttu-id="d5fc9-158">Un singolo canale di uscita Radiance al vertice p e viene valutato in ogni vertice della mesh.</span><span class="sxs-lookup"><span data-stu-id="d5fc9-158">A single channel of exit radiance at vertex p and is evaluated at every vertex on the mesh.</span></span>                     |
    | <span data-ttu-id="d5fc9-159">MK</span><span class="sxs-lookup"><span data-stu-id="d5fc9-159">Mₖ</span></span>             | <span data-ttu-id="d5fc9-160">Media per il cluster k.</span><span class="sxs-lookup"><span data-stu-id="d5fc9-160">The mean for cluster k.</span></span> <span data-ttu-id="d5fc9-161">Si tratta di un vettore Order ² di coefficienti.</span><span class="sxs-lookup"><span data-stu-id="d5fc9-161">This is an Order² vector of coefficients.</span></span>                                               |
    | <span data-ttu-id="d5fc9-162">k</span><span class="sxs-lookup"><span data-stu-id="d5fc9-162">k</span></span>              | <span data-ttu-id="d5fc9-163">ID del cluster per il vertice p.</span><span class="sxs-lookup"><span data-stu-id="d5fc9-163">The cluster ID for vertex p.</span></span>                                                                                    |
    | <span data-ttu-id="d5fc9-164">L<sup>'</sup></span><span class="sxs-lookup"><span data-stu-id="d5fc9-164">L<sup>'</sup></span></span>  | <span data-ttu-id="d5fc9-165">Approssimazione della luminosità di origine nelle funzioni di base SH.</span><span class="sxs-lookup"><span data-stu-id="d5fc9-165">The approximation of the source radiance into the SH basis functions.</span></span> <span data-ttu-id="d5fc9-166">Si tratta di un vettore Order ² di coefficienti.</span><span class="sxs-lookup"><span data-stu-id="d5fc9-166">This is an Order² vector of coefficients.</span></span> |
    | <span data-ttu-id="d5fc9-167">j</span><span class="sxs-lookup"><span data-stu-id="d5fc9-167">j</span></span>              | <span data-ttu-id="d5fc9-168">Intero che somma il numero di vettori PCA.</span><span class="sxs-lookup"><span data-stu-id="d5fc9-168">An integer that sums over the number of PCA vectors.</span></span>                                                            |
    | <span data-ttu-id="d5fc9-169">w<sub>PJ</sub></span><span class="sxs-lookup"><span data-stu-id="d5fc9-169">w<sub>pj</sub></span></span> | <span data-ttu-id="d5fc9-170">Peso PCA JTH per il punto p.</span><span class="sxs-lookup"><span data-stu-id="d5fc9-170">The jth PCA weight for point p.</span></span> <span data-ttu-id="d5fc9-171">Si tratta di un singolo coefficiente.</span><span class="sxs-lookup"><span data-stu-id="d5fc9-171">This is a single coefficient.</span></span>                                                   |
    | <span data-ttu-id="d5fc9-172">B<sub>kJ</sub></span><span class="sxs-lookup"><span data-stu-id="d5fc9-172">B<sub>kj</sub></span></span> | <span data-ttu-id="d5fc9-173">Vettore di base di JTH PCA per il cluster k.</span><span class="sxs-lookup"><span data-stu-id="d5fc9-173">The jth PCA basis vector for cluster k.</span></span> <span data-ttu-id="d5fc9-174">Si tratta di un vettore Order ² di coefficienti.</span><span class="sxs-lookup"><span data-stu-id="d5fc9-174">This is an Order² vector of coefficients.</span></span>                               |

    

     

    <span data-ttu-id="d5fc9-175">Estrazione... i metodi di [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) forniscono l'accesso ai dati compressi dalla simulazione.</span><span class="sxs-lookup"><span data-stu-id="d5fc9-175">The Extract... methods of [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) provide access to compressed data from the simulation.</span></span>

2.  <span data-ttu-id="d5fc9-176">Calcolo della luminosità di origine.</span><span class="sxs-lookup"><span data-stu-id="d5fc9-176">Compute the source radiance.</span></span>

    <span data-ttu-id="d5fc9-177">Sono disponibili diverse funzioni helper nell'API per gestire un'ampia gamma di scenari di illuminazione comuni.</span><span class="sxs-lookup"><span data-stu-id="d5fc9-177">There are several helper functions in the API to handle a variety of common lighting scenarios.</span></span>

    

    | <span data-ttu-id="d5fc9-178">Funzione</span><span class="sxs-lookup"><span data-stu-id="d5fc9-178">Function</span></span>                                                         | <span data-ttu-id="d5fc9-179">Scopo</span><span class="sxs-lookup"><span data-stu-id="d5fc9-179">Purpose</span></span>                                                                                                     |
    |------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
    | [<span data-ttu-id="d5fc9-180">**D3DXSHEvalDirectionalLight**</span><span class="sxs-lookup"><span data-stu-id="d5fc9-180">**D3DXSHEvalDirectionalLight**</span></span>](d3dxshevaldirectionallight.md) | <span data-ttu-id="d5fc9-181">Si avvicina a una luce direzionale convenzionale.</span><span class="sxs-lookup"><span data-stu-id="d5fc9-181">Approximates a conventional directional light.</span></span>                                                              |
    | [<span data-ttu-id="d5fc9-182">**D3DXSHEvalSphericalLight**</span><span class="sxs-lookup"><span data-stu-id="d5fc9-182">**D3DXSHEvalSphericalLight**</span></span>](d3dxshevalsphericallight.md)     | <span data-ttu-id="d5fc9-183">Approssima le fonti di luce sferiche locali.</span><span class="sxs-lookup"><span data-stu-id="d5fc9-183">Approximates local spherical light sources.</span></span> <span data-ttu-id="d5fc9-184">Si noti che PRT funziona solo con gli ambienti di illuminazione della distanza.</span><span class="sxs-lookup"><span data-stu-id="d5fc9-184">(Note that PRT only works with distance lighting environments.)</span></span> |
    | [<span data-ttu-id="d5fc9-185">**D3DXSHEvalConeLight**</span><span class="sxs-lookup"><span data-stu-id="d5fc9-185">**D3DXSHEvalConeLight**</span></span>](d3dxshevalconelight.md)               | <span data-ttu-id="d5fc9-186">Si avvicina a una sorgente di luce dell'area distante.</span><span class="sxs-lookup"><span data-stu-id="d5fc9-186">Approximates a distant area light source.</span></span> <span data-ttu-id="d5fc9-187">Un esempio è la luce solare (angolo conico molto piccolo).</span><span class="sxs-lookup"><span data-stu-id="d5fc9-187">An example would be the sun (very small cone angle).</span></span>              |
    | [<span data-ttu-id="d5fc9-188">**D3DXSHEvalHemisphereLight**</span><span class="sxs-lookup"><span data-stu-id="d5fc9-188">**D3DXSHEvalHemisphereLight**</span></span>](d3dxshevalhemispherelight.md)   | <span data-ttu-id="d5fc9-189">Valuta una luce che rappresenta un'interpolazione lineare tra due colori (uno in ogni polo di una sfera).</span><span class="sxs-lookup"><span data-stu-id="d5fc9-189">Evaluates a light that is a linear interpolation between two colors (one on each pole of a sphere).</span></span>         |

    

     

3.  <span data-ttu-id="d5fc9-190">Calcolo della luminosità di uscita.</span><span class="sxs-lookup"><span data-stu-id="d5fc9-190">Compute the exit radiance.</span></span>

    <span data-ttu-id="d5fc9-191">L'equazione 1 deve ora essere valutata in ogni punto usando un vertice o un pixel shader.</span><span class="sxs-lookup"><span data-stu-id="d5fc9-191">Equation 1 now has to be evaluated at every point using either a vertex or pixel shader.</span></span> <span data-ttu-id="d5fc9-192">Prima di poter valutare lo shader, le costanti devono essere pre-calcolate e caricate nella tabella Constant (vedere l' [esempio di demo PRT](https://msdn.microsoft.com/library/Ee418763(v=VS.85).aspx) per informazioni dettagliate).</span><span class="sxs-lookup"><span data-stu-id="d5fc9-192">Before the shader can be evaluated, constants have to be precomputed and loaded into the constant table (see the [PRT Demo Sample](https://msdn.microsoft.com/library/Ee418763(v=VS.85).aspx) for details).</span></span> <span data-ttu-id="d5fc9-193">Lo shader è una semplice implementazione di questa equazione.</span><span class="sxs-lookup"><span data-stu-id="d5fc9-193">The shader itself is a straightforward implementation of this equation.</span></span>

    ```
    struct VS_OUTPUT
    {
        float4 Position   : POSITION;   // vertex position 
        float2 TextureUV  : TEXCOORD0;  // vertex texture coordinates 
        float4 Diffuse    : COLOR0;     // vertex diffuse color
    };

    VS_OUTPUT Output;   
    Output.Position = mul(vPos, mWorldViewProjection);

    float4 vExitR = float4(0,0,0,0);
    float4 vExitG = float4(0,0,0,0);
    float4 vExitB = float4(0,0,0,0);
        
    for (int i=0; i < (NUM_PCA_VECTORS/4); i++) 
    {
       vExitR += vPCAWeights[i] * 
           vClusteredPCA[iClusterOffset+i+1+(NUM_PCA_VECTORS/4)*0];
       vExitG += vPCAWeights[i] * 
           vClusteredPCA[iClusterOffset+i+1+(NUM_PCA_VECTORS/4)*1];
       vExitB += vPCAWeights[i] * 
           vClusteredPCA[iClusterOffset+i+1+(NUM_PCA_VECTORS/4)*2];
    }
       
    float4 vExitRadiance = vClusteredPCA[iClusterOffset];
    vExitRadiance.r += dot(vExitR,1);
    vExitRadiance.g += dot(vExitG,1);
    vExitRadiance.b += dot(vExitB,1);

    Output.Diffuse = vExitRadiance;
    ```

    

## <a name="references"></a><span data-ttu-id="d5fc9-194">Riferimenti</span><span class="sxs-lookup"><span data-stu-id="d5fc9-194">References</span></span>

<span data-ttu-id="d5fc9-195">Per ulteriori informazioni sulle armoniche PRT e sferiche, vedere i seguenti documenti:</span><span class="sxs-lookup"><span data-stu-id="d5fc9-195">For more information about PRT and spherical harmonics, see the following papers:</span></span>


```
Precomputed Radiance Transfer for Real-Time Rendering in Dynamic, 
Low-Frequency Lighting Environments 
P.-P. Sloan, J. Kautz, J. Snyder
SIGGRAPH 2002 

Clustered Principal Components for Precomputed Radiance Transfer 
P.-P. Sloan, J. Hall, J. Hart, J. Snyder 
SIGGRAPH 2003 

Efficient Evaluation of Irradiance Environment Maps 
P.-P. Sloan 
ShaderX 2,  W. Engel 

Spherical Harmonic Lighting: The Gritty Details 
R. Green 
GDC 2003 

An Efficient Representation for Irradiance Environment Maps 
R. Ramamoorthi, P. Hanrahan 

A Practical Model for Subsurface Light Transport 
H. W. Jensen, S. R. Marschner, M. Levoy, and P. Hanrahan 
SIGGRAPH 2001 

Bi-Scale Radiance Transfer 
P.-P. Sloan, X. Liu, H.-Y. Shum, J. Snyder
SIGGRAPH 2003 

Fast, Arbitrary BRDF Shading for Low-Frequency Lighting Using Spherical 
Harmonics 
J. Kautz, P.-P. Sloan, J. Snyder
12th Eurographics Workshop on Rendering 

Precomputing Interactive Dynamic Deformable Scenes 
D. James, K. Fatahalian 
SIGGRAPH 2003 

All-Frequency Shadows Using Non-linear Wavelet Lighting Approximation 
R. Ng, R. Ramamoorth, P. Hanrahan 
SIGGRAPH 2003 

Matrix Radiance Transfer 
J. Lehtinen, J. Kautz
SIGGRAPH 2003 

Math World 
E. W. Weisstein, Wolfram Research, Inc. 

Quantum Theory of Angular Momentum 
D. A. Varshalovich, A.N. Moskalev, V.K. Khersonskii 
```



## <a name="related-topics"></a><span data-ttu-id="d5fc9-196">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d5fc9-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5fc9-197">Argomenti avanzati</span><span class="sxs-lookup"><span data-stu-id="d5fc9-197">Advanced Topics</span></span>](advanced-topics.md)
</dt> <dt>

[<span data-ttu-id="d5fc9-198">Equazioni PRT (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d5fc9-198">PRT Equations (Direct3D 9)</span></span>](prt-equations.md)
</dt> <dt>

[<span data-ttu-id="d5fc9-199">Rappresentazione di PRT con trame (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d5fc9-199">Representing PRT With Textures (Direct3D 9)</span></span>](representing-prt-with-textures.md)
</dt> <dt>

[<span data-ttu-id="d5fc9-200">**ID3DXPRTBuffer**</span><span class="sxs-lookup"><span data-stu-id="d5fc9-200">**ID3DXPRTBuffer**</span></span>](id3dxprtbuffer.md)
</dt> <dt>

[<span data-ttu-id="d5fc9-201">**ID3DXPRTCompBuffer**</span><span class="sxs-lookup"><span data-stu-id="d5fc9-201">**ID3DXPRTCompBuffer**</span></span>](id3dxprtcompbuffer.md)
</dt> <dt>

[<span data-ttu-id="d5fc9-202">**ID3DXPRTEngine**</span><span class="sxs-lookup"><span data-stu-id="d5fc9-202">**ID3DXPRTEngine**</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="d5fc9-203">**ID3DXTextureGutterHelper**</span><span class="sxs-lookup"><span data-stu-id="d5fc9-203">**ID3DXTextureGutterHelper**</span></span>](id3dxtexturegutterhelper.md)
</dt> <dt>

[<span data-ttu-id="d5fc9-204">Funzioni di trasferimento Radiance pre-calcolate</span><span class="sxs-lookup"><span data-stu-id="d5fc9-204">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[<span data-ttu-id="d5fc9-205">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="d5fc9-205">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 



