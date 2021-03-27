---
title: 'Funzione Texture2DMSArray:: Load (int, int, int, uint)'
description: "Legge i dati della trama e restituisce lo stato dell'operazione. | Funzione Texture2DMSArray:: Load (int, int, int, uint)"
ms.assetid: F5EA2FFF-7E43-4A34-9358-EA54382641DC
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
ms.openlocfilehash: 0065ee5e420c67876b87c67be1f5e5c8ff10e65b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995349"
---
# <a name="texture2dmsarrayloadintintintuint-function"></a><span data-ttu-id="6ef75-105">Funzione Texture2DMSArray:: Load (int, int, int, uint)</span><span class="sxs-lookup"><span data-stu-id="6ef75-105">Texture2DMSArray::Load(int,int,int,uint) function</span></span>

<span data-ttu-id="6ef75-106">Legge i dati della trama e restituisce lo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="6ef75-106">Reads texture data and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ef75-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6ef75-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  in  int  sampleindex,
  in  int  Offset,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="6ef75-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6ef75-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ef75-109">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6ef75-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ef75-110">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="6ef75-110">Type: **int**</span></span>

<span data-ttu-id="6ef75-111">Coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="6ef75-111">The texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="6ef75-112">*sampleindex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6ef75-112">*sampleindex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ef75-113">Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6ef75-113">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="6ef75-114">Indice di esempio.</span><span class="sxs-lookup"><span data-stu-id="6ef75-114">The sample index.</span></span>

</dd> <dt>

<span data-ttu-id="6ef75-115">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6ef75-115">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ef75-116">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="6ef75-116">Type: **int**</span></span>

<span data-ttu-id="6ef75-117">Offset applicato alle coordinate di trama prima del campionamento.</span><span class="sxs-lookup"><span data-stu-id="6ef75-117">An offset applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="6ef75-118">*Stato* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="6ef75-118">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ef75-119">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="6ef75-119">Type: **uint**</span></span>

<span data-ttu-id="6ef75-120">Stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="6ef75-120">The status of the operation.</span></span> <span data-ttu-id="6ef75-121">Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="6ef75-121">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="6ef75-122">**CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="6ef75-122">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="6ef75-123">Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="6ef75-123">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ef75-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6ef75-124">Return value</span></span>

<span data-ttu-id="6ef75-125">Digitare:</span><span class="sxs-lookup"><span data-stu-id="6ef75-125">Type:</span></span>

<span data-ttu-id="6ef75-126">Il tipo restituito corrisponde al tipo nella dichiarazione per l'oggetto [**Texture2DMSArray**](sm5-object-texture2dmsarray.md) .</span><span class="sxs-lookup"><span data-stu-id="6ef75-126">The return type matches the type in the declaration for the [**Texture2DMSArray**](sm5-object-texture2dmsarray.md) object.</span></span>

## <a name="see-also"></a><span data-ttu-id="6ef75-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6ef75-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ef75-128">Metodi Load</span><span class="sxs-lookup"><span data-stu-id="6ef75-128">Load methods</span></span>](texture2dmsarray-load.md)
</dt> <dt>

[<span data-ttu-id="6ef75-129">**Texture2DMSArray**</span><span class="sxs-lookup"><span data-stu-id="6ef75-129">**Texture2DMSArray**</span></span>](sm5-object-texture2dmsarray.md)
</dt> </dl>

 

 
