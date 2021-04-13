---
description: Crea una nuova mesh della patch con la dichiarazione di vertice specificata.
ms.assetid: cc488cd3-fb38-468f-8aec-17c6ed842582
title: 'Metodo ID3DXPatchMesh:: CloneMesh (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.CloneMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 249b4282aa84e3f7c5ba619a0b42e8c0b1fdf846
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354324"
---
# <a name="id3dxpatchmeshclonemesh-method"></a><span data-ttu-id="f01a5-103">Metodo ID3DXPatchMesh:: CloneMesh</span><span class="sxs-lookup"><span data-stu-id="f01a5-103">ID3DXPatchMesh::CloneMesh method</span></span>

<span data-ttu-id="f01a5-104">Crea una nuova mesh della patch con la dichiarazione di vertice specificata.</span><span class="sxs-lookup"><span data-stu-id="f01a5-104">Creates a new patch mesh with the specified vertex declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="f01a5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f01a5-105">Syntax</span></span>


```C++
HRESULT CloneMesh(
  [in]                DWORD             Options,
  [in]          const D3DVERTEXELEMENT9 *pDecl,
  [out, retval]       LPD3DXPATCHMESH   *pMesh
);
```



## <a name="parameters"></a><span data-ttu-id="f01a5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f01a5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f01a5-107">*Opzioni* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="f01a5-107">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f01a5-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f01a5-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f01a5-109">Combinazione di uno o più flag [**D3DXMESH**](./d3dxmesh.md) che specificano le opzioni di creazione per la mesh.</span><span class="sxs-lookup"><span data-stu-id="f01a5-109">Combination of one or more [**D3DXMESH**](./d3dxmesh.md) flags that specify creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="f01a5-110">*pDecl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f01a5-110">*pDecl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f01a5-111">Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="f01a5-111">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="f01a5-112">Matrice di elementi [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) che specificano il formato del vertice per i vertici nella mesh di output.</span><span class="sxs-lookup"><span data-stu-id="f01a5-112">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements that specify the vertex format for the vertices in the output mesh.</span></span>

</dd> <dt>

<span data-ttu-id="f01a5-113">*pMesh* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="f01a5-113">*pMesh* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="f01a5-114">Tipo: **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="f01a5-114">Type: **[**LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span></span>

<span data-ttu-id="f01a5-115">Indirizzo di un puntatore a un'interfaccia [**ID3DXPatchMesh**](id3dxpatchmesh.md) che rappresenta la mesh clonata.</span><span class="sxs-lookup"><span data-stu-id="f01a5-115">Address of a pointer to an [**ID3DXPatchMesh**](id3dxpatchmesh.md) interface that represents the cloned mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f01a5-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f01a5-116">Return value</span></span>

<span data-ttu-id="f01a5-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f01a5-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f01a5-118">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f01a5-118">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f01a5-119">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="f01a5-119">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="f01a5-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="f01a5-120">Remarks</span></span>

<span data-ttu-id="f01a5-121">**CloneMesh** converte il buffer dei vertici nella nuova dichiarazione di vertice.</span><span class="sxs-lookup"><span data-stu-id="f01a5-121">**CloneMesh** converts the vertex buffer to the new vertex declaration.</span></span> <span data-ttu-id="f01a5-122">Le voci della dichiarazione di vertice nuove per la mesh originale sono impostate su 0.</span><span class="sxs-lookup"><span data-stu-id="f01a5-122">Entries in the vertex declaration that are new to the original mesh are set to 0.</span></span> <span data-ttu-id="f01a5-123">Se la mesh corrente contiene adiacenza, anche la nuova mesh avrà adiacenza.</span><span class="sxs-lookup"><span data-stu-id="f01a5-123">If the current mesh has adjacency, the new mesh will also have adjacency.</span></span>

## <a name="requirements"></a><span data-ttu-id="f01a5-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f01a5-124">Requirements</span></span>



| <span data-ttu-id="f01a5-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f01a5-125">Requirement</span></span> | <span data-ttu-id="f01a5-126">Valore</span><span class="sxs-lookup"><span data-stu-id="f01a5-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f01a5-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f01a5-127">Header</span></span><br/>  | <dl> <span data-ttu-id="f01a5-128"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="f01a5-128"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="f01a5-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="f01a5-129">Library</span></span><br/> | <dl> <span data-ttu-id="f01a5-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f01a5-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f01a5-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f01a5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f01a5-132">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="f01a5-132">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
