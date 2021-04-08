---
description: Genera una nuova mesh con visi e vertici riordinati per ottimizzare le prestazioni del disegno.
ms.assetid: 6a9bf7b9-2cb9-4b42-92d9-2a121ff79284
title: 'Metodo ID3DXMesh:: Optimize (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.Optimize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7752e08236094d7038a5e77ac1a679f787305022
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969522"
---
# <a name="id3dxmeshoptimize-method"></a><span data-ttu-id="48947-103">Metodo ID3DXMesh:: Optimize</span><span class="sxs-lookup"><span data-stu-id="48947-103">ID3DXMesh::Optimize method</span></span>

<span data-ttu-id="48947-104">Genera una nuova mesh con visi e vertici riordinati per ottimizzare le prestazioni del disegno.</span><span class="sxs-lookup"><span data-stu-id="48947-104">Generates a new mesh with reordered faces and vertices to optimize drawing performance.</span></span>

## <a name="syntax"></a><span data-ttu-id="48947-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="48947-105">Syntax</span></span>


```C++
HRESULT Optimize(
  [in]            DWORD        Flags,
  [in]      const DWORD        *pAdjacencyIn,
  [in, out]       DWORD        *pAdjacencyOut,
  [in, out]       DWORD        *pFaceRemap,
  [out]           LPD3DXBUFFER *ppVertexRemap,
  [out]           LPD3DXMESH   *ppOptMesh
);
```



## <a name="parameters"></a><span data-ttu-id="48947-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="48947-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48947-107">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="48947-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48947-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="48947-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="48947-109">Specifica il tipo di ottimizzazione da eseguire.</span><span class="sxs-lookup"><span data-stu-id="48947-109">Specifies the type of optimization to perform.</span></span> <span data-ttu-id="48947-110">Questo parametro può essere impostato su una combinazione di uno o più flag di [**D3DXMESHOPT**](./d3dxmeshopt.md) e [**D3DXMESH**](./d3dxmesh.md) (eccetto D3DXMESH a \_ 32 bit, D3DXMESH \_ IB \_ WRITEONLY e D3DXMESH \_ WRITEONLY).</span><span class="sxs-lookup"><span data-stu-id="48947-110">This parameter can be set to a combination of one or more flags from [**D3DXMESHOPT**](./d3dxmeshopt.md) and [**D3DXMESH**](./d3dxmesh.md) (except D3DXMESH\_32BIT, D3DXMESH\_IB\_WRITEONLY, and D3DXMESH\_WRITEONLY).</span></span>

</dd> <dt>

<span data-ttu-id="48947-111">*pAdjacencyIn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="48947-111">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48947-112">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="48947-112">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="48947-113">Puntatore a una matrice di tre DWORD per ogni volto che specifica i tre elementi adiacenti per ogni viso nella mesh di origine.</span><span class="sxs-lookup"><span data-stu-id="48947-113">Pointer to an array of three DWORDs per face that specifies the three neighbors for each face in the source mesh.</span></span> <span data-ttu-id="48947-114">Se il bordo non ha visi adiacenti, il valore è 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="48947-114">If the edge has no adjacent faces, the value is 0xffffffff.</span></span> <span data-ttu-id="48947-115">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="48947-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="48947-116">*pAdjacencyOut* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="48947-116">*pAdjacencyOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="48947-117">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="48947-117">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="48947-118">Puntatore a una matrice di tre DWORD per ogni volto che specifica i tre elementi adiacenti per ogni viso nella mesh ottimizzata.</span><span class="sxs-lookup"><span data-stu-id="48947-118">Pointer to an array of three DWORDs per face that specifies the three neighbors for each face in the optimized mesh.</span></span> <span data-ttu-id="48947-119">Se il bordo non ha visi adiacenti, il valore è 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="48947-119">If the edge has no adjacent faces, the value is 0xffffffff.</span></span>

</dd> <dt>

<span data-ttu-id="48947-120">*pFaceRemap* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="48947-120">*pFaceRemap* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="48947-121">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="48947-121">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="48947-122">Matrice di DWORD, una per ogni volto, che identifica la faccia mesh originale che corrisponde a ogni face nella mesh ottimizzata.</span><span class="sxs-lookup"><span data-stu-id="48947-122">An array of DWORDs, one per face, that identifies the original mesh face that corresponds to each face in the optimized mesh.</span></span> <span data-ttu-id="48947-123">Se il valore fornito per questo argomento è **null**, non vengono restituiti i dati di riassociazione della faccia.</span><span class="sxs-lookup"><span data-stu-id="48947-123">If the value supplied for this argument is **NULL**, face remap data is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="48947-124">*ppVertexRemap* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="48947-124">*ppVertexRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="48947-125">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="48947-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="48947-126">Indirizzo di un puntatore a un'interfaccia [**ID3DXBuffer**](id3dxbuffer.md) , che contiene un valore DWORD per ogni vertice che specifica la modalità di mapping dei nuovi vertici ai vertici precedenti.</span><span class="sxs-lookup"><span data-stu-id="48947-126">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, which contains a DWORD for each vertex that specifies how the new vertices map to the old vertices.</span></span> <span data-ttu-id="48947-127">Questo mapping è utile se è necessario modificare i dati esterni in base al nuovo mapping dei vertici.</span><span class="sxs-lookup"><span data-stu-id="48947-127">This remap is useful if you need to alter external data based on the new vertex mapping.</span></span>

</dd> <dt>

<span data-ttu-id="48947-128">*ppOptMesh* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="48947-128">*ppOptMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="48947-129">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="48947-129">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="48947-130">Indirizzo di un puntatore a un'interfaccia [**ID3DXMesh**](id3dxmesh.md) , che rappresenta la mesh ottimizzata.</span><span class="sxs-lookup"><span data-stu-id="48947-130">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the optimized mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48947-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="48947-131">Return value</span></span>

<span data-ttu-id="48947-132">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="48947-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="48947-133">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="48947-133">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="48947-134">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="48947-134">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="48947-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="48947-135">Remarks</span></span>

<span data-ttu-id="48947-136">Questo metodo genera una nuova mesh.</span><span class="sxs-lookup"><span data-stu-id="48947-136">This method generates a new mesh.</span></span> <span data-ttu-id="48947-137">Prima di eseguire l'ottimizzazione, un'applicazione deve generare un buffer adiacenza chiamando [**ID3DXBaseMesh:: GenerateAdjacency**](id3dxbasemesh--generateadjacency.md).</span><span class="sxs-lookup"><span data-stu-id="48947-137">Before running Optimize, an application must generate an adjacency buffer by calling [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md).</span></span> <span data-ttu-id="48947-138">Il buffer adiacenza contiene dati adiacenza, ad esempio un elenco di bordi e i visi adiacenti.</span><span class="sxs-lookup"><span data-stu-id="48947-138">The adjacency buffer contains adjacency data, such as a list of edges and the faces that are adjacent to each other.</span></span>

<span data-ttu-id="48947-139">Questo metodo è molto simile al metodo [**ID3DXBaseMesh:: CloneMesh**](id3dxbasemesh--clonemesh.md) , ad eccezione del fatto che può eseguire l'ottimizzazione durante la generazione del nuovo clone della mesh.</span><span class="sxs-lookup"><span data-stu-id="48947-139">This method is very similar to the [**ID3DXBaseMesh::CloneMesh**](id3dxbasemesh--clonemesh.md) method, except that it can perform optimization while generating the new clone of the mesh.</span></span> <span data-ttu-id="48947-140">La mesh di output eredita tutti i parametri di creazione della mesh di input.</span><span class="sxs-lookup"><span data-stu-id="48947-140">The output mesh inherits all of the creation parameters of the input mesh.</span></span>

## <a name="requirements"></a><span data-ttu-id="48947-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="48947-141">Requirements</span></span>



| <span data-ttu-id="48947-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="48947-142">Requirement</span></span> | <span data-ttu-id="48947-143">Valore</span><span class="sxs-lookup"><span data-stu-id="48947-143">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="48947-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="48947-144">Header</span></span><br/>  | <dl> <span data-ttu-id="48947-145"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="48947-145"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="48947-146">Libreria</span><span class="sxs-lookup"><span data-stu-id="48947-146">Library</span></span><br/> | <dl> <span data-ttu-id="48947-147"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="48947-147"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="48947-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="48947-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48947-149">ID3DXMesh</span><span class="sxs-lookup"><span data-stu-id="48947-149">ID3DXMesh</span></span>](id3dxmesh.md)
</dt> <dt>

[<span data-ttu-id="48947-150">**ID3DXMesh:: OptimizeInplace**</span><span class="sxs-lookup"><span data-stu-id="48947-150">**ID3DXMesh::OptimizeInplace**</span></span>](id3dxmesh--optimizeinplace.md)
</dt> </dl>

 

 
