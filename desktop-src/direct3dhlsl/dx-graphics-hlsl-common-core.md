---
title: Common-Shader Core
description: Common-Shader Core
ms.assetid: f3cf2969-83a4-461f-8177-d336536194ba
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 66c1f763c4771a8406acd2f3401445d1a29cde79
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129718"
---
# <a name="common-shader-core"></a><span data-ttu-id="acee5-103">Common-Shader Core</span><span class="sxs-lookup"><span data-stu-id="acee5-103">Common-Shader Core</span></span>

<span data-ttu-id="acee5-104">Nel modello shader 4 tutte le fasi dello shader implementano la stessa funzionalità di base usando un core di shader comune.</span><span class="sxs-lookup"><span data-stu-id="acee5-104">In Shader Model 4, all shader stages implement the same base functionality using a common-shader core.</span></span> <span data-ttu-id="acee5-105">Inoltre, ognuna delle tre fasi dello shader (vertice, geometria e pixel) offre funzionalità specifiche per ogni fase, ad esempio la possibilità di generare nuove primitive dalla fase geometry shader o di eliminare un pixel specifico nella fase pixel shader.</span><span class="sxs-lookup"><span data-stu-id="acee5-105">In addition, each of the three shader stages (vertex, geometry, and pixel) offer functionality unique to each stage, such as the ability to generate new primitives from the geometry shader stage or to discard a specific pixel in the pixel shader stage.</span></span> <span data-ttu-id="acee5-106">Il diagramma seguente illustra il flusso dei dati attraverso una fase dello shader e la relazione tra il core dello shader comune e le risorse di memoria dello shader.</span><span class="sxs-lookup"><span data-stu-id="acee5-106">The following diagram shows how data flows through a shader stage, and the relationship of the common-shader core with shader memory resources.</span></span>

![diagramma del flusso di dati in una fase shader](images/d3d10-shader-unit.png)

-   <span data-ttu-id="acee5-108">**Dati di input:** un vertex shader riceve gli input dalla fase dell'assembler di input. I geometry shader e i pixel shader ricevono i rispettivi input dalla fase shader precedente.</span><span class="sxs-lookup"><span data-stu-id="acee5-108">**Input Data**: A vertex shader receives its inputs from the input assembler stage; geometry and pixel shaders receive their inputs from the previous shader stage.</span></span> <span data-ttu-id="acee5-109">Gli input aggiuntivi includono [la semantica dei](dx-graphics-hlsl-semantics.md)valori di sistema, che possono essere utilizzati dalla prima unità nella pipeline a cui sono applicabili.</span><span class="sxs-lookup"><span data-stu-id="acee5-109">Additional inputs include [system-value semantics](dx-graphics-hlsl-semantics.md), which are consumable by the first unit in the pipeline to which they are applicable.</span></span>
-   <span data-ttu-id="acee5-110">**Dati di** output: gli shader generano risultati di output da passare alla fase successiva nella pipeline.</span><span class="sxs-lookup"><span data-stu-id="acee5-110">**Output Data**: Shaders generate output results to be passed onto the subsequent stage in the pipeline.</span></span> <span data-ttu-id="acee5-111">Per uno shader geometry, la quantità di dati restituiti da una singola chiamata può variare.</span><span class="sxs-lookup"><span data-stu-id="acee5-111">For a geometry shader, the amount of data output from a single invocation can vary.</span></span> <span data-ttu-id="acee5-112">Alcuni output vengono interpretati dal core dello shader comune (ad esempio la posizione del vertice e l'indice render-target-array), altri sono progettati per essere interpretati da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="acee5-112">Some outputs are interpreted by the common-shader core (such as vertex position and render-target-array index), others are designed to be interpreted by an application.</span></span>
-   <span data-ttu-id="acee5-113">**Codice shader:** gli shader possono leggere dalla memoria, eseguire operazioni a virgola mobile vettoriale e aritmetiche su interi o operazioni di controllo del flusso.</span><span class="sxs-lookup"><span data-stu-id="acee5-113">**Shader Code**: Shaders can read from memory, perform vector floating point and integer arithmetic operations, or flow control operations.</span></span> <span data-ttu-id="acee5-114">Non esiste alcun limite al numero di istruzioni che possono essere implementate in uno shader.</span><span class="sxs-lookup"><span data-stu-id="acee5-114">There is no limit to the number of statements that can be implemented in a shader.</span></span>
-   <span data-ttu-id="acee5-115">**Campionatori:** i campionatori definiscono come campionare e filtrare le trame.</span><span class="sxs-lookup"><span data-stu-id="acee5-115">**Samplers**: Samplers define how to sample and filter textures.</span></span> <span data-ttu-id="acee5-116">A uno shader possono essere associati simultaneamente fino a 16 campionatori.</span><span class="sxs-lookup"><span data-stu-id="acee5-116">As many as 16 samplers can be bound to a shader simultaneously.</span></span>
-   <span data-ttu-id="acee5-117">**Trame:** le trame possono essere filtrate usando campionatori o lette in base ai texel direttamente con la funzione intrinseca [di](dx-graphics-hlsl-to-load.md) caricamento.</span><span class="sxs-lookup"><span data-stu-id="acee5-117">**Textures**: Textures can be filtered using samplers or read on a per-texel basis directly with the [load](dx-graphics-hlsl-to-load.md) intrinsic function.</span></span>
-   <span data-ttu-id="acee5-118">**Buffer:** i buffer non vengono mai filtrati, ma possono essere letti dalla memoria in base all'elemento direttamente con la funzione intrinseca [di](dx-graphics-hlsl-to-load.md) caricamento.</span><span class="sxs-lookup"><span data-stu-id="acee5-118">**Buffers**: Buffers are never filtered, but can be read from memory on a per-element basis directly with the [load](dx-graphics-hlsl-to-load.md) intrinsic function.</span></span> <span data-ttu-id="acee5-119">A uno shader possono essere associate simultaneamente fino a 128 risorse di trama e buffer (combinate).</span><span class="sxs-lookup"><span data-stu-id="acee5-119">As many as 128 texture and buffer resources (combined) can be bound to a shader simultaneously.</span></span>
-   <span data-ttu-id="acee5-120">**Buffer costanti:** i buffer costanti sono ottimizzati per le variabili costanti shader.</span><span class="sxs-lookup"><span data-stu-id="acee5-120">**Constant Buffers**: Constant buffers are optimized for shader constant-variables.</span></span> <span data-ttu-id="acee5-121">A una fase shader possono essere associati simultaneamente fino a 16 buffer costanti.</span><span class="sxs-lookup"><span data-stu-id="acee5-121">As many as 16 constant buffers can be bound to a shader stage simultaneously.</span></span> <span data-ttu-id="acee5-122">Sono progettati per un aggiornamento più frequente dalla CPU. pertanto hanno restrizioni aggiuntive per dimensioni, layout e accesso.</span><span class="sxs-lookup"><span data-stu-id="acee5-122">They are designed for more frequent update from the CPU; therefore, they have additional size, layout, and access restrictions.</span></span>


<span data-ttu-id="acee5-123">Differenze tra Direct3D 9 e Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="acee5-123">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="acee5-124">In Direct3D 9 ogni unità shader aveva un singolo file di registro costante di piccole dimensioni per archiviare tutte le variabili di shader costanti.</span><span class="sxs-lookup"><span data-stu-id="acee5-124">In Direct3D 9, each shader unit had a single, small constant register file to store all constant shader variables.</span></span> <span data-ttu-id="acee5-125">Per ospitare tutti gli shader con questo spazio costante limitato è necessario riciclare frequentemente le costanti da parte della CPU.</span><span class="sxs-lookup"><span data-stu-id="acee5-125">Accommodating all shaders with this limited constant space required frequent recycling of constants by the CPU.</span></span>
- <span data-ttu-id="acee5-126">In Direct3D 10 le costanti vengono archiviate in buffer non modificabili in memoria e vengono gestite come qualsiasi altra risorsa.</span><span class="sxs-lookup"><span data-stu-id="acee5-126">In Direct3D 10, constants are stored in immutable buffers in memory and are managed like any other resource.</span></span> <span data-ttu-id="acee5-127">Non esiste alcun limite al numero di buffer costanti che un'applicazione può creare.</span><span class="sxs-lookup"><span data-stu-id="acee5-127">There is no limit to the number of constant buffers an application can create.</span></span> <span data-ttu-id="acee5-128">Organizzando le costanti in buffer in base alla frequenza di aggiornamento e utilizzo, la quantità di larghezza di banda necessaria per aggiornare le costanti per contenere tutti gli shader può essere notevolmente ridotta.</span><span class="sxs-lookup"><span data-stu-id="acee5-128">By organizing constants into buffers by frequency of update and usage, the amount of bandwidth required to update constants to accommodate all shaders can be significantly reduced.</span></span>



 

## <a name="integer-and-bitwise-support"></a><span data-ttu-id="acee5-129">Supporto di interi e bit per bit</span><span class="sxs-lookup"><span data-stu-id="acee5-129">Integer and Bitwise Support</span></span>

<span data-ttu-id="acee5-130">Il nucleo comune dello shader fornisce un set completo di operazioni bit per bit e interi a 32 bit conformi a IEEE.</span><span class="sxs-lookup"><span data-stu-id="acee5-130">The common shader core provides a full set of IEEE-compliant 32-bit integer and bitwise operations.</span></span> <span data-ttu-id="acee5-131">Queste operazioni abilitano una nuova classe di algoritmi negli esempi di hardware grafico, tra cui tecniche di compressione e compressione, FFT e controllo del flusso di programma dei campi di bit.</span><span class="sxs-lookup"><span data-stu-id="acee5-131">These operations enable a new class of algorithms in graphics hardware examples include compression and packing techniques, FFTs, and bitfield program-flow control.</span></span>

<span data-ttu-id="acee5-132">I **tipi di** dati int e **uint** in HLSL Direct3D 10 sono mappati a interi a 32 bit nell'hardware.</span><span class="sxs-lookup"><span data-stu-id="acee5-132">The **int** and **uint** data types in Direct3D 10 HLSL map to 32-bit integers in hardware.</span></span>



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acee5-133">Differenze tra Direct3D 9 e Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="acee5-133">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="acee5-134">In Direct3D 9 gli input del flusso contrassegnati come integer in HLSL sono stati interpretati come a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="acee5-134">In Direct3D 9 stream inputs marked as integer in HLSL were interpreted as floating-point.</span></span> <span data-ttu-id="acee5-135">In Direct3D 10 gli input di flusso contrassegnati come integer vengono interpretati come integer a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="acee5-135">In Direct3D 10, stream inputs marked as integer are interpreted as a 32- bit integer.</span></span><br/> <span data-ttu-id="acee5-136">Inoltre, i valori booleani sono ora tutti bit impostati o tutti i bit non impostati.</span><span class="sxs-lookup"><span data-stu-id="acee5-136">In addition, boolean values are now all bits set or all bits unset.</span></span> <span data-ttu-id="acee5-137">I dati convertiti in **bool** verranno interpretati come true se il valore non è uguale a 0,0f (sia lo zero positivo che quello negativo possono essere false) e false in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="acee5-137">Data converted to **bool** will be interpreted as true if the value is not equal to 0.0f (both positive and negative zero are allowed to be false) and false otherwise.</span></span><br/> |



 

## <a name="bitwise-operators"></a><span data-ttu-id="acee5-138">Operatori bit per bit</span><span class="sxs-lookup"><span data-stu-id="acee5-138">Bitwise operators</span></span>

<span data-ttu-id="acee5-139">Il nucleo comune dello shader supporta gli operatori bit per bit seguenti:</span><span class="sxs-lookup"><span data-stu-id="acee5-139">The common shader core supports the following bitwise operators:</span></span>



| <span data-ttu-id="acee5-140">Operatore</span><span class="sxs-lookup"><span data-stu-id="acee5-140">Operator</span></span>  | <span data-ttu-id="acee5-141">Funzione</span><span class="sxs-lookup"><span data-stu-id="acee5-141">Function</span></span>          |
|-----------|-------------------|
| ~         | <span data-ttu-id="acee5-142">Not logico</span><span class="sxs-lookup"><span data-stu-id="acee5-142">Logical Not</span></span>       |
| <<  | <span data-ttu-id="acee5-143">Spostamento a sinistra</span><span class="sxs-lookup"><span data-stu-id="acee5-143">Left Shift</span></span>        |
| >>  | <span data-ttu-id="acee5-144">Spostamento a destra</span><span class="sxs-lookup"><span data-stu-id="acee5-144">Right Shift</span></span>       |
| &         | <span data-ttu-id="acee5-145">And logico</span><span class="sxs-lookup"><span data-stu-id="acee5-145">Logical And</span></span>       |
| \|        | <span data-ttu-id="acee5-146">Esegue un'operazione di Or logico.</span><span class="sxs-lookup"><span data-stu-id="acee5-146">Logical Or</span></span>        |
| ^         | <span data-ttu-id="acee5-147">Xor logico</span><span class="sxs-lookup"><span data-stu-id="acee5-147">Logical Xor</span></span>       |
| <<= | <span data-ttu-id="acee5-148">Spostamento a sinistra uguale</span><span class="sxs-lookup"><span data-stu-id="acee5-148">Left shift Equal</span></span>  |
| >>= | <span data-ttu-id="acee5-149">Right Shift Equal</span><span class="sxs-lookup"><span data-stu-id="acee5-149">Right Shift Equal</span></span> |
| &=        | <span data-ttu-id="acee5-150">Ed è uguale a</span><span class="sxs-lookup"><span data-stu-id="acee5-150">And Equal</span></span>         |
| \|=       | <span data-ttu-id="acee5-151">o uguale a</span><span class="sxs-lookup"><span data-stu-id="acee5-151">Or Equal</span></span>          |
| ^=        | <span data-ttu-id="acee5-152">Xor Uguale</span><span class="sxs-lookup"><span data-stu-id="acee5-152">Xor Equal</span></span>         |



 

<span data-ttu-id="acee5-153">Gli operatori bit per bit vengono definiti per operare solo sui **tipi di** dati int e **uint.**</span><span class="sxs-lookup"><span data-stu-id="acee5-153">Bitwise operators are defined to operate only on **int** and **uint** data types.</span></span> <span data-ttu-id="acee5-154">Il tentativo di usare operatori bit per bit **su tipi di** dati float o **struct** restituirà un errore.</span><span class="sxs-lookup"><span data-stu-id="acee5-154">Attempting to use bitwise operators on **float** or **struct** data types will result in an error.</span></span> <span data-ttu-id="acee5-155">Gli operatori bit per bit seguono la stessa precedenza di C rispetto ad altri operatori.</span><span class="sxs-lookup"><span data-stu-id="acee5-155">Bitwise operators follow the same precedence as C with regard to other operators.</span></span>

## <a name="binary-casts"></a><span data-ttu-id="acee5-156">Cast binari</span><span class="sxs-lookup"><span data-stu-id="acee5-156">Binary Casts</span></span>

<span data-ttu-id="acee5-157">Il cast tra un integer e un tipo a virgola mobile convertirà il valore numerico in base alle regole di troncamento C.</span><span class="sxs-lookup"><span data-stu-id="acee5-157">Casting between an integer and a floating-point type will convert the numeric value following C truncation rules.</span></span> <span data-ttu-id="acee5-158">Il cast di un valore **da float** a **int** e di nuovo a un **tipo float** è una conversione persa che dipende dalla precisione del tipo di dati di destinazione.</span><span class="sxs-lookup"><span data-stu-id="acee5-158">Casting a value from a **float**, to an **int**, and back to a **float** is a lossy conversion dependent on the precision of the target data type.</span></span> <span data-ttu-id="acee5-159">Ecco alcune delle funzioni di conversione: [**asfloat (DirectX HLSL),**](dx-graphics-hlsl-asfloat.md) [**asint (DirectX HLSL)**](dx-graphics-hlsl-asint.md), [**asuint (DirectX HLSL).**](dx-graphics-hlsl-asuint.md)</span><span class="sxs-lookup"><span data-stu-id="acee5-159">Here are some of the conversion functions: [**asfloat (DirectX HLSL)**](dx-graphics-hlsl-asfloat.md), [**asint (DirectX HLSL)**](dx-graphics-hlsl-asint.md), [**asuint (DirectX HLSL)**](dx-graphics-hlsl-asuint.md).</span></span>

<span data-ttu-id="acee5-160">I cast binari possono essere eseguiti anche usando funzioni intrinseche HLSL.</span><span class="sxs-lookup"><span data-stu-id="acee5-160">Binary casts can also be performed using HLSL intrinsic functions.</span></span> <span data-ttu-id="acee5-161">In questo modo il compilatore reinterpreta la rappresentazione di bit di un numero nel tipo di dati di destinazione.</span><span class="sxs-lookup"><span data-stu-id="acee5-161">These cause the compiler to reinterpret the bit representation of a number into the target data type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="acee5-162">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="acee5-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="acee5-163">Modello shader 4</span><span class="sxs-lookup"><span data-stu-id="acee5-163">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 





