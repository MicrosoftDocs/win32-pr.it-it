---
title: 'Funzione RWBuffer:: Load (int, uint)'
description: "Legge i dati del buffer e restituisce lo stato dell'operazione. | Funzione RWBuffer:: Load (int, uint)"
ms.assetid: 90C9ECE8-2068-47C7-B87A-941B2D4F221D
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
ms.openlocfilehash: 81d23d67b0d02ed375e07f310089067d6a7bbd67
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104132218"
---
# <a name="rwbufferloadintuint-function"></a><span data-ttu-id="097ae-105">Funzione RWBuffer:: Load (int, uint)</span><span class="sxs-lookup"><span data-stu-id="097ae-105">RWBuffer::Load(int,uint) function</span></span>

<span data-ttu-id="097ae-106">Legge i dati del buffer e restituisce lo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="097ae-106">Reads buffer data and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="097ae-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="097ae-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="097ae-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="097ae-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="097ae-109">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="097ae-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="097ae-110">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="097ae-110">Type: **int**</span></span>

<span data-ttu-id="097ae-111">Posizione del buffer.</span><span class="sxs-lookup"><span data-stu-id="097ae-111">The location of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="097ae-112">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="097ae-112">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="097ae-113">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="097ae-113">Type: **uint**</span></span>

<span data-ttu-id="097ae-114">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="097ae-114">The status of the operation.</span></span> <span data-ttu-id="097ae-115">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="097ae-115">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="097ae-116">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="097ae-116">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="097ae-117">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="097ae-117">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="097ae-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="097ae-118">Return value</span></span>

<span data-ttu-id="097ae-119">Digitare:</span><span class="sxs-lookup"><span data-stu-id="097ae-119">Type:</span></span>

<span data-ttu-id="097ae-120">Il tipo restituito corrisponde al tipo nella dichiarazione per l'oggetto [**RWBuffer**](sm5-object-rwbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="097ae-120">The return type matches the type in the declaration for the [**RWBuffer**](sm5-object-rwbuffer.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="097ae-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="097ae-121">Remarks</span></span>

<span data-ttu-id="097ae-122">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="097ae-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="097ae-123">Vertice</span><span class="sxs-lookup"><span data-stu-id="097ae-123">Vertex</span></span> | <span data-ttu-id="097ae-124">Hull</span><span class="sxs-lookup"><span data-stu-id="097ae-124">Hull</span></span> | <span data-ttu-id="097ae-125">Dominio</span><span class="sxs-lookup"><span data-stu-id="097ae-125">Domain</span></span> | <span data-ttu-id="097ae-126">Geometria</span><span class="sxs-lookup"><span data-stu-id="097ae-126">Geometry</span></span> | <span data-ttu-id="097ae-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="097ae-127">Pixel</span></span> | <span data-ttu-id="097ae-128">Calcolo</span><span class="sxs-lookup"><span data-stu-id="097ae-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="097ae-129">x</span><span class="sxs-lookup"><span data-stu-id="097ae-129">x</span></span>      | <span data-ttu-id="097ae-130">x</span><span class="sxs-lookup"><span data-stu-id="097ae-130">x</span></span>    | <span data-ttu-id="097ae-131">x</span><span class="sxs-lookup"><span data-stu-id="097ae-131">x</span></span>      | <span data-ttu-id="097ae-132">x</span><span class="sxs-lookup"><span data-stu-id="097ae-132">x</span></span>        | <span data-ttu-id="097ae-133">x</span><span class="sxs-lookup"><span data-stu-id="097ae-133">x</span></span>     | <span data-ttu-id="097ae-134">x</span><span class="sxs-lookup"><span data-stu-id="097ae-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="097ae-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="097ae-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="097ae-136">Metodi Load</span><span class="sxs-lookup"><span data-stu-id="097ae-136">Load methods</span></span>](rwbuffer-load.md)
</dt> </dl>

 

 
