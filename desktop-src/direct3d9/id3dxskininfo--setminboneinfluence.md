---
description: Imposta l'influenza dell'osso minima. I valori più piccoli di quelli che vengono ignorati.
ms.assetid: 9af19c9e-bb6e-4f93-973f-5c38f88eea3d
title: 'Metodo ID3DXSkinInfo:: SetMinBoneInfluence (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetMinBoneInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 03e3aeeed31a58231644784ba5070bc9422f7820
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322050"
---
# <a name="id3dxskininfosetminboneinfluence-method"></a><span data-ttu-id="30224-104">Metodo ID3DXSkinInfo:: SetMinBoneInfluence</span><span class="sxs-lookup"><span data-stu-id="30224-104">ID3DXSkinInfo::SetMinBoneInfluence method</span></span>

<span data-ttu-id="30224-105">Imposta l'influenza dell'osso minima.</span><span class="sxs-lookup"><span data-stu-id="30224-105">Sets the minimum bone influence.</span></span> <span data-ttu-id="30224-106">I valori più piccoli di quelli che vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="30224-106">Influence values smaller than this are ignored.</span></span>

## <a name="syntax"></a><span data-ttu-id="30224-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="30224-107">Syntax</span></span>


```C++
HRESULT SetMinBoneInfluence(
  [in] FLOAT MinInfl
);
```



## <a name="parameters"></a><span data-ttu-id="30224-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="30224-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30224-109">*MinInfl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30224-109">*MinInfl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30224-110">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="30224-110">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="30224-111">Valore di influenza minima.</span><span class="sxs-lookup"><span data-stu-id="30224-111">Minimum influence value.</span></span> <span data-ttu-id="30224-112">I valori più piccoli di quelli che vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="30224-112">Influence values smaller than this are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30224-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="30224-113">Return value</span></span>

<span data-ttu-id="30224-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="30224-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="30224-115">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="30224-115">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="30224-116">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="30224-116">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="30224-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="30224-117">Requirements</span></span>



| <span data-ttu-id="30224-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="30224-118">Requirement</span></span> | <span data-ttu-id="30224-119">Valore</span><span class="sxs-lookup"><span data-stu-id="30224-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="30224-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="30224-120">Header</span></span><br/>  | <dl> <span data-ttu-id="30224-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="30224-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="30224-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="30224-122">Library</span></span><br/> | <dl> <span data-ttu-id="30224-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="30224-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="30224-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="30224-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30224-125">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="30224-125">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="30224-126">**ID3DXSkinInfo::GetMinBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="30224-126">**ID3DXSkinInfo::GetMinBoneInfluence**</span></span>](id3dxskininfo--getminboneinfluence.md)
</dt> </dl>

 

 
