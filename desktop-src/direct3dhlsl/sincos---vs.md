---
title: SinCos-vs
description: Calcola il seno e il coseno, in radianti. | SinCos-vs
ms.assetid: 733a3980-ceaf-43dc-a862-923c369e4a65
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ca70a319852346c6e75ba544489d033a861d4c3b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103969236"
---
# <a name="sincos---vs"></a><span data-ttu-id="c137b-104">SinCos-vs</span><span class="sxs-lookup"><span data-stu-id="c137b-104">sincos - vs</span></span>

<span data-ttu-id="c137b-105">Calcola il seno e il coseno, in radianti.</span><span class="sxs-lookup"><span data-stu-id="c137b-105">Computes sine and cosine, in radians.</span></span>

## <a name="syntax"></a><span data-ttu-id="c137b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c137b-106">Syntax</span></span>

### <a name="vs_2_0-and-vs_2_x"></a><span data-ttu-id="c137b-107">vs \_ 2 \_ 0 e vs \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c137b-107">vs\_2\_0 and vs\_2\_x</span></span>



| <span data-ttu-id="c137b-108">SinCos DST. x</span><span class="sxs-lookup"><span data-stu-id="c137b-108">sincos dst.{x\</span></span>|<span data-ttu-id="c137b-109">y</span><span class="sxs-lookup"><span data-stu-id="c137b-109">y\</span></span>|<span data-ttu-id="c137b-110">XY}, src0. x</span><span class="sxs-lookup"><span data-stu-id="c137b-110">xy}, src0.{x\</span></span>|<span data-ttu-id="c137b-111">y</span><span class="sxs-lookup"><span data-stu-id="c137b-111">y\</span></span>|<span data-ttu-id="c137b-112">z</span><span class="sxs-lookup"><span data-stu-id="c137b-112">z\</span></span>|<span data-ttu-id="c137b-113">w}, src1, src2</span><span class="sxs-lookup"><span data-stu-id="c137b-113">w}, src1, src2</span></span> |
|------------------------------------------------------|



 

<span data-ttu-id="c137b-114">Dove:</span><span class="sxs-lookup"><span data-stu-id="c137b-114">Where:</span></span>

-   <span data-ttu-id="c137b-115">DST è il registro di destinazione e deve essere un [registro temporaneo](dx9-graphics-reference-asm-vs-registers-temporary.md) (r \# ).</span><span class="sxs-lookup"><span data-stu-id="c137b-115">dst is the destination register and has to be a [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md) (r\#).</span></span> <span data-ttu-id="c137b-116">Il registro di destinazione deve avere esattamente una delle tre maschere seguenti:. x \| . y \| . XY.</span><span class="sxs-lookup"><span data-stu-id="c137b-116">The destination register must have exactly one of the following three masks: .x \| .y \| .xy.</span></span>
-   <span data-ttu-id="c137b-117">src0 è un registro di origine che fornisce l'angolo di input, che deve essere compreso tra \[ -pi, + pi \] .</span><span class="sxs-lookup"><span data-stu-id="c137b-117">src0 is a source register that provides the input angle, which must be within \[-pi, +pi\].</span></span> <span data-ttu-id="c137b-118">{x \| y \| z \| w} è la replica obbligatoria Swizzle.</span><span class="sxs-lookup"><span data-stu-id="c137b-118">{x\|y\|z\|w} is the required replicate swizzle.</span></span>
-   <span data-ttu-id="c137b-119">src1 e src2 sono registri di origine e devono essere due diversi registri [float costanti](dx9-graphics-reference-asm-vs-registers-constant-float.md) (c \# ).</span><span class="sxs-lookup"><span data-stu-id="c137b-119">src1 and src2 are source registers and must be two different [Constant Float Register](dx9-graphics-reference-asm-vs-registers-constant-float.md) (c\#).</span></span> <span data-ttu-id="c137b-120">I valori di src1 e src2 devono corrispondere rispettivamente alle macro [**D3DSINCOSCONST1**](/windows/desktop/direct3d9/d3dsincosconst1) e [**D3DSINCOSCONST2**](/windows/desktop/direct3d9/d3dsincosconst2) .</span><span class="sxs-lookup"><span data-stu-id="c137b-120">The values of src1 and src2 must be that of the macros [**D3DSINCOSCONST1**](/windows/desktop/direct3d9/d3dsincosconst1) and [**D3DSINCOSCONST2**](/windows/desktop/direct3d9/d3dsincosconst2) respectively.</span></span>

### <a name="vs_3_0"></a><span data-ttu-id="c137b-121">vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c137b-121">vs\_3\_0</span></span>



| <span data-ttu-id="c137b-122">SinCos DST. x</span><span class="sxs-lookup"><span data-stu-id="c137b-122">sincos dst.{x\</span></span>|<span data-ttu-id="c137b-123">y</span><span class="sxs-lookup"><span data-stu-id="c137b-123">y\</span></span>|<span data-ttu-id="c137b-124">XY}, src0. x</span><span class="sxs-lookup"><span data-stu-id="c137b-124">xy}, src0.{x\</span></span>|<span data-ttu-id="c137b-125">y</span><span class="sxs-lookup"><span data-stu-id="c137b-125">y\</span></span>|<span data-ttu-id="c137b-126">z</span><span class="sxs-lookup"><span data-stu-id="c137b-126">z\</span></span>|<span data-ttu-id="c137b-127">w</span><span class="sxs-lookup"><span data-stu-id="c137b-127">w}</span></span> |
|------------------------------------------|



 

<span data-ttu-id="c137b-128">Dove:</span><span class="sxs-lookup"><span data-stu-id="c137b-128">Where:</span></span>

-   <span data-ttu-id="c137b-129">DST è un registro di destinazione e deve essere un [registro temporaneo](dx9-graphics-reference-asm-vs-registers-temporary.md) (r \# ).</span><span class="sxs-lookup"><span data-stu-id="c137b-129">dst is a destination register and has to be a [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md) (r\#).</span></span> <span data-ttu-id="c137b-130">Il registro di destinazione deve avere esattamente una delle tre maschere seguenti:. x \| . y \| . XY.</span><span class="sxs-lookup"><span data-stu-id="c137b-130">The destination register must have exactly one of the following three masks: .x \| .y \| .xy.</span></span>
-   <span data-ttu-id="c137b-131">src0 è un registro di origine che fornisce l'angolo di input, che deve essere compreso tra \[ -pi, + pi \] .</span><span class="sxs-lookup"><span data-stu-id="c137b-131">src0 is a source register that provides the input angle, which must be within \[-pi, +pi\].</span></span> <span data-ttu-id="c137b-132">{x \| y \| z \| w} è la replica obbligatoria Swizzle.</span><span class="sxs-lookup"><span data-stu-id="c137b-132">{x\|y\|z\|w} is the required replicate swizzle.</span></span>

## <a name="remarks"></a><span data-ttu-id="c137b-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="c137b-133">Remarks</span></span>



| <span data-ttu-id="c137b-134">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="c137b-134">Vertex shader versions</span></span> | <span data-ttu-id="c137b-135">1\_1</span><span class="sxs-lookup"><span data-stu-id="c137b-135">1\_1</span></span> | <span data-ttu-id="c137b-136">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c137b-136">2\_0</span></span> | <span data-ttu-id="c137b-137">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c137b-137">2\_x</span></span> | <span data-ttu-id="c137b-138">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c137b-138">2\_sw</span></span> | <span data-ttu-id="c137b-139">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c137b-139">3\_0</span></span> | <span data-ttu-id="c137b-140">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c137b-140">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="c137b-141">SinCos</span><span class="sxs-lookup"><span data-stu-id="c137b-141">sincos</span></span>                 |      | <span data-ttu-id="c137b-142">x</span><span class="sxs-lookup"><span data-stu-id="c137b-142">x</span></span>    | <span data-ttu-id="c137b-143">x</span><span class="sxs-lookup"><span data-stu-id="c137b-143">x</span></span>    | <span data-ttu-id="c137b-144">x</span><span class="sxs-lookup"><span data-stu-id="c137b-144">x</span></span>     | <span data-ttu-id="c137b-145">x</span><span class="sxs-lookup"><span data-stu-id="c137b-145">x</span></span>    | <span data-ttu-id="c137b-146">x</span><span class="sxs-lookup"><span data-stu-id="c137b-146">x</span></span>     |



 

### <a name="vs_2_0-and-vs_2_x-remarks"></a><span data-ttu-id="c137b-147">\_osservazioni vs 2 \_ 0 e vs \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c137b-147">vs\_2\_0 and vs\_2\_x Remarks</span></span>

<span data-ttu-id="c137b-148">Per vs \_ 2 \_ 0 e vs \_ 2 \_ x, è possibile usare SinCos con predicazione, ma con una restrizione a swizzle del [registro predicato](dx9-graphics-reference-asm-vs-registers-predicate.md) (P0): è consentita solo la replica di swizzle (. x \| . y \| . z \| . w).</span><span class="sxs-lookup"><span data-stu-id="c137b-148">For vs\_2\_0 and vs\_2\_x, sincos can be used with predication, but with one restriction to the swizzle of the [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md) (p0): only replicate swizzle (.x \| .y \| .z \| .w) is allowed.</span></span>

<span data-ttu-id="c137b-149">Per vs \_ 2 \_ 0 e vs \_ 2 \_ x, l'istruzione funziona nel modo seguente: (V = valore scalare da src0 con un swizzle di replica):</span><span class="sxs-lookup"><span data-stu-id="c137b-149">For vs\_2\_0 and vs\_2\_x, the instruction operates as follows: (V = the scalar value from src0 with a replicate swizzle):</span></span>

-   <span data-ttu-id="c137b-150">Se la maschera di scrittura è. x:</span><span class="sxs-lookup"><span data-stu-id="c137b-150">If the write mask is .x:</span></span>
    ```
    dest.x = cos( V )
    dest.y is undefined when the instruction completes
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="c137b-151">Se la maschera di scrittura è. y:</span><span class="sxs-lookup"><span data-stu-id="c137b-151">If the write mask is .y:</span></span>
    ```
    dest.x is undefined when the instruction completes
    dest.y = sin( V )
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="c137b-152">Se la maschera di scrittura è. XY:</span><span class="sxs-lookup"><span data-stu-id="c137b-152">If the write mask is .xy:</span></span>
    ```
    dest.x = cos( V )
    dest.y = sin( V )
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

### <a name="vs_3_0-remarks"></a><span data-ttu-id="c137b-153">Osservazioni di vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c137b-153">vs\_3\_0 Remarks</span></span>

<span data-ttu-id="c137b-154">Per vs \_ 3 \_ 0, SinCos può essere usato con predicazione senza alcuna restrizione.</span><span class="sxs-lookup"><span data-stu-id="c137b-154">For vs\_3\_0, sincos can be used with predication without any restriction.</span></span> <span data-ttu-id="c137b-155">Vedere [registro predicato](dx9-graphics-reference-asm-vs-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="c137b-155">See [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md).</span></span>

<span data-ttu-id="c137b-156">Per vs \_ 3 \_ 0, l'istruzione funziona nel modo seguente: (V = valore scalare da src0 con un swizzle di replica)</span><span class="sxs-lookup"><span data-stu-id="c137b-156">For vs\_3\_0, the instruction operates as follows: (V = the scalar value from src0 with a replicate swizzle)</span></span>

-   <span data-ttu-id="c137b-157">Se la maschera di scrittura è. x:</span><span class="sxs-lookup"><span data-stu-id="c137b-157">If the write mask is .x:</span></span>
    ```
    dest.x = cos( V )
    dest.y is not touched by the instruction
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="c137b-158">Se la maschera di scrittura è. y:</span><span class="sxs-lookup"><span data-stu-id="c137b-158">If the write mask is .y:</span></span>
    ```
    dest.x is not touched by the instruction
    dest.y = sin( V )
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="c137b-159">Se la maschera di scrittura è. XY:</span><span class="sxs-lookup"><span data-stu-id="c137b-159">If the write mask is .xy:</span></span>
    ```
    dest.x = cos( V )
    dest.y = sin( V )
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

<span data-ttu-id="c137b-160">L'applicazione può eseguire il mapping di un angolo arbitrario (in radianti) all'intervallo \[ -pi, + pi greco \] usando lo pseudocodice dello shader seguente:</span><span class="sxs-lookup"><span data-stu-id="c137b-160">The application can map an arbitrary angle (in radians) to the range \[-pi, +pi\] using the following shader pseudocode:</span></span>


```
def c0, pi, 0.5, 2*pi, 1/(2*pi)
mad r0.x, input_angle, c0.w, c0.y
frc r0.x, r0.x
mad r0.x, r0.x, c0.z, -c0.x
```



## <a name="related-topics"></a><span data-ttu-id="c137b-161">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c137b-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c137b-162">Istruzioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="c137b-162">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
