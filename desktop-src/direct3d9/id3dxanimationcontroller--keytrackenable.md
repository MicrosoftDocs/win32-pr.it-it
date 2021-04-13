---
description: Imposta una chiave evento che Abilita o Disabilita una traccia dell'animazione.
ms.assetid: de81e646-0b94-40d3-89c2-060d118d17b2
title: 'Metodo ID3DXAnimationController:: KeyTrackEnable (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackEnable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f22c732ff57e948ebcc2e89d790d352e4dc057ba
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354254"
---
# <a name="id3dxanimationcontrollerkeytrackenable-method"></a><span data-ttu-id="7b3be-103">Metodo ID3DXAnimationController:: KeyTrackEnable</span><span class="sxs-lookup"><span data-stu-id="7b3be-103">ID3DXAnimationController::KeyTrackEnable method</span></span>

<span data-ttu-id="7b3be-104">Imposta una chiave evento che Abilita o Disabilita una traccia dell'animazione.</span><span class="sxs-lookup"><span data-stu-id="7b3be-104">Sets an event key that enables or disables an animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b3be-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7b3be-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE KeyTrackEnable(
  [in] UINT   Track,
  [in] BOOL   NewEnable,
  [in] DOUBLE StartTime
);
```



## <a name="parameters"></a><span data-ttu-id="7b3be-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7b3be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b3be-107">*Traccia* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b3be-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b3be-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7b3be-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7b3be-109">Identificatore della traccia dell'animazione da modificare.</span><span class="sxs-lookup"><span data-stu-id="7b3be-109">Identifier of the animation track to modify.</span></span>

</dd> <dt>

<span data-ttu-id="7b3be-110">*NewEnable* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b3be-110">*NewEnable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b3be-111">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7b3be-111">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7b3be-112">Abilita flag.</span><span class="sxs-lookup"><span data-stu-id="7b3be-112">Enable flag.</span></span> <span data-ttu-id="7b3be-113">Impostare su **true** per abilitare la traccia dell'animazione oppure su **false** per disabilitare la traccia.</span><span class="sxs-lookup"><span data-stu-id="7b3be-113">Set this to **TRUE** to enable the animation track, or to **FALSE** to disable the track.</span></span>

</dd> <dt>

<span data-ttu-id="7b3be-114">*StartTime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b3be-114">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b3be-115">Tipo: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7b3be-115">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7b3be-116">Chiave temporale globale.</span><span class="sxs-lookup"><span data-stu-id="7b3be-116">Global time key.</span></span> <span data-ttu-id="7b3be-117">Specifica l'ora globale in cui verrà eseguita la modifica.</span><span class="sxs-lookup"><span data-stu-id="7b3be-117">Specifies the global time when the change will take place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b3be-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7b3be-118">Return value</span></span>

<span data-ttu-id="7b3be-119">Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="7b3be-119">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="7b3be-120">Handle di evento per l'evento di combinazione di priorità.</span><span class="sxs-lookup"><span data-stu-id="7b3be-120">Event handle to the priority blend event.</span></span> <span data-ttu-id="7b3be-121">Se Track non è valido, viene restituito **null** .</span><span class="sxs-lookup"><span data-stu-id="7b3be-121">**NULL** is returned if Track is invalid.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b3be-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7b3be-122">Requirements</span></span>



| <span data-ttu-id="7b3be-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b3be-123">Requirement</span></span> | <span data-ttu-id="7b3be-124">Valore</span><span class="sxs-lookup"><span data-stu-id="7b3be-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b3be-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7b3be-125">Header</span></span><br/>  | <dl> <span data-ttu-id="7b3be-126"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b3be-126"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="7b3be-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="7b3be-127">Library</span></span><br/> | <dl> <span data-ttu-id="7b3be-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7b3be-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7b3be-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7b3be-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b3be-130">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="7b3be-130">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
