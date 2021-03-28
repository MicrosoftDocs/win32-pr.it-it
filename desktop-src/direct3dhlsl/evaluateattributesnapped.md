---
title: EvaluateAttributeSnapped (funzione)
description: Valuta in corrispondenza del baricentro del pixel con un offset.
ms.assetid: f5085016-0e94-49bb-96b6-42fa15c30b9f
keywords:
- Funzione EvaluateAttributeSnapped HLSL
topic_type:
- apiref
api_name:
- EvaluateAttributeSnapped
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 70a9389ed9e9f4fff16f82610cb611bc4da2c7a3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104992896"
---
# <a name="evaluateattributesnapped-function"></a><span data-ttu-id="4e03f-104">EvaluateAttributeSnapped (funzione)</span><span class="sxs-lookup"><span data-stu-id="4e03f-104">EvaluateAttributeSnapped function</span></span>

<span data-ttu-id="4e03f-105">Valuta in corrispondenza del baricentro del pixel con un offset.</span><span class="sxs-lookup"><span data-stu-id="4e03f-105">Evaluates at the pixel centroid with an offset.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e03f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4e03f-106">Syntax</span></span>

``` syntax
numeric EvaluateAttributeSnapped(
  in attrib numeric value,
  in 
            int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="4e03f-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="4e03f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e03f-108">*valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="4e03f-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e03f-109">Tipo: formato **numerico attrib**</span><span class="sxs-lookup"><span data-stu-id="4e03f-109">Type: **attrib numeric**</span></span>

<span data-ttu-id="4e03f-110">Valore di input.</span><span class="sxs-lookup"><span data-stu-id="4e03f-110">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="4e03f-111">*offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e03f-111">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e03f-112">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="4e03f-112">Type: **int2**</span></span>

<span data-ttu-id="4e03f-113">Offset 2D dal centro pixel mediante una griglia 16x16.</span><span class="sxs-lookup"><span data-stu-id="4e03f-113">A 2D offset from the pixel center using a 16x16 grid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4e03f-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="4e03f-114">Remarks</span></span>

<span data-ttu-id="4e03f-115">L'intervallo per il parametro *offset* deve essere definito dal codice byte seguente.</span><span class="sxs-lookup"><span data-stu-id="4e03f-115">The range for the *offset* parameter must be defined by the following byte code.</span></span>

<span data-ttu-id="4e03f-116">Vengono utilizzati solo i 4 bit meno significativi dei primi due componenti (U, V) dell'offset pixel.</span><span class="sxs-lookup"><span data-stu-id="4e03f-116">Only the least significant 4 bits of the first two components (U, V) of the pixel offset are used.</span></span> <span data-ttu-id="4e03f-117">La conversione dal punto fisso a 4 bit a float è la seguente (MSB... LSB), in cui MSB è una parte della frazione e determina il segno:</span><span class="sxs-lookup"><span data-stu-id="4e03f-117">The conversion from the 4-bit fixed point to float is as follows (MSB...LSB), where the MSB is both a part of the fraction and determines the sign:</span></span>

-   <span data-ttu-id="4e03f-118">1000 =-0,5 f (-8/16)</span><span class="sxs-lookup"><span data-stu-id="4e03f-118">1000 = -0.5f (-8 / 16)</span></span>
-   <span data-ttu-id="4e03f-119">1001 =-0.4375 f (-7/16)</span><span class="sxs-lookup"><span data-stu-id="4e03f-119">1001 = -0.4375f (-7 / 16)</span></span>
-   <span data-ttu-id="4e03f-120">1010 =-0.375 f (-6/16)</span><span class="sxs-lookup"><span data-stu-id="4e03f-120">1010 = -0.375f (-6 / 16)</span></span>
-   <span data-ttu-id="4e03f-121">1011 =-0.3125 f (-5/16)</span><span class="sxs-lookup"><span data-stu-id="4e03f-121">1011 = -0.3125f (-5 / 16)</span></span>
-   <span data-ttu-id="4e03f-122">1100 =-0,25 f (-4/16)</span><span class="sxs-lookup"><span data-stu-id="4e03f-122">1100 = -0.25f (-4 / 16)</span></span>
-   <span data-ttu-id="4e03f-123">1101 =-0.1875 f (-3/16)</span><span class="sxs-lookup"><span data-stu-id="4e03f-123">1101 = -0.1875f (-3 / 16)</span></span>
-   <span data-ttu-id="4e03f-124">1110 =-0,125 f (-2/16)</span><span class="sxs-lookup"><span data-stu-id="4e03f-124">1110 = -0.125f (-2 / 16)</span></span>
-   <span data-ttu-id="4e03f-125">1111 =-0.0625 f (-1/16)</span><span class="sxs-lookup"><span data-stu-id="4e03f-125">1111 = -0.0625f (-1 / 16)</span></span>
-   <span data-ttu-id="4e03f-126">0000 = 0,0 f (0/16)</span><span class="sxs-lookup"><span data-stu-id="4e03f-126">0000 = 0.0f ( 0 / 16)</span></span>
-   <span data-ttu-id="4e03f-127">0001 = 0.0625 f (1/16)</span><span class="sxs-lookup"><span data-stu-id="4e03f-127">0001 = 0.0625f ( 1 / 16)</span></span>
-   <span data-ttu-id="4e03f-128">0010 = 0,125 f (2/16)</span><span class="sxs-lookup"><span data-stu-id="4e03f-128">0010 = 0.125f ( 2 / 16)</span></span>
-   <span data-ttu-id="4e03f-129">0011 = 0.1875 f (3/16)</span><span class="sxs-lookup"><span data-stu-id="4e03f-129">0011 = 0.1875f ( 3 / 16)</span></span>
-   <span data-ttu-id="4e03f-130">0100 = 0,25 f (4/16)</span><span class="sxs-lookup"><span data-stu-id="4e03f-130">0100 = 0.25f ( 4 / 16)</span></span>
-   <span data-ttu-id="4e03f-131">0101 = 0.3125 f (5/16)</span><span class="sxs-lookup"><span data-stu-id="4e03f-131">0101 = 0.3125f ( 5 / 16)</span></span>
-   <span data-ttu-id="4e03f-132">0110 = 0.375 f (6/16)</span><span class="sxs-lookup"><span data-stu-id="4e03f-132">0110 = 0.375f ( 6 / 16)</span></span>
-   <span data-ttu-id="4e03f-133">0111 = 0.4375 f (7/16)</span><span class="sxs-lookup"><span data-stu-id="4e03f-133">0111 = 0.4375f ( 7 / 16)</span></span>

> [!Note]  
> <span data-ttu-id="4e03f-134">I bordi sinistro e superiore di un pixel sono inclusi nell'offset; Tuttavia, i bordi inferiore e destro non sono inclusi.</span><span class="sxs-lookup"><span data-stu-id="4e03f-134">The left and top edges of a pixel are included in the offset; however, the bottom and right edges are not included.</span></span> <span data-ttu-id="4e03f-135">Tutti gli altri bit nei valori di offset integer a 32 bit vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="4e03f-135">All other bits in the 32-bit integer U and V offset values are ignored.</span></span>

 

<span data-ttu-id="4e03f-136">Un'implementazione può assumere l'offset fornito dallo shader e ottenere un valore a punto fisso a 32 bit completo (28,4), che si estende sull'intervallo valido, eseguendo il calcolo seguente:</span><span class="sxs-lookup"><span data-stu-id="4e03f-136">An implementation can take the offset provided by the shader and obtain a full 32-bit fixed point value (28.4), which spans the valid range, by performing the following calculation:</span></span>


```
iU = (iU<<28)>>28  // keep lowest 4 bits and sign extend, which yields [-8..7]
```



<span data-ttu-id="4e03f-137">Se un'implementazione deve eseguire il mapping dell'offset a un offset a virgola mobile, viene eseguito il calcolo seguente:</span><span class="sxs-lookup"><span data-stu-id="4e03f-137">If an implementation must map the offset to a floating-point offset, it performs the following calculation:</span></span>


```
fU = ((float)iU)/16
```



### <a name="minimum-shader-model"></a><span data-ttu-id="4e03f-138">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="4e03f-138">Minimum Shader Model</span></span>

<span data-ttu-id="4e03f-139">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="4e03f-139">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="4e03f-140">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="4e03f-140">Shader Model</span></span>                                                                | <span data-ttu-id="4e03f-141">Supportato</span><span class="sxs-lookup"><span data-stu-id="4e03f-141">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="4e03f-142">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="4e03f-142">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="4e03f-143">sì</span><span class="sxs-lookup"><span data-stu-id="4e03f-143">yes</span></span>       |



 

<span data-ttu-id="4e03f-144">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="4e03f-144">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="4e03f-145">Vertice</span><span class="sxs-lookup"><span data-stu-id="4e03f-145">Vertex</span></span> | <span data-ttu-id="4e03f-146">Hull</span><span class="sxs-lookup"><span data-stu-id="4e03f-146">Hull</span></span> | <span data-ttu-id="4e03f-147">Dominio</span><span class="sxs-lookup"><span data-stu-id="4e03f-147">Domain</span></span> | <span data-ttu-id="4e03f-148">Geometria</span><span class="sxs-lookup"><span data-stu-id="4e03f-148">Geometry</span></span> | <span data-ttu-id="4e03f-149">Pixel</span><span class="sxs-lookup"><span data-stu-id="4e03f-149">Pixel</span></span> | <span data-ttu-id="4e03f-150">Calcolo</span><span class="sxs-lookup"><span data-stu-id="4e03f-150">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="4e03f-151">x</span><span class="sxs-lookup"><span data-stu-id="4e03f-151">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="4e03f-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4e03f-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e03f-153">Funzioni intrinseche</span><span class="sxs-lookup"><span data-stu-id="4e03f-153">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="4e03f-154">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="4e03f-154">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




