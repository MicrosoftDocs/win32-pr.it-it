---
description: 'Metodo ID3DXPatchMesh::GetDeclaration: ottiene la dichiarazione del vertice.'
ms.assetid: 53ff2fb5-68b6-4edd-b48f-e06df306ee3f
title: Metodo ID3DXPatchMesh::GetDeclaration (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetDeclaration
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0fde070b1b013e651c84ffea7098eb8225aed8f9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093299"
---
# <a name="id3dxpatchmeshgetdeclaration-method"></a><span data-ttu-id="aacba-103">Metodo ID3DXPatchMesh::GetDeclaration</span><span class="sxs-lookup"><span data-stu-id="aacba-103">ID3DXPatchMesh::GetDeclaration method</span></span>

<span data-ttu-id="aacba-104">Ottiene la dichiarazione del vertice.</span><span class="sxs-lookup"><span data-stu-id="aacba-104">Gets the vertex declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="aacba-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aacba-105">Syntax</span></span>


```C++
HRESULT GetDeclaration(
  [out] LPD3DVERTEXELEMENT9 pDeclaration
);
```



## <a name="parameters"></a><span data-ttu-id="aacba-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="aacba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aacba-107">*pDeclaration* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="aacba-107">*pDeclaration* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aacba-108">Tipo: **[ **LPD3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span><span class="sxs-lookup"><span data-stu-id="aacba-108">Type: **[**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span></span>

<span data-ttu-id="aacba-109">Matrice di [**elementi D3DVERTEXELEMENT9**](d3dvertexelement9.md) che descrivono il formato dei vertici della mesh.</span><span class="sxs-lookup"><span data-stu-id="aacba-109">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements describing the vertex format of the mesh vertices.</span></span> <span data-ttu-id="aacba-110">La dimensione di questa matrice del dichiaratore è [**MAX \_ FVF \_ DECL \_ SIZE**](./max-fvf-decl-size.md).</span><span class="sxs-lookup"><span data-stu-id="aacba-110">The dimension of this declarator array is [**MAX\_FVF\_DECL\_SIZE**](./max-fvf-decl-size.md).</span></span> <span data-ttu-id="aacba-111">La matrice di elementi vertice termina con la macro [**D3DDECL \_ END.**](d3ddecl-end.md)</span><span class="sxs-lookup"><span data-stu-id="aacba-111">The vertex element array ends with the [**D3DDECL\_END**](d3ddecl-end.md) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aacba-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aacba-112">Return value</span></span>

<span data-ttu-id="aacba-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="aacba-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="aacba-114">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="aacba-114">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="aacba-115">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="aacba-115">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="aacba-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="aacba-116">Remarks</span></span>

<span data-ttu-id="aacba-117">La matrice di elementi include la macro [**D3DDECL \_ END,**](d3ddecl-end.md) che termina la dichiarazione.</span><span class="sxs-lookup"><span data-stu-id="aacba-117">The array of elements includes the [**D3DDECL\_END**](d3ddecl-end.md) macro, which ends the declaration.</span></span>

## <a name="requirements"></a><span data-ttu-id="aacba-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aacba-118">Requirements</span></span>



| <span data-ttu-id="aacba-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="aacba-119">Requirement</span></span> | <span data-ttu-id="aacba-120">Valore</span><span class="sxs-lookup"><span data-stu-id="aacba-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aacba-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aacba-121">Header</span></span><br/>  | <dl> <span data-ttu-id="aacba-122"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="aacba-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="aacba-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="aacba-123">Library</span></span><br/> | <dl> <span data-ttu-id="aacba-124"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="aacba-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="aacba-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aacba-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aacba-126">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="aacba-126">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
