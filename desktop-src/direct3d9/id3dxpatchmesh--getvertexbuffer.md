---
description: Ottiene il buffer del vertice mesh.
ms.assetid: 4ea4e99b-5c2c-467b-8b5d-8174c446680a
title: 'Metodo ID3DXPatchMesh:: GetVertexBuffer (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b8c3bb79d4c04db072adef857de195df7a0f0fff
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323719"
---
# <a name="id3dxpatchmeshgetvertexbuffer-method"></a><span data-ttu-id="22b60-103">Metodo ID3DXPatchMesh:: GetVertexBuffer</span><span class="sxs-lookup"><span data-stu-id="22b60-103">ID3DXPatchMesh::GetVertexBuffer method</span></span>

<span data-ttu-id="22b60-104">Ottiene il buffer del vertice mesh.</span><span class="sxs-lookup"><span data-stu-id="22b60-104">Gets the mesh vertex buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="22b60-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="22b60-105">Syntax</span></span>


```C++
HRESULT GetVertexBuffer(
  [out] LPDIRECT3DVERTEXBUFFER9 *ppVB
);
```



## <a name="parameters"></a><span data-ttu-id="22b60-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="22b60-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22b60-107">*ppVB* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="22b60-107">*ppVB* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="22b60-108">Tipo: **[ **LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)\***</span><span class="sxs-lookup"><span data-stu-id="22b60-108">Type: **[**LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)\***</span></span>

<span data-ttu-id="22b60-109">Puntatore al buffer del vertice.</span><span class="sxs-lookup"><span data-stu-id="22b60-109">Pointer to the vertex buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22b60-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="22b60-110">Return value</span></span>

<span data-ttu-id="22b60-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="22b60-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="22b60-112">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="22b60-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="22b60-113">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="22b60-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="22b60-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="22b60-114">Remarks</span></span>

<span data-ttu-id="22b60-115">Questo metodo presuppone un mosaico uniforme.</span><span class="sxs-lookup"><span data-stu-id="22b60-115">This method assumes uniform tessellation.</span></span>

## <a name="requirements"></a><span data-ttu-id="22b60-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="22b60-116">Requirements</span></span>



| <span data-ttu-id="22b60-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="22b60-117">Requirement</span></span> | <span data-ttu-id="22b60-118">Valore</span><span class="sxs-lookup"><span data-stu-id="22b60-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="22b60-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="22b60-119">Header</span></span><br/>  | <dl> <span data-ttu-id="22b60-120"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="22b60-120"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="22b60-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="22b60-121">Library</span></span><br/> | <dl> <span data-ttu-id="22b60-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="22b60-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="22b60-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="22b60-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22b60-124">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="22b60-124">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
