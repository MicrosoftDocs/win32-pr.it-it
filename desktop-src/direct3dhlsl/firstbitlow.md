---
title: firstbitlow (funzione)
description: Restituisce la posizione del primo bit impostato a partire dal bit di ordine più basso e procedendo verso l'alto, per componente.
ms.assetid: 204250f3-1a9b-445d-bd16-4cc9a5d9d60a
keywords:
- Funzione firstbitlow HLSL
topic_type:
- apiref
api_name:
- firstbitlow
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a647314383bc022b7c3b3e1b5a255a42a099c620
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046937"
---
# <a name="firstbitlow-function"></a><span data-ttu-id="92b13-104">firstbitlow (funzione)</span><span class="sxs-lookup"><span data-stu-id="92b13-104">firstbitlow function</span></span>

<span data-ttu-id="92b13-105">Restituisce la posizione del primo bit impostato a partire dal bit di ordine più basso e procedendo verso l'alto, per componente.</span><span class="sxs-lookup"><span data-stu-id="92b13-105">Returns the location of the first set bit starting from the lowest order bit and working upward, per component.</span></span>

## <a name="syntax"></a><span data-ttu-id="92b13-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="92b13-106">Syntax</span></span>

``` syntax
int firstbitlow(
  in int value
);
```

## <a name="parameters"></a><span data-ttu-id="92b13-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="92b13-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92b13-108">*valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="92b13-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92b13-109">Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="92b13-109">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="92b13-110">Valore di input.</span><span class="sxs-lookup"><span data-stu-id="92b13-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92b13-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="92b13-111">Return value</span></span>

<span data-ttu-id="92b13-112">Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="92b13-112">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="92b13-113">Posizione del primo bit impostato.</span><span class="sxs-lookup"><span data-stu-id="92b13-113">The location of the first set bit.</span></span>

## <a name="remarks"></a><span data-ttu-id="92b13-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="92b13-114">Remarks</span></span>

<span data-ttu-id="92b13-115">Sono disponibili anche le seguenti versioni di overload:</span><span class="sxs-lookup"><span data-stu-id="92b13-115">The following overloaded versions are also available:</span></span>

``` syntax
uint2 firstbitlow(uint2 value);
uint3 firstbitlow(uint3 value);
uint4 firstbitlow(uint4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="92b13-116">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="92b13-116">Minimum Shader Model</span></span>

<span data-ttu-id="92b13-117">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="92b13-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="92b13-118">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="92b13-118">Shader Model</span></span>                                                                | <span data-ttu-id="92b13-119">Supportato</span><span class="sxs-lookup"><span data-stu-id="92b13-119">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="92b13-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="92b13-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="92b13-121">sì</span><span class="sxs-lookup"><span data-stu-id="92b13-121">yes</span></span>       |



 

<span data-ttu-id="92b13-122">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="92b13-122">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="92b13-123">Vertice</span><span class="sxs-lookup"><span data-stu-id="92b13-123">Vertex</span></span> | <span data-ttu-id="92b13-124">Hull</span><span class="sxs-lookup"><span data-stu-id="92b13-124">Hull</span></span> | <span data-ttu-id="92b13-125">Dominio</span><span class="sxs-lookup"><span data-stu-id="92b13-125">Domain</span></span> | <span data-ttu-id="92b13-126">Geometria</span><span class="sxs-lookup"><span data-stu-id="92b13-126">Geometry</span></span> | <span data-ttu-id="92b13-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="92b13-127">Pixel</span></span> | <span data-ttu-id="92b13-128">Calcolo</span><span class="sxs-lookup"><span data-stu-id="92b13-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="92b13-129">x</span><span class="sxs-lookup"><span data-stu-id="92b13-129">x</span></span>      | <span data-ttu-id="92b13-130">x</span><span class="sxs-lookup"><span data-stu-id="92b13-130">x</span></span>    | <span data-ttu-id="92b13-131">x</span><span class="sxs-lookup"><span data-stu-id="92b13-131">x</span></span>      | <span data-ttu-id="92b13-132">x</span><span class="sxs-lookup"><span data-stu-id="92b13-132">x</span></span>        | <span data-ttu-id="92b13-133">x</span><span class="sxs-lookup"><span data-stu-id="92b13-133">x</span></span>     | <span data-ttu-id="92b13-134">x</span><span class="sxs-lookup"><span data-stu-id="92b13-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="92b13-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="92b13-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92b13-136">Funzioni intrinseche</span><span class="sxs-lookup"><span data-stu-id="92b13-136">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="92b13-137">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="92b13-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 