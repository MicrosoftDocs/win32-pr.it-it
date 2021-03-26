---
title: firstbithigh (funzione)
description: Ottiene la posizione del primo bit impostato a partire dal bit di ordine più alto e il lavoro verso il basso, per componente.
ms.assetid: 0fa89a9e-1706-44f7-8dd3-c37af5c11ddc
keywords:
- Funzione firstbithigh HLSL
topic_type:
- apiref
api_name:
- firstbithigh
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4da4956aa3a12d064566a3767423f42039b01355
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399211"
---
# <a name="firstbithigh-function"></a><span data-ttu-id="e4fc9-104">firstbithigh (funzione)</span><span class="sxs-lookup"><span data-stu-id="e4fc9-104">firstbithigh function</span></span>

<span data-ttu-id="e4fc9-105">Ottiene la posizione del primo bit impostato a partire dal bit di ordine più alto e il lavoro verso il basso, per componente.</span><span class="sxs-lookup"><span data-stu-id="e4fc9-105">Gets the location of the first set bit starting from the highest order bit and working downward, per component.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4fc9-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e4fc9-106">Syntax</span></span>

``` syntax
int firstbithigh(
  in int value
);
```

## <a name="parameters"></a><span data-ttu-id="e4fc9-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="e4fc9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4fc9-108">*valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="e4fc9-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4fc9-109">Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e4fc9-109">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e4fc9-110">Valore di input.</span><span class="sxs-lookup"><span data-stu-id="e4fc9-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4fc9-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e4fc9-111">Return value</span></span>

<span data-ttu-id="e4fc9-112">Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e4fc9-112">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e4fc9-113">Posizione del primo bit impostato.</span><span class="sxs-lookup"><span data-stu-id="e4fc9-113">The location of the first set bit.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4fc9-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="e4fc9-114">Remarks</span></span>

<span data-ttu-id="e4fc9-115">Per un intero con segno, il primo bit significativo è zero per un numero negativo.</span><span class="sxs-lookup"><span data-stu-id="e4fc9-115">For a signed integer, the first significant bit is zero for a negative number.</span></span>

<span data-ttu-id="e4fc9-116">Sono disponibili anche le seguenti versioni di overload:</span><span class="sxs-lookup"><span data-stu-id="e4fc9-116">The following overloaded versions are also available:</span></span>

``` syntax
int2 firstbithigh(int2 value);
int3 firstbithigh(int3 value);
int4 firstbithigh(int4 value);
uint firstbithigh(uint value);
uint2 firstbithigh(uint2 value);
uint3 firstbithigh(uint3 value);
uint4 firstbithigh(uint4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="e4fc9-117">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="e4fc9-117">Minimum Shader Model</span></span>

<span data-ttu-id="e4fc9-118">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="e4fc9-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e4fc9-119">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="e4fc9-119">Shader Model</span></span>                                                                | <span data-ttu-id="e4fc9-120">Supportato</span><span class="sxs-lookup"><span data-stu-id="e4fc9-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="e4fc9-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="e4fc9-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="e4fc9-122">sì</span><span class="sxs-lookup"><span data-stu-id="e4fc9-122">yes</span></span>       |



 

<span data-ttu-id="e4fc9-123">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="e4fc9-123">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="e4fc9-124">Vertice</span><span class="sxs-lookup"><span data-stu-id="e4fc9-124">Vertex</span></span> | <span data-ttu-id="e4fc9-125">Hull</span><span class="sxs-lookup"><span data-stu-id="e4fc9-125">Hull</span></span> | <span data-ttu-id="e4fc9-126">Dominio</span><span class="sxs-lookup"><span data-stu-id="e4fc9-126">Domain</span></span> | <span data-ttu-id="e4fc9-127">Geometria</span><span class="sxs-lookup"><span data-stu-id="e4fc9-127">Geometry</span></span> | <span data-ttu-id="e4fc9-128">Pixel</span><span class="sxs-lookup"><span data-stu-id="e4fc9-128">Pixel</span></span> | <span data-ttu-id="e4fc9-129">Calcolo</span><span class="sxs-lookup"><span data-stu-id="e4fc9-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="e4fc9-130">x</span><span class="sxs-lookup"><span data-stu-id="e4fc9-130">x</span></span>      | <span data-ttu-id="e4fc9-131">x</span><span class="sxs-lookup"><span data-stu-id="e4fc9-131">x</span></span>    | <span data-ttu-id="e4fc9-132">x</span><span class="sxs-lookup"><span data-stu-id="e4fc9-132">x</span></span>      | <span data-ttu-id="e4fc9-133">x</span><span class="sxs-lookup"><span data-stu-id="e4fc9-133">x</span></span>        | <span data-ttu-id="e4fc9-134">x</span><span class="sxs-lookup"><span data-stu-id="e4fc9-134">x</span></span>     | <span data-ttu-id="e4fc9-135">x</span><span class="sxs-lookup"><span data-stu-id="e4fc9-135">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="e4fc9-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e4fc9-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4fc9-137">Funzioni intrinseche</span><span class="sxs-lookup"><span data-stu-id="e4fc9-137">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="e4fc9-138">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="e4fc9-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 