---
title: 'Funzione RWByteAddressBuffer:: Load3 (uint)'
description: 'Ottiene tre valori. | Funzione RWByteAddressBuffer:: Load3 (uint)'
ms.assetid: cf8c4c5d-4748-43d7-896e-33ed07c94b9e
keywords:
- Funzione Load3 HLSL
topic_type:
- apiref
api_name:
- Load3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d6658b4929f09aa7296a284de1fdbf39c7c4f038
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104982058"
---
# <a name="rwbyteaddressbufferload3uint-function"></a><span data-ttu-id="cb3e3-105">Funzione RWByteAddressBuffer:: Load3 (uint)</span><span class="sxs-lookup"><span data-stu-id="cb3e3-105">RWByteAddressBuffer::Load3(uint) function</span></span>

<span data-ttu-id="cb3e3-106">Ottiene tre valori.</span><span class="sxs-lookup"><span data-stu-id="cb3e3-106">Gets three values.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb3e3-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cb3e3-107">Syntax</span></span>

``` syntax
uint3 Load3(
  in uint address
);
```

## <a name="parameters"></a><span data-ttu-id="cb3e3-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="cb3e3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb3e3-109">*Indirizzo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cb3e3-109">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb3e3-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="cb3e3-110">Type: **uint**</span></span>

<span data-ttu-id="cb3e3-111">Indirizzo di input in byte, che deve essere un multiplo di 4.</span><span class="sxs-lookup"><span data-stu-id="cb3e3-111">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb3e3-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cb3e3-112">Return value</span></span>

<span data-ttu-id="cb3e3-113">Tipo: **uint3**</span><span class="sxs-lookup"><span data-stu-id="cb3e3-113">Type: **uint3**</span></span>

<span data-ttu-id="cb3e3-114">Tre valori.</span><span class="sxs-lookup"><span data-stu-id="cb3e3-114">Three values.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb3e3-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="cb3e3-115">Remarks</span></span>

<span data-ttu-id="cb3e3-116">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb3e3-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="cb3e3-117">Vertice</span><span class="sxs-lookup"><span data-stu-id="cb3e3-117">Vertex</span></span> | <span data-ttu-id="cb3e3-118">Hull</span><span class="sxs-lookup"><span data-stu-id="cb3e3-118">Hull</span></span> | <span data-ttu-id="cb3e3-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="cb3e3-119">Domain</span></span> | <span data-ttu-id="cb3e3-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="cb3e3-120">Geometry</span></span> | <span data-ttu-id="cb3e3-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="cb3e3-121">Pixel</span></span> | <span data-ttu-id="cb3e3-122">Calcolo</span><span class="sxs-lookup"><span data-stu-id="cb3e3-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="cb3e3-123">x</span><span class="sxs-lookup"><span data-stu-id="cb3e3-123">x</span></span>     | <span data-ttu-id="cb3e3-124">x</span><span class="sxs-lookup"><span data-stu-id="cb3e3-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="cb3e3-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cb3e3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb3e3-126">Metodi Load3</span><span class="sxs-lookup"><span data-stu-id="cb3e3-126">Load3 methods</span></span>](rwbyteaddressbuffer-load3.md)
</dt> <dt>

[<span data-ttu-id="cb3e3-127">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="cb3e3-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




