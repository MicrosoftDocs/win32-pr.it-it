---
description: Pulisce una mesh, preparandola per semplificare.
ms.assetid: 2b586ecc-db87-4b20-a4fc-c8b547bebf65
title: Funzione D3DXCleanMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCleanMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5565978dc1ad0e80c33718275ea65080930ce7cf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323018"
---
# <a name="d3dxcleanmesh-function"></a><span data-ttu-id="3d8be-103">D3DXCleanMesh (funzione)</span><span class="sxs-lookup"><span data-stu-id="3d8be-103">D3DXCleanMesh function</span></span>

<span data-ttu-id="3d8be-104">Pulisce una mesh, preparandola per semplificare.</span><span class="sxs-lookup"><span data-stu-id="3d8be-104">Cleans a mesh, preparing it for simplification.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d8be-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3d8be-105">Syntax</span></span>


```C++
HRESULT D3DXCleanMesh(
  _In_        D3DXCLEANTYPE CleanType,
  _In_        LPD3DXMESH    pMeshIn,
  _In_  const DWORD         *pAdjacencyIn,
  _Out_       LPD3DXMESH    *ppMeshOut,
  _Out_       DWORD         *pAdjacencyOut,
  _Out_       LPD3DXBUFFER  *ppErrorsAndWarnings
);
```



## <a name="parameters"></a><span data-ttu-id="3d8be-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3d8be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d8be-107">*CleanType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d8be-107">*CleanType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d8be-108">Tipo: **[ **D3DXCLEANTYPE**](./d3dxcleantype.md)**</span><span class="sxs-lookup"><span data-stu-id="3d8be-108">Type: **[**D3DXCLEANTYPE**](./d3dxcleantype.md)**</span></span>

<span data-ttu-id="3d8be-109">Operazioni sui vertici da eseguire per preparare la pulizia della rete.</span><span class="sxs-lookup"><span data-stu-id="3d8be-109">Vertex operations to perform in preparation for mesh cleaning.</span></span> <span data-ttu-id="3d8be-110">Vedere [**D3DXCLEANTYPE**](./d3dxcleantype.md).</span><span class="sxs-lookup"><span data-stu-id="3d8be-110">See [**D3DXCLEANTYPE**](./d3dxcleantype.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d8be-111">*pMeshIn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d8be-111">*pMeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d8be-112">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="3d8be-112">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="3d8be-113">Puntatore a un'interfaccia [**ID3DXMesh**](id3dxmesh.md) , che rappresenta la mesh da pulire.</span><span class="sxs-lookup"><span data-stu-id="3d8be-113">Pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the mesh to be cleaned.</span></span>

</dd> <dt>

<span data-ttu-id="3d8be-114">*pAdjacencyIn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d8be-114">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d8be-115">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="3d8be-115">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3d8be-116">Puntatore a una matrice di tre DWORD per ogni volto che specifica i tre elementi adiacenti per ogni viso nella mesh da pulire.</span><span class="sxs-lookup"><span data-stu-id="3d8be-116">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh to be cleaned.</span></span>

</dd> <dt>

<span data-ttu-id="3d8be-117">*ppMeshOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3d8be-117">*ppMeshOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3d8be-118">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="3d8be-118">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="3d8be-119">Indirizzo di un puntatore a un'interfaccia [**ID3DXMesh**](id3dxmesh.md) , che rappresenta la mesh pulita restituita.</span><span class="sxs-lookup"><span data-stu-id="3d8be-119">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the returned cleaned mesh.</span></span> <span data-ttu-id="3d8be-120">Viene restituita la stessa mesh che è stata passata se non era necessaria alcuna pulizia.</span><span class="sxs-lookup"><span data-stu-id="3d8be-120">The same mesh is returned that was passed in if no cleaning was necessary.</span></span>

</dd> <dt>

<span data-ttu-id="3d8be-121">*pAdjacencyOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3d8be-121">*pAdjacencyOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3d8be-122">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3d8be-122">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3d8be-123">Puntatore a una matrice di tre DWORD per ogni volto che specifica i tre elementi adiacenti per ogni viso nella mesh di output.</span><span class="sxs-lookup"><span data-stu-id="3d8be-123">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the output mesh.</span></span>

</dd> <dt>

<span data-ttu-id="3d8be-124">*ppErrorsAndWarnings* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3d8be-124">*ppErrorsAndWarnings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3d8be-125">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="3d8be-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="3d8be-126">Restituisce un buffer contenente una stringa di errori e avvisi che illustra i problemi rilevati nella mesh.</span><span class="sxs-lookup"><span data-stu-id="3d8be-126">Returns a buffer containing a string of errors and warnings, which explain the problems found in the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d8be-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3d8be-127">Return value</span></span>

<span data-ttu-id="3d8be-128">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3d8be-128">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3d8be-129">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3d8be-129">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3d8be-130">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="3d8be-130">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d8be-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="3d8be-131">Remarks</span></span>

<span data-ttu-id="3d8be-132">Questa funzione pulisce una mesh usando il metodo di pulizia e le opzioni specificate nel parametro CleanType.</span><span class="sxs-lookup"><span data-stu-id="3d8be-132">This function cleans a mesh using the cleaning method and options specified in the CleanType parameter.</span></span> <span data-ttu-id="3d8be-133">Per una descrizione delle opzioni disponibili, vedere l'enumerazione [**D3DXCLEANTYPE**](./d3dxcleantype.md) .</span><span class="sxs-lookup"><span data-stu-id="3d8be-133">See the [**D3DXCLEANTYPE**](./d3dxcleantype.md) enumeration for a description of the available options.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d8be-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3d8be-134">Requirements</span></span>



| <span data-ttu-id="3d8be-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d8be-135">Requirement</span></span> | <span data-ttu-id="3d8be-136">Valore</span><span class="sxs-lookup"><span data-stu-id="3d8be-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d8be-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3d8be-137">Header</span></span><br/>  | <dl> <span data-ttu-id="3d8be-138"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d8be-138"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="3d8be-139">Libreria</span><span class="sxs-lookup"><span data-stu-id="3d8be-139">Library</span></span><br/> | <dl> <span data-ttu-id="3d8be-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3d8be-140"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3d8be-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3d8be-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d8be-142">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="3d8be-142">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
