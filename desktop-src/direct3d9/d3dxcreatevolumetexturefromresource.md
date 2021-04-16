---
description: Crea una trama del volume da una risorsa.
ms.assetid: 82a0b7aa-69fa-450d-b0d2-769f05fd75ea
title: Funzione D3DXCreateVolumeTextureFromResource (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTextureFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a5f0a0faf97f773c3174ced22ec7259091d6e07e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530907"
---
# <a name="d3dxcreatevolumetexturefromresource-function"></a><span data-ttu-id="6a4d1-103">D3DXCreateVolumeTextureFromResource (funzione)</span><span class="sxs-lookup"><span data-stu-id="6a4d1-103">D3DXCreateVolumeTextureFromResource function</span></span>

<span data-ttu-id="6a4d1-104">Crea una trama del volume da una risorsa.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-104">Creates a volume texture from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a4d1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6a4d1-105">Syntax</span></span>


```C++
HRESULT D3DXCreateVolumeTextureFromResource(
  _In_  LPDIRECT3DDEVICE9        pDevice,
  _In_  HMODULE                  hSrcModule,
  _In_  LPCTSTR                  pSrcResource,
  _Out_ LPDIRECT3DVOLUMETEXTURE9 *ppVolumeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="6a4d1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6a4d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a4d1-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a4d1-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a4d1-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="6a4d1-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="6a4d1-109">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo da associare alla trama del volume.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="6a4d1-110">*hSrcModule* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a4d1-110">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a4d1-111">Tipo: **[ **hmodule**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a4d1-111">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a4d1-112">Handle per il modulo in cui si trova la risorsa o **null** per il modulo associato all'immagine utilizzata dal sistema operativo per creare il processo corrente.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-112">Handle to the module where the resource is located, or **NULL** for the module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="6a4d1-113">*pSrcResource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a4d1-113">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a4d1-114">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a4d1-114">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a4d1-115">Puntatore a una stringa che specifica il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-115">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="6a4d1-116">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-116">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="6a4d1-117">In caso contrario, il tipo di dati String viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-117">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="6a4d1-118">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="6a4d1-119">*ppVolumeTexture* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6a4d1-119">*ppVolumeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a4d1-120">Tipo: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="6a4d1-120">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span></span>

<span data-ttu-id="6a4d1-121">Indirizzo di un puntatore a un'interfaccia [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) che rappresenta l'oggetto trama creato.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-121">Address of a pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a4d1-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6a4d1-122">Return value</span></span>

<span data-ttu-id="6a4d1-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6a4d1-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6a4d1-124">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-124">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6a4d1-125">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-125">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a4d1-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="6a4d1-126">Remarks</span></span>

<span data-ttu-id="6a4d1-127">L'impostazione del compilatore determina anche la versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-127">The compiler setting also determines the function version.</span></span> <span data-ttu-id="6a4d1-128">Se è definito Unicode, la chiamata di funzione viene risolta in D3DXCreateVolumeTextureFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-128">If Unicode is defined, the function call resolves to D3DXCreateVolumeTextureFromResourceW.</span></span> <span data-ttu-id="6a4d1-129">In caso contrario, la chiamata di funzione viene risolta in D3DXCreateVolumeTextureFromResourceA perché vengono utilizzate le stringhe ANSI.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-129">Otherwise, the function call resolves to D3DXCreateVolumeTextureFromResourceA because ANSI strings are being used.</span></span>

<span data-ttu-id="6a4d1-130">La funzione è equivalente a D3DXCreateVolumeTextureFromResourceEx (pDevice, hSrcModule, pSrcResource, D3DX \_ default, D3DX \_ default, D3DX \_ default, D3DX \_ default, 0, D3DFMT \_ Unknown, D3DPOOL \_ Managed, D3DX default \_ , D3DX \_ default, 0, **null**, **null**, ppVolumeTexture).</span><span class="sxs-lookup"><span data-stu-id="6a4d1-130">The function is equivalent to D3DXCreateVolumeTextureFromResourceEx(pDevice, hSrcModule, pSrcResource, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppVolumeTexture).</span></span>

<span data-ttu-id="6a4d1-131">La risorsa da caricare deve essere una risorsa definita dall'applicazione (RT \_ RCDATA).</span><span class="sxs-lookup"><span data-stu-id="6a4d1-131">The resource being loaded must be an application-defined resource (RT\_RCDATA).</span></span>

<span data-ttu-id="6a4d1-132">Questa funzione supporta i formati di file seguenti:. bmp,. DDS,. DIB,. HDR,. jpg,. PFM,. png,. ppm e. tga.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-132">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="6a4d1-133">Vedere [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="6a4d1-133">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="6a4d1-134">Si noti che una risorsa creata con questa funzione quando viene chiamata da un oggetto IDirect3DDevice9 verrà inserita nella classe di memoria indicata da D3DPOOL \_ gestito.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-134">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="6a4d1-135">Quando questo metodo viene chiamato da un oggetto IDirect3DDevice9Ex, la risorsa verrà inserita nella classe di memoria indicata da D3DPOOL \_ default.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-135">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="6a4d1-136">Il filtro viene applicato automaticamente a una trama creata utilizzando questo metodo.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-136">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="6a4d1-137">Il filtro è equivalente a D3DX Filter D3DX del filtro \_ \_ \| \_ \_ di retinazione nel [ \_ filtro D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="6a4d1-137">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6a4d1-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6a4d1-138">Requirements</span></span>



| <span data-ttu-id="6a4d1-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a4d1-139">Requirement</span></span> | <span data-ttu-id="6a4d1-140">Valore</span><span class="sxs-lookup"><span data-stu-id="6a4d1-140">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6a4d1-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6a4d1-141">Header</span></span><br/>  | <dl> <span data-ttu-id="6a4d1-142"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a4d1-142"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="6a4d1-143">Libreria</span><span class="sxs-lookup"><span data-stu-id="6a4d1-143">Library</span></span><br/> | <dl> <span data-ttu-id="6a4d1-144"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6a4d1-144"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="6a4d1-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6a4d1-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a4d1-146">**D3DXCreateVolumeTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="6a4d1-146">**D3DXCreateVolumeTextureFromFile**</span></span>](d3dxcreatevolumetexturefromfile.md)
</dt> <dt>

[<span data-ttu-id="6a4d1-147">**D3DXCreateVolumeTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="6a4d1-147">**D3DXCreateVolumeTextureFromFileEx**</span></span>](d3dxcreatevolumetexturefromfileex.md)
</dt> <dt>

[<span data-ttu-id="6a4d1-148">**D3DXCreateVolumeTextureFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="6a4d1-148">**D3DXCreateVolumeTextureFromFileInMemory**</span></span>](d3dxcreatevolumetexturefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="6a4d1-149">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="6a4d1-149">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span></span>](d3dxcreatevolumetexturefromfileinmemoryex.md)
</dt> <dt>

[<span data-ttu-id="6a4d1-150">**D3DXCreateVolumeTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="6a4d1-150">**D3DXCreateVolumeTextureFromResourceEx**</span></span>](d3dxcreatevolumetexturefromresourceex.md)
</dt> <dt>

[<span data-ttu-id="6a4d1-151">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="6a4d1-151">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
