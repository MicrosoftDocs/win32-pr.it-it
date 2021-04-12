---
title: 'Funzione OutputPatch:: operator'
description: "Restituisce l'ennesimo punto di controllo nella patch. | Funzione OutputPatch:: operator"
ms.assetid: 3ac15fe8-8bab-46a2-8826-61ade927c99e
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
ms.openlocfilehash: 8194713dc4967151991fab95000fa70c40122f26
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352711"
---
# <a name="outputpatchoperator--function"></a><span data-ttu-id="9f032-105">Funzione OutputPatch:: operator</span><span class="sxs-lookup"><span data-stu-id="9f032-105">OutputPatch::Operator  function</span></span>

<span data-ttu-id="9f032-106">Restituisce il punto <sup>di controllo</sup> *n* nella patch.</span><span class="sxs-lookup"><span data-stu-id="9f032-106">Returns the *n*<sup>th</sup> control point in the patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f032-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9f032-107">Syntax</span></span>

``` syntax
T Operator[](
  in uint n
);
```

## <a name="parameters"></a><span data-ttu-id="9f032-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9f032-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f032-109">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9f032-109">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f032-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="9f032-110">Type: **uint**</span></span>

<span data-ttu-id="9f032-111">Indice di input.</span><span class="sxs-lookup"><span data-stu-id="9f032-111">The input index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f032-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9f032-112">Return value</span></span>

<span data-ttu-id="9f032-113">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="9f032-113">Type: **T**</span></span>

<span data-ttu-id="9f032-114">Il punto <sup>di controllo</sup> *n*.</span><span class="sxs-lookup"><span data-stu-id="9f032-114">The *n*<sup>th</sup> control point.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f032-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="9f032-115">Remarks</span></span>

<span data-ttu-id="9f032-116">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="9f032-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="9f032-117">Vertice</span><span class="sxs-lookup"><span data-stu-id="9f032-117">Vertex</span></span> | <span data-ttu-id="9f032-118">Hull</span><span class="sxs-lookup"><span data-stu-id="9f032-118">Hull</span></span> | <span data-ttu-id="9f032-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="9f032-119">Domain</span></span> | <span data-ttu-id="9f032-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="9f032-120">Geometry</span></span> | <span data-ttu-id="9f032-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="9f032-121">Pixel</span></span> | <span data-ttu-id="9f032-122">Calcolo</span><span class="sxs-lookup"><span data-stu-id="9f032-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="9f032-123">x</span><span class="sxs-lookup"><span data-stu-id="9f032-123">x</span></span>    | <span data-ttu-id="9f032-124">x</span><span class="sxs-lookup"><span data-stu-id="9f032-124">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="9f032-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9f032-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f032-126">OutputPatch</span><span class="sxs-lookup"><span data-stu-id="9f032-126">OutputPatch</span></span>](sm5-object-outputpatch.md)
</dt> <dt>

[<span data-ttu-id="9f032-127">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="9f032-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




