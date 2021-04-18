---
description: Salva una superficie in un file di immagine.
ms.assetid: 6320e5ed-e43d-43bf-a746-5478df42941d
title: Funzione D3DXSaveSurfaceToFileInMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveSurfaceToFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8e8bbdd447b7154e150b3469a4b12180252ed516
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322599"
---
# <a name="d3dxsavesurfacetofileinmemory-function"></a><span data-ttu-id="8df3d-103">D3DXSaveSurfaceToFileInMemory (funzione)</span><span class="sxs-lookup"><span data-stu-id="8df3d-103">D3DXSaveSurfaceToFileInMemory function</span></span>

<span data-ttu-id="8df3d-104">Salva una superficie in un file di immagine.</span><span class="sxs-lookup"><span data-stu-id="8df3d-104">Saves a surface to an image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="8df3d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8df3d-105">Syntax</span></span>


```C++
HRESULT D3DXSaveSurfaceToFileInMemory(
  _Out_       LPD3DXBUFFER         *ppDestBuf,
  _In_        D3DXIMAGE_FILEFORMAT DestFormat,
  _In_        LPDIRECT3DSURFACE9   pSrcSurface,
  _In_  const PALETTEENTRY         *pSrcPalette,
  _In_  const RECT                 *pSrcRect
);
```



## <a name="parameters"></a><span data-ttu-id="8df3d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8df3d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8df3d-107">*ppDestBuf* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8df3d-107">*ppDestBuf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8df3d-108">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="8df3d-108">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="8df3d-109">Indirizzo di un puntatore a un [**ID3DXBuffer**](id3dxbuffer.md) in cui viene archiviata l'immagine.</span><span class="sxs-lookup"><span data-stu-id="8df3d-109">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) that will store the image.</span></span>

</dd> <dt>

<span data-ttu-id="8df3d-110">*DestFormat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8df3d-110">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8df3d-111">Tipo: **[ **D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="8df3d-111">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

<span data-ttu-id="8df3d-112">[**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md) che specifica il formato di file da utilizzare per il salvataggio.</span><span class="sxs-lookup"><span data-stu-id="8df3d-112">[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md) specifying the file format to use when saving.</span></span> <span data-ttu-id="8df3d-113">Questa funzione supporta il salvataggio in tutti i formati **D3DXIMAGE \_ FileFormat** ad eccezione di Portable Pixmap (. ppm) e targa/Truevision Graphics Adapter (. tga).</span><span class="sxs-lookup"><span data-stu-id="8df3d-113">This function supports saving to all **D3DXIMAGE\_FILEFORMAT** formats except Portable Pixmap (.ppm) and Targa/Truevision Graphics Adapter (.tga).</span></span>

</dd> <dt>

<span data-ttu-id="8df3d-114">*pSrcSurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8df3d-114">*pSrcSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8df3d-115">Tipo: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="8df3d-115">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="8df3d-116">Puntatore all'interfaccia [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) che contiene l'immagine da salvare.</span><span class="sxs-lookup"><span data-stu-id="8df3d-116">Pointer to [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface containing the image to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="8df3d-117">*pSrcPalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8df3d-117">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8df3d-118">Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="8df3d-118">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="8df3d-119">Puntatore a una struttura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) contenente una tavolozza di colori 256.</span><span class="sxs-lookup"><span data-stu-id="8df3d-119">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure containing a palette of 256 colors.</span></span> <span data-ttu-id="8df3d-120">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="8df3d-120">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8df3d-121">*pSrcRect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8df3d-121">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8df3d-122">Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="8df3d-122">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="8df3d-123">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8df3d-123">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="8df3d-124">Specifica il rettangolo di origine.</span><span class="sxs-lookup"><span data-stu-id="8df3d-124">Specifies the source rectangle.</span></span> <span data-ttu-id="8df3d-125">Impostare questo parametro su **null** per specificare l'intera immagine.</span><span class="sxs-lookup"><span data-stu-id="8df3d-125">Set this parameter to **NULL** to specify the entire image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8df3d-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8df3d-126">Return value</span></span>

<span data-ttu-id="8df3d-127">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8df3d-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8df3d-128">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8df3d-128">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8df3d-129">Se la funzione ha esito negativo, il valore restituito può essere il seguente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="8df3d-129">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="8df3d-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="8df3d-130">Remarks</span></span>

<span data-ttu-id="8df3d-131">Questa funzione gestisce la conversione da e verso formati di trama compressi.</span><span class="sxs-lookup"><span data-stu-id="8df3d-131">This function handles conversion to and from compressed texture formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="8df3d-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8df3d-132">Requirements</span></span>



| <span data-ttu-id="8df3d-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="8df3d-133">Requirement</span></span> | <span data-ttu-id="8df3d-134">Valore</span><span class="sxs-lookup"><span data-stu-id="8df3d-134">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8df3d-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8df3d-135">Header</span></span><br/>  | <dl> <span data-ttu-id="8df3d-136"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="8df3d-136"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="8df3d-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="8df3d-137">Library</span></span><br/> | <dl> <span data-ttu-id="8df3d-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8df3d-138"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="8df3d-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8df3d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8df3d-140">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="8df3d-140">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="8df3d-141">**D3DXSaveVolumeToFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="8df3d-141">**D3DXSaveVolumeToFileInMemory**</span></span>](d3dxsavevolumetofileinmemory.md)
</dt> </dl>

 

 
