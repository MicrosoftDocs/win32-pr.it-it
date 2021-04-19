---
description: L'interfaccia ID3DXPRTCompBuffer archivia una versione compressa di un buffer ID3DXPRTBuffer per l'uso con l'analisi dei componenti principali (PCA).
ms.assetid: 97f8576c-24d5-4f60-923b-4d8d94382fe9
title: Interfaccia ID3DXPRTCompBuffer (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 323ed6f2bbe9ce4caf495a00330c1b1e0e83e158
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323456"
---
# <a name="id3dxprtcompbuffer-interface"></a><span data-ttu-id="01772-103">Interfaccia ID3DXPRTCompBuffer</span><span class="sxs-lookup"><span data-stu-id="01772-103">ID3DXPRTCompBuffer interface</span></span>

<span data-ttu-id="01772-104">L'interfaccia **ID3DXPRTCompBuffer** archivia una versione compressa di un buffer [**ID3DXPRTBuffer**](id3dxprtbuffer.md) per l'uso con l'analisi dei componenti principali (PCA).</span><span class="sxs-lookup"><span data-stu-id="01772-104">The **ID3DXPRTCompBuffer** interface stores a compressed version of a [**ID3DXPRTBuffer**](id3dxprtbuffer.md) buffer, for use with principal component analysis (PCA).</span></span>

## <a name="members"></a><span data-ttu-id="01772-105">Membri</span><span class="sxs-lookup"><span data-stu-id="01772-105">Members</span></span>

<span data-ttu-id="01772-106">L'interfaccia **ID3DXPRTCompBuffer** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="01772-106">The **ID3DXPRTCompBuffer** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="01772-107">**ID3DXPRTCompBuffer** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="01772-107">**ID3DXPRTCompBuffer** also has these types of members:</span></span>

-   [<span data-ttu-id="01772-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="01772-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="01772-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="01772-109">Methods</span></span>

<span data-ttu-id="01772-110">L'interfaccia **ID3DXPRTCompBuffer** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="01772-110">The **ID3DXPRTCompBuffer** interface has these methods.</span></span>



| <span data-ttu-id="01772-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="01772-111">Method</span></span>                                                             | <span data-ttu-id="01772-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="01772-112">Description</span></span>                                                                                                                                                                                                                        |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="01772-113">**ExtractBasis**</span><span class="sxs-lookup"><span data-stu-id="01772-113">**ExtractBasis**</span></span>](id3dxprtcompbuffer--extractbasis.md)           | <span data-ttu-id="01772-114">Estrae i vettori di base di media e dell'analisi dei componenti principali (PCA) per un determinato cluster da un buffer di dati compresso **ID3DXPRTCompBuffer** .</span><span class="sxs-lookup"><span data-stu-id="01772-114">Extracts the mean and principal component analysis (PCA) basis vectors for a given cluster from an **ID3DXPRTCompBuffer** compressed data buffer.</span></span><br/>                                                                       |
| [<span data-ttu-id="01772-115">**ExtractClusterIDs**</span><span class="sxs-lookup"><span data-stu-id="01772-115">**ExtractClusterIDs**</span></span>](id3dxprtcompbuffer--extractclusterids.md) | <span data-ttu-id="01772-116">Estrae gli ID cluster per campione da un buffer di dati compresso **ID3DXPRTCompBuffer** .</span><span class="sxs-lookup"><span data-stu-id="01772-116">Extracts the per-sample cluster IDs from an **ID3DXPRTCompBuffer** compressed data buffer.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="01772-117">**ExtractPCA**</span><span class="sxs-lookup"><span data-stu-id="01772-117">**ExtractPCA**</span></span>](id3dxprtcompbuffer--extractpca.md)               | <span data-ttu-id="01772-118">Estrae i coefficienti di proiezione dell'analisi dei componenti principale per campione da un buffer di dati compresso **ID3DXPRTCompBuffer** .</span><span class="sxs-lookup"><span data-stu-id="01772-118">Extracts the per-sample principal component analysis (PCA) projection coefficients from an **ID3DXPRTCompBuffer** compressed data buffer.</span></span><br/>                                                                               |
| [<span data-ttu-id="01772-119">**ExtractTexture**</span><span class="sxs-lookup"><span data-stu-id="01772-119">**ExtractTexture**</span></span>](id3dxprtcompbuffer--extracttexture.md)       | <span data-ttu-id="01772-120">Estrae i coefficienti di proiezione del componente principale per campione (PCA) da un buffer di dati compresso **ID3DXPRTCompBuffer** e aggiunge i dati a un oggetto [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .</span><span class="sxs-lookup"><span data-stu-id="01772-120">Extracts the per-sample principal component analysis (PCA) projection coefficients from an **ID3DXPRTCompBuffer** compressed data buffer and adds the data to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) object.</span></span><br/> |
| [<span data-ttu-id="01772-121">**ExtractToMesh**</span><span class="sxs-lookup"><span data-stu-id="01772-121">**ExtractToMesh**</span></span>](id3dxprtcompbuffer--extracttomesh.md)         | <span data-ttu-id="01772-122">Estrae i coefficienti di proiezione del componente principale per campione (PCA) da un buffer di dati compresso **ID3DXPRTCompBuffer** e aggiunge i dati a un oggetto [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="01772-122">Extracts the per-sample principal component analysis (PCA) projection coefficients from an **ID3DXPRTCompBuffer** compressed data buffer and adds the data to an [**ID3DXMesh**](id3dxmesh.md) object.</span></span><br/>                 |
| [<span data-ttu-id="01772-123">**GetHeight**</span><span class="sxs-lookup"><span data-stu-id="01772-123">**GetHeight**</span></span>](id3dxprtcompbuffer--getheight.md)                 | <span data-ttu-id="01772-124">Recupera l'altezza, in pixel, della trama.</span><span class="sxs-lookup"><span data-stu-id="01772-124">Retrieves the height of the texture, in pixels.</span></span><br/>                                                                                                                                                                         |
| [<span data-ttu-id="01772-125">**GetNumChannels**</span><span class="sxs-lookup"><span data-stu-id="01772-125">**GetNumChannels**</span></span>](id3dxprtcompbuffer--getnumchannels.md)       | <span data-ttu-id="01772-126">Recupera il numero di canali di colore utilizzati in memoria per archiviare gli esempi.</span><span class="sxs-lookup"><span data-stu-id="01772-126">Retrieves the number of color channels used in memory to store samples.</span></span><br/>                                                                                                                                                 |
| [<span data-ttu-id="01772-127">**GetNumClusters**</span><span class="sxs-lookup"><span data-stu-id="01772-127">**GetNumClusters**</span></span>](id3dxprtcompbuffer--getnumclusters.md)       | <span data-ttu-id="01772-128">Recupera il numero di cluster da utilizzare per la compressione.</span><span class="sxs-lookup"><span data-stu-id="01772-128">Retrieves the number of clusters to use for compression.</span></span><br/>                                                                                                                                                                |
| [<span data-ttu-id="01772-129">**GetNumCoeffs**</span><span class="sxs-lookup"><span data-stu-id="01772-129">**GetNumCoeffs**</span></span>](id3dxprtcompbuffer--getnumcoeffs.md)           | <span data-ttu-id="01772-130">Recupera il numero di scalari per canale di colore utilizzato in memoria per archiviare gli esempi.</span><span class="sxs-lookup"><span data-stu-id="01772-130">Retrieves the number of scalars per color channel used in memory to store samples.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="01772-131">**GetNumPCA**</span><span class="sxs-lookup"><span data-stu-id="01772-131">**GetNumPCA**</span></span>](id3dxprtcompbuffer--getnumpca.md)                 | <span data-ttu-id="01772-132">Recupera il numero di vettori di base dell'analisi dei componenti principali (PCA) da usare in ogni cluster.</span><span class="sxs-lookup"><span data-stu-id="01772-132">Retrieves the number of principal component analysis (PCA) basis vectors to use in each cluster.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="01772-133">**GetNumSamples**</span><span class="sxs-lookup"><span data-stu-id="01772-133">**GetNumSamples**</span></span>](id3dxprtcompbuffer--getnumsamples.md)         | <span data-ttu-id="01772-134">Recupera il numero di vertici (o Texel) campionati.</span><span class="sxs-lookup"><span data-stu-id="01772-134">Retrieves the number of vertices (or texels) sampled.</span></span><br/>                                                                                                                                                                   |
| [<span data-ttu-id="01772-135">**GetWidth**</span><span class="sxs-lookup"><span data-stu-id="01772-135">**GetWidth**</span></span>](id3dxprtcompbuffer--getwidth.md)                   | <span data-ttu-id="01772-136">Recupera la larghezza della trama in pixel.</span><span class="sxs-lookup"><span data-stu-id="01772-136">Retrieves the width of the texture, in pixels.</span></span><br/>                                                                                                                                                                          |
| [<span data-ttu-id="01772-137">**Trama**</span><span class="sxs-lookup"><span data-stu-id="01772-137">**IsTexture**</span></span>](id3dxprtcompbuffer--istexture.md)                 | <span data-ttu-id="01772-138">Indica se il buffer contiene una trama.</span><span class="sxs-lookup"><span data-stu-id="01772-138">Indicates whether the buffer contains a texture.</span></span><br/>                                                                                                                                                                        |
| [<span data-ttu-id="01772-139">**NormalizeData**</span><span class="sxs-lookup"><span data-stu-id="01772-139">**NormalizeData**</span></span>](id3dxprtcompbuffer--normalizedata.md)         | <span data-ttu-id="01772-140">Normalizza tutti i pesi di analisi del componente principale (PCA) in modo che siano compresi tra-1 e 1.</span><span class="sxs-lookup"><span data-stu-id="01772-140">Normalizes all principal component analysis (PCA) weights so that they are between -1 and 1.</span></span> <span data-ttu-id="01772-141">I vettori di base vengono modificati per riflettere questa normalizzazione.</span><span class="sxs-lookup"><span data-stu-id="01772-141">Basis vectors are modified to reflect this normalization.</span></span><br/>                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="01772-142">Commenti</span><span class="sxs-lookup"><span data-stu-id="01772-142">Remarks</span></span>

<span data-ttu-id="01772-143">L'interfaccia **ID3DXPRTCompBuffer** viene ottenuta chiamando la funzione [**D3DXCreatePRTCompBuffer**](d3dxcreateprtcompbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="01772-143">The **ID3DXPRTCompBuffer** interface is obtained by calling the [**D3DXCreatePRTCompBuffer**](d3dxcreateprtcompbuffer.md) function.</span></span>

<span data-ttu-id="01772-144">Il tipo LPD3DXPRTCOMPBUFFER è definito come puntatore all'interfaccia **ID3DXPRTCompBuffer** .</span><span class="sxs-lookup"><span data-stu-id="01772-144">The LPD3DXPRTCOMPBUFFER type is defined as a pointer to the **ID3DXPRTCompBuffer** interface.</span></span>


```
typedef interface ID3DXPRTCompBuffer ID3DXPRTCompBuffer;
typedef interface ID3DXPRTCompBuffer *LPD3DXPRTCOMPBUFFER;
```



## <a name="requirements"></a><span data-ttu-id="01772-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="01772-145">Requirements</span></span>



| <span data-ttu-id="01772-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="01772-146">Requirement</span></span> | <span data-ttu-id="01772-147">Valore</span><span class="sxs-lookup"><span data-stu-id="01772-147">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="01772-148">Intestazione</span><span class="sxs-lookup"><span data-stu-id="01772-148">Header</span></span><br/>  | <dl> <span data-ttu-id="01772-149"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="01772-149"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="01772-150">Libreria</span><span class="sxs-lookup"><span data-stu-id="01772-150">Library</span></span><br/> | <dl> <span data-ttu-id="01772-151"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="01772-151"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="01772-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="01772-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01772-153">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="01772-153">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[<span data-ttu-id="01772-154">**D3DXCreatePRTCompBuffer**</span><span class="sxs-lookup"><span data-stu-id="01772-154">**D3DXCreatePRTCompBuffer**</span></span>](d3dxcreateprtcompbuffer.md)
</dt> <dt>

[<span data-ttu-id="01772-155">**ID3DXPRTBuffer**</span><span class="sxs-lookup"><span data-stu-id="01772-155">**ID3DXPRTBuffer**</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 
