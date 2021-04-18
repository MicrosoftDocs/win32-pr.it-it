---
description: Rimuove tutti gli eventi da una traccia di animazione specificata.
ms.assetid: 25c4d04a-0d75-4113-ad90-db84aa937098
title: 'Metodo ID3DXAnimationController:: UnkeyAllTrackEvents (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.UnkeyAllTrackEvents
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5904e9e09c8a821cdc532f9046217ae64bbf3de5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323636"
---
# <a name="id3dxanimationcontrollerunkeyalltrackevents-method"></a><span data-ttu-id="55c75-103">Metodo ID3DXAnimationController:: UnkeyAllTrackEvents</span><span class="sxs-lookup"><span data-stu-id="55c75-103">ID3DXAnimationController::UnkeyAllTrackEvents method</span></span>

<span data-ttu-id="55c75-104">Rimuove tutti gli eventi da una traccia di animazione specificata.</span><span class="sxs-lookup"><span data-stu-id="55c75-104">Removes all events from a specified animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="55c75-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="55c75-105">Syntax</span></span>


```C++
HRESULT UnkeyAllTrackEvents(
  [in] UINT Track
);
```



## <a name="parameters"></a><span data-ttu-id="55c75-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="55c75-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55c75-107">*Traccia* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="55c75-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55c75-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="55c75-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="55c75-109">Identificatore della traccia in cui tutti gli eventi devono essere rimossi.</span><span class="sxs-lookup"><span data-stu-id="55c75-109">Identifier of the track on which all events should be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55c75-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="55c75-110">Return value</span></span>

<span data-ttu-id="55c75-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="55c75-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="55c75-112">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="55c75-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="55c75-113">Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="55c75-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="55c75-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="55c75-114">Remarks</span></span>

<span data-ttu-id="55c75-115">Questo metodo impedisce l'esecuzione di tutti gli eventi pianificati in precedenza sulla traccia ed Elimina tutti i dati associati a tali eventi.</span><span class="sxs-lookup"><span data-stu-id="55c75-115">This method prevents the execution of all events previously scheduled on the track, and discards all data associated with those events.</span></span>

## <a name="requirements"></a><span data-ttu-id="55c75-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="55c75-116">Requirements</span></span>



| <span data-ttu-id="55c75-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="55c75-117">Requirement</span></span> | <span data-ttu-id="55c75-118">Valore</span><span class="sxs-lookup"><span data-stu-id="55c75-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="55c75-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="55c75-119">Header</span></span><br/>  | <dl> <span data-ttu-id="55c75-120"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="55c75-120"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="55c75-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="55c75-121">Library</span></span><br/> | <dl> <span data-ttu-id="55c75-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="55c75-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="55c75-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="55c75-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55c75-124">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="55c75-124">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
