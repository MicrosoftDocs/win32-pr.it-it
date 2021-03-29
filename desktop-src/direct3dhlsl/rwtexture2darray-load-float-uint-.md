---
title: 'Funzione RWTexture2DArray:: Load (int, uint)'
description: "Legge i dati della trama e restituisce lo stato dell'operazione. | Funzione RWTexture2DArray:: Load (int, uint)"
ms.assetid: 97D6E36A-1613-43BA-92C1-3034E0F344F0
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
ms.openlocfilehash: 969aa0a4efa62f7072c759a1f2188e4d210d8649
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981642"
---
# <a name="rwtexture2darrayloadintuint-function"></a><span data-ttu-id="340dc-105">Funzione RWTexture2DArray:: Load (int, uint)</span><span class="sxs-lookup"><span data-stu-id="340dc-105">RWTexture2DArray::Load(int,uint) function</span></span>

<span data-ttu-id="340dc-106">Legge i dati della trama e restituisce lo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="340dc-106">Reads texture data and returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="340dc-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="340dc-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="340dc-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="340dc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="340dc-109">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="340dc-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="340dc-110">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="340dc-110">Type: **int**</span></span>

<span data-ttu-id="340dc-111">Posizione della trama.</span><span class="sxs-lookup"><span data-stu-id="340dc-111">The location of the texture.</span></span>

</dd> <dt>

<span data-ttu-id="340dc-112">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="340dc-112">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="340dc-113">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="340dc-113">Type: **uint**</span></span>

<span data-ttu-id="340dc-114">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="340dc-114">The status of the operation.</span></span> <span data-ttu-id="340dc-115">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="340dc-115">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="340dc-116">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="340dc-116">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="340dc-117">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="340dc-117">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="340dc-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="340dc-118">Return value</span></span>

<span data-ttu-id="340dc-119">Digitare:</span><span class="sxs-lookup"><span data-stu-id="340dc-119">Type:</span></span>

<span data-ttu-id="340dc-120">Il tipo restituito corrisponde al tipo nella dichiarazione per l'oggetto [**RWTexture2DArray**](sm5-object-rwtexture2darray.md) .</span><span class="sxs-lookup"><span data-stu-id="340dc-120">The return type matches the type in the declaration for the [**RWTexture2DArray**](sm5-object-rwtexture2darray.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="340dc-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="340dc-121">Remarks</span></span>

<span data-ttu-id="340dc-122">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="340dc-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="340dc-123">Vertice</span><span class="sxs-lookup"><span data-stu-id="340dc-123">Vertex</span></span> | <span data-ttu-id="340dc-124">Hull</span><span class="sxs-lookup"><span data-stu-id="340dc-124">Hull</span></span> | <span data-ttu-id="340dc-125">Dominio</span><span class="sxs-lookup"><span data-stu-id="340dc-125">Domain</span></span> | <span data-ttu-id="340dc-126">Geometria</span><span class="sxs-lookup"><span data-stu-id="340dc-126">Geometry</span></span> | <span data-ttu-id="340dc-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="340dc-127">Pixel</span></span> | <span data-ttu-id="340dc-128">Calcolo</span><span class="sxs-lookup"><span data-stu-id="340dc-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="340dc-129">x</span><span class="sxs-lookup"><span data-stu-id="340dc-129">x</span></span>     | <span data-ttu-id="340dc-130">x</span><span class="sxs-lookup"><span data-stu-id="340dc-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="340dc-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="340dc-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="340dc-132">Metodi Load</span><span class="sxs-lookup"><span data-stu-id="340dc-132">Load methods</span></span>](rwtexture2darray-load.md)
</dt> </dl>

 

 
