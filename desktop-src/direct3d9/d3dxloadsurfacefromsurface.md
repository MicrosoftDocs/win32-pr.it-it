---
description: Carica una superficie da un'altra superficie con la conversione dei colori.
ms.assetid: eddb420d-fd32-4c09-afec-435887c4e905
title: Funzione D3DXLoadSurfaceFromSurface (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSurfaceFromSurface
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7b5138ddf540c3e4a87fe65f29938cb3557b2360
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762185"
---
# <a name="d3dxloadsurfacefromsurface-function"></a><span data-ttu-id="e6536-103">D3DXLoadSurfaceFromSurface (funzione)</span><span class="sxs-lookup"><span data-stu-id="e6536-103">D3DXLoadSurfaceFromSurface function</span></span>

<span data-ttu-id="e6536-104">Carica una superficie da un'altra superficie con la conversione dei colori.</span><span class="sxs-lookup"><span data-stu-id="e6536-104">Loads a surface from another surface with color conversion.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6536-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e6536-105">Syntax</span></span>


```C++
HRESULT D3DXLoadSurfaceFromSurface(
  _In_       LPDIRECT3DSURFACE9 pDestSurface,
  _In_ const PALETTEENTRY       *pDestPalette,
  _In_ const RECT               *pDestRect,
  _In_       LPDIRECT3DSURFACE9 pSrcSurface,
  _In_ const PALETTEENTRY       *pSrcPalette,
  _In_ const RECT               *pSrcRect,
  _In_       DWORD              Filter,
  _In_       D3DCOLOR           ColorKey
);
```



## <a name="parameters"></a><span data-ttu-id="e6536-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e6536-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6536-107">*pDestSurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e6536-107">*pDestSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6536-108">Tipo: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="e6536-108">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="e6536-109">Puntatore a un'interfaccia [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) .</span><span class="sxs-lookup"><span data-stu-id="e6536-109">Pointer to an [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface.</span></span> <span data-ttu-id="e6536-110">Specifica la superficie di destinazione che riceve l'immagine.</span><span class="sxs-lookup"><span data-stu-id="e6536-110">Specifies the destination surface, which receives the image.</span></span>

</dd> <dt>

<span data-ttu-id="e6536-111">*pDestPalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e6536-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6536-112">Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="e6536-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="e6536-113">Puntatore a una struttura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la tavolozza di destinazione di 256 colori o **null**.</span><span class="sxs-lookup"><span data-stu-id="e6536-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e6536-114">*pDestRect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e6536-114">*pDestRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6536-115">Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="e6536-115">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="e6536-116">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e6536-116">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="e6536-117">Specifica il rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e6536-117">Specifies the destination rectangle.</span></span> <span data-ttu-id="e6536-118">Impostare questo parametro su **null** per specificare l'intera superficie.</span><span class="sxs-lookup"><span data-stu-id="e6536-118">Set this parameter to **NULL** to specify the entire surface.</span></span>

</dd> <dt>

<span data-ttu-id="e6536-119">*pSrcSurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e6536-119">*pSrcSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6536-120">Tipo: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="e6536-120">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="e6536-121">Puntatore a un'interfaccia [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) , che rappresenta l'area di origine.</span><span class="sxs-lookup"><span data-stu-id="e6536-121">Pointer to an [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface, representing the source surface.</span></span>

</dd> <dt>

<span data-ttu-id="e6536-122">*pSrcPalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e6536-122">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6536-123">Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="e6536-123">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="e6536-124">Puntatore a una struttura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la tavolozza di origine di 256 colori o **null**.</span><span class="sxs-lookup"><span data-stu-id="e6536-124">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the source palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e6536-125">*pSrcRect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e6536-125">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6536-126">Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="e6536-126">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="e6536-127">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e6536-127">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="e6536-128">Specifica il rettangolo di origine.</span><span class="sxs-lookup"><span data-stu-id="e6536-128">Specifies the source rectangle.</span></span> <span data-ttu-id="e6536-129">Impostare questo parametro su **null** per specificare l'intera superficie.</span><span class="sxs-lookup"><span data-stu-id="e6536-129">Set this parameter to **NULL** to specify the entire surface.</span></span>

</dd> <dt>

<span data-ttu-id="e6536-130">*Filtro* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="e6536-130">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6536-131">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e6536-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e6536-132">Combinazione di uno o più [ \_ filtri D3DX](d3dx-filter.md), che controllano il modo in cui l'immagine viene filtrata.</span><span class="sxs-lookup"><span data-stu-id="e6536-132">A combination of one or more [D3DX\_FILTER](d3dx-filter.md), controlling how the image is filtered.</span></span> <span data-ttu-id="e6536-133">Specificare \_ il valore predefinito di D3DX per questo parametro equivale a specificare \_ il \_ \| \_ dithering del filtro D3DX del triangolo di filtro D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="e6536-133">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="e6536-134">*ColorKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e6536-134">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6536-135">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="e6536-135">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="e6536-136">Valore [**D3DCOLOR**](d3dcolor.md) da sostituire con nero trasparente oppure 0 per disabilitare il colorkey.</span><span class="sxs-lookup"><span data-stu-id="e6536-136">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="e6536-137">Si tratta sempre di un colore ARGB a 32 bit, indipendente dal formato di immagine di origine.</span><span class="sxs-lookup"><span data-stu-id="e6536-137">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="e6536-138">Alfa è significativo e in genere deve essere impostato su FF per le chiavi di colore opache.</span><span class="sxs-lookup"><span data-stu-id="e6536-138">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="e6536-139">Pertanto, per il nero opaco, il valore sarà uguale a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="e6536-139">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6536-140">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e6536-140">Return value</span></span>

<span data-ttu-id="e6536-141">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e6536-141">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e6536-142">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e6536-142">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e6536-143">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="e6536-143">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6536-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="e6536-144">Remarks</span></span>

<span data-ttu-id="e6536-145">Questa funzione gestisce la conversione da e verso formati di trama compressi.</span><span class="sxs-lookup"><span data-stu-id="e6536-145">This function handles conversion to and from compressed texture formats.</span></span>

<span data-ttu-id="e6536-146">La scrittura in una superficie non di livello zero non comporterà l'aggiornamento del rettangolo modificato.</span><span class="sxs-lookup"><span data-stu-id="e6536-146">Writing to a non-level-zero surface will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="e6536-147">Se viene chiamato **D3DXLoadSurfaceFromSurface** e la superficie non è già sporca (si tratta di un problema improbabile in scenari di utilizzo normali), l'applicazione deve chiamare in modo esplicito [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) sulla superficie.</span><span class="sxs-lookup"><span data-stu-id="e6536-147">If **D3DXLoadSurfaceFromSurface** is called and the surface was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) on the surface.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6536-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e6536-148">Requirements</span></span>



| <span data-ttu-id="e6536-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6536-149">Requirement</span></span> | <span data-ttu-id="e6536-150">Valore</span><span class="sxs-lookup"><span data-stu-id="e6536-150">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e6536-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e6536-151">Header</span></span><br/>  | <dl> <span data-ttu-id="e6536-152"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6536-152"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="e6536-153">Libreria</span><span class="sxs-lookup"><span data-stu-id="e6536-153">Library</span></span><br/> | <dl> <span data-ttu-id="e6536-154"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e6536-154"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="e6536-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e6536-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6536-156">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="e6536-156">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
