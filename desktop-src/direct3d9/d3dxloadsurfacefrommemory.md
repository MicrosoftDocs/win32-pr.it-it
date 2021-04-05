---
description: Carica una superficie dalla memoria.
ms.assetid: 9a36e395-fd00-47fe-8df1-cda8c80182ef
title: Funzione D3DXLoadSurfaceFromMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSurfaceFromMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ffb7be05301ae807505242153be902ab30eecf14
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058588"
---
# <a name="d3dxloadsurfacefrommemory-function"></a><span data-ttu-id="e3173-103">D3DXLoadSurfaceFromMemory (funzione)</span><span class="sxs-lookup"><span data-stu-id="e3173-103">D3DXLoadSurfaceFromMemory function</span></span>

<span data-ttu-id="e3173-104">Carica una superficie dalla memoria.</span><span class="sxs-lookup"><span data-stu-id="e3173-104">Loads a surface from memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3173-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e3173-105">Syntax</span></span>


```C++
HRESULT D3DXLoadSurfaceFromMemory(
  _In_       LPDIRECT3DSURFACE9 pDestSurface,
  _In_ const PALETTEENTRY       *pDestPalette,
  _In_ const RECT               *pDestRect,
  _In_       LPCVOID            pSrcMemory,
  _In_       D3DFORMAT          SrcFormat,
  _In_       UINT               SrcPitch,
  _In_ const PALETTEENTRY       *pSrcPalette,
  _In_ const RECT               *pSrcRect,
  _In_       DWORD              Filter,
  _In_       D3DCOLOR           ColorKey
);
```



## <a name="parameters"></a><span data-ttu-id="e3173-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e3173-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3173-107">*pDestSurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3173-107">*pDestSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3173-108">Tipo: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="e3173-108">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="e3173-109">Puntatore a un'interfaccia [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) .</span><span class="sxs-lookup"><span data-stu-id="e3173-109">Pointer to an [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface.</span></span> <span data-ttu-id="e3173-110">Specifica la superficie di destinazione che riceve l'immagine.</span><span class="sxs-lookup"><span data-stu-id="e3173-110">Specifies the destination surface, which receives the image.</span></span>

</dd> <dt>

<span data-ttu-id="e3173-111">*pDestPalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3173-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3173-112">Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="e3173-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="e3173-113">Puntatore a una struttura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la tavolozza di destinazione di 256 colori o **null**.</span><span class="sxs-lookup"><span data-stu-id="e3173-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e3173-114">*pDestRect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3173-114">*pDestRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3173-115">Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="e3173-115">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="e3173-116">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e3173-116">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="e3173-117">Specifica il rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e3173-117">Specifies the destination rectangle.</span></span> <span data-ttu-id="e3173-118">Impostare questo parametro su **null** per specificare l'intera superficie.</span><span class="sxs-lookup"><span data-stu-id="e3173-118">Set this parameter to **NULL** to specify the entire surface.</span></span>

</dd> <dt>

<span data-ttu-id="e3173-119">*pSrcMemory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3173-119">*pSrcMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3173-120">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e3173-120">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e3173-121">Puntatore all'angolo superiore sinistro dell'immagine di origine in memoria.</span><span class="sxs-lookup"><span data-stu-id="e3173-121">Pointer to the upper left corner of the source image in memory.</span></span>

</dd> <dt>

<span data-ttu-id="e3173-122">*SrcFormat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3173-122">*SrcFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3173-123">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="e3173-123">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="e3173-124">Membro del tipo enumerato [D3DFORMAT](d3dformat.md) , il formato pixel dell'immagine di origine.</span><span class="sxs-lookup"><span data-stu-id="e3173-124">Member of the [D3DFORMAT](d3dformat.md) enumerated type, the pixel format of the source image.</span></span>

</dd> <dt>

<span data-ttu-id="e3173-125">*SrcPitch* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3173-125">*SrcPitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3173-126">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e3173-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e3173-127">Pitch of source image, in bytes.</span><span class="sxs-lookup"><span data-stu-id="e3173-127">Pitch of source image, in bytes.</span></span> <span data-ttu-id="e3173-128">Per i formati DXT, questo numero deve rappresentare la larghezza di una riga di celle, in byte.</span><span class="sxs-lookup"><span data-stu-id="e3173-128">For DXT formats, this number should represent the width of one row of cells, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="e3173-129">*pSrcPalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3173-129">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3173-130">Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="e3173-130">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="e3173-131">Puntatore a una struttura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la tavolozza di origine di 256 colori o **null**.</span><span class="sxs-lookup"><span data-stu-id="e3173-131">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the source palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e3173-132">*pSrcRect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3173-132">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3173-133">Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="e3173-133">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="e3173-134">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e3173-134">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="e3173-135">Specifica le dimensioni dell'immagine di origine in memoria.</span><span class="sxs-lookup"><span data-stu-id="e3173-135">Specifies the dimensions of the source image in memory.</span></span> <span data-ttu-id="e3173-136">Questo valore non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="e3173-136">This value cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e3173-137">*Filtro* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="e3173-137">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3173-138">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e3173-138">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e3173-139">Combinazione di uno o più [ \_ filtri D3DX](d3dx-filter.md) che controllano il modo in cui l'immagine viene filtrata.</span><span class="sxs-lookup"><span data-stu-id="e3173-139">Combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="e3173-140">Specificare \_ il valore predefinito di D3DX per questo parametro equivale a specificare \_ il \_ \| \_ dithering del filtro D3DX del triangolo di filtro D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="e3173-140">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="e3173-141">*ColorKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3173-141">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3173-142">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="e3173-142">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="e3173-143">Valore [**D3DCOLOR**](d3dcolor.md) da sostituire con nero trasparente oppure 0 per disabilitare il colorkey.</span><span class="sxs-lookup"><span data-stu-id="e3173-143">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="e3173-144">Si tratta sempre di un colore ARGB a 32 bit, indipendente dal formato di immagine di origine.</span><span class="sxs-lookup"><span data-stu-id="e3173-144">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="e3173-145">Alfa è significativo e in genere deve essere impostato su FF per le chiavi di colore opache.</span><span class="sxs-lookup"><span data-stu-id="e3173-145">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="e3173-146">Pertanto, per il nero opaco, il valore sarà uguale a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="e3173-146">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3173-147">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e3173-147">Return value</span></span>

<span data-ttu-id="e3173-148">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e3173-148">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e3173-149">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e3173-149">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e3173-150">Se la funzione ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="e3173-150">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3173-151">Commenti</span><span class="sxs-lookup"><span data-stu-id="e3173-151">Remarks</span></span>

<span data-ttu-id="e3173-152">Questa funzione gestisce la conversione da e verso formati di trama compressi.</span><span class="sxs-lookup"><span data-stu-id="e3173-152">This function handles conversion to and from compressed texture formats.</span></span>

<span data-ttu-id="e3173-153">La scrittura in una superficie non di livello zero non comporterà l'aggiornamento del rettangolo modificato.</span><span class="sxs-lookup"><span data-stu-id="e3173-153">Writing to a non-level-zero surface will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="e3173-154">Se viene chiamato **D3DXLoadSurfaceFromMemory** e la superficie non è già sporca (si tratta di un problema improbabile in scenari di utilizzo normali), l'applicazione deve chiamare in modo esplicito [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) sulla superficie.</span><span class="sxs-lookup"><span data-stu-id="e3173-154">If **D3DXLoadSurfaceFromMemory** is called and the surface was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) on the surface.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3173-155">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e3173-155">Requirements</span></span>



| <span data-ttu-id="e3173-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3173-156">Requirement</span></span> | <span data-ttu-id="e3173-157">Valore</span><span class="sxs-lookup"><span data-stu-id="e3173-157">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e3173-158">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e3173-158">Header</span></span><br/>  | <dl> <span data-ttu-id="e3173-159"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3173-159"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="e3173-160">Libreria</span><span class="sxs-lookup"><span data-stu-id="e3173-160">Library</span></span><br/> | <dl> <span data-ttu-id="e3173-161"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e3173-161"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="e3173-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e3173-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3173-163">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="e3173-163">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
