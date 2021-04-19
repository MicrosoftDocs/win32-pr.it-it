---
description: Salva un volume in un file su disco.
ms.assetid: 4d33fba5-e003-4385-b683-aff6723af2a5
title: Funzione D3DXSaveVolumeToFile (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveVolumeToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 36550cda8d9ef664f96e236d2770a82c88412772
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322596"
---
# <a name="d3dxsavevolumetofile-function"></a><span data-ttu-id="3de31-103">D3DXSaveVolumeToFile (funzione)</span><span class="sxs-lookup"><span data-stu-id="3de31-103">D3DXSaveVolumeToFile function</span></span>

<span data-ttu-id="3de31-104">Salva un volume in un file su disco.</span><span class="sxs-lookup"><span data-stu-id="3de31-104">Saves a volume to a file on disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="3de31-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3de31-105">Syntax</span></span>


```C++
HRESULT D3DXSaveVolumeToFile(
  _In_       LPCTSTR              pDestFile,
  _In_       D3DXIMAGE_FILEFORMAT DestFormat,
  _In_       LPDIRECT3DVOLUME9    pSrcVolume,
  _In_ const PALETTEENTRY         *pSrcPalette,
  _In_ const D3DBOX               *pSrcBox
);
```



## <a name="parameters"></a><span data-ttu-id="3de31-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3de31-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3de31-107">*pDestFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3de31-107">*pDestFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3de31-108">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3de31-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3de31-109">Puntatore a una stringa che specifica il nome del file dell'immagine di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3de31-109">Pointer to a string that specifies the file name of the destination image.</span></span> <span data-ttu-id="3de31-110">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="3de31-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="3de31-111">In caso contrario, il tipo di dati String viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="3de31-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="3de31-112">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="3de31-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="3de31-113">*DestFormat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3de31-113">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3de31-114">Tipo: **[ **D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="3de31-114">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

<span data-ttu-id="3de31-115">[**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md) che specifica il formato di file da utilizzare per il salvataggio.</span><span class="sxs-lookup"><span data-stu-id="3de31-115">[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md) specifying the file format to use when saving.</span></span> <span data-ttu-id="3de31-116">Questa funzione supporta il salvataggio in tutti i formati **D3DXIMAGE \_ FileFormat** ad eccezione di Portable Pixmap (. ppm) e targa/Truevision Graphics Adapter (. tga).</span><span class="sxs-lookup"><span data-stu-id="3de31-116">This function supports saving to all **D3DXIMAGE\_FILEFORMAT** formats except Portable Pixmap (.ppm) and Targa/Truevision Graphics Adapter (.tga).</span></span>

</dd> <dt>

<span data-ttu-id="3de31-117">*pSrcVolume* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3de31-117">*pSrcVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3de31-118">Tipo: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="3de31-118">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="3de31-119">Puntatore all'interfaccia [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) che contiene l'immagine da salvare.</span><span class="sxs-lookup"><span data-stu-id="3de31-119">Pointer to [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface containing the image to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="3de31-120">*pSrcPalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3de31-120">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3de31-121">Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="3de31-121">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="3de31-122">Puntatore a una struttura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) contenente una tavolozza di colori 256.</span><span class="sxs-lookup"><span data-stu-id="3de31-122">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure containing a palette of 256 colors.</span></span> <span data-ttu-id="3de31-123">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="3de31-123">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3de31-124">*pSrcBox* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3de31-124">*pSrcBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3de31-125">Tipo: **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="3de31-125">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="3de31-126">Puntatore a una struttura [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="3de31-126">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="3de31-127">Specifica la casella di origine.</span><span class="sxs-lookup"><span data-stu-id="3de31-127">Specifies the source box.</span></span> <span data-ttu-id="3de31-128">Impostare questo parametro su **null** per specificare l'intero volume.</span><span class="sxs-lookup"><span data-stu-id="3de31-128">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3de31-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3de31-129">Return value</span></span>

<span data-ttu-id="3de31-130">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3de31-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3de31-131">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3de31-131">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3de31-132">Se la funzione ha esito negativo, il valore restituito può essere il seguente: D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="3de31-132">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="3de31-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="3de31-133">Remarks</span></span>

<span data-ttu-id="3de31-134">L'impostazione del compilatore determina anche la versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="3de31-134">The compiler setting also determines the function version.</span></span> <span data-ttu-id="3de31-135">Se è definito Unicode, la chiamata di funzione viene risolta in D3DXSaveVolumeToFileW.</span><span class="sxs-lookup"><span data-stu-id="3de31-135">If Unicode is defined, the function call resolves to D3DXSaveVolumeToFileW.</span></span> <span data-ttu-id="3de31-136">In caso contrario, la chiamata di funzione viene risolta in >D3DXSaveVolumeToFileA perché vengono utilizzate stringhe ANSI.</span><span class="sxs-lookup"><span data-stu-id="3de31-136">Otherwise, the function call resolves to >D3DXSaveVolumeToFileA because ANSI strings are being used.</span></span>

<span data-ttu-id="3de31-137">Questa funzione gestisce la conversione da e verso formati di trama compressi.</span><span class="sxs-lookup"><span data-stu-id="3de31-137">This function handles conversion to and from compressed texture formats.</span></span>

<span data-ttu-id="3de31-138">Se il volume è non dinamico (a causa di un parametro Usage impostato su 0 alla creazione) e situato nella memoria video (il pool di memoria impostato su D3DPOOL \_ default), [**D3DXSaveTextureToFile**](d3dxsavetexturetofile.md) avrà esito negativo perché D3DX non può bloccare i volumi non dinamici presenti nella memoria video.</span><span class="sxs-lookup"><span data-stu-id="3de31-138">If the volume is nondynamic (because of a usage parameter set to 0 at the creation) and located in video memory (the memory pool set to D3DPOOL\_DEFAULT), [**D3DXSaveTextureToFile**](d3dxsavetexturetofile.md) will fail because D3DX cannot lock nondynamic volumes located in video memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="3de31-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3de31-139">Requirements</span></span>



| <span data-ttu-id="3de31-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="3de31-140">Requirement</span></span> | <span data-ttu-id="3de31-141">Valore</span><span class="sxs-lookup"><span data-stu-id="3de31-141">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3de31-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3de31-142">Header</span></span><br/>  | <dl> <span data-ttu-id="3de31-143"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="3de31-143"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="3de31-144">Libreria</span><span class="sxs-lookup"><span data-stu-id="3de31-144">Library</span></span><br/> | <dl> <span data-ttu-id="3de31-145"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3de31-145"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="3de31-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3de31-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3de31-147">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="3de31-147">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="3de31-148">**D3DXSaveSurfaceToFile**</span><span class="sxs-lookup"><span data-stu-id="3de31-148">**D3DXSaveSurfaceToFile**</span></span>](d3dxsavesurfacetofile.md)
</dt> <dt>

[<span data-ttu-id="3de31-149">**D3DXSaveTextureToFile**</span><span class="sxs-lookup"><span data-stu-id="3de31-149">**D3DXSaveTextureToFile**</span></span>](d3dxsavetexturetofile.md)
</dt> <dt>

[<span data-ttu-id="3de31-150">**D3DXSaveVolumeToFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="3de31-150">**D3DXSaveVolumeToFileInMemory**</span></span>](d3dxsavevolumetofileinmemory.md)
</dt> </dl>

 

 
