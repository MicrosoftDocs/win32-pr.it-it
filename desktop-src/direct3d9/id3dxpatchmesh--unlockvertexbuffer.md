---
description: Sbloccare il buffer dei vertici.
ms.assetid: 98b82fd1-56e8-45f3-bf26-a1e3b54c2979
title: 'Metodo ID3DXPatchMesh:: UnlockVertexBuffer (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.UnlockVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c6d4b6a55281048b303733e1addf2ab4636f74ce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323709"
---
# <a name="id3dxpatchmeshunlockvertexbuffer-method"></a><span data-ttu-id="ae3dc-103">Metodo ID3DXPatchMesh:: UnlockVertexBuffer</span><span class="sxs-lookup"><span data-stu-id="ae3dc-103">ID3DXPatchMesh::UnlockVertexBuffer method</span></span>

<span data-ttu-id="ae3dc-104">Sbloccare il buffer dei vertici.</span><span class="sxs-lookup"><span data-stu-id="ae3dc-104">Unlock the vertex buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae3dc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ae3dc-105">Syntax</span></span>


```C++
HRESULT UnlockVertexBuffer();
```



## <a name="parameters"></a><span data-ttu-id="ae3dc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ae3dc-106">Parameters</span></span>

<span data-ttu-id="ae3dc-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="ae3dc-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ae3dc-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ae3dc-108">Return value</span></span>

<span data-ttu-id="ae3dc-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ae3dc-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ae3dc-110">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ae3dc-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ae3dc-111">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="ae3dc-111">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae3dc-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="ae3dc-112">Remarks</span></span>

<span data-ttu-id="ae3dc-113">Il buffer vertex viene in genere bloccato, scritto e quindi sbloccato per la lettura.</span><span class="sxs-lookup"><span data-stu-id="ae3dc-113">The vertex buffer is usually locked, written to, and then unlocked for reading.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae3dc-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ae3dc-114">Requirements</span></span>



| <span data-ttu-id="ae3dc-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae3dc-115">Requirement</span></span> | <span data-ttu-id="ae3dc-116">Valore</span><span class="sxs-lookup"><span data-stu-id="ae3dc-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae3dc-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ae3dc-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ae3dc-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae3dc-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ae3dc-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="ae3dc-119">Library</span></span><br/> | <dl> <span data-ttu-id="ae3dc-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ae3dc-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ae3dc-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ae3dc-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae3dc-122">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="ae3dc-122">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 




