---
description: Crea una trama del cubo da un file in memoria.
ms.assetid: f7e99d5a-5479-4f0b-b040-bb07e7e37666
title: Funzione D3DXCreateCubeTextureFromFileInMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3f1d6de3fba0dcbda959a2811ec665ebc4a6541c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322908"
---
# <a name="d3dxcreatecubetexturefromfileinmemory-function"></a><span data-ttu-id="cb5b2-103">D3DXCreateCubeTextureFromFileInMemory (funzione)</span><span class="sxs-lookup"><span data-stu-id="cb5b2-103">D3DXCreateCubeTextureFromFileInMemory function</span></span>

<span data-ttu-id="cb5b2-104">Crea una trama del cubo da un file in memoria.</span><span class="sxs-lookup"><span data-stu-id="cb5b2-104">Creates a cube texture from a file in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb5b2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cb5b2-105">Syntax</span></span>


```C++
HRESULT D3DXCreateCubeTextureFromFileInMemory(
  _In_  LPDIRECT3DDEVICE9      pDevice,
  _In_  LPCVOID                pSrcData,
  _In_  UINT                   SrcDataSize,
  _Out_ LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="cb5b2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cb5b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb5b2-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cb5b2-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb5b2-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="cb5b2-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="cb5b2-109">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo da associare alla trama del cubo.</span><span class="sxs-lookup"><span data-stu-id="cb5b2-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="cb5b2-110">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cb5b2-110">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb5b2-111">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cb5b2-111">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cb5b2-112">Puntatore al file in memoria da cui creare il mappa cubi.</span><span class="sxs-lookup"><span data-stu-id="cb5b2-112">Pointer to the file in memory from which to create the cubemap.</span></span> <span data-ttu-id="cb5b2-113">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="cb5b2-113">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="cb5b2-114">*SrcDataSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cb5b2-114">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb5b2-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cb5b2-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cb5b2-116">Dimensioni in byte del file in memoria.</span><span class="sxs-lookup"><span data-stu-id="cb5b2-116">Size of the file in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="cb5b2-117">*ppCubeTexture* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cb5b2-117">*ppCubeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb5b2-118">Tipo: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="cb5b2-118">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span></span>

<span data-ttu-id="cb5b2-119">Indirizzo di un puntatore a un'interfaccia [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) , che rappresenta l'oggetto trama del cubo creato.</span><span class="sxs-lookup"><span data-stu-id="cb5b2-119">Address of a pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the created cube texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb5b2-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cb5b2-120">Return value</span></span>

<span data-ttu-id="cb5b2-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cb5b2-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cb5b2-122">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cb5b2-122">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="cb5b2-123">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="cb5b2-123">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb5b2-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="cb5b2-124">Remarks</span></span>

<span data-ttu-id="cb5b2-125">Questa funzione supporta i formati di file seguenti:. bmp,. DDS,. DIB,. HDR,. jpg,. PFM,. png,. ppm e. tga.</span><span class="sxs-lookup"><span data-stu-id="cb5b2-125">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="cb5b2-126">Vedere [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="cb5b2-126">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="cb5b2-127">La funzione è equivalente a D3DXCreateCubeTextureFromFileInMemoryEx (pDevice, pSrcData, SrcDataSize, D3DX \_ default, D3DX \_ default, 0, D3DFMT \_ Unknown, D3DPOOL \_ Managed, D3DX \_ default, D3DX \_ default, 0, **null**, **null**, ppCubeTexture).</span><span class="sxs-lookup"><span data-stu-id="cb5b2-127">The function is equivalent to D3DXCreateCubeTextureFromFileInMemoryEx(pDevice, pSrcData, SrcDataSize, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppCubeTexture).</span></span>

<span data-ttu-id="cb5b2-128">Si noti che una risorsa creata con questa funzione quando viene chiamata da un oggetto IDirect3DDevice9 verrà inserita nella classe di memoria indicata da D3DPOOL \_ gestito.</span><span class="sxs-lookup"><span data-stu-id="cb5b2-128">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="cb5b2-129">Quando questo metodo viene chiamato da un oggetto IDirect3DDevice9Ex, la risorsa verrà inserita nella classe di memoria indicata da D3DPOOL \_ default.</span><span class="sxs-lookup"><span data-stu-id="cb5b2-129">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="cb5b2-130">Questo metodo è progettato per essere usato per il caricamento di file di immagine archiviati come RT \_ RCDATA, ovvero una risorsa definita dall'applicazione (dati non elaborati).</span><span class="sxs-lookup"><span data-stu-id="cb5b2-130">This method is designed to be used for loading image files stored as RT\_RCDATA, which is an application-defined resource (raw data).</span></span> <span data-ttu-id="cb5b2-131">In caso contrario, questo metodo avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="cb5b2-131">Otherwise this method will fail.</span></span>

<span data-ttu-id="cb5b2-132">Il filtro viene applicato automaticamente a una trama creata utilizzando questo metodo.</span><span class="sxs-lookup"><span data-stu-id="cb5b2-132">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="cb5b2-133">Il filtro è equivalente a D3DX Filter D3DX del filtro \_ \_ \| \_ \_ di retinazione nel [ \_ filtro D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="cb5b2-133">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

<span data-ttu-id="cb5b2-134">**D3DXCreateCubeTextureFromFileInMemory** usa il formato di file DirectDraw Surface (DDS).</span><span class="sxs-lookup"><span data-stu-id="cb5b2-134">**D3DXCreateCubeTextureFromFileInMemory** uses the DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="cb5b2-135">L'editor di trame DirectX (Dxtex.exe) consente di generare una mappa del cubo da altri formati di file e di salvarli nel formato di file DDS.</span><span class="sxs-lookup"><span data-stu-id="cb5b2-135">The DirectX Texture Editor (Dxtex.exe) enables you to generate a cube map from other file formats and save it in the DDS file format.</span></span> <span data-ttu-id="cb5b2-136">È possibile ottenere Dxtex.exe e ottenere informazioni su di esso da DirectX SDK.</span><span class="sxs-lookup"><span data-stu-id="cb5b2-136">You can get Dxtex.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="cb5b2-137">Per informazioni su DirectX SDK, vedere [dove è DirectX SDK?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="cb5b2-137">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cb5b2-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cb5b2-138">Requirements</span></span>



| <span data-ttu-id="cb5b2-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb5b2-139">Requirement</span></span> | <span data-ttu-id="cb5b2-140">Valore</span><span class="sxs-lookup"><span data-stu-id="cb5b2-140">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cb5b2-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cb5b2-141">Header</span></span><br/>  | <dl> <span data-ttu-id="cb5b2-142"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb5b2-142"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="cb5b2-143">Libreria</span><span class="sxs-lookup"><span data-stu-id="cb5b2-143">Library</span></span><br/> | <dl> <span data-ttu-id="cb5b2-144"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cb5b2-144"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="cb5b2-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cb5b2-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb5b2-146">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="cb5b2-146">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
