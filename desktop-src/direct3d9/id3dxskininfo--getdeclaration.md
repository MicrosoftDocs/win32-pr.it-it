---
description: 'Metodo ID3DXSkinInfo::GetDeclaration: ottiene la dichiarazione del vertice.'
ms.assetid: 49738e9b-09cb-489f-b9af-32d220fbede8
title: Metodo ID3DXSkinInfo::GetDeclaration (D3DX9Mesh.h)
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
ms.openlocfilehash: 83554b13fe8e20890b1edecd690c540c2e14d4d7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093139"
---
# <a name="id3dxskininfogetdeclaration-method"></a><span data-ttu-id="35188-103">Metodo ID3DXSkinInfo::GetDeclaration</span><span class="sxs-lookup"><span data-stu-id="35188-103">ID3DXSkinInfo::GetDeclaration method</span></span>

<span data-ttu-id="35188-104">Ottiene la dichiarazione del vertice.</span><span class="sxs-lookup"><span data-stu-id="35188-104">Gets the vertex declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="35188-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="35188-105">Syntax</span></span>


```C++
HRESULT GetDeclaration(
  [in, out] D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a><span data-ttu-id="35188-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="35188-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35188-107">*Dichiarazione* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="35188-107">*Declaration* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="35188-108">Tipo: **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span><span class="sxs-lookup"><span data-stu-id="35188-108">Type: **[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span></span>

<span data-ttu-id="35188-109">Matrice di [**elementi D3DVERTEXELEMENT9**](d3dvertexelement9.md) che descrivono il formato dei vertici della mesh.</span><span class="sxs-lookup"><span data-stu-id="35188-109">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements describing the vertex format of the mesh vertices.</span></span> <span data-ttu-id="35188-110">Il limite superiore di questa matrice di dichiaratori è [**MAX \_ FVF \_ DECL \_ SIZE**](./max-fvf-decl-size.md).</span><span class="sxs-lookup"><span data-stu-id="35188-110">The upper limit of this declarator array is [**MAX\_FVF\_DECL\_SIZE**](./max-fvf-decl-size.md).</span></span> <span data-ttu-id="35188-111">La matrice di elementi vertice termina con la macro [**D3DDECL \_ END.**](d3ddecl-end.md)</span><span class="sxs-lookup"><span data-stu-id="35188-111">The vertex element array ends with the [**D3DDECL\_END**](d3ddecl-end.md) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35188-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="35188-112">Return value</span></span>

<span data-ttu-id="35188-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="35188-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="35188-114">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="35188-114">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="35188-115">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="35188-115">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="35188-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="35188-116">Remarks</span></span>

<span data-ttu-id="35188-117">La matrice di elementi include la macro [**D3DDECL \_ END,**](d3ddecl-end.md) che termina la dichiarazione.</span><span class="sxs-lookup"><span data-stu-id="35188-117">The array of elements includes the [**D3DDECL\_END**](d3ddecl-end.md) macro, which ends the declaration.</span></span>

## <a name="requirements"></a><span data-ttu-id="35188-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35188-118">Requirements</span></span>



| <span data-ttu-id="35188-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="35188-119">Requirement</span></span> | <span data-ttu-id="35188-120">Valore</span><span class="sxs-lookup"><span data-stu-id="35188-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="35188-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="35188-121">Header</span></span><br/>  | <dl> <span data-ttu-id="35188-122"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="35188-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="35188-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="35188-123">Library</span></span><br/> | <dl> <span data-ttu-id="35188-124"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="35188-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="35188-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="35188-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35188-126">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="35188-126">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="35188-127">**ID3DXSkinInfo::SetDeclaration**</span><span class="sxs-lookup"><span data-stu-id="35188-127">**ID3DXSkinInfo::SetDeclaration**</span></span>](id3dxskininfo--setdeclaration.md)
</dt> </dl>

 

 
