---
title: AsDouble (funzione)
description: Reinterpreta un valore cast (valori a 2 32 bit) in un valore Double.
ms.assetid: 55e5276d-81e1-4e7e-8cb4-0beb57d2fb7f
keywords:
- funzione AsDouble HLSL
topic_type:
- apiref
api_name:
- asdouble
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: caa2c83ee01739a2e2ee9595d0a26e1bdb80fef1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045893"
---
# <a name="asdouble-function"></a><span data-ttu-id="c769c-104">AsDouble (funzione)</span><span class="sxs-lookup"><span data-stu-id="c769c-104">asdouble function</span></span>

<span data-ttu-id="c769c-105">Reinterpreta un valore cast (valori a 2 32 bit) in un valore Double.</span><span class="sxs-lookup"><span data-stu-id="c769c-105">Reinterprets a cast value (two 32-bit values) into a double.</span></span>

## <a name="syntax"></a><span data-ttu-id="c769c-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c769c-106">Syntax</span></span>

``` syntax
double asdouble(
  in uint lowbits,
  in uint highbits
);
```

## <a name="parameters"></a><span data-ttu-id="c769c-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="c769c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c769c-108">*lowbits* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c769c-108">*lowbits* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c769c-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="c769c-109">Type: **uint**</span></span>

<span data-ttu-id="c769c-110">Modello a 32 bit basso del valore di input.</span><span class="sxs-lookup"><span data-stu-id="c769c-110">The low 32-bit pattern of the input value.</span></span>

</dd> <dt>

<span data-ttu-id="c769c-111">*highbits* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c769c-111">*highbits* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c769c-112">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="c769c-112">Type: **uint**</span></span>

<span data-ttu-id="c769c-113">Modello a 32 bit elevato del valore di input.</span><span class="sxs-lookup"><span data-stu-id="c769c-113">The high 32-bit pattern of the input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c769c-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c769c-114">Return value</span></span>

<span data-ttu-id="c769c-115">Tipo: **Double**</span><span class="sxs-lookup"><span data-stu-id="c769c-115">Type: **double**</span></span>

<span data-ttu-id="c769c-116">L'input (valori a 2 32 bit) viene rieseguito come Double.</span><span class="sxs-lookup"><span data-stu-id="c769c-116">The input (two 32-bit values) recast as a double.</span></span>

## <a name="remarks"></a><span data-ttu-id="c769c-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="c769c-117">Remarks</span></span>

<span data-ttu-id="c769c-118">È disponibile anche la versione di overload seguente:</span><span class="sxs-lookup"><span data-stu-id="c769c-118">The following overloaded version is also available:</span></span>

``` syntax
double2 asdouble(uint2 lowbits, uint2 highbits);
```

<span data-ttu-id="c769c-119">Se il valore di input è costituito da componenti a 2 32 bit, il tipo restituito conterrà un valore Double.</span><span class="sxs-lookup"><span data-stu-id="c769c-119">If the input value is two 32-bit components, the return type will contain one double.</span></span> <span data-ttu-id="c769c-120">Se il valore di input è costituito da componenti a 4 32 bit, il tipo restituito conterrà due Double.</span><span class="sxs-lookup"><span data-stu-id="c769c-120">If the input value is four 32-bit components, the return type will contain two doubles.</span></span> <span data-ttu-id="c769c-121">Se il valore di input è un tipo a 64 bit, il valore restituito avrà lo stesso numero di componenti del valore di input.</span><span class="sxs-lookup"><span data-stu-id="c769c-121">If the input value is a 64-bit type, the returned value will have the same number of components as the input value.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="c769c-122">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="c769c-122">Minimum Shader Model</span></span>

<span data-ttu-id="c769c-123">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="c769c-123">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c769c-124">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="c769c-124">Shader Model</span></span>                                                                | <span data-ttu-id="c769c-125">Supportato</span><span class="sxs-lookup"><span data-stu-id="c769c-125">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="c769c-126">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="c769c-126">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="c769c-127">sì</span><span class="sxs-lookup"><span data-stu-id="c769c-127">yes</span></span>       |



 

<span data-ttu-id="c769c-128">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="c769c-128">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="c769c-129">Vertice</span><span class="sxs-lookup"><span data-stu-id="c769c-129">Vertex</span></span> | <span data-ttu-id="c769c-130">Hull</span><span class="sxs-lookup"><span data-stu-id="c769c-130">Hull</span></span> | <span data-ttu-id="c769c-131">Dominio</span><span class="sxs-lookup"><span data-stu-id="c769c-131">Domain</span></span> | <span data-ttu-id="c769c-132">Geometria</span><span class="sxs-lookup"><span data-stu-id="c769c-132">Geometry</span></span> | <span data-ttu-id="c769c-133">Pixel</span><span class="sxs-lookup"><span data-stu-id="c769c-133">Pixel</span></span> | <span data-ttu-id="c769c-134">Calcolo</span><span class="sxs-lookup"><span data-stu-id="c769c-134">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="c769c-135">x</span><span class="sxs-lookup"><span data-stu-id="c769c-135">x</span></span>      | <span data-ttu-id="c769c-136">x</span><span class="sxs-lookup"><span data-stu-id="c769c-136">x</span></span>    | <span data-ttu-id="c769c-137">x</span><span class="sxs-lookup"><span data-stu-id="c769c-137">x</span></span>      | <span data-ttu-id="c769c-138">x</span><span class="sxs-lookup"><span data-stu-id="c769c-138">x</span></span>        | <span data-ttu-id="c769c-139">x</span><span class="sxs-lookup"><span data-stu-id="c769c-139">x</span></span>     | <span data-ttu-id="c769c-140">x</span><span class="sxs-lookup"><span data-stu-id="c769c-140">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="c769c-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c769c-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c769c-142">Funzioni intrinseche</span><span class="sxs-lookup"><span data-stu-id="c769c-142">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="c769c-143">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="c769c-143">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




