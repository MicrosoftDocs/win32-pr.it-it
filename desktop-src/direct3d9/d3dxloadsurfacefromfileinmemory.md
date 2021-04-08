---
description: Carica una superficie da un file in memoria.
ms.assetid: 436a6151-2819-44eb-bd56-1b3777f709e5
title: Funzione D3DXLoadSurfaceFromFileInMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSurfaceFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a447c4c5b65e3085d84e26ef202283cf0c31c6b5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762334"
---
# <a name="d3dxloadsurfacefromfileinmemory-function"></a><span data-ttu-id="940d5-103">D3DXLoadSurfaceFromFileInMemory (funzione)</span><span class="sxs-lookup"><span data-stu-id="940d5-103">D3DXLoadSurfaceFromFileInMemory function</span></span>

<span data-ttu-id="940d5-104">Carica una superficie da un file in memoria.</span><span class="sxs-lookup"><span data-stu-id="940d5-104">Loads a surface from a file in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="940d5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="940d5-105">Syntax</span></span>


```C++
HRESULT D3DXLoadSurfaceFromFileInMemory(
  _In_          LPDIRECT3DSURFACE9 pDestSurface,
  _In_    const PALETTEENTRY       *pDestPalette,
  _In_    const RECT               *pDestRect,
  _In_          LPCVOID            pSrcData,
  _In_          UINT               SrcData,
  _In_    const RECT               *pSrcRect,
  _In_          DWORD              Filter,
  _In_          D3DCOLOR           ColorKey,
  _Inout_       D3DXIMAGE_INFO     *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="940d5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="940d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="940d5-107">*pDestSurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="940d5-107">*pDestSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="940d5-108">Tipo: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="940d5-108">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="940d5-109">Puntatore a un'interfaccia [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) .</span><span class="sxs-lookup"><span data-stu-id="940d5-109">Pointer to an [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface.</span></span> <span data-ttu-id="940d5-110">Specifica la superficie di destinazione che riceve l'immagine.</span><span class="sxs-lookup"><span data-stu-id="940d5-110">Specifies the destination surface, which receives the image.</span></span>

</dd> <dt>

<span data-ttu-id="940d5-111">*pDestPalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="940d5-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="940d5-112">Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="940d5-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="940d5-113">Puntatore a una struttura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la tavolozza di destinazione di 256 colori o **null**.</span><span class="sxs-lookup"><span data-stu-id="940d5-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="940d5-114">*pDestRect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="940d5-114">*pDestRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="940d5-115">Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="940d5-115">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="940d5-116">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="940d5-116">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="940d5-117">Specifica il rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="940d5-117">Specifies the destination rectangle.</span></span> <span data-ttu-id="940d5-118">Impostare questo parametro su **null** per specificare l'intera superficie.</span><span class="sxs-lookup"><span data-stu-id="940d5-118">Set this parameter to **NULL** to specify the entire surface.</span></span>

</dd> <dt>

<span data-ttu-id="940d5-119">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="940d5-119">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="940d5-120">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="940d5-120">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="940d5-121">Puntatore al file in memoria da cui caricare la superficie.</span><span class="sxs-lookup"><span data-stu-id="940d5-121">Pointer to the file in memory from which to load the surface.</span></span>

</dd> <dt>

<span data-ttu-id="940d5-122">*SrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="940d5-122">*SrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="940d5-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="940d5-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="940d5-124">Dimensioni in byte del file in memoria.</span><span class="sxs-lookup"><span data-stu-id="940d5-124">Size of the file in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="940d5-125">*pSrcRect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="940d5-125">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="940d5-126">Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="940d5-126">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="940d5-127">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="940d5-127">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="940d5-128">Specifica il rettangolo di origine.</span><span class="sxs-lookup"><span data-stu-id="940d5-128">Specifies the source rectangle.</span></span> <span data-ttu-id="940d5-129">Impostare questo parametro su **null** per specificare l'intera immagine.</span><span class="sxs-lookup"><span data-stu-id="940d5-129">Set this parameter to **NULL** to specify the entire image.</span></span>

</dd> <dt>

<span data-ttu-id="940d5-130">*Filtro* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="940d5-130">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="940d5-131">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="940d5-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="940d5-132">Combinazione di uno o più [ \_ filtri D3DX](d3dx-filter.md) che controllano il modo in cui l'immagine viene filtrata.</span><span class="sxs-lookup"><span data-stu-id="940d5-132">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="940d5-133">Specificare \_ il valore predefinito di D3DX per questo parametro equivale a specificare \_ il \_ \| \_ dithering del filtro D3DX del triangolo di filtro D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="940d5-133">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="940d5-134">*ColorKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="940d5-134">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="940d5-135">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="940d5-135">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="940d5-136">Valore [**D3DCOLOR**](d3dcolor.md) da sostituire con nero trasparente oppure 0 per disabilitare il colorkey.</span><span class="sxs-lookup"><span data-stu-id="940d5-136">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="940d5-137">Si tratta sempre di un colore ARGB a 32 bit, indipendente dal formato di immagine di origine.</span><span class="sxs-lookup"><span data-stu-id="940d5-137">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="940d5-138">Alfa è significativo e in genere deve essere impostato su FF per le chiavi di colore opache.</span><span class="sxs-lookup"><span data-stu-id="940d5-138">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="940d5-139">Pertanto, per il nero opaco, il valore sarà uguale a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="940d5-139">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="940d5-140">*pSrcInfo* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="940d5-140">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="940d5-141">Tipo: **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="940d5-141">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="940d5-142">Puntatore a una struttura di [**\_ informazioni D3DXIMAGE**](d3dximage-info.md) per la compilazione di una descrizione dei dati nel file di immagine di origine o **null**.</span><span class="sxs-lookup"><span data-stu-id="940d5-142">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="940d5-143">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="940d5-143">Return value</span></span>

<span data-ttu-id="940d5-144">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="940d5-144">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="940d5-145">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="940d5-145">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="940d5-146">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="940d5-146">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="940d5-147">Commenti</span><span class="sxs-lookup"><span data-stu-id="940d5-147">Remarks</span></span>

<span data-ttu-id="940d5-148">Questa funzione gestisce la conversione da e verso formati di trama compressi e supporta i formati di file seguenti: BMP, DDS, DIB, HDR, jpg, PFM, PNG, ppm e TGA.</span><span class="sxs-lookup"><span data-stu-id="940d5-148">This function handles conversion to and from compressed texture formats and supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="940d5-149">Vedere [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="940d5-149">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="940d5-150">La scrittura in una superficie non di livello zero non comporterà l'aggiornamento del rettangolo modificato.</span><span class="sxs-lookup"><span data-stu-id="940d5-150">Writing to a non-level-zero surface will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="940d5-151">Se viene chiamato **D3DXLoadSurfaceFromFileInMemory** e la superficie non è già sporca (si tratta di un problema improbabile in scenari di utilizzo normali), l'applicazione deve chiamare in modo esplicito [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) sulla superficie.</span><span class="sxs-lookup"><span data-stu-id="940d5-151">If **D3DXLoadSurfaceFromFileInMemory** is called and the surface was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) on the surface.</span></span>

## <a name="requirements"></a><span data-ttu-id="940d5-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="940d5-152">Requirements</span></span>



| <span data-ttu-id="940d5-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="940d5-153">Requirement</span></span> | <span data-ttu-id="940d5-154">Valore</span><span class="sxs-lookup"><span data-stu-id="940d5-154">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="940d5-155">Intestazione</span><span class="sxs-lookup"><span data-stu-id="940d5-155">Header</span></span><br/>  | <dl> <span data-ttu-id="940d5-156"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="940d5-156"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="940d5-157">Libreria</span><span class="sxs-lookup"><span data-stu-id="940d5-157">Library</span></span><br/> | <dl> <span data-ttu-id="940d5-158"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="940d5-158"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="940d5-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="940d5-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="940d5-160">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="940d5-160">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
