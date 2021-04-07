---
description: Uso di trame compresse (Direct3D 9)
ms.assetid: 60892a8b-93f4-43ba-87ef-d5c7cc6fb8c6
title: Uso di trame compresse (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 643b0618043f12ff3e1a84b806c86edb780ad929
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747602"
---
# <a name="using-compressed-textures-direct3d-9"></a><span data-ttu-id="148d4-103">Uso di trame compresse (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="148d4-103">Using Compressed Textures (Direct3D 9)</span></span>

## <a name="determining-support-for-compressed-textures"></a><span data-ttu-id="148d4-104">Determinazione del supporto per le trame compresse</span><span class="sxs-lookup"><span data-stu-id="148d4-104">Determining Support for Compressed Textures</span></span>

<span data-ttu-id="148d4-105">Per eseguire il test dell'adapter, specificare qualsiasi formato pixel che usa DXT1, DXT2, DXT3, DXT4 o DXT5.</span><span class="sxs-lookup"><span data-stu-id="148d4-105">To test the adapter, specify any pixel format that uses the DXT1, DXT2, DXT3, DXT4, or DXT5.</span></span> <span data-ttu-id="148d4-106">Se [**IDirect3D9:: CheckDeviceFormat**](/windows/desktop/api) restituisce D3D \_ OK, il dispositivo può creare una trama direttamente da una superficie di trama compressa che usa tale formato.</span><span class="sxs-lookup"><span data-stu-id="148d4-106">If [**IDirect3D9::CheckDeviceFormat**](/windows/desktop/api) returns D3D\_OK, the device can create texture directly from a compressed texture surface that uses that format.</span></span> <span data-ttu-id="148d4-107">In tal caso, è possibile usare le superfici di trama compresse direttamente con Direct3D chiamando il metodo [**IDirect3DDevice9:: setexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) .</span><span class="sxs-lookup"><span data-stu-id="148d4-107">If so, you can use compressed texture surfaces directly with Direct3D by calling the [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) method.</span></span> <span data-ttu-id="148d4-108">Nell'esempio di codice riportato di seguito viene illustrato come determinare se l'adapter supporta un formato di trama compresso.</span><span class="sxs-lookup"><span data-stu-id="148d4-108">The following code example shows how to determine if the adapter supports a compressed texture format.</span></span>


```
BOOL IsCompressedTextureFormatOk( D3DFORMAT TextureFormat, 
                                  D3DFORMAT AdapterFormat ) 
{
    HRESULT hr = pD3D->CheckDeviceFormat( D3DADAPTER_DEFAULT,
                                          D3DDEVTYPE_HAL,
                                          AdapterFormat,
                                          0,
                                          D3DRTYPE_TEXTURE,
                                          TextureFormat);

    return SUCCEEDED( hr );
}
```



<span data-ttu-id="148d4-109">Se il dispositivo non supporta la texturing da superfici di trama compresse, è comunque possibile archiviare i dati di trama in una superficie di formato compresso, ma è necessario convertire le trame compresse in un formato supportato prima di poterle usare per il texturing.</span><span class="sxs-lookup"><span data-stu-id="148d4-109">If the device does not support texturing from compressed texture surfaces, you can still store texture data in a compressed format surface, but you must convert any compressed textures to a supported format before they can be used for texturing.</span></span>

## <a name="creating-compressed-textures"></a><span data-ttu-id="148d4-110">Creazione di trame compresse</span><span class="sxs-lookup"><span data-stu-id="148d4-110">Creating Compressed Textures</span></span>

<span data-ttu-id="148d4-111">Dopo aver creato un dispositivo che supporta un formato di trama compresso sulla scheda, è possibile creare una risorsa di trama compressa.</span><span class="sxs-lookup"><span data-stu-id="148d4-111">After creating a device that supports a compressed texture format on the adapter, you can create a compressed texture resource.</span></span> <span data-ttu-id="148d4-112">Chiamare [**IDirect3DDevice9:: createTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) e specificare un formato di trama compresso per il parametro format.</span><span class="sxs-lookup"><span data-stu-id="148d4-112">Call [**IDirect3DDevice9::CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) and specify a compressed texture format for the Format parameter.</span></span>

<span data-ttu-id="148d4-113">Prima di caricare un'immagine in un oggetto trama, recuperare un puntatore alla superficie della trama chiamando il metodo [**IDirect3DTexture9:: GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel) .</span><span class="sxs-lookup"><span data-stu-id="148d4-113">Before loading an image into a texture object, retrieve a pointer to the texture surface by calling the [**IDirect3DTexture9::GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel) method.</span></span>

<span data-ttu-id="148d4-114">A questo punto è possibile usare qualsiasi funzione D3DXLoadSurfacexxx per caricare un'immagine nell'area recuperata tramite [**IDirect3DTexture9:: GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel).</span><span class="sxs-lookup"><span data-stu-id="148d4-114">Now you can use any D3DXLoadSurfacexxx function to load an image to the surface that was retrieved by using [**IDirect3DTexture9::GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel).</span></span> <span data-ttu-id="148d4-115">Queste funzioni gestiscono la conversione da e verso formati di trama compressi.</span><span class="sxs-lookup"><span data-stu-id="148d4-115">These functions handle conversion to and from compressed texture formats.</span></span>

<span data-ttu-id="148d4-116">È possibile creare e convertire file di trama compressi (DDS) usando l'editor di trame DirectX (Dxtex.exe) fornito con DirectX SDK.</span><span class="sxs-lookup"><span data-stu-id="148d4-116">You can create and convert compressed texture (DDS) files using the DirectX Texture Editor (Dxtex.exe) supplied with the DirectX SDK.</span></span> <span data-ttu-id="148d4-117">È possibile ottenere Dxtex.exe e ottenere informazioni su di esso da DirectX SDK.</span><span class="sxs-lookup"><span data-stu-id="148d4-117">You can get Dxtex.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="148d4-118">Per informazioni su DirectX SDK, vedere [dove è DirectX SDK?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="148d4-118">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

<span data-ttu-id="148d4-119">Il vantaggio di questo comportamento è che un'applicazione può copiare il contenuto di una superficie compressa in un file senza calcolare la quantità di spazio di archiviazione necessaria per una superficie di una particolare larghezza e altezza nel formato specifico.</span><span class="sxs-lookup"><span data-stu-id="148d4-119">The advantage of this behavior is that an application can copy the contents of a compressed surface to a file without calculating how much storage is required for a surface of a particular width and height in the specific format.</span></span>

<span data-ttu-id="148d4-120">La tabella seguente illustra i cinque tipi di trame compresse.</span><span class="sxs-lookup"><span data-stu-id="148d4-120">The following table shows the five types of compressed textures.</span></span> <span data-ttu-id="148d4-121">Per altre informazioni sulla modalità di archiviazione dei dati, vedere [formati di trama compressi (Direct3D 9)](compressed-texture-formats.md).</span><span class="sxs-lookup"><span data-stu-id="148d4-121">For more information about how the data is stored, see [Compressed Texture Formats (Direct3D 9)](compressed-texture-formats.md).</span></span> <span data-ttu-id="148d4-122">Queste informazioni sono necessarie solo se si scrivono routine di compressione personalizzate.</span><span class="sxs-lookup"><span data-stu-id="148d4-122">You only need this information if you are writing your own compression routines.</span></span>



| <span data-ttu-id="148d4-123">FOURCC</span><span class="sxs-lookup"><span data-stu-id="148d4-123">FOURCC</span></span> | <span data-ttu-id="148d4-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="148d4-124">Description</span></span>        | <span data-ttu-id="148d4-125">Alfa premoltiplicato?</span><span class="sxs-lookup"><span data-stu-id="148d4-125">Alpha premultiplied?</span></span> |
|--------|--------------------|----------------------|
| <span data-ttu-id="148d4-126">DXT1</span><span class="sxs-lookup"><span data-stu-id="148d4-126">DXT1</span></span>   | <span data-ttu-id="148d4-127">Alfa opaco/1 bit</span><span class="sxs-lookup"><span data-stu-id="148d4-127">Opaque/1-bit alpha</span></span> | <span data-ttu-id="148d4-128">N/D</span><span class="sxs-lookup"><span data-stu-id="148d4-128">N/A</span></span>                  |
| <span data-ttu-id="148d4-129">DXT2</span><span class="sxs-lookup"><span data-stu-id="148d4-129">DXT2</span></span>   | <span data-ttu-id="148d4-130">Alfa esplicito</span><span class="sxs-lookup"><span data-stu-id="148d4-130">Explicit alpha</span></span>     | <span data-ttu-id="148d4-131">Sì</span><span class="sxs-lookup"><span data-stu-id="148d4-131">Yes</span></span>                  |
| <span data-ttu-id="148d4-132">DXT3</span><span class="sxs-lookup"><span data-stu-id="148d4-132">DXT3</span></span>   | <span data-ttu-id="148d4-133">Alfa esplicito</span><span class="sxs-lookup"><span data-stu-id="148d4-133">Explicit alpha</span></span>     | <span data-ttu-id="148d4-134">No</span><span class="sxs-lookup"><span data-stu-id="148d4-134">No</span></span>                   |
| <span data-ttu-id="148d4-135">DXT4</span><span class="sxs-lookup"><span data-stu-id="148d4-135">DXT4</span></span>   | <span data-ttu-id="148d4-136">Alfa interpolata</span><span class="sxs-lookup"><span data-stu-id="148d4-136">Interpolated alpha</span></span> | <span data-ttu-id="148d4-137">Sì</span><span class="sxs-lookup"><span data-stu-id="148d4-137">Yes</span></span>                  |
| <span data-ttu-id="148d4-138">DXT5</span><span class="sxs-lookup"><span data-stu-id="148d4-138">DXT5</span></span>   | <span data-ttu-id="148d4-139">Alfa interpolata</span><span class="sxs-lookup"><span data-stu-id="148d4-139">Interpolated alpha</span></span> | <span data-ttu-id="148d4-140">No</span><span class="sxs-lookup"><span data-stu-id="148d4-140">No</span></span>                   |



 

<span data-ttu-id="148d4-141">Quando si trasferiscono i dati da un formato NonPremultiplied a un formato premoltiplicato, Direct3D ridimensiona i colori in base ai valori alfa.</span><span class="sxs-lookup"><span data-stu-id="148d4-141">When you transfer data from a nonpremultiplied format to a premultiplied format, Direct3D scales the colors based on the alpha values.</span></span> <span data-ttu-id="148d4-142">Il trasferimento dei dati da un formato premoltiplicato a un formato NonPremultiplied non è supportato.</span><span class="sxs-lookup"><span data-stu-id="148d4-142">Transferring data from a premultiplied format to a nonpremultiplied format is not supported.</span></span> <span data-ttu-id="148d4-143">Se si tenta di trasferire i dati da un'origine alfa premoltiplicata a una destinazione NonPremultiplied Alpha, il metodo restituisce D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="148d4-143">If you try to transfer data from a premultiplied alpha source to a nonpremultiplied alpha destination, the method returns D3DERR\_INVALIDCALL.</span></span> <span data-ttu-id="148d4-144">Se si trasferiscono i dati da un'origine alfa premoltiplicata a una destinazione senza Alpha, i componenti del colore di origine, che sono stati ridimensionati da Alpha, vengono copiati così come sono.</span><span class="sxs-lookup"><span data-stu-id="148d4-144">If you transfer data from a premultiplied alpha source to a destination that has no alpha, the source color components, which have been scaled by alpha, are copied as is.</span></span>

## <a name="decompressing-compressed-texture-surfaces"></a><span data-ttu-id="148d4-145">Decompressione delle superfici di trama compresse</span><span class="sxs-lookup"><span data-stu-id="148d4-145">Decompressing Compressed Texture Surfaces</span></span>

<span data-ttu-id="148d4-146">Come per la compressione di una superficie di trama, la decompressione di una trama compressa viene eseguita tramite i servizi di copia Direct3D.</span><span class="sxs-lookup"><span data-stu-id="148d4-146">As with compressing a texture surface, decompressing a compressed texture is performed through Direct3D copying services.</span></span>

<span data-ttu-id="148d4-147">Per copiare una superficie di trama compressa in una superficie di trama non compressa, usare la funzione [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md).</span><span class="sxs-lookup"><span data-stu-id="148d4-147">To copy a compressed texture surface to a uncompressed texture surface, use the function [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md).</span></span> <span data-ttu-id="148d4-148">Questa funzione gestisce la compressione da e verso le superfici compresse e non compresse.</span><span class="sxs-lookup"><span data-stu-id="148d4-148">This functions handles compression to and from compressed and uncompressed surfaces.</span></span>

## <a name="related-topics"></a><span data-ttu-id="148d4-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="148d4-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="148d4-150">Risorse di trama compresse</span><span class="sxs-lookup"><span data-stu-id="148d4-150">Compressed Texture Resources</span></span>](compressed-texture-resources.md)
</dt> </dl>

 

 
