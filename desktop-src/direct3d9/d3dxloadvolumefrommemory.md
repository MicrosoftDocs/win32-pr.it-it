---
description: Carica un volume dalla memoria.
ms.assetid: 9f74fcc0-f935-4466-865b-e798711a1f2f
title: Funzione D3DXLoadVolumeFromMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadVolumeFromMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7d6c3f1bdfe40f19eeb57b4f0d8a38c40a239404
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322139"
---
# <a name="d3dxloadvolumefrommemory-function"></a><span data-ttu-id="6e119-103">D3DXLoadVolumeFromMemory (funzione)</span><span class="sxs-lookup"><span data-stu-id="6e119-103">D3DXLoadVolumeFromMemory function</span></span>

<span data-ttu-id="6e119-104">Carica un volume dalla memoria.</span><span class="sxs-lookup"><span data-stu-id="6e119-104">Loads a volume from memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e119-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6e119-105">Syntax</span></span>


```C++
HRESULT D3DXLoadVolumeFromMemory(
  _In_       LPDIRECT3DVOLUME9 pDestVolume,
  _In_ const PALETTEENTRY      *pDestPalette,
  _In_ const D3DBOX            *pDestBox,
  _In_       LPCVOID           pSrcMemory,
  _In_       D3DFORMAT         SrcFormat,
  _In_       UINT              SrcRowPitch,
  _In_       UINT              SrcSlicePitch,
  _In_ const PALETTEENTRY      *pSrcPalette,
  _In_ const D3DBOX            *pSrcBox,
  _In_       DWORD             Filter,
  _In_       D3DCOLOR          ColorKey
);
```



## <a name="parameters"></a><span data-ttu-id="6e119-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6e119-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e119-107">*pDestVolume* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6e119-107">*pDestVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e119-108">Tipo: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="6e119-108">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="6e119-109">Puntatore a un'interfaccia [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) .</span><span class="sxs-lookup"><span data-stu-id="6e119-109">Pointer to an [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface.</span></span> <span data-ttu-id="6e119-110">Specifica il volume di destinazione, che riceve l'immagine.</span><span class="sxs-lookup"><span data-stu-id="6e119-110">Specifies the destination volume, which receives the image.</span></span>

</dd> <dt>

<span data-ttu-id="6e119-111">*pDestPalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6e119-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e119-112">Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="6e119-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="6e119-113">Puntatore a una struttura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la tavolozza di destinazione di 256 colori o **null**.</span><span class="sxs-lookup"><span data-stu-id="6e119-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6e119-114">*pDestBox* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6e119-114">*pDestBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e119-115">Tipo: **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="6e119-115">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="6e119-116">Puntatore a una struttura [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="6e119-116">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="6e119-117">Specifica la casella di destinazione.</span><span class="sxs-lookup"><span data-stu-id="6e119-117">Specifies the destination box.</span></span> <span data-ttu-id="6e119-118">Impostare questo parametro su **null** per specificare l'intero volume.</span><span class="sxs-lookup"><span data-stu-id="6e119-118">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="6e119-119">*pSrcMemory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6e119-119">*pSrcMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e119-120">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6e119-120">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6e119-121">Puntatore all'angolo superiore sinistro del volume di origine in memoria.</span><span class="sxs-lookup"><span data-stu-id="6e119-121">Pointer to the top-left corner of the source volume in memory.</span></span>

</dd> <dt>

<span data-ttu-id="6e119-122">*SrcFormat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6e119-122">*SrcFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e119-123">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="6e119-123">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="6e119-124">Membro del tipo enumerato [D3DFORMAT](d3dformat.md) , il formato pixel del volume di origine.</span><span class="sxs-lookup"><span data-stu-id="6e119-124">Member of the [D3DFORMAT](d3dformat.md) enumerated type, the pixel format of the source volume.</span></span>

</dd> <dt>

<span data-ttu-id="6e119-125">*SrcRowPitch* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6e119-125">*SrcRowPitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e119-126">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6e119-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6e119-127">Pitch of source image, in bytes.</span><span class="sxs-lookup"><span data-stu-id="6e119-127">Pitch of source image, in bytes.</span></span> <span data-ttu-id="6e119-128">Per i formati DXT (formati di trama compressi), questo numero deve rappresentare le dimensioni di una riga di celle, in byte.</span><span class="sxs-lookup"><span data-stu-id="6e119-128">For DXT formats (compressed texture formats), this number should represent the size of one row of cells, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="6e119-129">*SrcSlicePitch* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6e119-129">*SrcSlicePitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e119-130">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6e119-130">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6e119-131">Pitch of source image, in bytes.</span><span class="sxs-lookup"><span data-stu-id="6e119-131">Pitch of source image, in bytes.</span></span> <span data-ttu-id="6e119-132">Per i formati DXT (formati di trama compressi), questo numero deve rappresentare la dimensione di una sezione di celle, in byte.</span><span class="sxs-lookup"><span data-stu-id="6e119-132">For DXT formats (compressed texture formats), this number should represent the size of one slice of cells, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="6e119-133">*pSrcPalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6e119-133">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e119-134">Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="6e119-134">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="6e119-135">Puntatore a una struttura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la tavolozza di origine di 256 colori o **null**.</span><span class="sxs-lookup"><span data-stu-id="6e119-135">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the source palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6e119-136">*pSrcBox* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6e119-136">*pSrcBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e119-137">Tipo: **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="6e119-137">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="6e119-138">Puntatore a una struttura [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="6e119-138">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="6e119-139">Specifica la casella di origine.</span><span class="sxs-lookup"><span data-stu-id="6e119-139">Specifies the source box.</span></span> <span data-ttu-id="6e119-140">**Null** non è un valore valido per questo parametro.</span><span class="sxs-lookup"><span data-stu-id="6e119-140">**NULL** is not a valid value for this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="6e119-141">*Filtro* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="6e119-141">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e119-142">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6e119-142">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6e119-143">Combinazione di uno o più [ \_ filtri D3DX](d3dx-filter.md) che controllano il modo in cui l'immagine viene filtrata.</span><span class="sxs-lookup"><span data-stu-id="6e119-143">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="6e119-144">Specificare \_ il valore predefinito di D3DX per questo parametro equivale a specificare \_ il \_ \| \_ dithering del filtro D3DX del triangolo di filtro D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="6e119-144">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="6e119-145">*ColorKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6e119-145">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e119-146">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="6e119-146">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="6e119-147">Valore [**D3DCOLOR**](d3dcolor.md) da sostituire con nero trasparente oppure 0 per disabilitare il colorkey.</span><span class="sxs-lookup"><span data-stu-id="6e119-147">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="6e119-148">Si tratta sempre di un colore ARGB a 32 bit, indipendente dal formato di immagine di origine.</span><span class="sxs-lookup"><span data-stu-id="6e119-148">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="6e119-149">Alfa è significativo e in genere deve essere impostato su FF per le chiavi di colore opache.</span><span class="sxs-lookup"><span data-stu-id="6e119-149">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="6e119-150">Pertanto, per il nero opaco, il valore sarà uguale a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="6e119-150">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e119-151">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6e119-151">Return value</span></span>

<span data-ttu-id="6e119-152">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6e119-152">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6e119-153">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6e119-153">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6e119-154">Se la funzione ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="6e119-154">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e119-155">Commenti</span><span class="sxs-lookup"><span data-stu-id="6e119-155">Remarks</span></span>

<span data-ttu-id="6e119-156">La scrittura in una superficie non di livello zero della trama del volume non comporterà l'aggiornamento del rettangolo modificato.</span><span class="sxs-lookup"><span data-stu-id="6e119-156">Writing to a non-level-zero surface of the volume texture will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="6e119-157">Se viene chiamato **D3DXLoadVolumeFromMemory** e la trama non è già sporca (probabilmente in scenari di utilizzo normali), l'applicazione deve chiamare in modo esplicito [**IDirect3DVolumeTexture9:: AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) sulla trama del volume.</span><span class="sxs-lookup"><span data-stu-id="6e119-157">If **D3DXLoadVolumeFromMemory** is called and the texture was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**IDirect3DVolumeTexture9::AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) on the volume texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e119-158">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6e119-158">Requirements</span></span>



| <span data-ttu-id="6e119-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e119-159">Requirement</span></span> | <span data-ttu-id="6e119-160">Valore</span><span class="sxs-lookup"><span data-stu-id="6e119-160">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6e119-161">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6e119-161">Header</span></span><br/>  | <dl> <span data-ttu-id="6e119-162"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e119-162"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="6e119-163">Libreria</span><span class="sxs-lookup"><span data-stu-id="6e119-163">Library</span></span><br/> | <dl> <span data-ttu-id="6e119-164"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6e119-164"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="6e119-165">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6e119-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e119-166">**D3DXLoadVolumeFromFile**</span><span class="sxs-lookup"><span data-stu-id="6e119-166">**D3DXLoadVolumeFromFile**</span></span>](d3dxloadvolumefromfile.md)
</dt> <dt>

[<span data-ttu-id="6e119-167">**D3DXLoadVolumeFromResource**</span><span class="sxs-lookup"><span data-stu-id="6e119-167">**D3DXLoadVolumeFromResource**</span></span>](d3dxloadvolumefromresource.md)
</dt> <dt>

[<span data-ttu-id="6e119-168">**D3DXLoadVolumeFromVolume**</span><span class="sxs-lookup"><span data-stu-id="6e119-168">**D3DXLoadVolumeFromVolume**</span></span>](d3dxloadvolumefromvolume.md)
</dt> <dt>

[<span data-ttu-id="6e119-169">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="6e119-169">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
