---
description: Crea una mesh a N patch da una mesh triangolare.
ms.assetid: f565ed0b-72fc-4184-b423-f68b0acfafb0
title: Funzione D3DXCreateNPatchMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateNPatchMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0ab73d1254700808bbd56b7b46f7781b27b188b7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323547"
---
# <a name="d3dxcreatenpatchmesh-function"></a><span data-ttu-id="65b0b-103">D3DXCreateNPatchMesh (funzione)</span><span class="sxs-lookup"><span data-stu-id="65b0b-103">D3DXCreateNPatchMesh function</span></span>

<span data-ttu-id="65b0b-104">Crea una mesh a N patch da una mesh triangolare.</span><span class="sxs-lookup"><span data-stu-id="65b0b-104">Creates an N-patch mesh from a triangle mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="65b0b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="65b0b-105">Syntax</span></span>


```C++
HRESULT D3DXCreateNPatchMesh(
  _In_    LPD3DXMESH      pMeshSysMem,
  _Inout_ LPD3DXPATCHMESH *pPatchMesh
);
```



## <a name="parameters"></a><span data-ttu-id="65b0b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="65b0b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65b0b-107">*pMeshSysMem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="65b0b-107">*pMeshSysMem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65b0b-108">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="65b0b-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="65b0b-109">Indirizzo di un puntatore a un'interfaccia [**ID3DXMesh**](id3dxmesh.md) che rappresenta l'oggetto mesh triangolare.</span><span class="sxs-lookup"><span data-stu-id="65b0b-109">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface that represents the triangle mesh object.</span></span>

</dd> <dt>

<span data-ttu-id="65b0b-110">*pPatchMesh* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="65b0b-110">*pPatchMesh* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="65b0b-111">Tipo: **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="65b0b-111">Type: **[**LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span></span>

<span data-ttu-id="65b0b-112">Indirizzo di un puntatore a un'interfaccia [**ID3DXPatchMesh**](id3dxpatchmesh.md) che rappresenta l'oggetto mesh patch creato.</span><span class="sxs-lookup"><span data-stu-id="65b0b-112">Address of a pointer to an [**ID3DXPatchMesh**](id3dxpatchmesh.md) interface that represents the created patch mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65b0b-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="65b0b-113">Return value</span></span>

<span data-ttu-id="65b0b-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="65b0b-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="65b0b-115">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="65b0b-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="65b0b-116">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="65b0b-116">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="65b0b-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="65b0b-117">Requirements</span></span>



| <span data-ttu-id="65b0b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="65b0b-118">Requirement</span></span> | <span data-ttu-id="65b0b-119">Valore</span><span class="sxs-lookup"><span data-stu-id="65b0b-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="65b0b-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="65b0b-120">Header</span></span><br/>  | <dl> <span data-ttu-id="65b0b-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="65b0b-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="65b0b-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="65b0b-122">Library</span></span><br/> | <dl> <span data-ttu-id="65b0b-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="65b0b-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="65b0b-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="65b0b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65b0b-125">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="65b0b-125">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 




