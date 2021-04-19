---
description: Ottiene i vertici e i pesi influenzati da un osso.
ms.assetid: 84cb064b-b6b2-402d-81cc-8c02de6f8b52
title: 'Metodo ID3DXSkinInfo:: GetBoneInfluence (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetBoneInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8b4b31ab08aca476ced1cb28dfc5ed5bfe61d044
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322066"
---
# <a name="id3dxskininfogetboneinfluence-method"></a><span data-ttu-id="27c94-103">Metodo ID3DXSkinInfo:: GetBoneInfluence</span><span class="sxs-lookup"><span data-stu-id="27c94-103">ID3DXSkinInfo::GetBoneInfluence method</span></span>

<span data-ttu-id="27c94-104">Ottiene i vertici e i pesi influenzati da un osso.</span><span class="sxs-lookup"><span data-stu-id="27c94-104">Gets the vertices and weights that a bone influences.</span></span>

## <a name="syntax"></a><span data-ttu-id="27c94-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="27c94-105">Syntax</span></span>


```C++
HRESULT GetBoneInfluence(
  [in]      DWORD Bone,
  [in, out] DWORD *vertices,
  [in, out] FLOAT *weights
);
```



## <a name="parameters"></a><span data-ttu-id="27c94-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="27c94-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27c94-107">*Osso* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="27c94-107">*Bone* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27c94-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="27c94-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="27c94-109">Numero osso.</span><span class="sxs-lookup"><span data-stu-id="27c94-109">Bone number.</span></span>

</dd> <dt>

<span data-ttu-id="27c94-110">*vertici* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="27c94-110">*vertices* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="27c94-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="27c94-111">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="27c94-112">Ottenere la matrice di vertici influenzato da un osso.</span><span class="sxs-lookup"><span data-stu-id="27c94-112">Get the array of vertices influenced by a bone.</span></span>

</dd> <dt>

<span data-ttu-id="27c94-113">*pesi* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="27c94-113">*weights* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="27c94-114">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="27c94-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="27c94-115">Ottenere la matrice di pesi influenzata da un osso.</span><span class="sxs-lookup"><span data-stu-id="27c94-115">Get the array of weights influenced by a bone.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27c94-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="27c94-116">Return value</span></span>

<span data-ttu-id="27c94-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="27c94-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="27c94-118">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="27c94-118">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="27c94-119">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="27c94-119">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="27c94-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="27c94-120">Remarks</span></span>

<span data-ttu-id="27c94-121">Usare [**ID3DXSkinInfo:: GetNumBoneInfluences**](id3dxskininfo--getnumboneinfluences.md) per determinare il numero di vertici influenzati dall'osso.</span><span class="sxs-lookup"><span data-stu-id="27c94-121">Use [**ID3DXSkinInfo::GetNumBoneInfluences**](id3dxskininfo--getnumboneinfluences.md) to find out how many vertices the bone influences.</span></span>

## <a name="requirements"></a><span data-ttu-id="27c94-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="27c94-122">Requirements</span></span>



| <span data-ttu-id="27c94-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="27c94-123">Requirement</span></span> | <span data-ttu-id="27c94-124">Valore</span><span class="sxs-lookup"><span data-stu-id="27c94-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="27c94-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="27c94-125">Header</span></span><br/>  | <dl> <span data-ttu-id="27c94-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="27c94-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="27c94-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="27c94-127">Library</span></span><br/> | <dl> <span data-ttu-id="27c94-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="27c94-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="27c94-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="27c94-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27c94-130">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="27c94-130">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="27c94-131">**ID3DXSkinInfo::SetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="27c94-131">**ID3DXSkinInfo::SetBoneInfluence**</span></span>](id3dxskininfo--setboneinfluence.md)
</dt> </dl>

 

 
