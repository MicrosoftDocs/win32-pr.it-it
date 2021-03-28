---
title: 'Funzione ByteAddressBuffer:: Load (int, uint)'
description: Ottiene un valore e lo stato dell'operazione.
ms.assetid: 8F90671B-CEEB-4F8C-9469-D85940568872
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
ms.openlocfilehash: 319daad35da0256a4d36ef4580df62fd4d295854
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104118754"
---
# <a name="byteaddressbufferloadint-uint-function"></a><span data-ttu-id="4b13b-104">Funzione ByteAddressBuffer:: Load (int, uint)</span><span class="sxs-lookup"><span data-stu-id="4b13b-104">ByteAddressBuffer::Load(int, uint) function</span></span>

<span data-ttu-id="4b13b-105">Ottiene un valore e lo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="4b13b-105">Gets one value and the status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b13b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4b13b-106">Syntax</span></span>

``` syntax
uint Load(
  in  int Location,
  out uint Status
);
```

## <a name="parameters"></a><span data-ttu-id="4b13b-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="4b13b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b13b-108">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4b13b-108">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b13b-109">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="4b13b-109">Type: **int**</span></span>

<span data-ttu-id="4b13b-110">Indirizzo di input in byte, che deve essere un multiplo di 4.</span><span class="sxs-lookup"><span data-stu-id="4b13b-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="4b13b-111">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="4b13b-111">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4b13b-112">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="4b13b-112">Type: **uint**</span></span>

<span data-ttu-id="4b13b-113">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="4b13b-113">The status of the operation.</span></span> <span data-ttu-id="4b13b-114">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="4b13b-114">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="4b13b-115">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="4b13b-115">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="4b13b-116">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="4b13b-116">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b13b-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4b13b-117">Return value</span></span>

<span data-ttu-id="4b13b-118">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="4b13b-118">Type: **uint**</span></span>

<span data-ttu-id="4b13b-119">Un valore.</span><span class="sxs-lookup"><span data-stu-id="4b13b-119">One value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b13b-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="4b13b-120">Remarks</span></span>

<span data-ttu-id="4b13b-121">Questa funzione è supportata per i tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="4b13b-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="4b13b-122">Vertice</span><span class="sxs-lookup"><span data-stu-id="4b13b-122">Vertex</span></span> | <span data-ttu-id="4b13b-123">Hull</span><span class="sxs-lookup"><span data-stu-id="4b13b-123">Hull</span></span> | <span data-ttu-id="4b13b-124">Dominio</span><span class="sxs-lookup"><span data-stu-id="4b13b-124">Domain</span></span> | <span data-ttu-id="4b13b-125">Geometria</span><span class="sxs-lookup"><span data-stu-id="4b13b-125">Geometry</span></span> | <span data-ttu-id="4b13b-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="4b13b-126">Pixel</span></span> | <span data-ttu-id="4b13b-127">Calcolo</span><span class="sxs-lookup"><span data-stu-id="4b13b-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="4b13b-128">x</span><span class="sxs-lookup"><span data-stu-id="4b13b-128">x</span></span>      | <span data-ttu-id="4b13b-129">x</span><span class="sxs-lookup"><span data-stu-id="4b13b-129">x</span></span>    | <span data-ttu-id="4b13b-130">x</span><span class="sxs-lookup"><span data-stu-id="4b13b-130">x</span></span>      | <span data-ttu-id="4b13b-131">x</span><span class="sxs-lookup"><span data-stu-id="4b13b-131">x</span></span>        | <span data-ttu-id="4b13b-132">x</span><span class="sxs-lookup"><span data-stu-id="4b13b-132">x</span></span>     | <span data-ttu-id="4b13b-133">x</span><span class="sxs-lookup"><span data-stu-id="4b13b-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="4b13b-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4b13b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b13b-135">Metodi Load</span><span class="sxs-lookup"><span data-stu-id="4b13b-135">Load methods</span></span>](byteaddressbuffer-load.md)
</dt> <dt>

[<span data-ttu-id="4b13b-136">**ByteAddressBuffer**</span><span class="sxs-lookup"><span data-stu-id="4b13b-136">**ByteAddressBuffer**</span></span>](sm5-object-byteaddressbuffer.md)
</dt> </dl>

 

 
