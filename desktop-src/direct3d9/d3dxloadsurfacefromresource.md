---
description: Carica una superficie da una risorsa.
ms.assetid: 16d49f61-8c84-4e15-aacc-1d26099e65e0
title: Funzione D3DXLoadSurfaceFromResource (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSurfaceFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ae802a1b7e18ce5f2b0a11c6679628ea1deb25aa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969304"
---
# <a name="d3dxloadsurfacefromresource-function"></a><span data-ttu-id="4206e-103">D3DXLoadSurfaceFromResource (funzione)</span><span class="sxs-lookup"><span data-stu-id="4206e-103">D3DXLoadSurfaceFromResource function</span></span>

<span data-ttu-id="4206e-104">Carica una superficie da una risorsa.</span><span class="sxs-lookup"><span data-stu-id="4206e-104">Loads a surface from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="4206e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4206e-105">Syntax</span></span>


```C++
HRESULT D3DXLoadSurfaceFromResource(
  _In_          LPDIRECT3DSURFACE9 pDestSurface,
  _In_    const PALETTEENTRY       *pDestPalette,
  _In_    const RECT               *pDestRect,
  _In_          HMODULE            hSrcModule,
  _In_          LPCTSTR            pSrcResource,
  _In_    const RECT               *pSrcRect,
  _In_          DWORD              Filter,
  _In_          D3DCOLOR           ColorKey,
  _Inout_       D3DXIMAGE_INFO     *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="4206e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4206e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4206e-107">*pDestSurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4206e-107">*pDestSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4206e-108">Tipo: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="4206e-108">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="4206e-109">Puntatore a un'interfaccia [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) .</span><span class="sxs-lookup"><span data-stu-id="4206e-109">Pointer to an [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface.</span></span> <span data-ttu-id="4206e-110">Specifica la superficie di destinazione che riceve l'immagine.</span><span class="sxs-lookup"><span data-stu-id="4206e-110">Specifies the destination surface, which receives the image.</span></span>

</dd> <dt>

<span data-ttu-id="4206e-111">*pDestPalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4206e-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4206e-112">Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="4206e-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="4206e-113">Puntatore a una struttura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la tavolozza di destinazione di 256 colori o **null**.</span><span class="sxs-lookup"><span data-stu-id="4206e-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4206e-114">*pDestRect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4206e-114">*pDestRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4206e-115">Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="4206e-115">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="4206e-116">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="4206e-116">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="4206e-117">Specifica il rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4206e-117">Specifies the destination rectangle.</span></span> <span data-ttu-id="4206e-118">Impostare questo parametro su **null** per specificare l'intera superficie.</span><span class="sxs-lookup"><span data-stu-id="4206e-118">Set this parameter to **NULL** to specify the entire surface.</span></span>

</dd> <dt>

<span data-ttu-id="4206e-119">*hSrcModule* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4206e-119">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4206e-120">Tipo: **[ **hmodule**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4206e-120">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4206e-121">Handle per il modulo in cui si trova la risorsa o **null** per il modulo associato all'immagine utilizzata dal sistema operativo per creare il processo corrente.</span><span class="sxs-lookup"><span data-stu-id="4206e-121">Handle to the module where the resource is located, or **NULL** for module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="4206e-122">*pSrcResource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4206e-122">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4206e-123">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4206e-123">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4206e-124">Puntatore a una stringa che specifica il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="4206e-124">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="4206e-125">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="4206e-125">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="4206e-126">In caso contrario, il tipo di dati String viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="4206e-126">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="4206e-127">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="4206e-127">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="4206e-128">*pSrcRect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4206e-128">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4206e-129">Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="4206e-129">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="4206e-130">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="4206e-130">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="4206e-131">Specifica il rettangolo di origine.</span><span class="sxs-lookup"><span data-stu-id="4206e-131">Specifies the source rectangle.</span></span> <span data-ttu-id="4206e-132">Impostare questo parametro su **null** per specificare l'intera immagine.</span><span class="sxs-lookup"><span data-stu-id="4206e-132">Set this parameter to **NULL** to specify the entire image.</span></span>

</dd> <dt>

<span data-ttu-id="4206e-133">*Filtro* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="4206e-133">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4206e-134">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4206e-134">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4206e-135">Combinazione di uno o più [ \_ filtri D3DX](d3dx-filter.md) che controllano il modo in cui l'immagine viene filtrata.</span><span class="sxs-lookup"><span data-stu-id="4206e-135">Combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="4206e-136">Specificare \_ il valore predefinito di D3DX per questo parametro equivale a specificare \_ il \_ \| \_ dithering del filtro D3DX del triangolo di filtro D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="4206e-136">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="4206e-137">*ColorKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4206e-137">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4206e-138">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="4206e-138">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="4206e-139">Valore [**D3DCOLOR**](d3dcolor.md) da sostituire con nero trasparente oppure 0 per disabilitare il colorkey.</span><span class="sxs-lookup"><span data-stu-id="4206e-139">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="4206e-140">Si tratta sempre di un colore ARGB a 32 bit, indipendente dal formato di immagine di origine.</span><span class="sxs-lookup"><span data-stu-id="4206e-140">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="4206e-141">Alfa è significativo e in genere deve essere impostato su FF per le chiavi di colore opache, quindi, per il nero opaco, il valore è uguale a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="4206e-141">Alpha is significant and should usually be set to FF for opaque color keys Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="4206e-142">*pSrcInfo* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="4206e-142">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4206e-143">Tipo: **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="4206e-143">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="4206e-144">Puntatore a una struttura di [**\_ informazioni D3DXIMAGE**](d3dximage-info.md) per la compilazione di una descrizione dei dati nel file di immagine di origine o **null**.</span><span class="sxs-lookup"><span data-stu-id="4206e-144">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4206e-145">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4206e-145">Return value</span></span>

<span data-ttu-id="4206e-146">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4206e-146">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4206e-147">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4206e-147">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4206e-148">Se la funzione ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="4206e-148">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="4206e-149">Commenti</span><span class="sxs-lookup"><span data-stu-id="4206e-149">Remarks</span></span>

<span data-ttu-id="4206e-150">L'impostazione del compilatore determina anche la versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="4206e-150">The compiler setting also determines the function version.</span></span> <span data-ttu-id="4206e-151">Se è definito Unicode, la chiamata di funzione viene risolta in D3DXLoadSurfaceFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="4206e-151">If Unicode is defined, the function call resolves to D3DXLoadSurfaceFromResourceW.</span></span> <span data-ttu-id="4206e-152">In caso contrario, la chiamata di funzione viene risolta in D3DXLoadSurfaceFromResourceA perché vengono utilizzate le stringhe ANSI.</span><span class="sxs-lookup"><span data-stu-id="4206e-152">Otherwise, the function call resolves to D3DXLoadSurfaceFromResourceA because ANSI strings are being used.</span></span>

<span data-ttu-id="4206e-153">La risorsa da caricare deve essere di tipo RT \_ bitmap o RT \_ RCDATA.</span><span class="sxs-lookup"><span data-stu-id="4206e-153">The resource being loaded must be of type RT\_BITMAP or RT\_RCDATA.</span></span> <span data-ttu-id="4206e-154">Il tipo di risorsa RT \_ RCDATA viene usato per caricare formati diversi da bitmap, ad esempio. tga,. jpg e. DDS.</span><span class="sxs-lookup"><span data-stu-id="4206e-154">Resource type RT\_RCDATA is used to load formats other than bitmaps (such as .tga, .jpg, and .dds).</span></span>

<span data-ttu-id="4206e-155">Questa funzione gestisce la conversione da e verso formati di trama compressi.</span><span class="sxs-lookup"><span data-stu-id="4206e-155">This function handles conversion to and from compressed texture formats.</span></span>

<span data-ttu-id="4206e-156">La scrittura in una superficie non di livello zero non comporterà l'aggiornamento del rettangolo modificato.</span><span class="sxs-lookup"><span data-stu-id="4206e-156">Writing to a non-level-zero surface will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="4206e-157">Se viene chiamato [**D3DXLoadSurfaceFromFile**](d3dxloadsurfacefromfile.md) e la superficie non è già sporca (si tratta di un problema improbabile in scenari di utilizzo normali), l'applicazione deve chiamare in modo esplicito [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) sulla superficie.</span><span class="sxs-lookup"><span data-stu-id="4206e-157">If [**D3DXLoadSurfaceFromFile**](d3dxloadsurfacefromfile.md) is called and the surface was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) on the surface.</span></span>

## <a name="requirements"></a><span data-ttu-id="4206e-158">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4206e-158">Requirements</span></span>



| <span data-ttu-id="4206e-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="4206e-159">Requirement</span></span> | <span data-ttu-id="4206e-160">Valore</span><span class="sxs-lookup"><span data-stu-id="4206e-160">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4206e-161">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4206e-161">Header</span></span><br/>  | <dl> <span data-ttu-id="4206e-162"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="4206e-162"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="4206e-163">Libreria</span><span class="sxs-lookup"><span data-stu-id="4206e-163">Library</span></span><br/> | <dl> <span data-ttu-id="4206e-164"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4206e-164"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="4206e-165">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4206e-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4206e-166">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="4206e-166">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
