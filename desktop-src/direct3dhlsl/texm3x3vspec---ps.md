---
title: texm3x3vspec-PS
description: Esegue una moltiplicazione della matrice 3x3 e usa il risultato per eseguire una ricerca di trama.
ms.assetid: 3798bc23-2929-48fe-93ae-5aa025823714
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 28f1ee1ddb0193f9ccdaa4976e4963e748091f37
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103956079"
---
# <a name="texm3x3vspec---ps"></a><span data-ttu-id="6a046-103">texm3x3vspec-PS</span><span class="sxs-lookup"><span data-stu-id="6a046-103">texm3x3vspec - ps</span></span>

<span data-ttu-id="6a046-104">Esegue una moltiplicazione della matrice 3x3 e usa il risultato per eseguire una ricerca di trama.</span><span class="sxs-lookup"><span data-stu-id="6a046-104">Performs a 3x3 matrix multiply and uses the result to perform a texture lookup.</span></span> <span data-ttu-id="6a046-105">Questo può essere usato per la reflection speculare e il mapping dell'ambiente in cui il vettore degli occhi non è costante.</span><span class="sxs-lookup"><span data-stu-id="6a046-105">This can be used for specular reflection and environment mapping where the eye-ray vector is not constant.</span></span> <span data-ttu-id="6a046-106">texm3x3vspec deve essere usato in combinazione con due istruzioni [texm3x3pad-PS](texm3x3pad---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="6a046-106">texm3x3vspec must be used in conjunction with two [texm3x3pad - ps](texm3x3pad---ps.md) instructions.</span></span> <span data-ttu-id="6a046-107">Se il vettore di raggi occhio è costante, l'istruzione [texm3x3spec-PS](texm3x3spec---ps.md) eseguirà la stessa moltiplicazione della matrice e la stessa ricerca della trama.</span><span class="sxs-lookup"><span data-stu-id="6a046-107">If the eye-ray vector is constant, the [texm3x3spec - ps](texm3x3spec---ps.md) instruction will perform the same matrix multiply and texture lookup.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a046-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6a046-108">Syntax</span></span>



| <span data-ttu-id="6a046-109">texm3x3vspec DST, src</span><span class="sxs-lookup"><span data-stu-id="6a046-109">texm3x3vspec dst, src</span></span> |
|-----------------------|



 

<span data-ttu-id="6a046-110">dove</span><span class="sxs-lookup"><span data-stu-id="6a046-110">where</span></span>

-   <span data-ttu-id="6a046-111">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="6a046-111">dst is the destination register.</span></span>
-   <span data-ttu-id="6a046-112">src è un registro di origine.</span><span class="sxs-lookup"><span data-stu-id="6a046-112">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a046-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="6a046-113">Remarks</span></span>



| <span data-ttu-id="6a046-114">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="6a046-114">Pixel shader versions</span></span> | <span data-ttu-id="6a046-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="6a046-115">1\_1</span></span> | <span data-ttu-id="6a046-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="6a046-116">1\_2</span></span> | <span data-ttu-id="6a046-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="6a046-117">1\_3</span></span> | <span data-ttu-id="6a046-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="6a046-118">1\_4</span></span> | <span data-ttu-id="6a046-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6a046-119">2\_0</span></span> | <span data-ttu-id="6a046-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="6a046-120">2\_x</span></span> | <span data-ttu-id="6a046-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="6a046-121">2\_sw</span></span> | <span data-ttu-id="6a046-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6a046-122">3\_0</span></span> | <span data-ttu-id="6a046-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="6a046-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="6a046-124">texm3x3vspec</span><span class="sxs-lookup"><span data-stu-id="6a046-124">texm3x3vspec</span></span>          | <span data-ttu-id="6a046-125">x</span><span class="sxs-lookup"><span data-stu-id="6a046-125">x</span></span>    | <span data-ttu-id="6a046-126">x</span><span class="sxs-lookup"><span data-stu-id="6a046-126">x</span></span>    | <span data-ttu-id="6a046-127">x</span><span class="sxs-lookup"><span data-stu-id="6a046-127">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="6a046-128">Questa istruzione esegue la riga finale di un'operazione di moltiplicazione della matrice 3x3, interpreta il vettore risultante come vettore normale per riflettere un vettore di occhi, quindi usa il vettore riflesso come un indirizzo di trama per una ricerca di trama.</span><span class="sxs-lookup"><span data-stu-id="6a046-128">This instruction performs the final row of a 3x3 matrix multiply operation, interprets the resulting vector as a normal vector to reflect an eye-ray vector, and then uses the reflected vector as a texture address for a texture lookup.</span></span> <span data-ttu-id="6a046-129">Funziona esattamente come [texm3x3spec-PS](texm3x3spec---ps.md), tranne per il fatto che il vettore di tipo Eye-Ray viene tratto dal quarto componente delle coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="6a046-129">It works just like [texm3x3spec - ps](texm3x3spec---ps.md), except that the eye-ray vector is taken from the fourth component of the texture coordinates.</span></span> <span data-ttu-id="6a046-130">La moltiplicazione della matrice 3x3 è in genere utile per orientare un vettore normale allo spazio tangente corretto per la superficie di cui viene eseguito il rendering.</span><span class="sxs-lookup"><span data-stu-id="6a046-130">The 3x3 matrix multiply is typically useful for orienting a normal vector to the correct tangent space for the surface being rendered.</span></span>

<span data-ttu-id="6a046-131">La matrice 3x3 è costituita dalle coordinate di trama della terza fase della trama e dalle due fasi di trama precedenti.</span><span class="sxs-lookup"><span data-stu-id="6a046-131">The 3x3 matrix is comprised of the texture coordinates of the third texture stage and the two preceding texture stages.</span></span> <span data-ttu-id="6a046-132">Il vettore di post-Reflection risultante (UVW) viene usato per campionare la trama nella fase 3.</span><span class="sxs-lookup"><span data-stu-id="6a046-132">The resulting post-reflection vector (UVW) is used to sample the texture in stage 3.</span></span> <span data-ttu-id="6a046-133">Qualsiasi trama assegnata alle due fasi di trama precedenti viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="6a046-133">Any texture assigned to the preceding two texture stages is ignored.</span></span>

<span data-ttu-id="6a046-134">Questa istruzione deve essere utilizzata con l'istruzione texm3x3pad.</span><span class="sxs-lookup"><span data-stu-id="6a046-134">This instruction must be used with the texm3x3pad instruction.</span></span> <span data-ttu-id="6a046-135">I registri di trama devono usare la sequenza seguente.</span><span class="sxs-lookup"><span data-stu-id="6a046-135">Texture registers must use the following sequence.</span></span>


```
tex t(n)                    // Define tn as a standard 3-vector (tn must
                            //   be defined in some way before it is used)
texm3x3pad   t(m),   t(n)   // where m > n
                            // Perform first row of matrix multiply
texm3x3pad   t(m+1), t(n)   // Perform second row of matrix multiply
texm3x3vspec t(m+2), t(n)   // Perform third row of matrix multiply
                            // Then do a texture lookup on the texture
                            // associated with texture stage m+2
```



<span data-ttu-id="6a046-136">La prima istruzione texm3x3pad esegue la prima riga dell'istruzione Multiply per<sup>Find u.</sup></span><span class="sxs-lookup"><span data-stu-id="6a046-136">The first texm3x3pad instruction performs the first row of the multiply to find u<sup>'</sup>.</span></span>

<span data-ttu-id="6a046-137">u<sup>'</sup> = TextureCoordinates (fase m)<sub>UVW</sub> \* t (n) <sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="6a046-137">u<sup>'</sup> = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n) <sub>RGB</sub></span></span>

<span data-ttu-id="6a046-138">La seconda istruzione texm3x3pad esegue la seconda riga della moltiplicazione per trovare la<sup>v.</sup></span><span class="sxs-lookup"><span data-stu-id="6a046-138">The second texm3x3pad instruction performs the second row of the multiply to find v<sup>'</sup>.</span></span>

<span data-ttu-id="6a046-139">v<sup>'</sup> = TextureCoordinates (fase m + 1)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="6a046-139">v<sup>'</sup> = TextureCoordinates(stage m+1)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="6a046-140">L'istruzione texm3x3spec esegue la terza riga del moltiplicatore per<sup>trovare w.</sup></span><span class="sxs-lookup"><span data-stu-id="6a046-140">The texm3x3spec instruction performs the third row of the multiply to find w<sup>'</sup>.</span></span>

<span data-ttu-id="6a046-141">w<sup>'</sup> = TextureCoordinates (fase m + 2)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="6a046-141">w<sup>'</sup> = TextureCoordinates(stage m+2)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="6a046-142">L'istruzione texm3x3vspec esegue anche un calcolo della reflection.</span><span class="sxs-lookup"><span data-stu-id="6a046-142">The texm3x3vspec instruction also does a reflection calculation.</span></span>

<span data-ttu-id="6a046-143">(u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) = 2 \* \[ (n \* E)/(n \* n) \] \* n-E</span><span class="sxs-lookup"><span data-stu-id="6a046-143">(u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) = 2\*\[(N\*E)/(N\*N)\]\*N - E</span></span>

<span data-ttu-id="6a046-144">dove il normale N viene fornito da</span><span class="sxs-lookup"><span data-stu-id="6a046-144">// where the normal N is given by</span></span>

<span data-ttu-id="6a046-145">N = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> )</span><span class="sxs-lookup"><span data-stu-id="6a046-145">// N = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> )</span></span>

<span data-ttu-id="6a046-146">il vettore e il vettore di luce sono forniti da</span><span class="sxs-lookup"><span data-stu-id="6a046-146">// and the eye-ray vector E is given by</span></span>

<span data-ttu-id="6a046-147">E = (TextureCoordinates (fase m)<sub>Q</sub> ,</span><span class="sxs-lookup"><span data-stu-id="6a046-147">// E = (TextureCoordinates(stage m)<sub>Q</sub> ,</span></span>

<span data-ttu-id="6a046-148">TextureCoordinates (fase m + 1)<sub>Q</sub> ,</span><span class="sxs-lookup"><span data-stu-id="6a046-148">// TextureCoordinates(stage m+1)<sub>Q</sub> ,</span></span>

<span data-ttu-id="6a046-149">TextureCoordinates (fase m + 2)<sub>Q</sub> )</span><span class="sxs-lookup"><span data-stu-id="6a046-149">// TextureCoordinates(stage m+2)<sub>Q</sub> )</span></span>

<span data-ttu-id="6a046-150">Infine, l'istruzione texm3x3vspec Samples t (m + 2) with (u<sup>'</sup>, v<sup>'</sup>, w<sup>'</sup>) e archivia il risultato in t (m + 2).</span><span class="sxs-lookup"><span data-stu-id="6a046-150">Lastly, the texm3x3vspec instruction samples t(m+2) with (u<sup>'</sup>,v<sup>'</sup>,w<sup>'</sup>)and stores the result in t(m+2).</span></span>

<span data-ttu-id="6a046-151">t (m + 2)<sub>RGBA</sub> = TextureSample (fase m + 2)<sub>RGBA</sub> using (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) come coordinate</span><span class="sxs-lookup"><span data-stu-id="6a046-151">t(m+2)<sub>RGBA</sub> = TextureSample(stage m+2)<sub>RGBA</sub> using (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) as coordinates</span></span>

## <a name="examples"></a><span data-ttu-id="6a046-152">Esempio</span><span class="sxs-lookup"><span data-stu-id="6a046-152">Examples</span></span>

<span data-ttu-id="6a046-153">Di seguito è riportato un esempio di shader con le mappe di trama identificate e le fasi di trama identificate.</span><span class="sxs-lookup"><span data-stu-id="6a046-153">Here is an example shader with the texture maps identified and the texture stages identified.</span></span>


```
ps_1_1
tex t0                // Bind texture in stage 0 to register t0
texm3x3pad   t1,  t0  // First row of matrix multiply
texm3x3pad   t2,  t0  // Second row of matrix multiply
texm3x3vspec t3,  t0  // Third row of matrix multiply to get a 3-vector
                      // Reflect 3-vector by the eye-ray vector
                      // Use reflected vector to do a texture lookup
                      //   at stage 3
mov r0, t3            // Output the result
```



<span data-ttu-id="6a046-154">Questo esempio richiede la seguente configurazione della fase di trama.</span><span class="sxs-lookup"><span data-stu-id="6a046-154">This example requires the following texture stage setup.</span></span>

-   <span data-ttu-id="6a046-155">Alla fase 0 viene assegnata una mappa di trama con dati normali.</span><span class="sxs-lookup"><span data-stu-id="6a046-155">Stage 0 is assigned a texture map with normal data.</span></span> <span data-ttu-id="6a046-156">Questa operazione viene spesso definita mappa Bump.</span><span class="sxs-lookup"><span data-stu-id="6a046-156">This is often referred to as a bump map.</span></span> <span data-ttu-id="6a046-157">I dati sono normali (XYZ) per ogni Texel.</span><span class="sxs-lookup"><span data-stu-id="6a046-157">The data is (XYZ) normals for each texel.</span></span> <span data-ttu-id="6a046-158">Le coordinate di trama nella fase n definiscono come campionare questa mappa normale.</span><span class="sxs-lookup"><span data-stu-id="6a046-158">Texture coordinates at stage n defines how to sample this normal map.</span></span>
-   <span data-ttu-id="6a046-159">Il set di coordinate di trama m viene assegnato alla riga 1 della matrice 3x3.</span><span class="sxs-lookup"><span data-stu-id="6a046-159">Texture coordinate set m is assigned to row 1 of the 3x3 matrix.</span></span> <span data-ttu-id="6a046-160">Qualsiasi trama assegnata alla fase m viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="6a046-160">Any texture assigned to stage m is ignored.</span></span>
-   <span data-ttu-id="6a046-161">Il set di coordinate di trama m + 1 viene assegnato alla riga 2 della matrice 3x3.</span><span class="sxs-lookup"><span data-stu-id="6a046-161">Texture coordinate set m+1 is assigned to row 2 of the 3x3 matrix.</span></span> <span data-ttu-id="6a046-162">Qualsiasi trama assegnata alla fase m + 1 viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="6a046-162">Any texture assigned to stage m+1 is ignored.</span></span>
-   <span data-ttu-id="6a046-163">Il set di coordinate di trama m + 2 viene assegnato alla riga 3 della matrice 3x3.</span><span class="sxs-lookup"><span data-stu-id="6a046-163">Texture coordinate set m+2 is assigned to row 3 of the 3x3 matrix.</span></span> <span data-ttu-id="6a046-164">Alla fase m + 2 viene assegnata una mappa di trama del volume o del cubo.</span><span class="sxs-lookup"><span data-stu-id="6a046-164">Stage m+2 is assigned a volume or cube texture map.</span></span> <span data-ttu-id="6a046-165">La trama fornisce dati di colore (RGBA).</span><span class="sxs-lookup"><span data-stu-id="6a046-165">The texture provides color data (RGBA).</span></span>
-   <span data-ttu-id="6a046-166">Il vettore a forma di occhio E viene passato all'istruzione nel quarto componente (q) dei dati delle coordinate di trama a fasi m, m + 1 e m + 2.</span><span class="sxs-lookup"><span data-stu-id="6a046-166">The eye-ray vector E is passed into the instruction in the fourth component (q) of the texture coordinate data at stages m, m+1, and m+2.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a046-167">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6a046-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a046-168">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="6a046-168">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




