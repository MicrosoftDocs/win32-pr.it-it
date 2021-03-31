---
title: 'Funzione ByteAddressBuffer:: load2 (uint, uint)'
description: Ottiene due valori e lo stato dell'operazione.
ms.assetid: EE6FA09D-0C86-499D-86F9-EAA56125EB91
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
ms.openlocfilehash: 662e40789f59b75e53111fbab6d24288f27c8e35
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047130"
---
# <a name="load2uint-uint-function"></a><span data-ttu-id="8a571-104">Funzione load2 (uint, uint)</span><span class="sxs-lookup"><span data-stu-id="8a571-104">Load2(uint, uint) function</span></span>

<span data-ttu-id="8a571-105">Ottiene due valori e lo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="8a571-105">Gets two values and the status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a571-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8a571-106">Syntax</span></span>

``` syntax
uint2 Load2(
  in  uint Location,
  out uint Status
);
```

## <a name="parameters"></a><span data-ttu-id="8a571-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="8a571-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a571-108">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8a571-108">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a571-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="8a571-109">Type: **uint**</span></span>

<span data-ttu-id="8a571-110">Indirizzo di input in byte, che deve essere un multiplo di 4.</span><span class="sxs-lookup"><span data-stu-id="8a571-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="8a571-111">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="8a571-111">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a571-112">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="8a571-112">Type: **uint**</span></span>

<span data-ttu-id="8a571-113">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="8a571-113">The status of the operation.</span></span> <span data-ttu-id="8a571-114">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="8a571-114">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="8a571-115">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="8a571-115">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="8a571-116">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="8a571-116">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a571-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8a571-117">Return value</span></span>

<span data-ttu-id="8a571-118">Tipo: **uint2**</span><span class="sxs-lookup"><span data-stu-id="8a571-118">Type: **uint2**</span></span>

<span data-ttu-id="8a571-119">Due valori.</span><span class="sxs-lookup"><span data-stu-id="8a571-119">Two values.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a571-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="8a571-120">Remarks</span></span>

<span data-ttu-id="8a571-121">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="8a571-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="8a571-122">Vertice</span><span class="sxs-lookup"><span data-stu-id="8a571-122">Vertex</span></span> | <span data-ttu-id="8a571-123">Hull</span><span class="sxs-lookup"><span data-stu-id="8a571-123">Hull</span></span> | <span data-ttu-id="8a571-124">Dominio</span><span class="sxs-lookup"><span data-stu-id="8a571-124">Domain</span></span> | <span data-ttu-id="8a571-125">Geometria</span><span class="sxs-lookup"><span data-stu-id="8a571-125">Geometry</span></span> | <span data-ttu-id="8a571-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="8a571-126">Pixel</span></span> | <span data-ttu-id="8a571-127">Calcolo</span><span class="sxs-lookup"><span data-stu-id="8a571-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="8a571-128">x</span><span class="sxs-lookup"><span data-stu-id="8a571-128">x</span></span>      | <span data-ttu-id="8a571-129">x</span><span class="sxs-lookup"><span data-stu-id="8a571-129">x</span></span>    | <span data-ttu-id="8a571-130">x</span><span class="sxs-lookup"><span data-stu-id="8a571-130">x</span></span>      | <span data-ttu-id="8a571-131">x</span><span class="sxs-lookup"><span data-stu-id="8a571-131">x</span></span>        | <span data-ttu-id="8a571-132">x</span><span class="sxs-lookup"><span data-stu-id="8a571-132">x</span></span>     | <span data-ttu-id="8a571-133">x</span><span class="sxs-lookup"><span data-stu-id="8a571-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="8a571-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8a571-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a571-135">Metodi load2</span><span class="sxs-lookup"><span data-stu-id="8a571-135">Load2 methods</span></span>](byteaddressbuffer-load2.md)
</dt> <dt>

[<span data-ttu-id="8a571-136">**ByteAddressBuffer**</span><span class="sxs-lookup"><span data-stu-id="8a571-136">**ByteAddressBuffer**</span></span>](sm5-object-byteaddressbuffer.md)
</dt> </dl>

 

 