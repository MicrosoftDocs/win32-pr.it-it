---
description: Recupera una dichiarazione che descrive i vertici nella mesh.
ms.assetid: e9028282-acf1-4ca4-8af0-7fb655dcb5d1
title: 'Metodo ID3DXBaseMesh:: getDeclaration (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetDeclaration
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 34f8736e822bfe4a959f35f60bb79783e79f2d52
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322068"
---
# <a name="id3dxbasemeshgetdeclaration-method"></a><span data-ttu-id="62935-103">Metodo ID3DXBaseMesh:: getDeclaration</span><span class="sxs-lookup"><span data-stu-id="62935-103">ID3DXBaseMesh::GetDeclaration method</span></span>

<span data-ttu-id="62935-104">Recupera una dichiarazione che descrive i vertici nella mesh.</span><span class="sxs-lookup"><span data-stu-id="62935-104">Retrieves a declaration describing the vertices in the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="62935-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="62935-105">Syntax</span></span>


```C++
HRESULT GetDeclaration(
  [in, out] D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a><span data-ttu-id="62935-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="62935-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62935-107">*Dichiarazione* \[ di in uscita\]</span><span class="sxs-lookup"><span data-stu-id="62935-107">*Declaration* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="62935-108">Tipo: **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span><span class="sxs-lookup"><span data-stu-id="62935-108">Type: **[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span></span>

<span data-ttu-id="62935-109">Matrice di elementi [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) che descrive il formato del vertice dei vertici della mesh.</span><span class="sxs-lookup"><span data-stu-id="62935-109">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements describing the vertex format of the mesh vertices.</span></span> <span data-ttu-id="62935-110">Il limite superiore della matrice di dichiaratori è [**Max \_ FVF \_ decl \_ size**](./max-fvf-decl-size.md).</span><span class="sxs-lookup"><span data-stu-id="62935-110">The upper limit of this declarator array is [**MAX\_FVF\_DECL\_SIZE**](./max-fvf-decl-size.md).</span></span> <span data-ttu-id="62935-111">La matrice di elementi Vertex termina con la macro [**D3DDECL \_ end**](d3ddecl-end.md) .</span><span class="sxs-lookup"><span data-stu-id="62935-111">The vertex element array ends with the [**D3DDECL\_END**](d3ddecl-end.md) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62935-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="62935-112">Return value</span></span>

<span data-ttu-id="62935-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="62935-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="62935-114">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="62935-114">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="62935-115">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="62935-115">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="62935-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="62935-116">Remarks</span></span>

<span data-ttu-id="62935-117">La matrice di elementi include la macro [**D3DDECL \_ end**](d3ddecl-end.md) , che termina la dichiarazione.</span><span class="sxs-lookup"><span data-stu-id="62935-117">The array of elements includes the [**D3DDECL\_END**](d3ddecl-end.md) macro, which ends the declaration.</span></span>

## <a name="requirements"></a><span data-ttu-id="62935-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="62935-118">Requirements</span></span>



| <span data-ttu-id="62935-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="62935-119">Requirement</span></span> | <span data-ttu-id="62935-120">Valore</span><span class="sxs-lookup"><span data-stu-id="62935-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="62935-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="62935-121">Header</span></span><br/>  | <dl> <span data-ttu-id="62935-122"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="62935-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="62935-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="62935-123">Library</span></span><br/> | <dl> <span data-ttu-id="62935-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="62935-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="62935-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="62935-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62935-126">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="62935-126">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
