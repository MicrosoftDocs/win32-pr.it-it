---
title: 'Funzione buffer:: Load (int, uint)'
description: "Legge i dati del buffer e restituisce lo stato dell'operazione. | Funzione buffer:: Load (int, uint)"
ms.assetid: 0C7FC522-C962-4467-AA3E-6611064C188B
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
ms.openlocfilehash: eccd5c367e593559b6a719777dfd1535ae2d423a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981087"
---
# <a name="bufferloadint-uint-function"></a><span data-ttu-id="96c0e-105">Funzione buffer:: Load (int, uint)</span><span class="sxs-lookup"><span data-stu-id="96c0e-105">Buffer::Load(int, uint) function</span></span>

<span data-ttu-id="96c0e-106">Legge i dati del buffer e restituisce lo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="96c0e-106">Reads buffer data and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="96c0e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="96c0e-107">Syntax</span></span>

``` syntax
 Load(
  in  int Location,
  out uint Status
);
```

## <a name="parameters"></a><span data-ttu-id="96c0e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="96c0e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96c0e-109">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="96c0e-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96c0e-110">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="96c0e-110">Type: **int**</span></span>

<span data-ttu-id="96c0e-111">Posizione del buffer.</span><span class="sxs-lookup"><span data-stu-id="96c0e-111">The location of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="96c0e-112">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="96c0e-112">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="96c0e-113">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="96c0e-113">Type: **uint**</span></span>

<span data-ttu-id="96c0e-114">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="96c0e-114">The status of the operation.</span></span> <span data-ttu-id="96c0e-115">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="96c0e-115">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="96c0e-116">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="96c0e-116">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="96c0e-117">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="96c0e-117">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96c0e-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="96c0e-118">Return value</span></span>

<span data-ttu-id="96c0e-119">Digitare:</span><span class="sxs-lookup"><span data-stu-id="96c0e-119">Type:</span></span>

<span data-ttu-id="96c0e-120">Il tipo restituito corrisponde al tipo nella dichiarazione per l'oggetto [**buffer**](sm5-object-buffer.md) .</span><span class="sxs-lookup"><span data-stu-id="96c0e-120">The return type matches the type in the declaration for the [**Buffer**](sm5-object-buffer.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="96c0e-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="96c0e-121">Remarks</span></span>

<span data-ttu-id="96c0e-122">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="96c0e-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="96c0e-123">Vertice</span><span class="sxs-lookup"><span data-stu-id="96c0e-123">Vertex</span></span> | <span data-ttu-id="96c0e-124">Hull</span><span class="sxs-lookup"><span data-stu-id="96c0e-124">Hull</span></span> | <span data-ttu-id="96c0e-125">Dominio</span><span class="sxs-lookup"><span data-stu-id="96c0e-125">Domain</span></span> | <span data-ttu-id="96c0e-126">Geometria</span><span class="sxs-lookup"><span data-stu-id="96c0e-126">Geometry</span></span> | <span data-ttu-id="96c0e-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="96c0e-127">Pixel</span></span> | <span data-ttu-id="96c0e-128">Calcolo</span><span class="sxs-lookup"><span data-stu-id="96c0e-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="96c0e-129">x</span><span class="sxs-lookup"><span data-stu-id="96c0e-129">x</span></span>      | <span data-ttu-id="96c0e-130">x</span><span class="sxs-lookup"><span data-stu-id="96c0e-130">x</span></span>    | <span data-ttu-id="96c0e-131">x</span><span class="sxs-lookup"><span data-stu-id="96c0e-131">x</span></span>      | <span data-ttu-id="96c0e-132">x</span><span class="sxs-lookup"><span data-stu-id="96c0e-132">x</span></span>        | <span data-ttu-id="96c0e-133">x</span><span class="sxs-lookup"><span data-stu-id="96c0e-133">x</span></span>     | <span data-ttu-id="96c0e-134">x</span><span class="sxs-lookup"><span data-stu-id="96c0e-134">x</span></span>       |



 

## <a name="examples"></a><span data-ttu-id="96c0e-135">Esempio</span><span class="sxs-lookup"><span data-stu-id="96c0e-135">Examples</span></span>

<span data-ttu-id="96c0e-136">Questo esempio illustra come usare **Load**:</span><span class="sxs-lookup"><span data-stu-id="96c0e-136">This example shows how to use **Load**:</span></span>

``` syntax
Buffer<float4> myBuffer;
float loc;
uint status;
float4 myColor = myBuffer.Load( loc , status );
```

## <a name="see-also"></a><span data-ttu-id="96c0e-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="96c0e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96c0e-138">Metodi Load</span><span class="sxs-lookup"><span data-stu-id="96c0e-138">Load methods</span></span>](buffer-load.md)
</dt> </dl>

 

 
