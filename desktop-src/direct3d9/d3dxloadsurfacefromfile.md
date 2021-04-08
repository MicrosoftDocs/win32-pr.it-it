---
description: Carica una superficie da un file.
ms.assetid: cbd360b6-6cee-418b-8c45-506e190eb2f6
title: Funzione D3DXLoadSurfaceFromFile (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSurfaceFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f53343e436ac78b93bcee30c7da5c9d8eb2dc415
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762335"
---
# <a name="d3dxloadsurfacefromfile-function"></a><span data-ttu-id="70cf4-103">D3DXLoadSurfaceFromFile (funzione)</span><span class="sxs-lookup"><span data-stu-id="70cf4-103">D3DXLoadSurfaceFromFile function</span></span>

<span data-ttu-id="70cf4-104">Carica una superficie da un file.</span><span class="sxs-lookup"><span data-stu-id="70cf4-104">Loads a surface from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="70cf4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="70cf4-105">Syntax</span></span>


```C++
HRESULT D3DXLoadSurfaceFromFile(
  _In_          LPDIRECT3DSURFACE9 pDestSurface,
  _In_    const PALETTEENTRY       *pDestPalette,
  _In_    const RECT               *pDestRect,
  _In_          LPCTSTR            pSrcFile,
  _In_    const RECT               *pSrcRect,
  _In_          DWORD              Filter,
  _In_          D3DCOLOR           ColorKey,
  _Inout_       D3DXIMAGE_INFO     *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="70cf4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="70cf4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70cf4-107">*pDestSurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="70cf4-107">*pDestSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70cf4-108">Tipo: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="70cf4-108">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="70cf4-109">Puntatore a un'interfaccia [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) .</span><span class="sxs-lookup"><span data-stu-id="70cf4-109">Pointer to an [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface.</span></span> <span data-ttu-id="70cf4-110">Specifica la superficie di destinazione che riceve l'immagine.</span><span class="sxs-lookup"><span data-stu-id="70cf4-110">Specifies the destination surface, which receives the image.</span></span>

</dd> <dt>

<span data-ttu-id="70cf4-111">*pDestPalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="70cf4-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70cf4-112">Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="70cf4-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="70cf4-113">Puntatore a una struttura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la tavolozza di destinazione di 256 colori o **null**.</span><span class="sxs-lookup"><span data-stu-id="70cf4-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="70cf4-114">*pDestRect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="70cf4-114">*pDestRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70cf4-115">Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="70cf4-115">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="70cf4-116">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="70cf4-116">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="70cf4-117">Specifica il rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="70cf4-117">Specifies the destination rectangle.</span></span> <span data-ttu-id="70cf4-118">Impostare questo parametro su **null** per specificare l'intera superficie.</span><span class="sxs-lookup"><span data-stu-id="70cf4-118">Set this parameter to **NULL** to specify the entire surface.</span></span>

</dd> <dt>

<span data-ttu-id="70cf4-119">*pSrcFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="70cf4-119">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70cf4-120">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="70cf4-120">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="70cf4-121">Puntatore a una stringa che specifica il nome del file.</span><span class="sxs-lookup"><span data-stu-id="70cf4-121">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="70cf4-122">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="70cf4-122">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="70cf4-123">In caso contrario, il tipo di dati String viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="70cf4-123">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="70cf4-124">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="70cf4-124">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="70cf4-125">*pSrcRect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="70cf4-125">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70cf4-126">Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="70cf4-126">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="70cf4-127">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="70cf4-127">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="70cf4-128">Specifica il rettangolo di origine.</span><span class="sxs-lookup"><span data-stu-id="70cf4-128">Specifies the source rectangle.</span></span> <span data-ttu-id="70cf4-129">Impostare questo parametro su **null** per specificare l'intera immagine.</span><span class="sxs-lookup"><span data-stu-id="70cf4-129">Set this parameter to **NULL** to specify the entire image.</span></span>

</dd> <dt>

<span data-ttu-id="70cf4-130">*Filtro* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="70cf4-130">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70cf4-131">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="70cf4-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="70cf4-132">Combinazione di uno o più [ \_ filtri D3DX](d3dx-filter.md) che controllano il modo in cui l'immagine viene filtrata.</span><span class="sxs-lookup"><span data-stu-id="70cf4-132">Combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="70cf4-133">Specificare \_ il valore predefinito di D3DX per questo parametro equivale a specificare \_ il \_ \| \_ dithering del filtro D3DX del triangolo di filtro D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="70cf4-133">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="70cf4-134">*ColorKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="70cf4-134">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70cf4-135">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="70cf4-135">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="70cf4-136">Valore [**D3DCOLOR**](d3dcolor.md) da sostituire con nero trasparente oppure 0 per disabilitare il colorkey.</span><span class="sxs-lookup"><span data-stu-id="70cf4-136">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="70cf4-137">Si tratta sempre di un colore ARGB a 32 bit, indipendente dal formato di immagine di origine.</span><span class="sxs-lookup"><span data-stu-id="70cf4-137">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="70cf4-138">Alfa è significativo e in genere deve essere impostato su FF per le chiavi di colore opache, quindi, per il nero opaco, il valore è uguale a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="70cf4-138">Alpha is significant and should usually be set to FF for opaque color keys Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="70cf4-139">*pSrcInfo* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="70cf4-139">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="70cf4-140">Tipo: **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="70cf4-140">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="70cf4-141">Puntatore a una struttura di [**\_ informazioni D3DXIMAGE**](d3dximage-info.md) per la compilazione di una descrizione dei dati nel file di immagine di origine o **null**.</span><span class="sxs-lookup"><span data-stu-id="70cf4-141">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70cf4-142">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="70cf4-142">Return value</span></span>

<span data-ttu-id="70cf4-143">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="70cf4-143">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="70cf4-144">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="70cf4-144">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="70cf4-145">Se la funzione ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="70cf4-145">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="70cf4-146">Commenti</span><span class="sxs-lookup"><span data-stu-id="70cf4-146">Remarks</span></span>

<span data-ttu-id="70cf4-147">L'impostazione del compilatore determina anche la versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="70cf4-147">The compiler setting also determines the function version.</span></span> <span data-ttu-id="70cf4-148">Se è definito Unicode, la chiamata di funzione viene risolta in D3DXLoadSurfaceFromFileW.</span><span class="sxs-lookup"><span data-stu-id="70cf4-148">If Unicode is defined, the function call resolves to D3DXLoadSurfaceFromFileW.</span></span> <span data-ttu-id="70cf4-149">In caso contrario, la chiamata di funzione viene risolta in D3DXLoadSurfaceFromFileA perché vengono utilizzate le stringhe ANSI.</span><span class="sxs-lookup"><span data-stu-id="70cf4-149">Otherwise, the function call resolves to D3DXLoadSurfaceFromFileA because ANSI strings are being used.</span></span>

<span data-ttu-id="70cf4-150">Questa funzione gestisce la conversione da e verso formati di trama compressi e supporta i formati di file seguenti: BMP, DDS, DIB, HDR, jpg, PFM, PNG, ppm e TGA.</span><span class="sxs-lookup"><span data-stu-id="70cf4-150">This function handles conversion to and from compressed texture formats and supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="70cf4-151">Vedere [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="70cf4-151">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="70cf4-152">La scrittura in una superficie non di livello zero non comporterà l'aggiornamento del rettangolo modificato.</span><span class="sxs-lookup"><span data-stu-id="70cf4-152">Writing to a non-level-zero surface will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="70cf4-153">Se viene chiamato **D3DXLoadSurfaceFromFile** e la superficie non è già sporca (si tratta di un problema improbabile in scenari di utilizzo normali), l'applicazione deve chiamare in modo esplicito [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) sulla superficie.</span><span class="sxs-lookup"><span data-stu-id="70cf4-153">If **D3DXLoadSurfaceFromFile** is called and the surface was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) on the surface.</span></span>

## <a name="requirements"></a><span data-ttu-id="70cf4-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="70cf4-154">Requirements</span></span>



| <span data-ttu-id="70cf4-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="70cf4-155">Requirement</span></span> | <span data-ttu-id="70cf4-156">Valore</span><span class="sxs-lookup"><span data-stu-id="70cf4-156">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="70cf4-157">Intestazione</span><span class="sxs-lookup"><span data-stu-id="70cf4-157">Header</span></span><br/>  | <dl> <span data-ttu-id="70cf4-158"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="70cf4-158"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="70cf4-159">Libreria</span><span class="sxs-lookup"><span data-stu-id="70cf4-159">Library</span></span><br/> | <dl> <span data-ttu-id="70cf4-160"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="70cf4-160"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="70cf4-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="70cf4-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70cf4-162">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="70cf4-162">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
