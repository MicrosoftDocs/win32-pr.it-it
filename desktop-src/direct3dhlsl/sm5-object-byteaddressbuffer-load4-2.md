---
title: 'Funzione ByteAddressBuffer:: Load4 (uint, uint)'
description: Ottiene quattro valori e lo stato dell'operazione.
ms.assetid: C814F717-9FD4-4BFC-A91B-319477B7F3DE
keywords:
- Funzione Load4 HLSL
topic_type:
- apiref
api_name:
- Load4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ab27ed9002562643ddf4df6b33efe9d8f0454d94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046768"
---
# <a name="load4uint-uint-function"></a><span data-ttu-id="c13eb-104">Funzione Load4 (uint, uint)</span><span class="sxs-lookup"><span data-stu-id="c13eb-104">Load4(uint, uint) function</span></span>

<span data-ttu-id="c13eb-105">Ottiene quattro valori e lo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="c13eb-105">Gets four values and the status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="c13eb-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c13eb-106">Syntax</span></span>

``` syntax
uint4 Load4(
  in  uint Location,
  out uint Status
);
```

## <a name="parameters"></a><span data-ttu-id="c13eb-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="c13eb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c13eb-108">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c13eb-108">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c13eb-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="c13eb-109">Type: **uint**</span></span>

<span data-ttu-id="c13eb-110">Indirizzo di input in byte, che deve essere un multiplo di 4.</span><span class="sxs-lookup"><span data-stu-id="c13eb-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="c13eb-111">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="c13eb-111">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c13eb-112">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="c13eb-112">Type: **uint**</span></span>

<span data-ttu-id="c13eb-113">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="c13eb-113">The status of the operation.</span></span> <span data-ttu-id="c13eb-114">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="c13eb-114">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="c13eb-115">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="c13eb-115">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="c13eb-116">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="c13eb-116">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c13eb-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c13eb-117">Return value</span></span>

<span data-ttu-id="c13eb-118">Tipo: **uint4**</span><span class="sxs-lookup"><span data-stu-id="c13eb-118">Type: **uint4**</span></span>

<span data-ttu-id="c13eb-119">Quattro valori.</span><span class="sxs-lookup"><span data-stu-id="c13eb-119">Four values.</span></span>

## <a name="remarks"></a><span data-ttu-id="c13eb-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="c13eb-120">Remarks</span></span>

<span data-ttu-id="c13eb-121">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="c13eb-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="c13eb-122">Vertice</span><span class="sxs-lookup"><span data-stu-id="c13eb-122">Vertex</span></span> | <span data-ttu-id="c13eb-123">Hull</span><span class="sxs-lookup"><span data-stu-id="c13eb-123">Hull</span></span> | <span data-ttu-id="c13eb-124">Dominio</span><span class="sxs-lookup"><span data-stu-id="c13eb-124">Domain</span></span> | <span data-ttu-id="c13eb-125">Geometria</span><span class="sxs-lookup"><span data-stu-id="c13eb-125">Geometry</span></span> | <span data-ttu-id="c13eb-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="c13eb-126">Pixel</span></span> | <span data-ttu-id="c13eb-127">Calcolo</span><span class="sxs-lookup"><span data-stu-id="c13eb-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="c13eb-128">x</span><span class="sxs-lookup"><span data-stu-id="c13eb-128">x</span></span>      | <span data-ttu-id="c13eb-129">x</span><span class="sxs-lookup"><span data-stu-id="c13eb-129">x</span></span>    | <span data-ttu-id="c13eb-130">x</span><span class="sxs-lookup"><span data-stu-id="c13eb-130">x</span></span>      | <span data-ttu-id="c13eb-131">x</span><span class="sxs-lookup"><span data-stu-id="c13eb-131">x</span></span>        | <span data-ttu-id="c13eb-132">x</span><span class="sxs-lookup"><span data-stu-id="c13eb-132">x</span></span>     | <span data-ttu-id="c13eb-133">x</span><span class="sxs-lookup"><span data-stu-id="c13eb-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="c13eb-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c13eb-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c13eb-135">Metodi Load4</span><span class="sxs-lookup"><span data-stu-id="c13eb-135">Load4 methods</span></span>](byteaddressbuffer-load4.md)
</dt> <dt>

[<span data-ttu-id="c13eb-136">**ByteAddressBuffer**</span><span class="sxs-lookup"><span data-stu-id="c13eb-136">**ByteAddressBuffer**</span></span>](sm5-object-byteaddressbuffer.md)
</dt> </dl>

 

 