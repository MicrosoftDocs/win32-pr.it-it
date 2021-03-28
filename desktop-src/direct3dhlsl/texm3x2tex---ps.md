---
title: texm3x2tex-PS
description: Esegue la riga finale di una matrice 3x2 moltiplicata e utilizza il risultato per eseguire una ricerca di trama. texm3x2tex deve essere usato in combinazione con l'istruzione texm3x2pad-PS.
ms.assetid: c6cfbf75-4a63-4c82-9fb6-286b51b7f883
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 62206bc4ef1e1b64ec760a240a087ec13526d896
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993093"
---
# <a name="texm3x2tex---ps"></a><span data-ttu-id="3c56c-104">texm3x2tex-PS</span><span class="sxs-lookup"><span data-stu-id="3c56c-104">texm3x2tex - ps</span></span>

<span data-ttu-id="3c56c-105">Esegue la riga finale di una matrice 3x2 moltiplicata e utilizza il risultato per eseguire una ricerca di trama.</span><span class="sxs-lookup"><span data-stu-id="3c56c-105">Performs the final row of a 3x2 matrix multiply and uses the result to do a texture lookup.</span></span> <span data-ttu-id="3c56c-106">texm3x2tex deve essere usato in combinazione con l'istruzione [texm3x2pad-PS](texm3x2pad---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="3c56c-106">texm3x2tex must be used in conjunction with the [texm3x2pad - ps](texm3x2pad---ps.md) instruction.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c56c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3c56c-107">Syntax</span></span>



| <span data-ttu-id="3c56c-108">texm3x2tex DST, src</span><span class="sxs-lookup"><span data-stu-id="3c56c-108">texm3x2tex dst, src</span></span> |
|---------------------|



 

<span data-ttu-id="3c56c-109">dove</span><span class="sxs-lookup"><span data-stu-id="3c56c-109">where</span></span>

-   <span data-ttu-id="3c56c-110">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3c56c-110">dst is the destination register.</span></span>
-   <span data-ttu-id="3c56c-111">src è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="3c56c-111">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c56c-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="3c56c-112">Remarks</span></span>



| <span data-ttu-id="3c56c-113">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="3c56c-113">Pixel shader versions</span></span> | <span data-ttu-id="3c56c-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="3c56c-114">1\_1</span></span> | <span data-ttu-id="3c56c-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="3c56c-115">1\_2</span></span> | <span data-ttu-id="3c56c-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="3c56c-116">1\_3</span></span> | <span data-ttu-id="3c56c-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="3c56c-117">1\_4</span></span> | <span data-ttu-id="3c56c-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3c56c-118">2\_0</span></span> | <span data-ttu-id="3c56c-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3c56c-119">2\_x</span></span> | <span data-ttu-id="3c56c-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3c56c-120">2\_sw</span></span> | <span data-ttu-id="3c56c-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3c56c-121">3\_0</span></span> | <span data-ttu-id="3c56c-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3c56c-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="3c56c-123">texm3x2tex</span><span class="sxs-lookup"><span data-stu-id="3c56c-123">texm3x2tex</span></span>            | <span data-ttu-id="3c56c-124">x</span><span class="sxs-lookup"><span data-stu-id="3c56c-124">x</span></span>    | <span data-ttu-id="3c56c-125">x</span><span class="sxs-lookup"><span data-stu-id="3c56c-125">x</span></span>    | <span data-ttu-id="3c56c-126">x</span><span class="sxs-lookup"><span data-stu-id="3c56c-126">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="3c56c-127">L'istruzione viene utilizzata come una delle due istruzioni che rappresentano un'operazione di moltiplicazione della matrice 3x2.</span><span class="sxs-lookup"><span data-stu-id="3c56c-127">The instruction is used as one of two instructions representing a 3x2 matrix multiply operation.</span></span> <span data-ttu-id="3c56c-128">Questa istruzione deve essere usata con l'istruzione [texm3x2pad-PS](texm3x2pad---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="3c56c-128">This instruction must be used with the [texm3x2pad - ps](texm3x2pad---ps.md) instruction.</span></span>

<span data-ttu-id="3c56c-129">Quando si usano queste due istruzioni, i registri di trama devono usare la sequenza seguente.</span><span class="sxs-lookup"><span data-stu-id="3c56c-129">When using these two instructions, texture registers must use the following sequence.</span></span>


```
 
tex t(n)                      // Define tn as a standard 3-vector (tn must 
                              // be defined in some way before it is used)
texm3x2pad  t(m),   t(n)      // where m > n
                              // Perform first row of matrix multiply
texm3x2tex  t(m+1), t(n)      // Perform second row of matrix multiply 
                              // to get (u,v) to sample texture 
                              // associated with stage m+1
```



<span data-ttu-id="3c56c-130">Ecco altri dettagli sul modo in cui viene eseguita la moltiplicazione 3x2.</span><span class="sxs-lookup"><span data-stu-id="3c56c-130">Here is more detail about how the 3x2 multiply is accomplished.</span></span>

<span data-ttu-id="3c56c-131">L'istruzione texm3x2pad esegue la prima riga dell'istruzione Multiply per<sup>Find u.</sup></span><span class="sxs-lookup"><span data-stu-id="3c56c-131">The texm3x2pad instruction performs the first row of the multiply to find u<sup>'</sup>.</span></span>

<span data-ttu-id="3c56c-132">u<sup>'</sup> = t (n)<sub>RGB</sub> \* TextureCoordinates (fase m)<sub>UVW</sub></span><span class="sxs-lookup"><span data-stu-id="3c56c-132">u<sup>'</sup> = t(n)<sub>RGB</sub> \* TextureCoordinates(stage m)<sub>UVW</sub></span></span>

<span data-ttu-id="3c56c-133">L'istruzione texm3x2tex esegue la seconda riga della moltiplicazione per trovare la<sup>v.</sup></span><span class="sxs-lookup"><span data-stu-id="3c56c-133">The texm3x2tex instruction performs the second row of the multiply to find v<sup>'</sup>.</span></span>

<span data-ttu-id="3c56c-134">v<sup>'</sup> = t (n)<sub>RGB</sub> \* TextureCoordinates (stage m + 1)<sub>UVW</sub></span><span class="sxs-lookup"><span data-stu-id="3c56c-134">v<sup>'</sup> = t(n)<sub>RGB</sub> \* TextureCoordinates(stage m+1)<sub>UVW</sub></span></span>

<span data-ttu-id="3c56c-135">L'istruzione texm3x2tex esegue il campionamento della trama sulla fase (m + 1) con (u<sup>'</sup>, v<sup>'</sup>) e archivia il risultato in t (m + 1).</span><span class="sxs-lookup"><span data-stu-id="3c56c-135">The texm3x2tex instruction samples the texture on stage (m+1) with (u<sup>'</sup>,v<sup>'</sup>) and stores the result in t(m+1).</span></span>

<span data-ttu-id="3c56c-136">t (m + 1)<sub>RGB</sub> = TextureSample (stage m + 1)<sub>RGB</sub> using (u<sup>'</sup>, v<sup>'</sup> ) As coordinates</span><span class="sxs-lookup"><span data-stu-id="3c56c-136">t(m+1)<sub>RGB</sub> = TextureSample(stage m+1)<sub>RGB</sub> using (u<sup>'</sup>, v<sup>'</sup> ) as coordinates</span></span>

## <a name="examples"></a><span data-ttu-id="3c56c-137">Esempio</span><span class="sxs-lookup"><span data-stu-id="3c56c-137">Examples</span></span>

<span data-ttu-id="3c56c-138">Di seguito è riportato un esempio di shader con le mappe di trama e le fasi di trama identificate.</span><span class="sxs-lookup"><span data-stu-id="3c56c-138">Here is an example shader with the texture maps and the texture stages identified.</span></span>


```
ps_1_1
tex t0                // Bind texture in stage 0 to register t0
texm3x2pad  t1,  t0   // First row of matrix multiply
texm3x2tex  t2,  t0   // Second row of matrix multiply to get (u,v)
                      // with which to sample texture in stage 2
mov r0, t2            // Output result
```



<span data-ttu-id="3c56c-139">Questo esempio richiede le seguenti trame nelle fasi di trama seguenti.</span><span class="sxs-lookup"><span data-stu-id="3c56c-139">This example requires the following textures in the following texture stages.</span></span>

-   <span data-ttu-id="3c56c-140">La fase 0 accetta una mappa con i dati di perturbazione (x, y, z).</span><span class="sxs-lookup"><span data-stu-id="3c56c-140">Stage 0 takes a map with (x,y,z) perturbation data.</span></span>
-   <span data-ttu-id="3c56c-141">La fase 1 include le coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="3c56c-141">Stage 1 holds texture coordinates.</span></span> <span data-ttu-id="3c56c-142">Non è necessaria alcuna trama nella fase della trama.</span><span class="sxs-lookup"><span data-stu-id="3c56c-142">No texture is required in the texture stage.</span></span>
-   <span data-ttu-id="3c56c-143">La fase 2 include entrambe le coordinate di trama e un set di trame 2D in quella fase della trama.</span><span class="sxs-lookup"><span data-stu-id="3c56c-143">Stage 2 holds both texture coordinates as well as a 2D texture set at that texture stage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c56c-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3c56c-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c56c-145">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="3c56c-145">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




