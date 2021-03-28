---
title: 'Funzione RWByteAddressBuffer:: load2 (uint, uint)'
description: Ottiene due valori e restituisce lo stato dell'operazione.
ms.assetid: E6BBA8A7-D53F-4718-B007-EBDE50FADB06
keywords:
- Funzione load2 HLSL
topic_type:
- apiref
api_name:
- Load2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 92fc492fddb6ad024a4507829e81dab4886af590
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117766"
---
# <a name="load2uintuint-function"></a><span data-ttu-id="a510e-104">Funzione load2 (uint, uint)</span><span class="sxs-lookup"><span data-stu-id="a510e-104">Load2(uint,uint) function</span></span>

<span data-ttu-id="a510e-105">Ottiene due valori e restituisce lo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="a510e-105">Gets two values and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="a510e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a510e-106">Syntax</span></span>


``` syntax
uint2 Load2(
  in  uint Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="a510e-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="a510e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a510e-108">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a510e-108">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a510e-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="a510e-109">Type: **uint**</span></span>

<span data-ttu-id="a510e-110">Posizione del buffer.</span><span class="sxs-lookup"><span data-stu-id="a510e-110">The location of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="a510e-111">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="a510e-111">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a510e-112">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="a510e-112">Type: **uint**</span></span>

<span data-ttu-id="a510e-113">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="a510e-113">The status of the operation.</span></span> <span data-ttu-id="a510e-114">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="a510e-114">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="a510e-115">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="a510e-115">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="a510e-116">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="a510e-116">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a510e-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a510e-117">Return value</span></span>

<span data-ttu-id="a510e-118">Tipo: **uint2**</span><span class="sxs-lookup"><span data-stu-id="a510e-118">Type: **uint2**</span></span>

<span data-ttu-id="a510e-119">Due valori.</span><span class="sxs-lookup"><span data-stu-id="a510e-119">Two values.</span></span>

## <a name="remarks"></a><span data-ttu-id="a510e-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="a510e-120">Remarks</span></span>

<span data-ttu-id="a510e-121">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="a510e-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="a510e-122">Vertice</span><span class="sxs-lookup"><span data-stu-id="a510e-122">Vertex</span></span> | <span data-ttu-id="a510e-123">Hull</span><span class="sxs-lookup"><span data-stu-id="a510e-123">Hull</span></span> | <span data-ttu-id="a510e-124">Dominio</span><span class="sxs-lookup"><span data-stu-id="a510e-124">Domain</span></span> | <span data-ttu-id="a510e-125">Geometria</span><span class="sxs-lookup"><span data-stu-id="a510e-125">Geometry</span></span> | <span data-ttu-id="a510e-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="a510e-126">Pixel</span></span> | <span data-ttu-id="a510e-127">Calcolo</span><span class="sxs-lookup"><span data-stu-id="a510e-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="a510e-128">x</span><span class="sxs-lookup"><span data-stu-id="a510e-128">x</span></span>     | <span data-ttu-id="a510e-129">x</span><span class="sxs-lookup"><span data-stu-id="a510e-129">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="a510e-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a510e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a510e-131">Metodi load2</span><span class="sxs-lookup"><span data-stu-id="a510e-131">Load2 methods</span></span>](rwbyteaddressbuffer-load2.md)
</dt> </dl>

 

 