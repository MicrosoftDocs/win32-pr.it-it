---
description: Crea una trama del cubo da un file.
ms.assetid: 7ff3b051-568c-4c77-b8a6-b626ba156eb1
title: Funzione D3DXCreateCubeTextureFromFile (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2071a1d1e16e769d1a0623138e24c2e0fbab85e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322910"
---
# <a name="d3dxcreatecubetexturefromfile-function"></a><span data-ttu-id="da219-103">D3DXCreateCubeTextureFromFile (funzione)</span><span class="sxs-lookup"><span data-stu-id="da219-103">D3DXCreateCubeTextureFromFile function</span></span>

<span data-ttu-id="da219-104">Crea una trama del cubo da un file.</span><span class="sxs-lookup"><span data-stu-id="da219-104">Creates a cube texture from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="da219-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="da219-105">Syntax</span></span>


```C++
HRESULT D3DXCreateCubeTextureFromFile(
  _In_  LPDIRECT3DDEVICE9      pDevice,
  _In_  LPCTSTR                pSrcFile,
  _Out_ LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="da219-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="da219-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da219-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da219-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da219-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="da219-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="da219-109">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo da associare alla trama del cubo.</span><span class="sxs-lookup"><span data-stu-id="da219-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="da219-110">*pSrcFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da219-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da219-111">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="da219-111">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="da219-112">Puntatore a una stringa che specifica il nome del file.</span><span class="sxs-lookup"><span data-stu-id="da219-112">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="da219-113">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="da219-113">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="da219-114">In caso contrario, il tipo di dati String viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="da219-114">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="da219-115">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="da219-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="da219-116">*ppCubeTexture* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="da219-116">*ppCubeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="da219-117">Tipo: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="da219-117">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span></span>

<span data-ttu-id="da219-118">Indirizzo di un puntatore a un'interfaccia [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) , che rappresenta l'oggetto trama del cubo creato.</span><span class="sxs-lookup"><span data-stu-id="da219-118">Address of a pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the created cube texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da219-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="da219-119">Return value</span></span>

<span data-ttu-id="da219-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="da219-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="da219-121">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="da219-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="da219-122">Se la funzione ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR INVALIDDATA \_ , E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="da219-122">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="da219-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="da219-123">Remarks</span></span>

<span data-ttu-id="da219-124">L'impostazione del compilatore determina anche la versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="da219-124">The compiler setting also determines the function version.</span></span> <span data-ttu-id="da219-125">Se è definito Unicode, la chiamata di funzione viene risolta in **D3DXCreateCubeTextureFromFileW**.</span><span class="sxs-lookup"><span data-stu-id="da219-125">If Unicode is defined, the function call resolves to **D3DXCreateCubeTextureFromFileW**.</span></span> <span data-ttu-id="da219-126">In caso contrario, la chiamata di funzione viene risolta in **D3DXCreateCubeTextureFromFileA** perché vengono utilizzate le stringhe ANSI.</span><span class="sxs-lookup"><span data-stu-id="da219-126">Otherwise, the function call resolves to **D3DXCreateCubeTextureFromFileA** because ANSI strings are being used.</span></span>

<span data-ttu-id="da219-127">La funzione è equivalente a D3DXCreateCubeTextureFromFileEx (pDevice, pSrcFile, D3DX \_ default, D3DX \_ default, 0, D3DFMT \_ Unknown, D3DPOOL \_ Managed, D3DX \_ default, D3DX \_ default, 0, **null**, **null**, ppCubeTexture).</span><span class="sxs-lookup"><span data-stu-id="da219-127">The function is equivalent to D3DXCreateCubeTextureFromFileEx(pDevice, pSrcFile, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppCubeTexture).</span></span>

<span data-ttu-id="da219-128">Questa funzione supporta i formati di file seguenti:. bmp,. DDS,. DIB,. HDR,. jpg,. PFM,. png,. ppm e. tga.</span><span class="sxs-lookup"><span data-stu-id="da219-128">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="da219-129">Vedere [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="da219-129">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="da219-130">Si noti che una risorsa creata con questa funzione quando viene chiamata da un oggetto IDirect3DDevice9 verrà inserita nella classe di memoria indicata da D3DPOOL \_ gestito.</span><span class="sxs-lookup"><span data-stu-id="da219-130">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="da219-131">Quando questo metodo viene chiamato da un oggetto IDirect3DDevice9Ex, la risorsa verrà inserita nella classe di memoria indicata da D3DPOOL \_ default.</span><span class="sxs-lookup"><span data-stu-id="da219-131">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="da219-132">Il filtro viene applicato automaticamente a una trama creata utilizzando questo metodo.</span><span class="sxs-lookup"><span data-stu-id="da219-132">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="da219-133">Il filtro è equivalente a D3DX Filter D3DX del filtro \_ \_ \| \_ \_ di retinazione nel [ \_ filtro D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="da219-133">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

<span data-ttu-id="da219-134">**D3DXCreateCubeTextureFromFile** usa il formato di file DirectDraw Surface (DDS).</span><span class="sxs-lookup"><span data-stu-id="da219-134">**D3DXCreateCubeTextureFromFile** uses the DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="da219-135">L'editor di trame DirectX (Dxtex.exe) consente di generare una mappa del cubo da altri formati di file e di salvarli nel formato di file DDS.</span><span class="sxs-lookup"><span data-stu-id="da219-135">The DirectX Texture Editor (Dxtex.exe) enables you to generate a cube map from other file formats and save it in the DDS file format.</span></span> <span data-ttu-id="da219-136">È possibile ottenere Dxtex.exe e ottenere informazioni su di esso da DirectX SDK.</span><span class="sxs-lookup"><span data-stu-id="da219-136">You can get Dxtex.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="da219-137">Per informazioni su DirectX SDK, vedere [dove è DirectX SDK?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="da219-137">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="da219-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="da219-138">Requirements</span></span>



| <span data-ttu-id="da219-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="da219-139">Requirement</span></span> | <span data-ttu-id="da219-140">Valore</span><span class="sxs-lookup"><span data-stu-id="da219-140">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="da219-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="da219-141">Header</span></span><br/>  | <dl> <span data-ttu-id="da219-142"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="da219-142"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="da219-143">Libreria</span><span class="sxs-lookup"><span data-stu-id="da219-143">Library</span></span><br/> | <dl> <span data-ttu-id="da219-144"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="da219-144"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="da219-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="da219-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da219-146">**D3DXCreateCubeTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="da219-146">**D3DXCreateCubeTextureFromFileEx**</span></span>](d3dxcreatecubetexturefromfileex.md)
</dt> <dt>

[<span data-ttu-id="da219-147">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="da219-147">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
