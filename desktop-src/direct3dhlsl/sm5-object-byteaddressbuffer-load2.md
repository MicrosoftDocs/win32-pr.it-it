---
title: 'Funzione ByteAddressBuffer:: load2 (uint)'
description: 'Ottiene due valori. | Funzione ByteAddressBuffer:: load2 (uint)'
ms.assetid: 696ce310-4d65-4382-97ec-046160197c67
keywords:
- Funzione load2 HLSL
topic_type:
- apiref
api_name:
- Load2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 78204fc3d41daf07a54974fbf103685e718ab79d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761615"
---
# <a name="byteaddressbufferload2uint-function"></a><span data-ttu-id="46467-105">Funzione ByteAddressBuffer:: load2 (uint)</span><span class="sxs-lookup"><span data-stu-id="46467-105">ByteAddressBuffer::Load2(uint) function</span></span>

<span data-ttu-id="46467-106">Ottiene due valori.</span><span class="sxs-lookup"><span data-stu-id="46467-106">Gets two values.</span></span>

## <a name="syntax"></a><span data-ttu-id="46467-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="46467-107">Syntax</span></span>

``` syntax
uint2 Load2(
  in uint address
);
```

## <a name="parameters"></a><span data-ttu-id="46467-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="46467-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46467-109">*Indirizzo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46467-109">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46467-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="46467-110">Type: **uint**</span></span>

<span data-ttu-id="46467-111">Indirizzo di input in byte, che deve essere un multiplo di 4.</span><span class="sxs-lookup"><span data-stu-id="46467-111">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46467-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="46467-112">Return value</span></span>

<span data-ttu-id="46467-113">Tipo: **uint2**</span><span class="sxs-lookup"><span data-stu-id="46467-113">Type: **uint2**</span></span>

<span data-ttu-id="46467-114">Due valori.</span><span class="sxs-lookup"><span data-stu-id="46467-114">Two values.</span></span>

## <a name="remarks"></a><span data-ttu-id="46467-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="46467-115">Remarks</span></span>

<span data-ttu-id="46467-116">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="46467-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="46467-117">Vertice</span><span class="sxs-lookup"><span data-stu-id="46467-117">Vertex</span></span> | <span data-ttu-id="46467-118">Hull</span><span class="sxs-lookup"><span data-stu-id="46467-118">Hull</span></span> | <span data-ttu-id="46467-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="46467-119">Domain</span></span> | <span data-ttu-id="46467-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="46467-120">Geometry</span></span> | <span data-ttu-id="46467-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="46467-121">Pixel</span></span> | <span data-ttu-id="46467-122">Calcolo</span><span class="sxs-lookup"><span data-stu-id="46467-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="46467-123">x</span><span class="sxs-lookup"><span data-stu-id="46467-123">x</span></span>      | <span data-ttu-id="46467-124">x</span><span class="sxs-lookup"><span data-stu-id="46467-124">x</span></span>    | <span data-ttu-id="46467-125">x</span><span class="sxs-lookup"><span data-stu-id="46467-125">x</span></span>      | <span data-ttu-id="46467-126">x</span><span class="sxs-lookup"><span data-stu-id="46467-126">x</span></span>        | <span data-ttu-id="46467-127">x</span><span class="sxs-lookup"><span data-stu-id="46467-127">x</span></span>     | <span data-ttu-id="46467-128">x</span><span class="sxs-lookup"><span data-stu-id="46467-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="46467-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="46467-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46467-130">Metodi load2</span><span class="sxs-lookup"><span data-stu-id="46467-130">Load2 methods</span></span>](byteaddressbuffer-load2.md)
</dt> <dt>

[<span data-ttu-id="46467-131">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="46467-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




