---
description: Salva una trama in un file di immagine.
ms.assetid: 8dcfd58a-ae1e-43c3-8ff1-94e3fa398b0f
title: Funzione D3DXSaveTextureToFileInMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveTextureToFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c58da1663abc5295e8ce17c500bd46d6c365a2d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132330"
---
# <a name="d3dxsavetexturetofileinmemory-function"></a><span data-ttu-id="fe69b-103">D3DXSaveTextureToFileInMemory (funzione)</span><span class="sxs-lookup"><span data-stu-id="fe69b-103">D3DXSaveTextureToFileInMemory function</span></span>

<span data-ttu-id="fe69b-104">Salva una trama in un file di immagine.</span><span class="sxs-lookup"><span data-stu-id="fe69b-104">Saves a texture to an image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe69b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fe69b-105">Syntax</span></span>


```C++
HRESULT D3DXSaveTextureToFileInMemory(
  _Out_       LPD3DXBUFFER           *ppDestBuf,
  _In_        D3DXIMAGE_FILEFORMAT   DestFormat,
  _In_        LPDIRECT3DBASETEXTURE9 pSrcTexture,
  _In_  const PALETTEENTRY           *pSrcPalette
);
```



## <a name="parameters"></a><span data-ttu-id="fe69b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fe69b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe69b-107">*ppDestBuf* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fe69b-107">*ppDestBuf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe69b-108">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="fe69b-108">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="fe69b-109">Indirizzo di un puntatore a un [**ID3DXBuffer**](id3dxbuffer.md) in cui viene archiviata l'immagine.</span><span class="sxs-lookup"><span data-stu-id="fe69b-109">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) that will store the image.</span></span>

</dd> <dt>

<span data-ttu-id="fe69b-110">*DestFormat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe69b-110">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe69b-111">Tipo: **[ **D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="fe69b-111">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

<span data-ttu-id="fe69b-112">[**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md) che specifica il formato di file da utilizzare per il salvataggio.</span><span class="sxs-lookup"><span data-stu-id="fe69b-112">[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md) specifying the file format to use when saving.</span></span> <span data-ttu-id="fe69b-113">Questa funzione supporta il salvataggio in tutti i formati **D3DXIMAGE \_ FileFormat** ad eccezione di Portable Pixmap (. ppm) e targa/Truevision Graphics Adapter (. tga).</span><span class="sxs-lookup"><span data-stu-id="fe69b-113">This function supports saving to all **D3DXIMAGE\_FILEFORMAT** formats except Portable Pixmap (.ppm) and Targa/Truevision Graphics Adapter (.tga).</span></span>

</dd> <dt>

<span data-ttu-id="fe69b-114">*pSrcTexture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe69b-114">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe69b-115">Tipo: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span><span class="sxs-lookup"><span data-stu-id="fe69b-115">Type: **[**LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span></span>

<span data-ttu-id="fe69b-116">Puntatore all'interfaccia [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) che contiene l'immagine da salvare.</span><span class="sxs-lookup"><span data-stu-id="fe69b-116">Pointer to [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) interface containing the image to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="fe69b-117">*pSrcPalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe69b-117">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe69b-118">Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="fe69b-118">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="fe69b-119">Puntatore a una struttura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) contenente una tavolozza di colori 256.</span><span class="sxs-lookup"><span data-stu-id="fe69b-119">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure containing a palette of 256 colors.</span></span> <span data-ttu-id="fe69b-120">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="fe69b-120">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe69b-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fe69b-121">Return value</span></span>

<span data-ttu-id="fe69b-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fe69b-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fe69b-123">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fe69b-123">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fe69b-124">Se la funzione ha esito negativo, il valore restituito può essere il seguente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="fe69b-124">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe69b-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="fe69b-125">Remarks</span></span>

<span data-ttu-id="fe69b-126">Questa funzione gestisce la conversione da e verso formati di trama compressi.</span><span class="sxs-lookup"><span data-stu-id="fe69b-126">This function handles conversion to and from compressed texture formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe69b-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fe69b-127">Requirements</span></span>



| <span data-ttu-id="fe69b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe69b-128">Requirement</span></span> | <span data-ttu-id="fe69b-129">Valore</span><span class="sxs-lookup"><span data-stu-id="fe69b-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fe69b-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fe69b-130">Header</span></span><br/>  | <dl> <span data-ttu-id="fe69b-131"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe69b-131"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="fe69b-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="fe69b-132">Library</span></span><br/> | <dl> <span data-ttu-id="fe69b-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe69b-133"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="fe69b-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fe69b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe69b-135">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="fe69b-135">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="fe69b-136">**D3DXSaveSurfaceToFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="fe69b-136">**D3DXSaveSurfaceToFileInMemory**</span></span>](d3dxsavesurfacetofileinmemory.md)
</dt> <dt>

[<span data-ttu-id="fe69b-137">**D3DXSaveVolumeToFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="fe69b-137">**D3DXSaveVolumeToFileInMemory**</span></span>](d3dxsavevolumetofileinmemory.md)
</dt> </dl>

 

 
