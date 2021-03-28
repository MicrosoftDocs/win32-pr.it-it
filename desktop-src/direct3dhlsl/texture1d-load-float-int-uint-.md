---
title: 'Funzione Texture1D:: Load (int, int, uint)'
description: "Legge i dati della trama e restituisce lo stato dell'operazione. | Funzione Texture1D:: Load (int, int, uint)"
ms.assetid: 5C489CBD-E4F6-4CB5-8E7E-EC34633D75B0
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
ms.openlocfilehash: 0c7733ab4802037d83dbb2b4ce523ff7bb57f729
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981618"
---
# <a name="texture1dloadintintuint-function"></a><span data-ttu-id="fe2b7-105">Funzione Texture1D:: Load (int, int, uint)</span><span class="sxs-lookup"><span data-stu-id="fe2b7-105">Texture1D::Load(int,int,uint) function</span></span>

<span data-ttu-id="fe2b7-106">Legge i dati della trama e restituisce lo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="fe2b7-106">Reads texture data and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe2b7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fe2b7-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  in  int  Offset,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="fe2b7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="fe2b7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe2b7-109">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe2b7-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe2b7-110">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="fe2b7-110">Type: **int**</span></span>

<span data-ttu-id="fe2b7-111">Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="fe2b7-111">The texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="fe2b7-112">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe2b7-112">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe2b7-113">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="fe2b7-113">Type: **int**</span></span>

<span data-ttu-id="fe2b7-114">Offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="fe2b7-114">An offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="fe2b7-115">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="fe2b7-115">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe2b7-116">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="fe2b7-116">Type: **uint**</span></span>

<span data-ttu-id="fe2b7-117">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="fe2b7-117">The status of the operation.</span></span> <span data-ttu-id="fe2b7-118">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="fe2b7-118">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="fe2b7-119">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="fe2b7-119">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="fe2b7-120">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="fe2b7-120">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe2b7-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fe2b7-121">Return value</span></span>

<span data-ttu-id="fe2b7-122">Digitare:</span><span class="sxs-lookup"><span data-stu-id="fe2b7-122">Type:</span></span>

<span data-ttu-id="fe2b7-123">Il tipo restituito corrisponde al tipo nella dichiarazione per l'oggetto [**Texture1D**](sm5-object-texture1d.md) .</span><span class="sxs-lookup"><span data-stu-id="fe2b7-123">The return type matches the type in the declaration for the [**Texture1D**](sm5-object-texture1d.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe2b7-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="fe2b7-124">Remarks</span></span>

<span data-ttu-id="fe2b7-125">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="fe2b7-125">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="fe2b7-126">Vertice</span><span class="sxs-lookup"><span data-stu-id="fe2b7-126">Vertex</span></span> | <span data-ttu-id="fe2b7-127">Hull</span><span class="sxs-lookup"><span data-stu-id="fe2b7-127">Hull</span></span> | <span data-ttu-id="fe2b7-128">Dominio</span><span class="sxs-lookup"><span data-stu-id="fe2b7-128">Domain</span></span> | <span data-ttu-id="fe2b7-129">Geometria</span><span class="sxs-lookup"><span data-stu-id="fe2b7-129">Geometry</span></span> | <span data-ttu-id="fe2b7-130">Pixel</span><span class="sxs-lookup"><span data-stu-id="fe2b7-130">Pixel</span></span> | <span data-ttu-id="fe2b7-131">Calcolo</span><span class="sxs-lookup"><span data-stu-id="fe2b7-131">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="fe2b7-132">x</span><span class="sxs-lookup"><span data-stu-id="fe2b7-132">x</span></span>      | <span data-ttu-id="fe2b7-133">x</span><span class="sxs-lookup"><span data-stu-id="fe2b7-133">x</span></span>    | <span data-ttu-id="fe2b7-134">x</span><span class="sxs-lookup"><span data-stu-id="fe2b7-134">x</span></span>      | <span data-ttu-id="fe2b7-135">x</span><span class="sxs-lookup"><span data-stu-id="fe2b7-135">x</span></span>        | <span data-ttu-id="fe2b7-136">x</span><span class="sxs-lookup"><span data-stu-id="fe2b7-136">x</span></span>     | <span data-ttu-id="fe2b7-137">x</span><span class="sxs-lookup"><span data-stu-id="fe2b7-137">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="fe2b7-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fe2b7-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe2b7-139">Metodi Load</span><span class="sxs-lookup"><span data-stu-id="fe2b7-139">Load methods</span></span>](texture1d-load.md)
</dt> <dt>

[<span data-ttu-id="fe2b7-140">**Texture1D**</span><span class="sxs-lookup"><span data-stu-id="fe2b7-140">**Texture1D**</span></span>](sm5-object-texture1d.md)
</dt> </dl>

 

 
