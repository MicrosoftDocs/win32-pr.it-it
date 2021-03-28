---
title: 'Funzione RWByteAddressBuffer:: Store3'
description: Imposta tre valori.
ms.assetid: eaf12b5a-c9c6-413a-9646-3d14e7825460
keywords:
- Funzione Store3 HLSL
topic_type:
- apiref
api_name:
- Store3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fd27684c3adf506e086fb17f789272c6b263ab20
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/06/2019
ms.locfileid: "104335087"
---
# <a name="store3-function"></a><span data-ttu-id="7e632-104">Store3 (funzione)</span><span class="sxs-lookup"><span data-stu-id="7e632-104">Store3 function</span></span>

<span data-ttu-id="7e632-105">Imposta tre valori.</span><span class="sxs-lookup"><span data-stu-id="7e632-105">Sets three values.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e632-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7e632-106">Syntax</span></span>

``` syntax
void Store3(
  in uint address,
  in uint3 values
);
```

## <a name="parameters"></a><span data-ttu-id="7e632-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="7e632-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e632-108">*Indirizzo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7e632-108">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e632-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="7e632-109">Type: **uint**</span></span>

<span data-ttu-id="7e632-110">Indirizzo di input in byte, che deve essere un multiplo di 4.</span><span class="sxs-lookup"><span data-stu-id="7e632-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="7e632-111">*valori* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="7e632-111">*values* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e632-112">Tipo: **uint3**</span><span class="sxs-lookup"><span data-stu-id="7e632-112">Type: **uint3**</span></span>

<span data-ttu-id="7e632-113">Tre valori di input.</span><span class="sxs-lookup"><span data-stu-id="7e632-113">Three input values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e632-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7e632-114">Return value</span></span>

<span data-ttu-id="7e632-115">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="7e632-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e632-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="7e632-116">Remarks</span></span>

<span data-ttu-id="7e632-117">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="7e632-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="7e632-118">Vertice</span><span class="sxs-lookup"><span data-stu-id="7e632-118">Vertex</span></span> | <span data-ttu-id="7e632-119">Hull</span><span class="sxs-lookup"><span data-stu-id="7e632-119">Hull</span></span> | <span data-ttu-id="7e632-120">Dominio</span><span class="sxs-lookup"><span data-stu-id="7e632-120">Domain</span></span> | <span data-ttu-id="7e632-121">Geometria</span><span class="sxs-lookup"><span data-stu-id="7e632-121">Geometry</span></span> | <span data-ttu-id="7e632-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="7e632-122">Pixel</span></span> | <span data-ttu-id="7e632-123">Calcolo</span><span class="sxs-lookup"><span data-stu-id="7e632-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="7e632-124">x</span><span class="sxs-lookup"><span data-stu-id="7e632-124">x</span></span>     | <span data-ttu-id="7e632-125">x</span><span class="sxs-lookup"><span data-stu-id="7e632-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="7e632-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7e632-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e632-127">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="7e632-127">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="7e632-128">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="7e632-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




