---
description: Carica un volume da un file in memoria.
ms.assetid: d450b652-3a74-45ea-9506-e05da87821d7
title: Funzione D3DXLoadVolumeFromFileInMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadVolumeFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 97ac67ab66a0072598bfea3b190bdf2c81ceba9a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969338"
---
# <a name="d3dxloadvolumefromfileinmemory-function"></a><span data-ttu-id="a33ae-103">D3DXLoadVolumeFromFileInMemory (funzione)</span><span class="sxs-lookup"><span data-stu-id="a33ae-103">D3DXLoadVolumeFromFileInMemory function</span></span>

<span data-ttu-id="a33ae-104">Carica un volume da un file in memoria.</span><span class="sxs-lookup"><span data-stu-id="a33ae-104">Loads a volume from a file in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="a33ae-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a33ae-105">Syntax</span></span>


```C++
HRESULT D3DXLoadVolumeFromFileInMemory(
  _In_       LPDIRECT3DVOLUME9 pDestVolume,
  _In_ const PALETTEENTRY      *pDestPalette,
  _In_ const D3DBOX            *pDestBox,
  _In_       LPCVOID           pSrcData,
  _In_       UINT              SrcDataSize,
  _In_ const D3DBOX            *pSrcBox,
  _In_       DWORD             Filter,
  _In_       D3DCOLOR          ColorKey,
  _In_       D3DXIMAGE_INFO    *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="a33ae-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a33ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a33ae-107">*pDestVolume* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a33ae-107">*pDestVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a33ae-108">Tipo: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="a33ae-108">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="a33ae-109">Puntatore a un'interfaccia [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) .</span><span class="sxs-lookup"><span data-stu-id="a33ae-109">Pointer to an [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface.</span></span> <span data-ttu-id="a33ae-110">Specifica il volume di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a33ae-110">Specifies the destination volume.</span></span>

</dd> <dt>

<span data-ttu-id="a33ae-111">*pDestPalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a33ae-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a33ae-112">Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="a33ae-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="a33ae-113">Puntatore a una struttura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la tavolozza di destinazione di 256 colori o **null**.</span><span class="sxs-lookup"><span data-stu-id="a33ae-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a33ae-114">*pDestBox* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a33ae-114">*pDestBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a33ae-115">Tipo: **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="a33ae-115">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="a33ae-116">Puntatore a una struttura [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="a33ae-116">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="a33ae-117">Specifica la casella di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a33ae-117">Specifies the destination box.</span></span> <span data-ttu-id="a33ae-118">Impostare questo parametro su **null** per specificare l'intero volume.</span><span class="sxs-lookup"><span data-stu-id="a33ae-118">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="a33ae-119">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a33ae-119">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a33ae-120">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a33ae-120">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a33ae-121">Puntatore al file in memoria da cui caricare il volume.</span><span class="sxs-lookup"><span data-stu-id="a33ae-121">Pointer to the file in memory from which to load the volume.</span></span>

</dd> <dt>

<span data-ttu-id="a33ae-122">*SrcDataSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a33ae-122">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a33ae-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a33ae-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a33ae-124">Dimensioni in byte del file in memoria.</span><span class="sxs-lookup"><span data-stu-id="a33ae-124">Size in bytes of the file in memory.</span></span>

</dd> <dt>

<span data-ttu-id="a33ae-125">*pSrcBox* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a33ae-125">*pSrcBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a33ae-126">Tipo: **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="a33ae-126">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="a33ae-127">Puntatore a una struttura [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="a33ae-127">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="a33ae-128">Specifica la casella di origine.</span><span class="sxs-lookup"><span data-stu-id="a33ae-128">Specifies the source box.</span></span> <span data-ttu-id="a33ae-129">Impostare questo parametro su **null** per specificare l'intero volume.</span><span class="sxs-lookup"><span data-stu-id="a33ae-129">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="a33ae-130">*Filtro* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="a33ae-130">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a33ae-131">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a33ae-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a33ae-132">Combinazione di uno o più [ \_ filtri D3DX](d3dx-filter.md), che controllano il modo in cui l'immagine viene filtrata.</span><span class="sxs-lookup"><span data-stu-id="a33ae-132">Combination of one or more [D3DX\_FILTER](d3dx-filter.md), controlling how the image is filtered.</span></span> <span data-ttu-id="a33ae-133">Specificare \_ il valore predefinito di D3DX per questo parametro equivale a specificare \_ il \_ \| \_ dithering del filtro D3DX del triangolo di filtro D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="a33ae-133">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="a33ae-134">*ColorKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a33ae-134">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a33ae-135">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="a33ae-135">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="a33ae-136">Valore [**D3DCOLOR**](d3dcolor.md) da sostituire con nero trasparente oppure 0 per disabilitare il colorkey.</span><span class="sxs-lookup"><span data-stu-id="a33ae-136">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="a33ae-137">Si tratta sempre di un colore ARGB a 32 bit, indipendente dal formato di immagine di origine.</span><span class="sxs-lookup"><span data-stu-id="a33ae-137">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="a33ae-138">Alfa è significativo e in genere deve essere impostato su FF per le chiavi di colore opache.</span><span class="sxs-lookup"><span data-stu-id="a33ae-138">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="a33ae-139">Pertanto, per il nero opaco, il valore sarà uguale a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="a33ae-139">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="a33ae-140">*pSrcInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a33ae-140">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a33ae-141">Tipo: **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="a33ae-141">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="a33ae-142">Puntatore a una struttura di [**\_ informazioni D3DXIMAGE**](d3dximage-info.md) per la compilazione di una descrizione dei dati nel file di immagine di origine o **null**.</span><span class="sxs-lookup"><span data-stu-id="a33ae-142">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a33ae-143">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a33ae-143">Return value</span></span>

<span data-ttu-id="a33ae-144">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a33ae-144">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a33ae-145">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a33ae-145">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a33ae-146">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="a33ae-146">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="a33ae-147">Commenti</span><span class="sxs-lookup"><span data-stu-id="a33ae-147">Remarks</span></span>

<span data-ttu-id="a33ae-148">Questa funzione gestisce la conversione da e verso formati di trama compressi e supporta i formati di file seguenti: BMP, DDS, DIB, HDR, jpg, PFM, PNG, ppm e TGA.</span><span class="sxs-lookup"><span data-stu-id="a33ae-148">This function handles conversion to and from compressed texture formats and supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="a33ae-149">Vedere [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="a33ae-149">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="a33ae-150">La scrittura in una superficie non di livello zero della trama del volume non comporterà l'aggiornamento del rettangolo modificato.</span><span class="sxs-lookup"><span data-stu-id="a33ae-150">Writing to a non-level-zero surface of the volume texture will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="a33ae-151">Se viene chiamato **D3DXLoadVolumeFromFileInMemory** e la trama non è già sporca (probabilmente in scenari di utilizzo normali), l'applicazione deve chiamare in modo esplicito [**IDirect3DVolumeTexture9:: AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) sulla trama del volume.</span><span class="sxs-lookup"><span data-stu-id="a33ae-151">If **D3DXLoadVolumeFromFileInMemory** is called and the texture was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**IDirect3DVolumeTexture9::AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) on the volume texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="a33ae-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a33ae-152">Requirements</span></span>



| <span data-ttu-id="a33ae-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="a33ae-153">Requirement</span></span> | <span data-ttu-id="a33ae-154">Valore</span><span class="sxs-lookup"><span data-stu-id="a33ae-154">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a33ae-155">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a33ae-155">Header</span></span><br/>  | <dl> <span data-ttu-id="a33ae-156"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="a33ae-156"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="a33ae-157">Libreria</span><span class="sxs-lookup"><span data-stu-id="a33ae-157">Library</span></span><br/> | <dl> <span data-ttu-id="a33ae-158"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a33ae-158"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="a33ae-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a33ae-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a33ae-160">**D3DXLoadVolumeFromFile**</span><span class="sxs-lookup"><span data-stu-id="a33ae-160">**D3DXLoadVolumeFromFile**</span></span>](d3dxloadvolumefromfile.md)
</dt> <dt>

[<span data-ttu-id="a33ae-161">**D3DXLoadVolumeFromMemory**</span><span class="sxs-lookup"><span data-stu-id="a33ae-161">**D3DXLoadVolumeFromMemory**</span></span>](d3dxloadvolumefrommemory.md)
</dt> <dt>

[<span data-ttu-id="a33ae-162">**D3DXLoadVolumeFromResource**</span><span class="sxs-lookup"><span data-stu-id="a33ae-162">**D3DXLoadVolumeFromResource**</span></span>](d3dxloadvolumefromresource.md)
</dt> <dt>

[<span data-ttu-id="a33ae-163">**D3DXLoadVolumeFromVolume**</span><span class="sxs-lookup"><span data-stu-id="a33ae-163">**D3DXLoadVolumeFromVolume**</span></span>](d3dxloadvolumefromvolume.md)
</dt> <dt>

[<span data-ttu-id="a33ae-164">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="a33ae-164">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
