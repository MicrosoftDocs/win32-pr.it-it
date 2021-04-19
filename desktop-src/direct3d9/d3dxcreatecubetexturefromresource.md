---
description: Crea una trama del cubo da una risorsa.
ms.assetid: 9153944a-af8b-4365-9e91-fc1136a84caa
title: Funzione D3DXCreateCubeTextureFromResource (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c0bd65799bada2df8a3c9e0b113db3c911a53536
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322906"
---
# <a name="d3dxcreatecubetexturefromresource-function"></a><span data-ttu-id="e3d8f-103">D3DXCreateCubeTextureFromResource (funzione)</span><span class="sxs-lookup"><span data-stu-id="e3d8f-103">D3DXCreateCubeTextureFromResource function</span></span>

<span data-ttu-id="e3d8f-104">Crea una trama del cubo da una risorsa.</span><span class="sxs-lookup"><span data-stu-id="e3d8f-104">Creates a cube texture from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3d8f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e3d8f-105">Syntax</span></span>


```C++
HRESULT D3DXCreateCubeTextureFromResource(
  _In_  LPDIRECT3DDEVICE9      pDevice,
  _In_  HMODULE                hSrcModule,
  _In_  LPCTSTR                pSrcResource,
  _Out_ LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="e3d8f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e3d8f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3d8f-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3d8f-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3d8f-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="e3d8f-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="e3d8f-109">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo da associare alla trama del cubo.</span><span class="sxs-lookup"><span data-stu-id="e3d8f-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="e3d8f-110">*hSrcModule* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3d8f-110">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3d8f-111">Tipo: **[ **hmodule**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e3d8f-111">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e3d8f-112">Handle per il modulo in cui si trova la risorsa o **null** per il modulo associato all'immagine utilizzata dal sistema operativo per creare il processo corrente.</span><span class="sxs-lookup"><span data-stu-id="e3d8f-112">Handle to the module where the resource is located, or **NULL** for the module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="e3d8f-113">*pSrcResource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3d8f-113">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3d8f-114">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e3d8f-114">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e3d8f-115">Puntatore a una stringa che specifica il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="e3d8f-115">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="e3d8f-116">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="e3d8f-116">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="e3d8f-117">In caso contrario, il tipo di dati String viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="e3d8f-117">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="e3d8f-118">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="e3d8f-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="e3d8f-119">*ppCubeTexture* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e3d8f-119">*ppCubeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3d8f-120">Tipo: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="e3d8f-120">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span></span>

<span data-ttu-id="e3d8f-121">Indirizzo di un puntatore a un'interfaccia [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) , che rappresenta l'oggetto trama del cubo creato.</span><span class="sxs-lookup"><span data-stu-id="e3d8f-121">Address of a pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the created cube texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3d8f-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e3d8f-122">Return value</span></span>

<span data-ttu-id="e3d8f-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e3d8f-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e3d8f-124">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e3d8f-124">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e3d8f-125">Se la funzione ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR INVALIDDATA \_ , E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="e3d8f-125">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3d8f-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="e3d8f-126">Remarks</span></span>

<span data-ttu-id="e3d8f-127">L'impostazione del compilatore determina la versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="e3d8f-127">The compiler setting determines the function version.</span></span> <span data-ttu-id="e3d8f-128">Se è definito Unicode, la chiamata di funzione viene risolta in **D3DXCreateCubeTextureFromResourceW**.</span><span class="sxs-lookup"><span data-stu-id="e3d8f-128">If Unicode is defined, the function call resolves to **D3DXCreateCubeTextureFromResourceW**.</span></span> <span data-ttu-id="e3d8f-129">In caso contrario, la chiamata di funzione viene risolta in **D3DXCreateCubeTextureFromResourceA** perché vengono utilizzate le stringhe ANSI.</span><span class="sxs-lookup"><span data-stu-id="e3d8f-129">Otherwise, the function call resolves to **D3DXCreateCubeTextureFromResourceA** because ANSI strings are being used.</span></span>

<span data-ttu-id="e3d8f-130">La funzione è equivalente a D3DXCreateCubeTextureFromResourceEx (pDevice, hSrcModule, pSrcResource, D3DX \_ default, D3DX \_ default, 0, D3DFMT \_ Unknown, D3DPOOL \_ Managed, D3DX \_ default, D3DX \_ default, 0, **null**, **null**, ppCubeTexture).</span><span class="sxs-lookup"><span data-stu-id="e3d8f-130">The function is equivalent to D3DXCreateCubeTextureFromResourceEx(pDevice, hSrcModule, pSrcResource, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppCubeTexture).</span></span>

<span data-ttu-id="e3d8f-131">Questa funzione supporta i formati di file seguenti:. bmp,. DDS,. DIB,. HDR,. jpg,. PFM,. png,. ppm e. tga.</span><span class="sxs-lookup"><span data-stu-id="e3d8f-131">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="e3d8f-132">Vedere [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="e3d8f-132">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="e3d8f-133">Si noti che una risorsa creata con questa funzione quando viene chiamata da un oggetto IDirect3DDevice9 verrà inserita nella classe di memoria indicata da D3DPOOL \_ gestito.</span><span class="sxs-lookup"><span data-stu-id="e3d8f-133">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="e3d8f-134">Quando questo metodo viene chiamato da un oggetto IDirect3DDevice9Ex, la risorsa verrà inserita nella classe di memoria indicata da D3DPOOL \_ default.</span><span class="sxs-lookup"><span data-stu-id="e3d8f-134">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="e3d8f-135">Il filtro viene applicato automaticamente a una trama creata utilizzando questo metodo.</span><span class="sxs-lookup"><span data-stu-id="e3d8f-135">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="e3d8f-136">Il filtro è equivalente a D3DX Filter D3DX del filtro \_ \_ \| \_ \_ di retinazione nel [ \_ filtro D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="e3d8f-136">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

<span data-ttu-id="e3d8f-137">**D3DXCreateCubeTextureFromResource** usa il formato di file DirectDraw Surface (DDS).</span><span class="sxs-lookup"><span data-stu-id="e3d8f-137">**D3DXCreateCubeTextureFromResource** uses the DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="e3d8f-138">L'editor di trame DirectX (Dxtex.exe) consente di generare una mappa del cubo da altri formati di file e di salvarli nel formato di file DDS.</span><span class="sxs-lookup"><span data-stu-id="e3d8f-138">The DirectX Texture Editor (Dxtex.exe) enables you to generate a cube map from other file formats and save it in the DDS file format.</span></span> <span data-ttu-id="e3d8f-139">È possibile ottenere Dxtex.exe e ottenere informazioni su di esso da DirectX SDK.</span><span class="sxs-lookup"><span data-stu-id="e3d8f-139">You can get Dxtex.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="e3d8f-140">Per informazioni su DirectX SDK, vedere [dove è DirectX SDK?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="e3d8f-140">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e3d8f-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e3d8f-141">Requirements</span></span>



| <span data-ttu-id="e3d8f-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3d8f-142">Requirement</span></span> | <span data-ttu-id="e3d8f-143">Valore</span><span class="sxs-lookup"><span data-stu-id="e3d8f-143">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e3d8f-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e3d8f-144">Header</span></span><br/>  | <dl> <span data-ttu-id="e3d8f-145"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3d8f-145"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="e3d8f-146">Libreria</span><span class="sxs-lookup"><span data-stu-id="e3d8f-146">Library</span></span><br/> | <dl> <span data-ttu-id="e3d8f-147"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e3d8f-147"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="e3d8f-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e3d8f-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3d8f-149">**D3DXCreateCubeTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="e3d8f-149">**D3DXCreateCubeTextureFromResourceEx**</span></span>](d3dxcreatecubetexturefromresourceex.md)
</dt> <dt>

[<span data-ttu-id="e3d8f-150">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="e3d8f-150">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
