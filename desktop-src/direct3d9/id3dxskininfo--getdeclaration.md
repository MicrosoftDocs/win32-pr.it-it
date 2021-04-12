---
description: Ottiene la dichiarazione del vertice.
ms.assetid: 49738e9b-09cb-489f-b9af-32d220fbede8
title: 'Metodo ID3DXSkinInfo:: getDeclaration (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetDeclaration
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: de80694bbbb6eea29f391b3b39cff9caacd4791c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354064"
---
# <a name="id3dxskininfogetdeclaration-method"></a><span data-ttu-id="aa945-103">Metodo ID3DXSkinInfo:: getDeclaration</span><span class="sxs-lookup"><span data-stu-id="aa945-103">ID3DXSkinInfo::GetDeclaration method</span></span>

<span data-ttu-id="aa945-104">Ottiene la dichiarazione del vertice.</span><span class="sxs-lookup"><span data-stu-id="aa945-104">Gets the vertex declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa945-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aa945-105">Syntax</span></span>


```C++
HRESULT GetDeclaration(
  [in, out] D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a><span data-ttu-id="aa945-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="aa945-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa945-107">*Dichiarazione* \[ di in uscita\]</span><span class="sxs-lookup"><span data-stu-id="aa945-107">*Declaration* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa945-108">Tipo: **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span><span class="sxs-lookup"><span data-stu-id="aa945-108">Type: **[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span></span>

<span data-ttu-id="aa945-109">Matrice di elementi [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) che descrive il formato del vertice dei vertici della mesh.</span><span class="sxs-lookup"><span data-stu-id="aa945-109">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements describing the vertex format of the mesh vertices.</span></span> <span data-ttu-id="aa945-110">Il limite superiore della matrice di dichiaratori è [**Max \_ FVF \_ decl \_ size**](./max-fvf-decl-size.md).</span><span class="sxs-lookup"><span data-stu-id="aa945-110">The upper limit of this declarator array is [**MAX\_FVF\_DECL\_SIZE**](./max-fvf-decl-size.md).</span></span> <span data-ttu-id="aa945-111">La matrice di elementi Vertex termina con la macro [**D3DDECL \_ end**](d3ddecl-end.md) .</span><span class="sxs-lookup"><span data-stu-id="aa945-111">The vertex element array ends with the [**D3DDECL\_END**](d3ddecl-end.md) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa945-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aa945-112">Return value</span></span>

<span data-ttu-id="aa945-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="aa945-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="aa945-114">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="aa945-114">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="aa945-115">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="aa945-115">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa945-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="aa945-116">Remarks</span></span>

<span data-ttu-id="aa945-117">La matrice di elementi include la macro [**D3DDECL \_ end**](d3ddecl-end.md) , che termina la dichiarazione.</span><span class="sxs-lookup"><span data-stu-id="aa945-117">The array of elements includes the [**D3DDECL\_END**](d3ddecl-end.md) macro, which ends the declaration.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa945-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aa945-118">Requirements</span></span>



| <span data-ttu-id="aa945-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa945-119">Requirement</span></span> | <span data-ttu-id="aa945-120">Valore</span><span class="sxs-lookup"><span data-stu-id="aa945-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa945-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aa945-121">Header</span></span><br/>  | <dl> <span data-ttu-id="aa945-122"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa945-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="aa945-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="aa945-123">Library</span></span><br/> | <dl> <span data-ttu-id="aa945-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aa945-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="aa945-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aa945-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa945-126">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="aa945-126">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="aa945-127">**ID3DXSkinInfo:: sedichiarazione**</span><span class="sxs-lookup"><span data-stu-id="aa945-127">**ID3DXSkinInfo::SetDeclaration**</span></span>](id3dxskininfo--setdeclaration.md)
</dt> </dl>

 

 
