---
description: Eseguire il skining del software su una matrice di vertici.
ms.assetid: 6c1a713f-4ae7-4ee2-afa6-079dd8354fe7
title: Metodo ID3DX10SkinInfo::D oSoftwareSkinning (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.DoSoftwareSkinning
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 54dfe909e36be0273e0679a824ff0674b0e3b38c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322744"
---
# <a name="id3dx10skininfodosoftwareskinning-method"></a><span data-ttu-id="8e5e4-103">ID3DX10SkinInfo::D Metodo oSoftwareSkinning</span><span class="sxs-lookup"><span data-stu-id="8e5e4-103">ID3DX10SkinInfo::DoSoftwareSkinning method</span></span>

<span data-ttu-id="8e5e4-104">Eseguire il skining del software su una matrice di vertici.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-104">Do software skinning on an array of vertices.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e5e4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8e5e4-105">Syntax</span></span>


```C++
HRESULT DoSoftwareSkinning(
  [in]      UINT                    StartVertex,
  [in]      UINT                    VertexCount,
  [in]      void                    *pSrcVertices,
  [in]      UINT                    SrcStride,
  [in, out] void                    *pDestVertices,
  [in]      UINT                    DestStride,
  [in]      D3DXMATRIX              *pBoneMatrices,
  [in]      D3DXMATRIX              *pInverseTransposeBoneMatrices,
  [in]      D3DX10_SKINNING_CHANNEL *pChannelDescs,
  [in]      UINT                    NumChannels
);
```



## <a name="parameters"></a><span data-ttu-id="8e5e4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8e5e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e5e4-107">*StartVertex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8e5e4-107">*StartVertex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e5e4-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8e5e4-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8e5e4-109">Un indice in base 0 in pSrcVertices.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-109">A 0-based index into pSrcVertices.</span></span>

</dd> <dt>

<span data-ttu-id="8e5e4-110">*VertexCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8e5e4-110">*VertexCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e5e4-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8e5e4-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8e5e4-112">Numero di vertici da trasformare.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-112">Number of vertices to transform.</span></span>

</dd> <dt>

<span data-ttu-id="8e5e4-113">*pSrcVertices* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8e5e4-113">*pSrcVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e5e4-114">Tipo: **void \***</span><span class="sxs-lookup"><span data-stu-id="8e5e4-114">Type: **void\***</span></span>

<span data-ttu-id="8e5e4-115">Puntatore a una matrice di vertici da trasformare.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-115">Pointer to an array of vertices to transform.</span></span>

</dd> <dt>

<span data-ttu-id="8e5e4-116">*SrcStride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8e5e4-116">*SrcStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e5e4-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8e5e4-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8e5e4-118">Dimensione, in byte, di un vertice in pSrcVertices.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-118">The size, in bytes, of a vertex in pSrcVertices.</span></span>

</dd> <dt>

<span data-ttu-id="8e5e4-119">*pDestVertices* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="8e5e4-119">*pDestVertices* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8e5e4-120">Tipo: **void \***</span><span class="sxs-lookup"><span data-stu-id="8e5e4-120">Type: **void\***</span></span>

<span data-ttu-id="8e5e4-121">Puntatore a una matrice di vertici, che verrà riempito con i vertici trasformati.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-121">Pointer to an array of vertices, which will be filled with the transformed vertices.</span></span>

</dd> <dt>

<span data-ttu-id="8e5e4-122">*DestStride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8e5e4-122">*DestStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e5e4-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8e5e4-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8e5e4-124">Dimensione, in byte, di un vertice in pDestVertices.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-124">The size, in bytes, of a vertex in pDestVertices.</span></span>

</dd> <dt>

<span data-ttu-id="8e5e4-125">*pBoneMatrices* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8e5e4-125">*pBoneMatrices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e5e4-126">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="8e5e4-126">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="8e5e4-127">Matrice di matrici che verrà usata per trasformare i punti di cui è stato eseguito il mapping a ogni osso, in modo che i vertici mappati a Bone \[ i \] verranno trasformati da pBoneMatrices \[ i \] .</span><span class="sxs-lookup"><span data-stu-id="8e5e4-127">An array of matrices that will be used to transform the points mapped to each bone, such that the vertices mapped to bone\[i\] will be transformed by pBoneMatrices\[i\].</span></span> <span data-ttu-id="8e5e4-128">Questa matrice verrà utilizzata per trasformare le matrici solo se il valore di pChannelDescs è impostato su **false**. in caso contrario, verrà utilizzato pInverseTransposeBoneMatrices.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-128">This array will be used to transform the matrices only if the IsNormal value in pChannelDescs is set to **FALSE**, otherwise pInverseTransposeBoneMatrices will be used.</span></span>

</dd> <dt>

<span data-ttu-id="8e5e4-129">*pInverseTransposeBoneMatrices* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8e5e4-129">*pInverseTransposeBoneMatrices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e5e4-130">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="8e5e4-130">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="8e5e4-131">Se questo valore è **null**, verrà impostato su un valore uguale a pBoneMatrices.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-131">If this value is **NULL**, it will be set equal to pBoneMatrices.</span></span> <span data-ttu-id="8e5e4-132">Questa matrice di matrici verrà utilizzata per trasformare i vertici solo se il valore di pChannelDescs è impostato su **true**; in caso contrario, verrà utilizzato pBoneMatrices.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-132">This array of matrices will be used to transform the vertices only if the IsNormal value in pChannelDescs is set to **TRUE**, otherwise pBoneMatrices will be used.</span></span>

</dd> <dt>

<span data-ttu-id="8e5e4-133">*pChannelDescs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8e5e4-133">*pChannelDescs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e5e4-134">Tipo: **[ **d3dx10 \_ Skin \_ Channel**](d3dx10-skinning-channel.md)\***</span><span class="sxs-lookup"><span data-stu-id="8e5e4-134">Type: **[**D3DX10\_SKINNING\_CHANNEL**](d3dx10-skinning-channel.md)\***</span></span>

<span data-ttu-id="8e5e4-135">Puntatore a una \_ struttura del canale di skinning di d3dx10 \_ , che determina il membro del vertice decl in cui verrà eseguita la skining del software.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-135">Pointer to a D3DX10\_SKINNING\_CHANNEL structure, which determines the member of the vertex decl the software skinning will be done on.</span></span>

</dd> <dt>

<span data-ttu-id="8e5e4-136">*NumChannels* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8e5e4-136">*NumChannels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e5e4-137">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8e5e4-137">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8e5e4-138">Il numero di strutture del canale di D3DX10 \_ Skinning \_ in pChannelDescs.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-138">The number of D3DX10\_SKINNING\_CHANNEL structures in pChannelDescs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e5e4-139">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8e5e4-139">Return value</span></span>

<span data-ttu-id="8e5e4-140">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8e5e4-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8e5e4-141">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-141">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="8e5e4-142">Se il metodo ha esito negativo, il valore restituito può essere: E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-142">If the method fails, the return value can be: E\_INVALIDARG.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e5e4-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="8e5e4-143">Remarks</span></span>

<span data-ttu-id="8e5e4-144">Di seguito è riportato un esempio di come usare la skining del software:</span><span class="sxs-lookup"><span data-stu-id="8e5e4-144">Here is an example of how to use software skinning:</span></span>


```
//vertex definition
struct MyVertex
{
    D3DXVECTOR3 Position;
    D3DXVECTOR2 Weight;
    D3DXVECTOR2 TexCoord;
};

//create vertex data
const UINT numVertices = 16;
MyVertex vertices[numVertices] = {...};
MyVertex destVertices[numVertices];

//create bone matrices
D3DXMATRIX boneMatrices[2];
D3DXMatrixIdentity(&boneMatrices[0]);
D3DXMatrixRotationX(&boneMatrices[1], 3.14159f / 180.0f);

//create bone indices and weights
UINT boneIndices[numVertices] = {...};
float boneWeights[2][numVertices] = {...};

//create skin info, populate it with bones and vertices, and then map them to each other
ID3DX10SkinInfo *pSkinInfo = NULL;
D3DX10CreateSkinInfo(&pSkinInfo);
pSkinInfo->AddBones(2);
pSkinInfo->AddVertices(numVertices);
pSkinInfo->AddBoneInfluences(0, numVertices, boneIndices, boneWeights[0]);
pSkinInfo->AddBoneInfluences(1, numVertices, boneIndices, boneWeights[1]);

//create channel desc
D3DX10_SKINNING_CHANNEL channelDesc;
channelDesc.SrcOffset = 0;
channelDesc.DestOffset = 0;
channelDesc.IsNormal = FALSE;

//do the skinning
pSkinInfo->DoSoftwareSkinning(0, numVertices,
                              vertices, sizeof(MyVertex), 
                              destVertices, sizeof(MyVertex), 
                              boneMatrices, NULL, 
                              &channelDesc, 1);
```



## <a name="requirements"></a><span data-ttu-id="8e5e4-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8e5e4-145">Requirements</span></span>



| <span data-ttu-id="8e5e4-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e5e4-146">Requirement</span></span> | <span data-ttu-id="8e5e4-147">Valore</span><span class="sxs-lookup"><span data-stu-id="8e5e4-147">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8e5e4-148">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8e5e4-148">Header</span></span><br/>  | <dl> <span data-ttu-id="8e5e4-149"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e5e4-149"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="8e5e4-150">Libreria</span><span class="sxs-lookup"><span data-stu-id="8e5e4-150">Library</span></span><br/> | <dl> <span data-ttu-id="8e5e4-151"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8e5e4-151"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e5e4-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8e5e4-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e5e4-153">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="8e5e4-153">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="8e5e4-154">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="8e5e4-154">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
