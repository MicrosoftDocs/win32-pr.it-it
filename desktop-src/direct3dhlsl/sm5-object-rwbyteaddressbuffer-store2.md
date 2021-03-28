---
title: 'Funzione RWByteAddressBuffer:: Archivio2'
description: Imposta due valori.
ms.assetid: 7b32c84c-9ea2-47ae-a0f3-df6d95249163
keywords:
- Funzione Archivio2 HLSL
topic_type:
- apiref
api_name:
- Store2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 574ad7fd59921767308e980e645bac966be87709
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/06/2019
ms.locfileid: "104045984"
---
# <a name="store2-function"></a><span data-ttu-id="3e36e-104">Archivio2 (funzione)</span><span class="sxs-lookup"><span data-stu-id="3e36e-104">Store2 function</span></span>

<span data-ttu-id="3e36e-105">Imposta due valori.</span><span class="sxs-lookup"><span data-stu-id="3e36e-105">Sets two values.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e36e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3e36e-106">Syntax</span></span>

``` syntax
void Store2(
  in uint address,
  in uint2 values
);
```

## <a name="parameters"></a><span data-ttu-id="3e36e-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="3e36e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e36e-108">*Indirizzo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3e36e-108">*address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e36e-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="3e36e-109">Type: **uint**</span></span>

<span data-ttu-id="3e36e-110">Indirizzo di input in byte, che deve essere un multiplo di 4.</span><span class="sxs-lookup"><span data-stu-id="3e36e-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="3e36e-111">*valori* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="3e36e-111">*values* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e36e-112">Tipo: **uint2**</span><span class="sxs-lookup"><span data-stu-id="3e36e-112">Type: **uint2**</span></span>

<span data-ttu-id="3e36e-113">Due valori di input.</span><span class="sxs-lookup"><span data-stu-id="3e36e-113">Two input values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e36e-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3e36e-114">Return value</span></span>

<span data-ttu-id="3e36e-115">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="3e36e-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e36e-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="3e36e-116">Remarks</span></span>

<span data-ttu-id="3e36e-117">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="3e36e-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="3e36e-118">Vertice</span><span class="sxs-lookup"><span data-stu-id="3e36e-118">Vertex</span></span> | <span data-ttu-id="3e36e-119">Hull</span><span class="sxs-lookup"><span data-stu-id="3e36e-119">Hull</span></span> | <span data-ttu-id="3e36e-120">Dominio</span><span class="sxs-lookup"><span data-stu-id="3e36e-120">Domain</span></span> | <span data-ttu-id="3e36e-121">Geometria</span><span class="sxs-lookup"><span data-stu-id="3e36e-121">Geometry</span></span> | <span data-ttu-id="3e36e-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="3e36e-122">Pixel</span></span> | <span data-ttu-id="3e36e-123">Calcolo</span><span class="sxs-lookup"><span data-stu-id="3e36e-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="3e36e-124">x</span><span class="sxs-lookup"><span data-stu-id="3e36e-124">x</span></span>     | <span data-ttu-id="3e36e-125">x</span><span class="sxs-lookup"><span data-stu-id="3e36e-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="3e36e-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3e36e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e36e-127">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="3e36e-127">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="3e36e-128">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="3e36e-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




