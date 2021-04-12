---
description: Ottiene la dichiarazione del vertice.
ms.assetid: 53ff2fb5-68b6-4edd-b48f-e06df306ee3f
title: 'Metodo ID3DXPatchMesh:: getDeclaration (D3DX9Mesh. h)'
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
ms.openlocfilehash: 7d2d39192368fdca8ccaba7c51e64f60ea030568
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104356084"
---
# <a name="id3dxpatchmeshgetdeclaration-method"></a><span data-ttu-id="100b4-103">Metodo ID3DXPatchMesh:: getDeclaration</span><span class="sxs-lookup"><span data-stu-id="100b4-103">ID3DXPatchMesh::GetDeclaration method</span></span>

<span data-ttu-id="100b4-104">Ottiene la dichiarazione del vertice.</span><span class="sxs-lookup"><span data-stu-id="100b4-104">Gets the vertex declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="100b4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="100b4-105">Syntax</span></span>


```C++
HRESULT GetDeclaration(
  [out] LPD3DVERTEXELEMENT9 pDeclaration
);
```



## <a name="parameters"></a><span data-ttu-id="100b4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="100b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="100b4-107">*pDeclaration* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="100b4-107">*pDeclaration* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="100b4-108">Tipo: **[ **LPD3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span><span class="sxs-lookup"><span data-stu-id="100b4-108">Type: **[**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span></span>

<span data-ttu-id="100b4-109">Matrice di elementi [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) che descrive il formato del vertice dei vertici della mesh.</span><span class="sxs-lookup"><span data-stu-id="100b4-109">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements describing the vertex format of the mesh vertices.</span></span> <span data-ttu-id="100b4-110">La dimensione della matrice di dichiaratori è [**Max \_ FVF \_ decl \_ size**](./max-fvf-decl-size.md).</span><span class="sxs-lookup"><span data-stu-id="100b4-110">The dimension of this declarator array is [**MAX\_FVF\_DECL\_SIZE**](./max-fvf-decl-size.md).</span></span> <span data-ttu-id="100b4-111">La matrice di elementi Vertex termina con la macro [**D3DDECL \_ end**](d3ddecl-end.md) .</span><span class="sxs-lookup"><span data-stu-id="100b4-111">The vertex element array ends with the [**D3DDECL\_END**](d3ddecl-end.md) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="100b4-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="100b4-112">Return value</span></span>

<span data-ttu-id="100b4-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="100b4-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="100b4-114">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="100b4-114">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="100b4-115">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="100b4-115">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="100b4-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="100b4-116">Remarks</span></span>

<span data-ttu-id="100b4-117">La matrice di elementi include la macro [**D3DDECL \_ end**](d3ddecl-end.md) , che termina la dichiarazione.</span><span class="sxs-lookup"><span data-stu-id="100b4-117">The array of elements includes the [**D3DDECL\_END**](d3ddecl-end.md) macro, which ends the declaration.</span></span>

## <a name="requirements"></a><span data-ttu-id="100b4-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="100b4-118">Requirements</span></span>



| <span data-ttu-id="100b4-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="100b4-119">Requirement</span></span> | <span data-ttu-id="100b4-120">Valore</span><span class="sxs-lookup"><span data-stu-id="100b4-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="100b4-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="100b4-121">Header</span></span><br/>  | <dl> <span data-ttu-id="100b4-122"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="100b4-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="100b4-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="100b4-123">Library</span></span><br/> | <dl> <span data-ttu-id="100b4-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="100b4-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="100b4-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="100b4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="100b4-126">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="100b4-126">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
