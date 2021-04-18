---
description: Imposta il valore di influenza per un osso.
ms.assetid: c6dc8a33-8f5c-47d0-8637-a2492b1e3089
title: 'Metodo ID3DXSkinInfo:: SetBoneInfluence (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetBoneInfluence
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 16ed3514c986dee89f964074d18a646bcf3a1249
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322060"
---
# <a name="id3dxskininfosetboneinfluence-method"></a><span data-ttu-id="43a9c-103">Metodo ID3DXSkinInfo:: SetBoneInfluence</span><span class="sxs-lookup"><span data-stu-id="43a9c-103">ID3DXSkinInfo::SetBoneInfluence method</span></span>

<span data-ttu-id="43a9c-104">Imposta il valore di influenza per un osso.</span><span class="sxs-lookup"><span data-stu-id="43a9c-104">Sets the influence value for a bone.</span></span>

## <a name="syntax"></a><span data-ttu-id="43a9c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="43a9c-105">Syntax</span></span>


```C++
HRESULT SetBoneInfluence(
  [in]       DWORD Bone,
  [in]       DWORD numInfluences,
  [in] const DWORD *vertices,
  [in] const FLOAT *weights
);
```



## <a name="parameters"></a><span data-ttu-id="43a9c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="43a9c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43a9c-107">*Osso* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="43a9c-107">*Bone* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43a9c-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="43a9c-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="43a9c-109">Numero osso.</span><span class="sxs-lookup"><span data-stu-id="43a9c-109">Bone number.</span></span>

</dd> <dt>

<span data-ttu-id="43a9c-110">*numInfluences* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="43a9c-110">*numInfluences* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43a9c-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="43a9c-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="43a9c-112">Numero di influenze.</span><span class="sxs-lookup"><span data-stu-id="43a9c-112">Number of influences.</span></span>

</dd> <dt>

<span data-ttu-id="43a9c-113">*vertici* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="43a9c-113">*vertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43a9c-114">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="43a9c-114">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="43a9c-115">Matrice di vertici influenzato da un osso.</span><span class="sxs-lookup"><span data-stu-id="43a9c-115">The array of vertices influenced by a bone.</span></span>

</dd> <dt>

<span data-ttu-id="43a9c-116">*pesi* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="43a9c-116">*weights* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43a9c-117">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="43a9c-117">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="43a9c-118">Matrice di pesi influenzati da un osso.</span><span class="sxs-lookup"><span data-stu-id="43a9c-118">The array of weights influenced by a bone.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43a9c-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="43a9c-119">Return value</span></span>

<span data-ttu-id="43a9c-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="43a9c-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="43a9c-121">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="43a9c-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="43a9c-122">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="43a9c-122">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="43a9c-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="43a9c-123">Requirements</span></span>



| <span data-ttu-id="43a9c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="43a9c-124">Requirement</span></span> | <span data-ttu-id="43a9c-125">Valore</span><span class="sxs-lookup"><span data-stu-id="43a9c-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="43a9c-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="43a9c-126">Header</span></span><br/>  | <dl> <span data-ttu-id="43a9c-127"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="43a9c-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="43a9c-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="43a9c-128">Library</span></span><br/> | <dl> <span data-ttu-id="43a9c-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="43a9c-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="43a9c-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="43a9c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43a9c-131">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="43a9c-131">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="43a9c-132">**ID3DXSkinInfo::GetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="43a9c-132">**ID3DXSkinInfo::GetBoneInfluence**</span></span>](id3dxskininfo--getboneinfluence.md)
</dt> <dt>

[<span data-ttu-id="43a9c-133">**ID3DXSkinInfo::GetNumBoneInfluences**</span><span class="sxs-lookup"><span data-stu-id="43a9c-133">**ID3DXSkinInfo::GetNumBoneInfluences**</span></span>](id3dxskininfo--getnumboneinfluences.md)
</dt> </dl>

 

 
