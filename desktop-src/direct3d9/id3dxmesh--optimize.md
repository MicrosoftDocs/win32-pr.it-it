---
description: 'Metodo ID3DXMesh::Optimize: genera una nuova mesh con visi e vertici riordinati per ottimizzare le prestazioni del disegno.'
ms.assetid: 6a9bf7b9-2cb9-4b42-92d9-2a121ff79284
title: Metodo ID3DXMesh::Optimize (D3DX9Mesh.h)
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
ms.openlocfilehash: debec1c0ee54e612ab0de832dbc5c2481dcefad8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093309"
---
# <a name="id3dxmeshoptimize-method"></a><span data-ttu-id="4db5c-103">Metodo ID3DXMesh::Optimize</span><span class="sxs-lookup"><span data-stu-id="4db5c-103">ID3DXMesh::Optimize method</span></span>

<span data-ttu-id="4db5c-104">Genera una nuova mesh con visi e vertici riordinati per ottimizzare le prestazioni del disegno.</span><span class="sxs-lookup"><span data-stu-id="4db5c-104">Generates a new mesh with reordered faces and vertices to optimize drawing performance.</span></span>

## <a name="syntax"></a><span data-ttu-id="4db5c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4db5c-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="4db5c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4db5c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4db5c-107">*Flag* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="4db5c-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4db5c-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4db5c-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4db5c-109">Specifica il tipo di ottimizzazione da eseguire.</span><span class="sxs-lookup"><span data-stu-id="4db5c-109">Specifies the type of optimization to perform.</span></span> <span data-ttu-id="4db5c-110">Questo parametro può essere impostato su una combinazione di uno o più flag [**di D3DXMESHOPT**](./d3dxmeshopt.md) e [**D3DXMESH**](./d3dxmesh.md) (ad eccezione di D3DXMESH \_ 32BIT, D3DXMESH \_ IB \_ WRITEONLY e D3DXMESH \_ WRITEONLY).</span><span class="sxs-lookup"><span data-stu-id="4db5c-110">This parameter can be set to a combination of one or more flags from [**D3DXMESHOPT**](./d3dxmeshopt.md) and [**D3DXMESH**](./d3dxmesh.md) (except D3DXMESH\_32BIT, D3DXMESH\_IB\_WRITEONLY, and D3DXMESH\_WRITEONLY).</span></span>

</dd> <dt>

<span data-ttu-id="4db5c-111">*pAdjacencyIn* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="4db5c-111">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4db5c-112">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="4db5c-112">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="4db5c-113">Puntatore a una matrice di tre DWORD per ogni viso che specifica i tre elementi adiacenti per ogni viso nella mesh di origine.</span><span class="sxs-lookup"><span data-stu-id="4db5c-113">Pointer to an array of three DWORDs per face that specifies the three neighbors for each face in the source mesh.</span></span> <span data-ttu-id="4db5c-114">Se il bordo non ha visi adiacenti, il valore è 0xffffffff.</span><span class="sxs-lookup"><span data-stu-id="4db5c-114">If the edge has no adjacent faces, the value is 0xffffffff.</span></span> <span data-ttu-id="4db5c-115">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="4db5c-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="4db5c-116">*pAdjacencyOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="4db5c-116">*pAdjacencyOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4db5c-117">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="4db5c-117">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="4db5c-118">Puntatore a una matrice di tre DWORD per ogni viso che specifica i tre elementi adiacenti per ogni viso nella mesh ottimizzata.</span><span class="sxs-lookup"><span data-stu-id="4db5c-118">Pointer to an array of three DWORDs per face that specifies the three neighbors for each face in the optimized mesh.</span></span> <span data-ttu-id="4db5c-119">Se il bordo non ha visi adiacenti, il valore è 0xffffffff.</span><span class="sxs-lookup"><span data-stu-id="4db5c-119">If the edge has no adjacent faces, the value is 0xffffffff.</span></span>

</dd> <dt>

<span data-ttu-id="4db5c-120">*pFaceRemap* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="4db5c-120">*pFaceRemap* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4db5c-121">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="4db5c-121">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="4db5c-122">Matrice di DWORD, uno per ogni viso, che identifica il viso della mesh originale corrispondente a ogni viso nella mesh ottimizzata.</span><span class="sxs-lookup"><span data-stu-id="4db5c-122">An array of DWORDs, one per face, that identifies the original mesh face that corresponds to each face in the optimized mesh.</span></span> <span data-ttu-id="4db5c-123">Se il valore fornito per questo argomento è **NULL,** i dati di modifica del mapping dei visi non vengono restituiti.</span><span class="sxs-lookup"><span data-stu-id="4db5c-123">If the value supplied for this argument is **NULL**, face remap data is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="4db5c-124">*ppVertexRemap* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="4db5c-124">*ppVertexRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4db5c-125">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="4db5c-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="4db5c-126">Indirizzo di un puntatore a un'interfaccia [**ID3DXBuffer,**](id3dxbuffer.md) che contiene un valore DWORD per ogni vertice che specifica il mapping dei nuovi vertici ai vertici vecchi.</span><span class="sxs-lookup"><span data-stu-id="4db5c-126">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, which contains a DWORD for each vertex that specifies how the new vertices map to the old vertices.</span></span> <span data-ttu-id="4db5c-127">Questo nuovo mapping è utile se è necessario modificare i dati esterni in base al nuovo mapping dei vertici.</span><span class="sxs-lookup"><span data-stu-id="4db5c-127">This remap is useful if you need to alter external data based on the new vertex mapping.</span></span>

</dd> <dt>

<span data-ttu-id="4db5c-128">*ppOptMesh* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="4db5c-128">*ppOptMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4db5c-129">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="4db5c-129">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="4db5c-130">Indirizzo di un puntatore a [**un'interfaccia ID3DXMesh,**](id3dxmesh.md) che rappresenta la mesh ottimizzata.</span><span class="sxs-lookup"><span data-stu-id="4db5c-130">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the optimized mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4db5c-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4db5c-131">Return value</span></span>

<span data-ttu-id="4db5c-132">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4db5c-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4db5c-133">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4db5c-133">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4db5c-134">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="4db5c-134">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="4db5c-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="4db5c-135">Remarks</span></span>

<span data-ttu-id="4db5c-136">Questo metodo genera una nuova mesh.</span><span class="sxs-lookup"><span data-stu-id="4db5c-136">This method generates a new mesh.</span></span> <span data-ttu-id="4db5c-137">Prima di eseguire Optimize, un'applicazione deve generare un buffer di adiacenza chiamando [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md).</span><span class="sxs-lookup"><span data-stu-id="4db5c-137">Before running Optimize, an application must generate an adjacency buffer by calling [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md).</span></span> <span data-ttu-id="4db5c-138">Il buffer di adienze contiene dati di adizia, ad esempio un elenco di bordi e le facce adiacenti l'una all'altra.</span><span class="sxs-lookup"><span data-stu-id="4db5c-138">The adjacency buffer contains adjacency data, such as a list of edges and the faces that are adjacent to each other.</span></span>

<span data-ttu-id="4db5c-139">Questo metodo è molto simile al metodo [**ID3DXBaseMesh::CloneMesh,**](id3dxbasemesh--clonemesh.md) ad eccezione del fatto che può eseguire l'ottimizzazione durante la generazione del nuovo clone della mesh.</span><span class="sxs-lookup"><span data-stu-id="4db5c-139">This method is very similar to the [**ID3DXBaseMesh::CloneMesh**](id3dxbasemesh--clonemesh.md) method, except that it can perform optimization while generating the new clone of the mesh.</span></span> <span data-ttu-id="4db5c-140">La mesh di output eredita tutti i parametri di creazione della mesh di input.</span><span class="sxs-lookup"><span data-stu-id="4db5c-140">The output mesh inherits all of the creation parameters of the input mesh.</span></span>

## <a name="requirements"></a><span data-ttu-id="4db5c-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4db5c-141">Requirements</span></span>



| <span data-ttu-id="4db5c-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="4db5c-142">Requirement</span></span> | <span data-ttu-id="4db5c-143">Valore</span><span class="sxs-lookup"><span data-stu-id="4db5c-143">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4db5c-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4db5c-144">Header</span></span><br/>  | <dl> <span data-ttu-id="4db5c-145"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="4db5c-145"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="4db5c-146">Libreria</span><span class="sxs-lookup"><span data-stu-id="4db5c-146">Library</span></span><br/> | <dl> <span data-ttu-id="4db5c-147"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="4db5c-147"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4db5c-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4db5c-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4db5c-149">ID3DXMesh</span><span class="sxs-lookup"><span data-stu-id="4db5c-149">ID3DXMesh</span></span>](id3dxmesh.md)
</dt> <dt>

[<span data-ttu-id="4db5c-150">**ID3DXMesh::OptimizeInplace**</span><span class="sxs-lookup"><span data-stu-id="4db5c-150">**ID3DXMesh::OptimizeInplace**</span></span>](id3dxmesh--optimizeinplace.md)
</dt> </dl>

 

 
