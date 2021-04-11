---
description: Ricampiona una trama nella parametrizzazione di questo gutterhelper.
ms.assetid: a5ace0e4-2e89-471b-bdfb-67d5e85c6f46
title: 'Metodo ID3DXTextureGutterHelper:: ResampleTex (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.ResampleTex
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0ad8b4cefe0b368cbf81de4ddc030f32cda8fb17
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235136"
---
# <a name="id3dxtexturegutterhelperresampletex-method"></a><span data-ttu-id="ae987-103">Metodo ID3DXTextureGutterHelper:: ResampleTex</span><span class="sxs-lookup"><span data-stu-id="ae987-103">ID3DXTextureGutterHelper::ResampleTex method</span></span>

<span data-ttu-id="ae987-104">Ricampiona una trama nella parametrizzazione di questo gutterhelper.</span><span class="sxs-lookup"><span data-stu-id="ae987-104">Resamples a texture into this gutterhelper's parameterization.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae987-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ae987-105">Syntax</span></span>


```C++
HRESULT ResampleTex(
  [in]  LPDIRECT3DTEXTURE9 pTextureIn,
  [in]  LPD3DXMESH         pMeshIn,
  [in]  D3DDECLUSAGE       Usage,
  [in]  UINT               UsageIndex,
  [out] LPDIRECT3DTEXTURE9 pTextureOut
);
```



## <a name="parameters"></a><span data-ttu-id="ae987-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ae987-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae987-107">*pTextureIn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ae987-107">*pTextureIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae987-108">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="ae987-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="ae987-109">Trama che corrisponde alla parametrizzazione originale in pMeshIn.</span><span class="sxs-lookup"><span data-stu-id="ae987-109">Texture that corresponds to the original parameterization in pMeshIn.</span></span> <span data-ttu-id="ae987-110">Questa trama verrà usata per creare pTextureOut.</span><span class="sxs-lookup"><span data-stu-id="ae987-110">This texture will be used to create pTextureOut.</span></span>

</dd> <dt>

<span data-ttu-id="ae987-111">*pMeshIn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ae987-111">*pMeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae987-112">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="ae987-112">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="ae987-113">Mesh contenente le parametrizzazioni originali e nuove.</span><span class="sxs-lookup"><span data-stu-id="ae987-113">Mesh containing the original and new parameterizations.</span></span> <span data-ttu-id="ae987-114">È necessario archiviare la nuova parametrizzazione in D3DDECLUSAGE \_ TEXCOORD index 0.</span><span class="sxs-lookup"><span data-stu-id="ae987-114">It is required to store the new parameterization in D3DDECLUSAGE\_TEXCOORD index 0.</span></span>

</dd> <dt>

<span data-ttu-id="ae987-115">*Utilizzo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="ae987-115">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae987-116">Tipo: **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**</span><span class="sxs-lookup"><span data-stu-id="ae987-116">Type: **[**D3DDECLUSAGE**](./d3ddeclusage.md)**</span></span>

<span data-ttu-id="ae987-117">Utilizzo dei dati dei vertici (usato in combinazione con UsageIndex) che identifica il componente della dichiarazione di vertice che contiene la parametrizzazione originale in pMeshIn.</span><span class="sxs-lookup"><span data-stu-id="ae987-117">Vertex data usage (used in combination with UsageIndex) which identifies the component of the vertex declaration that contains the original parameterization in pMeshIn.</span></span> <span data-ttu-id="ae987-118">Vedere [**D3DDECLUSAGE**](./d3ddeclusage.md).</span><span class="sxs-lookup"><span data-stu-id="ae987-118">See [**D3DDECLUSAGE**](./d3ddeclusage.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae987-119">*UsageIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ae987-119">*UsageIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae987-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ae987-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ae987-121">Indice in base zero (usato in combinazione con Usage), che identifica il componente della dichiarazione di vertice che contiene la parametrizzazione originale in pMeshIn.</span><span class="sxs-lookup"><span data-stu-id="ae987-121">Zero-based index (used in combination with Usage), which identifies the component of the vertex declaration that contains the original parameterization in pMeshIn.</span></span> <span data-ttu-id="ae987-122">\_Per la nuova parametrizzazione è necessaria la combinazione di D3DDECLUSAGE TEXCOORD e index 0. qualsiasi altra combinazione di utilizzo/indice può essere utilizzata.</span><span class="sxs-lookup"><span data-stu-id="ae987-122">The combination of D3DDECLUSAGE\_TEXCOORD and index 0 is required for the new parameterization; any other usage/index combination may be used.</span></span>

</dd> <dt>

<span data-ttu-id="ae987-123">*pTextureOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ae987-123">*pTextureOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae987-124">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="ae987-124">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="ae987-125">Trama ricampionata.</span><span class="sxs-lookup"><span data-stu-id="ae987-125">Resampled texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae987-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ae987-126">Return value</span></span>

<span data-ttu-id="ae987-127">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ae987-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ae987-128">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ae987-128">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ae987-129">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="ae987-129">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae987-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="ae987-130">Remarks</span></span>

<span data-ttu-id="ae987-131">Una parametrizzazione nel caso di questa funzione è un set di coordinate di trama che esegue il mapping dei triangoli di una mesh ai triangoli di una trama.</span><span class="sxs-lookup"><span data-stu-id="ae987-131">A parameterization in the case of this function is a set of texture coordinates that maps the triangles of a mesh to the triangles on a texture.</span></span> <span data-ttu-id="ae987-132">La nuova parametrizzazione è il set di coordinate di trama contenute nell'interfaccia di supporto della barra di navigazione e la parametrizzazione originale è il set di coordinate di trama contenute all'interno della mesh di input.</span><span class="sxs-lookup"><span data-stu-id="ae987-132">The new parameterization is the set of texture coordinates contained in the gutter helper interface, and the original parameterization is the set of texture coordinates contained within the input mesh.</span></span>

<span data-ttu-id="ae987-133">Si presuppone che le coordinate di trama siano comprese tra 0 e 1, inclusi, e la nuova parametrizzazione deve essere dichiarata nella dichiarazione del vertice come coordinata di trama indice 0.</span><span class="sxs-lookup"><span data-stu-id="ae987-133">It is assumed that texture coordinates are between 0 and 1, inclusive, and the new parameterization must be declared in the vertex declaration as texture coordinate index 0.</span></span> <span data-ttu-id="ae987-134">La trama originale e la trama ricampionata devono avere la stessa larghezza e altezza.</span><span class="sxs-lookup"><span data-stu-id="ae987-134">The original texture and the resampled texture must have the same width and height.</span></span>

<span data-ttu-id="ae987-135">Ad esempio, per preparare il ricampionamento di una trama:</span><span class="sxs-lookup"><span data-stu-id="ae987-135">For example, to prepare for resampling a texture:</span></span>

-   <span data-ttu-id="ae987-136">Creare l'interfaccia di trama originale (pOriginalTex sotto) usando una funzione come [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md).</span><span class="sxs-lookup"><span data-stu-id="ae987-136">Create the original texture interface (pOriginalTex below) using a function like [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md).</span></span>
-   <span data-ttu-id="ae987-137">Creare la nuova interfaccia di trama per la trama ricampionata (pResampledTex di seguito).</span><span class="sxs-lookup"><span data-stu-id="ae987-137">Create the new texture interface for the resampled texture (pResampledTex below).</span></span> <span data-ttu-id="ae987-138">Le dimensioni di questa trama devono corrispondere alla dimensione (larghezza e altezza) della trama di supporto della barra di navigazione.</span><span class="sxs-lookup"><span data-stu-id="ae987-138">The size of this texture must match the size (width and height) of the gutter helper texture.</span></span>
-   <span data-ttu-id="ae987-139">Chiamare [**D3DXCreateTextureGutterHelper**](d3dxcreatetexturegutterhelper.md) per ottenere la nuova parametrizzazione, come illustrato di seguito:</span><span class="sxs-lookup"><span data-stu-id="ae987-139">Call [**D3DXCreateTextureGutterHelper**](d3dxcreatetexturegutterhelper.md) to obtain the new parameterization as shown here:</span></span>


```
// Given:
// pMesh points to a mesh that contains the original and new texture coordinates
ID3DXTextureGutterHelper * pGutterHelper;
    
// Mesh vertex declaration
D3DVERTEXELEMENT9 decl[] = {
    {0,  0, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL, 0},
    // contains new set of texcoords
    {0, 24, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 0}, 
    // contains original set of texcoords
    {0, 32, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 1}, 
    D3DDECL_END()
};
    
// Create a gutter helper with the new parameterization
hr = D3DXCreateTextureGutterHelper(width, height, pMesh, 1, &pGutterHelper);  
    
// Resample the texture
hr = pGutterHelper->ResampleTex(pOriginalTex, pMesh, D3DDECLUSAGE_TEXCOORD, 
           1, pResampledTex); 
    
// Release the gutter helper interface when done with it
```



<span data-ttu-id="ae987-140">Uno scenario comune potrebbe consistere nell'usare UVAtlas per creare un Atlante di trama e quindi usare ResampleTex per ricampionare la trama nella nuova parametrizzazione.</span><span class="sxs-lookup"><span data-stu-id="ae987-140">One common scenario might be to use UVAtlas to create a texture atlas and then use ResampleTex to resample the texture into the new parameterization.</span></span> <span data-ttu-id="ae987-141">Per altre informazioni sugli atlanti, vedere [uso di UVAtlas (Direct3D 9)](using-uvatlas.md).</span><span class="sxs-lookup"><span data-stu-id="ae987-141">For more information about atlases, see [Using UVAtlas (Direct3D 9)](using-uvatlas.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ae987-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ae987-142">Requirements</span></span>



| <span data-ttu-id="ae987-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae987-143">Requirement</span></span> | <span data-ttu-id="ae987-144">Valore</span><span class="sxs-lookup"><span data-stu-id="ae987-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae987-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ae987-145">Header</span></span><br/>  | <dl> <span data-ttu-id="ae987-146"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae987-146"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ae987-147">Libreria</span><span class="sxs-lookup"><span data-stu-id="ae987-147">Library</span></span><br/> | <dl> <span data-ttu-id="ae987-148"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ae987-148"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ae987-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ae987-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae987-150">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="ae987-150">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> <dt>

[<span data-ttu-id="ae987-151">**D3DXUVAtlasCreate**</span><span class="sxs-lookup"><span data-stu-id="ae987-151">**D3DXUVAtlasCreate**</span></span>](d3dxuvatlascreate.md)
</dt> </dl>

 

 
