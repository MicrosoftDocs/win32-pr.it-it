---
title: 'Funzione Texture2DMS:: Load (int, int, int, uint)'
description: "Legge i dati della trama e restituisce lo stato dell'operazione. | Funzione Texture2DMS:: Load (int, int, int, uint)"
ms.assetid: 4230962C-2968-4030-9770-8318F1760AEB
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
ms.openlocfilehash: e967d69929c0b20317ffb74fc97c4e60e36c2854
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352071"
---
# <a name="texture2dmsloadintintintuint-function"></a><span data-ttu-id="a3085-105">Funzione Texture2DMS:: Load (int, int, int, uint)</span><span class="sxs-lookup"><span data-stu-id="a3085-105">Texture2DMS::Load(int,int,int,uint) function</span></span>

<span data-ttu-id="a3085-106">Legge i dati della trama e restituisce lo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="a3085-106">Reads texture data and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3085-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a3085-107">Syntax</span></span>


``` syntax
 Load(
  in  int2 Location,
  in  int  sampleindex,
  in  int2 Offset,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="a3085-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a3085-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3085-109">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3085-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3085-110">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="a3085-110">Type: **int2**</span></span>

<span data-ttu-id="a3085-111">Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="a3085-111">The texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="a3085-112">*sampleindex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3085-112">*sampleindex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3085-113">Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a3085-113">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a3085-114">Indice di esempio.</span><span class="sxs-lookup"><span data-stu-id="a3085-114">The sample index.</span></span>

</dd> <dt>

<span data-ttu-id="a3085-115">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3085-115">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3085-116">Tipo: **int2**</span><span class="sxs-lookup"><span data-stu-id="a3085-116">Type: **int2**</span></span>

<span data-ttu-id="a3085-117">Offset applicato alle coordinate di trama prima del caricamento.</span><span class="sxs-lookup"><span data-stu-id="a3085-117">An offset applied to the texture coordinates before loading.</span></span>

</dd> <dt>

<span data-ttu-id="a3085-118">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="a3085-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3085-119">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="a3085-119">Type: **uint**</span></span>

<span data-ttu-id="a3085-120">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="a3085-120">The status of the operation.</span></span> <span data-ttu-id="a3085-121">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="a3085-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="a3085-122">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="a3085-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="a3085-123">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="a3085-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3085-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a3085-124">Return value</span></span>

<span data-ttu-id="a3085-125">Digitare:</span><span class="sxs-lookup"><span data-stu-id="a3085-125">Type:</span></span>

<span data-ttu-id="a3085-126">Il tipo restituito corrisponde al tipo nella dichiarazione per l'oggetto [**Texture2DMS**](sm5-object-texture2dms.md) .</span><span class="sxs-lookup"><span data-stu-id="a3085-126">The return type matches the type in the declaration for the [**Texture2DMS**](sm5-object-texture2dms.md) object.</span></span>

## <a name="see-also"></a><span data-ttu-id="a3085-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a3085-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3085-128">Metodi Load</span><span class="sxs-lookup"><span data-stu-id="a3085-128">Load methods</span></span>](texture2dms-load.md)
</dt> <dt>

[<span data-ttu-id="a3085-129">**Texture2DMS**</span><span class="sxs-lookup"><span data-stu-id="a3085-129">**Texture2DMS**</span></span>](sm5-object-texture2dms.md)
</dt> </dl>

 

 
