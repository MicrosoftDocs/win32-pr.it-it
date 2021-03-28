---
title: 'Funzione RWByteAddressBuffer:: Store'
description: Imposta un valore.
ms.assetid: edfda955-602c-44f4-adc3-77b61c9dcd05
keywords:
- Funzione di archivio HLSL
topic_type:
- apiref
api_name:
- Store
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9e161e4fb64d09e41c6529954e63b2ace55207e9
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/06/2019
ms.locfileid: "104976226"
---
# <a name="store-function"></a><span data-ttu-id="9cacd-104">Funzione Store</span><span class="sxs-lookup"><span data-stu-id="9cacd-104">Store function</span></span>

<span data-ttu-id="9cacd-105">Imposta un valore.</span><span class="sxs-lookup"><span data-stu-id="9cacd-105">Sets one value.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cacd-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9cacd-106">Syntax</span></span>

``` syntax
void Store(
  in uint address,
  in uint value
);
```

## <a name="parameters"></a><span data-ttu-id="9cacd-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="9cacd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cacd-108">*Indirizzo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9cacd-108">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9cacd-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="9cacd-109">Type: **uint**</span></span>

<span data-ttu-id="9cacd-110">Indirizzo di input in byte, che deve essere un multiplo di 4.</span><span class="sxs-lookup"><span data-stu-id="9cacd-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="9cacd-111">*valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="9cacd-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9cacd-112">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="9cacd-112">Type: **uint**</span></span>

<span data-ttu-id="9cacd-113">Un valore di input.</span><span class="sxs-lookup"><span data-stu-id="9cacd-113">One input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cacd-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9cacd-114">Return value</span></span>

<span data-ttu-id="9cacd-115">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="9cacd-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9cacd-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="9cacd-116">Remarks</span></span>

<span data-ttu-id="9cacd-117">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="9cacd-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="9cacd-118">Vertice</span><span class="sxs-lookup"><span data-stu-id="9cacd-118">Vertex</span></span> | <span data-ttu-id="9cacd-119">Hull</span><span class="sxs-lookup"><span data-stu-id="9cacd-119">Hull</span></span> | <span data-ttu-id="9cacd-120">Dominio</span><span class="sxs-lookup"><span data-stu-id="9cacd-120">Domain</span></span> | <span data-ttu-id="9cacd-121">Geometria</span><span class="sxs-lookup"><span data-stu-id="9cacd-121">Geometry</span></span> | <span data-ttu-id="9cacd-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="9cacd-122">Pixel</span></span> | <span data-ttu-id="9cacd-123">Calcolo</span><span class="sxs-lookup"><span data-stu-id="9cacd-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="9cacd-124">x</span><span class="sxs-lookup"><span data-stu-id="9cacd-124">x</span></span>     | <span data-ttu-id="9cacd-125">x</span><span class="sxs-lookup"><span data-stu-id="9cacd-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="9cacd-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9cacd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cacd-127">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="9cacd-127">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="9cacd-128">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="9cacd-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




