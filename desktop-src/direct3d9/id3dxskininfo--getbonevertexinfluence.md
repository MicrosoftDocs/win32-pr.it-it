---
description: Recupera il fattore di fusione e il vertice interessati da un'influenza dell'osso specificata.
ms.assetid: bbed4766-e571-4a9e-b7e3-047052470cbe
title: 'Metodo ID3DXSkinInfo:: GetBoneVertexInfluence (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetBoneVertexInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6e3cb7c530ed72a65f9a3e8de6b0735b1a7ae5e4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354074"
---
# <a name="id3dxskininfogetbonevertexinfluence-method"></a><span data-ttu-id="12f4c-103">Metodo ID3DXSkinInfo:: GetBoneVertexInfluence</span><span class="sxs-lookup"><span data-stu-id="12f4c-103">ID3DXSkinInfo::GetBoneVertexInfluence method</span></span>

<span data-ttu-id="12f4c-104">Recupera il fattore di fusione e il vertice interessati da un'influenza dell'osso specificata.</span><span class="sxs-lookup"><span data-stu-id="12f4c-104">Retrieves the blend factor and vertex affected by a specified bone influence.</span></span>

## <a name="syntax"></a><span data-ttu-id="12f4c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="12f4c-105">Syntax</span></span>


```C++
HRESULT GetBoneVertexInfluence(
  [in]      DWORD boneNum,
  [in]      DWORD influenceNum,
  [in, out] FLOAT *pWeight,
  [in, out] DWORD *pVertexNum
);
```



## <a name="parameters"></a><span data-ttu-id="12f4c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="12f4c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12f4c-107">*boneNum* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="12f4c-107">*boneNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12f4c-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="12f4c-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="12f4c-109">Indice dell'osso.</span><span class="sxs-lookup"><span data-stu-id="12f4c-109">Index of the bone.</span></span> <span data-ttu-id="12f4c-110">Deve essere compreso tra 0 e il numero di ossa.</span><span class="sxs-lookup"><span data-stu-id="12f4c-110">Must be between 0 and the number of bones.</span></span>

</dd> <dt>

<span data-ttu-id="12f4c-111">*influenceNum* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="12f4c-111">*influenceNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12f4c-112">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="12f4c-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="12f4c-113">Indice della matrice di influenza dell'osso specificato.</span><span class="sxs-lookup"><span data-stu-id="12f4c-113">Index of the influence array of the specified bone.</span></span>

</dd> <dt>

<span data-ttu-id="12f4c-114">*pWeight* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="12f4c-114">*pWeight* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="12f4c-115">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="12f4c-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="12f4c-116">Puntatore al fattore di Blend influenzato da influenceNum.</span><span class="sxs-lookup"><span data-stu-id="12f4c-116">Pointer to the blend factor influenced by influenceNum.</span></span>

</dd> <dt>

<span data-ttu-id="12f4c-117">*pVertexNum* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="12f4c-117">*pVertexNum* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="12f4c-118">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="12f4c-118">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="12f4c-119">Puntatore al vertice influenzato da influenceNum.</span><span class="sxs-lookup"><span data-stu-id="12f4c-119">Pointer to the vertex influenced by influenceNum.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12f4c-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="12f4c-120">Return value</span></span>

<span data-ttu-id="12f4c-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="12f4c-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="12f4c-122">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="12f4c-122">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="12f4c-123">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="12f4c-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="12f4c-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="12f4c-124">Requirements</span></span>



| <span data-ttu-id="12f4c-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="12f4c-125">Requirement</span></span> | <span data-ttu-id="12f4c-126">Valore</span><span class="sxs-lookup"><span data-stu-id="12f4c-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="12f4c-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="12f4c-127">Header</span></span><br/>  | <dl> <span data-ttu-id="12f4c-128"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="12f4c-128"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="12f4c-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="12f4c-129">Library</span></span><br/> | <dl> <span data-ttu-id="12f4c-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="12f4c-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="12f4c-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="12f4c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12f4c-132">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="12f4c-132">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="12f4c-133">**ID3DXSkinInfo::SetBoneVertexInfluence**</span><span class="sxs-lookup"><span data-stu-id="12f4c-133">**ID3DXSkinInfo::SetBoneVertexInfluence**</span></span>](id3dxskininfo--setbonevertexinfluence.md)
</dt> <dt>

[<span data-ttu-id="12f4c-134">**ID3DXSkinInfo::FindBoneVertexInfluenceIndex**</span><span class="sxs-lookup"><span data-stu-id="12f4c-134">**ID3DXSkinInfo::FindBoneVertexInfluenceIndex**</span></span>](id3dxskininfo--findbonevertexinfluenceindex.md)
</dt> <dt>

[<span data-ttu-id="12f4c-135">**ID3DXSkinInfo::GetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="12f4c-135">**ID3DXSkinInfo::GetBoneInfluence**</span></span>](id3dxskininfo--getboneinfluence.md)
</dt> </dl>

 

 
