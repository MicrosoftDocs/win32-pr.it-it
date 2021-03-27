---
title: 'Funzione Texture3D:: Load (int, int, uint)'
description: "Legge i dati della trama e restituisce lo stato dell'operazione. | Funzione Texture3D:: Load (int, int, uint)"
ms.assetid: 3F562ADB-225F-462B-A7AC-40797BBB632A
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
ms.openlocfilehash: 19522fe60567e55565265ce0c8b5051c7bf7ccdd
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995325"
---
# <a name="texture3dloadintintuint-function"></a><span data-ttu-id="6f1fb-105">Funzione Texture3D:: Load (int, int, uint)</span><span class="sxs-lookup"><span data-stu-id="6f1fb-105">Texture3D::Load(int,int,uint) function</span></span>

<span data-ttu-id="6f1fb-106">Legge i dati della trama e restituisce lo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-106">Reads texture data and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f1fb-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6f1fb-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  in  int  Offset,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="6f1fb-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6f1fb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f1fb-109">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6f1fb-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f1fb-110">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="6f1fb-110">Type: **int**</span></span>

<span data-ttu-id="6f1fb-111">Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-111">The texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="6f1fb-112">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6f1fb-112">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f1fb-113">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="6f1fb-113">Type: **int**</span></span>

<span data-ttu-id="6f1fb-114">Offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-114">An offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="6f1fb-115">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="6f1fb-115">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f1fb-116">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="6f1fb-116">Type: **uint**</span></span>

<span data-ttu-id="6f1fb-117">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-117">The status of the operation.</span></span> <span data-ttu-id="6f1fb-118">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="6f1fb-118">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="6f1fb-119">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="6f1fb-119">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="6f1fb-120">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="6f1fb-120">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f1fb-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6f1fb-121">Return value</span></span>

<span data-ttu-id="6f1fb-122">Digitare:</span><span class="sxs-lookup"><span data-stu-id="6f1fb-122">Type:</span></span>

<span data-ttu-id="6f1fb-123">Il tipo restituito corrisponde al tipo nella dichiarazione per l'oggetto [**Texture3D**](sm5-object-texture3d.md) .</span><span class="sxs-lookup"><span data-stu-id="6f1fb-123">The return type matches the type in the declaration for the [**Texture3D**](sm5-object-texture3d.md) object.</span></span>

## <a name="see-also"></a><span data-ttu-id="6f1fb-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6f1fb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f1fb-125">Metodi Load</span><span class="sxs-lookup"><span data-stu-id="6f1fb-125">Load methods</span></span>](texture3d-load.md)
</dt> <dt>

[<span data-ttu-id="6f1fb-126">**Texture3D**</span><span class="sxs-lookup"><span data-stu-id="6f1fb-126">**Texture3D**</span></span>](sm5-object-texture3d.md)
</dt> </dl>

 

 
