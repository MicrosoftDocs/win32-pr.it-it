---
description: Crea una trama vuota, modificando i parametri di chiamata in base alle esigenze.
ms.assetid: ea028aa9-4f37-4625-9e07-9072ec1a61d0
title: Funzione D3DXCreateTexture (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ecbd5cbb94355af9c1e51e6c7e8fc31a862b03be
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530918"
---
# <a name="d3dxcreatetexture-function"></a><span data-ttu-id="70ac8-103">D3DXCreateTexture (funzione)</span><span class="sxs-lookup"><span data-stu-id="70ac8-103">D3DXCreateTexture function</span></span>

<span data-ttu-id="70ac8-104">Crea una trama vuota, modificando i parametri di chiamata in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="70ac8-104">Creates an empty texture, adjusting the calling parameters as needed.</span></span>

## <a name="syntax"></a><span data-ttu-id="70ac8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="70ac8-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTexture(
  _In_  LPDIRECT3DDEVICE9  pDevice,
  _In_  UINT               Width,
  _In_  UINT               Height,
  _In_  UINT               MipLevels,
  _In_  DWORD              Usage,
  _In_  D3DFORMAT          Format,
  _In_  D3DPOOL            Pool,
  _Out_ LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a><span data-ttu-id="70ac8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="70ac8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70ac8-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="70ac8-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70ac8-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="70ac8-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="70ac8-109">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo da associare alla trama.</span><span class="sxs-lookup"><span data-stu-id="70ac8-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="70ac8-110">*Larghezza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="70ac8-110">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70ac8-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="70ac8-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="70ac8-112">Larghezza in pixel.</span><span class="sxs-lookup"><span data-stu-id="70ac8-112">Width in pixels.</span></span> <span data-ttu-id="70ac8-113">Se questo valore è 0, viene utilizzato il valore 1.</span><span class="sxs-lookup"><span data-stu-id="70ac8-113">If this value is 0, a value of 1 is used.</span></span> <span data-ttu-id="70ac8-114">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="70ac8-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="70ac8-115">*Altezza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="70ac8-115">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70ac8-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="70ac8-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="70ac8-117">Altezza in pixel.</span><span class="sxs-lookup"><span data-stu-id="70ac8-117">Height in pixels.</span></span> <span data-ttu-id="70ac8-118">Se questo valore è 0, viene utilizzato il valore 1.</span><span class="sxs-lookup"><span data-stu-id="70ac8-118">If this value is 0, a value of 1 is used.</span></span> <span data-ttu-id="70ac8-119">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="70ac8-119">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="70ac8-120">*MipLevels* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="70ac8-120">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70ac8-121">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="70ac8-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="70ac8-122">Numero di livelli MIP richiesti.</span><span class="sxs-lookup"><span data-stu-id="70ac8-122">Number of mip levels requested.</span></span> <span data-ttu-id="70ac8-123">Se questo valore è zero o D3DX \_ default, viene creata una catena mipmap completa.</span><span class="sxs-lookup"><span data-stu-id="70ac8-123">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="70ac8-124">*Utilizzo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="70ac8-124">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70ac8-125">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="70ac8-125">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="70ac8-126">0, [**D3DUSAGE \_ RENDERTARGET**](d3dusage.md)o **D3DUSAGE \_ Dynamic**.</span><span class="sxs-lookup"><span data-stu-id="70ac8-126">0, [**D3DUSAGE\_RENDERTARGET**](d3dusage.md), or **D3DUSAGE\_DYNAMIC**.</span></span> <span data-ttu-id="70ac8-127">L'impostazione di questo flag su **D3DUSAGE \_ RENDERTARGET** indica che la superficie deve essere utilizzata come destinazione di rendering chiamando il metodo [**SetRenderTarget**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="70ac8-127">Setting this flag to **D3DUSAGE\_RENDERTARGET** indicates that the surface is to be used as a render target by calling the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="70ac8-128">Se viene specificato **D3DUSAGE \_ RENDERTARGET** o **D3DUSAGE \_ Dynamic** , l'applicazione deve verificare che il dispositivo supporti questa operazione chiamando [**CheckDeviceFormat**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="70ac8-128">If either **D3DUSAGE\_RENDERTARGET** or **D3DUSAGE\_DYNAMIC** is specified, the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="70ac8-129">Per ulteriori informazioni sull'utilizzo di trame dinamiche, vedere [using Dynamic Textures](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="70ac8-129">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="70ac8-130">*Formato* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="70ac8-130">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70ac8-131">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="70ac8-131">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="70ac8-132">Membro del tipo enumerato [D3DFORMAT](d3dformat.md) , che descrive il formato pixel richiesto per la trama.</span><span class="sxs-lookup"><span data-stu-id="70ac8-132">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the texture.</span></span> <span data-ttu-id="70ac8-133">Il formato della trama restituita può essere diverso da quello specificato, se il dispositivo non supporta il formato richiesto.</span><span class="sxs-lookup"><span data-stu-id="70ac8-133">The returned texture may be of a different format from that specified, if the device does not support the requested format.</span></span> <span data-ttu-id="70ac8-134">Le applicazioni devono controllare il formato della trama restituita per verificare se corrisponde al formato richiesto.</span><span class="sxs-lookup"><span data-stu-id="70ac8-134">Applications should check the format of the returned texture to see if it matches the format requested.</span></span>

</dd> <dt>

<span data-ttu-id="70ac8-135">*Pool* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="70ac8-135">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70ac8-136">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="70ac8-136">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="70ac8-137">Membro del tipo enumerato [**D3DPOOL**](./d3dpool.md) , che descrive la classe di memoria in cui deve essere posizionata la trama.</span><span class="sxs-lookup"><span data-stu-id="70ac8-137">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="70ac8-138">*ppTexture* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="70ac8-138">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="70ac8-139">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="70ac8-139">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="70ac8-140">Indirizzo di un puntatore a un'interfaccia [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , che rappresenta l'oggetto trama creato.</span><span class="sxs-lookup"><span data-stu-id="70ac8-140">Address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70ac8-141">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="70ac8-141">Return value</span></span>

<span data-ttu-id="70ac8-142">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="70ac8-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="70ac8-143">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="70ac8-143">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="70ac8-144">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="70ac8-144">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="70ac8-145">Commenti</span><span class="sxs-lookup"><span data-stu-id="70ac8-145">Remarks</span></span>

<span data-ttu-id="70ac8-146">Internamente, D3DXCreateTexture USA [**D3DXCheckTextureRequirements**](d3dxchecktexturerequirements.md) per modificare i parametri di chiamata.</span><span class="sxs-lookup"><span data-stu-id="70ac8-146">Internally, D3DXCreateTexture uses [**D3DXCheckTextureRequirements**](d3dxchecktexturerequirements.md) to adjust the calling parameters.</span></span> <span data-ttu-id="70ac8-147">Di conseguenza, le chiamate a D3DXCreateTexture avranno spesso esito positivo laddove le chiamate a [**createTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) non riusciranno.</span><span class="sxs-lookup"><span data-stu-id="70ac8-147">Therefore, calls to D3DXCreateTexture will often succeed where calls to [**CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) would fail.</span></span>

<span data-ttu-id="70ac8-148">Se l'altezza e la larghezza sono impostate su [D3DX \_ default](other-d3dx-constants.md), per entrambi i parametri viene utilizzato il valore 256.</span><span class="sxs-lookup"><span data-stu-id="70ac8-148">If both Height and Width are set to [D3DX\_DEFAULT](other-d3dx-constants.md), a value of 256 is used for both parameters.</span></span> <span data-ttu-id="70ac8-149">Se l'altezza o la larghezza è impostata su D3DX \_ default e l'altro parametro è impostato su un valore numerico, la trama sarà quadrata con l'altezza e la larghezza uguali al valore numerico.</span><span class="sxs-lookup"><span data-stu-id="70ac8-149">If either Height or Width is set to D3DX\_DEFAULT And the other parameter is set to a numeric value, the texture will be square with both the height and width equal to the numeric value.</span></span>

## <a name="requirements"></a><span data-ttu-id="70ac8-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="70ac8-150">Requirements</span></span>



| <span data-ttu-id="70ac8-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="70ac8-151">Requirement</span></span> | <span data-ttu-id="70ac8-152">Valore</span><span class="sxs-lookup"><span data-stu-id="70ac8-152">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="70ac8-153">Intestazione</span><span class="sxs-lookup"><span data-stu-id="70ac8-153">Header</span></span><br/>  | <dl> <span data-ttu-id="70ac8-154"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="70ac8-154"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="70ac8-155">Libreria</span><span class="sxs-lookup"><span data-stu-id="70ac8-155">Library</span></span><br/> | <dl> <span data-ttu-id="70ac8-156"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="70ac8-156"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="70ac8-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="70ac8-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70ac8-158">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="70ac8-158">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
