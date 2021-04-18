---
description: Carica un volume da un file.
ms.assetid: ea0fc588-094e-4488-bd82-54507ee0fc91
title: Funzione D3DXLoadVolumeFromFile (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadVolumeFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ff427c58b62d99c2c4716081aab82bd94f146edd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322140"
---
# <a name="d3dxloadvolumefromfile-function"></a><span data-ttu-id="ff105-103">D3DXLoadVolumeFromFile (funzione)</span><span class="sxs-lookup"><span data-stu-id="ff105-103">D3DXLoadVolumeFromFile function</span></span>

<span data-ttu-id="ff105-104">Carica un volume da un file.</span><span class="sxs-lookup"><span data-stu-id="ff105-104">Loads a volume from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff105-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ff105-105">Syntax</span></span>


```C++
HRESULT D3DXLoadVolumeFromFile(
  _In_       LPDIRECT3DVOLUME9 pDestVolume,
  _In_ const PALETTEENTRY      *pDestPalette,
  _In_ const D3DBOX            *pDestBox,
  _In_       LPCTSTR           pSrcFile,
  _In_ const D3DBOX            *pSrcBox,
  _In_       DWORD             Filter,
  _In_       D3DCOLOR          ColorKey,
  _In_       D3DXIMAGE_INFO    *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="ff105-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ff105-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff105-107">*pDestVolume* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ff105-107">*pDestVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff105-108">Tipo: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="ff105-108">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="ff105-109">Puntatore a un'interfaccia [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) .</span><span class="sxs-lookup"><span data-stu-id="ff105-109">Pointer to an [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface.</span></span> <span data-ttu-id="ff105-110">Specifica il volume di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ff105-110">Specifies the destination volume.</span></span>

</dd> <dt>

<span data-ttu-id="ff105-111">*pDestPalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ff105-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff105-112">Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="ff105-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="ff105-113">Puntatore a una struttura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la tavolozza di destinazione di 256 colori o **null**.</span><span class="sxs-lookup"><span data-stu-id="ff105-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ff105-114">*pDestBox* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ff105-114">*pDestBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff105-115">Tipo: **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="ff105-115">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="ff105-116">Puntatore a una struttura [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="ff105-116">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="ff105-117">Specifica la casella di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ff105-117">Specifies the destination box.</span></span> <span data-ttu-id="ff105-118">Impostare questo parametro su **null** per specificare l'intero volume.</span><span class="sxs-lookup"><span data-stu-id="ff105-118">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="ff105-119">*pSrcFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ff105-119">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff105-120">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ff105-120">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ff105-121">Puntatore a una stringa che specifica il nome del file.</span><span class="sxs-lookup"><span data-stu-id="ff105-121">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="ff105-122">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="ff105-122">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="ff105-123">In caso contrario, il tipo di dati String viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="ff105-123">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="ff105-124">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="ff105-124">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ff105-125">*pSrcBox* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ff105-125">*pSrcBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff105-126">Tipo: **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="ff105-126">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="ff105-127">Puntatore a una struttura [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="ff105-127">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="ff105-128">Specifica la casella di origine.</span><span class="sxs-lookup"><span data-stu-id="ff105-128">Specifies the source box.</span></span> <span data-ttu-id="ff105-129">Impostare questo parametro su **null** per specificare l'intero volume.</span><span class="sxs-lookup"><span data-stu-id="ff105-129">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="ff105-130">*Filtro* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="ff105-130">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff105-131">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ff105-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ff105-132">Combinazione di uno o più [ \_ filtri D3DX](d3dx-filter.md), che controllano il modo in cui l'immagine viene filtrata.</span><span class="sxs-lookup"><span data-stu-id="ff105-132">Combination of one or more [D3DX\_FILTER](d3dx-filter.md), controlling how the image is filtered.</span></span> <span data-ttu-id="ff105-133">Specificare \_ il valore predefinito di D3DX per questo parametro equivale a specificare \_ il \_ \| \_ dithering del filtro D3DX del triangolo di filtro D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="ff105-133">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="ff105-134">*ColorKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ff105-134">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff105-135">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="ff105-135">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="ff105-136">Valore [**D3DCOLOR**](d3dcolor.md) da sostituire con nero trasparente oppure 0 per disabilitare il colorkey.</span><span class="sxs-lookup"><span data-stu-id="ff105-136">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="ff105-137">Si tratta sempre di un colore ARGB a 32 bit, indipendente dal formato di immagine di origine.</span><span class="sxs-lookup"><span data-stu-id="ff105-137">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="ff105-138">Alfa è significativo e in genere deve essere impostato su FF per le chiavi di colore opache.</span><span class="sxs-lookup"><span data-stu-id="ff105-138">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="ff105-139">Pertanto, per il nero opaco, il valore sarà uguale a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="ff105-139">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="ff105-140">*pSrcInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ff105-140">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff105-141">Tipo: **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="ff105-141">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="ff105-142">Puntatore a una struttura di [**\_ informazioni D3DXIMAGE**](d3dximage-info.md) per la compilazione di una descrizione dei dati nel file di immagine di origine o **null**.</span><span class="sxs-lookup"><span data-stu-id="ff105-142">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff105-143">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ff105-143">Return value</span></span>

<span data-ttu-id="ff105-144">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ff105-144">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ff105-145">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ff105-145">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ff105-146">Se la funzione ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="ff105-146">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff105-147">Commenti</span><span class="sxs-lookup"><span data-stu-id="ff105-147">Remarks</span></span>

<span data-ttu-id="ff105-148">L'impostazione del compilatore determina anche la versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="ff105-148">The compiler setting also determines the function version.</span></span> <span data-ttu-id="ff105-149">Se è definito Unicode, la chiamata di funzione viene risolta in D3DXLoadVolumeFromFileW.</span><span class="sxs-lookup"><span data-stu-id="ff105-149">If Unicode is defined, the function call resolves to D3DXLoadVolumeFromFileW.</span></span> <span data-ttu-id="ff105-150">In caso contrario, la chiamata di funzione viene risolta in D3DXLoadVolumeFromFileA perché vengono utilizzate le stringhe ANSI.</span><span class="sxs-lookup"><span data-stu-id="ff105-150">Otherwise, the function call resolves to D3DXLoadVolumeFromFileA because ANSI strings are being used.</span></span>

<span data-ttu-id="ff105-151">Questa funzione gestisce la conversione da e verso formati di trama compressi e supporta i formati di file seguenti: BMP, DDS, DIB, HDR, jpg, PFM, PNG, ppm e TGA.</span><span class="sxs-lookup"><span data-stu-id="ff105-151">This function handles conversion to and from compressed texture formats and supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="ff105-152">Vedere [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="ff105-152">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="ff105-153">La scrittura in una superficie non di livello zero della trama del volume non comporterà l'aggiornamento del rettangolo modificato.</span><span class="sxs-lookup"><span data-stu-id="ff105-153">Writing to a non-level-zero surface of the volume texture will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="ff105-154">Se viene chiamato **D3DXLoadVolumeFromFile** e la trama non è già sporca (probabilmente in scenari di utilizzo normali), l'applicazione deve chiamare in modo esplicito [**IDirect3DVolumeTexture9:: AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) sulla trama del volume.</span><span class="sxs-lookup"><span data-stu-id="ff105-154">If **D3DXLoadVolumeFromFile** is called and the texture was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**IDirect3DVolumeTexture9::AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) on the volume texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff105-155">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ff105-155">Requirements</span></span>



| <span data-ttu-id="ff105-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff105-156">Requirement</span></span> | <span data-ttu-id="ff105-157">Valore</span><span class="sxs-lookup"><span data-stu-id="ff105-157">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ff105-158">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ff105-158">Header</span></span><br/>  | <dl> <span data-ttu-id="ff105-159"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff105-159"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="ff105-160">Libreria</span><span class="sxs-lookup"><span data-stu-id="ff105-160">Library</span></span><br/> | <dl> <span data-ttu-id="ff105-161"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ff105-161"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ff105-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ff105-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff105-163">**D3DXLoadVolumeFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="ff105-163">**D3DXLoadVolumeFromFileInMemory**</span></span>](d3dxloadvolumefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="ff105-164">**D3DXLoadVolumeFromMemory**</span><span class="sxs-lookup"><span data-stu-id="ff105-164">**D3DXLoadVolumeFromMemory**</span></span>](d3dxloadvolumefrommemory.md)
</dt> <dt>

[<span data-ttu-id="ff105-165">**D3DXLoadVolumeFromResource**</span><span class="sxs-lookup"><span data-stu-id="ff105-165">**D3DXLoadVolumeFromResource**</span></span>](d3dxloadvolumefromresource.md)
</dt> <dt>

[<span data-ttu-id="ff105-166">**D3DXLoadVolumeFromVolume**</span><span class="sxs-lookup"><span data-stu-id="ff105-166">**D3DXLoadVolumeFromVolume**</span></span>](d3dxloadvolumefromvolume.md)
</dt> <dt>

[<span data-ttu-id="ff105-167">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="ff105-167">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
