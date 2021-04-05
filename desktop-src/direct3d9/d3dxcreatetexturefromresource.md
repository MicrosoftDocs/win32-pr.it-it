---
description: Crea una trama da una risorsa.
ms.assetid: 7c841f21-5565-4923-a2fe-bbd618616f87
title: Funzione D3DXCreateTextureFromResource (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4ce9101caed2a60dc3be7fe0039a1e391423f1fe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103886279"
---
# <a name="d3dxcreatetexturefromresource-function"></a><span data-ttu-id="b995f-103">D3DXCreateTextureFromResource (funzione)</span><span class="sxs-lookup"><span data-stu-id="b995f-103">D3DXCreateTextureFromResource function</span></span>

<span data-ttu-id="b995f-104">Crea una trama da una risorsa.</span><span class="sxs-lookup"><span data-stu-id="b995f-104">Creates a texture from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="b995f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b995f-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureFromResource(
  _In_  LPDIRECT3DDEVICE9  pDevice,
  _In_  HMODULE            hSrcModule,
  _In_  LPCTSTR            pSrcResource,
  _Out_ LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a><span data-ttu-id="b995f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b995f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b995f-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b995f-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b995f-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="b995f-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="b995f-109">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo da associare alla trama.</span><span class="sxs-lookup"><span data-stu-id="b995f-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="b995f-110">*hSrcModule* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b995f-110">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b995f-111">Tipo: **[ **hmodule**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b995f-111">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b995f-112">Handle per il modulo in cui si trova la risorsa o **null** per il modulo associato all'immagine utilizzata dal sistema operativo per creare il processo corrente.</span><span class="sxs-lookup"><span data-stu-id="b995f-112">Handle to the module where the resource is located, or **NULL** for module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="b995f-113">*pSrcResource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b995f-113">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b995f-114">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b995f-114">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b995f-115">Puntatore a una stringa che specifica il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="b995f-115">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="b995f-116">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="b995f-116">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="b995f-117">In caso contrario, il tipo di dati String viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="b995f-117">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="b995f-118">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="b995f-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="b995f-119">*ppTexture* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b995f-119">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b995f-120">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="b995f-120">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="b995f-121">Indirizzo di un puntatore a un'interfaccia [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , che rappresenta l'oggetto trama creato.</span><span class="sxs-lookup"><span data-stu-id="b995f-121">Address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b995f-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b995f-122">Return value</span></span>

<span data-ttu-id="b995f-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b995f-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b995f-124">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b995f-124">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b995f-125">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="b995f-125">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="b995f-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="b995f-126">Remarks</span></span>

<span data-ttu-id="b995f-127">L'impostazione del compilatore determina anche la versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="b995f-127">The compiler setting also determines the function version.</span></span> <span data-ttu-id="b995f-128">Se è definito Unicode, la chiamata di funzione viene risolta in D3DXCreateTextureFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="b995f-128">If Unicode is defined, the function call resolves to D3DXCreateTextureFromResourceW.</span></span> <span data-ttu-id="b995f-129">In caso contrario, la chiamata di funzione viene risolta in D3DXCreateTextureFromResourceA perché vengono utilizzate le stringhe ANSI.</span><span class="sxs-lookup"><span data-stu-id="b995f-129">Otherwise, the function call resolves to D3DXCreateTextureFromResourceA because ANSI strings are being used.</span></span>

<span data-ttu-id="b995f-130">La funzione è equivalente a D3DXCreateTextureFromResourceEx (pDevice, hSrcModule, pSrcResource, D3DX \_ default, D3DX \_ default, D3DX \_ default, 0, D3DFMT \_ Unknown, D3DPOOL \_ Managed, D3DX default, \_ D3DX \_ default, 0, **null**, **null**, ppTexture).</span><span class="sxs-lookup"><span data-stu-id="b995f-130">The function is equivalent to D3DXCreateTextureFromResourceEx(pDevice, hSrcModule, pSrcResource, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppTexture).</span></span>

<span data-ttu-id="b995f-131">La risorsa da caricare deve essere di tipo RT \_ bitmap o RT \_ RCDATA.</span><span class="sxs-lookup"><span data-stu-id="b995f-131">The resource being loaded must be of type RT\_BITMAP or RT\_RCDATA.</span></span> <span data-ttu-id="b995f-132">Il tipo di risorsa RT \_ RCDATA viene usato per caricare formati diversi da bitmap, ad esempio. tga,. jpg e. DDS.</span><span class="sxs-lookup"><span data-stu-id="b995f-132">Resource type RT\_RCDATA is used to load formats other than bitmaps (such as .tga, .jpg, and .dds).</span></span>

<span data-ttu-id="b995f-133">Questa funzione supporta i formati di file seguenti:. bmp,. DDS,. DIB,. HDR,. jpg,. PFM,. png,. ppm e. tga.</span><span class="sxs-lookup"><span data-stu-id="b995f-133">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="b995f-134">Vedere [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="b995f-134">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="b995f-135">Si noti che una risorsa creata con questa funzione quando viene chiamata da un oggetto IDirect3DDevice9 verrà inserita nella classe di memoria indicata da D3DPOOL \_ gestito.</span><span class="sxs-lookup"><span data-stu-id="b995f-135">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="b995f-136">Quando questo metodo viene chiamato da un oggetto IDirect3DDevice9Ex, la risorsa verrà inserita nella classe di memoria indicata da D3DPOOL \_ default.</span><span class="sxs-lookup"><span data-stu-id="b995f-136">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="b995f-137">Il filtro viene applicato automaticamente a una trama creata utilizzando questo metodo.</span><span class="sxs-lookup"><span data-stu-id="b995f-137">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="b995f-138">Il filtro è equivalente a D3DX Filter D3DX del filtro \_ \_ \| \_ \_ di retinazione nel [ \_ filtro D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="b995f-138">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b995f-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b995f-139">Requirements</span></span>



| <span data-ttu-id="b995f-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="b995f-140">Requirement</span></span> | <span data-ttu-id="b995f-141">Valore</span><span class="sxs-lookup"><span data-stu-id="b995f-141">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b995f-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b995f-142">Header</span></span><br/>  | <dl> <span data-ttu-id="b995f-143"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="b995f-143"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="b995f-144">Libreria</span><span class="sxs-lookup"><span data-stu-id="b995f-144">Library</span></span><br/> | <dl> <span data-ttu-id="b995f-145"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b995f-145"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="b995f-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b995f-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b995f-147">**D3DXCreateTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="b995f-147">**D3DXCreateTextureFromResourceEx**</span></span>](d3dxcreatetexturefromresourceex.md)
</dt> <dt>

[<span data-ttu-id="b995f-148">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="b995f-148">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
