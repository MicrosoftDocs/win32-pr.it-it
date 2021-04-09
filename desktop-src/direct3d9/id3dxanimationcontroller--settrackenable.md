---
description: Abilita o Disabilita una traccia nel controller animazione.
ms.assetid: 8d06287b-e076-4553-962c-5c423e355101
title: 'Metodo ID3DXAnimationController:: SetTrackEnable (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackEnable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 920576cbf630e061cd4d460315e905bdabf31ff5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058660"
---
# <a name="id3dxanimationcontrollersettrackenable-method"></a><span data-ttu-id="773e3-103">Metodo ID3DXAnimationController:: SetTrackEnable</span><span class="sxs-lookup"><span data-stu-id="773e3-103">ID3DXAnimationController::SetTrackEnable method</span></span>

<span data-ttu-id="773e3-104">Abilita o Disabilita una traccia nel controller animazione.</span><span class="sxs-lookup"><span data-stu-id="773e3-104">Enables or disables a track in the animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="773e3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="773e3-105">Syntax</span></span>


```C++
HRESULT SetTrackEnable(
  [in] UINT Track,
  [in] BOOL Enable
);
```



## <a name="parameters"></a><span data-ttu-id="773e3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="773e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="773e3-107">*Traccia* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="773e3-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="773e3-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="773e3-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="773e3-109">Identificatore della traccia da combinare.</span><span class="sxs-lookup"><span data-stu-id="773e3-109">Identifier of the track to be mixed.</span></span>

</dd> <dt>

<span data-ttu-id="773e3-110">*Abilita* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="773e3-110">*Enable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="773e3-111">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="773e3-111">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="773e3-112">Abilita valore.</span><span class="sxs-lookup"><span data-stu-id="773e3-112">Enable value.</span></span> <span data-ttu-id="773e3-113">Impostare su **true** per abilitare questa traccia nel controller oppure su **false** per impedire che venga mescolata.</span><span class="sxs-lookup"><span data-stu-id="773e3-113">Set to **TRUE** to enable this track in the controller, or to **FALSE** to prevent it from being mixed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="773e3-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="773e3-114">Return value</span></span>

<span data-ttu-id="773e3-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="773e3-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="773e3-116">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="773e3-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="773e3-117">Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="773e3-117">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="773e3-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="773e3-118">Remarks</span></span>

<span data-ttu-id="773e3-119">Per combinare una traccia con altre tracce, il flag di abilitazione deve essere impostato su **true**.</span><span class="sxs-lookup"><span data-stu-id="773e3-119">To mix a track with other tracks, the Enable flag must be set to **TRUE**.</span></span> <span data-ttu-id="773e3-120">Viceversa, se si imposta il flag su **false** , la traccia non verrà mescolata con altre tracce.</span><span class="sxs-lookup"><span data-stu-id="773e3-120">Conversely, setting the flag to **FALSE** will prevent the track from being mixed with other tracks.</span></span>

## <a name="requirements"></a><span data-ttu-id="773e3-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="773e3-121">Requirements</span></span>



| <span data-ttu-id="773e3-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="773e3-122">Requirement</span></span> | <span data-ttu-id="773e3-123">Valore</span><span class="sxs-lookup"><span data-stu-id="773e3-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="773e3-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="773e3-124">Header</span></span><br/>  | <dl> <span data-ttu-id="773e3-125"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="773e3-125"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="773e3-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="773e3-126">Library</span></span><br/> | <dl> <span data-ttu-id="773e3-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="773e3-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="773e3-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="773e3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="773e3-129">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="773e3-129">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
