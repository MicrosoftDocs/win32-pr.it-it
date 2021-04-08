---
description: Imposta la matrice di offset dell'osso.
ms.assetid: f8ac1117-510d-42af-a6bf-422cbaaf6b74
title: 'Metodo ID3DXSkinInfo:: SetBoneOffsetMatrix (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetBoneOffsetMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 283d36bb68e33cfa0e2349bab304b0cdde7ef77e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103761920"
---
# <a name="id3dxskininfosetboneoffsetmatrix-method"></a><span data-ttu-id="7b299-103">Metodo ID3DXSkinInfo:: SetBoneOffsetMatrix</span><span class="sxs-lookup"><span data-stu-id="7b299-103">ID3DXSkinInfo::SetBoneOffsetMatrix method</span></span>

<span data-ttu-id="7b299-104">Imposta la matrice di offset dell'osso.</span><span class="sxs-lookup"><span data-stu-id="7b299-104">Sets the bone offset matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b299-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7b299-105">Syntax</span></span>


```C++
HRESULT SetBoneOffsetMatrix(
  [in]       DWORD      Bone,
  [in] const D3DXMATRIX *pBoneTransform
);
```



## <a name="parameters"></a><span data-ttu-id="7b299-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7b299-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b299-107">*Osso* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b299-107">*Bone* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b299-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7b299-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7b299-109">Numero osso.</span><span class="sxs-lookup"><span data-stu-id="7b299-109">Bone number.</span></span>

</dd> <dt>

<span data-ttu-id="7b299-110">*pBoneTransform* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b299-110">*pBoneTransform* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b299-111">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="7b299-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="7b299-112">Puntatore alla matrice di offset dell'osso.</span><span class="sxs-lookup"><span data-stu-id="7b299-112">Pointer to the bone offset matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b299-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7b299-113">Return value</span></span>

<span data-ttu-id="7b299-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7b299-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7b299-115">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7b299-115">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7b299-116">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="7b299-116">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b299-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="7b299-117">Remarks</span></span>

<span data-ttu-id="7b299-118">I nomi di osso vengono restituiti da [**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md).</span><span class="sxs-lookup"><span data-stu-id="7b299-118">Bone names are returned by [**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7b299-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7b299-119">Requirements</span></span>



| <span data-ttu-id="7b299-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b299-120">Requirement</span></span> | <span data-ttu-id="7b299-121">Valore</span><span class="sxs-lookup"><span data-stu-id="7b299-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b299-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7b299-122">Header</span></span><br/>  | <dl> <span data-ttu-id="7b299-123"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b299-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="7b299-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="7b299-124">Library</span></span><br/> | <dl> <span data-ttu-id="7b299-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7b299-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7b299-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7b299-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b299-127">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="7b299-127">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="7b299-128">**ID3DXSkinInfo::GetBoneOffsetMatrix**</span><span class="sxs-lookup"><span data-stu-id="7b299-128">**ID3DXSkinInfo::GetBoneOffsetMatrix**</span></span>](id3dxskininfo--getboneoffsetmatrix.md)
</dt> </dl>

 

 
