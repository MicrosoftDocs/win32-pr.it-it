---
description: Carica un volume da una risorsa.
ms.assetid: 3fa1243b-5e31-4737-8d3c-08852d6528d9
title: Funzione D3DXLoadVolumeFromResource (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadVolumeFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9d57ce492db24ac9920662d4de5baed4650dd801
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322138"
---
# <a name="d3dxloadvolumefromresource-function"></a><span data-ttu-id="5dbeb-103">D3DXLoadVolumeFromResource (funzione)</span><span class="sxs-lookup"><span data-stu-id="5dbeb-103">D3DXLoadVolumeFromResource function</span></span>

<span data-ttu-id="5dbeb-104">Carica un volume da una risorsa.</span><span class="sxs-lookup"><span data-stu-id="5dbeb-104">Loads a volume from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="5dbeb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5dbeb-105">Syntax</span></span>


```C++
HRESULT D3DXLoadVolumeFromResource(
  _In_       LPDIRECT3DVOLUME9 pDestVolume,
  _In_ const PALETTEENTRY      *pDestPalette,
  _In_ const D3DBOX            *pDestBox,
  _In_       HMODULE           hSrcModule,
  _In_       LPCSTR            pSrcResource,
  _In_ const D3DBOX            *pSrcBox,
  _In_       DWORD             Filter,
  _In_       D3DCOLOR          ColorKey,
  _In_       D3DXIMAGE_INFO    *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="5dbeb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5dbeb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5dbeb-107">*pDestVolume* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5dbeb-107">*pDestVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5dbeb-108">Tipo: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="5dbeb-108">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="5dbeb-109">Puntatore a un'interfaccia [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) .</span><span class="sxs-lookup"><span data-stu-id="5dbeb-109">Pointer to an [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface.</span></span> <span data-ttu-id="5dbeb-110">Specifica il volume di destinazione.</span><span class="sxs-lookup"><span data-stu-id="5dbeb-110">Specifies the destination volume.</span></span>

</dd> <dt>

<span data-ttu-id="5dbeb-111">*pDestPalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5dbeb-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5dbeb-112">Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="5dbeb-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="5dbeb-113">Puntatore a una struttura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la tavolozza di destinazione di 256 colori o **null**.</span><span class="sxs-lookup"><span data-stu-id="5dbeb-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5dbeb-114">*pDestBox* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5dbeb-114">*pDestBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5dbeb-115">Tipo: **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="5dbeb-115">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="5dbeb-116">Puntatore a una struttura [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="5dbeb-116">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="5dbeb-117">Specifica la casella di destinazione.</span><span class="sxs-lookup"><span data-stu-id="5dbeb-117">Specifies the destination box.</span></span> <span data-ttu-id="5dbeb-118">Impostare questo parametro su **null** per specificare l'intero volume.</span><span class="sxs-lookup"><span data-stu-id="5dbeb-118">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="5dbeb-119">*hSrcModule* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5dbeb-119">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5dbeb-120">Tipo: **[ **hmodule**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5dbeb-120">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5dbeb-121">Handle per il modulo in cui si trova la risorsa o **null** per il modulo associato all'immagine utilizzata dal sistema operativo per creare il processo corrente.</span><span class="sxs-lookup"><span data-stu-id="5dbeb-121">Handle to the module where the resource is located, or **NULL** for module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="5dbeb-122">*pSrcResource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5dbeb-122">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5dbeb-123">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5dbeb-123">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5dbeb-124">Puntatore a una stringa che specifica il nome del file dell'immagine di origine.</span><span class="sxs-lookup"><span data-stu-id="5dbeb-124">Pointer to a string that specifies the file name of the source image.</span></span> <span data-ttu-id="5dbeb-125">Se \_ sono definiti Unicode o Unicode, questo tipo di parametro è LPCWSTR; in caso contrario, il tipo è LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="5dbeb-125">If UNICODE or \_UNICODE are defined, this parameter type is LPCWSTR, otherwise, the type is LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="5dbeb-126">*pSrcBox* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5dbeb-126">*pSrcBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5dbeb-127">Tipo: **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="5dbeb-127">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="5dbeb-128">Puntatore a una struttura [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="5dbeb-128">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="5dbeb-129">Specifica la casella di origine.</span><span class="sxs-lookup"><span data-stu-id="5dbeb-129">Specifies the source box.</span></span> <span data-ttu-id="5dbeb-130">Impostare questo parametro su **null** per specificare l'intero volume.</span><span class="sxs-lookup"><span data-stu-id="5dbeb-130">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="5dbeb-131">*Filtro* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="5dbeb-131">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5dbeb-132">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5dbeb-132">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5dbeb-133">Combinazione di uno o più [ \_ filtri D3DX](d3dx-filter.md), che controllano il modo in cui l'immagine viene filtrata.</span><span class="sxs-lookup"><span data-stu-id="5dbeb-133">Combination of one or more [D3DX\_FILTER](d3dx-filter.md), controlling how the image is filtered.</span></span> <span data-ttu-id="5dbeb-134">Specificare \_ il valore predefinito di D3DX per questo parametro equivale a specificare \_ il \_ \| \_ dithering del filtro D3DX del triangolo di filtro D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="5dbeb-134">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="5dbeb-135">*ColorKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5dbeb-135">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5dbeb-136">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="5dbeb-136">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="5dbeb-137">Valore [**D3DCOLOR**](d3dcolor.md) da sostituire con nero trasparente oppure 0 per disabilitare il colorkey.</span><span class="sxs-lookup"><span data-stu-id="5dbeb-137">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="5dbeb-138">Si tratta sempre di un colore ARGB a 32 bit, indipendente dal formato di immagine di origine.</span><span class="sxs-lookup"><span data-stu-id="5dbeb-138">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="5dbeb-139">Alfa è significativo e in genere deve essere impostato su FF per le chiavi di colore opache.</span><span class="sxs-lookup"><span data-stu-id="5dbeb-139">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="5dbeb-140">Pertanto, per il nero opaco, il valore sarà uguale a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="5dbeb-140">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="5dbeb-141">*pSrcInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5dbeb-141">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5dbeb-142">Tipo: **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="5dbeb-142">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="5dbeb-143">Puntatore a una struttura di [**\_ informazioni D3DXIMAGE**](d3dximage-info.md) per la compilazione di una descrizione dei dati nel file di immagine di origine o **null**.</span><span class="sxs-lookup"><span data-stu-id="5dbeb-143">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5dbeb-144">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5dbeb-144">Return value</span></span>

<span data-ttu-id="5dbeb-145">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5dbeb-145">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5dbeb-146">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5dbeb-146">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5dbeb-147">Se la funzione ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="5dbeb-147">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="5dbeb-148">Commenti</span><span class="sxs-lookup"><span data-stu-id="5dbeb-148">Remarks</span></span>

<span data-ttu-id="5dbeb-149">La risorsa da caricare deve essere una risorsa bitmap ( \_ bitmap RT).</span><span class="sxs-lookup"><span data-stu-id="5dbeb-149">The resource being loaded must be a bitmap resource(RT\_BITMAP).</span></span>

<span data-ttu-id="5dbeb-150">Questa funzione gestisce la conversione da e verso formati di trama compressi.</span><span class="sxs-lookup"><span data-stu-id="5dbeb-150">This function handles conversion to and from compressed texture formats.</span></span>

<span data-ttu-id="5dbeb-151">La scrittura in una superficie non di livello zero della trama del volume non comporterà l'aggiornamento del rettangolo modificato.</span><span class="sxs-lookup"><span data-stu-id="5dbeb-151">Writing to a non-level-zero surface of the volume texture will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="5dbeb-152">Se viene chiamato [**D3DXLoadVolumeFromFile**](d3dxloadvolumefromfile.md) e la trama non è già sporca (probabilmente in scenari di utilizzo normali), l'applicazione deve chiamare in modo esplicito [**IDirect3DVolumeTexture9:: AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) sulla trama del volume.</span><span class="sxs-lookup"><span data-stu-id="5dbeb-152">If [**D3DXLoadVolumeFromFile**](d3dxloadvolumefromfile.md) is called and the texture was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**IDirect3DVolumeTexture9::AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) on the volume texture.</span></span>

<span data-ttu-id="5dbeb-153">Questa funzione supporta le stringhe Unicode e ANSI.</span><span class="sxs-lookup"><span data-stu-id="5dbeb-153">This function supports both Unicode and ANSI strings.</span></span>

## <a name="requirements"></a><span data-ttu-id="5dbeb-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5dbeb-154">Requirements</span></span>



| <span data-ttu-id="5dbeb-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="5dbeb-155">Requirement</span></span> | <span data-ttu-id="5dbeb-156">Valore</span><span class="sxs-lookup"><span data-stu-id="5dbeb-156">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5dbeb-157">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5dbeb-157">Header</span></span><br/>  | <dl> <span data-ttu-id="5dbeb-158"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="5dbeb-158"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="5dbeb-159">Libreria</span><span class="sxs-lookup"><span data-stu-id="5dbeb-159">Library</span></span><br/> | <dl> <span data-ttu-id="5dbeb-160"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5dbeb-160"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="5dbeb-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5dbeb-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dbeb-162">**D3DXLoadVolumeFromFile**</span><span class="sxs-lookup"><span data-stu-id="5dbeb-162">**D3DXLoadVolumeFromFile**</span></span>](d3dxloadvolumefromfile.md)
</dt> <dt>

[<span data-ttu-id="5dbeb-163">**D3DXLoadVolumeFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="5dbeb-163">**D3DXLoadVolumeFromFileInMemory**</span></span>](d3dxloadvolumefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="5dbeb-164">**D3DXLoadVolumeFromMemory**</span><span class="sxs-lookup"><span data-stu-id="5dbeb-164">**D3DXLoadVolumeFromMemory**</span></span>](d3dxloadvolumefrommemory.md)
</dt> <dt>

[<span data-ttu-id="5dbeb-165">**D3DXLoadVolumeFromVolume**</span><span class="sxs-lookup"><span data-stu-id="5dbeb-165">**D3DXLoadVolumeFromVolume**</span></span>](d3dxloadvolumefromvolume.md)
</dt> <dt>

[<span data-ttu-id="5dbeb-166">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="5dbeb-166">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
