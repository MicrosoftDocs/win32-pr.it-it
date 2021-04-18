---
description: Salva una superficie in un file.
ms.assetid: 28bbf728-afde-4d25-8562-9d6a957aab2d
title: Funzione D3DXSaveSurfaceToFile (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveSurfaceToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cd19e0a8f7b9557b6bcbe6c71afcdca7c9037b70
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322600"
---
# <a name="d3dxsavesurfacetofile-function"></a><span data-ttu-id="6275b-103">D3DXSaveSurfaceToFile (funzione)</span><span class="sxs-lookup"><span data-stu-id="6275b-103">D3DXSaveSurfaceToFile function</span></span>

<span data-ttu-id="6275b-104">Salva una superficie in un file.</span><span class="sxs-lookup"><span data-stu-id="6275b-104">Saves a surface to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="6275b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6275b-105">Syntax</span></span>


```C++
HRESULT D3DXSaveSurfaceToFile(
  _In_       LPCTSTR              pDestFile,
  _In_       D3DXIMAGE_FILEFORMAT DestFormat,
  _In_       LPDIRECT3DSURFACE9   pSrcSurface,
  _In_ const PALETTEENTRY         *pSrcPalette,
  _In_ const RECT                 *pSrcRect
);
```



## <a name="parameters"></a><span data-ttu-id="6275b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6275b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6275b-107">*pDestFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6275b-107">*pDestFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6275b-108">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6275b-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6275b-109">Puntatore a una stringa che specifica il nome del file dell'immagine di destinazione.</span><span class="sxs-lookup"><span data-stu-id="6275b-109">Pointer to a string that specifies the file name of the destination image.</span></span> <span data-ttu-id="6275b-110">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="6275b-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="6275b-111">In caso contrario, il tipo di dati String viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="6275b-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="6275b-112">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="6275b-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="6275b-113">*DestFormat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6275b-113">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6275b-114">Tipo: **[ **D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="6275b-114">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

<span data-ttu-id="6275b-115">[**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md) che specifica il formato di file da utilizzare per il salvataggio.</span><span class="sxs-lookup"><span data-stu-id="6275b-115">[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md) specifying the file format to use when saving.</span></span> <span data-ttu-id="6275b-116">Questa funzione supporta il salvataggio in tutti i formati **D3DXIMAGE \_ FileFormat** ad eccezione di Portable Pixmap (. ppm) e targa/Truevision Graphics Adapter (. tga).</span><span class="sxs-lookup"><span data-stu-id="6275b-116">This function supports saving to all **D3DXIMAGE\_FILEFORMAT** formats except Portable Pixmap (.ppm) and Targa/Truevision Graphics Adapter (.tga).</span></span>

</dd> <dt>

<span data-ttu-id="6275b-117">*pSrcSurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6275b-117">*pSrcSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6275b-118">Tipo: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="6275b-118">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="6275b-119">Puntatore all'interfaccia [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) che contiene l'immagine da salvare.</span><span class="sxs-lookup"><span data-stu-id="6275b-119">Pointer to [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface, containing the image to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="6275b-120">*pSrcPalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6275b-120">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6275b-121">Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="6275b-121">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="6275b-122">Puntatore a una struttura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) contenente una tavolozza di colori 256.</span><span class="sxs-lookup"><span data-stu-id="6275b-122">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure containing a palette of 256 colors.</span></span> <span data-ttu-id="6275b-123">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="6275b-123">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6275b-124">*pSrcRect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6275b-124">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6275b-125">Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="6275b-125">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="6275b-126">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="6275b-126">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="6275b-127">Specifica il rettangolo di origine.</span><span class="sxs-lookup"><span data-stu-id="6275b-127">Specifies the source rectangle.</span></span> <span data-ttu-id="6275b-128">Impostare questo parametro su **null** per specificare l'intera immagine.</span><span class="sxs-lookup"><span data-stu-id="6275b-128">Set this parameter to **NULL** to specify the entire image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6275b-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6275b-129">Return value</span></span>

<span data-ttu-id="6275b-130">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6275b-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6275b-131">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6275b-131">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6275b-132">Se la funzione ha esito negativo, il valore restituito può essere il seguente: D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="6275b-132">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="6275b-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="6275b-133">Remarks</span></span>

<span data-ttu-id="6275b-134">L'impostazione del compilatore determina anche la versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="6275b-134">The compiler setting also determines the function version.</span></span> <span data-ttu-id="6275b-135">Se è definito Unicode, la chiamata di funzione viene risolta in D3DXSaveSurfaceToFileW.</span><span class="sxs-lookup"><span data-stu-id="6275b-135">If Unicode is defined, the function call resolves to D3DXSaveSurfaceToFileW.</span></span> <span data-ttu-id="6275b-136">In caso contrario, la chiamata di funzione viene risolta in D3DXSaveSurfaceToFileA perché vengono utilizzate le stringhe ANSI.</span><span class="sxs-lookup"><span data-stu-id="6275b-136">Otherwise, the function call resolves to D3DXSaveSurfaceToFileA because ANSI strings are being used.</span></span>

<span data-ttu-id="6275b-137">Questa funzione gestisce la conversione da e verso formati di trama compressi.</span><span class="sxs-lookup"><span data-stu-id="6275b-137">This function handles conversion to and from compressed texture formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="6275b-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6275b-138">Requirements</span></span>



| <span data-ttu-id="6275b-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="6275b-139">Requirement</span></span> | <span data-ttu-id="6275b-140">Valore</span><span class="sxs-lookup"><span data-stu-id="6275b-140">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6275b-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6275b-141">Header</span></span><br/>  | <dl> <span data-ttu-id="6275b-142"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="6275b-142"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="6275b-143">Libreria</span><span class="sxs-lookup"><span data-stu-id="6275b-143">Library</span></span><br/> | <dl> <span data-ttu-id="6275b-144"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6275b-144"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="6275b-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6275b-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6275b-146">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="6275b-146">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="6275b-147">**D3DXSaveTextureToFile**</span><span class="sxs-lookup"><span data-stu-id="6275b-147">**D3DXSaveTextureToFile**</span></span>](d3dxsavetexturetofile.md)
</dt> <dt>

[<span data-ttu-id="6275b-148">**D3DXSaveVolumeToFile**</span><span class="sxs-lookup"><span data-stu-id="6275b-148">**D3DXSaveVolumeToFile**</span></span>](d3dxsavevolumetofile.md)
</dt> </dl>

 

 
