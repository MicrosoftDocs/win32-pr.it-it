---
title: 'Funzione RWStructuredBuffer:: Load (int, uint)'
description: "Legge i dati del buffer e restituisce lo stato dell'operazione. | Funzione RWStructuredBuffer:: Load (int, uint)"
ms.assetid: 19FAA031-F31E-4B73-BC69-489CDF0CF184
keywords:
- Funzione Load HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 74a153d4b56ec16b80dec180287005666747d259
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981250"
---
# <a name="rwstructuredbufferloadintuint-function"></a><span data-ttu-id="0ac92-105">Funzione RWStructuredBuffer:: Load (int, uint)</span><span class="sxs-lookup"><span data-stu-id="0ac92-105">RWStructuredBuffer::Load(int,uint) function</span></span>

<span data-ttu-id="0ac92-106">Legge i dati del buffer e restituisce lo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="0ac92-106">Reads buffer data and returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ac92-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0ac92-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="0ac92-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0ac92-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ac92-109">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0ac92-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ac92-110">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="0ac92-110">Type: **int**</span></span>

<span data-ttu-id="0ac92-111">Posizione del buffer.</span><span class="sxs-lookup"><span data-stu-id="0ac92-111">The location of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="0ac92-112">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="0ac92-112">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ac92-113">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="0ac92-113">Type: **uint**</span></span>

<span data-ttu-id="0ac92-114">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="0ac92-114">The status of the operation.</span></span> <span data-ttu-id="0ac92-115">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="0ac92-115">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="0ac92-116">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="0ac92-116">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="0ac92-117">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="0ac92-117">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ac92-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0ac92-118">Return value</span></span>

<span data-ttu-id="0ac92-119">Digitare:</span><span class="sxs-lookup"><span data-stu-id="0ac92-119">Type:</span></span>

<span data-ttu-id="0ac92-120">Il tipo restituito corrisponde al tipo nella dichiarazione per l'oggetto [**RWStructuredBuffer**](sm5-object-rwstructuredbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="0ac92-120">The return type matches the type in the declaration for the [**RWStructuredBuffer**](sm5-object-rwstructuredbuffer.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ac92-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="0ac92-121">Remarks</span></span>

<span data-ttu-id="0ac92-122">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="0ac92-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="0ac92-123">Vertice</span><span class="sxs-lookup"><span data-stu-id="0ac92-123">Vertex</span></span> | <span data-ttu-id="0ac92-124">Hull</span><span class="sxs-lookup"><span data-stu-id="0ac92-124">Hull</span></span> | <span data-ttu-id="0ac92-125">Dominio</span><span class="sxs-lookup"><span data-stu-id="0ac92-125">Domain</span></span> | <span data-ttu-id="0ac92-126">Geometria</span><span class="sxs-lookup"><span data-stu-id="0ac92-126">Geometry</span></span> | <span data-ttu-id="0ac92-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="0ac92-127">Pixel</span></span> | <span data-ttu-id="0ac92-128">Calcolo</span><span class="sxs-lookup"><span data-stu-id="0ac92-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="0ac92-129">x</span><span class="sxs-lookup"><span data-stu-id="0ac92-129">x</span></span>      | <span data-ttu-id="0ac92-130">x</span><span class="sxs-lookup"><span data-stu-id="0ac92-130">x</span></span>    | <span data-ttu-id="0ac92-131">x</span><span class="sxs-lookup"><span data-stu-id="0ac92-131">x</span></span>      | <span data-ttu-id="0ac92-132">x</span><span class="sxs-lookup"><span data-stu-id="0ac92-132">x</span></span>        | <span data-ttu-id="0ac92-133">x</span><span class="sxs-lookup"><span data-stu-id="0ac92-133">x</span></span>     | <span data-ttu-id="0ac92-134">x</span><span class="sxs-lookup"><span data-stu-id="0ac92-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="0ac92-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0ac92-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ac92-136">Metodi Load</span><span class="sxs-lookup"><span data-stu-id="0ac92-136">Load methods</span></span>](rwstructuredbuffer-load.md)
</dt> </dl>

 

 
