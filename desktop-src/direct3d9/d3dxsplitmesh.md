---
description: Suddivide una mesh in mesh di dimensioni inferiori a quelle specificate.
ms.assetid: 55cdd82f-91fa-4805-969f-8fbe53cbde58
title: Funzione D3DXSplitMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSplitMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d1f01cdb4ddd009f5cdf0b7f0310a492840955f1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322584"
---
# <a name="d3dxsplitmesh-function"></a><span data-ttu-id="23be2-103">D3DXSplitMesh (funzione)</span><span class="sxs-lookup"><span data-stu-id="23be2-103">D3DXSplitMesh function</span></span>

<span data-ttu-id="23be2-104">Suddivide una mesh in mesh di dimensioni inferiori a quelle specificate.</span><span class="sxs-lookup"><span data-stu-id="23be2-104">Splits a mesh into meshes smaller than the specified size.</span></span>

## <a name="syntax"></a><span data-ttu-id="23be2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="23be2-105">Syntax</span></span>


```C++
void D3DXSplitMesh(
  _In_        LPD3DXMESH   pMeshIn,
  _In_  const DWORD        *pAdjacencyIn,
  _In_  const DWORD        MaxSize,
  _In_  const DWORD        Options,
  _Out_       DWORD        *pMeshesOut,
  _Out_       LPD3DXBUFFER *ppMeshArrayOut,
  _Out_       LPD3DXBUFFER *ppAdjacencyArrayOut,
  _Out_       LPD3DXBUFFER *ppFaceRemapArrayOut,
  _Out_       LPD3DXBUFFER *ppVertRemapArrayOut
);
```



## <a name="parameters"></a><span data-ttu-id="23be2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="23be2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23be2-107">*pMeshIn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="23be2-107">*pMeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23be2-108">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="23be2-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="23be2-109">Puntatore a un'interfaccia [**ID3DXMesh**](id3dxmesh.md) , che rappresenta la mesh di origine.</span><span class="sxs-lookup"><span data-stu-id="23be2-109">Pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the source mesh.</span></span>

</dd> <dt>

<span data-ttu-id="23be2-110">*pAdjacencyIn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="23be2-110">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23be2-111">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="23be2-111">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="23be2-112">Puntatore a una matrice di tre DWORD per volto che specificano i tre elementi adiacenti per ogni viso nella mesh da semplificare.</span><span class="sxs-lookup"><span data-stu-id="23be2-112">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh to be simplified.</span></span>

</dd> <dt>

<span data-ttu-id="23be2-113">*MaxSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="23be2-113">*MaxSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23be2-114">Tipo: **const [**DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="23be2-114">Type: **const [**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="23be2-115">Numero massimo di vertici nel mesh risultante.</span><span class="sxs-lookup"><span data-stu-id="23be2-115">Maximum number of vertices in the resulting mesh.</span></span>

</dd> <dt>

<span data-ttu-id="23be2-116">*Opzioni* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="23be2-116">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23be2-117">Tipo: **const [**DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="23be2-117">Type: **const [**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="23be2-118">Flag di opzione per le nuove mesh.</span><span class="sxs-lookup"><span data-stu-id="23be2-118">Option flags for the new meshes.</span></span>

</dd> <dt>

<span data-ttu-id="23be2-119">*pMeshesOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="23be2-119">*pMeshesOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="23be2-120">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="23be2-120">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="23be2-121">Numero di mesh restituite.</span><span class="sxs-lookup"><span data-stu-id="23be2-121">Number of meshes returned.</span></span>

</dd> <dt>

<span data-ttu-id="23be2-122">*ppMeshArrayOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="23be2-122">*ppMeshArrayOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="23be2-123">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="23be2-123">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="23be2-124">Buffer contenente una matrice di interfacce [**ID3DXMesh**](id3dxmesh.md) per le nuove mesh.</span><span class="sxs-lookup"><span data-stu-id="23be2-124">Buffer containing an array of [**ID3DXMesh**](id3dxmesh.md) interfaces for the new meshes.</span></span> <span data-ttu-id="23be2-125">Per una mesh di origine divisa in n mesh, *ppMeshArrayOut* è una matrice di n puntatori **ID3DXMesh** .</span><span class="sxs-lookup"><span data-stu-id="23be2-125">For a source mesh split into n meshes, *ppMeshArrayOut* is an array of n **ID3DXMesh** pointers.</span></span>

</dd> <dt>

<span data-ttu-id="23be2-126">*ppAdjacencyArrayOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="23be2-126">*ppAdjacencyArrayOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="23be2-127">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="23be2-127">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="23be2-128">Buffer contenente una matrice di matrici adiacenza (DWORD) per le nuove mesh.</span><span class="sxs-lookup"><span data-stu-id="23be2-128">Buffer containing an array of adjacency arrays (DWORDs) for the new meshes.</span></span> <span data-ttu-id="23be2-129">Vedere [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="23be2-129">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span> <span data-ttu-id="23be2-130">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="23be2-130">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="23be2-131">*ppFaceRemapArrayOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="23be2-131">*ppFaceRemapArrayOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="23be2-132">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="23be2-132">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="23be2-133">Buffer contenente una matrice di matrici di mapping delle facce (DWORD) per le nuove mesh.</span><span class="sxs-lookup"><span data-stu-id="23be2-133">Buffer containing an array of face remap arrays (DWORDs) for the new meshes.</span></span> <span data-ttu-id="23be2-134">Vedere [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="23be2-134">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span> <span data-ttu-id="23be2-135">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="23be2-135">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="23be2-136">*ppVertRemapArrayOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="23be2-136">*ppVertRemapArrayOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="23be2-137">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="23be2-137">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="23be2-138">Buffer contenente una matrice di matrici di riassociazione dei vertici per le nuove mesh.</span><span class="sxs-lookup"><span data-stu-id="23be2-138">Buffer containing an array of vertex remap arrays for the new meshes.</span></span> <span data-ttu-id="23be2-139">Vedere [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="23be2-139">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span> <span data-ttu-id="23be2-140">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="23be2-140">This parameter is optional.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23be2-141">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="23be2-141">Return value</span></span>

<span data-ttu-id="23be2-142">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="23be2-142">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="23be2-143">Se la funzione ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="23be2-143">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="23be2-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="23be2-144">Remarks</span></span>

<span data-ttu-id="23be2-145">Un uso comune di questa funzione consiste nel dividere una mesh con indici a 32 bit (più di 65535 vertici) in più di una mesh, ognuno dei quali ha indici a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="23be2-145">A common use of this function is to split a mesh with 32-bit indices (more than 65535 vertices) into more than one mesh, each of which has 16-bit indices.</span></span>

<span data-ttu-id="23be2-146">Le matrici adiacenza, mapping dei vertici e mapping delle facce sono matrici sono DWORD in cui ogni matrice contiene n puntatori DWORD, seguiti dai dati DWORD a cui fanno riferimento i puntatori.</span><span class="sxs-lookup"><span data-stu-id="23be2-146">The adjacency, vertex remap and face remap arrays are arrays are DWORDs where each array contains n DWORD pointers, followed by the DWORD data referenced by the pointers.</span></span> <span data-ttu-id="23be2-147">Per ottenere, ad esempio, le informazioni di modifica del mapping delle facce per la faccia 3 nella mesh 2, è possibile usare il codice seguente, presupponendo che i dati di riassociazione volti siano stati restituiti in una variabile denominata *ppFaceRemapArrayOut*.</span><span class="sxs-lookup"><span data-stu-id="23be2-147">For example, to obtain the face remap information for face 3 in mesh 2, the following code could be used, assuming the face remap data was returned in a variable named *ppFaceRemapArrayOut*.</span></span>


```
   
const DWORD **face_remaps = 
    static_cast<DWORD **>(ppFaceRemapArrayOut->GetBufferPointer());
const DWORD remap = face_remaps[2][3];
```



## <a name="requirements"></a><span data-ttu-id="23be2-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="23be2-148">Requirements</span></span>



| <span data-ttu-id="23be2-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="23be2-149">Requirement</span></span> | <span data-ttu-id="23be2-150">Valore</span><span class="sxs-lookup"><span data-stu-id="23be2-150">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="23be2-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="23be2-151">Header</span></span><br/>  | <dl> <span data-ttu-id="23be2-152"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="23be2-152"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="23be2-153">Libreria</span><span class="sxs-lookup"><span data-stu-id="23be2-153">Library</span></span><br/> | <dl> <span data-ttu-id="23be2-154"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="23be2-154"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="23be2-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="23be2-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23be2-156">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="23be2-156">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
