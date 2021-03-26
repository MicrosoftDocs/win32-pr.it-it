---
title: 'Funzione RWByteAddressBuffer:: Load (int, uint)'
description: Ottiene un valore e restituisce lo stato dell'operazione.
ms.assetid: E3FD0FFA-6A9B-4B44-A90D-47270326F9BA
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
ms.openlocfilehash: 71f142d35ae8be3800ccf85b5e8114d5e85c44ac
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103873161"
---
# <a name="rwbyteaddressbufferloadintuint-function"></a><span data-ttu-id="a2d40-104">Funzione RWByteAddressBuffer:: Load (int, uint)</span><span class="sxs-lookup"><span data-stu-id="a2d40-104">RWByteAddressBuffer::Load(int,uint) function</span></span>

<span data-ttu-id="a2d40-105">Ottiene un valore e restituisce lo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="a2d40-105">Gets one value and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2d40-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a2d40-106">Syntax</span></span>


``` syntax
uint Load(
  in  int  Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="a2d40-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="a2d40-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2d40-108">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a2d40-108">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2d40-109">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="a2d40-109">Type: **int**</span></span>

<span data-ttu-id="a2d40-110">Posizione del buffer.</span><span class="sxs-lookup"><span data-stu-id="a2d40-110">The location of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="a2d40-111">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="a2d40-111">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a2d40-112">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="a2d40-112">Type: **uint**</span></span>

<span data-ttu-id="a2d40-113">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="a2d40-113">The status of the operation.</span></span> <span data-ttu-id="a2d40-114">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="a2d40-114">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="a2d40-115">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="a2d40-115">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="a2d40-116">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="a2d40-116">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2d40-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a2d40-117">Return value</span></span>

<span data-ttu-id="a2d40-118">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="a2d40-118">Type: **uint**</span></span>

<span data-ttu-id="a2d40-119">Un valore.</span><span class="sxs-lookup"><span data-stu-id="a2d40-119">One value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2d40-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="a2d40-120">Remarks</span></span>

<span data-ttu-id="a2d40-121">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="a2d40-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="a2d40-122">Vertice</span><span class="sxs-lookup"><span data-stu-id="a2d40-122">Vertex</span></span> | <span data-ttu-id="a2d40-123">Hull</span><span class="sxs-lookup"><span data-stu-id="a2d40-123">Hull</span></span> | <span data-ttu-id="a2d40-124">Dominio</span><span class="sxs-lookup"><span data-stu-id="a2d40-124">Domain</span></span> | <span data-ttu-id="a2d40-125">Geometria</span><span class="sxs-lookup"><span data-stu-id="a2d40-125">Geometry</span></span> | <span data-ttu-id="a2d40-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="a2d40-126">Pixel</span></span> | <span data-ttu-id="a2d40-127">Calcolo</span><span class="sxs-lookup"><span data-stu-id="a2d40-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="a2d40-128">x</span><span class="sxs-lookup"><span data-stu-id="a2d40-128">x</span></span>     | <span data-ttu-id="a2d40-129">x</span><span class="sxs-lookup"><span data-stu-id="a2d40-129">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="a2d40-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a2d40-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2d40-131">Metodi Load</span><span class="sxs-lookup"><span data-stu-id="a2d40-131">Load methods</span></span>](rwbyteaddressbuffer-load.md)
</dt> </dl>

 

 
