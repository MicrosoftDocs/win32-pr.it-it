---
title: funzione ddy_coarse
description: Calcola una derivata parziale con precisione bassa rispetto alla coordinata y dello spazio dello schermo.
ms.assetid: f6103cd3-f7ee-41c2-b3cf-9e72ca84b25e
keywords:
- funzione ddy_coarse HLSL
topic_type:
- apiref
api_name:
- ddy_coarse
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b6fef330e919a31e39306742bb03280454d47626
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045874"
---
# <a name="ddy_coarse-function"></a><span data-ttu-id="33643-104">ddy- \_ funzione grossolana</span><span class="sxs-lookup"><span data-stu-id="33643-104">ddy\_coarse function</span></span>

<span data-ttu-id="33643-105">Calcola una derivata parziale con precisione bassa rispetto alla coordinata y dello spazio dello schermo.</span><span class="sxs-lookup"><span data-stu-id="33643-105">Computes a low precision partial derivative with respect to the screen-space y-coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="33643-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="33643-106">Syntax</span></span>

``` syntax
float ddy_coarse(
  in float value
);
```

## <a name="parameters"></a><span data-ttu-id="33643-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="33643-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33643-108">*valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="33643-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33643-109">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="33643-109">Type: **float**</span></span>

<span data-ttu-id="33643-110">Valore di input.</span><span class="sxs-lookup"><span data-stu-id="33643-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33643-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="33643-111">Return value</span></span>

<span data-ttu-id="33643-112">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="33643-112">Type: **float**</span></span>

<span data-ttu-id="33643-113">Derivato parziale di precisione bassa del *valore*.</span><span class="sxs-lookup"><span data-stu-id="33643-113">The low precision partial derivative of *value*.</span></span>

## <a name="remarks"></a><span data-ttu-id="33643-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="33643-114">Remarks</span></span>

<span data-ttu-id="33643-115">Sono disponibili anche le seguenti versioni di overload:</span><span class="sxs-lookup"><span data-stu-id="33643-115">The following overloaded versions are also available:</span></span>

``` syntax
float2 ddy_coarse(float2 value);
float3 ddy_coarse(float3 value);
float4 ddy_coarse(float4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="33643-116">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="33643-116">Minimum Shader Model</span></span>

<span data-ttu-id="33643-117">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="33643-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="33643-118">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="33643-118">Shader Model</span></span>                                                                | <span data-ttu-id="33643-119">Supportato</span><span class="sxs-lookup"><span data-stu-id="33643-119">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="33643-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="33643-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="33643-121">sì</span><span class="sxs-lookup"><span data-stu-id="33643-121">yes</span></span>       |



 

<span data-ttu-id="33643-122">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="33643-122">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="33643-123">Vertice</span><span class="sxs-lookup"><span data-stu-id="33643-123">Vertex</span></span> | <span data-ttu-id="33643-124">Hull</span><span class="sxs-lookup"><span data-stu-id="33643-124">Hull</span></span> | <span data-ttu-id="33643-125">Dominio</span><span class="sxs-lookup"><span data-stu-id="33643-125">Domain</span></span> | <span data-ttu-id="33643-126">Geometria</span><span class="sxs-lookup"><span data-stu-id="33643-126">Geometry</span></span> | <span data-ttu-id="33643-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="33643-127">Pixel</span></span> | <span data-ttu-id="33643-128">Calcolo</span><span class="sxs-lookup"><span data-stu-id="33643-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="33643-129">x</span><span class="sxs-lookup"><span data-stu-id="33643-129">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="33643-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="33643-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33643-131">Funzioni intrinseche</span><span class="sxs-lookup"><span data-stu-id="33643-131">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="33643-132">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="33643-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




