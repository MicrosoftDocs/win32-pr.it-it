---
description: L'interfaccia ID3DXPRTBuffer viene usata come buffer di dati per archiviare i dati dei vertici e dei pixel per l'uso con funzioni e metodi PRT (pre-Computed Radiance Transfer).
ms.assetid: 36c1fd13-0949-4991-93cb-41ace458802d
title: Interfaccia ID3DXPRTBuffer (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: daadb5b0ad8155062e75ea4eca566a0afbf3631b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323695"
---
# <a name="id3dxprtbuffer-interface"></a><span data-ttu-id="6f92b-103">Interfaccia ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="6f92b-103">ID3DXPRTBuffer interface</span></span>

<span data-ttu-id="6f92b-104">L'interfaccia ID3DXPRTBuffer viene usata come buffer di dati per archiviare i dati dei vertici e dei pixel per l'uso con funzioni e metodi PRT (pre-Computed Radiance Transfer).</span><span class="sxs-lookup"><span data-stu-id="6f92b-104">The ID3DXPRTBuffer interface is used as a data buffer to store vertex and pixel data for use with precomputed radiance transfer (PRT) methods and functions.</span></span>

## <a name="members"></a><span data-ttu-id="6f92b-105">Membri</span><span class="sxs-lookup"><span data-stu-id="6f92b-105">Members</span></span>

<span data-ttu-id="6f92b-106">L'interfaccia **ID3DXPRTBuffer** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="6f92b-106">The **ID3DXPRTBuffer** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6f92b-107">**ID3DXPRTBuffer** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6f92b-107">**ID3DXPRTBuffer** also has these types of members:</span></span>

-   [<span data-ttu-id="6f92b-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="6f92b-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6f92b-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="6f92b-109">Methods</span></span>

<span data-ttu-id="6f92b-110">L'interfaccia **ID3DXPRTBuffer** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="6f92b-110">The **ID3DXPRTBuffer** interface has these methods.</span></span>



| <span data-ttu-id="6f92b-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="6f92b-111">Method</span></span>                                                   | <span data-ttu-id="6f92b-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6f92b-112">Description</span></span>                                                                                                                                                                                   |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6f92b-113">**AddBuffer**</span><span class="sxs-lookup"><span data-stu-id="6f92b-113">**AddBuffer**</span></span>](id3dxprtbuffer--addbuffer.md)           | <span data-ttu-id="6f92b-114">Aggiunge un altro buffer a **ID3DXPRTBuffer** e archivia i risultati in **ID3DXPRTBuffer**.</span><span class="sxs-lookup"><span data-stu-id="6f92b-114">Adds another buffer to the **ID3DXPRTBuffer** and stores the results in **ID3DXPRTBuffer**.</span></span><br/>                                                                                        |
| [<span data-ttu-id="6f92b-115">**AttachGH**</span><span class="sxs-lookup"><span data-stu-id="6f92b-115">**AttachGH**</span></span>](id3dxprtbuffer--attachgh.md)             | <span data-ttu-id="6f92b-116">Associa un oggetto [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) all'oggetto **ID3DXPRTBuffer** .</span><span class="sxs-lookup"><span data-stu-id="6f92b-116">Associates an [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object with the **ID3DXPRTBuffer** object.</span></span><br/>                                                              |
| [<span data-ttu-id="6f92b-117">**EvalGH**</span><span class="sxs-lookup"><span data-stu-id="6f92b-117">**EvalGH**</span></span>](id3dxprtbuffer--evalgh.md)                 | <span data-ttu-id="6f92b-118">Applica i dati della rilegatura di trama archiviati a un buffer di trama **ID3DXPRTBuffer** .</span><span class="sxs-lookup"><span data-stu-id="6f92b-118">Applies stored texture gutter data to an **ID3DXPRTBuffer** texture buffer.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="6f92b-119">**ExtractTexture**</span><span class="sxs-lookup"><span data-stu-id="6f92b-119">**ExtractTexture**</span></span>](id3dxprtbuffer--extracttexture.md) | <span data-ttu-id="6f92b-120">Estrae i dati coefficienti da un canale colori del buffer per un intervallo di coefficienti specificato e aggiunge i dati a un oggetto [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .</span><span class="sxs-lookup"><span data-stu-id="6f92b-120">Extracts coefficient data from a color channel of the buffer for a specified range of coefficients, and adds the data to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) object.</span></span><br/> |
| [<span data-ttu-id="6f92b-121">**ExtractToMesh**</span><span class="sxs-lookup"><span data-stu-id="6f92b-121">**ExtractToMesh**</span></span>](id3dxprtbuffer--extracttomesh.md)   | <span data-ttu-id="6f92b-122">Estrae i dati coefficienti da un buffer a canale singolo e li aggiunge a un oggetto [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="6f92b-122">Extracts coefficient data from a single-channel buffer and adds the data to an [**ID3DXMesh**](id3dxmesh.md) object.</span></span><br/>                                                              |
| [<span data-ttu-id="6f92b-123">**GetHeight**</span><span class="sxs-lookup"><span data-stu-id="6f92b-123">**GetHeight**</span></span>](id3dxprtbuffer--getheight.md)           | <span data-ttu-id="6f92b-124">Recupera l'altezza, in pixel, della trama.</span><span class="sxs-lookup"><span data-stu-id="6f92b-124">Retrieves the height of the texture, in pixels.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="6f92b-125">**GetNumChannels**</span><span class="sxs-lookup"><span data-stu-id="6f92b-125">**GetNumChannels**</span></span>](id3dxprtbuffer--getnumchannels.md) | <span data-ttu-id="6f92b-126">Recupera il numero di canali di colore utilizzati in memoria per archiviare gli esempi.</span><span class="sxs-lookup"><span data-stu-id="6f92b-126">Retrieves the number of color channels used in memory to store samples.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="6f92b-127">**GetNumCoeffs**</span><span class="sxs-lookup"><span data-stu-id="6f92b-127">**GetNumCoeffs**</span></span>](id3dxprtbuffer--getnumcoeffs.md)     | <span data-ttu-id="6f92b-128">Recupera il numero di scalari per canale di colore utilizzato in memoria per archiviare gli esempi.</span><span class="sxs-lookup"><span data-stu-id="6f92b-128">Retrieves the number of scalars per color channel used in memory to store samples.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="6f92b-129">**GetNumSamples**</span><span class="sxs-lookup"><span data-stu-id="6f92b-129">**GetNumSamples**</span></span>](id3dxprtbuffer--getnumsamples.md)   | <span data-ttu-id="6f92b-130">Recupera il numero di vertici (o Texel) campionati.</span><span class="sxs-lookup"><span data-stu-id="6f92b-130">Retrieves the number of vertices (or texels) sampled.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="6f92b-131">**GetWidth**</span><span class="sxs-lookup"><span data-stu-id="6f92b-131">**GetWidth**</span></span>](id3dxprtbuffer--getwidth.md)             | <span data-ttu-id="6f92b-132">Recupera la larghezza della trama in pixel.</span><span class="sxs-lookup"><span data-stu-id="6f92b-132">Retrieves the width of the texture, in pixels.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="6f92b-133">**Trama**</span><span class="sxs-lookup"><span data-stu-id="6f92b-133">**IsTexture**</span></span>](id3dxprtbuffer--istexture.md)           | <span data-ttu-id="6f92b-134">Indica se il buffer contiene una trama.</span><span class="sxs-lookup"><span data-stu-id="6f92b-134">Indicates whether the buffer contains a texture.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="6f92b-135">**LockBuffer**</span><span class="sxs-lookup"><span data-stu-id="6f92b-135">**LockBuffer**</span></span>](id3dxprtbuffer--lockbuffer.md)         | <span data-ttu-id="6f92b-136">Blocca un intervallo di dati di esempio vertici o Texel e ottiene un puntatore alla posizione nella memoria del buffer.</span><span class="sxs-lookup"><span data-stu-id="6f92b-136">Locks a range of vertex or texel sample data and obtains a pointer to the location in buffer memory.</span></span><br/>                                                                               |
| [<span data-ttu-id="6f92b-137">**ReleaseGH**</span><span class="sxs-lookup"><span data-stu-id="6f92b-137">**ReleaseGH**</span></span>](id3dxprtbuffer--releasegh.md)           | <span data-ttu-id="6f92b-138">Annulla l'associazione di un oggetto [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) associato all'oggetto **ID3DXPRTBuffer** .</span><span class="sxs-lookup"><span data-stu-id="6f92b-138">Unassociates an attached [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object with the **ID3DXPRTBuffer** object.</span></span><br/>                                                   |
| [<span data-ttu-id="6f92b-139">**Ridimensionamento**</span><span class="sxs-lookup"><span data-stu-id="6f92b-139">**Resize**</span></span>](id3dxprtbuffer--resize.md)                 | <span data-ttu-id="6f92b-140">Modifica il numero di campioni contenuti nel buffer.</span><span class="sxs-lookup"><span data-stu-id="6f92b-140">Changes the number of samples contained in the buffer.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="6f92b-141">**ScaleBuffer**</span><span class="sxs-lookup"><span data-stu-id="6f92b-141">**ScaleBuffer**</span></span>](id3dxprtbuffer--scalebuffer.md)       | <span data-ttu-id="6f92b-142">Moltiplica ogni valore nel buffer per un valore costante.</span><span class="sxs-lookup"><span data-stu-id="6f92b-142">Multiplies every value in the buffer by a constant value.</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="6f92b-143">**UnlockBuffer**</span><span class="sxs-lookup"><span data-stu-id="6f92b-143">**UnlockBuffer**</span></span>](id3dxprtbuffer--unlockbuffer.md)     | <span data-ttu-id="6f92b-144">Termina la durata del puntatore ppData restituito da [**ID3DXPRTBuffer:: LockBuffer**](id3dxprtbuffer--lockbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="6f92b-144">Ends the lifespan of the ppData pointer returned by [**ID3DXPRTBuffer::LockBuffer**](id3dxprtbuffer--lockbuffer.md).</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="6f92b-145">Commenti</span><span class="sxs-lookup"><span data-stu-id="6f92b-145">Remarks</span></span>

<span data-ttu-id="6f92b-146">L'interfaccia **ID3DXPRTBuffer** viene ottenuta chiamando le funzioni [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) o [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) .</span><span class="sxs-lookup"><span data-stu-id="6f92b-146">The **ID3DXPRTBuffer** interface is obtained by calling the [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) or [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) functions.</span></span>

<span data-ttu-id="6f92b-147">Il tipo LPD3DXPRTBUFFER è definito come puntatore all'interfaccia **ID3DXPRTBuffer** .</span><span class="sxs-lookup"><span data-stu-id="6f92b-147">The LPD3DXPRTBUFFER type is defined as a pointer to the **ID3DXPRTBuffer** interface.</span></span>


```
typedef interface ID3DXPRTBuffer ID3DXPRTBuffer;
typedef interface ID3DXPRTBuffer *LPD3DXPRTBUFFER;
```



## <a name="requirements"></a><span data-ttu-id="6f92b-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6f92b-148">Requirements</span></span>



| <span data-ttu-id="6f92b-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f92b-149">Requirement</span></span> | <span data-ttu-id="6f92b-150">Valore</span><span class="sxs-lookup"><span data-stu-id="6f92b-150">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f92b-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6f92b-151">Header</span></span><br/>  | <dl> <span data-ttu-id="6f92b-152"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f92b-152"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="6f92b-153">Libreria</span><span class="sxs-lookup"><span data-stu-id="6f92b-153">Library</span></span><br/> | <dl> <span data-ttu-id="6f92b-154"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6f92b-154"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6f92b-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6f92b-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f92b-156">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="6f92b-156">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[<span data-ttu-id="6f92b-157">**D3DXCreatePRTBuffer**</span><span class="sxs-lookup"><span data-stu-id="6f92b-157">**D3DXCreatePRTBuffer**</span></span>](d3dxcreateprtbuffer.md)
</dt> <dt>

[<span data-ttu-id="6f92b-158">**D3DXCreatePRTBufferTex**</span><span class="sxs-lookup"><span data-stu-id="6f92b-158">**D3DXCreatePRTBufferTex**</span></span>](d3dxcreateprtbuffertex.md)
</dt> <dt>

[<span data-ttu-id="6f92b-159">**ID3DXPRTCompBuffer**</span><span class="sxs-lookup"><span data-stu-id="6f92b-159">**ID3DXPRTCompBuffer**</span></span>](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
