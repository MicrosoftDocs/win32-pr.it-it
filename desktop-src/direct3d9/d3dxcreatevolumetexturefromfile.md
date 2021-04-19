---
description: Crea una trama del volume da un file.
ms.assetid: e68ac4bb-a89a-41a1-b2ba-40a1ac519e3d
title: Funzione D3DXCreateVolumeTextureFromFile (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTextureFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 51ee51f1aee7a69fbd86d7f9bb2ded894dde9ead
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322720"
---
# <a name="d3dxcreatevolumetexturefromfile-function"></a><span data-ttu-id="60991-103">D3DXCreateVolumeTextureFromFile (funzione)</span><span class="sxs-lookup"><span data-stu-id="60991-103">D3DXCreateVolumeTextureFromFile function</span></span>

<span data-ttu-id="60991-104">Crea una trama del volume da un file.</span><span class="sxs-lookup"><span data-stu-id="60991-104">Creates a volume texture from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="60991-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="60991-105">Syntax</span></span>


```C++
HRESULT D3DXCreateVolumeTextureFromFile(
  _In_  LPDIRECT3DDEVICE9        pDevice,
  _In_  LPCTSTR                  pSrcFile,
  _Out_ LPDIRECT3DVOLUMETEXTURE9 *ppVolumeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="60991-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="60991-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60991-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="60991-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60991-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="60991-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="60991-109">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo da associare alla trama del volume.</span><span class="sxs-lookup"><span data-stu-id="60991-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="60991-110">*pSrcFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="60991-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60991-111">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="60991-111">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="60991-112">Puntatore a una stringa che specifica il nome del file.</span><span class="sxs-lookup"><span data-stu-id="60991-112">Pointer to a string that specifies the file name.</span></span> <span data-ttu-id="60991-113">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="60991-113">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="60991-114">In caso contrario, il tipo di dati String viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="60991-114">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="60991-115">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="60991-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="60991-116">*ppVolumeTexture* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="60991-116">*ppVolumeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60991-117">Tipo: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="60991-117">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span></span>

<span data-ttu-id="60991-118">Indirizzo di un puntatore a un'interfaccia [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) che rappresenta l'oggetto trama creato.</span><span class="sxs-lookup"><span data-stu-id="60991-118">Address of a pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60991-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="60991-119">Return value</span></span>

<span data-ttu-id="60991-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="60991-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="60991-121">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="60991-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="60991-122">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="60991-122">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="60991-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="60991-123">Remarks</span></span>

<span data-ttu-id="60991-124">L'impostazione del compilatore determina anche la versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="60991-124">The compiler setting also determines the function version.</span></span> <span data-ttu-id="60991-125">Se è definito Unicode, la chiamata di funzione viene risolta in D3DXCreateVolumeTextureFromFileW.</span><span class="sxs-lookup"><span data-stu-id="60991-125">If Unicode is defined, the function call resolves to D3DXCreateVolumeTextureFromFileW.</span></span> <span data-ttu-id="60991-126">In caso contrario, la chiamata di funzione viene risolta in D3DXCreateVolumeTextureFromFileA perché vengono utilizzate le stringhe ANSI.</span><span class="sxs-lookup"><span data-stu-id="60991-126">Otherwise, the function call resolves to D3DXCreateVolumeTextureFromFileA because ANSI strings are being used.</span></span>

<span data-ttu-id="60991-127">La funzione è equivalente a D3DXCreateVolumeTextureFromFileEx (pDevice, pSrcFile, D3DX \_ default, D3DX \_ default, D3DX \_ default, D3DX \_ default, 0, D3DFMT \_ Unknown, D3DPOOL \_ Managed, D3DX \_ default, D3DX \_ default, 0, **null**, **null**, ppVolumeTexture).</span><span class="sxs-lookup"><span data-stu-id="60991-127">The function is equivalent to D3DXCreateVolumeTextureFromFileEx(pDevice, pSrcFile, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppVolumeTexture).</span></span>

<span data-ttu-id="60991-128">Questa funzione supporta i formati di file seguenti:. bmp,. DDS,. DIB,. HDR,. jpg,. PFM,. png,. ppm e. tga.</span><span class="sxs-lookup"><span data-stu-id="60991-128">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="60991-129">Vedere [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="60991-129">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="60991-130">Le trame mipmap dispongono automaticamente di ogni livello riempito con la trama caricata.</span><span class="sxs-lookup"><span data-stu-id="60991-130">Mipmapped textures automatically have each level filled with the loaded texture.</span></span>

<span data-ttu-id="60991-131">Quando si caricano immagini in trame mipmap, alcuni dispositivi non sono in grado di passare a un'immagine 1x1 e questa funzione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="60991-131">When loading images into mipmapped textures, some devices are unable to go to a 1x1 image and this function will fail.</span></span> <span data-ttu-id="60991-132">In tal caso, è necessario caricare le immagini manualmente.</span><span class="sxs-lookup"><span data-stu-id="60991-132">If this happens, then the images need to be loaded manually.</span></span>

<span data-ttu-id="60991-133">Si noti che una risorsa creata con questa funzione quando viene chiamata da un oggetto IDirect3DDevice9 verrà inserita nella classe di memoria indicata da D3DPOOL \_ gestito.</span><span class="sxs-lookup"><span data-stu-id="60991-133">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="60991-134">Quando questo metodo viene chiamato da un oggetto IDirect3DDevice9Ex, la risorsa verrà inserita nella classe di memoria indicata da D3DPOOL \_ default.</span><span class="sxs-lookup"><span data-stu-id="60991-134">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="60991-135">Il filtro viene applicato automaticamente a una trama creata utilizzando questo metodo.</span><span class="sxs-lookup"><span data-stu-id="60991-135">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="60991-136">Il filtro è equivalente a D3DX Filter D3DX del filtro \_ \_ \| \_ \_ di retinazione nel [ \_ filtro D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="60991-136">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="60991-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="60991-137">Requirements</span></span>



| <span data-ttu-id="60991-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="60991-138">Requirement</span></span> | <span data-ttu-id="60991-139">Valore</span><span class="sxs-lookup"><span data-stu-id="60991-139">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="60991-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="60991-140">Header</span></span><br/>  | <dl> <span data-ttu-id="60991-141"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="60991-141"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="60991-142">Libreria</span><span class="sxs-lookup"><span data-stu-id="60991-142">Library</span></span><br/> | <dl> <span data-ttu-id="60991-143"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="60991-143"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="60991-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="60991-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60991-145">**D3DXCreateVolumeTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="60991-145">**D3DXCreateVolumeTextureFromFileEx**</span></span>](d3dxcreatevolumetexturefromfileex.md)
</dt> <dt>

[<span data-ttu-id="60991-146">**D3DXCreateVolumeTextureFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="60991-146">**D3DXCreateVolumeTextureFromFileInMemory**</span></span>](d3dxcreatevolumetexturefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="60991-147">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="60991-147">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span></span>](d3dxcreatevolumetexturefromfileinmemoryex.md)
</dt> <dt>

[<span data-ttu-id="60991-148">**D3DXCreateVolumeTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="60991-148">**D3DXCreateVolumeTextureFromResource**</span></span>](d3dxcreatevolumetexturefromresource.md)
</dt> <dt>

[<span data-ttu-id="60991-149">**D3DXCreateVolumeTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="60991-149">**D3DXCreateVolumeTextureFromResourceEx**</span></span>](d3dxcreatevolumetexturefromresourceex.md)
</dt> <dt>

[<span data-ttu-id="60991-150">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="60991-150">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
