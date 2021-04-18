---
description: Recupera l'indice dell'influenza ossea che interessa un singolo vertice.
ms.assetid: vs|directx_sdk|~\id3dxskininfo__findbonevertexinfluenceindex.htm
title: 'Metodo ID3DXSkinInfo:: FindBoneVertexInfluenceIndex (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.FindBoneVertexInfluenceIndex
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 05a86e98e5001092700fdec12f2a7afc33ddf082
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322067"
---
# <a name="id3dxskininfofindbonevertexinfluenceindex-method"></a><span data-ttu-id="c4044-103">Metodo ID3DXSkinInfo:: FindBoneVertexInfluenceIndex</span><span class="sxs-lookup"><span data-stu-id="c4044-103">ID3DXSkinInfo::FindBoneVertexInfluenceIndex method</span></span>

<span data-ttu-id="c4044-104">Recupera l'indice dell'influenza ossea che interessa un singolo vertice.</span><span class="sxs-lookup"><span data-stu-id="c4044-104">Retrieves the index of the bone influence affecting a single vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4044-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c4044-105">Syntax</span></span>


```C++
HRESULT FindBoneVertexInfluenceIndex(
  [in]      DWORD boneNum,
  [in]      DWORD vertexNum,
  [in, out] DWORD *pInfluenceIndex
);
```



## <a name="parameters"></a><span data-ttu-id="c4044-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c4044-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4044-107">*boneNum* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4044-107">*boneNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4044-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c4044-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c4044-109">Indice dell'osso.</span><span class="sxs-lookup"><span data-stu-id="c4044-109">Index of the bone.</span></span> <span data-ttu-id="c4044-110">Deve essere compreso tra 0 e il numero di ossa.</span><span class="sxs-lookup"><span data-stu-id="c4044-110">Must be between 0 and the number of bones.</span></span>

</dd> <dt>

<span data-ttu-id="c4044-111">*vertexNum* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4044-111">*vertexNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4044-112">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c4044-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c4044-113">Indice del vertice per il quale è necessario trovare l'influenza dell'osso.</span><span class="sxs-lookup"><span data-stu-id="c4044-113">Index of the vertex for which the bone influence is to be found.</span></span> <span data-ttu-id="c4044-114">Deve essere compreso tra 0 e il numero di vertici nella rete.</span><span class="sxs-lookup"><span data-stu-id="c4044-114">Must be between 0 and the number of vertices in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="c4044-115">*pInfluenceIndex* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="c4044-115">*pInfluenceIndex* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c4044-116">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c4044-116">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c4044-117">Puntatore all'indice dell'influenza dell'osso che interessa vertexNum.</span><span class="sxs-lookup"><span data-stu-id="c4044-117">Pointer to the index of the bone influence that affects vertexNum.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4044-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c4044-118">Return value</span></span>

<span data-ttu-id="c4044-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c4044-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c4044-120">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c4044-120">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="c4044-121">Se l'osso specificato non influenza il vertice dato, \_ viene restituito S false.</span><span class="sxs-lookup"><span data-stu-id="c4044-121">If the specified bone does not influence the given vertex, S\_FALSE is returned.</span></span> <span data-ttu-id="c4044-122">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="c4044-122">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4044-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c4044-123">Requirements</span></span>



| <span data-ttu-id="c4044-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4044-124">Requirement</span></span> | <span data-ttu-id="c4044-125">Valore</span><span class="sxs-lookup"><span data-stu-id="c4044-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4044-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c4044-126">Header</span></span><br/>  | <dl> <span data-ttu-id="c4044-127"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4044-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="c4044-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="c4044-128">Library</span></span><br/> | <dl> <span data-ttu-id="c4044-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4044-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c4044-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c4044-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4044-131">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="c4044-131">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="c4044-132">**ID3DXSkinInfo::GetBoneVertexInfluence**</span><span class="sxs-lookup"><span data-stu-id="c4044-132">**ID3DXSkinInfo::GetBoneVertexInfluence**</span></span>](id3dxskininfo--getbonevertexinfluence.md)
</dt> <dt>

[<span data-ttu-id="c4044-133">**ID3DXSkinInfo::SetBoneVertexInfluence**</span><span class="sxs-lookup"><span data-stu-id="c4044-133">**ID3DXSkinInfo::SetBoneVertexInfluence**</span></span>](id3dxskininfo--setbonevertexinfluence.md)
</dt> <dt>

[<span data-ttu-id="c4044-134">**ID3DXSkinInfo::GetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="c4044-134">**ID3DXSkinInfo::GetBoneInfluence**</span></span>](id3dxskininfo--getboneinfluence.md)
</dt> </dl>

 

 
