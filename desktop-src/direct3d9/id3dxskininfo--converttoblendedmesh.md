---
description: Accetta una mesh e restituisce una nuova mesh con pesi di Blend per vertice e una tabella delle combinazioni di osso. La tabella descrive le ossa che influiscono sui subset della mesh.
ms.assetid: c26a9e84-5731-4394-a047-5f1ffe7688d9
title: 'Metodo ID3DXSkinInfo:: ConvertToBlendedMesh (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.ConvertToBlendedMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 051c51291416dd7e190c83433a9bf84baeb92957
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323520"
---
# <a name="id3dxskininfoconverttoblendedmesh-method"></a><span data-ttu-id="9c749-104">Metodo ID3DXSkinInfo:: ConvertToBlendedMesh</span><span class="sxs-lookup"><span data-stu-id="9c749-104">ID3DXSkinInfo::ConvertToBlendedMesh method</span></span>

<span data-ttu-id="9c749-105">Accetta una mesh e restituisce una nuova mesh con pesi di Blend per vertice e una tabella delle combinazioni di osso.</span><span class="sxs-lookup"><span data-stu-id="9c749-105">Takes a mesh and returns a new mesh with per-vertex blend weights and a bone combination table.</span></span> <span data-ttu-id="9c749-106">La tabella descrive le ossa che influiscono sui subset della mesh.</span><span class="sxs-lookup"><span data-stu-id="9c749-106">The table describes which bones affect which subsets of the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c749-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9c749-107">Syntax</span></span>


```C++
HRESULT ConvertToBlendedMesh(
  [in]        LPD3DXMESH   pMesh,
  [in]        DWORD        Options,
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



## <a name="parameters"></a><span data-ttu-id="9c749-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9c749-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c749-109">*pMesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9c749-109">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c749-110">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="9c749-110">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="9c749-111">Mesh di input.</span><span class="sxs-lookup"><span data-stu-id="9c749-111">Input mesh.</span></span> <span data-ttu-id="9c749-112">Vedere [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="9c749-112">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c749-113">*Opzioni* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="9c749-113">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c749-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9c749-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9c749-115">Attualmente non usato.</span><span class="sxs-lookup"><span data-stu-id="9c749-115">Currently unused.</span></span>

</dd> <dt>

<span data-ttu-id="9c749-116">*pAdjacencyIn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9c749-116">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c749-117">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="9c749-117">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9c749-118">Informazioni adiacenza mesh di input.</span><span class="sxs-lookup"><span data-stu-id="9c749-118">Input mesh adjacency information.</span></span>

</dd> <dt>

<span data-ttu-id="9c749-119">*pAdjacencyOut* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9c749-119">*pAdjacencyOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c749-120">Tipo: **[ **LPDWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9c749-120">Type: **[**LPDWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9c749-121">Informazioni adiacenza mesh di output.</span><span class="sxs-lookup"><span data-stu-id="9c749-121">Output mesh adjacency information.</span></span>

</dd> <dt>

<span data-ttu-id="9c749-122">*pFaceRemap* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9c749-122">*pFaceRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9c749-123">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9c749-123">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9c749-124">Matrice di DWORD, una per ogni volto, che identifica la faccia mesh originale che corrisponde a ogni face nella mesh di Blend.</span><span class="sxs-lookup"><span data-stu-id="9c749-124">An array of DWORDs, one per face, that identifies the original mesh face that corresponds to each face in the blended mesh.</span></span> <span data-ttu-id="9c749-125">Se il valore fornito per questo argomento è **null**, non vengono restituiti i dati di riassociazione della faccia.</span><span class="sxs-lookup"><span data-stu-id="9c749-125">If the value supplied for this argument is **NULL**, face remap data is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="9c749-126">*ppVertexRemap* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9c749-126">*ppVertexRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9c749-127">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="9c749-127">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="9c749-128">Indirizzo di un puntatore a un'interfaccia [**ID3DXBuffer**](id3dxbuffer.md) , che contiene un valore DWORD per ogni vertice che specifica la modalità di mapping dei nuovi vertici ai vertici precedenti.</span><span class="sxs-lookup"><span data-stu-id="9c749-128">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, which contains a DWORD for each vertex that specifies how the new vertices map to the old vertices.</span></span> <span data-ttu-id="9c749-129">Questo mapping è utile se è necessario modificare i dati esterni in base al nuovo mapping dei vertici.</span><span class="sxs-lookup"><span data-stu-id="9c749-129">This remap is useful if you need to alter external data based on the new vertex mapping.</span></span> <span data-ttu-id="9c749-130">Questo parametro è facoltativo; È possibile utilizzare **null** .</span><span class="sxs-lookup"><span data-stu-id="9c749-130">This parameter is optional; **NULL** may be used.</span></span>

</dd> <dt>

<span data-ttu-id="9c749-131">*pMaxVertexInfl* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9c749-131">*pMaxVertexInfl* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9c749-132">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9c749-132">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9c749-133">Puntatore a un valore DWORD che conterrà il numero massimo di influenze dell'osso necessarie per ogni vertice per questo metodo di skinning.</span><span class="sxs-lookup"><span data-stu-id="9c749-133">Pointer to a DWORD that will contain the maximum number of bone influences required per vertex for this skinning method.</span></span>

</dd> <dt>

<span data-ttu-id="9c749-134">*pNumBoneCombinations* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9c749-134">*pNumBoneCombinations* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9c749-135">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9c749-135">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9c749-136">Puntatore al numero di ossa nella tabella delle combinazioni di osso.</span><span class="sxs-lookup"><span data-stu-id="9c749-136">Pointer to the number of bones in the bone combination table.</span></span>

</dd> <dt>

<span data-ttu-id="9c749-137">*ppBoneCombinationTable* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9c749-137">*ppBoneCombinationTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9c749-138">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="9c749-138">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="9c749-139">Puntatore alla tabella delle combinazioni di osso.</span><span class="sxs-lookup"><span data-stu-id="9c749-139">Pointer to the bone combination table.</span></span> <span data-ttu-id="9c749-140">I dati sono organizzati in una struttura [**D3DXBONECOMBINATION**](d3dxbonecombination.md) .</span><span class="sxs-lookup"><span data-stu-id="9c749-140">The data is organized in a [**D3DXBONECOMBINATION**](d3dxbonecombination.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9c749-141">*ppMesh* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9c749-141">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9c749-142">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="9c749-142">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="9c749-143">Puntatore alla nuova mesh.</span><span class="sxs-lookup"><span data-stu-id="9c749-143">Pointer to the new mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c749-144">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9c749-144">Return value</span></span>

<span data-ttu-id="9c749-145">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9c749-145">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9c749-146">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9c749-146">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9c749-147">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="9c749-147">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c749-148">Commenti</span><span class="sxs-lookup"><span data-stu-id="9c749-148">Remarks</span></span>

<span data-ttu-id="9c749-149">Ogni elemento nella matrice di modifica del mapping specifica l'indice precedente per tale posizione.</span><span class="sxs-lookup"><span data-stu-id="9c749-149">Each element in the remap array specifies the previous index for that position.</span></span> <span data-ttu-id="9c749-150">Se, ad esempio, un vertice era nella posizione 3 ma è stato rimappato alla posizione 5, il quinto elemento di pVertexRemap conterrà 3.</span><span class="sxs-lookup"><span data-stu-id="9c749-150">For example, if a vertex was in position 3 but has been remapped to position 5, then the fifth element of pVertexRemap will contain 3.</span></span>

<span data-ttu-id="9c749-151">Questo metodo non viene eseguito su hardware che non supporta la fusione di vertici a funzione fissa.</span><span class="sxs-lookup"><span data-stu-id="9c749-151">This method does not run on hardware that does not support fixed-function vertex blending.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c749-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9c749-152">Requirements</span></span>



| <span data-ttu-id="9c749-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c749-153">Requirement</span></span> | <span data-ttu-id="9c749-154">Valore</span><span class="sxs-lookup"><span data-stu-id="9c749-154">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c749-155">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9c749-155">Header</span></span><br/>  | <dl> <span data-ttu-id="9c749-156"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c749-156"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="9c749-157">Libreria</span><span class="sxs-lookup"><span data-stu-id="9c749-157">Library</span></span><br/> | <dl> <span data-ttu-id="9c749-158"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9c749-158"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9c749-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9c749-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c749-160">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="9c749-160">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 
