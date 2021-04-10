---
description: Ottiene la descrizione della traccia.
ms.assetid: 7663a26f-5ad3-4a17-a502-c0dcfa730db2
title: 'Metodo ID3DXAnimationController:: GetTrackDesc (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetTrackDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 940b43ede480766155d09ebe51dfb55eba114c50
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762155"
---
# <a name="id3dxanimationcontrollergettrackdesc-method"></a><span data-ttu-id="99ea5-103">Metodo ID3DXAnimationController:: GetTrackDesc</span><span class="sxs-lookup"><span data-stu-id="99ea5-103">ID3DXAnimationController::GetTrackDesc method</span></span>

<span data-ttu-id="99ea5-104">Ottiene la descrizione della traccia.</span><span class="sxs-lookup"><span data-stu-id="99ea5-104">Gets the track description.</span></span>

## <a name="syntax"></a><span data-ttu-id="99ea5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="99ea5-105">Syntax</span></span>


```C++
HRESULT GetTrackDesc(
  [in]  UINT             Track,
  [out] LPD3DXTRACK_DESC pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="99ea5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="99ea5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99ea5-107">*Traccia* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="99ea5-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99ea5-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="99ea5-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="99ea5-109">Identificatore di traccia.</span><span class="sxs-lookup"><span data-stu-id="99ea5-109">Track identifier.</span></span>

</dd> <dt>

<span data-ttu-id="99ea5-110">*pDesc* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="99ea5-110">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="99ea5-111">Tipo: **[ **LPD3DXTRACK \_ desc**](d3dxtrack-desc.md)**</span><span class="sxs-lookup"><span data-stu-id="99ea5-111">Type: **[**LPD3DXTRACK\_DESC**](d3dxtrack-desc.md)**</span></span>

<span data-ttu-id="99ea5-112">Puntatore alla descrizione della traccia.</span><span class="sxs-lookup"><span data-stu-id="99ea5-112">Pointer to the track description.</span></span> <span data-ttu-id="99ea5-113">Vedere [**D3DXTRACK \_ desc**](d3dxtrack-desc.md).</span><span class="sxs-lookup"><span data-stu-id="99ea5-113">See [**D3DXTRACK\_DESC**](d3dxtrack-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99ea5-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="99ea5-114">Return value</span></span>

<span data-ttu-id="99ea5-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="99ea5-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="99ea5-116">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="99ea5-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="99ea5-117">Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="99ea5-117">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="99ea5-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="99ea5-118">Requirements</span></span>



| <span data-ttu-id="99ea5-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="99ea5-119">Requirement</span></span> | <span data-ttu-id="99ea5-120">Valore</span><span class="sxs-lookup"><span data-stu-id="99ea5-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="99ea5-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="99ea5-121">Header</span></span><br/>  | <dl> <span data-ttu-id="99ea5-122"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="99ea5-122"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="99ea5-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="99ea5-123">Library</span></span><br/> | <dl> <span data-ttu-id="99ea5-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="99ea5-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="99ea5-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="99ea5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99ea5-126">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="99ea5-126">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
