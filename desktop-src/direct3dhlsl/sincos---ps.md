---
title: SinCos-PS
description: Calcola il seno e il coseno, in radianti. | SinCos-PS
ms.assetid: 639237ea-1b7a-4959-9093-78f134c11863
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1e7ccdca91af206862384ae14cf25a85d0817814
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995541"
---
# <a name="sincos---ps"></a><span data-ttu-id="15ecd-104">SinCos-PS</span><span class="sxs-lookup"><span data-stu-id="15ecd-104">sincos - ps</span></span>

<span data-ttu-id="15ecd-105">Calcola il seno e il coseno, in radianti.</span><span class="sxs-lookup"><span data-stu-id="15ecd-105">Computes sine and cosine, in radians.</span></span>

## <a name="syntax"></a><span data-ttu-id="15ecd-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="15ecd-106">Syntax</span></span>

### <a name="ps_2_0-and-ps_2_x"></a><span data-ttu-id="15ecd-107">PS \_ 2 \_ 0 e PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="15ecd-107">ps\_2\_0 and ps\_2\_x</span></span>



| <span data-ttu-id="15ecd-108">SinCos DST. x</span><span class="sxs-lookup"><span data-stu-id="15ecd-108">sincos dst.{x\</span></span>|<span data-ttu-id="15ecd-109">y</span><span class="sxs-lookup"><span data-stu-id="15ecd-109">y\</span></span>|<span data-ttu-id="15ecd-110">XY}, src0. x</span><span class="sxs-lookup"><span data-stu-id="15ecd-110">xy}, src0.{x\</span></span>|<span data-ttu-id="15ecd-111">y</span><span class="sxs-lookup"><span data-stu-id="15ecd-111">y\</span></span>|<span data-ttu-id="15ecd-112">z</span><span class="sxs-lookup"><span data-stu-id="15ecd-112">z\</span></span>|<span data-ttu-id="15ecd-113">w}, src1, src2</span><span class="sxs-lookup"><span data-stu-id="15ecd-113">w}, src1, src2</span></span> |
|------------------------------------------------------|



 

<span data-ttu-id="15ecd-114">Dove:</span><span class="sxs-lookup"><span data-stu-id="15ecd-114">Where:</span></span>

-   <span data-ttu-id="15ecd-115">DST è il registro di destinazione e deve essere un [registro temporaneo](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ).</span><span class="sxs-lookup"><span data-stu-id="15ecd-115">dst is the destination register and has to be a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#).</span></span> <span data-ttu-id="15ecd-116">Il registro di destinazione deve avere esattamente una delle tre maschere seguenti:. x \| . y \| . XY.</span><span class="sxs-lookup"><span data-stu-id="15ecd-116">The destination register must have exactly one of the following three masks: .x \| .y \| .xy.</span></span>
-   <span data-ttu-id="15ecd-117">src0 è un registro di origine che fornisce l'angolo di input, che deve essere compreso tra \[ -pi, + pi \] .</span><span class="sxs-lookup"><span data-stu-id="15ecd-117">src0 is a source register that provides the input angle, which must be within \[-pi, +pi\].</span></span> <span data-ttu-id="15ecd-118">{x \| y \| z \| w} è la replica obbligatoria Swizzle.</span><span class="sxs-lookup"><span data-stu-id="15ecd-118">{x\|y\|z\|w} is the required replicate swizzle.</span></span>
-   <span data-ttu-id="15ecd-119">src1 e src2 sono registri di origine e devono essere due diversi registri [float costanti](dx9-graphics-reference-asm-ps-registers-constant-float.md)(c \# ).</span><span class="sxs-lookup"><span data-stu-id="15ecd-119">src1 and src2 are source registers and must be two different [Constant Float Register](dx9-graphics-reference-asm-ps-registers-constant-float.md)s (c\#).</span></span> <span data-ttu-id="15ecd-120">I valori di src1 e src2 devono corrispondere rispettivamente alle macro [**D3DSINCOSCONST1**](/windows/desktop/direct3d9/d3dsincosconst1) e [**D3DSINCOSCONST2**](/windows/desktop/direct3d9/d3dsincosconst2) .</span><span class="sxs-lookup"><span data-stu-id="15ecd-120">The values of src1 and src2 must be that of the macros [**D3DSINCOSCONST1**](/windows/desktop/direct3d9/d3dsincosconst1) and [**D3DSINCOSCONST2**](/windows/desktop/direct3d9/d3dsincosconst2) respectively.</span></span>

### <a name="ps_3_0"></a><span data-ttu-id="15ecd-121">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="15ecd-121">ps\_3\_0</span></span>



| <span data-ttu-id="15ecd-122">SinCos DST. x</span><span class="sxs-lookup"><span data-stu-id="15ecd-122">sincos dst.{x\</span></span>|<span data-ttu-id="15ecd-123">y</span><span class="sxs-lookup"><span data-stu-id="15ecd-123">y\</span></span>|<span data-ttu-id="15ecd-124">XY}, src0. x</span><span class="sxs-lookup"><span data-stu-id="15ecd-124">xy}, src0.{x\</span></span>|<span data-ttu-id="15ecd-125">y</span><span class="sxs-lookup"><span data-stu-id="15ecd-125">y\</span></span>|<span data-ttu-id="15ecd-126">z</span><span class="sxs-lookup"><span data-stu-id="15ecd-126">z\</span></span>|<span data-ttu-id="15ecd-127">w</span><span class="sxs-lookup"><span data-stu-id="15ecd-127">w}</span></span> |
|------------------------------------------|



 

<span data-ttu-id="15ecd-128">Dove:</span><span class="sxs-lookup"><span data-stu-id="15ecd-128">Where:</span></span>

-   <span data-ttu-id="15ecd-129">DST è un registro di destinazione e deve essere un [registro temporaneo](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ).</span><span class="sxs-lookup"><span data-stu-id="15ecd-129">dst is a destination register and has to be a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#).</span></span> <span data-ttu-id="15ecd-130">Il registro di destinazione deve avere esattamente una delle tre maschere seguenti:. x \| . y \| . XY.</span><span class="sxs-lookup"><span data-stu-id="15ecd-130">The destination register must have exactly one of the following three masks: .x \| .y \| .xy.</span></span>
-   <span data-ttu-id="15ecd-131">src0 è un registro di origine che fornisce l'angolo di input, che deve essere compreso tra \[ -pi, + pi \] .</span><span class="sxs-lookup"><span data-stu-id="15ecd-131">src0 is a source register that provides the input angle, which must be within \[-pi, +pi\].</span></span> <span data-ttu-id="15ecd-132">{x \| y \| z \| w} è la replica obbligatoria Swizzle.</span><span class="sxs-lookup"><span data-stu-id="15ecd-132">{x\|y\|z\|w} is the required replicate swizzle.</span></span>

## <a name="remarks"></a><span data-ttu-id="15ecd-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="15ecd-133">Remarks</span></span>



| <span data-ttu-id="15ecd-134">Versioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="15ecd-134">Pixel shader versions</span></span> | <span data-ttu-id="15ecd-135">1\_1</span><span class="sxs-lookup"><span data-stu-id="15ecd-135">1\_1</span></span> | <span data-ttu-id="15ecd-136">1\_2</span><span class="sxs-lookup"><span data-stu-id="15ecd-136">1\_2</span></span> | <span data-ttu-id="15ecd-137">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="15ecd-137">1\_3</span></span> | <span data-ttu-id="15ecd-138">1\_4</span><span class="sxs-lookup"><span data-stu-id="15ecd-138">1\_4</span></span> | <span data-ttu-id="15ecd-139">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="15ecd-139">2\_0</span></span> | <span data-ttu-id="15ecd-140">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="15ecd-140">2\_x</span></span> | <span data-ttu-id="15ecd-141">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="15ecd-141">2\_sw</span></span> | <span data-ttu-id="15ecd-142">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="15ecd-142">3\_0</span></span> | <span data-ttu-id="15ecd-143">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="15ecd-143">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="15ecd-144">SinCos</span><span class="sxs-lookup"><span data-stu-id="15ecd-144">sincos</span></span>                |      |      |      |      | <span data-ttu-id="15ecd-145">x</span><span class="sxs-lookup"><span data-stu-id="15ecd-145">x</span></span>    | <span data-ttu-id="15ecd-146">x</span><span class="sxs-lookup"><span data-stu-id="15ecd-146">x</span></span>    | <span data-ttu-id="15ecd-147">x</span><span class="sxs-lookup"><span data-stu-id="15ecd-147">x</span></span>     | <span data-ttu-id="15ecd-148">x</span><span class="sxs-lookup"><span data-stu-id="15ecd-148">x</span></span>    | <span data-ttu-id="15ecd-149">x</span><span class="sxs-lookup"><span data-stu-id="15ecd-149">x</span></span>     |



 

### <a name="ps_2_0-and-ps_2_x"></a><span data-ttu-id="15ecd-150">PS \_ 2 \_ 0 e PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="15ecd-150">ps\_2\_0 and ps\_2\_x</span></span>

<span data-ttu-id="15ecd-151">Per PS \_ 2 \_ 0 e PS \_ 2 \_ x, è possibile usare SinCos con predicazione, ma con una restrizione a swizzle del [registro predicato](dx9-graphics-reference-asm-ps-registers-predicate.md) (P0): è consentita solo la replica di swizzle (. x \| . y \| . z \| . w).</span><span class="sxs-lookup"><span data-stu-id="15ecd-151">For ps\_2\_0 and ps\_2\_x, sincos can be used with predication, but with one restriction to the swizzle of the [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md) (p0): only replicate swizzle (.x \| .y \| .z \| .w) is allowed.</span></span>

<span data-ttu-id="15ecd-152">Per PS \_ 2 \_ 0 e PS \_ 2 \_ x, l'istruzione opera nel modo seguente (V = valore scalare da src0 con un swizzle di replica):</span><span class="sxs-lookup"><span data-stu-id="15ecd-152">For ps\_2\_0 and ps\_2\_x, the instruction operates as follows (V = the scalar value from src0 with a replicate swizzle):</span></span>

-   <span data-ttu-id="15ecd-153">Se la maschera di scrittura è. x:</span><span class="sxs-lookup"><span data-stu-id="15ecd-153">If the write mask is .x:</span></span>
    ```
    dest.x = cos(V)
    dest.y is undefined when the instruction completes
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="15ecd-154">Se la maschera di scrittura è. y:</span><span class="sxs-lookup"><span data-stu-id="15ecd-154">If the write mask is .y:</span></span>
    ```
    dest.x is undefined when the instruction completes
    dest.y = sin(V)
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="15ecd-155">Se la maschera di scrittura è. XY:</span><span class="sxs-lookup"><span data-stu-id="15ecd-155">If the write mask is .xy:</span></span>
    ```
    dest.x = cos(V)
    dest.y = sin(V)
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

### <a name="ps_3_0"></a><span data-ttu-id="15ecd-156">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="15ecd-156">ps\_3\_0</span></span>

<span data-ttu-id="15ecd-157">Per PS \_ 3 \_ 0, è possibile usare SinCos con predicazione senza alcuna restrizione.</span><span class="sxs-lookup"><span data-stu-id="15ecd-157">For ps\_3\_0, sincos can be used with predication without any restriction.</span></span> <span data-ttu-id="15ecd-158">Vedere [registro predicato](dx9-graphics-reference-asm-ps-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="15ecd-158">See [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).</span></span>

<span data-ttu-id="15ecd-159">Per PS \_ 3 \_ 0, l'istruzione funziona nel modo seguente (V = valore scalare da src0 con un swizzle di replica):</span><span class="sxs-lookup"><span data-stu-id="15ecd-159">For ps\_3\_0, the instruction operates as follows (V = the scalar value from src0 with a replicate swizzle):</span></span>

-   <span data-ttu-id="15ecd-160">Se la maschera di scrittura è. x:</span><span class="sxs-lookup"><span data-stu-id="15ecd-160">If the write mask is .x:</span></span>
    ```
    dest.x = cos(V)
    dest.y is not touched by the instruction
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="15ecd-161">Se la maschera di scrittura è. y:</span><span class="sxs-lookup"><span data-stu-id="15ecd-161">If the write mask is .y:</span></span>
    ```
    dest.x is not touched by the instruction
    dest.y = sin(V)
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="15ecd-162">Se la maschera di scrittura è. XY:</span><span class="sxs-lookup"><span data-stu-id="15ecd-162">If the write mask is .xy:</span></span>
    ```
    dest.x = cos(V)
    dest.y = sin(V)
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

<span data-ttu-id="15ecd-163">L'applicazione può eseguire il mapping di un angolo arbitrario (in radianti) all'intervallo \[ -pi, + pi greco \] usando lo pseudocodice dello shader seguente:</span><span class="sxs-lookup"><span data-stu-id="15ecd-163">The application can map an arbitrary angle (in radians) to the range \[-pi, +pi\] using the following shader pseudocode:</span></span>


```
def c0, pi, 0.5, 2*pi, 1/(2*pi)
mad r0.x, input_angle, c0.w, c0.y
frc r0.x, r0.x
mad r0.x, r0.x, c0.z, -c0.x
```



## <a name="related-topics"></a><span data-ttu-id="15ecd-164">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="15ecd-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15ecd-165">Istruzioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="15ecd-165">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 
