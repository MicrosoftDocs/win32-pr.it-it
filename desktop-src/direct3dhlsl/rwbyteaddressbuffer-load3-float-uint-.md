---
title: 'Funzione RWByteAddressBuffer:: Load3 (uint, uint)'
description: Ottiene tre valori e restituisce lo stato dell'operazione.
ms.assetid: EBCCDAF3-69B9-4132-85EC-82759F292811
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
ms.openlocfilehash: 8451abe17c3ff74a1906828b3570dc6ee98782f1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338591"
---
# <a name="load3uintuint-function"></a><span data-ttu-id="76090-104">Funzione Load3 (uint, uint)</span><span class="sxs-lookup"><span data-stu-id="76090-104">Load3(uint,uint) function</span></span>

<span data-ttu-id="76090-105">Ottiene tre valori e restituisce lo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="76090-105">Gets three values and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="76090-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="76090-106">Syntax</span></span>


``` syntax
uint3 Load3(
  in  uint Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="76090-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="76090-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76090-108">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76090-108">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76090-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="76090-109">Type: **uint**</span></span>

<span data-ttu-id="76090-110">Posizione del buffer.</span><span class="sxs-lookup"><span data-stu-id="76090-110">The location of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="76090-111">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="76090-111">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="76090-112">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="76090-112">Type: **uint**</span></span>

<span data-ttu-id="76090-113">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="76090-113">The status of the operation.</span></span> <span data-ttu-id="76090-114">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="76090-114">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="76090-115">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="76090-115">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="76090-116">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="76090-116">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76090-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="76090-117">Return value</span></span>

<span data-ttu-id="76090-118">Tipo: **uint3**</span><span class="sxs-lookup"><span data-stu-id="76090-118">Type: **uint3**</span></span>

<span data-ttu-id="76090-119">Tre valori.</span><span class="sxs-lookup"><span data-stu-id="76090-119">Three values.</span></span>

## <a name="remarks"></a><span data-ttu-id="76090-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="76090-120">Remarks</span></span>

<span data-ttu-id="76090-121">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="76090-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="76090-122">Vertice</span><span class="sxs-lookup"><span data-stu-id="76090-122">Vertex</span></span> | <span data-ttu-id="76090-123">Hull</span><span class="sxs-lookup"><span data-stu-id="76090-123">Hull</span></span> | <span data-ttu-id="76090-124">Dominio</span><span class="sxs-lookup"><span data-stu-id="76090-124">Domain</span></span> | <span data-ttu-id="76090-125">Geometria</span><span class="sxs-lookup"><span data-stu-id="76090-125">Geometry</span></span> | <span data-ttu-id="76090-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="76090-126">Pixel</span></span> | <span data-ttu-id="76090-127">Calcolo</span><span class="sxs-lookup"><span data-stu-id="76090-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="76090-128">x</span><span class="sxs-lookup"><span data-stu-id="76090-128">x</span></span>     | <span data-ttu-id="76090-129">x</span><span class="sxs-lookup"><span data-stu-id="76090-129">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="76090-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="76090-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76090-131">Metodi Load3</span><span class="sxs-lookup"><span data-stu-id="76090-131">Load3 methods</span></span>](rwbyteaddressbuffer-load3.md)
</dt> </dl>

 

 