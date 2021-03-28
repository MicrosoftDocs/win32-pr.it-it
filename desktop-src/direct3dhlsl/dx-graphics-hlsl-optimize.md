---
title: Ottimizzazione degli shader HLSL
description: Questa sezione descrive le strategie generali che è possibile usare per ottimizzare gli shader. È possibile applicare queste strategie agli shader scritti in qualsiasi linguaggio, su qualsiasi piattaforma.
ms.assetid: 014b9cb3-a489-48d7-8174-b97de168bf3a
keywords:
- linguaggio shader di alto livello
- HLSL, prestazioni
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 06d3bb806e98e489020aa1755ef2a6c952459d86
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045102"
---
# <a name="optimizing-hlsl-shaders"></a><span data-ttu-id="206a9-106">Ottimizzazione degli shader HLSL</span><span class="sxs-lookup"><span data-stu-id="206a9-106">Optimizing HLSL Shaders</span></span>

<span data-ttu-id="206a9-107">Questa sezione descrive le strategie generali che è possibile usare per ottimizzare gli shader.</span><span class="sxs-lookup"><span data-stu-id="206a9-107">This section describes general-purpose strategies that you can use to optimize your shaders.</span></span> <span data-ttu-id="206a9-108">È possibile applicare queste strategie agli shader scritti in qualsiasi linguaggio, su qualsiasi piattaforma.</span><span class="sxs-lookup"><span data-stu-id="206a9-108">You can apply these strategies to shaders that are written in any language, on any platform.</span></span>

-   [<span data-ttu-id="206a9-109">Informazioni su dove eseguire i calcoli dello shader</span><span class="sxs-lookup"><span data-stu-id="206a9-109">Know Where To Perform Shader Calculations</span></span>](#know-where-to-perform-shader-calculations)
-   [<span data-ttu-id="206a9-110">Ignora istruzioni non necessarie</span><span class="sxs-lookup"><span data-stu-id="206a9-110">Skip Unnecessary Instructions</span></span>](#skip-unnecessary-instructions)
-   [<span data-ttu-id="206a9-111">Variabili Pack e Interpolants</span><span class="sxs-lookup"><span data-stu-id="206a9-111">Pack Variables and Interpolants</span></span>](#pack-variables-and-interpolants)
-   [<span data-ttu-id="206a9-112">Ridurre la complessità dello shader</span><span class="sxs-lookup"><span data-stu-id="206a9-112">Reduce Shader Complexity</span></span>](#reduce-shader-complexity)
-   [<span data-ttu-id="206a9-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="206a9-113">Related Topics</span></span>](#related-topics)
-   [<span data-ttu-id="206a9-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="206a9-114">Related topics</span></span>](#related-topics)

## <a name="know-where-to-perform-shader-calculations"></a><span data-ttu-id="206a9-115">Informazioni su dove eseguire i calcoli dello shader</span><span class="sxs-lookup"><span data-stu-id="206a9-115">Know Where To Perform Shader Calculations</span></span>

<span data-ttu-id="206a9-116">I vertex shader eseguono operazioni che includono il recupero di vertici e l'esecuzione della trasformazione matrice dei dati dei vertici.</span><span class="sxs-lookup"><span data-stu-id="206a9-116">Vertex shaders perform operations that include fetching vertices and performing matrix transformation of vertex data.</span></span> <span data-ttu-id="206a9-117">I vertex shader vengono in genere eseguiti una volta per ogni vertice.</span><span class="sxs-lookup"><span data-stu-id="206a9-117">Typically, vertex shaders are executed once per vertex.</span></span>

<span data-ttu-id="206a9-118">I pixel shader eseguono operazioni che includono il recupero dei dati di trama e l'esecuzione di calcoli di illuminazione.</span><span class="sxs-lookup"><span data-stu-id="206a9-118">Pixel Shaders perform operations that include fetching texture data and performing lighting calculations.</span></span> <span data-ttu-id="206a9-119">In genere, i pixel shader vengono eseguiti una volta per ogni pixel per una determinata porzione di geometria.</span><span class="sxs-lookup"><span data-stu-id="206a9-119">Typically, pixel shaders are executed once per pixel for a given piece of geometry.</span></span>

<span data-ttu-id="206a9-120">In genere, i pixel superano i vertici in una scena, quindi i pixel shader vengono eseguiti più spesso rispetto ai vertex shader.</span><span class="sxs-lookup"><span data-stu-id="206a9-120">Typically, pixels outnumber vertices in a scene, so pixel shaders execute more often than vertex shaders.</span></span>

<span data-ttu-id="206a9-121">Quando si progettano gli algoritmi dello shader, tenere presente quanto segue:</span><span class="sxs-lookup"><span data-stu-id="206a9-121">When you design shader algorithms, keep the following in mind:</span></span>

-   <span data-ttu-id="206a9-122">Se possibile, eseguire calcoli sul vertex shader.</span><span class="sxs-lookup"><span data-stu-id="206a9-122">Perform calculations on the vertex shader if possible.</span></span> <span data-ttu-id="206a9-123">Un calcolo eseguito su un pixel shader è molto più costoso di un calcolo eseguito su un vertex shader.</span><span class="sxs-lookup"><span data-stu-id="206a9-123">A calculation that is performed on a pixel shader is much more expensive than a calculation that is performed on a vertex shader.</span></span>
-   <span data-ttu-id="206a9-124">Prendere in considerazione l'uso di calcoli per vertice per migliorare le prestazioni in situazioni come le mesh dense.</span><span class="sxs-lookup"><span data-stu-id="206a9-124">Consider using per-vertex calculations to improve performance in situations such as dense meshes.</span></span> <span data-ttu-id="206a9-125">Per le mesh dense, i calcoli per vertice possono produrre risultati non distinguibili visivamente dai risultati prodotti con calcoli per pixel.</span><span class="sxs-lookup"><span data-stu-id="206a9-125">For dense meshes, per-vertex calculations may produce results that are visually indistinguishable from results produced with per-pixel calculations.</span></span>

## <a name="skip-unnecessary-instructions"></a><span data-ttu-id="206a9-126">Ignora istruzioni non necessarie</span><span class="sxs-lookup"><span data-stu-id="206a9-126">Skip Unnecessary Instructions</span></span>

<span data-ttu-id="206a9-127">In HLSL, la creazione di rami dinamici consente di limitare il numero di istruzioni eseguite.</span><span class="sxs-lookup"><span data-stu-id="206a9-127">In HLSL, dynamic branching provides the ability to limit the number of instructions that are executed.</span></span> <span data-ttu-id="206a9-128">La creazione di rami dinamici consente pertanto di velocizzare il tempo di esecuzione dello shader.</span><span class="sxs-lookup"><span data-stu-id="206a9-128">Therefore, dynamic branching can help speed up shader execution time.</span></span> <span data-ttu-id="206a9-129">Se la geometria o i pixel non sono visualizzati, utilizzare la diramazione dinamica per uscire dallo shader o per limitare le istruzioni.</span><span class="sxs-lookup"><span data-stu-id="206a9-129">If geometry or pixels are not displayed, use dynamic branching to exit the shader or to limit instructions.</span></span> <span data-ttu-id="206a9-130">Se, ad esempio, un pixel non è acceso, non è presente alcun punto nell'esecuzione dell'algoritmo di illuminazione.</span><span class="sxs-lookup"><span data-stu-id="206a9-130">For example, if a pixel is not lit, there is no point in executing the lighting algorithm.</span></span>

<span data-ttu-id="206a9-131">Nella tabella seguente sono elencati alcuni casi in cui è possibile testare le condizioni nello shader e utilizzare la diramazione dinamica per ignorare le istruzioni superflue.</span><span class="sxs-lookup"><span data-stu-id="206a9-131">The following table lists some cases where you can test conditions in your shader and use dynamic branching to skip unnecessary instructions.</span></span> <span data-ttu-id="206a9-132">La tabella non è completa.</span><span class="sxs-lookup"><span data-stu-id="206a9-132">The table not comprehensive.</span></span> <span data-ttu-id="206a9-133">Piuttosto, è destinato a fornire idee per l'ottimizzazione del codice.</span><span class="sxs-lookup"><span data-stu-id="206a9-133">Rather, it is intended to give you ideas for optimizing your code.</span></span>



| <span data-ttu-id="206a9-134">Condizione da controllare</span><span class="sxs-lookup"><span data-stu-id="206a9-134">Condition to Check</span></span>                                    | <span data-ttu-id="206a9-135">Risposta nello shader</span><span class="sxs-lookup"><span data-stu-id="206a9-135">Response in the Shader</span></span>       |
|-------------------------------------------------------|------------------------------|
| <span data-ttu-id="206a9-136">Il controllo alfa determina che un pixel non verrà visualizzato.</span><span class="sxs-lookup"><span data-stu-id="206a9-136">Alpha check determines that a pixel will not be seen.</span></span> | <span data-ttu-id="206a9-137">Ignora il resto dello shader.</span><span class="sxs-lookup"><span data-stu-id="206a9-137">Skip the rest of the shader.</span></span> |
| <span data-ttu-id="206a9-138">Il pixel o la geometria è completamente offuscata.</span><span class="sxs-lookup"><span data-stu-id="206a9-138">The pixel or geometry is fully fogged.</span></span>                | <span data-ttu-id="206a9-139">Ignora il resto dello shader.</span><span class="sxs-lookup"><span data-stu-id="206a9-139">Skip the rest of the shader.</span></span> |
| <span data-ttu-id="206a9-140">I pesi dell'interfaccia sono pari a zero.</span><span class="sxs-lookup"><span data-stu-id="206a9-140">Skin weights are zero.</span></span>                                | <span data-ttu-id="206a9-141">Ignora ossa.</span><span class="sxs-lookup"><span data-stu-id="206a9-141">Skip bones.</span></span>                  |
| <span data-ttu-id="206a9-142">Attenuazione chiara è pari a zero.</span><span class="sxs-lookup"><span data-stu-id="206a9-142">Light attenuation is zero.</span></span>                            | <span data-ttu-id="206a9-143">Ignora illuminazione.</span><span class="sxs-lookup"><span data-stu-id="206a9-143">Skip lighting.</span></span>               |
| <span data-ttu-id="206a9-144">Termine Lambertian non positivo.</span><span class="sxs-lookup"><span data-stu-id="206a9-144">Non-positive Lambertian term.</span></span>                         | <span data-ttu-id="206a9-145">Ignora illuminazione.</span><span class="sxs-lookup"><span data-stu-id="206a9-145">Skip lighting.</span></span>               |



 

## <a name="pack-variables-and-interpolants"></a><span data-ttu-id="206a9-146">Variabili Pack e Interpolants</span><span class="sxs-lookup"><span data-stu-id="206a9-146">Pack Variables and Interpolants</span></span>

<span data-ttu-id="206a9-147">Tenere presente lo spazio necessario per i dati dello shader.</span><span class="sxs-lookup"><span data-stu-id="206a9-147">Be mindful of the space required for shader data.</span></span> <span data-ttu-id="206a9-148">Comprimere la maggior parte delle informazioni in una variabile o interpolabile come possibile.</span><span class="sxs-lookup"><span data-stu-id="206a9-148">Pack as much information into a variable or interpolant as possible.</span></span> <span data-ttu-id="206a9-149">In alcuni casi, le informazioni di due variabili possono essere compresse nello spazio di memoria di una singola variabile.</span><span class="sxs-lookup"><span data-stu-id="206a9-149">Sometimes, the information from two variables can be packed into the memory space of a single variable.</span></span>

## <a name="reduce-shader-complexity"></a><span data-ttu-id="206a9-150">Ridurre la complessità dello shader</span><span class="sxs-lookup"><span data-stu-id="206a9-150">Reduce Shader Complexity</span></span>

<span data-ttu-id="206a9-151">Mantieni gli shader piccoli e semplici.</span><span class="sxs-lookup"><span data-stu-id="206a9-151">Keep your shaders small and simple.</span></span> <span data-ttu-id="206a9-152">In generale, gli shader con meno istruzioni vengono eseguiti più rapidamente degli shader con ulteriori istruzioni.</span><span class="sxs-lookup"><span data-stu-id="206a9-152">In general, shaders with fewer instructions execute more quickly than shaders with more instructions.</span></span> <span data-ttu-id="206a9-153">È anche più semplice eseguire il debug e ottimizzare gli shader più piccoli e meno complessi.</span><span class="sxs-lookup"><span data-stu-id="206a9-153">It is also easier to debug and optimize smaller, less complex shaders.</span></span>

## <a name="related-topics"></a><span data-ttu-id="206a9-154">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="206a9-154">Related Topics</span></span>

[<span data-ttu-id="206a9-155">Guida alla programmazione per HLSL</span><span class="sxs-lookup"><span data-stu-id="206a9-155">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)


## <a name="related-topics"></a><span data-ttu-id="206a9-156">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="206a9-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="206a9-157">Guida alla programmazione per HLSL</span><span class="sxs-lookup"><span data-stu-id="206a9-157">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 




