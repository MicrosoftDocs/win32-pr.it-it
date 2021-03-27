---
title: 'Funzione AppendStructuredBuffer:: Append'
description: Aggiunge un valore alla fine del buffer.
ms.assetid: 667bc6dc-c0d0-419a-9227-99ce30b9cc73
keywords:
- Funzione Append HLSL
topic_type:
- apiref
api_name:
- Append
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 79db73558cb243437560cc77ed66b64f2807fe13
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/06/2019
ms.locfileid: "103956033"
---
# <a name="append-function"></a><span data-ttu-id="56f3b-104">Append (funzione)</span><span class="sxs-lookup"><span data-stu-id="56f3b-104">Append function</span></span>

<span data-ttu-id="56f3b-105">Aggiunge un valore alla fine del buffer.</span><span class="sxs-lookup"><span data-stu-id="56f3b-105">Appends a value to the end of the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="56f3b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="56f3b-106">Syntax</span></span>

``` syntax
void Append(
  in T value
);
```

## <a name="parameters"></a><span data-ttu-id="56f3b-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="56f3b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56f3b-108">*valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="56f3b-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56f3b-109">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="56f3b-109">Type: **T**</span></span>

<span data-ttu-id="56f3b-110">Valore di input.</span><span class="sxs-lookup"><span data-stu-id="56f3b-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56f3b-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="56f3b-111">Return value</span></span>

<span data-ttu-id="56f3b-112">nessuno</span><span class="sxs-lookup"><span data-stu-id="56f3b-112">None</span></span>

## <a name="remarks"></a><span data-ttu-id="56f3b-113">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="56f3b-113">Remarks</span></span>

<span data-ttu-id="56f3b-114">T può essere qualsiasi tipo di dati, incluse le strutture.</span><span class="sxs-lookup"><span data-stu-id="56f3b-114">T can be any data type including structures.</span></span>

<span data-ttu-id="56f3b-115">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="56f3b-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="56f3b-116">Vertice</span><span class="sxs-lookup"><span data-stu-id="56f3b-116">Vertex</span></span> | <span data-ttu-id="56f3b-117">Hull</span><span class="sxs-lookup"><span data-stu-id="56f3b-117">Hull</span></span> | <span data-ttu-id="56f3b-118">Dominio</span><span class="sxs-lookup"><span data-stu-id="56f3b-118">Domain</span></span> | <span data-ttu-id="56f3b-119">Geometria</span><span class="sxs-lookup"><span data-stu-id="56f3b-119">Geometry</span></span> | <span data-ttu-id="56f3b-120">Pixel</span><span class="sxs-lookup"><span data-stu-id="56f3b-120">Pixel</span></span> | <span data-ttu-id="56f3b-121">Calcolo</span><span class="sxs-lookup"><span data-stu-id="56f3b-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="56f3b-122">x</span><span class="sxs-lookup"><span data-stu-id="56f3b-122">x</span></span>      | <span data-ttu-id="56f3b-123">x</span><span class="sxs-lookup"><span data-stu-id="56f3b-123">x</span></span>    | <span data-ttu-id="56f3b-124">x</span><span class="sxs-lookup"><span data-stu-id="56f3b-124">x</span></span>      | <span data-ttu-id="56f3b-125">x</span><span class="sxs-lookup"><span data-stu-id="56f3b-125">x</span></span>        | <span data-ttu-id="56f3b-126">x</span><span class="sxs-lookup"><span data-stu-id="56f3b-126">x</span></span>     | <span data-ttu-id="56f3b-127">x</span><span class="sxs-lookup"><span data-stu-id="56f3b-127">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="56f3b-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="56f3b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56f3b-129">AppendStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="56f3b-129">AppendStructuredBuffer</span></span>](sm5-object-appendstructuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="56f3b-130">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="56f3b-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




