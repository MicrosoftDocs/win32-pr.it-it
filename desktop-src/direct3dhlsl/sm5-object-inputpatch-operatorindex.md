---
title: 'Funzione InputPatch:: operator'
description: "Restituisce l'ennesimo punto di controllo nella patch. | Funzione InputPatch:: operator"
ms.assetid: 2c1eda6b-a9c1-40d3-be91-7a2e8f1da9fc
keywords:
- Funzione operator HLSL
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5d95cb8adae6e7a91629614e0ae10b4161dbac3f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234722"
---
# <a name="inputpatchoperator--function"></a><span data-ttu-id="45b0b-105">Funzione InputPatch:: operator</span><span class="sxs-lookup"><span data-stu-id="45b0b-105">InputPatch::Operator  function</span></span>

<span data-ttu-id="45b0b-106">Restituisce il punto <sup>di controllo</sup> *n* nella patch.</span><span class="sxs-lookup"><span data-stu-id="45b0b-106">Returns the *n*<sup>th</sup> control point in the patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="45b0b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="45b0b-107">Syntax</span></span>

``` syntax
T Operator[](
  in uint n
);
```

## <a name="parameters"></a><span data-ttu-id="45b0b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="45b0b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45b0b-109">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="45b0b-109">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45b0b-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="45b0b-110">Type: **uint**</span></span>

<span data-ttu-id="45b0b-111">Indice di input.</span><span class="sxs-lookup"><span data-stu-id="45b0b-111">The input index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45b0b-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="45b0b-112">Return value</span></span>

<span data-ttu-id="45b0b-113">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="45b0b-113">Type: **T**</span></span>

<span data-ttu-id="45b0b-114">Il punto <sup>di controllo</sup> *n*.</span><span class="sxs-lookup"><span data-stu-id="45b0b-114">The *n*<sup>th</sup> control point.</span></span>

## <a name="remarks"></a><span data-ttu-id="45b0b-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="45b0b-115">Remarks</span></span>

<span data-ttu-id="45b0b-116">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="45b0b-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="45b0b-117">Vertice</span><span class="sxs-lookup"><span data-stu-id="45b0b-117">Vertex</span></span> | <span data-ttu-id="45b0b-118">Hull</span><span class="sxs-lookup"><span data-stu-id="45b0b-118">Hull</span></span> | <span data-ttu-id="45b0b-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="45b0b-119">Domain</span></span> | <span data-ttu-id="45b0b-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="45b0b-120">Geometry</span></span> | <span data-ttu-id="45b0b-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="45b0b-121">Pixel</span></span> | <span data-ttu-id="45b0b-122">Calcolo</span><span class="sxs-lookup"><span data-stu-id="45b0b-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="45b0b-123">x</span><span class="sxs-lookup"><span data-stu-id="45b0b-123">x</span></span>    |        |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="45b0b-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="45b0b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45b0b-125">InputPatch</span><span class="sxs-lookup"><span data-stu-id="45b0b-125">InputPatch</span></span>](sm5-object-inputpatch.md)
</dt> <dt>

[<span data-ttu-id="45b0b-126">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="45b0b-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




