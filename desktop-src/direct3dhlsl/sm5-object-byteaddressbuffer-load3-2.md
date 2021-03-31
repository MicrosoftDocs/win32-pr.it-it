---
title: 'Funzione ByteAddressBuffer:: Load3 (uint, uint)'
description: Ottiene tre valori e lo stato dell'operazione.
ms.assetid: 6AD8E957-F646-4749-A9B4-5C0C936D90E3
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
ms.openlocfilehash: 1bf3ffda082b8d2ae9cf22db59c1c38682563136
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337534"
---
# <a name="load3uint-uint-function"></a><span data-ttu-id="3ced5-104">Funzione Load3 (uint, uint)</span><span class="sxs-lookup"><span data-stu-id="3ced5-104">Load3(uint, uint) function</span></span>

<span data-ttu-id="3ced5-105">Ottiene tre valori e lo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="3ced5-105">Gets three values and the status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ced5-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3ced5-106">Syntax</span></span>

``` syntax
uint3 Load3(
  in  uint Location,
  out uint Status
);
```

## <a name="parameters"></a><span data-ttu-id="3ced5-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="3ced5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ced5-108">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3ced5-108">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ced5-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="3ced5-109">Type: **uint**</span></span>

<span data-ttu-id="3ced5-110">Indirizzo di input in byte, che deve essere un multiplo di 4.</span><span class="sxs-lookup"><span data-stu-id="3ced5-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="3ced5-111">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="3ced5-111">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ced5-112">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="3ced5-112">Type: **uint**</span></span>

<span data-ttu-id="3ced5-113">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="3ced5-113">The status of the operation.</span></span> <span data-ttu-id="3ced5-114">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="3ced5-114">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="3ced5-115">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="3ced5-115">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="3ced5-116">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="3ced5-116">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ced5-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3ced5-117">Return value</span></span>

<span data-ttu-id="3ced5-118">Tipo: **uint3**</span><span class="sxs-lookup"><span data-stu-id="3ced5-118">Type: **uint3**</span></span>

<span data-ttu-id="3ced5-119">Tre valori.</span><span class="sxs-lookup"><span data-stu-id="3ced5-119">Three values.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ced5-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="3ced5-120">Remarks</span></span>

<span data-ttu-id="3ced5-121">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="3ced5-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="3ced5-122">Vertice</span><span class="sxs-lookup"><span data-stu-id="3ced5-122">Vertex</span></span> | <span data-ttu-id="3ced5-123">Hull</span><span class="sxs-lookup"><span data-stu-id="3ced5-123">Hull</span></span> | <span data-ttu-id="3ced5-124">Dominio</span><span class="sxs-lookup"><span data-stu-id="3ced5-124">Domain</span></span> | <span data-ttu-id="3ced5-125">Geometria</span><span class="sxs-lookup"><span data-stu-id="3ced5-125">Geometry</span></span> | <span data-ttu-id="3ced5-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="3ced5-126">Pixel</span></span> | <span data-ttu-id="3ced5-127">Calcolo</span><span class="sxs-lookup"><span data-stu-id="3ced5-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="3ced5-128">x</span><span class="sxs-lookup"><span data-stu-id="3ced5-128">x</span></span>      | <span data-ttu-id="3ced5-129">x</span><span class="sxs-lookup"><span data-stu-id="3ced5-129">x</span></span>    | <span data-ttu-id="3ced5-130">x</span><span class="sxs-lookup"><span data-stu-id="3ced5-130">x</span></span>      | <span data-ttu-id="3ced5-131">x</span><span class="sxs-lookup"><span data-stu-id="3ced5-131">x</span></span>        | <span data-ttu-id="3ced5-132">x</span><span class="sxs-lookup"><span data-stu-id="3ced5-132">x</span></span>     | <span data-ttu-id="3ced5-133">x</span><span class="sxs-lookup"><span data-stu-id="3ced5-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="3ced5-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3ced5-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ced5-135">Metodi Load3</span><span class="sxs-lookup"><span data-stu-id="3ced5-135">Load3 methods</span></span>](byteaddressbuffer-load3.md)
</dt> <dt>

[<span data-ttu-id="3ced5-136">**ByteAddressBuffer**</span><span class="sxs-lookup"><span data-stu-id="3ced5-136">**ByteAddressBuffer**</span></span>](sm5-object-byteaddressbuffer.md)
</dt> </dl>

 

 