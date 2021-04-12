---
description: Ottiene la matrice di offset dell'osso.
ms.assetid: 99d47635-ffae-4668-a37c-b15442148fa1
title: 'Metodo ID3DXSkinInfo:: GetBoneOffsetMatrix (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetBoneOffsetMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fce108dc1d0eb08f198ae9375ac35ed149c5e760
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354094"
---
# <a name="id3dxskininfogetboneoffsetmatrix-method"></a><span data-ttu-id="fccc2-103">Metodo ID3DXSkinInfo:: GetBoneOffsetMatrix</span><span class="sxs-lookup"><span data-stu-id="fccc2-103">ID3DXSkinInfo::GetBoneOffsetMatrix method</span></span>

<span data-ttu-id="fccc2-104">Ottiene la matrice di offset dell'osso.</span><span class="sxs-lookup"><span data-stu-id="fccc2-104">Gets the bone offset matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="fccc2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fccc2-105">Syntax</span></span>


```C++
LPD3DXMATRIX GetBoneOffsetMatrix(
  [in] DWORD Bone
);
```



## <a name="parameters"></a><span data-ttu-id="fccc2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fccc2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fccc2-107">*Osso* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fccc2-107">*Bone* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fccc2-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fccc2-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fccc2-109">Numero osso.</span><span class="sxs-lookup"><span data-stu-id="fccc2-109">Bone number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fccc2-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fccc2-110">Return value</span></span>

<span data-ttu-id="fccc2-111">Tipo: **[ **LPD3DXMATRIX**](d3dxmatrix.md)**</span><span class="sxs-lookup"><span data-stu-id="fccc2-111">Type: **[**LPD3DXMATRIX**](d3dxmatrix.md)**</span></span>

<span data-ttu-id="fccc2-112">Restituisce un puntatore alla matrice di offset dell'osso.</span><span class="sxs-lookup"><span data-stu-id="fccc2-112">Returns a pointer to the bone offset matrix.</span></span> <span data-ttu-id="fccc2-113">Non liberare questo puntatore.</span><span class="sxs-lookup"><span data-stu-id="fccc2-113">Do not free this pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="fccc2-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fccc2-114">Requirements</span></span>



| <span data-ttu-id="fccc2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fccc2-115">Requirement</span></span> | <span data-ttu-id="fccc2-116">Valore</span><span class="sxs-lookup"><span data-stu-id="fccc2-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fccc2-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fccc2-117">Header</span></span><br/>  | <dl> <span data-ttu-id="fccc2-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="fccc2-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="fccc2-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="fccc2-119">Library</span></span><br/> | <dl> <span data-ttu-id="fccc2-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fccc2-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fccc2-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fccc2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fccc2-122">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="fccc2-122">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="fccc2-123">**SetBoneOffsetMatrix**</span><span class="sxs-lookup"><span data-stu-id="fccc2-123">**SetBoneOffsetMatrix**</span></span>](id3dxskininfo--setboneoffsetmatrix.md)
</dt> <dt>

[<span data-ttu-id="fccc2-124">**GetNumBones**</span><span class="sxs-lookup"><span data-stu-id="fccc2-124">**GetNumBones**</span></span>](id3dxskininfo--getnumbones.md)
</dt> </dl>

 

 
