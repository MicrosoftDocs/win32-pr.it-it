---
description: Ottiene il nome dell'osso, dall'indice di osso.
ms.assetid: f56faf41-c119-4cdd-bb8a-86fc99ff5893
title: 'Metodo ID3DXSkinInfo:: getbonename (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetBoneName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0566d423d277dc3f39f36f8c1fda297ec917eb7f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322065"
---
# <a name="id3dxskininfogetbonename-method"></a><span data-ttu-id="a3531-103">Metodo ID3DXSkinInfo:: getbonename</span><span class="sxs-lookup"><span data-stu-id="a3531-103">ID3DXSkinInfo::GetBoneName method</span></span>

<span data-ttu-id="a3531-104">Ottiene il nome dell'osso, dall'indice di osso.</span><span class="sxs-lookup"><span data-stu-id="a3531-104">Gets the bone name, from the bone index.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3531-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a3531-105">Syntax</span></span>


```C++
LPCSTR GetBoneName(
  [in] DWORD Bone
);
```



## <a name="parameters"></a><span data-ttu-id="a3531-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a3531-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3531-107">*Osso* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3531-107">*Bone* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3531-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a3531-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a3531-109">Numero osso.</span><span class="sxs-lookup"><span data-stu-id="a3531-109">Bone number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3531-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a3531-110">Return value</span></span>

<span data-ttu-id="a3531-111">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a3531-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a3531-112">Restituisce il nome dell'osso.</span><span class="sxs-lookup"><span data-stu-id="a3531-112">Returns the bone name.</span></span> <span data-ttu-id="a3531-113">Non liberare questa stringa.</span><span class="sxs-lookup"><span data-stu-id="a3531-113">Do not free this string.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3531-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a3531-114">Requirements</span></span>



| <span data-ttu-id="a3531-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3531-115">Requirement</span></span> | <span data-ttu-id="a3531-116">Valore</span><span class="sxs-lookup"><span data-stu-id="a3531-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3531-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a3531-117">Header</span></span><br/>  | <dl> <span data-ttu-id="a3531-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3531-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a3531-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="a3531-119">Library</span></span><br/> | <dl> <span data-ttu-id="a3531-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a3531-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a3531-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a3531-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3531-122">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="a3531-122">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="a3531-123">**ID3DXSkinInfo:: sebonename**</span><span class="sxs-lookup"><span data-stu-id="a3531-123">**ID3DXSkinInfo::SetBoneName**</span></span>](id3dxskininfo--setbonename.md)
</dt> <dt>

[<span data-ttu-id="a3531-124">**ID3DXSkinInfo::GetNumBones**</span><span class="sxs-lookup"><span data-stu-id="a3531-124">**ID3DXSkinInfo::GetNumBones**</span></span>](id3dxskininfo--getnumbones.md)
</dt> </dl>

 

 
