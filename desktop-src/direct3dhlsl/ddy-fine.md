---
title: funzione ddy_fine
description: Calcola una derivata parziale a precisione elevata rispetto alla coordinata x dello spazio dello schermo. | funzione ddy_fine
ms.assetid: 29fcdbc9-470b-4b5b-b18c-f75dd2c87920
keywords:
- funzione ddy_fine HLSL
topic_type:
- apiref
api_name:
- ddy_fine
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2a4cb297180a4988cb049ccebfa4f82571c4655c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995774"
---
# <a name="ddy_fine-function"></a><span data-ttu-id="05d9f-105">\_funzione ddy fine</span><span class="sxs-lookup"><span data-stu-id="05d9f-105">ddy\_fine function</span></span>

<span data-ttu-id="05d9f-106">Calcola una derivata parziale a precisione elevata rispetto alla coordinata x dello spazio dello schermo.</span><span class="sxs-lookup"><span data-stu-id="05d9f-106">Computes a high precision partial derivative with respect to the screen-space x-coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="05d9f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="05d9f-107">Syntax</span></span>

``` syntax
float ddy_fine(
  in float value
);
```

## <a name="parameters"></a><span data-ttu-id="05d9f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="05d9f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05d9f-109">*valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="05d9f-109">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05d9f-110">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="05d9f-110">Type: **float**</span></span>

<span data-ttu-id="05d9f-111">Valore di input.</span><span class="sxs-lookup"><span data-stu-id="05d9f-111">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05d9f-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="05d9f-112">Return value</span></span>

<span data-ttu-id="05d9f-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="05d9f-113">Type: **float**</span></span>

<span data-ttu-id="05d9f-114">Derivato parziale di precisione elevata del *valore*.</span><span class="sxs-lookup"><span data-stu-id="05d9f-114">The high precision partial derivative of *value*.</span></span>

## <a name="remarks"></a><span data-ttu-id="05d9f-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="05d9f-115">Remarks</span></span>

<span data-ttu-id="05d9f-116">Sono disponibili anche le seguenti versioni di overload:</span><span class="sxs-lookup"><span data-stu-id="05d9f-116">The following overloaded versions are also available:</span></span>

``` syntax
float2 ddy_fine(float2 value);
float3 ddy_fine(float3 value);
float4 ddy_fine(float4 value);  
```

### <a name="minimum-shader-model"></a><span data-ttu-id="05d9f-117">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="05d9f-117">Minimum Shader Model</span></span>

<span data-ttu-id="05d9f-118">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="05d9f-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="05d9f-119">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="05d9f-119">Shader Model</span></span>                                                                | <span data-ttu-id="05d9f-120">Supportato</span><span class="sxs-lookup"><span data-stu-id="05d9f-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="05d9f-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="05d9f-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="05d9f-122">sì</span><span class="sxs-lookup"><span data-stu-id="05d9f-122">yes</span></span>       |



 

<span data-ttu-id="05d9f-123">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="05d9f-123">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="05d9f-124">Vertice</span><span class="sxs-lookup"><span data-stu-id="05d9f-124">Vertex</span></span> | <span data-ttu-id="05d9f-125">Hull</span><span class="sxs-lookup"><span data-stu-id="05d9f-125">Hull</span></span> | <span data-ttu-id="05d9f-126">Dominio</span><span class="sxs-lookup"><span data-stu-id="05d9f-126">Domain</span></span> | <span data-ttu-id="05d9f-127">Geometria</span><span class="sxs-lookup"><span data-stu-id="05d9f-127">Geometry</span></span> | <span data-ttu-id="05d9f-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="05d9f-128">Pixel</span></span> | <span data-ttu-id="05d9f-129">Calcolo</span><span class="sxs-lookup"><span data-stu-id="05d9f-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="05d9f-130">x</span><span class="sxs-lookup"><span data-stu-id="05d9f-130">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="05d9f-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="05d9f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05d9f-132">Funzioni intrinseche</span><span class="sxs-lookup"><span data-stu-id="05d9f-132">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="05d9f-133">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="05d9f-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




