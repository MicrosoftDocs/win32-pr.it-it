---
description: Ottiene il buffer dell'indice mesh.
ms.assetid: d9152f3b-c8e6-4def-8cf1-a517ca4d34e7
title: 'Metodo ID3DXPatchMesh:: GetIndexBuffer (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c2730b90f77d33db519d2231a68ab7fdc2b520fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323466"
---
# <a name="id3dxpatchmeshgetindexbuffer-method"></a><span data-ttu-id="9044c-103">Metodo ID3DXPatchMesh:: GetIndexBuffer</span><span class="sxs-lookup"><span data-stu-id="9044c-103">ID3DXPatchMesh::GetIndexBuffer method</span></span>

<span data-ttu-id="9044c-104">Ottiene il buffer dell'indice mesh.</span><span class="sxs-lookup"><span data-stu-id="9044c-104">Gets the mesh index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="9044c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9044c-105">Syntax</span></span>


```C++
HRESULT GetIndexBuffer(
  [out, retval] LPDIRECT3DINDEXBUFFER9 *ppIB
);
```



## <a name="parameters"></a><span data-ttu-id="9044c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9044c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9044c-107">*ppIB* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="9044c-107">*ppIB* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="9044c-108">Tipo: **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span><span class="sxs-lookup"><span data-stu-id="9044c-108">Type: **[**LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span></span>

<span data-ttu-id="9044c-109">Puntatore al buffer dell'indice.</span><span class="sxs-lookup"><span data-stu-id="9044c-109">Pointer to the index buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9044c-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9044c-110">Return value</span></span>

<span data-ttu-id="9044c-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9044c-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9044c-112">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9044c-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9044c-113">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="9044c-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="9044c-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="9044c-114">Remarks</span></span>

<span data-ttu-id="9044c-115">Il buffer di indice contiene l'ordinamento dei vertici nel buffer dei vertici.</span><span class="sxs-lookup"><span data-stu-id="9044c-115">The index buffer contains the vertex ordering in the vertex buffer.</span></span> <span data-ttu-id="9044c-116">Il buffer di indice viene usato per accedere al buffer del vertice quando viene eseguito il rendering della mesh.</span><span class="sxs-lookup"><span data-stu-id="9044c-116">The index buffer is used to access the vertex buffer when the mesh is rendered.</span></span>

## <a name="requirements"></a><span data-ttu-id="9044c-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9044c-117">Requirements</span></span>



| <span data-ttu-id="9044c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9044c-118">Requirement</span></span> | <span data-ttu-id="9044c-119">Valore</span><span class="sxs-lookup"><span data-stu-id="9044c-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9044c-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9044c-120">Header</span></span><br/>  | <dl> <span data-ttu-id="9044c-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="9044c-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="9044c-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="9044c-122">Library</span></span><br/> | <dl> <span data-ttu-id="9044c-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9044c-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9044c-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9044c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9044c-125">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="9044c-125">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
