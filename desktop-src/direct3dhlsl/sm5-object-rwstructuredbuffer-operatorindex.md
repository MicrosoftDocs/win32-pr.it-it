---
title: 'Funzione RWStructuredBuffer:: operator'
description: 'Restituisce una variabile di risorsa. | Funzione RWStructuredBuffer:: operator'
ms.assetid: e821b60e-38db-463f-b0c6-47f2a4c9ccee
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
ms.openlocfilehash: e915d7862f7994d3b438bf3255ee836ede4b3d7d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104530631"
---
# <a name="rwstructuredbufferoperator--function"></a><span data-ttu-id="77975-105">Funzione RWStructuredBuffer:: operator</span><span class="sxs-lookup"><span data-stu-id="77975-105">RWStructuredBuffer::Operator  function</span></span>

<span data-ttu-id="77975-106">Restituisce una variabile di risorsa.</span><span class="sxs-lookup"><span data-stu-id="77975-106">Returns a resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="77975-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="77975-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a><span data-ttu-id="77975-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="77975-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77975-109">*pos* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="77975-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77975-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="77975-110">Type: **uint**</span></span>

<span data-ttu-id="77975-111">Posizione dell'indice.</span><span class="sxs-lookup"><span data-stu-id="77975-111">The index position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77975-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="77975-112">Return value</span></span>

<span data-ttu-id="77975-113">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="77975-113">Type: **R**</span></span>

<span data-ttu-id="77975-114">Variabile di risorsa.</span><span class="sxs-lookup"><span data-stu-id="77975-114">A resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="77975-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="77975-115">Remarks</span></span>

<span data-ttu-id="77975-116">Una risorsa strutturata può essere ulteriormente indicizzata in base ai nomi dei componenti delle strutture.</span><span class="sxs-lookup"><span data-stu-id="77975-116">A structured resource can be further indexed based on the component names of the structures.</span></span>

<span data-ttu-id="77975-117">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="77975-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="77975-118">Vertice</span><span class="sxs-lookup"><span data-stu-id="77975-118">Vertex</span></span> | <span data-ttu-id="77975-119">Hull</span><span class="sxs-lookup"><span data-stu-id="77975-119">Hull</span></span> | <span data-ttu-id="77975-120">Dominio</span><span class="sxs-lookup"><span data-stu-id="77975-120">Domain</span></span> | <span data-ttu-id="77975-121">Geometria</span><span class="sxs-lookup"><span data-stu-id="77975-121">Geometry</span></span> | <span data-ttu-id="77975-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="77975-122">Pixel</span></span> | <span data-ttu-id="77975-123">Calcolo</span><span class="sxs-lookup"><span data-stu-id="77975-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="77975-124">x</span><span class="sxs-lookup"><span data-stu-id="77975-124">x</span></span>     | <span data-ttu-id="77975-125">x</span><span class="sxs-lookup"><span data-stu-id="77975-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="77975-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="77975-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77975-127">RWStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="77975-127">RWStructuredBuffer</span></span>](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="77975-128">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="77975-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




