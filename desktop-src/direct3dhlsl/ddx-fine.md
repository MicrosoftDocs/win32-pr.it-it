---
title: funzione ddx_fine
description: Calcola una derivata parziale a precisione elevata rispetto alla coordinata x dello spazio dello schermo. | funzione ddx_fine
ms.assetid: 41062d6f-2b7f-4594-a6de-da37ded5d444
keywords:
- funzione ddx_fine HLSL
topic_type:
- apiref
api_name:
- ddx_fine
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c1a579ba5899cf4d3ac3f25ef5a40337f6291977
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104982082"
---
# <a name="ddx_fine-function"></a><span data-ttu-id="7edc9-105">\_funzione DDX fine</span><span class="sxs-lookup"><span data-stu-id="7edc9-105">ddx\_fine function</span></span>

<span data-ttu-id="7edc9-106">Calcola una derivata parziale a precisione elevata rispetto alla coordinata x dello spazio dello schermo.</span><span class="sxs-lookup"><span data-stu-id="7edc9-106">Computes a high precision partial derivative with respect to the screen-space x-coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="7edc9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7edc9-107">Syntax</span></span>

``` syntax
float ddx_fine(
  in float value
);
```

## <a name="parameters"></a><span data-ttu-id="7edc9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7edc9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7edc9-109">*valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="7edc9-109">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7edc9-110">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="7edc9-110">Type: **float**</span></span>

<span data-ttu-id="7edc9-111">Valore di input.</span><span class="sxs-lookup"><span data-stu-id="7edc9-111">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7edc9-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7edc9-112">Return value</span></span>

<span data-ttu-id="7edc9-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="7edc9-113">Type: **float**</span></span>

<span data-ttu-id="7edc9-114">Derivato parziale di precisione elevata del *valore*.</span><span class="sxs-lookup"><span data-stu-id="7edc9-114">The high precision partial derivative of *value*.</span></span>

## <a name="remarks"></a><span data-ttu-id="7edc9-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="7edc9-115">Remarks</span></span>

<span data-ttu-id="7edc9-116">Sono disponibili anche le seguenti versioni di overload:</span><span class="sxs-lookup"><span data-stu-id="7edc9-116">The following overloaded versions are also available:</span></span>

``` syntax
float2 ddx_fine(float2 value);
float3 ddx_fine(float3 value);
float4 ddx_fine(float4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="7edc9-117">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="7edc9-117">Minimum Shader Model</span></span>

<span data-ttu-id="7edc9-118">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="7edc9-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="7edc9-119">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="7edc9-119">Shader Model</span></span>                                                                | <span data-ttu-id="7edc9-120">Supportato</span><span class="sxs-lookup"><span data-stu-id="7edc9-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="7edc9-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="7edc9-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="7edc9-122">sì</span><span class="sxs-lookup"><span data-stu-id="7edc9-122">yes</span></span>       |



 

<span data-ttu-id="7edc9-123">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="7edc9-123">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="7edc9-124">Vertice</span><span class="sxs-lookup"><span data-stu-id="7edc9-124">Vertex</span></span> | <span data-ttu-id="7edc9-125">Hull</span><span class="sxs-lookup"><span data-stu-id="7edc9-125">Hull</span></span> | <span data-ttu-id="7edc9-126">Dominio</span><span class="sxs-lookup"><span data-stu-id="7edc9-126">Domain</span></span> | <span data-ttu-id="7edc9-127">Geometria</span><span class="sxs-lookup"><span data-stu-id="7edc9-127">Geometry</span></span> | <span data-ttu-id="7edc9-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="7edc9-128">Pixel</span></span> | <span data-ttu-id="7edc9-129">Calcolo</span><span class="sxs-lookup"><span data-stu-id="7edc9-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="7edc9-130">x</span><span class="sxs-lookup"><span data-stu-id="7edc9-130">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="7edc9-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7edc9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7edc9-132">Funzioni intrinseche</span><span class="sxs-lookup"><span data-stu-id="7edc9-132">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="7edc9-133">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="7edc9-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




