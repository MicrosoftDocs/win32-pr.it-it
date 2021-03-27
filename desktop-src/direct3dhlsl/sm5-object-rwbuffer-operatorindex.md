---
title: 'Funzione RWBuffer:: operator'
description: 'Restituisce una variabile di risorsa. | Funzione RWBuffer:: operator'
ms.assetid: 59e5e4ec-ff0d-43aa-805a-04b79f5ab57f
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
ms.openlocfilehash: 40336c8ad6ee9e8008b82c172f1a5b863e967c0d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995309"
---
# <a name="rwbufferoperator--function"></a><span data-ttu-id="d7cbd-105">Funzione RWBuffer:: operator</span><span class="sxs-lookup"><span data-stu-id="d7cbd-105">RWBuffer::Operator  function</span></span>

<span data-ttu-id="d7cbd-106">Restituisce una variabile di risorsa.</span><span class="sxs-lookup"><span data-stu-id="d7cbd-106">Returns a resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7cbd-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d7cbd-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a><span data-ttu-id="d7cbd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d7cbd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7cbd-109">*pos* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d7cbd-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7cbd-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="d7cbd-110">Type: **uint**</span></span>

<span data-ttu-id="d7cbd-111">Posizione dell'indice.</span><span class="sxs-lookup"><span data-stu-id="d7cbd-111">The index position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7cbd-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d7cbd-112">Return value</span></span>

<span data-ttu-id="d7cbd-113">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="d7cbd-113">Type: **R**</span></span>

<span data-ttu-id="d7cbd-114">Variabile di risorsa.</span><span class="sxs-lookup"><span data-stu-id="d7cbd-114">A resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7cbd-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="d7cbd-115">Remarks</span></span>

<span data-ttu-id="d7cbd-116">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="d7cbd-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="d7cbd-117">Vertice</span><span class="sxs-lookup"><span data-stu-id="d7cbd-117">Vertex</span></span> | <span data-ttu-id="d7cbd-118">Hull</span><span class="sxs-lookup"><span data-stu-id="d7cbd-118">Hull</span></span> | <span data-ttu-id="d7cbd-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="d7cbd-119">Domain</span></span> | <span data-ttu-id="d7cbd-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="d7cbd-120">Geometry</span></span> | <span data-ttu-id="d7cbd-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="d7cbd-121">Pixel</span></span> | <span data-ttu-id="d7cbd-122">Calcolo</span><span class="sxs-lookup"><span data-stu-id="d7cbd-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="d7cbd-123">x</span><span class="sxs-lookup"><span data-stu-id="d7cbd-123">x</span></span>      | <span data-ttu-id="d7cbd-124">x</span><span class="sxs-lookup"><span data-stu-id="d7cbd-124">x</span></span>    | <span data-ttu-id="d7cbd-125">x</span><span class="sxs-lookup"><span data-stu-id="d7cbd-125">x</span></span>      | <span data-ttu-id="d7cbd-126">x</span><span class="sxs-lookup"><span data-stu-id="d7cbd-126">x</span></span>        | <span data-ttu-id="d7cbd-127">x</span><span class="sxs-lookup"><span data-stu-id="d7cbd-127">x</span></span>     | <span data-ttu-id="d7cbd-128">x</span><span class="sxs-lookup"><span data-stu-id="d7cbd-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="d7cbd-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d7cbd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7cbd-130">RWBuffer</span><span class="sxs-lookup"><span data-stu-id="d7cbd-130">RWBuffer</span></span>](sm5-object-rwbuffer.md)
</dt> <dt>

[<span data-ttu-id="d7cbd-131">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="d7cbd-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




