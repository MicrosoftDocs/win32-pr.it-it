---
title: 'Funzione Texture1DArray:: Load (int, int, uint)'
description: "Legge i dati della trama e restituisce lo stato dell'operazione. | Funzione Texture1DArray:: Load (int, int, uint)"
ms.assetid: D5877CED-BE73-4E37-B09D-4096726776EC
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
ms.openlocfilehash: ee367aaf98aa971aa10c6859f117f15df9fcdd83
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981463"
---
# <a name="texture1darrayloadintintuint-function"></a><span data-ttu-id="2defd-105">Funzione Texture1DArray:: Load (int, int, uint)</span><span class="sxs-lookup"><span data-stu-id="2defd-105">Texture1DArray::Load(int,int,uint) function</span></span>

<span data-ttu-id="2defd-106">Legge i dati della trama e restituisce lo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="2defd-106">Reads texture data and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="2defd-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2defd-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  in  int  Offset,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="2defd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2defd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2defd-109">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2defd-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2defd-110">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="2defd-110">Type: **int**</span></span>

<span data-ttu-id="2defd-111">Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="2defd-111">The texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="2defd-112">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2defd-112">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2defd-113">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="2defd-113">Type: **int**</span></span>

<span data-ttu-id="2defd-114">Offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="2defd-114">An offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="2defd-115">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="2defd-115">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2defd-116">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="2defd-116">Type: **uint**</span></span>

<span data-ttu-id="2defd-117">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="2defd-117">The status of the operation.</span></span> <span data-ttu-id="2defd-118">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="2defd-118">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="2defd-119">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="2defd-119">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="2defd-120">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="2defd-120">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2defd-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2defd-121">Return value</span></span>

<span data-ttu-id="2defd-122">Digitare:</span><span class="sxs-lookup"><span data-stu-id="2defd-122">Type:</span></span>

<span data-ttu-id="2defd-123">Il tipo restituito corrisponde al tipo nella dichiarazione per l'oggetto [**Texture1DArray**](sm5-object-texture1darray.md) .</span><span class="sxs-lookup"><span data-stu-id="2defd-123">The return type matches the type in the declaration for the [**Texture1DArray**](sm5-object-texture1darray.md) object.</span></span>

## <a name="see-also"></a><span data-ttu-id="2defd-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2defd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2defd-125">Metodi Load</span><span class="sxs-lookup"><span data-stu-id="2defd-125">Load methods</span></span>](texture1darray-load.md)
</dt> </dl>

 

 
