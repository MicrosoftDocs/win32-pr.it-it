---
description: Imposta una chiave evento che modifica la frequenza di riproduzione di una traccia di animazione.
ms.assetid: 217d3a2d-0fb7-4995-86ec-7a4e8420e338
title: 'Metodo ID3DXAnimationController:: KeyTrackSpeed (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackSpeed
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 09705dd03e7767e94b1508cf4951186a509a3c5b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323643"
---
# <a name="id3dxanimationcontrollerkeytrackspeed-method"></a><span data-ttu-id="999d3-103">Metodo ID3DXAnimationController:: KeyTrackSpeed</span><span class="sxs-lookup"><span data-stu-id="999d3-103">ID3DXAnimationController::KeyTrackSpeed method</span></span>

<span data-ttu-id="999d3-104">Imposta una chiave evento che modifica la frequenza di riproduzione di una traccia di animazione.</span><span class="sxs-lookup"><span data-stu-id="999d3-104">Sets an event key that changes the rate of play of an animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="999d3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="999d3-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE KeyTrackSpeed(
  [in] UINT                Track,
  [in] FLOAT               NewSpeed,
  [in] DOUBLE              StartTime,
  [in] DOUBLE              Duration,
  [in] D3DXTRANSITION_TYPE Transition
);
```



## <a name="parameters"></a><span data-ttu-id="999d3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="999d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="999d3-107">*Traccia* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="999d3-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="999d3-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="999d3-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="999d3-109">Identificatore della traccia da modificare.</span><span class="sxs-lookup"><span data-stu-id="999d3-109">Identifier of the track to modify.</span></span>

</dd> <dt>

<span data-ttu-id="999d3-110">*NewSpeed* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="999d3-110">*NewSpeed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="999d3-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="999d3-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="999d3-112">Nuova velocità della traccia dell'animazione.</span><span class="sxs-lookup"><span data-stu-id="999d3-112">New speed of the animation track.</span></span>

</dd> <dt>

<span data-ttu-id="999d3-113">*StartTime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="999d3-113">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="999d3-114">Tipo: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="999d3-114">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="999d3-115">Chiave temporale globale.</span><span class="sxs-lookup"><span data-stu-id="999d3-115">Global time key.</span></span> <span data-ttu-id="999d3-116">Specifica l'ora globale in cui verrà eseguita la modifica.</span><span class="sxs-lookup"><span data-stu-id="999d3-116">Specifies the global time when the change will take place.</span></span>

</dd> <dt>

<span data-ttu-id="999d3-117">*Durata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="999d3-117">*Duration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="999d3-118">Tipo: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="999d3-118">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="999d3-119">Tempo di transizione, che specifica il tempo necessario per il completamento della transizione senza problemi.</span><span class="sxs-lookup"><span data-stu-id="999d3-119">Transition time, which specifies how long the smooth transition will take to complete.</span></span>

</dd> <dt>

<span data-ttu-id="999d3-120">*Transizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="999d3-120">*Transition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="999d3-121">Tipo: **[ **D3DXTRANSITION \_**](./d3dxtransition-type.md)**</span><span class="sxs-lookup"><span data-stu-id="999d3-121">Type: **[**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md)**</span></span>

<span data-ttu-id="999d3-122">Specifica il tipo di transizione utilizzato per la transizione tra le velocità.</span><span class="sxs-lookup"><span data-stu-id="999d3-122">Specifies the transition type used for transitioning between speeds.</span></span> <span data-ttu-id="999d3-123">Vedere [**D3DXTRANSITION \_ Type**](./d3dxtransition-type.md).</span><span class="sxs-lookup"><span data-stu-id="999d3-123">See [**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="999d3-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="999d3-124">Return value</span></span>

<span data-ttu-id="999d3-125">Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="999d3-125">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="999d3-126">Handle di evento per l'evento di combinazione di priorità.</span><span class="sxs-lookup"><span data-stu-id="999d3-126">Event handle to the priority blend event.</span></span> <span data-ttu-id="999d3-127">Se uno o più parametri di input non sono validi oppure non è disponibile alcun evento libero, viene restituito **null** .</span><span class="sxs-lookup"><span data-stu-id="999d3-127">**NULL** is returned if one or more of the input parameters is invalid, or no free event is available.</span></span>

## <a name="requirements"></a><span data-ttu-id="999d3-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="999d3-128">Requirements</span></span>



| <span data-ttu-id="999d3-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="999d3-129">Requirement</span></span> | <span data-ttu-id="999d3-130">Valore</span><span class="sxs-lookup"><span data-stu-id="999d3-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="999d3-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="999d3-131">Header</span></span><br/>  | <dl> <span data-ttu-id="999d3-132"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="999d3-132"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="999d3-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="999d3-133">Library</span></span><br/> | <dl> <span data-ttu-id="999d3-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="999d3-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="999d3-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="999d3-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="999d3-136">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="999d3-136">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
