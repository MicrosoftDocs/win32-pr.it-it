---
title: Modificatori per ps_2_0 e versioni successive
description: I modificatori di istruzione influiscono sul risultato dell'istruzione prima che venga scritto nel registro di destinazione.
ms.assetid: eb2a8a1f-51bc-4516-b679-a8fb25b0dda0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7141576b80b7a05a3e61ee9a98fa36958b1d5530
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856985"
---
# <a name="modifiers-for-ps_2_0-and-above"></a><span data-ttu-id="e64bd-103">Modificatori per PS \_ 2 \_ 0 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="e64bd-103">Modifiers for ps\_2\_0 and Above</span></span>

<span data-ttu-id="e64bd-104">I modificatori di istruzione influiscono sul risultato dell'istruzione prima che venga scritto nel registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e64bd-104">Instruction modifiers affect the result of the instruction before it is written into the destination register.</span></span>

<span data-ttu-id="e64bd-105">Questa sezione contiene informazioni di riferimento per i modificatori di istruzioni implementati da pixel shader versione 2 \_ 0 e successive.</span><span class="sxs-lookup"><span data-stu-id="e64bd-105">This section contains reference information for the instruction modifiers implemented by pixel shader version 2\_0 and above.</span></span>



| <span data-ttu-id="e64bd-106">Name</span><span class="sxs-lookup"><span data-stu-id="e64bd-106">Name</span></span>                                     | <span data-ttu-id="e64bd-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e64bd-107">Syntax</span></span>     | <span data-ttu-id="e64bd-108">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e64bd-108">2\_0</span></span> | <span data-ttu-id="e64bd-109">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e64bd-109">2\_x</span></span> | <span data-ttu-id="e64bd-110">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e64bd-110">2\_sw</span></span> | <span data-ttu-id="e64bd-111">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e64bd-111">3\_0</span></span> | <span data-ttu-id="e64bd-112">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e64bd-112">3\_sw</span></span> |
|------------------------------------------|------------|------|------|-------|------|-------|
| [<span data-ttu-id="e64bd-113">Centro</span><span class="sxs-lookup"><span data-stu-id="e64bd-113">Centroid</span></span>](#centroid)                    | <span data-ttu-id="e64bd-114">\_centro</span><span class="sxs-lookup"><span data-stu-id="e64bd-114">\_centroid</span></span> | <span data-ttu-id="e64bd-115">x</span><span class="sxs-lookup"><span data-stu-id="e64bd-115">x</span></span>    | <span data-ttu-id="e64bd-116">x</span><span class="sxs-lookup"><span data-stu-id="e64bd-116">x</span></span>    | <span data-ttu-id="e64bd-117">x</span><span class="sxs-lookup"><span data-stu-id="e64bd-117">x</span></span>     | <span data-ttu-id="e64bd-118">x</span><span class="sxs-lookup"><span data-stu-id="e64bd-118">x</span></span>    | <span data-ttu-id="e64bd-119">x</span><span class="sxs-lookup"><span data-stu-id="e64bd-119">x</span></span>     |
| [<span data-ttu-id="e64bd-120">\_Precisione parziale</span><span class="sxs-lookup"><span data-stu-id="e64bd-120">Partial\_Precision</span></span>](#partial-precision) | <span data-ttu-id="e64bd-121">\_PP</span><span class="sxs-lookup"><span data-stu-id="e64bd-121">\_pp</span></span>       | <span data-ttu-id="e64bd-122">x</span><span class="sxs-lookup"><span data-stu-id="e64bd-122">x</span></span>    | <span data-ttu-id="e64bd-123">x</span><span class="sxs-lookup"><span data-stu-id="e64bd-123">x</span></span>    | <span data-ttu-id="e64bd-124">x</span><span class="sxs-lookup"><span data-stu-id="e64bd-124">x</span></span>     | <span data-ttu-id="e64bd-125">x</span><span class="sxs-lookup"><span data-stu-id="e64bd-125">x</span></span>    | <span data-ttu-id="e64bd-126">x</span><span class="sxs-lookup"><span data-stu-id="e64bd-126">x</span></span>     |
| [<span data-ttu-id="e64bd-127">Saturazione</span><span class="sxs-lookup"><span data-stu-id="e64bd-127">Saturate</span></span>](#saturate)                    | <span data-ttu-id="e64bd-128">\_Sat</span><span class="sxs-lookup"><span data-stu-id="e64bd-128">\_sat</span></span>      | <span data-ttu-id="e64bd-129">x</span><span class="sxs-lookup"><span data-stu-id="e64bd-129">x</span></span>    | <span data-ttu-id="e64bd-130">x</span><span class="sxs-lookup"><span data-stu-id="e64bd-130">x</span></span>    | <span data-ttu-id="e64bd-131">x</span><span class="sxs-lookup"><span data-stu-id="e64bd-131">x</span></span>     | <span data-ttu-id="e64bd-132">x</span><span class="sxs-lookup"><span data-stu-id="e64bd-132">x</span></span>    | <span data-ttu-id="e64bd-133">x</span><span class="sxs-lookup"><span data-stu-id="e64bd-133">x</span></span>     |



 

## <a name="centroid"></a><span data-ttu-id="e64bd-134">Centro</span><span class="sxs-lookup"><span data-stu-id="e64bd-134">Centroid</span></span>

<span data-ttu-id="e64bd-135">Il modificatore del centro è un modificatore facoltativo che blocca l'interpolazione degli attributi all'interno dell'intervallo della primitiva quando un pixel Center multisample non è coperto dalla primitiva.</span><span class="sxs-lookup"><span data-stu-id="e64bd-135">The centroid modifier is an optional modifier that clamps attribute interpolation within the range of the primitive when a multisample pixel center is not covered by the primitive.</span></span> <span data-ttu-id="e64bd-136">Questo può essere visualizzato nel [campionamento](https://msdn.microsoft.com/library/ee415231(VS.85).aspx)del centro.</span><span class="sxs-lookup"><span data-stu-id="e64bd-136">This can be seen in [Centroid Sampling](https://msdn.microsoft.com/library/ee415231(VS.85).aspx).</span></span>

<span data-ttu-id="e64bd-137">È possibile applicare il modificatore di baricentro a un'istruzione di assembly, come illustrato di seguito:</span><span class="sxs-lookup"><span data-stu-id="e64bd-137">You can apply the centroid modifier to an assembly instruction as shown here:</span></span>


```
dcl_texcoord0_centroid v0
```



<span data-ttu-id="e64bd-138">È anche possibile applicare il modificatore di baricentro a una semantica, come illustrato di seguito:</span><span class="sxs-lookup"><span data-stu-id="e64bd-138">You can also apply the centroid modifier to a semantic as shown here:</span></span>


```
float4 TexturePointCentroidPS( float4 TexCoord : TEXCOORD0_centroid ) : COLOR0
{
    return tex2D( PointSampler, TexCoord );
}
```



<span data-ttu-id="e64bd-139">Inoltre, per qualsiasi [Registro dei colori di input](dx9-graphics-reference-asm-ps-registers-input-color.md) (v \# ) dichiarato con una semantica di colore verrà applicato automaticamente il baricentro.</span><span class="sxs-lookup"><span data-stu-id="e64bd-139">In addition, any [Input Color Register](dx9-graphics-reference-asm-ps-registers-input-color.md) (v\#) declared with a color semantic will automatically have centroid applied.</span></span> <span data-ttu-id="e64bd-140">Non è garantita l'accuratezza delle sfumature calcolate in base agli attributi campionati di baricentro.</span><span class="sxs-lookup"><span data-stu-id="e64bd-140">Gradients computed from attributes that are centroid sampled are not guaranteed to be accurate.</span></span>

## <a name="partial-precision"></a><span data-ttu-id="e64bd-141">Precisione parziale</span><span class="sxs-lookup"><span data-stu-id="e64bd-141">Partial Precision</span></span>

<span data-ttu-id="e64bd-142">Il modificatore di istruzioni di precisione parziale ( \_ PP) indica le aree in cui la precisione parziale è accettabile, a condizione che l'implementazione sottostante la supporti.</span><span class="sxs-lookup"><span data-stu-id="e64bd-142">The partial precision instruction modifier (\_pp) indicates areas where partial precision is acceptable, provided that the underlying implementation supports it.</span></span> <span data-ttu-id="e64bd-143">Le implementazioni sono sempre libere di ignorare il modificatore ed eseguire le operazioni interessate con la massima precisione.</span><span class="sxs-lookup"><span data-stu-id="e64bd-143">Implementations are always free to ignore the modifier and perform the affected operations in full precision.</span></span>

<span data-ttu-id="e64bd-144">Il \_ modificatore di PP può essere eseguito in due contesti:</span><span class="sxs-lookup"><span data-stu-id="e64bd-144">The \_pp modifier can occur in two contexts:</span></span>

-   <span data-ttu-id="e64bd-145">In una dichiarazione di coordinata di trama per consentire il passaggio di coordinate di trama al pixel shader in formato a precisione parziale.</span><span class="sxs-lookup"><span data-stu-id="e64bd-145">On a texture coordinate declaration to enable passing texture coordinates to the pixel shader in partial-precision form.</span></span> <span data-ttu-id="e64bd-146">Questo consente, ad esempio, l'uso di coordinate di trama per inoltrare i dati di colore al pixel shader, che può essere più veloce con precisione parziale rispetto alla precisione completa in alcune implementazioni.</span><span class="sxs-lookup"><span data-stu-id="e64bd-146">This allows, for example, the use of texture coordinates to relay color data to the pixel shader, which may be faster with partial precision than with full precision in some implementations.</span></span> <span data-ttu-id="e64bd-147">In assenza di questo modificatore, le coordinate di trama devono essere passate con la massima precisione.</span><span class="sxs-lookup"><span data-stu-id="e64bd-147">In the absence of this modifier, texture coordinates must be passed in full precision.</span></span>
-   <span data-ttu-id="e64bd-148">In qualsiasi istruzione, incluse le istruzioni per il caricamento della trama.</span><span class="sxs-lookup"><span data-stu-id="e64bd-148">On any instruction including texture load instructions.</span></span> <span data-ttu-id="e64bd-149">Ciò indica che l'implementazione è autorizzata a eseguire l'istruzione con precisione parziale e archiviare un risultato di precisione parziale.</span><span class="sxs-lookup"><span data-stu-id="e64bd-149">This indicates that the implementation is allowed to execute the instruction with partial precision and store a partial precision result.</span></span> <span data-ttu-id="e64bd-150">In assenza di un modificatore esplicito, l'istruzione deve essere eseguita a precisione completa (indipendentemente dalla precisione di input).</span><span class="sxs-lookup"><span data-stu-id="e64bd-150">In the absence of an explicit modifier, the instruction must be performed at full precision (regardless of the input precision).</span></span>

<span data-ttu-id="e64bd-151">Esempi:</span><span class="sxs-lookup"><span data-stu-id="e64bd-151">Examples:</span></span>


```
dcl_texcoord0_pp t1
cmp_pp r0, r1, r2, r3
```



## <a name="saturate"></a><span data-ttu-id="e64bd-152">Saturazione</span><span class="sxs-lookup"><span data-stu-id="e64bd-152">Saturate</span></span>

<span data-ttu-id="e64bd-153">Il modificatore di istruzioni di saturazione ( \_ Sat) satura (o clamp) il risultato dell'istruzione nell'intervallo \[ 0, 1 \] prima della scrittura nel registro di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e64bd-153">The saturate instruction modifier (\_sat) saturates (or clamps) the instruction result to the range \[0, 1\] before writing to the destination register.</span></span>

<span data-ttu-id="e64bd-154">Il \_ modificatore di istruzioni Sat può essere usato con qualsiasi istruzione ad eccezione di [FRC-PS](frc---ps.md), [SinCos-PS](sincos---ps.md)ed eventuali \* istruzioni Tex.</span><span class="sxs-lookup"><span data-stu-id="e64bd-154">The \_sat instruction modifier can be used with any instruction except [frc - ps](frc---ps.md), [sincos - ps](sincos---ps.md), and any tex\* instructions.</span></span>

<span data-ttu-id="e64bd-155">Per PS \_ 2 \_ 0, PS \_ 2 \_ x e PS \_ 2 \_ SW, il \_ modificatore di istruzioni Sat non può essere usato con le istruzioni scritte in tutti i registri di output ([Registro colori di output](dx9-graphics-reference-asm-ps-registers-output-color.md) o [Registro profondità output](dx9-graphics-reference-asm-ps-registers-output-depth.md)).</span><span class="sxs-lookup"><span data-stu-id="e64bd-155">For ps\_2\_0, ps\_2\_x, and ps\_2\_sw, the \_sat instruction modifier cannot be used with instructions writing to any output registers ([Output Color Register](dx9-graphics-reference-asm-ps-registers-output-color.md) or [Output Depth Register](dx9-graphics-reference-asm-ps-registers-output-depth.md)).</span></span> <span data-ttu-id="e64bd-156">Questa restrizione non si applica a PS \_ 3 \_ 0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="e64bd-156">This restriction does not apply to ps\_3\_0 and above.</span></span>

<span data-ttu-id="e64bd-157">Esempio:</span><span class="sxs-lookup"><span data-stu-id="e64bd-157">Example:</span></span>


```
dp3_sat r0, v0, c1
```



## <a name="related-topics"></a><span data-ttu-id="e64bd-158">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e64bd-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e64bd-159">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="e64bd-159">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




