---
description: Acquisisce una mesh e restituisce una nuova mesh con pesi di Blend per vertice, indici e una tabella combinata Bone. La tabella descrive le tavolozze ossee che influiscono sui subset della mesh.
ms.assetid: e4758a3b-8a45-4ed3-aa62-9713d12afc56
title: 'Metodo ID3DXSkinInfo:: ConvertToIndexedBlendedMesh (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.ConvertToIndexedBlendedMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 87c8a4b943a647e52d7260f1ff53b32b40756761
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323372"
---
# <a name="id3dxskininfoconverttoindexedblendedmesh-method"></a><span data-ttu-id="9998b-104">Metodo ID3DXSkinInfo:: ConvertToIndexedBlendedMesh</span><span class="sxs-lookup"><span data-stu-id="9998b-104">ID3DXSkinInfo::ConvertToIndexedBlendedMesh method</span></span>

<span data-ttu-id="9998b-105">Acquisisce una mesh e restituisce una nuova mesh con pesi di Blend per vertice, indici e una tabella combinata Bone.</span><span class="sxs-lookup"><span data-stu-id="9998b-105">Takes a mesh and returns a new mesh with per-vertex blend weights, indices, and a bone combination table.</span></span> <span data-ttu-id="9998b-106">La tabella descrive le tavolozze ossee che influiscono sui subset della mesh.</span><span class="sxs-lookup"><span data-stu-id="9998b-106">The table describes which bone palettes affect which subsets of the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="9998b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9998b-107">Syntax</span></span>


```C++
HRESULT ConvertToIndexedBlendedMesh(
  [in]        LPD3DXMESH   pMesh,
  [in]        DWORD        Options,
  [in]        DWORD        paletteSize,
  [in]  const DWORD        *pAdjacencyIn,
  [in]        LPDWORD      pAdjacencyOut,
  [out]       DWORD        *pFaceRemap,
  [out]       LPD3DXBUFFER *ppVertexRemap,
  [out]       DWORD        *pMaxVertexInfl,
  [out]       DWORD        *pNumBoneCombinations,
  [out]       LPD3DXBUFFER *ppBoneCombinationTable,
  [out]       LPD3DXMESH   *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="9998b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9998b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9998b-109">*pMesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9998b-109">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9998b-110">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="9998b-110">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="9998b-111">Mesh di input.</span><span class="sxs-lookup"><span data-stu-id="9998b-111">The input mesh.</span></span> <span data-ttu-id="9998b-112">Vedere [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="9998b-112">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="9998b-113">*Opzioni* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="9998b-113">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9998b-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9998b-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9998b-115">Attualmente non usato.</span><span class="sxs-lookup"><span data-stu-id="9998b-115">Currently unused.</span></span>

</dd> <dt>

<span data-ttu-id="9998b-116">*paletteSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9998b-116">*paletteSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9998b-117">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9998b-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9998b-118">Numero di matrici di osso disponibili per la personalizzazione della tavolozza della tabella.</span><span class="sxs-lookup"><span data-stu-id="9998b-118">Number of bone matrices available for matrix palette skinning.</span></span>

</dd> <dt>

<span data-ttu-id="9998b-119">*pAdjacencyIn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9998b-119">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9998b-120">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="9998b-120">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9998b-121">Informazioni adiacenza mesh di input.</span><span class="sxs-lookup"><span data-stu-id="9998b-121">Input mesh adjacency information.</span></span>

</dd> <dt>

<span data-ttu-id="9998b-122">*pAdjacencyOut* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9998b-122">*pAdjacencyOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9998b-123">Tipo: **[ **LPDWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9998b-123">Type: **[**LPDWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9998b-124">Informazioni adiacenza mesh di output.</span><span class="sxs-lookup"><span data-stu-id="9998b-124">Output mesh adjacency information.</span></span>

</dd> <dt>

<span data-ttu-id="9998b-125">*pFaceRemap* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9998b-125">*pFaceRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9998b-126">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9998b-126">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9998b-127">Matrice di DWORD, una per ogni volto, che identifica la faccia mesh originale che corrisponde a ogni face nella mesh di Blend.</span><span class="sxs-lookup"><span data-stu-id="9998b-127">An array of DWORDs, one per face, that identifies the original mesh face that corresponds to each face in the blended mesh.</span></span> <span data-ttu-id="9998b-128">Se il valore fornito per questo argomento è **null**, non vengono restituiti i dati di riassociazione della faccia.</span><span class="sxs-lookup"><span data-stu-id="9998b-128">If the value supplied for this argument is **NULL**, face remap data is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="9998b-129">*ppVertexRemap* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9998b-129">*ppVertexRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9998b-130">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="9998b-130">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="9998b-131">Indirizzo di un puntatore a un'interfaccia [**ID3DXBuffer**](id3dxbuffer.md) , che contiene un valore DWORD per ogni vertice che specifica la modalità di mapping dei nuovi vertici ai vertici precedenti.</span><span class="sxs-lookup"><span data-stu-id="9998b-131">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, which contains a DWORD for each vertex that specifies how the new vertices map to the old vertices.</span></span> <span data-ttu-id="9998b-132">Questo mapping è utile se è necessario modificare i dati esterni in base al nuovo mapping dei vertici.</span><span class="sxs-lookup"><span data-stu-id="9998b-132">This remap is useful if you need to alter external data based on the new vertex mapping.</span></span> <span data-ttu-id="9998b-133">Questo parametro è facoltativo; È possibile utilizzare **null** .</span><span class="sxs-lookup"><span data-stu-id="9998b-133">This parameter is optional; **NULL** may be used.</span></span>

</dd> <dt>

<span data-ttu-id="9998b-134">*pMaxVertexInfl* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9998b-134">*pMaxVertexInfl* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9998b-135">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9998b-135">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9998b-136">Puntatore a un valore DWORD che conterrà il numero massimo di influenze dell'osso necessarie per ogni vertice per questo metodo di skinning.</span><span class="sxs-lookup"><span data-stu-id="9998b-136">Pointer to a DWORD that will contain the maximum number of bone influences required per vertex for this skinning method.</span></span>

</dd> <dt>

<span data-ttu-id="9998b-137">*pNumBoneCombinations* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9998b-137">*pNumBoneCombinations* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9998b-138">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9998b-138">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9998b-139">Puntatore al numero di ossa nella tabella delle combinazioni di osso.</span><span class="sxs-lookup"><span data-stu-id="9998b-139">Pointer to the number of bones in the bone combination table.</span></span>

</dd> <dt>

<span data-ttu-id="9998b-140">*ppBoneCombinationTable* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9998b-140">*ppBoneCombinationTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9998b-141">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="9998b-141">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="9998b-142">Puntatore alla tabella delle combinazioni di osso.</span><span class="sxs-lookup"><span data-stu-id="9998b-142">Pointer to the bone combination table.</span></span> <span data-ttu-id="9998b-143">I dati sono organizzati in una struttura [**D3DXBONECOMBINATION**](d3dxbonecombination.md) .</span><span class="sxs-lookup"><span data-stu-id="9998b-143">The data is organized in a [**D3DXBONECOMBINATION**](d3dxbonecombination.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9998b-144">*ppMesh* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9998b-144">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9998b-145">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="9998b-145">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="9998b-146">Puntatore alla nuova mesh.</span><span class="sxs-lookup"><span data-stu-id="9998b-146">Pointer to the new mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9998b-147">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9998b-147">Return value</span></span>

<span data-ttu-id="9998b-148">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9998b-148">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9998b-149">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9998b-149">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9998b-150">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="9998b-150">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="9998b-151">Commenti</span><span class="sxs-lookup"><span data-stu-id="9998b-151">Remarks</span></span>

<span data-ttu-id="9998b-152">Ogni elemento nelle matrici di riassociazione consente di specificare l'indice precedente per tale posizione.</span><span class="sxs-lookup"><span data-stu-id="9998b-152">Each element in the remap arrays specifies the previous index for that position.</span></span> <span data-ttu-id="9998b-153">Se, ad esempio, un vertice era nella posizione 3 ma è stato rimappato alla posizione 5, il quinto elemento di pVertexRemap conterrà 3.</span><span class="sxs-lookup"><span data-stu-id="9998b-153">For example, if a vertex was in position 3 but has been remapped to position 5, then the fifth element of pVertexRemap will contain 3.</span></span>

<span data-ttu-id="9998b-154">Questo metodo non viene eseguito su hardware che non supporta la fusione di vertici a funzione fissa.</span><span class="sxs-lookup"><span data-stu-id="9998b-154">This method does not run on hardware that does not support fixed-function vertex blending.</span></span>

## <a name="requirements"></a><span data-ttu-id="9998b-155">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9998b-155">Requirements</span></span>



| <span data-ttu-id="9998b-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="9998b-156">Requirement</span></span> | <span data-ttu-id="9998b-157">Valore</span><span class="sxs-lookup"><span data-stu-id="9998b-157">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9998b-158">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9998b-158">Header</span></span><br/>  | <dl> <span data-ttu-id="9998b-159"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="9998b-159"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="9998b-160">Libreria</span><span class="sxs-lookup"><span data-stu-id="9998b-160">Library</span></span><br/> | <dl> <span data-ttu-id="9998b-161"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9998b-161"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9998b-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9998b-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9998b-163">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="9998b-163">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 
