---
description: Salva una trama in un file.
ms.assetid: b14dd893-e967-4be9-81e8-aeb52035d91c
title: Funzione D3DXSaveTextureToFile (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveTextureToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c11cc8b512527fb0610c288fdbaeba6c976604a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322598"
---
# <a name="d3dxsavetexturetofile-function"></a><span data-ttu-id="4e5cb-103">D3DXSaveTextureToFile (funzione)</span><span class="sxs-lookup"><span data-stu-id="4e5cb-103">D3DXSaveTextureToFile function</span></span>

<span data-ttu-id="4e5cb-104">Salva una trama in un file.</span><span class="sxs-lookup"><span data-stu-id="4e5cb-104">Saves a texture to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e5cb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4e5cb-105">Syntax</span></span>


```C++
HRESULT D3DXSaveTextureToFile(
  _In_       LPCTSTR                pDestFile,
  _In_       D3DXIMAGE_FILEFORMAT   DestFormat,
  _In_       LPDIRECT3DBASETEXTURE9 pSrcTexture,
  _In_ const PALETTEENTRY           *pSrcPalette
);
```



## <a name="parameters"></a><span data-ttu-id="4e5cb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4e5cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e5cb-107">*pDestFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e5cb-107">*pDestFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e5cb-108">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e5cb-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4e5cb-109">Puntatore a una stringa che specifica il nome del file dell'immagine di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4e5cb-109">Pointer to a string that specifies the file name of the destination image.</span></span> <span data-ttu-id="4e5cb-110">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="4e5cb-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="4e5cb-111">In caso contrario, il tipo di dati String viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="4e5cb-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="4e5cb-112">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="4e5cb-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="4e5cb-113">*DestFormat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e5cb-113">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e5cb-114">Tipo: **[ **D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="4e5cb-114">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

<span data-ttu-id="4e5cb-115">[**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md) che specifica il formato di file da utilizzare per il salvataggio.</span><span class="sxs-lookup"><span data-stu-id="4e5cb-115">[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md) specifying the file format to use when saving.</span></span> <span data-ttu-id="4e5cb-116">Questa funzione supporta il salvataggio in tutti i formati **D3DXIMAGE \_ FileFormat** ad eccezione di Portable Pixmap (. ppm) e targa/Truevision Graphics Adapter (. tga).</span><span class="sxs-lookup"><span data-stu-id="4e5cb-116">This function supports saving to all **D3DXIMAGE\_FILEFORMAT** formats except Portable Pixmap (.ppm) and Targa/Truevision Graphics Adapter (.tga).</span></span>

</dd> <dt>

<span data-ttu-id="4e5cb-117">*pSrcTexture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e5cb-117">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e5cb-118">Tipo: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span><span class="sxs-lookup"><span data-stu-id="4e5cb-118">Type: **[**LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span></span>

<span data-ttu-id="4e5cb-119">Puntatore all'interfaccia [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) contenente la trama da salvare.</span><span class="sxs-lookup"><span data-stu-id="4e5cb-119">Pointer to [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) interface, containing the texture to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="4e5cb-120">*pSrcPalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e5cb-120">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e5cb-121">Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="4e5cb-121">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="4e5cb-122">Puntatore a una struttura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) contenente una tavolozza di colori 256.</span><span class="sxs-lookup"><span data-stu-id="4e5cb-122">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure containing a palette of 256 colors.</span></span> <span data-ttu-id="4e5cb-123">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="4e5cb-123">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e5cb-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4e5cb-124">Return value</span></span>

<span data-ttu-id="4e5cb-125">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4e5cb-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4e5cb-126">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4e5cb-126">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4e5cb-127">Se la funzione ha esito negativo, il valore restituito può essere il seguente: D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="4e5cb-127">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="4e5cb-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="4e5cb-128">Remarks</span></span>

<span data-ttu-id="4e5cb-129">L'impostazione del compilatore determina anche la versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="4e5cb-129">The compiler setting also determines the function version.</span></span> <span data-ttu-id="4e5cb-130">Se è definito Unicode, la chiamata di funzione viene risolta in D3DXSaveTextureToFileW.</span><span class="sxs-lookup"><span data-stu-id="4e5cb-130">If Unicode is defined, the function call resolves to D3DXSaveTextureToFileW.</span></span> <span data-ttu-id="4e5cb-131">In caso contrario, la chiamata di funzione viene risolta in D3DXSaveTextureToFileA perché vengono utilizzate le stringhe ANSI.</span><span class="sxs-lookup"><span data-stu-id="4e5cb-131">Otherwise, the function call resolves to D3DXSaveTextureToFileA because ANSI strings are being used.</span></span>

<span data-ttu-id="4e5cb-132">Questa funzione gestisce la conversione da e verso formati di trama compressi.</span><span class="sxs-lookup"><span data-stu-id="4e5cb-132">This function handles conversion to and from compressed texture formats.</span></span>

<span data-ttu-id="4e5cb-133">Se il volume è non dinamico (a causa di un parametro Usage impostato su 0 alla creazione) e situato nella memoria video (il pool di memoria impostato su D3DPOOL \_ default), **D3DXSaveTextureToFile** avrà esito negativo perché D3DX non può bloccare i volumi non dinamici presenti nella memoria video.</span><span class="sxs-lookup"><span data-stu-id="4e5cb-133">If the volume is nondynamic (because of a usage parameter set to 0 at the creation) and located in video memory (the memory pool set to D3DPOOL\_DEFAULT), **D3DXSaveTextureToFile** will fail because D3DX cannot lock nondynamic volumes located in video memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e5cb-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4e5cb-134">Requirements</span></span>



| <span data-ttu-id="4e5cb-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e5cb-135">Requirement</span></span> | <span data-ttu-id="4e5cb-136">Valore</span><span class="sxs-lookup"><span data-stu-id="4e5cb-136">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4e5cb-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4e5cb-137">Header</span></span><br/>  | <dl> <span data-ttu-id="4e5cb-138"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e5cb-138"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="4e5cb-139">Libreria</span><span class="sxs-lookup"><span data-stu-id="4e5cb-139">Library</span></span><br/> | <dl> <span data-ttu-id="4e5cb-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4e5cb-140"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="4e5cb-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4e5cb-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e5cb-142">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="4e5cb-142">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="4e5cb-143">**D3DXSaveSurfaceToFile**</span><span class="sxs-lookup"><span data-stu-id="4e5cb-143">**D3DXSaveSurfaceToFile**</span></span>](d3dxsavesurfacetofile.md)
</dt> <dt>

[<span data-ttu-id="4e5cb-144">**D3DXSaveVolumeToFile**</span><span class="sxs-lookup"><span data-stu-id="4e5cb-144">**D3DXSaveVolumeToFile**</span></span>](d3dxsavevolumetofile.md)
</dt> </dl>

 

 
