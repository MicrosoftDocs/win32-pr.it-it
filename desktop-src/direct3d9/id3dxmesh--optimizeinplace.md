---
description: Genera una mesh con visi e vertici riordinati per ottimizzare le prestazioni del disegno. Questo metodo riordina la mesh esistente.
ms.assetid: 2cdaf627-d1d3-44f0-a5ae-9023d4b0de45
title: 'Metodo ID3DXMesh:: OptimizeInplace (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.OptimizeInplace
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f889e0d3754cc1321ffa59eba294038b87991489
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762304"
---
# <a name="id3dxmeshoptimizeinplace-method"></a><span data-ttu-id="14059-104">Metodo ID3DXMesh:: OptimizeInplace</span><span class="sxs-lookup"><span data-stu-id="14059-104">ID3DXMesh::OptimizeInplace method</span></span>

<span data-ttu-id="14059-105">Genera una mesh con visi e vertici riordinati per ottimizzare le prestazioni del disegno.</span><span class="sxs-lookup"><span data-stu-id="14059-105">Generates a mesh with reordered faces and vertices to optimize drawing performance.</span></span> <span data-ttu-id="14059-106">Questo metodo riordina la mesh esistente.</span><span class="sxs-lookup"><span data-stu-id="14059-106">This method reorders the existing mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="14059-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="14059-107">Syntax</span></span>


```C++
HRESULT OptimizeInplace(
  [in]        DWORD        Flags,
  [in]  const DWORD        *pAdjacencyIn,
  [out]       DWORD        *pAdjacencyOut,
  [out]       DWORD        *pFaceRemap,
  [out]       LPD3DXBUFFER *ppVertexRemap
);
```



## <a name="parameters"></a><span data-ttu-id="14059-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="14059-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14059-109">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="14059-109">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14059-110">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="14059-110">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="14059-111">Combinazione di uno o più flag [**D3DXMESHOPT**](./d3dxmeshopt.md) , che specifica il tipo di ottimizzazione da eseguire.</span><span class="sxs-lookup"><span data-stu-id="14059-111">Combination of one or more [**D3DXMESHOPT**](./d3dxmeshopt.md) flags, specifying the type of optimization to perform.</span></span>

</dd> <dt>

<span data-ttu-id="14059-112">*pAdjacencyIn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="14059-112">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14059-113">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="14059-113">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="14059-114">Puntatore a una matrice di tre DWORD per ogni volto che specifica i tre elementi adiacenti per ogni viso nella mesh di origine.</span><span class="sxs-lookup"><span data-stu-id="14059-114">Pointer to an array of three DWORDs per face that specifies the three neighbors for each face in the source mesh.</span></span> <span data-ttu-id="14059-115">Se il bordo non ha visi adiacenti, il valore è 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="14059-115">If the edge has no adjacent faces, the value is 0xffffffff.</span></span>

</dd> <dt>

<span data-ttu-id="14059-116">*pAdjacencyOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="14059-116">*pAdjacencyOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="14059-117">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="14059-117">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="14059-118">Puntatore a una matrice di tre DWORD per ogni volto che specifica i tre elementi adiacenti per ogni viso nella mesh ottimizzata.</span><span class="sxs-lookup"><span data-stu-id="14059-118">Pointer to an array of three DWORDs per face that specifies the three neighbors for each face in the optimized mesh.</span></span> <span data-ttu-id="14059-119">Se il bordo non ha visi adiacenti, il valore è 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="14059-119">If the edge has no adjacent faces, the value is 0xffffffff.</span></span> <span data-ttu-id="14059-120">Se il valore specificato per questo argomento è **null**, i dati adiacenza non vengono restituiti.</span><span class="sxs-lookup"><span data-stu-id="14059-120">If the value supplied for this argument is **NULL**, adjacency data is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="14059-121">*pFaceRemap* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="14059-121">*pFaceRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="14059-122">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="14059-122">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="14059-123">Matrice di DWORD, una per ogni volto, che identifica la faccia mesh originale che corrisponde a ogni face nella mesh ottimizzata.</span><span class="sxs-lookup"><span data-stu-id="14059-123">An array of DWORDs, one per face, that identifies the original mesh face that corresponds to each face in the optimized mesh.</span></span> <span data-ttu-id="14059-124">Se il valore fornito per questo argomento è **null**, non vengono restituiti i dati di riassociazione della faccia.</span><span class="sxs-lookup"><span data-stu-id="14059-124">If the value supplied for this argument is **NULL**, face remap data is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="14059-125">*ppVertexRemap* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="14059-125">*ppVertexRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="14059-126">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="14059-126">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="14059-127">Indirizzo di un puntatore a un'interfaccia [**ID3DXBuffer**](id3dxbuffer.md) , che contiene un valore DWORD per ogni vertice che specifica la modalità di mapping dei nuovi vertici ai vertici precedenti.</span><span class="sxs-lookup"><span data-stu-id="14059-127">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, which contains a DWORD for each vertex that specifies how the new vertices map to the old vertices.</span></span> <span data-ttu-id="14059-128">Questo mapping è utile se è necessario modificare i dati esterni in base al nuovo mapping dei vertici.</span><span class="sxs-lookup"><span data-stu-id="14059-128">This remap is useful if you need to alter external data based on the new vertex mapping.</span></span> <span data-ttu-id="14059-129">Se il valore specificato per questo argomento è **null**, i dati di riassociazione dei vertici non vengono restituiti.</span><span class="sxs-lookup"><span data-stu-id="14059-129">If the value supplied for this argument is **NULL**, vertex remap data is not returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14059-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="14059-130">Return value</span></span>

<span data-ttu-id="14059-131">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="14059-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="14059-132">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="14059-132">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="14059-133">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ CANNOTATTRSORT, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="14059-133">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_CANNOTATTRSORT, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="14059-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="14059-134">Remarks</span></span>

<span data-ttu-id="14059-135">Prima di eseguire **ID3DXMesh:: OptimizeInplace**, un'applicazione deve generare un buffer adiacenza chiamando [**ID3DXBaseMesh:: GenerateAdjacency**](id3dxbasemesh--generateadjacency.md).</span><span class="sxs-lookup"><span data-stu-id="14059-135">Before running **ID3DXMesh::OptimizeInplace**, an application must generate an adjacency buffer by calling [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md).</span></span> <span data-ttu-id="14059-136">Il buffer adiacenza contiene dati adiacenza, ad esempio un elenco di bordi e i visi adiacenti.</span><span class="sxs-lookup"><span data-stu-id="14059-136">The adjacency buffer contains adjacency data, such as a list of edges and the faces that are adjacent to each other.</span></span>

> [!Note]  
> <span data-ttu-id="14059-137">Questo metodo avrà esito negativo se la mesh sta condividendo il buffer dei vertici con un'altra mesh, a meno che D3DXMESHOPT \_ IGNOREVERTS non sia impostato nei flag.</span><span class="sxs-lookup"><span data-stu-id="14059-137">This method will fail if the mesh is sharing its vertex buffer with another mesh, unless the D3DXMESHOPT\_IGNOREVERTS is set in Flags.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="14059-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="14059-138">Requirements</span></span>



| <span data-ttu-id="14059-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="14059-139">Requirement</span></span> | <span data-ttu-id="14059-140">Valore</span><span class="sxs-lookup"><span data-stu-id="14059-140">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="14059-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="14059-141">Header</span></span><br/>  | <dl> <span data-ttu-id="14059-142"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="14059-142"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="14059-143">Libreria</span><span class="sxs-lookup"><span data-stu-id="14059-143">Library</span></span><br/> | <dl> <span data-ttu-id="14059-144"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="14059-144"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="14059-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="14059-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14059-146">ID3DXMesh</span><span class="sxs-lookup"><span data-stu-id="14059-146">ID3DXMesh</span></span>](id3dxmesh.md)
</dt> <dt>

[<span data-ttu-id="14059-147">**ID3DXMesh:: Optimize**</span><span class="sxs-lookup"><span data-stu-id="14059-147">**ID3DXMesh::Optimize**</span></span>](id3dxmesh--optimize.md)
</dt> </dl>

 

 
