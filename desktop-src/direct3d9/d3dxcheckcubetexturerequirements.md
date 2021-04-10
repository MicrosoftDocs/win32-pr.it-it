---
description: Verifica i parametri di creazione della trama del cubo.
ms.assetid: 56ced947-1142-4d05-95e3-ca6a26b147d4
title: Funzione D3DXCheckCubeTextureRequirements (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCheckCubeTextureRequirements
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9f800617920c5d79361b5e6da291fd88b5b963b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762352"
---
# <a name="d3dxcheckcubetexturerequirements-function"></a><span data-ttu-id="cec45-103">D3DXCheckCubeTextureRequirements (funzione)</span><span class="sxs-lookup"><span data-stu-id="cec45-103">D3DXCheckCubeTextureRequirements function</span></span>

<span data-ttu-id="cec45-104">Verifica i parametri di creazione della trama del cubo.</span><span class="sxs-lookup"><span data-stu-id="cec45-104">Checks cube-texture-creation parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="cec45-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cec45-105">Syntax</span></span>


```C++
HRESULT D3DXCheckCubeTextureRequirements(
  _In_    LPDIRECT3DDEVICE9 pDevice,
  _Inout_ UINT              *pSize,
  _Inout_ UINT              *pNumMipLevels,
  _In_    DWORD             Usage,
  _Inout_ D3DFORMAT         *pFormat,
  _In_    D3DPOOL           Pool
);
```



## <a name="parameters"></a><span data-ttu-id="cec45-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cec45-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cec45-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cec45-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cec45-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="cec45-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="cec45-109">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo da associare alla trama del cubo.</span><span class="sxs-lookup"><span data-stu-id="cec45-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="cec45-110">*psize* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="cec45-110">*pSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cec45-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="cec45-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="cec45-112">Puntatore alla larghezza e all'altezza richieste in pixel o **null**.</span><span class="sxs-lookup"><span data-stu-id="cec45-112">Pointer to the requested width and height in pixels, or **NULL**.</span></span> <span data-ttu-id="cec45-113">Restituisce la dimensione corretta.</span><span class="sxs-lookup"><span data-stu-id="cec45-113">Returns the corrected size.</span></span>

</dd> <dt>

<span data-ttu-id="cec45-114">*pNumMipLevels* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="cec45-114">*pNumMipLevels* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cec45-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="cec45-115">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="cec45-116">Puntatore al numero di livelli di mipmap richiesti o **null**.</span><span class="sxs-lookup"><span data-stu-id="cec45-116">Pointer to the number of requested mipmap levels, or **NULL**.</span></span> <span data-ttu-id="cec45-117">Restituisce il numero corretto di livelli di mipmap.</span><span class="sxs-lookup"><span data-stu-id="cec45-117">Returns the corrected number of mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="cec45-118">*Utilizzo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="cec45-118">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cec45-119">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cec45-119">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cec45-120">0 o D3DUSAGE \_ RENDERTARGET.</span><span class="sxs-lookup"><span data-stu-id="cec45-120">0 or D3DUSAGE\_RENDERTARGET.</span></span> <span data-ttu-id="cec45-121">L'impostazione di questo flag su D3DUSAGE \_ RENDERTARGET indica che la superficie deve essere utilizzata come destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="cec45-121">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="cec45-122">La risorsa può quindi essere passata al parametro pNewRenderTarget del metodo [**SetRenderTarget**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="cec45-122">The resource can then be passed to the pNewRenderTarget parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="cec45-123">Se \_ viene specificato D3DUSAGE RENDERTARGET, l'applicazione deve verificare che il dispositivo supporti questa operazione chiamando [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat).</span><span class="sxs-lookup"><span data-stu-id="cec45-123">If D3DUSAGE\_RENDERTARGET is specified, the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat).</span></span>

</dd> <dt>

<span data-ttu-id="cec45-124">*pFormat* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="cec45-124">*pFormat* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cec45-125">Tipo: **[D3DFORMAT](d3dformat.md)\***</span><span class="sxs-lookup"><span data-stu-id="cec45-125">Type: **[D3DFORMAT](d3dformat.md)\***</span></span>

<span data-ttu-id="cec45-126">Puntatore a un membro del tipo enumerato [D3DFORMAT](d3dformat.md) .</span><span class="sxs-lookup"><span data-stu-id="cec45-126">Pointer to a member of the [D3DFORMAT](d3dformat.md) enumerated type.</span></span> <span data-ttu-id="cec45-127">Specifica il formato pixel desiderato o **null**.</span><span class="sxs-lookup"><span data-stu-id="cec45-127">Specifies the desired pixel format, or **NULL**.</span></span> <span data-ttu-id="cec45-128">Restituisce il formato corretto.</span><span class="sxs-lookup"><span data-stu-id="cec45-128">Returns the corrected format.</span></span>

</dd> <dt>

<span data-ttu-id="cec45-129">*Pool* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="cec45-129">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cec45-130">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="cec45-130">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="cec45-131">Membro del tipo enumerato [**D3DPOOL**](./d3dpool.md) , che descrive la classe di memoria in cui deve essere posizionata la trama.</span><span class="sxs-lookup"><span data-stu-id="cec45-131">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cec45-132">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cec45-132">Return value</span></span>

<span data-ttu-id="cec45-133">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cec45-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cec45-134">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cec45-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="cec45-135">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ NOTAVAILABLE, D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="cec45-135">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="cec45-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="cec45-136">Remarks</span></span>

<span data-ttu-id="cec45-137">Se i parametri di questa funzione non sono validi, questa funzione restituisce parametri corretti.</span><span class="sxs-lookup"><span data-stu-id="cec45-137">If parameters to this function are invalid, this function returns corrected parameters.</span></span>

<span data-ttu-id="cec45-138">Le trame del cubo differiscono dalle altre superfici perché sono raccolte di superfici.</span><span class="sxs-lookup"><span data-stu-id="cec45-138">Cube textures differ from other surfaces in that they are collections of surfaces.</span></span> <span data-ttu-id="cec45-139">Per chiamare [**SetRenderTarget**](/windows/desktop/api) con una trama del cubo, è necessario selezionare un singolo volto usando [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) e passare la superficie risultante a **SetRenderTarget**.</span><span class="sxs-lookup"><span data-stu-id="cec45-139">To call [**SetRenderTarget**](/windows/desktop/api) with a cube texture, you must select an individual face using [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) and pass the resulting surface to **SetRenderTarget**.</span></span>

## <a name="requirements"></a><span data-ttu-id="cec45-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cec45-140">Requirements</span></span>



| <span data-ttu-id="cec45-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="cec45-141">Requirement</span></span> | <span data-ttu-id="cec45-142">Valore</span><span class="sxs-lookup"><span data-stu-id="cec45-142">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cec45-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cec45-143">Header</span></span><br/>  | <dl> <span data-ttu-id="cec45-144"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="cec45-144"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="cec45-145">Libreria</span><span class="sxs-lookup"><span data-stu-id="cec45-145">Library</span></span><br/> | <dl> <span data-ttu-id="cec45-146"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cec45-146"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="cec45-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cec45-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cec45-148">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="cec45-148">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
