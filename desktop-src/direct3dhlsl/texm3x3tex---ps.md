---
title: texm3x3tex-PS
description: Esegue una moltiplicazione della matrice 3x3 e usa il risultato per eseguire una ricerca di trama. texm3x3tex deve essere usato con due istruzioni texm3x3pad-PS.
ms.assetid: bb61cd6f-57d0-4b2d-9186-f04f7f4d3516
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a228b61dbed22dc8d285e0fdc833de53b16e7be7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398314"
---
# <a name="texm3x3tex---ps"></a><span data-ttu-id="0ea50-104">texm3x3tex-PS</span><span class="sxs-lookup"><span data-stu-id="0ea50-104">texm3x3tex - ps</span></span>

<span data-ttu-id="0ea50-105">Esegue una moltiplicazione della matrice 3x3 e usa il risultato per eseguire una ricerca di trama.</span><span class="sxs-lookup"><span data-stu-id="0ea50-105">Performs a 3x3 matrix multiply and uses the result to do a texture lookup.</span></span> <span data-ttu-id="0ea50-106">texm3x3tex deve essere usato con due istruzioni [texm3x3pad-PS](texm3x3pad---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="0ea50-106">texm3x3tex must be used with two [texm3x3pad - ps](texm3x3pad---ps.md) instructions.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ea50-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0ea50-107">Syntax</span></span>



| <span data-ttu-id="0ea50-108">texm3x3tex DST, src</span><span class="sxs-lookup"><span data-stu-id="0ea50-108">texm3x3tex dst, src</span></span> |
|---------------------|



 

<span data-ttu-id="0ea50-109">dove</span><span class="sxs-lookup"><span data-stu-id="0ea50-109">where</span></span>

-   <span data-ttu-id="0ea50-110">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0ea50-110">dst is the destination register.</span></span>
-   <span data-ttu-id="0ea50-111">src è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="0ea50-111">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ea50-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="0ea50-112">Remarks</span></span>



| <span data-ttu-id="0ea50-113">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="0ea50-113">Pixel shader versions</span></span> | <span data-ttu-id="0ea50-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="0ea50-114">1\_1</span></span> | <span data-ttu-id="0ea50-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="0ea50-115">1\_2</span></span> | <span data-ttu-id="0ea50-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="0ea50-116">1\_3</span></span> | <span data-ttu-id="0ea50-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="0ea50-117">1\_4</span></span> | <span data-ttu-id="0ea50-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0ea50-118">2\_0</span></span> | <span data-ttu-id="0ea50-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="0ea50-119">2\_x</span></span> | <span data-ttu-id="0ea50-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0ea50-120">2\_sw</span></span> | <span data-ttu-id="0ea50-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0ea50-121">3\_0</span></span> | <span data-ttu-id="0ea50-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0ea50-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="0ea50-123">texm3x3tex</span><span class="sxs-lookup"><span data-stu-id="0ea50-123">texm3x3tex</span></span>            | <span data-ttu-id="0ea50-124">x</span><span class="sxs-lookup"><span data-stu-id="0ea50-124">x</span></span>    | <span data-ttu-id="0ea50-125">x</span><span class="sxs-lookup"><span data-stu-id="0ea50-125">x</span></span>    | <span data-ttu-id="0ea50-126">x</span><span class="sxs-lookup"><span data-stu-id="0ea50-126">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="0ea50-127">Questa istruzione viene usata come finale di tre istruzioni che rappresentano un'operazione di moltiplicazione della matrice 3x3, seguita da una ricerca di trama.</span><span class="sxs-lookup"><span data-stu-id="0ea50-127">This instruction is used as the final of three instructions representing a 3x3 matrix multiply operation, followed by a texture lookup.</span></span> <span data-ttu-id="0ea50-128">La matrice 3x3 è costituita dalle coordinate di trama della terza fase della trama e dalle due fasi di trama precedenti.</span><span class="sxs-lookup"><span data-stu-id="0ea50-128">The 3x3 matrix is comprised of the texture coordinates of the third texture stage and the two preceding texture stages.</span></span> <span data-ttu-id="0ea50-129">Il vettore a tre componenti risultante (u, v, w) viene usato per campionare la trama nella fase 3.</span><span class="sxs-lookup"><span data-stu-id="0ea50-129">The resulting three-component vector (u,v,w) is used to sample the texture in stage 3.</span></span> <span data-ttu-id="0ea50-130">Qualsiasi trama assegnata alle due fasi di trama precedenti viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="0ea50-130">Any texture assigned to the preceding two texture stages is ignored.</span></span> <span data-ttu-id="0ea50-131">La moltiplicazione della matrice 3x3 è in genere utile per orientare un vettore normale allo spazio tangente corretto per la superficie di cui viene eseguito il rendering.</span><span class="sxs-lookup"><span data-stu-id="0ea50-131">The 3x3 matrix multiply is typically useful for orienting a normal vector to the correct tangent space for the surface being rendered.</span></span>

<span data-ttu-id="0ea50-132">Questa istruzione deve essere utilizzata con l'istruzione texm3x3pad.</span><span class="sxs-lookup"><span data-stu-id="0ea50-132">This instruction must be used with the texm3x3pad instruction.</span></span> <span data-ttu-id="0ea50-133">I registri di trama devono usare la sequenza seguente.</span><span class="sxs-lookup"><span data-stu-id="0ea50-133">Texture registers must use the following sequence.</span></span>


```
 
tex t(n)                 // Define tn as a standard 3-vector (tn must
                         //   be defined in some way before it is used)
texm3x3pad t(m),   t(n)  //   where m > n
                         // Perform first row of matrix multiply
texm3x3pad t(m+1), t(n)  // Perform second row of matrix multiply
texm3x3tex t(m+2), t(n)  // Perform third row of matrix multiply to get a
                         //   3-vector with which to sample texture
                         //   associated with texture stage m+2
```



<span data-ttu-id="0ea50-134">Di seguito sono riportati altri dettagli su come viene eseguita la moltiplicazione 3x3.</span><span class="sxs-lookup"><span data-stu-id="0ea50-134">Here is more detail about how the 3x3 multiply is accomplished.</span></span>

<span data-ttu-id="0ea50-135">La prima istruzione texm3x3pad esegue la prima riga dell'istruzione Multiply per<sup>Find u.</sup></span><span class="sxs-lookup"><span data-stu-id="0ea50-135">The first texm3x3pad instruction performs the first row of the multiply to find u<sup>'</sup>.</span></span>

<span data-ttu-id="0ea50-136">u<sup>'</sup> = TextureCoordinates (fase m)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="0ea50-136">u<sup>'</sup> = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="0ea50-137">La seconda istruzione texm3x3pad esegue la seconda riga della moltiplicazione per trovare la<sup>v.</sup></span><span class="sxs-lookup"><span data-stu-id="0ea50-137">The second texm3x3pad instruction performs the second row of the multiply to find v<sup>'</sup>.</span></span>

<span data-ttu-id="0ea50-138">v<sup>'</sup> = TextureCoordinates (fase m + 1)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="0ea50-138">v<sup>'</sup> = TextureCoordinates(stage m+1)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="0ea50-139">L'istruzione texm3x3spec esegue la terza riga del moltiplicatore per<sup>trovare w.</sup></span><span class="sxs-lookup"><span data-stu-id="0ea50-139">The texm3x3spec instruction performs the third row of the multiply to find w<sup>'</sup>.</span></span>

<span data-ttu-id="0ea50-140">w<sup>'</sup> = TextureCoordinates (fase m + 2)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="0ea50-140">w<sup>'</sup> = TextureCoordinates(stage m+2)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="0ea50-141">Infine, l'istruzione texm3x3tex Samples t (m + 2) with (u<sup>'</sup>, v<sup>'</sup>, w<sup>'</sup>) e archivia il risultato in t (m + 2).</span><span class="sxs-lookup"><span data-stu-id="0ea50-141">Lastly, the texm3x3tex instruction samples t(m+2) with (u<sup>'</sup>,v<sup>'</sup>,w<sup>'</sup>) and stores the result in t(m+2).</span></span>

<span data-ttu-id="0ea50-142">t (m + 2)<sub>RGBA</sub> = TextureSample (stage m + 2)<sub>RGBA</sub> using (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) come coordinates.</span><span class="sxs-lookup"><span data-stu-id="0ea50-142">t(m+2)<sub>RGBA</sub> = TextureSample(stage m+2)<sub>RGBA</sub> using (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) as coordinates.</span></span>

## <a name="examples"></a><span data-ttu-id="0ea50-143">Esempio</span><span class="sxs-lookup"><span data-stu-id="0ea50-143">Examples</span></span>

<span data-ttu-id="0ea50-144">Di seguito è riportato un esempio di shader con le mappe di trama identificate e le fasi di trama identificate.</span><span class="sxs-lookup"><span data-stu-id="0ea50-144">Here is an example shader with the texture maps identified and the texture stages identified.</span></span>


```
ps_1_1
tex t0                // Bind texture in stage 0 to register t0
texm3x3pad  t1,  t0   // First row of matrix multiply
texm3x3pad  t2,  t0   // Second row of matrix multiply
texm3x3tex  t3,  t0   // Third row of matrix multiply to get a
                      // 3-vector with which to sample texture at 
mov r0, t3            // stage 3 output result
```



<span data-ttu-id="0ea50-145">Questo esempio richiede la seguente configurazione della fase di trama.</span><span class="sxs-lookup"><span data-stu-id="0ea50-145">This example requires the following texture stage setup.</span></span>

-   <span data-ttu-id="0ea50-146">Alla fase 0 viene assegnata una mappa di trama con dati normali.</span><span class="sxs-lookup"><span data-stu-id="0ea50-146">Stage 0 is assigned a texture map with normal data.</span></span> <span data-ttu-id="0ea50-147">Questa operazione viene spesso definita mappa Bump.</span><span class="sxs-lookup"><span data-stu-id="0ea50-147">This is often referred to as a bump map.</span></span> <span data-ttu-id="0ea50-148">I dati sono normali (XYZ) per ogni Texel.</span><span class="sxs-lookup"><span data-stu-id="0ea50-148">The data is (XYZ) normals for each texel.</span></span> <span data-ttu-id="0ea50-149">Il set di coordinate di trama 0 definisce come campionare questa mappa normale.</span><span class="sxs-lookup"><span data-stu-id="0ea50-149">Texture coordinate set 0 defines how to sample this normal map.</span></span>
-   <span data-ttu-id="0ea50-150">Il set di coordinate di trama 1 viene assegnato alla riga 1 della matrice 3x3.</span><span class="sxs-lookup"><span data-stu-id="0ea50-150">Texture coordinate set 1 is assigned to row 1 of the 3x3 matrix.</span></span> <span data-ttu-id="0ea50-151">Qualsiasi trama assegnata alla fase 1 viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="0ea50-151">Any texture assigned to stage 1 is ignored.</span></span>
-   <span data-ttu-id="0ea50-152">Il set 2 della coordinata di trama viene assegnato alla riga 2 della matrice 3x3.</span><span class="sxs-lookup"><span data-stu-id="0ea50-152">Texture coordinate set 2 is assigned to row 2 of the 3x3 matrix.</span></span> <span data-ttu-id="0ea50-153">Qualsiasi trama assegnata alla fase 2 viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="0ea50-153">Any texture assigned to stage 2 is ignored.</span></span>
-   <span data-ttu-id="0ea50-154">Il set di coordinate di trama 3 viene assegnato alla riga 3 della matrice 3x3.</span><span class="sxs-lookup"><span data-stu-id="0ea50-154">Texture coordinate set 3 is assigned to row 3 of the 3x3 matrix.</span></span> <span data-ttu-id="0ea50-155">È necessario impostare una trama del volume o del cubo sulla fase 3 per la ricerca tramite il vettore 3D trasformato.</span><span class="sxs-lookup"><span data-stu-id="0ea50-155">A volume or cube texture should be set to stage 3 for lookup by the transformed 3D vector.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ea50-156">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0ea50-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ea50-157">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="0ea50-157">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




