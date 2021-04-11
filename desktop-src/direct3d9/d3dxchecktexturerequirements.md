---
description: Verifica i parametri per la creazione di trame.
ms.assetid: f8e788f3-02a9-4ee7-b74d-9e781a2fb39f
title: Funzione D3DXCheckTextureRequirements (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCheckTextureRequirements
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d4fdc0998bfda2144e900c099919bc75c01e8ee3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235062"
---
# <a name="d3dxchecktexturerequirements-function"></a><span data-ttu-id="99a4a-103">D3DXCheckTextureRequirements (funzione)</span><span class="sxs-lookup"><span data-stu-id="99a4a-103">D3DXCheckTextureRequirements function</span></span>

<span data-ttu-id="99a4a-104">Verifica i parametri per la creazione di trame.</span><span class="sxs-lookup"><span data-stu-id="99a4a-104">Checks texture-creation parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="99a4a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="99a4a-105">Syntax</span></span>


```C++
HRESULT D3DXCheckTextureRequirements(
  _In_    LPDIRECT3DDEVICE9 pDevice,
  _Inout_ UINT              *pWidth,
  _Inout_ UINT              *pHeight,
  _Inout_ UINT              *pNumMipLevels,
  _In_    DWORD             Usage,
  _Inout_ D3DFORMAT         *pFormat,
  _In_    D3DPOOL           Pool
);
```



## <a name="parameters"></a><span data-ttu-id="99a4a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="99a4a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99a4a-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="99a4a-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99a4a-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="99a4a-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="99a4a-109">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo da associare alla trama.</span><span class="sxs-lookup"><span data-stu-id="99a4a-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="99a4a-110">*pWidth* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="99a4a-110">*pWidth* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="99a4a-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="99a4a-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="99a4a-112">Puntatore alla larghezza richiesta, in pixel, o **null**.</span><span class="sxs-lookup"><span data-stu-id="99a4a-112">Pointer to the requested width in pixels, or **NULL**.</span></span> <span data-ttu-id="99a4a-113">Restituisce la dimensione corretta.</span><span class="sxs-lookup"><span data-stu-id="99a4a-113">Returns the corrected size.</span></span>

</dd> <dt>

<span data-ttu-id="99a4a-114">*pHeight* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="99a4a-114">*pHeight* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="99a4a-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="99a4a-115">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="99a4a-116">Puntatore all'altezza richiesta, in pixel, o **null**.</span><span class="sxs-lookup"><span data-stu-id="99a4a-116">Pointer to the requested height in pixels, or **NULL**.</span></span> <span data-ttu-id="99a4a-117">Restituisce la dimensione corretta.</span><span class="sxs-lookup"><span data-stu-id="99a4a-117">Returns the corrected size.</span></span>

</dd> <dt>

<span data-ttu-id="99a4a-118">*pNumMipLevels* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="99a4a-118">*pNumMipLevels* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="99a4a-119">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="99a4a-119">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="99a4a-120">Puntatore al numero di livelli di mipmap richiesti o **null**.</span><span class="sxs-lookup"><span data-stu-id="99a4a-120">Pointer to number of requested mipmap levels, or **NULL**.</span></span> <span data-ttu-id="99a4a-121">Restituisce il numero corretto di livelli di mipmap.</span><span class="sxs-lookup"><span data-stu-id="99a4a-121">Returns the corrected number of mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="99a4a-122">*Utilizzo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="99a4a-122">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99a4a-123">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="99a4a-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="99a4a-124">0 o [**D3DUSAGE \_ RENDERTARGET**](d3dusage.md).</span><span class="sxs-lookup"><span data-stu-id="99a4a-124">0 or [**D3DUSAGE\_RENDERTARGET**](d3dusage.md).</span></span> <span data-ttu-id="99a4a-125">L'impostazione di questo flag su D3DUSAGE \_ RENDERTARGET indica che la superficie deve essere utilizzata come destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="99a4a-125">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="99a4a-126">La risorsa può quindi essere passata al parametro pNewRenderTarget del metodo [**SetRenderTarget**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="99a4a-126">The resource can then be passed to the pNewRenderTarget parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="99a4a-127">Se viene specificato **D3DUSAGE \_ RENDERTARGET** , l'applicazione deve verificare che il dispositivo supporti questa operazione chiamando [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat).</span><span class="sxs-lookup"><span data-stu-id="99a4a-127">If **D3DUSAGE\_RENDERTARGET** is specified, the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat).</span></span>

</dd> <dt>

<span data-ttu-id="99a4a-128">*pFormat* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="99a4a-128">*pFormat* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="99a4a-129">Tipo: **[D3DFORMAT](d3dformat.md)\***</span><span class="sxs-lookup"><span data-stu-id="99a4a-129">Type: **[D3DFORMAT](d3dformat.md)\***</span></span>

<span data-ttu-id="99a4a-130">Puntatore a un membro del tipo enumerato [D3DFORMAT](d3dformat.md) .</span><span class="sxs-lookup"><span data-stu-id="99a4a-130">Pointer to a member of the [D3DFORMAT](d3dformat.md) enumerated type.</span></span> <span data-ttu-id="99a4a-131">Specifica il formato pixel desiderato o **null**.</span><span class="sxs-lookup"><span data-stu-id="99a4a-131">Specifies the desired pixel format, or **NULL**.</span></span> <span data-ttu-id="99a4a-132">Restituisce il formato corretto.</span><span class="sxs-lookup"><span data-stu-id="99a4a-132">Returns the corrected format.</span></span>

</dd> <dt>

<span data-ttu-id="99a4a-133">*Pool* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="99a4a-133">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99a4a-134">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="99a4a-134">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="99a4a-135">Membro del tipo enumerato [**D3DPOOL**](./d3dpool.md) , che descrive la classe di memoria in cui deve essere posizionata la trama.</span><span class="sxs-lookup"><span data-stu-id="99a4a-135">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99a4a-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="99a4a-136">Return value</span></span>

<span data-ttu-id="99a4a-137">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="99a4a-137">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="99a4a-138">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="99a4a-138">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="99a4a-139">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="99a4a-139">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE.</span></span>

## <a name="remarks"></a><span data-ttu-id="99a4a-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="99a4a-140">Remarks</span></span>

<span data-ttu-id="99a4a-141">Se i parametri di questa funzione non sono validi, questa funzione restituisce parametri corretti.</span><span class="sxs-lookup"><span data-stu-id="99a4a-141">If parameters to this function are invalid, this function returns corrected parameters.</span></span>

<span data-ttu-id="99a4a-142">Questa funzione usa l'euristica seguente quando si confrontano i requisiti richiesti rispetto ai formati disponibili:</span><span class="sxs-lookup"><span data-stu-id="99a4a-142">This function uses the following heuristics when comparing the requested requirements against available formats:</span></span>

-   <span data-ttu-id="99a4a-143">Non scegliere un formato con un minor numero di canali.</span><span class="sxs-lookup"><span data-stu-id="99a4a-143">Do not choose a format that has fewer channels.</span></span>
-   <span data-ttu-id="99a4a-144">Evitare i formati [fourcc](d3dformat.md) e a 24 bit a meno che non vengano richiesti in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="99a4a-144">Avoid [FOURCC](d3dformat.md) And 24-bit formats unless explicitly requested.</span></span>
-   <span data-ttu-id="99a4a-145">Provare a non aggiungere nuovi canali.</span><span class="sxs-lookup"><span data-stu-id="99a4a-145">Try not to add new channels.</span></span>
-   <span data-ttu-id="99a4a-146">Provare a non modificare il numero di bit per canale.</span><span class="sxs-lookup"><span data-stu-id="99a4a-146">Try not to change the number of bits per channel.</span></span>
-   <span data-ttu-id="99a4a-147">Provare a evitare la conversione tra tipi di formati.</span><span class="sxs-lookup"><span data-stu-id="99a4a-147">Try to avoid converting between types of formats.</span></span> <span data-ttu-id="99a4a-148">Ad esempio, evitare di convertire un formato ARGB in un formato di profondità.</span><span class="sxs-lookup"><span data-stu-id="99a4a-148">For instance, avoid converting an ARGB format to a depth format.</span></span>

## <a name="requirements"></a><span data-ttu-id="99a4a-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="99a4a-149">Requirements</span></span>



| <span data-ttu-id="99a4a-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="99a4a-150">Requirement</span></span> | <span data-ttu-id="99a4a-151">Valore</span><span class="sxs-lookup"><span data-stu-id="99a4a-151">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="99a4a-152">Intestazione</span><span class="sxs-lookup"><span data-stu-id="99a4a-152">Header</span></span><br/>  | <dl> <span data-ttu-id="99a4a-153"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="99a4a-153"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="99a4a-154">Libreria</span><span class="sxs-lookup"><span data-stu-id="99a4a-154">Library</span></span><br/> | <dl> <span data-ttu-id="99a4a-155"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="99a4a-155"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="99a4a-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="99a4a-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99a4a-157">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="99a4a-157">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
