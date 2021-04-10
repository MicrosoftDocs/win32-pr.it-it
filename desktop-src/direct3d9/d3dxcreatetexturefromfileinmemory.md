---
description: Crea una trama da un file in memoria.
ms.assetid: 3ea811be-7db8-4436-b138-f0102389bb4d
title: Funzione D3DXCreateTextureFromFileInMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 743a944da52bc6d2ae13b045f854d95b4751712d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762065"
---
# <a name="d3dxcreatetexturefromfileinmemory-function"></a><span data-ttu-id="ca4df-103">D3DXCreateTextureFromFileInMemory (funzione)</span><span class="sxs-lookup"><span data-stu-id="ca4df-103">D3DXCreateTextureFromFileInMemory function</span></span>

<span data-ttu-id="ca4df-104">Crea una trama da un file in memoria.</span><span class="sxs-lookup"><span data-stu-id="ca4df-104">Creates a texture from a file in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca4df-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ca4df-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureFromFileInMemory(
  _In_  LPDIRECT3DDEVICE9  pDevice,
  _In_  LPCVOID            pSrcData,
  _In_  UINT               SrcDataSize,
  _Out_ LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a><span data-ttu-id="ca4df-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ca4df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca4df-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ca4df-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca4df-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="ca4df-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="ca4df-109">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) che rappresenta il dispositivo da associare alla trama.</span><span class="sxs-lookup"><span data-stu-id="ca4df-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="ca4df-110">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ca4df-110">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca4df-111">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ca4df-111">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ca4df-112">Puntatore al file in memoria da cui creare la trama.</span><span class="sxs-lookup"><span data-stu-id="ca4df-112">Pointer to the file in memory from which to create the texture.</span></span>

</dd> <dt>

<span data-ttu-id="ca4df-113">*SrcDataSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ca4df-113">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca4df-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ca4df-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ca4df-115">Dimensioni in byte del file in memoria.</span><span class="sxs-lookup"><span data-stu-id="ca4df-115">Size in bytes of the file in memory.</span></span>

</dd> <dt>

<span data-ttu-id="ca4df-116">*ppTexture* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ca4df-116">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ca4df-117">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="ca4df-117">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="ca4df-118">Indirizzo di un puntatore a un'interfaccia [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) che rappresenta l'oggetto trama creato.</span><span class="sxs-lookup"><span data-stu-id="ca4df-118">Address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca4df-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ca4df-119">Return value</span></span>

<span data-ttu-id="ca4df-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ca4df-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ca4df-121">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ca4df-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ca4df-122">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="ca4df-122">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca4df-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="ca4df-123">Remarks</span></span>

<span data-ttu-id="ca4df-124">La funzione è equivalente a D3DXCreateTextureFromFileInMemoryEx (pDevice, pSrcData, SrcDataSize, D3DX \_ default, D3DX \_ default, D3DX \_ default, 0, D3DFMT \_ Unknown, D3DPOOL \_ Managed, D3DX default, \_ D3DX \_ default, 0, **null**, **null**, ppTexture).</span><span class="sxs-lookup"><span data-stu-id="ca4df-124">The function is equivalent to D3DXCreateTextureFromFileInMemoryEx(pDevice, pSrcData, SrcDataSize, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppTexture).</span></span>

<span data-ttu-id="ca4df-125">Questa funzione supporta i formati di file seguenti:. bmp,. DDS,. DIB,. HDR,. jpg,. PFM,. png,. ppm e. tga.</span><span class="sxs-lookup"><span data-stu-id="ca4df-125">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="ca4df-126">Vedere [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="ca4df-126">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="ca4df-127">Si noti che una risorsa creata con questa funzione quando viene chiamata da un oggetto IDirect3DDevice9 verrà inserita nella classe di memoria indicata da D3DPOOL \_ gestito.</span><span class="sxs-lookup"><span data-stu-id="ca4df-127">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="ca4df-128">Quando questo metodo viene chiamato da un oggetto IDirect3DDevice9Ex, la risorsa verrà inserita nella classe di memoria indicata da D3DPOOL \_ default.</span><span class="sxs-lookup"><span data-stu-id="ca4df-128">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="ca4df-129">Il filtro viene applicato automaticamente a una trama creata utilizzando questo metodo.</span><span class="sxs-lookup"><span data-stu-id="ca4df-129">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="ca4df-130">Il filtro è equivalente a D3DX Filter D3DX del filtro \_ \_ \| \_ \_ di retinazione nel [ \_ filtro D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="ca4df-130">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ca4df-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ca4df-131">Requirements</span></span>



| <span data-ttu-id="ca4df-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca4df-132">Requirement</span></span> | <span data-ttu-id="ca4df-133">Valore</span><span class="sxs-lookup"><span data-stu-id="ca4df-133">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ca4df-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ca4df-134">Header</span></span><br/>  | <dl> <span data-ttu-id="ca4df-135"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca4df-135"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="ca4df-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="ca4df-136">Library</span></span><br/> | <dl> <span data-ttu-id="ca4df-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ca4df-137"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ca4df-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ca4df-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca4df-139">**D3DXCreateTextureFromFileInMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="ca4df-139">**D3DXCreateTextureFromFileInMemoryEx**</span></span>](d3dxcreatetexturefromfileinmemoryex.md)
</dt> <dt>

[<span data-ttu-id="ca4df-140">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="ca4df-140">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
