---
description: Genera un elenco di bordi della mesh, oltre a un elenco di visi che condividono ogni bordo.
ms.assetid: 9d52290f-1c9e-43a7-b239-35cd54e36466
title: 'Metodo ID3DXBaseMesh:: GenerateAdjacency (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GenerateAdjacency
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b5b1d304878a4977bb14d6ef98ad7256b6c3181f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401996"
---
# <a name="id3dxbasemeshgenerateadjacency-method"></a><span data-ttu-id="5a0ed-103">Metodo ID3DXBaseMesh:: GenerateAdjacency</span><span class="sxs-lookup"><span data-stu-id="5a0ed-103">ID3DXBaseMesh::GenerateAdjacency method</span></span>

<span data-ttu-id="5a0ed-104">Genera un elenco di bordi della mesh, oltre a un elenco di visi che condividono ogni bordo.</span><span class="sxs-lookup"><span data-stu-id="5a0ed-104">Generate a list of mesh edges, as well as a list of faces that share each edge.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a0ed-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5a0ed-105">Syntax</span></span>


```C++
HRESULT GenerateAdjacency(
  [in] FLOAT Epsilon,
  [in] DWORD *pAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="5a0ed-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5a0ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a0ed-107">*Epsilon* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5a0ed-107">*Epsilon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a0ed-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5a0ed-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5a0ed-109">Specifica che i vertici che differiscono dalla posizione minore di Epsilon devono essere considerati coincidenti.</span><span class="sxs-lookup"><span data-stu-id="5a0ed-109">Specifies that vertices that differ in position by less than epsilon should be treated as coincident.</span></span>

</dd> <dt>

<span data-ttu-id="5a0ed-110">*pAdjacency* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5a0ed-110">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a0ed-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5a0ed-111">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5a0ed-112">Puntatore a una matrice di tre DWORD per volto da riempire con gli indici di visi adiacenti.</span><span class="sxs-lookup"><span data-stu-id="5a0ed-112">Pointer to an array of three DWORDs per face to be filled with the indices of adjacent faces.</span></span> <span data-ttu-id="5a0ed-113">Il numero di byte in questa matrice deve essere almeno 3 \* [**ID3DXBaseMesh:: GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof (DWORD).</span><span class="sxs-lookup"><span data-stu-id="5a0ed-113">The number of bytes in this array must be at least 3 \* [**ID3DXBaseMesh::GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof(DWORD).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a0ed-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5a0ed-114">Return value</span></span>

<span data-ttu-id="5a0ed-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5a0ed-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5a0ed-116">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5a0ed-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5a0ed-117">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="5a0ed-117">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a0ed-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="5a0ed-118">Remarks</span></span>

<span data-ttu-id="5a0ed-119">Quando un'applicazione genera informazioni adiacenza per una mesh, i dati della mesh possono essere ottimizzati per migliorare le prestazioni di disegno.</span><span class="sxs-lookup"><span data-stu-id="5a0ed-119">After an application generates adjacency information for a mesh, the mesh data can be optimized for better drawing performance.</span></span>

<span data-ttu-id="5a0ed-120">L'ordine delle voci nel buffer adiacenza è determinato dall'ordine degli indici dei vertici nel buffer dell'indice.</span><span class="sxs-lookup"><span data-stu-id="5a0ed-120">The order of the entries in the adjacency buffer is determined by the order of the vertex indices in the index buffer.</span></span> <span data-ttu-id="5a0ed-121">Il triangolo adiacente 0 corrisponde sempre al bordo tra gli indici degli angoli 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="5a0ed-121">The adjacent triangle 0 always corresponds to the edge between the indices of the corners 0 and 1.</span></span> <span data-ttu-id="5a0ed-122">Il triangolo adiacente 1 corrisponde sempre al bordo tra gli indici degli angoli 1 e 2, mentre il triangolo adiacente 2 corrisponde al bordo tra gli indici degli angoli 2 e 0.</span><span class="sxs-lookup"><span data-stu-id="5a0ed-122">The adjacent triangle 1 always corresponds to the edge between the indices of the corners 1 and 2 while the adjacent triangle 2 corresponds to the edge between the indices of the corners 2 and 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a0ed-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5a0ed-123">Requirements</span></span>



| <span data-ttu-id="5a0ed-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a0ed-124">Requirement</span></span> | <span data-ttu-id="5a0ed-125">Valore</span><span class="sxs-lookup"><span data-stu-id="5a0ed-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a0ed-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5a0ed-126">Header</span></span><br/>  | <dl> <span data-ttu-id="5a0ed-127"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a0ed-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="5a0ed-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="5a0ed-128">Library</span></span><br/> | <dl> <span data-ttu-id="5a0ed-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a0ed-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5a0ed-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5a0ed-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a0ed-131">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="5a0ed-131">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> <dt>

[<span data-ttu-id="5a0ed-132">**ID3DXMesh:: Optimize**</span><span class="sxs-lookup"><span data-stu-id="5a0ed-132">**ID3DXMesh::Optimize**</span></span>](id3dxmesh--optimize.md)
</dt> <dt>

[<span data-ttu-id="5a0ed-133">**ID3DXMesh:: OptimizeInplace**</span><span class="sxs-lookup"><span data-stu-id="5a0ed-133">**ID3DXMesh::OptimizeInplace**</span></span>](id3dxmesh--optimizeinplace.md)
</dt> </dl>

 

 
