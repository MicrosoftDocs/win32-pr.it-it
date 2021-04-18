---
description: Imposta un valore di influenza di un osso in un singolo vertice.
ms.assetid: 9283866f-3dfe-467d-a74f-77e89c2778c4
title: 'Metodo ID3DXSkinInfo:: SetBoneVertexInfluence (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetBoneVertexInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: db84cdf9a1647bc5302c421e52d50f812e74596e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322052"
---
# <a name="id3dxskininfosetbonevertexinfluence-method"></a><span data-ttu-id="efb08-103">Metodo ID3DXSkinInfo:: SetBoneVertexInfluence</span><span class="sxs-lookup"><span data-stu-id="efb08-103">ID3DXSkinInfo::SetBoneVertexInfluence method</span></span>

<span data-ttu-id="efb08-104">Imposta un valore di influenza di un osso in un singolo vertice.</span><span class="sxs-lookup"><span data-stu-id="efb08-104">Sets an influence value of a bone on a single vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="efb08-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="efb08-105">Syntax</span></span>


```C++
HRESULT SetBoneVertexInfluence(
  [in] DWORD boneNum,
  [in] DWORD influenceNum,
  [in] FLOAT weight
);
```



## <a name="parameters"></a><span data-ttu-id="efb08-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="efb08-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efb08-107">*boneNum* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="efb08-107">*boneNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efb08-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="efb08-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="efb08-109">Indice dell'osso.</span><span class="sxs-lookup"><span data-stu-id="efb08-109">Index of the bone.</span></span> <span data-ttu-id="efb08-110">Deve essere compreso tra 0 e il numero di ossa.</span><span class="sxs-lookup"><span data-stu-id="efb08-110">Must be between 0 and the number of bones.</span></span>

</dd> <dt>

<span data-ttu-id="efb08-111">*influenceNum* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="efb08-111">*influenceNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efb08-112">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="efb08-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="efb08-113">Indice della matrice di influenza dell'osso specificato.</span><span class="sxs-lookup"><span data-stu-id="efb08-113">Index of the influence array of the specified bone.</span></span>

</dd> <dt>

<span data-ttu-id="efb08-114">*peso* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="efb08-114">*weight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efb08-115">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="efb08-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="efb08-116">Fattore di fusione dell'influenza dell'osso specificata.</span><span class="sxs-lookup"><span data-stu-id="efb08-116">Blend factor of the specified bone influence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efb08-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="efb08-117">Return value</span></span>

<span data-ttu-id="efb08-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="efb08-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="efb08-119">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="efb08-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="efb08-120">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="efb08-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="efb08-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="efb08-121">Requirements</span></span>



| <span data-ttu-id="efb08-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="efb08-122">Requirement</span></span> | <span data-ttu-id="efb08-123">Valore</span><span class="sxs-lookup"><span data-stu-id="efb08-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="efb08-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="efb08-124">Header</span></span><br/>  | <dl> <span data-ttu-id="efb08-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="efb08-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="efb08-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="efb08-126">Library</span></span><br/> | <dl> <span data-ttu-id="efb08-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="efb08-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="efb08-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="efb08-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efb08-129">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="efb08-129">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="efb08-130">**ID3DXSkinInfo::GetBoneVertexInfluence**</span><span class="sxs-lookup"><span data-stu-id="efb08-130">**ID3DXSkinInfo::GetBoneVertexInfluence**</span></span>](id3dxskininfo--getbonevertexinfluence.md)
</dt> <dt>

[<span data-ttu-id="efb08-131">**ID3DXSkinInfo::FindBoneVertexInfluenceIndex**</span><span class="sxs-lookup"><span data-stu-id="efb08-131">**ID3DXSkinInfo::FindBoneVertexInfluenceIndex**</span></span>](id3dxskininfo--findbonevertexinfluenceindex.md)
</dt> <dt>

[<span data-ttu-id="efb08-132">**ID3DXSkinInfo::GetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="efb08-132">**ID3DXSkinInfo::GetBoneInfluence**</span></span>](id3dxskininfo--getboneinfluence.md)
</dt> </dl>

 

 
