---
title: 'Funzione RWByteAddressBuffer:: Load4 (uint, uint)'
description: Ottiene quattro valori e restituisce lo stato dell'operazione.
ms.assetid: 10C21836-3CE4-4AE9-82F4-C8BBDE19CA69
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
ms.openlocfilehash: 14cb5354c21935c22833ea6f4b54b20fedc696f0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730122"
---
# <a name="load4uintuint-function"></a><span data-ttu-id="cf646-104">Funzione Load4 (uint, uint)</span><span class="sxs-lookup"><span data-stu-id="cf646-104">Load4(uint,uint) function</span></span>

<span data-ttu-id="cf646-105">Ottiene quattro valori e restituisce lo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="cf646-105">Gets four values and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf646-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cf646-106">Syntax</span></span>


``` syntax
uint4 Load4(
  in  uint Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="cf646-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="cf646-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf646-108">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cf646-108">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf646-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="cf646-109">Type: **uint**</span></span>

<span data-ttu-id="cf646-110">Posizione del buffer.</span><span class="sxs-lookup"><span data-stu-id="cf646-110">The location of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="cf646-111">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="cf646-111">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf646-112">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="cf646-112">Type: **uint**</span></span>

<span data-ttu-id="cf646-113">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="cf646-113">The status of the operation.</span></span> <span data-ttu-id="cf646-114">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="cf646-114">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="cf646-115">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="cf646-115">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="cf646-116">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="cf646-116">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf646-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cf646-117">Return value</span></span>

<span data-ttu-id="cf646-118">Tipo: **uint4**</span><span class="sxs-lookup"><span data-stu-id="cf646-118">Type: **uint4**</span></span>

<span data-ttu-id="cf646-119">Quattro valori.</span><span class="sxs-lookup"><span data-stu-id="cf646-119">Four values.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf646-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="cf646-120">Remarks</span></span>

<span data-ttu-id="cf646-121">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="cf646-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="cf646-122">Vertice</span><span class="sxs-lookup"><span data-stu-id="cf646-122">Vertex</span></span> | <span data-ttu-id="cf646-123">Hull</span><span class="sxs-lookup"><span data-stu-id="cf646-123">Hull</span></span> | <span data-ttu-id="cf646-124">Dominio</span><span class="sxs-lookup"><span data-stu-id="cf646-124">Domain</span></span> | <span data-ttu-id="cf646-125">Geometria</span><span class="sxs-lookup"><span data-stu-id="cf646-125">Geometry</span></span> | <span data-ttu-id="cf646-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="cf646-126">Pixel</span></span> | <span data-ttu-id="cf646-127">Calcolo</span><span class="sxs-lookup"><span data-stu-id="cf646-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="cf646-128">x</span><span class="sxs-lookup"><span data-stu-id="cf646-128">x</span></span>     | <span data-ttu-id="cf646-129">x</span><span class="sxs-lookup"><span data-stu-id="cf646-129">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="cf646-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cf646-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf646-131">Metodi Load4</span><span class="sxs-lookup"><span data-stu-id="cf646-131">Load4 methods</span></span>](rwbyteaddressbuffer-load4.md)
</dt> </dl>

 

 