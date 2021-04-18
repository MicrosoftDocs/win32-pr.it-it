---
description: Sbloccare il buffer dell'indice.
ms.assetid: de3d0893-1596-42df-b049-6574c58ffa8d
title: 'Metodo ID3DXPatchMesh:: UnlockIndexBuffer (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.UnlockIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9bae54c6c4477682422328410558f1b405eb2677
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323048"
---
# <a name="id3dxpatchmeshunlockindexbuffer-method"></a><span data-ttu-id="b8d01-103">Metodo ID3DXPatchMesh:: UnlockIndexBuffer</span><span class="sxs-lookup"><span data-stu-id="b8d01-103">ID3DXPatchMesh::UnlockIndexBuffer method</span></span>

<span data-ttu-id="b8d01-104">Sbloccare il buffer dell'indice.</span><span class="sxs-lookup"><span data-stu-id="b8d01-104">Unlock the index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8d01-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b8d01-105">Syntax</span></span>


```C++
HRESULT UnlockIndexBuffer();
```



## <a name="parameters"></a><span data-ttu-id="b8d01-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b8d01-106">Parameters</span></span>

<span data-ttu-id="b8d01-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="b8d01-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b8d01-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b8d01-108">Return value</span></span>

<span data-ttu-id="b8d01-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b8d01-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b8d01-110">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b8d01-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b8d01-111">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="b8d01-111">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8d01-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="b8d01-112">Remarks</span></span>

<span data-ttu-id="b8d01-113">Il buffer dell'indice viene in genere bloccato, scritto e quindi sbloccato per la lettura.</span><span class="sxs-lookup"><span data-stu-id="b8d01-113">The index buffer is usually locked, written to, and then unlocked for reading.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8d01-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b8d01-114">Requirements</span></span>



| <span data-ttu-id="b8d01-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8d01-115">Requirement</span></span> | <span data-ttu-id="b8d01-116">Valore</span><span class="sxs-lookup"><span data-stu-id="b8d01-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8d01-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b8d01-117">Header</span></span><br/>  | <dl> <span data-ttu-id="b8d01-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8d01-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b8d01-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="b8d01-119">Library</span></span><br/> | <dl> <span data-ttu-id="b8d01-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b8d01-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b8d01-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b8d01-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8d01-122">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="b8d01-122">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 




