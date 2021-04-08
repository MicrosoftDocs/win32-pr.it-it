---
description: Carica un volume da un altro volume.
ms.assetid: bc162f91-feb7-4571-ae4a-abaa5e7953f6
title: Funzione D3DXLoadVolumeFromVolume (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadVolumeFromVolume
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: da2cedf42533fa1d170269e97a366f7e4a1a41f5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969448"
---
# <a name="d3dxloadvolumefromvolume-function"></a><span data-ttu-id="a3d5c-103">D3DXLoadVolumeFromVolume (funzione)</span><span class="sxs-lookup"><span data-stu-id="a3d5c-103">D3DXLoadVolumeFromVolume function</span></span>

<span data-ttu-id="a3d5c-104">Carica un volume da un altro volume.</span><span class="sxs-lookup"><span data-stu-id="a3d5c-104">Loads a volume from another volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3d5c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a3d5c-105">Syntax</span></span>


```C++
HRESULT D3DXLoadVolumeFromVolume(
  _In_       LPDIRECT3DVOLUME9 pDestVolume,
  _In_ const PALETTEENTRY      *pDestPalette,
  _In_ const D3DBOX            *pDestBox,
  _In_       LPDIRECT3DVOLUME9 pSrcVolume,
  _In_ const PALETTEENTRY      *pSrcPalette,
  _In_ const D3DBOX            *pSrcBox,
  _In_       DWORD             Filter,
  _In_       D3DCOLOR          ColorKey
);
```



## <a name="parameters"></a><span data-ttu-id="a3d5c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a3d5c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3d5c-107">*pDestVolume* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3d5c-107">*pDestVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3d5c-108">Tipo: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="a3d5c-108">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="a3d5c-109">Puntatore a un'interfaccia [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) .</span><span class="sxs-lookup"><span data-stu-id="a3d5c-109">Pointer to an [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface.</span></span> <span data-ttu-id="a3d5c-110">Specifica il volume di destinazione, che riceve l'immagine.</span><span class="sxs-lookup"><span data-stu-id="a3d5c-110">Specifies the destination volume, which receives the image.</span></span>

</dd> <dt>

<span data-ttu-id="a3d5c-111">*pDestPalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3d5c-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3d5c-112">Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="a3d5c-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="a3d5c-113">Puntatore a una struttura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la tavolozza di destinazione di 256 colori o **null**.</span><span class="sxs-lookup"><span data-stu-id="a3d5c-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a3d5c-114">*pDestBox* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3d5c-114">*pDestBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3d5c-115">Tipo: **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="a3d5c-115">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="a3d5c-116">Puntatore a una struttura [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="a3d5c-116">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="a3d5c-117">Specifica la casella di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a3d5c-117">Specifies the destination box.</span></span> <span data-ttu-id="a3d5c-118">Impostare questo parametro su **null** per specificare l'intero volume.</span><span class="sxs-lookup"><span data-stu-id="a3d5c-118">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="a3d5c-119">*pSrcVolume* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3d5c-119">*pSrcVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3d5c-120">Tipo: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="a3d5c-120">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="a3d5c-121">Puntatore a un'interfaccia [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) .</span><span class="sxs-lookup"><span data-stu-id="a3d5c-121">A Pointer to an [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface.</span></span> <span data-ttu-id="a3d5c-122">Specifica il volume di origine.</span><span class="sxs-lookup"><span data-stu-id="a3d5c-122">Specifies the source volume.</span></span>

</dd> <dt>

<span data-ttu-id="a3d5c-123">*pSrcPalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3d5c-123">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3d5c-124">Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="a3d5c-124">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="a3d5c-125">Puntatore a una struttura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la tavolozza di origine di 256 colori o **null**.</span><span class="sxs-lookup"><span data-stu-id="a3d5c-125">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the source palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a3d5c-126">*pSrcBox* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3d5c-126">*pSrcBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3d5c-127">Tipo: **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="a3d5c-127">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="a3d5c-128">Puntatore a una struttura [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="a3d5c-128">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="a3d5c-129">Specifica la casella di origine.</span><span class="sxs-lookup"><span data-stu-id="a3d5c-129">Specifies the source box.</span></span> <span data-ttu-id="a3d5c-130">Impostare questo parametro su **null** per specificare l'intero volume.</span><span class="sxs-lookup"><span data-stu-id="a3d5c-130">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="a3d5c-131">*Filtro* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="a3d5c-131">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3d5c-132">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a3d5c-132">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a3d5c-133">Combinazione di uno o più [ \_ filtri D3DX](d3dx-filter.md), che controllano il modo in cui l'immagine viene filtrata.</span><span class="sxs-lookup"><span data-stu-id="a3d5c-133">A combination of one or more [D3DX\_FILTER](d3dx-filter.md), controlling how the image is filtered.</span></span> <span data-ttu-id="a3d5c-134">Specificare \_ il valore predefinito di D3DX per questo parametro equivale a specificare \_ il \_ \| \_ dithering del filtro D3DX del triangolo di filtro D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="a3d5c-134">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="a3d5c-135">*ColorKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3d5c-135">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3d5c-136">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="a3d5c-136">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="a3d5c-137">Valore [**D3DCOLOR**](d3dcolor.md) da sostituire con nero trasparente oppure 0 per disabilitare il colorkey.</span><span class="sxs-lookup"><span data-stu-id="a3d5c-137">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="a3d5c-138">Si tratta sempre di un colore ARGB a 32 bit, indipendente dal formato di immagine di origine.</span><span class="sxs-lookup"><span data-stu-id="a3d5c-138">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="a3d5c-139">Alfa è significativo e in genere deve essere impostato su FF per le chiavi di colore opache.</span><span class="sxs-lookup"><span data-stu-id="a3d5c-139">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="a3d5c-140">Pertanto, per il nero opaco, il valore sarà uguale a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="a3d5c-140">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3d5c-141">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a3d5c-141">Return value</span></span>

<span data-ttu-id="a3d5c-142">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a3d5c-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a3d5c-143">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a3d5c-143">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a3d5c-144">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="a3d5c-144">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3d5c-145">Commenti</span><span class="sxs-lookup"><span data-stu-id="a3d5c-145">Remarks</span></span>

<span data-ttu-id="a3d5c-146">La scrittura in una superficie non di livello zero della trama del volume non comporterà l'aggiornamento del rettangolo modificato.</span><span class="sxs-lookup"><span data-stu-id="a3d5c-146">Writing to a non-level-zero surface of the volume texture will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="a3d5c-147">Se viene chiamato **D3DXLoadVolumeFromVolume** e la superficie non è già sporca (si tratta di un problema improbabile in scenari di utilizzo normali), l'applicazione deve chiamare in modo esplicito [**IDirect3DVolumeTexture9:: AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) sulla superficie.</span><span class="sxs-lookup"><span data-stu-id="a3d5c-147">If **D3DXLoadVolumeFromVolume** is called and the surface was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**IDirect3DVolumeTexture9::AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) on the surface.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3d5c-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a3d5c-148">Requirements</span></span>



| <span data-ttu-id="a3d5c-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3d5c-149">Requirement</span></span> | <span data-ttu-id="a3d5c-150">Valore</span><span class="sxs-lookup"><span data-stu-id="a3d5c-150">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a3d5c-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a3d5c-151">Header</span></span><br/>  | <dl> <span data-ttu-id="a3d5c-152"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3d5c-152"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="a3d5c-153">Libreria</span><span class="sxs-lookup"><span data-stu-id="a3d5c-153">Library</span></span><br/> | <dl> <span data-ttu-id="a3d5c-154"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a3d5c-154"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="a3d5c-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a3d5c-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3d5c-156">**D3DXLoadVolumeFromFile**</span><span class="sxs-lookup"><span data-stu-id="a3d5c-156">**D3DXLoadVolumeFromFile**</span></span>](d3dxloadvolumefromfile.md)
</dt> <dt>

[<span data-ttu-id="a3d5c-157">**D3DXLoadVolumeFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="a3d5c-157">**D3DXLoadVolumeFromFileInMemory**</span></span>](d3dxloadvolumefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="a3d5c-158">**D3DXLoadVolumeFromMemory**</span><span class="sxs-lookup"><span data-stu-id="a3d5c-158">**D3DXLoadVolumeFromMemory**</span></span>](d3dxloadvolumefrommemory.md)
</dt> <dt>

[<span data-ttu-id="a3d5c-159">**D3DXLoadVolumeFromResource**</span><span class="sxs-lookup"><span data-stu-id="a3d5c-159">**D3DXLoadVolumeFromResource**</span></span>](d3dxloadvolumefromresource.md)
</dt> <dt>

[<span data-ttu-id="a3d5c-160">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="a3d5c-160">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
