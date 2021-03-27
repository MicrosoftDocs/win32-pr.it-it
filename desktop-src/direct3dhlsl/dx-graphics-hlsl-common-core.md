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
ms.openlocfilehash: e27ebe7d908c473890ac5b851eac3e0bc840c859
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855722"
---
# <a name="common-shader-core"></a><span data-ttu-id="8f3df-103">Common-Shader Core</span><span class="sxs-lookup"><span data-stu-id="8f3df-103">Common-Shader Core</span></span>

<span data-ttu-id="8f3df-104">In Shader Model 4, tutte le fasi dello shader implementano la stessa funzionalità di base usando un core shader comune.</span><span class="sxs-lookup"><span data-stu-id="8f3df-104">In Shader Model 4, all shader stages implement the same base functionality using a common-shader core.</span></span> <span data-ttu-id="8f3df-105">Inoltre, ognuna delle tre fasi dello shader (vertice, geometria e pixel) offre funzionalità univoche per ogni fase, ad esempio la possibilità di generare nuove primitive dalla fase geometry shader o di rimuovere un pixel specifico nella fase pixel shader.</span><span class="sxs-lookup"><span data-stu-id="8f3df-105">In addition, each of the three shader stages (vertex, geometry, and pixel) offer functionality unique to each stage, such as the ability to generate new primitives from the geometry shader stage or to discard a specific pixel in the pixel shader stage.</span></span> <span data-ttu-id="8f3df-106">Il diagramma seguente illustra il flusso dei dati attraverso una fase dello shader e la relazione tra il nucleo di shader comune e le risorse di memoria dello shader.</span><span class="sxs-lookup"><span data-stu-id="8f3df-106">The following diagram shows how data flows through a shader stage, and the relationship of the common-shader core with shader memory resources.</span></span>

![diagramma del flusso di dati in una fase dello shader](images/d3d10-shader-unit.png)

-   <span data-ttu-id="8f3df-108">**Dati di input**: un vertex shader riceve gli input dalla fase dell'assembler di input. la geometria e i pixel shader ricevono gli input dalla fase precedente dello shader.</span><span class="sxs-lookup"><span data-stu-id="8f3df-108">**Input Data**: A vertex shader receives its inputs from the input assembler stage; geometry and pixel shaders receive their inputs from the previous shader stage.</span></span> <span data-ttu-id="8f3df-109">Gli input aggiuntivi includono la [semantica dei valori di sistema](dx-graphics-hlsl-semantics.md), che possono essere utilizzati dalla prima unità nella pipeline a cui sono applicabili.</span><span class="sxs-lookup"><span data-stu-id="8f3df-109">Additional inputs include [system-value semantics](dx-graphics-hlsl-semantics.md), which are consumable by the first unit in the pipeline to which they are applicable.</span></span>
-   <span data-ttu-id="8f3df-110">**Dati di output**: gli shader generano i risultati di output da passare alla fase successiva nella pipeline.</span><span class="sxs-lookup"><span data-stu-id="8f3df-110">**Output Data**: Shaders generate output results to be passed onto the subsequent stage in the pipeline.</span></span> <span data-ttu-id="8f3df-111">Per un geometry shader, la quantità di output di dati da una singola chiamata può variare.</span><span class="sxs-lookup"><span data-stu-id="8f3df-111">For a geometry shader, the amount of data output from a single invocation can vary.</span></span> <span data-ttu-id="8f3df-112">Alcuni output sono interpretati da Common-shader core, ad esempio la posizione del vertice e l'indice della matrice di destinazione di rendering, altri sono progettati per essere interpretati da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8f3df-112">Some outputs are interpreted by the common-shader core (such as vertex position and render-target-array index), others are designed to be interpreted by an application.</span></span>
-   <span data-ttu-id="8f3df-113">**Codice shader**: gli shader possono leggere dalla memoria, eseguire operazioni aritmetiche a virgola mobile e numeri interi o operazioni di controllo di flusso.</span><span class="sxs-lookup"><span data-stu-id="8f3df-113">**Shader Code**: Shaders can read from memory, perform vector floating point and integer arithmetic operations, or flow control operations.</span></span> <span data-ttu-id="8f3df-114">Non esiste alcun limite al numero di istruzioni che possono essere implementate in uno shader.</span><span class="sxs-lookup"><span data-stu-id="8f3df-114">There is no limit to the number of statements that can be implemented in a shader.</span></span>
-   <span data-ttu-id="8f3df-115">**Samplers**: i sampler definiscono le modalità di campionamento e filtro delle trame.</span><span class="sxs-lookup"><span data-stu-id="8f3df-115">**Samplers**: Samplers define how to sample and filter textures.</span></span> <span data-ttu-id="8f3df-116">È possibile associare un massimo di 16 campioni a uno shader simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="8f3df-116">As many as 16 samplers can be bound to a shader simultaneously.</span></span>
-   <span data-ttu-id="8f3df-117">**Trame**: è possibile filtrare le trame usando i sampler o leggere direttamente in base a Texel con la funzione intrinseca [Load](dx-graphics-hlsl-to-load.md) .</span><span class="sxs-lookup"><span data-stu-id="8f3df-117">**Textures**: Textures can be filtered using samplers or read on a per-texel basis directly with the [load](dx-graphics-hlsl-to-load.md) intrinsic function.</span></span>
-   <span data-ttu-id="8f3df-118">**Buffer**: i buffer non vengono mai filtrati, ma possono essere letti dalla memoria in base a ogni elemento direttamente con la funzione intrinseca [Load](dx-graphics-hlsl-to-load.md) .</span><span class="sxs-lookup"><span data-stu-id="8f3df-118">**Buffers**: Buffers are never filtered, but can be read from memory on a per-element basis directly with the [load](dx-graphics-hlsl-to-load.md) intrinsic function.</span></span> <span data-ttu-id="8f3df-119">Fino a un massimo di 128, le risorse di trama e buffer (combinate) possono essere associate contemporaneamente a uno shader.</span><span class="sxs-lookup"><span data-stu-id="8f3df-119">As many as 128 texture and buffer resources (combined) can be bound to a shader simultaneously.</span></span>
-   <span data-ttu-id="8f3df-120">**Buffer costanti**: i buffer costanti sono ottimizzati per le variabili costanti dello shader.</span><span class="sxs-lookup"><span data-stu-id="8f3df-120">**Constant Buffers**: Constant buffers are optimized for shader constant-variables.</span></span> <span data-ttu-id="8f3df-121">Fino a un massimo di 16 buffer costanti è possibile associare contemporaneamente una fase dello shader.</span><span class="sxs-lookup"><span data-stu-id="8f3df-121">As many as 16 constant buffers can be bound to a shader stage simultaneously.</span></span> <span data-ttu-id="8f3df-122">Sono progettate per un aggiornamento più frequente dalla CPU; Pertanto, presentano restrizioni di dimensioni, layout e accesso aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="8f3df-122">They are designed for more frequent update from the CPU; therefore, they have additional size, layout, and access restrictions.</span></span>



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f3df-123">Differenze tra Direct3D 9 e Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="8f3df-123">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="8f3df-124">In Direct3D 9 ogni unità shader aveva un singolo file di registro costante di piccole dimensioni per archiviare tutte le variabili di shader costanti.</span><span class="sxs-lookup"><span data-stu-id="8f3df-124">In Direct3D 9, each shader unit had a single, small constant register file to store all constant shader variables.</span></span> <span data-ttu-id="8f3df-125">Per ospitare tutti gli shader con questo spazio costante limitato è necessario riciclo frequente delle costanti da parte della CPU.</span><span class="sxs-lookup"><span data-stu-id="8f3df-125">Accommodating all shaders with this limited constant space required frequent recycling of constants by the CPU.</span></span><br/> <span data-ttu-id="8f3df-126">In Direct3D 10, le costanti vengono archiviate in buffer non modificabili in memoria e vengono gestite come qualsiasi altra risorsa.</span><span class="sxs-lookup"><span data-stu-id="8f3df-126">In Direct3D 10, constants are stored in immutable buffers in memory and are managed like any other resource.</span></span> <span data-ttu-id="8f3df-127">Non esiste alcun limite al numero di buffer costanti che un'applicazione può creare.</span><span class="sxs-lookup"><span data-stu-id="8f3df-127">There is no limit to the number of constant buffers an application can create.</span></span> <span data-ttu-id="8f3df-128">Organizzando le costanti in buffer in base alla frequenza di aggiornamento e utilizzo, la quantità di larghezza di banda necessaria per aggiornare le costanti per adattarsi a tutti gli shader può essere notevolmente ridotta.</span><span class="sxs-lookup"><span data-stu-id="8f3df-128">By organizing constants into buffers by frequency of update and usage, the amount of bandwidth required to update constants to accommodate all shaders can be significantly reduced.</span></span><br/> |



 

## <a name="integer-and-bitwise-support"></a><span data-ttu-id="8f3df-129">Supporto Integer e bit per bit</span><span class="sxs-lookup"><span data-stu-id="8f3df-129">Integer and Bitwise Support</span></span>

<span data-ttu-id="8f3df-130">Common shader Core offre un set completo di operazioni bit per bit conformi a IEEE e a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="8f3df-130">The common shader core provides a full set of IEEE-compliant 32-bit integer and bitwise operations.</span></span> <span data-ttu-id="8f3df-131">Queste operazioni abilitano una nuova classe di algoritmi negli esempi di hardware grafico sono le tecniche di compressione e compressione, FFT e il controllo del flusso del programma bit.</span><span class="sxs-lookup"><span data-stu-id="8f3df-131">These operations enable a new class of algorithms in graphics hardware examples include compression and packing techniques, FFTs, and bitfield program-flow control.</span></span>

<span data-ttu-id="8f3df-132">I tipi di dati **int** e **uint** in Direct3D 10 HLSL vengono mappati a interi a 32 bit nell'hardware.</span><span class="sxs-lookup"><span data-stu-id="8f3df-132">The **int** and **uint** data types in Direct3D 10 HLSL map to 32-bit integers in hardware.</span></span>



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f3df-133">Differenze tra Direct3D 9 e Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="8f3df-133">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="8f3df-134">Negli input di flusso Direct3D 9 contrassegnati come Integer in HLSL sono stati interpretati come virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="8f3df-134">In Direct3D 9 stream inputs marked as integer in HLSL were interpreted as floating-point.</span></span> <span data-ttu-id="8f3df-135">In Direct3D 10, gli input di flusso contrassegnati come Integer vengono interpretati come Integer a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="8f3df-135">In Direct3D 10, stream inputs marked as integer are interpreted as a 32- bit integer.</span></span><br/> <span data-ttu-id="8f3df-136">Inoltre, i valori booleani sono ora tutti impostati su bit oppure tutti i bit non vengono impostati.</span><span class="sxs-lookup"><span data-stu-id="8f3df-136">In addition, boolean values are now all bits set or all bits unset.</span></span> <span data-ttu-id="8f3df-137">I dati convertiti in **bool** verranno interpretati come true se il valore non è uguale a 0,0 f (il valore zero positivo e negativo possono essere false) e false in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="8f3df-137">Data converted to **bool** will be interpreted as true if the value is not equal to 0.0f (both positive and negative zero are allowed to be false) and false otherwise.</span></span><br/> |



 

## <a name="bitwise-operators"></a><span data-ttu-id="8f3df-138">Operatori bit per bit</span><span class="sxs-lookup"><span data-stu-id="8f3df-138">Bitwise operators</span></span>

<span data-ttu-id="8f3df-139">Common shader Core supporta gli operatori bit per bit seguenti:</span><span class="sxs-lookup"><span data-stu-id="8f3df-139">The common shader core supports the following bitwise operators:</span></span>



| <span data-ttu-id="8f3df-140">Operatore</span><span class="sxs-lookup"><span data-stu-id="8f3df-140">Operator</span></span>  | <span data-ttu-id="8f3df-141">Funzione</span><span class="sxs-lookup"><span data-stu-id="8f3df-141">Function</span></span>          |
|-----------|-------------------|
| ~         | <span data-ttu-id="8f3df-142">Not logico</span><span class="sxs-lookup"><span data-stu-id="8f3df-142">Logical Not</span></span>       |
| <<  | <span data-ttu-id="8f3df-143">Spostamento a sinistra</span><span class="sxs-lookup"><span data-stu-id="8f3df-143">Left Shift</span></span>        |
| >>  | <span data-ttu-id="8f3df-144">Spostamento a destra</span><span class="sxs-lookup"><span data-stu-id="8f3df-144">Right Shift</span></span>       |
| &         | <span data-ttu-id="8f3df-145">And logico</span><span class="sxs-lookup"><span data-stu-id="8f3df-145">Logical And</span></span>       |
| \|        | <span data-ttu-id="8f3df-146">Esegue un'operazione di Or logico.</span><span class="sxs-lookup"><span data-stu-id="8f3df-146">Logical Or</span></span>        |
| ^         | <span data-ttu-id="8f3df-147">XOR logico</span><span class="sxs-lookup"><span data-stu-id="8f3df-147">Logical Xor</span></span>       |
| <<= | <span data-ttu-id="8f3df-148">Spostamento a sinistra uguale</span><span class="sxs-lookup"><span data-stu-id="8f3df-148">Left shift Equal</span></span>  |
| >>= | <span data-ttu-id="8f3df-149">Spostamento a destra uguale</span><span class="sxs-lookup"><span data-stu-id="8f3df-149">Right Shift Equal</span></span> |
| &=        | <span data-ttu-id="8f3df-150">E uguale a</span><span class="sxs-lookup"><span data-stu-id="8f3df-150">And Equal</span></span>         |
| \|=       | <span data-ttu-id="8f3df-151">O uguale a</span><span class="sxs-lookup"><span data-stu-id="8f3df-151">Or Equal</span></span>          |
| ^=        | <span data-ttu-id="8f3df-152">XOR uguale</span><span class="sxs-lookup"><span data-stu-id="8f3df-152">Xor Equal</span></span>         |



 

<span data-ttu-id="8f3df-153">Gli operatori bit per bit vengono definiti per operare solo sui tipi di dati **int** e **uint** .</span><span class="sxs-lookup"><span data-stu-id="8f3df-153">Bitwise operators are defined to operate only on **int** and **uint** data types.</span></span> <span data-ttu-id="8f3df-154">Il tentativo di utilizzare operatori bit per bit sui tipi di dati **float** o **struct** genererà un errore.</span><span class="sxs-lookup"><span data-stu-id="8f3df-154">Attempting to use bitwise operators on **float** or **struct** data types will result in an error.</span></span> <span data-ttu-id="8f3df-155">Gli operatori bit per bit seguono la stessa precedenza di C rispetto ad altri operatori.</span><span class="sxs-lookup"><span data-stu-id="8f3df-155">Bitwise operators follow the same precedence as C with regard to other operators.</span></span>

## <a name="binary-casts"></a><span data-ttu-id="8f3df-156">Cast binari</span><span class="sxs-lookup"><span data-stu-id="8f3df-156">Binary Casts</span></span>

<span data-ttu-id="8f3df-157">Eseguendo il cast tra un Integer e un tipo a virgola mobile, il valore numerico viene convertito dopo le regole di troncamento C.</span><span class="sxs-lookup"><span data-stu-id="8f3df-157">Casting between an integer and a floating-point type will convert the numeric value following C truncation rules.</span></span> <span data-ttu-id="8f3df-158">Il cast di un valore da un valore **float**, a un valore **int** e **viceversa è una** conversione con perdita di dati dipendente dalla precisione del tipo di dati di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8f3df-158">Casting a value from a **float**, to an **int**, and back to a **float** is a lossy conversion dependent on the precision of the target data type.</span></span> <span data-ttu-id="8f3df-159">Di seguito sono riportate alcune delle funzioni di conversione: [**AsFloat (DirectX HLSL)**](dx-graphics-hlsl-asfloat.md), [**AsInt (DirectX HLSL)**](dx-graphics-hlsl-asint.md), [**asuint (DirectX HLSL)**](dx-graphics-hlsl-asuint.md).</span><span class="sxs-lookup"><span data-stu-id="8f3df-159">Here are some of the conversion functions: [**asfloat (DirectX HLSL)**](dx-graphics-hlsl-asfloat.md), [**asint (DirectX HLSL)**](dx-graphics-hlsl-asint.md), [**asuint (DirectX HLSL)**](dx-graphics-hlsl-asuint.md).</span></span>

<span data-ttu-id="8f3df-160">I cast binari possono essere eseguiti anche usando funzioni intrinseche HLSL.</span><span class="sxs-lookup"><span data-stu-id="8f3df-160">Binary casts can also be performed using HLSL intrinsic functions.</span></span> <span data-ttu-id="8f3df-161">In questo modo il compilatore reinterpreta la rappresentazione di bit di un numero nel tipo di dati di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8f3df-161">These cause the compiler to reinterpret the bit representation of a number into the target data type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8f3df-162">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8f3df-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f3df-163">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="8f3df-163">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 





