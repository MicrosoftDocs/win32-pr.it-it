---
title: 'Funzione RWTexture1D:: Load (int, uint)'
description: "Legge i dati della trama e restituisce lo stato dell'operazione. | Funzione RWTexture1D:: Load (int, uint)"
ms.assetid: 3BF2397D-400C-48EE-8D45-872BA61F007B
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
ms.openlocfilehash: afba9445d152810e5776ae0ee7f603bb7ee55ac2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981247"
---
# <a name="rwtexture1dloadintuint-function"></a><span data-ttu-id="36106-105">Funzione RWTexture1D:: Load (int, uint)</span><span class="sxs-lookup"><span data-stu-id="36106-105">RWTexture1D::Load(int,uint) function</span></span>

<span data-ttu-id="36106-106">Legge i dati della trama e restituisce lo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="36106-106">Reads texture data and returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="36106-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="36106-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="36106-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="36106-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36106-109">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="36106-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36106-110">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="36106-110">Type: **int**</span></span>

<span data-ttu-id="36106-111">Posizione della trama.</span><span class="sxs-lookup"><span data-stu-id="36106-111">The location of the texture.</span></span>

</dd> <dt>

<span data-ttu-id="36106-112">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="36106-112">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="36106-113">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="36106-113">Type: **uint**</span></span>

<span data-ttu-id="36106-114">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="36106-114">The status of the operation.</span></span> <span data-ttu-id="36106-115">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="36106-115">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="36106-116">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="36106-116">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="36106-117">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="36106-117">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36106-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="36106-118">Return value</span></span>

<span data-ttu-id="36106-119">Digitare:</span><span class="sxs-lookup"><span data-stu-id="36106-119">Type:</span></span>

<span data-ttu-id="36106-120">Il tipo restituito corrisponde al tipo nella dichiarazione per l'oggetto [**RWTexture1D**](sm5-object-rwtexture1d.md) .</span><span class="sxs-lookup"><span data-stu-id="36106-120">The return type matches the type in the declaration for the [**RWTexture1D**](sm5-object-rwtexture1d.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="36106-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="36106-121">Remarks</span></span>

<span data-ttu-id="36106-122">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="36106-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="36106-123">Vertice</span><span class="sxs-lookup"><span data-stu-id="36106-123">Vertex</span></span> | <span data-ttu-id="36106-124">Hull</span><span class="sxs-lookup"><span data-stu-id="36106-124">Hull</span></span> | <span data-ttu-id="36106-125">Dominio</span><span class="sxs-lookup"><span data-stu-id="36106-125">Domain</span></span> | <span data-ttu-id="36106-126">Geometria</span><span class="sxs-lookup"><span data-stu-id="36106-126">Geometry</span></span> | <span data-ttu-id="36106-127">Pixel</span><span class="sxs-lookup"><span data-stu-id="36106-127">Pixel</span></span> | <span data-ttu-id="36106-128">Calcolo</span><span class="sxs-lookup"><span data-stu-id="36106-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="36106-129">x</span><span class="sxs-lookup"><span data-stu-id="36106-129">x</span></span>     | <span data-ttu-id="36106-130">x</span><span class="sxs-lookup"><span data-stu-id="36106-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="36106-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="36106-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36106-132">Metodi Load</span><span class="sxs-lookup"><span data-stu-id="36106-132">Load methods</span></span>](rwtexture1d-load.md)
</dt> </dl>

 

 
