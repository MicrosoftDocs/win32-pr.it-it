---
title: Modificatori per ps_2_0 e superiori
description: I modificatori di istruzione influiscono sul risultato dell'istruzione prima che venga scritta nel registro di destinazione. Informazioni sui modificatori per ps_2_0 e successive.
ms.assetid: eb2a8a1f-51bc-4516-b679-a8fb25b0dda0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dc8ed91f8e103ebbab7c43ffe53201f0e1d5dfcf
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989286"
---
# <a name="modifiers-for-ps_2_0-and-above"></a><span data-ttu-id="fefab-104">Modificatori per ps \_ 2 \_ 0 e superiori</span><span class="sxs-lookup"><span data-stu-id="fefab-104">Modifiers for ps\_2\_0 and Above</span></span>

<span data-ttu-id="fefab-105">I modificatori di istruzione influiscono sul risultato dell'istruzione prima che venga scritta nel registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="fefab-105">Instruction modifiers affect the result of the instruction before it is written into the destination register.</span></span>

<span data-ttu-id="fefab-106">Questa sezione contiene informazioni di riferimento per i modificatori di istruzione implementati pixel shader versione 2 \_ 0 e successive.</span><span class="sxs-lookup"><span data-stu-id="fefab-106">This section contains reference information for the instruction modifiers implemented by pixel shader version 2\_0 and above.</span></span>



| <span data-ttu-id="fefab-107">Name</span><span class="sxs-lookup"><span data-stu-id="fefab-107">Name</span></span>                                     | <span data-ttu-id="fefab-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fefab-108">Syntax</span></span>     | <span data-ttu-id="fefab-109">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="fefab-109">2\_0</span></span> | <span data-ttu-id="fefab-110">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="fefab-110">2\_x</span></span> | <span data-ttu-id="fefab-111">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="fefab-111">2\_sw</span></span> | <span data-ttu-id="fefab-112">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="fefab-112">3\_0</span></span> | <span data-ttu-id="fefab-113">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="fefab-113">3\_sw</span></span> |
|------------------------------------------|------------|------|------|-------|------|-------|
| [<span data-ttu-id="fefab-114">Baricentro</span><span class="sxs-lookup"><span data-stu-id="fefab-114">Centroid</span></span>](#centroid)                    | <span data-ttu-id="fefab-115">\_Baricentro</span><span class="sxs-lookup"><span data-stu-id="fefab-115">\_centroid</span></span> | <span data-ttu-id="fefab-116">x</span><span class="sxs-lookup"><span data-stu-id="fefab-116">x</span></span>    | <span data-ttu-id="fefab-117">x</span><span class="sxs-lookup"><span data-stu-id="fefab-117">x</span></span>    | <span data-ttu-id="fefab-118">x</span><span class="sxs-lookup"><span data-stu-id="fefab-118">x</span></span>     | <span data-ttu-id="fefab-119">x</span><span class="sxs-lookup"><span data-stu-id="fefab-119">x</span></span>    | <span data-ttu-id="fefab-120">x</span><span class="sxs-lookup"><span data-stu-id="fefab-120">x</span></span>     |
| [<span data-ttu-id="fefab-121">Precisione \_ parziale</span><span class="sxs-lookup"><span data-stu-id="fefab-121">Partial\_Precision</span></span>](#partial-precision) | <span data-ttu-id="fefab-122">\_Pp</span><span class="sxs-lookup"><span data-stu-id="fefab-122">\_pp</span></span>       | <span data-ttu-id="fefab-123">x</span><span class="sxs-lookup"><span data-stu-id="fefab-123">x</span></span>    | <span data-ttu-id="fefab-124">x</span><span class="sxs-lookup"><span data-stu-id="fefab-124">x</span></span>    | <span data-ttu-id="fefab-125">x</span><span class="sxs-lookup"><span data-stu-id="fefab-125">x</span></span>     | <span data-ttu-id="fefab-126">x</span><span class="sxs-lookup"><span data-stu-id="fefab-126">x</span></span>    | <span data-ttu-id="fefab-127">x</span><span class="sxs-lookup"><span data-stu-id="fefab-127">x</span></span>     |
| [<span data-ttu-id="fefab-128">Saturazione</span><span class="sxs-lookup"><span data-stu-id="fefab-128">Saturate</span></span>](#saturate)                    | <span data-ttu-id="fefab-129">\_Sab</span><span class="sxs-lookup"><span data-stu-id="fefab-129">\_sat</span></span>      | <span data-ttu-id="fefab-130">x</span><span class="sxs-lookup"><span data-stu-id="fefab-130">x</span></span>    | <span data-ttu-id="fefab-131">x</span><span class="sxs-lookup"><span data-stu-id="fefab-131">x</span></span>    | <span data-ttu-id="fefab-132">x</span><span class="sxs-lookup"><span data-stu-id="fefab-132">x</span></span>     | <span data-ttu-id="fefab-133">x</span><span class="sxs-lookup"><span data-stu-id="fefab-133">x</span></span>    | <span data-ttu-id="fefab-134">x</span><span class="sxs-lookup"><span data-stu-id="fefab-134">x</span></span>     |



 

## <a name="centroid"></a><span data-ttu-id="fefab-135">Baricentro</span><span class="sxs-lookup"><span data-stu-id="fefab-135">Centroid</span></span>

<span data-ttu-id="fefab-136">Il modificatore centroide è un modificatore facoltativo che stringe l'interpolazione degli attributi all'interno dell'intervallo della primitiva quando un centro pixel multicampionamento non è coperto dalla primitiva.</span><span class="sxs-lookup"><span data-stu-id="fefab-136">The centroid modifier is an optional modifier that clamps attribute interpolation within the range of the primitive when a multisample pixel center is not covered by the primitive.</span></span> <span data-ttu-id="fefab-137">Questa operazione può essere osservata in [Campionamento centroide.](https://msdn.microsoft.com/library/ee415231(VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="fefab-137">This can be seen in [Centroid Sampling](https://msdn.microsoft.com/library/ee415231(VS.85).aspx).</span></span>

<span data-ttu-id="fefab-138">È possibile applicare il modificatore centroide a un'istruzione di assembly, come illustrato di seguito:</span><span class="sxs-lookup"><span data-stu-id="fefab-138">You can apply the centroid modifier to an assembly instruction as shown here:</span></span>


```
dcl_texcoord0_centroid v0
```



<span data-ttu-id="fefab-139">È anche possibile applicare il modificatore centroide a una semantica, come illustrato di seguito:</span><span class="sxs-lookup"><span data-stu-id="fefab-139">You can also apply the centroid modifier to a semantic as shown here:</span></span>


```
float4 TexturePointCentroidPS( float4 TexCoord : TEXCOORD0_centroid ) : COLOR0
{
    return tex2D( PointSampler, TexCoord );
}
```



<span data-ttu-id="fefab-140">Inoltre, a qualsiasi [registro colori di input](dx9-graphics-reference-asm-ps-registers-input-color.md) (v ) dichiarato con una semantica dei colori verrà applicato \# automaticamente il centroide.</span><span class="sxs-lookup"><span data-stu-id="fefab-140">In addition, any [Input Color Register](dx9-graphics-reference-asm-ps-registers-input-color.md) (v\#) declared with a color semantic will automatically have centroid applied.</span></span> <span data-ttu-id="fefab-141">Non è garantito che le sfumature calcolate da attributi campionati al centroide siano accurate.</span><span class="sxs-lookup"><span data-stu-id="fefab-141">Gradients computed from attributes that are centroid sampled are not guaranteed to be accurate.</span></span>

## <a name="partial-precision"></a><span data-ttu-id="fefab-142">Precisione parziale</span><span class="sxs-lookup"><span data-stu-id="fefab-142">Partial Precision</span></span>

<span data-ttu-id="fefab-143">Il modificatore di istruzione di precisione parziale (pp) indica le aree in cui la precisione parziale è accettabile, a condizione \_ che l'implementazione sottostante la supporti.</span><span class="sxs-lookup"><span data-stu-id="fefab-143">The partial precision instruction modifier (\_pp) indicates areas where partial precision is acceptable, provided that the underlying implementation supports it.</span></span> <span data-ttu-id="fefab-144">Le implementazioni sono sempre liberi di ignorare il modificatore ed eseguire le operazioni interessate con la massima precisione.</span><span class="sxs-lookup"><span data-stu-id="fefab-144">Implementations are always free to ignore the modifier and perform the affected operations in full precision.</span></span>

<span data-ttu-id="fefab-145">Il \_ modificatore pp può verificarsi in due contesti:</span><span class="sxs-lookup"><span data-stu-id="fefab-145">The \_pp modifier can occur in two contexts:</span></span>

-   <span data-ttu-id="fefab-146">In una dichiarazione di coordinate di trama per consentire il passaggio delle coordinate della trama pixel shader in forma a precisione parziale.</span><span class="sxs-lookup"><span data-stu-id="fefab-146">On a texture coordinate declaration to enable passing texture coordinates to the pixel shader in partial-precision form.</span></span> <span data-ttu-id="fefab-147">Ciò consente, ad esempio, l'uso di coordinate di trama per inoltrare i dati di colore al pixel shader, che può essere più veloce con precisione parziale rispetto alla precisione completa in alcune implementazioni.</span><span class="sxs-lookup"><span data-stu-id="fefab-147">This allows, for example, the use of texture coordinates to relay color data to the pixel shader, which may be faster with partial precision than with full precision in some implementations.</span></span> <span data-ttu-id="fefab-148">In assenza di questo modificatore, le coordinate della trama devono essere passate con precisione completa.</span><span class="sxs-lookup"><span data-stu-id="fefab-148">In the absence of this modifier, texture coordinates must be passed in full precision.</span></span>
-   <span data-ttu-id="fefab-149">In qualsiasi istruzione, incluse le istruzioni di caricamento della trama.</span><span class="sxs-lookup"><span data-stu-id="fefab-149">On any instruction including texture load instructions.</span></span> <span data-ttu-id="fefab-150">Ciò indica che l'implementazione può eseguire l'istruzione con precisione parziale e archiviare un risultato di precisione parziale.</span><span class="sxs-lookup"><span data-stu-id="fefab-150">This indicates that the implementation is allowed to execute the instruction with partial precision and store a partial precision result.</span></span> <span data-ttu-id="fefab-151">In assenza di un modificatore esplicito, l'istruzione deve essere eseguita con precisione completa (indipendentemente dalla precisione di input).</span><span class="sxs-lookup"><span data-stu-id="fefab-151">In the absence of an explicit modifier, the instruction must be performed at full precision (regardless of the input precision).</span></span>

<span data-ttu-id="fefab-152">Esempi:</span><span class="sxs-lookup"><span data-stu-id="fefab-152">Examples:</span></span>


```
dcl_texcoord0_pp t1
cmp_pp r0, r1, r2, r3
```



## <a name="saturate"></a><span data-ttu-id="fefab-153">Saturazione</span><span class="sxs-lookup"><span data-stu-id="fefab-153">Saturate</span></span>

<span data-ttu-id="fefab-154">Il modificatore di istruzione satura ( sat) satura (o stringe) il risultato dell'istruzione nell'intervallo \_ 0, 1 prima di scrivere nel registro \[ \] di destinazione.</span><span class="sxs-lookup"><span data-stu-id="fefab-154">The saturate instruction modifier (\_sat) saturates (or clamps) the instruction result to the range \[0, 1\] before writing to the destination register.</span></span>

<span data-ttu-id="fefab-155">Il modificatore di istruzione sat può essere usato con qualsiasi istruzione tranne \_ [frc - ps](frc---ps.md), [sincos - ps](sincos---ps.md)e qualsiasi istruzione tex. \*</span><span class="sxs-lookup"><span data-stu-id="fefab-155">The \_sat instruction modifier can be used with any instruction except [frc - ps](frc---ps.md), [sincos - ps](sincos---ps.md), and any tex\* instructions.</span></span>

<span data-ttu-id="fefab-156">Per ps \_ 2 \_ 0, ps 2 x e \_ \_ ps \_ 2 \_ sw, \_ [](dx9-graphics-reference-asm-ps-registers-output-color.md) [](dx9-graphics-reference-asm-ps-registers-output-depth.md)il modificatore di istruzione sat non può essere usato con istruzioni che scrivono in registri di output (Output Color Register o Output Depth Register).</span><span class="sxs-lookup"><span data-stu-id="fefab-156">For ps\_2\_0, ps\_2\_x, and ps\_2\_sw, the \_sat instruction modifier cannot be used with instructions writing to any output registers ([Output Color Register](dx9-graphics-reference-asm-ps-registers-output-color.md) or [Output Depth Register](dx9-graphics-reference-asm-ps-registers-output-depth.md)).</span></span> <span data-ttu-id="fefab-157">Questa restrizione non si applica a ps \_ 3 \_ 0 e versione superiore.</span><span class="sxs-lookup"><span data-stu-id="fefab-157">This restriction does not apply to ps\_3\_0 and above.</span></span>

<span data-ttu-id="fefab-158">Esempio:</span><span class="sxs-lookup"><span data-stu-id="fefab-158">Example:</span></span>


```
dp3_sat r0, v0, c1
```



## <a name="related-topics"></a><span data-ttu-id="fefab-159">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fefab-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fefab-160">Istruzioni per pixel shader</span><span class="sxs-lookup"><span data-stu-id="fefab-160">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




