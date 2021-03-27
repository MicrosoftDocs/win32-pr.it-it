---
title: 'Funzione RWByteAddressBuffer:: Store4'
description: Imposta quattro valori.
ms.assetid: 261dd270-79a7-4566-9fbd-52bd8dc3e1bf
keywords:
- Funzione Store4 HLSL
topic_type:
- apiref
api_name:
- Store4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 219cd04e4f68ad6f0d16d964e6685c558fed98b1
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/06/2019
ms.locfileid: "104398102"
---
# <a name="store4-function"></a><span data-ttu-id="c77e3-104">Store4 (funzione)</span><span class="sxs-lookup"><span data-stu-id="c77e3-104">Store4 function</span></span>

<span data-ttu-id="c77e3-105">Imposta quattro valori.</span><span class="sxs-lookup"><span data-stu-id="c77e3-105">Sets four values.</span></span>

## <a name="syntax"></a><span data-ttu-id="c77e3-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c77e3-106">Syntax</span></span>

``` syntax
void Store4(
  in uint address,
  in uint4 values
);
```

## <a name="parameters"></a><span data-ttu-id="c77e3-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="c77e3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c77e3-108">*Indirizzo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c77e3-108">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c77e3-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="c77e3-109">Type: **uint**</span></span>

<span data-ttu-id="c77e3-110">Indirizzo di input in byte, che deve essere un multiplo di 4.</span><span class="sxs-lookup"><span data-stu-id="c77e3-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="c77e3-111">*valori* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="c77e3-111">*values* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c77e3-112">Tipo: **uint4**</span><span class="sxs-lookup"><span data-stu-id="c77e3-112">Type: **uint4**</span></span>

<span data-ttu-id="c77e3-113">Quattro valori di input.</span><span class="sxs-lookup"><span data-stu-id="c77e3-113">Four input values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c77e3-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c77e3-114">Return value</span></span>

<span data-ttu-id="c77e3-115">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="c77e3-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c77e3-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="c77e3-116">Remarks</span></span>

<span data-ttu-id="c77e3-117">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="c77e3-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="c77e3-118">Vertice</span><span class="sxs-lookup"><span data-stu-id="c77e3-118">Vertex</span></span> | <span data-ttu-id="c77e3-119">Hull</span><span class="sxs-lookup"><span data-stu-id="c77e3-119">Hull</span></span> | <span data-ttu-id="c77e3-120">Dominio</span><span class="sxs-lookup"><span data-stu-id="c77e3-120">Domain</span></span> | <span data-ttu-id="c77e3-121">Geometria</span><span class="sxs-lookup"><span data-stu-id="c77e3-121">Geometry</span></span> | <span data-ttu-id="c77e3-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="c77e3-122">Pixel</span></span> | <span data-ttu-id="c77e3-123">Calcolo</span><span class="sxs-lookup"><span data-stu-id="c77e3-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="c77e3-124">x</span><span class="sxs-lookup"><span data-stu-id="c77e3-124">x</span></span>     | <span data-ttu-id="c77e3-125">x</span><span class="sxs-lookup"><span data-stu-id="c77e3-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="c77e3-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c77e3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c77e3-127">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="c77e3-127">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="c77e3-128">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="c77e3-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




