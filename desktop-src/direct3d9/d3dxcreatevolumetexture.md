---
description: Crea una trama del volume vuota, modificando i parametri di chiamata in base alle esigenze.
ms.assetid: 8fc515cd-2fb3-40c7-8192-a41d93ac1e99
title: Funzione D3DXCreateVolumeTexture (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 50baf125d2e5375bddb63a41a0d10ae063a57b78
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969359"
---
# <a name="d3dxcreatevolumetexture-function"></a><span data-ttu-id="f3eb2-103">D3DXCreateVolumeTexture (funzione)</span><span class="sxs-lookup"><span data-stu-id="f3eb2-103">D3DXCreateVolumeTexture function</span></span>

<span data-ttu-id="f3eb2-104">Crea una trama del volume vuota, modificando i parametri di chiamata in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-104">Creates an empty volume texture, adjusting the calling parameters as needed.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3eb2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f3eb2-105">Syntax</span></span>


```C++
HRESULT D3DXCreateVolumeTexture(
  _In_  LPDIRECT3DDEVICE9        pDevice,
  _In_  UINT                     Width,
  _In_  UINT                     Height,
  _In_  UINT                     Depth,
  _In_  UINT                     MipLevels,
  _In_  DWORD                    Usage,
  _In_  D3DFORMAT                Format,
  _In_  D3DPOOL                  Pool,
  _Out_ LPDIRECT3DVOLUMETEXTURE9 *ppVolumeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="f3eb2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f3eb2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3eb2-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f3eb2-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3eb2-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="f3eb2-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="f3eb2-109">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo da associare alla trama del volume.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb2-110">*Larghezza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f3eb2-110">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3eb2-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f3eb2-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f3eb2-112">Larghezza in pixel.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-112">Width in pixels.</span></span> <span data-ttu-id="f3eb2-113">Questo valore deve essere diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-113">This value must be nonzero.</span></span> <span data-ttu-id="f3eb2-114">La dimensione massima supportata da un driver (per larghezza, altezza e profondità) si trova in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="f3eb2-114">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="f3eb2-115">*Altezza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f3eb2-115">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3eb2-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f3eb2-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f3eb2-117">Altezza in pixel.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-117">Height in pixels.</span></span> <span data-ttu-id="f3eb2-118">Questo valore deve essere diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-118">This value must be nonzero.</span></span> <span data-ttu-id="f3eb2-119">La dimensione massima supportata da un driver (per larghezza, altezza e profondità) si trova in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="f3eb2-119">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="f3eb2-120">*Profondità* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f3eb2-120">*Depth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3eb2-121">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f3eb2-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f3eb2-122">Profondità in pixel.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-122">Depth in pixels.</span></span> <span data-ttu-id="f3eb2-123">Questo valore deve essere diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-123">This value must be nonzero.</span></span> <span data-ttu-id="f3eb2-124">La dimensione massima supportata da un driver (per larghezza, altezza e profondità) si trova in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="f3eb2-124">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="f3eb2-125">*MipLevels* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f3eb2-125">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3eb2-126">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f3eb2-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f3eb2-127">Numero di livelli MIP richiesti.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-127">Number of mip levels requested.</span></span> <span data-ttu-id="f3eb2-128">Se questo valore è zero o D3DX \_ default, viene creata una catena mipmap completa.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-128">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb2-129">*Utilizzo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="f3eb2-129">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3eb2-130">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f3eb2-130">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f3eb2-131">0 o D3DUSAGE \_ dinamico.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-131">0 or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="f3eb2-132">Per ulteriori informazioni sull'utilizzo di trame dinamiche, vedere [using Dynamic Textures](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="f3eb2-132">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3eb2-133">*Formato* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f3eb2-133">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3eb2-134">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="f3eb2-134">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="f3eb2-135">Membro del tipo enumerato [D3DFORMAT](d3dformat.md) , che descrive il formato pixel richiesto per la trama del volume.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-135">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the volume texture.</span></span> <span data-ttu-id="f3eb2-136">Il formato della trama del volume restituito può essere diverso da quello specificato dal formato.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-136">The returned volume texture might have a different format from that specified by Format.</span></span> <span data-ttu-id="f3eb2-137">Le applicazioni devono controllare il formato della trama del volume restituito.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-137">Applications should check the format of the returned volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb2-138">*Pool* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="f3eb2-138">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3eb2-139">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="f3eb2-139">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="f3eb2-140">Membro del tipo enumerato [**D3DPOOL**](./d3dpool.md) , che descrive la classe di memoria in cui deve essere inserita la trama del volume.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-140">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the volume texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb2-141">*ppVolumeTexture* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f3eb2-141">*ppVolumeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f3eb2-142">Tipo: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="f3eb2-142">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span></span>

<span data-ttu-id="f3eb2-143">Indirizzo di un puntatore a un'interfaccia [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) , che rappresenta l'oggetto trama del volume creato.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-143">Address of a pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface, representing the created volume texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3eb2-144">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f3eb2-144">Return value</span></span>

<span data-ttu-id="f3eb2-145">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f3eb2-145">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f3eb2-146">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-146">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f3eb2-147">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-147">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, E\_OUTOFMEMORY .</span></span>

## <a name="remarks"></a><span data-ttu-id="f3eb2-148">Commenti</span><span class="sxs-lookup"><span data-stu-id="f3eb2-148">Remarks</span></span>

<span data-ttu-id="f3eb2-149">Internamente, D3DXCreateVolumeTexture USA [**D3DXCheckVolumeTextureRequirements**](d3dxcheckvolumetexturerequirements.md) per modificare i parametri di chiamata.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-149">Internally, D3DXCreateVolumeTexture uses [**D3DXCheckVolumeTextureRequirements**](d3dxcheckvolumetexturerequirements.md) to adjust the calling parameters.</span></span> <span data-ttu-id="f3eb2-150">Di conseguenza, le chiamate a D3DXCreateVolumeTexture avranno spesso esito positivo laddove le chiamate a [**CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture) non riusciranno.</span><span class="sxs-lookup"><span data-stu-id="f3eb2-150">Therefore, calls to D3DXCreateVolumeTexture will often succeed where calls to [**CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture) would fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3eb2-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f3eb2-151">Requirements</span></span>



| <span data-ttu-id="f3eb2-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3eb2-152">Requirement</span></span> | <span data-ttu-id="f3eb2-153">Valore</span><span class="sxs-lookup"><span data-stu-id="f3eb2-153">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f3eb2-154">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f3eb2-154">Header</span></span><br/>  | <dl> <span data-ttu-id="f3eb2-155"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3eb2-155"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="f3eb2-156">Libreria</span><span class="sxs-lookup"><span data-stu-id="f3eb2-156">Library</span></span><br/> | <dl> <span data-ttu-id="f3eb2-157"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f3eb2-157"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="f3eb2-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f3eb2-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3eb2-159">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="f3eb2-159">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
