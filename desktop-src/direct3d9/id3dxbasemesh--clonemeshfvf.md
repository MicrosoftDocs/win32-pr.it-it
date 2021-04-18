---
description: Clona una mesh usando un codice FVF (Flexible Vertex Format).
ms.assetid: b7d23ea9-1a2f-46e3-bcb5-82040d2a1e12
title: 'Metodo ID3DXBaseMesh:: CloneMeshFVF (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.CloneMeshFVF
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4cb3b0ad33e54e79464949f441842173fb48a180
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322556"
---
# <a name="id3dxbasemeshclonemeshfvf-method"></a><span data-ttu-id="8dcae-103">Metodo ID3DXBaseMesh:: CloneMeshFVF</span><span class="sxs-lookup"><span data-stu-id="8dcae-103">ID3DXBaseMesh::CloneMeshFVF method</span></span>

<span data-ttu-id="8dcae-104">Clona una mesh usando un codice FVF (Flexible Vertex Format).</span><span class="sxs-lookup"><span data-stu-id="8dcae-104">Clones a mesh using a flexible vertex format (FVF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="8dcae-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8dcae-105">Syntax</span></span>


```C++
HRESULT CloneMeshFVF(
  [in]          DWORD             Options,
  [in]          DWORD             FVF,
  [in]          LPDIRECT3DDEVICE9 pDevice,
  [out, retval] LPD3DXMESH        *ppCloneMesh
);
```



## <a name="parameters"></a><span data-ttu-id="8dcae-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8dcae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8dcae-107">*Opzioni* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="8dcae-107">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8dcae-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8dcae-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8dcae-109">Combinazione di uno o più flag [**D3DXMESH**](./d3dxmesh.md) che specificano le opzioni di creazione per la mesh.</span><span class="sxs-lookup"><span data-stu-id="8dcae-109">A combination of one or more [**D3DXMESH**](./d3dxmesh.md) flags specifying creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="8dcae-110">*FVF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8dcae-110">*FVF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8dcae-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8dcae-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8dcae-112">Combinazione di codici FVF, che specifica il formato del vertice per i vertici nella mesh di output.</span><span class="sxs-lookup"><span data-stu-id="8dcae-112">Combination of FVF codes, which specifies the vertex format for the vertices in the output mesh.</span></span> <span data-ttu-id="8dcae-113">Per i valori dei codici, vedere [D3DFVF](d3dfvf.md).</span><span class="sxs-lookup"><span data-stu-id="8dcae-113">For the values of the codes, see [D3DFVF](d3dfvf.md).</span></span>

</dd> <dt>

<span data-ttu-id="8dcae-114">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8dcae-114">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8dcae-115">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="8dcae-115">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="8dcae-116">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) che rappresenta l'oggetto dispositivo associato alla mesh.</span><span class="sxs-lookup"><span data-stu-id="8dcae-116">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface representing the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="8dcae-117">*ppCloneMesh* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="8dcae-117">*ppCloneMesh* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="8dcae-118">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="8dcae-118">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="8dcae-119">Indirizzo di un puntatore a un'interfaccia [**ID3DXMesh**](id3dxmesh.md) , che rappresenta la mesh clonata.</span><span class="sxs-lookup"><span data-stu-id="8dcae-119">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the cloned mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8dcae-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8dcae-120">Return value</span></span>

<span data-ttu-id="8dcae-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8dcae-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8dcae-122">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8dcae-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8dcae-123">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="8dcae-123">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="8dcae-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="8dcae-124">Remarks</span></span>

<span data-ttu-id="8dcae-125">**ID3DXBaseMesh:: CloneMeshFVF** viene usato per riformattare e modificare il layout dei dati del vertice.</span><span class="sxs-lookup"><span data-stu-id="8dcae-125">**ID3DXBaseMesh::CloneMeshFVF** is used to reformat and change the vertex data layout.</span></span> <span data-ttu-id="8dcae-126">Questa operazione viene eseguita creando un nuovo oggetto mesh.</span><span class="sxs-lookup"><span data-stu-id="8dcae-126">This is done by creating a new mesh object.</span></span> <span data-ttu-id="8dcae-127">Ad esempio, usarlo per aggiungere spazio per normali, coordinate di trama, colori, pesi e così via, che non erano presenti prima.</span><span class="sxs-lookup"><span data-stu-id="8dcae-127">For example, use it to to add space for normals, texture coordinates, colors, weights, etc. that were not present before.</span></span>

<span data-ttu-id="8dcae-128">[**ID3DXBaseMesh:: UpdateSemantics**](id3dxbasemesh--updatesemantics.md) aggiorna la dichiarazione di vertice con informazioni semantiche diverse senza modificare il layout del buffer del vertice.</span><span class="sxs-lookup"><span data-stu-id="8dcae-128">[**ID3DXBaseMesh::UpdateSemantics**](id3dxbasemesh--updatesemantics.md) updates the vertex declaration with different semantic information without changing the layout of the vertex buffer.</span></span> <span data-ttu-id="8dcae-129">Questo metodo non modifica il contenuto del buffer dei vertici.</span><span class="sxs-lookup"><span data-stu-id="8dcae-129">This method does not modify the contents of the vertex buffer.</span></span> <span data-ttu-id="8dcae-130">Ad esempio, usarlo per rietichettare una coordinata di trama 3D come una binormale o tangente o viceversa.</span><span class="sxs-lookup"><span data-stu-id="8dcae-130">For example, use it to relabel a 3D texture coordinate as a binormal or tangent or vice versa.</span></span>

## <a name="requirements"></a><span data-ttu-id="8dcae-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8dcae-131">Requirements</span></span>



| <span data-ttu-id="8dcae-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="8dcae-132">Requirement</span></span> | <span data-ttu-id="8dcae-133">Valore</span><span class="sxs-lookup"><span data-stu-id="8dcae-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8dcae-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8dcae-134">Header</span></span><br/>  | <dl> <span data-ttu-id="8dcae-135"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="8dcae-135"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="8dcae-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="8dcae-136">Library</span></span><br/> | <dl> <span data-ttu-id="8dcae-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8dcae-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8dcae-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8dcae-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8dcae-139">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="8dcae-139">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> <dt>

[<span data-ttu-id="8dcae-140">**D3DXFVFFromDeclarator**</span><span class="sxs-lookup"><span data-stu-id="8dcae-140">**D3DXFVFFromDeclarator**</span></span>](d3dxfvffromdeclarator.md)
</dt> </dl>

 

 
