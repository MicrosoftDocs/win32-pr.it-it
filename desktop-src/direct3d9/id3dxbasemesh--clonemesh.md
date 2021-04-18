---
description: Clona una mesh usando un dichiaratore.
ms.assetid: 47e0329a-ea85-478d-af8b-cf85d2a779f6
title: 'Metodo ID3DXBaseMesh:: CloneMesh (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.CloneMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 421b72a080564886a10c187594223fb58a0b69fb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322558"
---
# <a name="id3dxbasemeshclonemesh-method"></a><span data-ttu-id="58ff9-103">Metodo ID3DXBaseMesh:: CloneMesh</span><span class="sxs-lookup"><span data-stu-id="58ff9-103">ID3DXBaseMesh::CloneMesh method</span></span>

<span data-ttu-id="58ff9-104">Clona una mesh usando un dichiaratore.</span><span class="sxs-lookup"><span data-stu-id="58ff9-104">Clones a mesh using a declarator.</span></span>

## <a name="syntax"></a><span data-ttu-id="58ff9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="58ff9-105">Syntax</span></span>


```C++
HRESULT CloneMesh(
  [in]                DWORD             Options,
  [in]          const D3DVERTEXELEMENT9 *pDeclaration,
  [in]                LPDIRECT3DDEVICE9 pDevice,
  [out, retval]       LPD3DXMESH        *ppCloneMesh
);
```



## <a name="parameters"></a><span data-ttu-id="58ff9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="58ff9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58ff9-107">*Opzioni* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="58ff9-107">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58ff9-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="58ff9-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="58ff9-109">Combinazione di uno o più flag [**D3DXMESH**](./d3dxmesh.md) che specificano le opzioni di creazione per la mesh.</span><span class="sxs-lookup"><span data-stu-id="58ff9-109">A combination of one or more [**D3DXMESH**](./d3dxmesh.md) flags specifying creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="58ff9-110">*pDeclaration* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58ff9-110">*pDeclaration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58ff9-111">Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="58ff9-111">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="58ff9-112">Matrice di elementi [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , che specifica il formato del vertice per i vertici nella mesh di output.</span><span class="sxs-lookup"><span data-stu-id="58ff9-112">An array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements, which specify the vertex format for the vertices in the output mesh.</span></span>

</dd> <dt>

<span data-ttu-id="58ff9-113">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58ff9-113">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58ff9-114">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="58ff9-114">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="58ff9-115">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta l'oggetto dispositivo associato alla mesh.</span><span class="sxs-lookup"><span data-stu-id="58ff9-115">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="58ff9-116">*ppCloneMesh* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="58ff9-116">*ppCloneMesh* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="58ff9-117">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="58ff9-117">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="58ff9-118">Indirizzo di un puntatore a un'interfaccia [**ID3DXMesh**](id3dxmesh.md) , che rappresenta la mesh clonata.</span><span class="sxs-lookup"><span data-stu-id="58ff9-118">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the cloned mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58ff9-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="58ff9-119">Return value</span></span>

<span data-ttu-id="58ff9-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="58ff9-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="58ff9-121">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="58ff9-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="58ff9-122">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="58ff9-122">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="58ff9-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="58ff9-123">Remarks</span></span>

<span data-ttu-id="58ff9-124">**ID3DXBaseMesh:: CloneMesh** viene usato per riformattare e modificare il layout dei dati del vertice.</span><span class="sxs-lookup"><span data-stu-id="58ff9-124">**ID3DXBaseMesh::CloneMesh** is used to reformat and change the vertex data layout.</span></span> <span data-ttu-id="58ff9-125">Questa operazione viene eseguita creando un nuovo oggetto mesh.</span><span class="sxs-lookup"><span data-stu-id="58ff9-125">This is done by creating a new mesh object.</span></span> <span data-ttu-id="58ff9-126">Ad esempio, usarlo per aggiungere spazio per normali, coordinate di trama, colori, pesi e così via, che non erano presenti prima.</span><span class="sxs-lookup"><span data-stu-id="58ff9-126">For example, use it to add space for normals, texture coordinates, colors, weights, etc. that were not present before.</span></span>

<span data-ttu-id="58ff9-127">[**ID3DXBaseMesh:: UpdateSemantics**](id3dxbasemesh--updatesemantics.md) aggiorna la dichiarazione di vertice con informazioni semantiche diverse senza modificare il layout del buffer del vertice.</span><span class="sxs-lookup"><span data-stu-id="58ff9-127">[**ID3DXBaseMesh::UpdateSemantics**](id3dxbasemesh--updatesemantics.md) updates the vertex declaration with different semantic information without changing the layout of the vertex buffer.</span></span> <span data-ttu-id="58ff9-128">Questo metodo non modifica il contenuto del buffer dei vertici.</span><span class="sxs-lookup"><span data-stu-id="58ff9-128">This method does not modify the contents of the vertex buffer.</span></span> <span data-ttu-id="58ff9-129">Ad esempio, usarlo per rietichettare una coordinata di trama 3D come una binormale o tangente o viceversa.</span><span class="sxs-lookup"><span data-stu-id="58ff9-129">For example, use it to relabel a 3D texture coordinate as a binormal or tangent or vice versa.</span></span>

## <a name="requirements"></a><span data-ttu-id="58ff9-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="58ff9-130">Requirements</span></span>



| <span data-ttu-id="58ff9-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="58ff9-131">Requirement</span></span> | <span data-ttu-id="58ff9-132">Valore</span><span class="sxs-lookup"><span data-stu-id="58ff9-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="58ff9-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="58ff9-133">Header</span></span><br/>  | <dl> <span data-ttu-id="58ff9-134"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="58ff9-134"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="58ff9-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="58ff9-135">Library</span></span><br/> | <dl> <span data-ttu-id="58ff9-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="58ff9-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="58ff9-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="58ff9-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58ff9-138">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="58ff9-138">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> <dt>

[<span data-ttu-id="58ff9-139">**ID3DXBaseMesh::CloneMeshFVF**</span><span class="sxs-lookup"><span data-stu-id="58ff9-139">**ID3DXBaseMesh::CloneMeshFVF**</span></span>](id3dxbasemesh--clonemeshfvf.md)
</dt> <dt>

[<span data-ttu-id="58ff9-140">**D3DXDeclaratorFromFVF**</span><span class="sxs-lookup"><span data-stu-id="58ff9-140">**D3DXDeclaratorFromFVF**</span></span>](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 
