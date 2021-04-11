---
description: Salva un volume in un buffer. Il metodo crea un buffer ID3DXBuffer per archiviare i dati e restituisce tale oggetto.
ms.assetid: 4887ff1f-7904-4764-b284-b2c8e037f806
title: Funzione D3DXSaveVolumeToFileInMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveVolumeToFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7daaa41e0cc87ea03a0aedc5fc2f7ca96653329f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235001"
---
# <a name="d3dxsavevolumetofileinmemory-function"></a><span data-ttu-id="2b958-104">D3DXSaveVolumeToFileInMemory (funzione)</span><span class="sxs-lookup"><span data-stu-id="2b958-104">D3DXSaveVolumeToFileInMemory function</span></span>

<span data-ttu-id="2b958-105">Salva un volume in un buffer.</span><span class="sxs-lookup"><span data-stu-id="2b958-105">Saves a volume to a buffer.</span></span> <span data-ttu-id="2b958-106">Il metodo crea un buffer [**ID3DXBuffer**](id3dxbuffer.md) per archiviare i dati e restituisce tale oggetto.</span><span class="sxs-lookup"><span data-stu-id="2b958-106">The method creates an [**ID3DXBuffer**](id3dxbuffer.md) buffer to store the data, and returns that object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b958-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2b958-107">Syntax</span></span>


```C++
HRESULT D3DXSaveVolumeToFileInMemory(
  _Out_       LPD3DXBUFFER         *ppDestBuf,
  _In_        D3DXIMAGE_FILEFORMAT DestFormat,
  _In_        LPDIRECT3DVOLUME9    pSrcVolume,
  _In_  const PALETTEENTRY         *pSrcPalette,
  _In_  const D3DBOX               *pSrcBox
);
```



## <a name="parameters"></a><span data-ttu-id="2b958-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2b958-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b958-109">*ppDestBuf* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2b958-109">*ppDestBuf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b958-110">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="2b958-110">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="2b958-111">Indirizzo di un puntatore a un buffer [**ID3DXBuffer**](id3dxbuffer.md) che archivia l'immagine.</span><span class="sxs-lookup"><span data-stu-id="2b958-111">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) buffer that will store the image.</span></span>

</dd> <dt>

<span data-ttu-id="2b958-112">*DestFormat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2b958-112">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b958-113">Tipo: **[ **D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="2b958-113">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

<span data-ttu-id="2b958-114">[**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md) che specifica il formato di file da utilizzare per il salvataggio.</span><span class="sxs-lookup"><span data-stu-id="2b958-114">[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md) specifying the file format to use when saving.</span></span> <span data-ttu-id="2b958-115">Questa funzione supporta il salvataggio in tutti i formati **D3DXIMAGE \_ FileFormat** ad eccezione di Portable Pixmap (. ppm) e targa/Truevision Graphics Adapter (. tga).</span><span class="sxs-lookup"><span data-stu-id="2b958-115">This function supports saving to all **D3DXIMAGE\_FILEFORMAT** formats except Portable Pixmap (.ppm) and Targa/Truevision Graphics Adapter (.tga).</span></span>

</dd> <dt>

<span data-ttu-id="2b958-116">*pSrcVolume* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2b958-116">*pSrcVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b958-117">Tipo: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="2b958-117">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="2b958-118">Puntatore all'interfaccia [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) che contiene l'immagine da salvare.</span><span class="sxs-lookup"><span data-stu-id="2b958-118">Pointer to [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface containing the image to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="2b958-119">*pSrcPalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2b958-119">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b958-120">Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="2b958-120">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="2b958-121">Puntatore a una struttura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) contenente una tavolozza di colori 256.</span><span class="sxs-lookup"><span data-stu-id="2b958-121">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure containing a palette of 256 colors.</span></span> <span data-ttu-id="2b958-122">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="2b958-122">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2b958-123">*pSrcBox* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2b958-123">*pSrcBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b958-124">Tipo: **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="2b958-124">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="2b958-125">Puntatore a una struttura [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="2b958-125">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="2b958-126">Specifica la casella di origine.</span><span class="sxs-lookup"><span data-stu-id="2b958-126">Specifies the source box.</span></span> <span data-ttu-id="2b958-127">Impostare questo parametro su **null** per specificare l'intero volume.</span><span class="sxs-lookup"><span data-stu-id="2b958-127">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b958-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2b958-128">Return value</span></span>

<span data-ttu-id="2b958-129">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2b958-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2b958-130">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2b958-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2b958-131">Se la funzione ha esito negativo, il valore restituito può essere il seguente: D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="2b958-131">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="2b958-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2b958-132">Requirements</span></span>



| <span data-ttu-id="2b958-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b958-133">Requirement</span></span> | <span data-ttu-id="2b958-134">Valore</span><span class="sxs-lookup"><span data-stu-id="2b958-134">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2b958-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2b958-135">Header</span></span><br/>  | <dl> <span data-ttu-id="2b958-136"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b958-136"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="2b958-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="2b958-137">Library</span></span><br/> | <dl> <span data-ttu-id="2b958-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2b958-138"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="2b958-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2b958-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b958-140">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="2b958-140">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="2b958-141">**D3DXSaveVolumeToFile**</span><span class="sxs-lookup"><span data-stu-id="2b958-141">**D3DXSaveVolumeToFile**</span></span>](d3dxsavevolumetofile.md)
</dt> </dl>

 

 
