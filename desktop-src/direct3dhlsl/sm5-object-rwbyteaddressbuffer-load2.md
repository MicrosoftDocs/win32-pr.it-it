---
title: 'Funzione RWByteAddressBuffer:: load2 (uint)'
description: 'Ottiene due valori. | Funzione RWByteAddressBuffer:: load2 (uint)'
ms.assetid: a00396cb-e68d-479e-ab3f-4c52f2cfc3bc
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
ms.openlocfilehash: 7595477448deb087b94664100710690a6f386a94
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104982028"
---
# <a name="rwbyteaddressbufferload2uint-function"></a><span data-ttu-id="93e17-105">Funzione RWByteAddressBuffer:: load2 (uint)</span><span class="sxs-lookup"><span data-stu-id="93e17-105">RWByteAddressBuffer::Load2(uint) function</span></span>

<span data-ttu-id="93e17-106">Ottiene due valori.</span><span class="sxs-lookup"><span data-stu-id="93e17-106">Gets two values.</span></span>

## <a name="syntax"></a><span data-ttu-id="93e17-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="93e17-107">Syntax</span></span>

``` syntax
uint2 Load2(
  in uint address
);
```

## <a name="parameters"></a><span data-ttu-id="93e17-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="93e17-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93e17-109">*Indirizzo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="93e17-109">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93e17-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="93e17-110">Type: **uint**</span></span>

<span data-ttu-id="93e17-111">Indirizzo di input in byte, che deve essere un multiplo di 4.</span><span class="sxs-lookup"><span data-stu-id="93e17-111">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93e17-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="93e17-112">Return value</span></span>

<span data-ttu-id="93e17-113">Tipo: **uint2**</span><span class="sxs-lookup"><span data-stu-id="93e17-113">Type: **uint2**</span></span>

<span data-ttu-id="93e17-114">Due valori.</span><span class="sxs-lookup"><span data-stu-id="93e17-114">Two values.</span></span>

## <a name="remarks"></a><span data-ttu-id="93e17-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="93e17-115">Remarks</span></span>

<span data-ttu-id="93e17-116">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="93e17-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="93e17-117">Vertice</span><span class="sxs-lookup"><span data-stu-id="93e17-117">Vertex</span></span> | <span data-ttu-id="93e17-118">Hull</span><span class="sxs-lookup"><span data-stu-id="93e17-118">Hull</span></span> | <span data-ttu-id="93e17-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="93e17-119">Domain</span></span> | <span data-ttu-id="93e17-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="93e17-120">Geometry</span></span> | <span data-ttu-id="93e17-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="93e17-121">Pixel</span></span> | <span data-ttu-id="93e17-122">Calcolo</span><span class="sxs-lookup"><span data-stu-id="93e17-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="93e17-123">x</span><span class="sxs-lookup"><span data-stu-id="93e17-123">x</span></span>     | <span data-ttu-id="93e17-124">x</span><span class="sxs-lookup"><span data-stu-id="93e17-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="93e17-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="93e17-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93e17-126">Metodi load2</span><span class="sxs-lookup"><span data-stu-id="93e17-126">Load2 methods</span></span>](rwbyteaddressbuffer-load2.md)
</dt> <dt>

[<span data-ttu-id="93e17-127">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="93e17-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




