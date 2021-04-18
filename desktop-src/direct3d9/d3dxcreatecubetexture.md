---
description: Crea una trama del cubo vuota, modificando i parametri di chiamata in base alle esigenze.
ms.assetid: 96cf3fc1-9efc-4b97-a082-2956386145c7
title: Funzione D3DXCreateCubeTexture (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8fa31945cea5e65cdf00eae512059308090bcbab
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323422"
---
# <a name="d3dxcreatecubetexture-function"></a><span data-ttu-id="1c4a0-103">D3DXCreateCubeTexture (funzione)</span><span class="sxs-lookup"><span data-stu-id="1c4a0-103">D3DXCreateCubeTexture function</span></span>

<span data-ttu-id="1c4a0-104">Crea una trama del cubo vuota, modificando i parametri di chiamata in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="1c4a0-104">Creates an empty cube texture, adjusting the calling parameters as needed.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c4a0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1c4a0-105">Syntax</span></span>


```C++
HRESULT D3DXCreateCubeTexture(
  _In_  LPDIRECT3DDEVICE9      pDevice,
  _In_  UINT                   Size,
  _In_  UINT                   MipLevels,
  _In_  DWORD                  Usage,
  _In_  D3DFORMAT              Format,
  _In_  D3DPOOL                Pool,
  _Out_ LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="1c4a0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1c4a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c4a0-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1c4a0-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c4a0-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="1c4a0-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="1c4a0-109">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo da associare alla trama.</span><span class="sxs-lookup"><span data-stu-id="1c4a0-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="1c4a0-110">*Dimensioni* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1c4a0-110">*Size* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c4a0-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1c4a0-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1c4a0-112">Larghezza e altezza della trama del cubo, in pixel.</span><span class="sxs-lookup"><span data-stu-id="1c4a0-112">Width and height of the cube texture, in pixels.</span></span> <span data-ttu-id="1c4a0-113">Se, ad esempio, la trama del cubo è un cubo da 8 pixel a 8 pixel, il valore di questo parametro deve essere 8.</span><span class="sxs-lookup"><span data-stu-id="1c4a0-113">For example, if the cube texture is an 8-pixel by 8-pixel cube, the value for this parameter should be 8.</span></span>

</dd> <dt>

<span data-ttu-id="1c4a0-114">*MipLevels* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1c4a0-114">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c4a0-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1c4a0-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1c4a0-116">Numero di livelli MIP richiesti.</span><span class="sxs-lookup"><span data-stu-id="1c4a0-116">Number of mip levels requested.</span></span> <span data-ttu-id="1c4a0-117">Se questo valore è zero o D3DX \_ default, viene creata una catena mipmap completa.</span><span class="sxs-lookup"><span data-stu-id="1c4a0-117">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="1c4a0-118">*Utilizzo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="1c4a0-118">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c4a0-119">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1c4a0-119">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1c4a0-120">0, D3DUSAGE \_ RENDERTARGET o D3DUSAGE \_ Dynamic.</span><span class="sxs-lookup"><span data-stu-id="1c4a0-120">0, D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="1c4a0-121">L'impostazione di questo flag su D3DUSAGE \_ RENDERTARGET indica che la superficie deve essere utilizzata come destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="1c4a0-121">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="1c4a0-122">La risorsa può quindi essere passata al parametro *pNewRenderTarget* del metodo [**SetRenderTarget**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="1c4a0-122">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="1c4a0-123">Se \_ viene specificato D3DUSAGE RENDERTARGET, l'applicazione deve verificare che il dispositivo supporti questa operazione chiamando [**CheckDeviceFormat**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="1c4a0-123">If D3DUSAGE\_RENDERTARGET is specified, the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="1c4a0-124">Per ulteriori informazioni sull'utilizzo di trame dinamiche, vedere [using Dynamic Textures](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="1c4a0-124">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c4a0-125">*Formato* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1c4a0-125">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c4a0-126">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="1c4a0-126">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="1c4a0-127">Membro del tipo enumerato [D3DFORMAT](d3dformat.md) , che descrive il formato pixel richiesto per la trama del cubo.</span><span class="sxs-lookup"><span data-stu-id="1c4a0-127">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the cube texture.</span></span> <span data-ttu-id="1c4a0-128">La trama del cubo restituita potrebbe avere un formato diverso da quello specificato dal *formato*.</span><span class="sxs-lookup"><span data-stu-id="1c4a0-128">The returned cube texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="1c4a0-129">Le applicazioni devono controllare il formato della trama del cubo restituita.</span><span class="sxs-lookup"><span data-stu-id="1c4a0-129">Applications should check the format of the returned cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="1c4a0-130">*Pool* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="1c4a0-130">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c4a0-131">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="1c4a0-131">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="1c4a0-132">Membro del tipo enumerato [**D3DPOOL**](./d3dpool.md) , che descrive la classe di memoria in cui deve essere inserita la trama del cubo.</span><span class="sxs-lookup"><span data-stu-id="1c4a0-132">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the cube texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="1c4a0-133">*ppCubeTexture* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1c4a0-133">*ppCubeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1c4a0-134">Tipo: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="1c4a0-134">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span></span>

<span data-ttu-id="1c4a0-135">Indirizzo di un puntatore a un'interfaccia [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) , che rappresenta l'oggetto trama del cubo creato.</span><span class="sxs-lookup"><span data-stu-id="1c4a0-135">Address of a pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the created cube texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c4a0-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1c4a0-136">Return value</span></span>

<span data-ttu-id="1c4a0-137">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1c4a0-137">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1c4a0-138">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1c4a0-138">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1c4a0-139">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="1c4a0-139">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c4a0-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="1c4a0-140">Remarks</span></span>

<span data-ttu-id="1c4a0-141">Le trame del cubo differiscono dalle altre superfici perché sono raccolte di superfici.</span><span class="sxs-lookup"><span data-stu-id="1c4a0-141">Cube textures differ from other surfaces in that they are collections of surfaces.</span></span>

<span data-ttu-id="1c4a0-142">Internamente, D3DXCreateCubeTexture USA [**D3DXCheckCubeTextureRequirements**](d3dxcheckcubetexturerequirements.md) per modificare i parametri di chiamata.</span><span class="sxs-lookup"><span data-stu-id="1c4a0-142">Internally, D3DXCreateCubeTexture uses [**D3DXCheckCubeTextureRequirements**](d3dxcheckcubetexturerequirements.md) to adjust the calling parameters.</span></span> <span data-ttu-id="1c4a0-143">Di conseguenza, le chiamate a D3DXCreateCubeTexture avranno spesso esito positivo laddove le chiamate a [**CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) non riusciranno.</span><span class="sxs-lookup"><span data-stu-id="1c4a0-143">Therefore, calls to D3DXCreateCubeTexture will often succeed where calls to [**CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) would fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c4a0-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c4a0-144">Requirements</span></span>



| <span data-ttu-id="1c4a0-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c4a0-145">Requirement</span></span> | <span data-ttu-id="1c4a0-146">Valore</span><span class="sxs-lookup"><span data-stu-id="1c4a0-146">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1c4a0-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1c4a0-147">Header</span></span><br/>  | <dl> <span data-ttu-id="1c4a0-148"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c4a0-148"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="1c4a0-149">Libreria</span><span class="sxs-lookup"><span data-stu-id="1c4a0-149">Library</span></span><br/> | <dl> <span data-ttu-id="1c4a0-150"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1c4a0-150"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="1c4a0-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c4a0-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c4a0-152">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="1c4a0-152">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
