---
title: texm3x3spec-PS
description: Esegue una moltiplicazione della matrice 3x3 e usa il risultato per eseguire una ricerca di trama. Questa operazione può essere utilizzata per la reflection speculare e il mapping dell'ambiente. texm3x3spec deve essere usato in combinazione con due istruzioni texm3x3pad-PS.
ms.assetid: 74269bcf-de1d-48b4-a4d0-aa08fd54b8e6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d872a5f9ebf716142fb5bc506edb77bb0b66850a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398226"
---
# <a name="texm3x3spec---ps"></a><span data-ttu-id="0e687-105">texm3x3spec-PS</span><span class="sxs-lookup"><span data-stu-id="0e687-105">texm3x3spec - ps</span></span>

<span data-ttu-id="0e687-106">Esegue una moltiplicazione della matrice 3x3 e usa il risultato per eseguire una ricerca di trama.</span><span class="sxs-lookup"><span data-stu-id="0e687-106">Performs a 3x3 matrix multiply and uses the result to perform a texture lookup.</span></span> <span data-ttu-id="0e687-107">Questa operazione può essere utilizzata per la reflection speculare e il mapping dell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="0e687-107">This can be used for specular reflection and environment mapping.</span></span> <span data-ttu-id="0e687-108">texm3x3spec deve essere usato in combinazione con due istruzioni [texm3x3pad-PS](texm3x3pad---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="0e687-108">texm3x3spec must be used in conjunction with two [texm3x3pad - ps](texm3x3pad---ps.md) instructions.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e687-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0e687-109">Syntax</span></span>



| <span data-ttu-id="0e687-110">texm3x3spec DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="0e687-110">texm3x3spec dst, src0, src1</span></span> |
|-----------------------------|



 

<span data-ttu-id="0e687-111">dove</span><span class="sxs-lookup"><span data-stu-id="0e687-111">where</span></span>

-   <span data-ttu-id="0e687-112">DST è il registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0e687-112">dst is the destination register.</span></span>
-   <span data-ttu-id="0e687-113">src0 e src1 sono registri di origine.</span><span class="sxs-lookup"><span data-stu-id="0e687-113">src0 and src1 are source registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e687-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="0e687-114">Remarks</span></span>



| <span data-ttu-id="0e687-115">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="0e687-115">Pixel shader versions</span></span> | <span data-ttu-id="0e687-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="0e687-116">1\_1</span></span> | <span data-ttu-id="0e687-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="0e687-117">1\_2</span></span> | <span data-ttu-id="0e687-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="0e687-118">1\_3</span></span> | <span data-ttu-id="0e687-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="0e687-119">1\_4</span></span> | <span data-ttu-id="0e687-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0e687-120">2\_0</span></span> | <span data-ttu-id="0e687-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="0e687-121">2\_x</span></span> | <span data-ttu-id="0e687-122">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0e687-122">2\_sw</span></span> | <span data-ttu-id="0e687-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0e687-123">3\_0</span></span> | <span data-ttu-id="0e687-124">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0e687-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="0e687-125">texm3x3spec</span><span class="sxs-lookup"><span data-stu-id="0e687-125">texm3x3spec</span></span>           | <span data-ttu-id="0e687-126">x</span><span class="sxs-lookup"><span data-stu-id="0e687-126">x</span></span>    | <span data-ttu-id="0e687-127">x</span><span class="sxs-lookup"><span data-stu-id="0e687-127">x</span></span>    | <span data-ttu-id="0e687-128">x</span><span class="sxs-lookup"><span data-stu-id="0e687-128">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="0e687-129">Questa istruzione esegue la riga finale di una matrice 3x3 moltiplicata, usa il vettore risultante come vettore normale per riflettere un vettore di occhi, quindi usa il vettore riflesso per eseguire una ricerca di trama.</span><span class="sxs-lookup"><span data-stu-id="0e687-129">This instruction performs the final row of a 3x3 matrix multiply, uses the resulting vector as a normal vector to reflect an eye-ray vector, and then uses the reflected vector to perform a texture lookup.</span></span> <span data-ttu-id="0e687-130">Lo shader legge il vettore degli occhi da un registro costante.</span><span class="sxs-lookup"><span data-stu-id="0e687-130">The shader reads the eye-ray vector from a constant register.</span></span> <span data-ttu-id="0e687-131">La moltiplicazione della matrice 3x3 è in genere utile per orientare un vettore normale allo spazio tangente corretto per la superficie di cui viene eseguito il rendering.</span><span class="sxs-lookup"><span data-stu-id="0e687-131">The 3x3 matrix multiply is typically useful for orienting a normal vector to the correct tangent space for the surface being rendered.</span></span>

<span data-ttu-id="0e687-132">La matrice 3x3 è costituita dalle coordinate di trama della terza fase della trama e dalle due fasi di trama precedenti.</span><span class="sxs-lookup"><span data-stu-id="0e687-132">The 3x3 matrix is comprised of the texture coordinates of the third texture stage and the two preceding texture stages.</span></span> <span data-ttu-id="0e687-133">Il vettore di Reflection post risultante (u, v, w) viene usato per campionare la trama sulla fase di trama finale.</span><span class="sxs-lookup"><span data-stu-id="0e687-133">The resulting post reflection vector (u,v,w) is used to sample the texture on the final texture stage.</span></span> <span data-ttu-id="0e687-134">Qualsiasi trama assegnata alle due fasi di trama precedenti viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="0e687-134">Any texture assigned to the preceding two texture stages is ignored.</span></span>

<span data-ttu-id="0e687-135">Questa istruzione deve essere utilizzata con due istruzioni texm3x3pad.</span><span class="sxs-lookup"><span data-stu-id="0e687-135">This instruction must be used with two texm3x3pad instructions.</span></span> <span data-ttu-id="0e687-136">I registri di trama devono usare la sequenza seguente.</span><span class="sxs-lookup"><span data-stu-id="0e687-136">Texture registers must use the following sequence.</span></span>


```
 
tex t(n)                      // Define tn as a standard 3-vector (tn must
                              //   be defined in some way before it is used)
texm3x3pad t(m),   t(n)       //   where m > n
                              // Perform first row of matrix multiply
texm3x3pad  t(m+1), t(n)      // Perform second row of matrix multiply
texm3x3spec t(m+2), t(n), c0  // Perform third row of matrix multiply
                              // Then do a texture lookup on the texture
                              //   associated with texture stage m+2
```



<span data-ttu-id="0e687-137">La prima istruzione texm3x3pad esegue la prima riga dell'istruzione Multiply per<sup>Find u.</sup></span><span class="sxs-lookup"><span data-stu-id="0e687-137">The first texm3x3pad instruction performs the first row of the multiply to find u<sup>'</sup>.</span></span>

<span data-ttu-id="0e687-138">u<sup>'</sup> = TextureCoordinates (fase m)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="0e687-138">u<sup>'</sup> = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="0e687-139">La seconda istruzione texm3x3pad esegue la seconda riga della moltiplicazione per trovare la<sup>v.</sup></span><span class="sxs-lookup"><span data-stu-id="0e687-139">The second texm3x3pad instruction performs the second row of the multiply to find v<sup>'</sup>.</span></span>

<span data-ttu-id="0e687-140">v<sup>'</sup> = TextureCoordinates (fase m + 1)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="0e687-140">v<sup>'</sup> = TextureCoordinates(stage m+1)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="0e687-141">L'istruzione texm3x3spec esegue la terza riga del moltiplicatore per<sup>trovare w.</sup></span><span class="sxs-lookup"><span data-stu-id="0e687-141">The texm3x3spec instruction performs the third row of the multiply to find w<sup>'</sup>.</span></span>

<span data-ttu-id="0e687-142">w<sup>'</sup> = TextureCoordinates (fase m + 2)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="0e687-142">w<sup>'</sup> = TextureCoordinates(stage m+2)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="0e687-143">L'istruzione texm3x3spec esegue quindi un calcolo della reflection.</span><span class="sxs-lookup"><span data-stu-id="0e687-143">The texm3x3spec instruction then does a reflection calculation.</span></span>

<span data-ttu-id="0e687-144">(u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) = 2 \* \[ (n \* E)/(n \* n) \] \* n-E</span><span class="sxs-lookup"><span data-stu-id="0e687-144">(u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) = 2\*\[(N\*E)/(N\*N)\]\*N - E</span></span>

<span data-ttu-id="0e687-145">dove il normale N viene fornito da</span><span class="sxs-lookup"><span data-stu-id="0e687-145">// where the normal N is given by</span></span>

<span data-ttu-id="0e687-146">N = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> )</span><span class="sxs-lookup"><span data-stu-id="0e687-146">// N = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> )</span></span>

<span data-ttu-id="0e687-147">e il vettore di raggio E viene fornito dal registro delle costanti</span><span class="sxs-lookup"><span data-stu-id="0e687-147">// and the eye-ray vector E is given by the constant register</span></span>

<span data-ttu-id="0e687-148">E = c \# (qualsiasi registro costante--C0, C1, C2 e così via--può essere usato)</span><span class="sxs-lookup"><span data-stu-id="0e687-148">// E = c\# (Any constant register--c0, c1, c2, etc.--can be used)</span></span>

<span data-ttu-id="0e687-149">Infine, l'istruzione texm3x3spec Samples t (m + 2) with (u<sup>'</sup>, v<sup>'</sup>, w<sup>'</sup>) e archivia il risultato in t (m + 2).</span><span class="sxs-lookup"><span data-stu-id="0e687-149">Lastly, the texm3x3spec instruction samples t(m+2) with (u<sup>'</sup>,v<sup>'</sup>,w<sup>'</sup>) and stores the result in t(m+2).</span></span>

<span data-ttu-id="0e687-150">t (m + 2)<sub>RGBA</sub> = TextureSample (fase m + 2)<sub>RGBA</sub> using (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) come coordinate</span><span class="sxs-lookup"><span data-stu-id="0e687-150">t(m+2)<sub>RGBA</sub> = TextureSample(stage m+2)<sub>RGBA</sub> using (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) as coordinates</span></span>

## <a name="examples"></a><span data-ttu-id="0e687-151">Esempio</span><span class="sxs-lookup"><span data-stu-id="0e687-151">Examples</span></span>

<span data-ttu-id="0e687-152">Di seguito è riportato un esempio di shader con le mappe di trama e le fasi di trama identificate.</span><span class="sxs-lookup"><span data-stu-id="0e687-152">Here is an example shader with the texture maps and the texture stages identified.</span></span>


```
ps_1_1
tex t0                    // Bind texture in stage 0 to register t0 (tn must
                          //   be defined in some way before it is used)
texm3x3pad  t1,  t0       // First row of matrix multiply
texm3x3pad  t2,  t0       // Second row of matrix multiply
texm3x3spec t3,  t0,  c#  // Third row of matrix multiply to get a 3-vector
                          // Reflect 3-vector by the eye-ray vector in c#  
                          // Use reflected vector to lookup texture in
                          //   stage 3
mov r0, t3                // Output the result
```



<span data-ttu-id="0e687-153">Questo esempio richiede la seguente configurazione della fase di trama.</span><span class="sxs-lookup"><span data-stu-id="0e687-153">This example requires the following texture stage setup.</span></span>

-   <span data-ttu-id="0e687-154">Alla fase 0 viene assegnata una mappa di trama con dati normali.</span><span class="sxs-lookup"><span data-stu-id="0e687-154">Stage 0 is assigned a texture map with normal data.</span></span> <span data-ttu-id="0e687-155">Questa operazione viene spesso definita mappa Bump.</span><span class="sxs-lookup"><span data-stu-id="0e687-155">This is often referred to as a bump map.</span></span> <span data-ttu-id="0e687-156">I dati sono normali (XYZ) per ogni Texel.</span><span class="sxs-lookup"><span data-stu-id="0e687-156">The data is (XYZ) normals for each texel.</span></span> <span data-ttu-id="0e687-157">Le coordinate di trama nella fase n definiscono la posizione in cui eseguire il campionamento della mappa normale.</span><span class="sxs-lookup"><span data-stu-id="0e687-157">Texture coordinates at stage n defines where to sample this normal map.</span></span>
-   <span data-ttu-id="0e687-158">Il set di coordinate di trama m viene assegnato alla riga 1 della matrice 3x3.</span><span class="sxs-lookup"><span data-stu-id="0e687-158">Texture coordinate set m is assigned to row 1 of the 3x3 matrix.</span></span> <span data-ttu-id="0e687-159">Qualsiasi trama assegnata alla fase m viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="0e687-159">Any texture assigned to stage m is ignored.</span></span>
-   <span data-ttu-id="0e687-160">Il set di coordinate di trama m + 1 viene assegnato alla riga 2 della matrice 3x3.</span><span class="sxs-lookup"><span data-stu-id="0e687-160">Texture coordinate set m+1 is assigned to row 2 of the 3x3 matrix.</span></span> <span data-ttu-id="0e687-161">Qualsiasi trama assegnata alla fase m + 1 viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="0e687-161">Any texture assigned to stage m+1 is ignored.</span></span>
-   <span data-ttu-id="0e687-162">Il set di coordinate di trama m + 2 viene assegnato alla riga 3 della matrice 3x3.</span><span class="sxs-lookup"><span data-stu-id="0e687-162">Texture coordinate set m+2 is assigned to row 3 of the 3x3 matrix.</span></span> <span data-ttu-id="0e687-163">Alla fase m + 2 viene assegnata una mappa di trama del volume o del cubo.</span><span class="sxs-lookup"><span data-stu-id="0e687-163">Stage m+2 is assigned a volume or cube texture map.</span></span> <span data-ttu-id="0e687-164">La trama fornisce dati di colore (RGBA).</span><span class="sxs-lookup"><span data-stu-id="0e687-164">The texture provides color data (RGBA).</span></span>
-   <span data-ttu-id="0e687-165">Il vettore di raggio E viene fornito da un registro costante E = c \# .</span><span class="sxs-lookup"><span data-stu-id="0e687-165">The eye-ray vector E is given by a constant register E = c\#.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e687-166">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0e687-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e687-167">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="0e687-167">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




