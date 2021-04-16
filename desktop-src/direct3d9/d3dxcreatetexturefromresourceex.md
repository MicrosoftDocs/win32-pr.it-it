---
description: Crea una trama da una risorsa. Si tratta di una funzione più avanzata rispetto a D3DXCreateTextureFromResource.
ms.assetid: 6015e2fa-9deb-4e6a-a401-f10fb05f40b7
title: Funzione D3DXCreateTextureFromResourceEx (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromResourceEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 26298f8a63ccfde2171578c27e9208011c16dd28
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530913"
---
# <a name="d3dxcreatetexturefromresourceex-function"></a><span data-ttu-id="9fa58-104">D3DXCreateTextureFromResourceEx (funzione)</span><span class="sxs-lookup"><span data-stu-id="9fa58-104">D3DXCreateTextureFromResourceEx function</span></span>

<span data-ttu-id="9fa58-105">Crea una trama da una risorsa.</span><span class="sxs-lookup"><span data-stu-id="9fa58-105">Creates a texture from a resource.</span></span> <span data-ttu-id="9fa58-106">Si tratta di una funzione più avanzata rispetto a [**D3DXCreateTextureFromResource**](d3dxcreatetexturefromresource.md).</span><span class="sxs-lookup"><span data-stu-id="9fa58-106">This is a more advanced function than [**D3DXCreateTextureFromResource**](d3dxcreatetexturefromresource.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9fa58-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9fa58-107">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureFromResourceEx(
  _In_    LPDIRECT3DDEVICE9  pDevice,
  _In_    HMODULE            hSrcModule,
  _In_    LPCTSTR            pSrcResource,
  _In_    UINT               Width,
  _In_    UINT               Height,
  _In_    UINT               MipLevels,
  _In_    DWORD              Usage,
  _In_    D3DFORMAT          Format,
  _In_    D3DPOOL            Pool,
  _In_    DWORD              Filter,
  _In_    DWORD              MipFilter,
  _In_    D3DCOLOR           ColorKey,
  _Inout_ D3DXIMAGE_INFO     *pSrcInfo,
  _Out_   PALETTEENTRY       *pPalette,
  _Out_   LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a><span data-ttu-id="9fa58-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9fa58-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fa58-109">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9fa58-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fa58-110">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="9fa58-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="9fa58-111">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo da associare alla trama.</span><span class="sxs-lookup"><span data-stu-id="9fa58-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="9fa58-112">*hSrcModule* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9fa58-112">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fa58-113">Tipo: **[ **hmodule**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9fa58-113">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9fa58-114">Handle per il modulo in cui si trova la risorsa o **null** per il modulo associato all'immagine utilizzata dal sistema operativo per creare il processo corrente.</span><span class="sxs-lookup"><span data-stu-id="9fa58-114">Handle to the module where the resource is located, or **NULL** for module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="9fa58-115">*pSrcResource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9fa58-115">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fa58-116">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9fa58-116">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9fa58-117">Puntatore a una stringa che specifica il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="9fa58-117">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="9fa58-118">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="9fa58-118">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="9fa58-119">In caso contrario, il tipo di dati String viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="9fa58-119">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="9fa58-120">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="9fa58-120">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="9fa58-121">*Larghezza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9fa58-121">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fa58-122">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9fa58-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9fa58-123">Larghezza in pixel.</span><span class="sxs-lookup"><span data-stu-id="9fa58-123">Width in pixels.</span></span> <span data-ttu-id="9fa58-124">Se questo valore è zero o D3DX \_ default, le dimensioni vengono ricavate dal file.</span><span class="sxs-lookup"><span data-stu-id="9fa58-124">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span>

</dd> <dt>

<span data-ttu-id="9fa58-125">*Altezza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9fa58-125">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fa58-126">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9fa58-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9fa58-127">Altezza, in pixel.</span><span class="sxs-lookup"><span data-stu-id="9fa58-127">Height, in pixels.</span></span> <span data-ttu-id="9fa58-128">Se questo valore è zero o D3DX \_ default, le dimensioni vengono ricavate dal file.</span><span class="sxs-lookup"><span data-stu-id="9fa58-128">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span>

</dd> <dt>

<span data-ttu-id="9fa58-129">*MipLevels* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9fa58-129">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fa58-130">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9fa58-130">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9fa58-131">Numero di livelli MIP richiesti.</span><span class="sxs-lookup"><span data-stu-id="9fa58-131">Number of mip levels requested.</span></span> <span data-ttu-id="9fa58-132">Se questo valore è zero o D3DX \_ default, viene creata una catena mipmap completa.</span><span class="sxs-lookup"><span data-stu-id="9fa58-132">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="9fa58-133">*Utilizzo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="9fa58-133">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fa58-134">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9fa58-134">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9fa58-135">0, D3DUSAGE \_ RENDERTARGET o D3DUSAGE \_ Dynamic.</span><span class="sxs-lookup"><span data-stu-id="9fa58-135">0, D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="9fa58-136">L'impostazione di questo flag su D3DUSAGE \_ RENDERTARGET indica che la superficie deve essere utilizzata come destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="9fa58-136">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="9fa58-137">La risorsa può quindi essere passata al parametro *pNewRenderTarget* del metodo [**SetRenderTarget**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="9fa58-137">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="9fa58-138">Se \_ viene specificato D3DUSAGE RENDERTARGET o D3DUSAGE, il *pool* deve essere impostato su D3DPOOL \_ default e l'applicazione deve verificare che il dispositivo supporti questa operazione chiamando [**CheckDeviceFormat**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="9fa58-138">If either D3DUSAGE\_RENDERTARGET or D3DUSAGE is specified, *Pool* must be set to D3DPOOL\_DEFAULT, and the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="9fa58-139">D3DUSAGE \_ Dynamic indica che la superficie deve essere gestita dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="9fa58-139">D3DUSAGE\_DYNAMIC indicates that the surface should be handled dynamically.</span></span> <span data-ttu-id="9fa58-140">Per altre informazioni sull'uso delle trame dinamiche, vedere [ottimizzazioni delle prestazioni (Direct3D 9)](performance-optimizations.md)usando trame dinamiche.</span><span class="sxs-lookup"><span data-stu-id="9fa58-140">For more information about using dynamic textures, see [Performance Optimizations (Direct3D 9)](performance-optimizations.md)Using Dynamic Textures.</span></span>

</dd> <dt>

<span data-ttu-id="9fa58-141">*Formato* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9fa58-141">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fa58-142">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="9fa58-142">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="9fa58-143">Membro del tipo enumerato [D3DFORMAT](d3dformat.md) , che descrive il formato pixel richiesto per la trama.</span><span class="sxs-lookup"><span data-stu-id="9fa58-143">A member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the texture.</span></span> <span data-ttu-id="9fa58-144">La trama restituita potrebbe avere un formato diverso da quello specificato dal *formato*.</span><span class="sxs-lookup"><span data-stu-id="9fa58-144">The returned texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="9fa58-145">Le applicazioni devono verificare il formato della trama restituita.</span><span class="sxs-lookup"><span data-stu-id="9fa58-145">Applications should check the format of the returned texture.</span></span> <span data-ttu-id="9fa58-146">Se [D3DFMT è \_ sconosciuto](other-d3dx-constants.md), il formato viene ricavato dal file.</span><span class="sxs-lookup"><span data-stu-id="9fa58-146">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="9fa58-147">Se D3DFMT \_ da \_ file, il formato viene considerato esattamente come si trova nel file e la chiamata avrà esito negativo se viola le funzionalità del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9fa58-147">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="9fa58-148">*Pool* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="9fa58-148">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fa58-149">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="9fa58-149">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="9fa58-150">Membro del tipo enumerato [**D3DPOOL**](./d3dpool.md) , che descrive la classe di memoria in cui deve essere posizionata la trama.</span><span class="sxs-lookup"><span data-stu-id="9fa58-150">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="9fa58-151">*Filtro* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="9fa58-151">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fa58-152">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9fa58-152">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9fa58-153">Combinazione di uno o più [ \_ filtri D3DX](d3dx-filter.md) che controllano il modo in cui l'immagine viene filtrata.</span><span class="sxs-lookup"><span data-stu-id="9fa58-153">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="9fa58-154">Specificare \_ il valore predefinito di D3DX per questo parametro equivale a specificare \_ il \_ \| \_ dithering del filtro D3DX del triangolo di filtro D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="9fa58-154">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="9fa58-155">*MipFilter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9fa58-155">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fa58-156">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9fa58-156">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9fa58-157">Combinazione di uno o più [ \_ filtri D3DX](d3dx-filter.md) che controllano il modo in cui l'immagine viene filtrata.</span><span class="sxs-lookup"><span data-stu-id="9fa58-157">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="9fa58-158">La specifica \_ di D3DX default per questo parametro equivale alla specifica della \_ casella di filtro D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="9fa58-158">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span>

</dd> <dt>

<span data-ttu-id="9fa58-159">*ColorKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9fa58-159">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fa58-160">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="9fa58-160">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="9fa58-161">Valore [**D3DCOLOR**](d3dcolor.md) da sostituire con nero trasparente oppure 0 per disabilitare il colorkey.</span><span class="sxs-lookup"><span data-stu-id="9fa58-161">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="9fa58-162">Si tratta sempre di un colore ARGB a 32 bit, indipendente dal formato di immagine di origine.</span><span class="sxs-lookup"><span data-stu-id="9fa58-162">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="9fa58-163">Alfa è significativo e in genere deve essere impostato su FF per le chiavi di colore opache.</span><span class="sxs-lookup"><span data-stu-id="9fa58-163">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="9fa58-164">Pertanto, per il nero opaco, il valore sarà uguale a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="9fa58-164">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="9fa58-165">*pSrcInfo* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="9fa58-165">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9fa58-166">Tipo: **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="9fa58-166">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="9fa58-167">Puntatore a una struttura di [**\_ informazioni D3DXIMAGE**](d3dximage-info.md) per la compilazione di una descrizione dei dati nel file di immagine di origine o **null**.</span><span class="sxs-lookup"><span data-stu-id="9fa58-167">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9fa58-168">*pPalette* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9fa58-168">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9fa58-169">Tipo: **[ **PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="9fa58-169">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="9fa58-170">Puntatore a una struttura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) che rappresenta una tavolozza dei colori 256 da compilare o **null**.</span><span class="sxs-lookup"><span data-stu-id="9fa58-170">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9fa58-171">*ppTexture* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9fa58-171">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9fa58-172">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="9fa58-172">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="9fa58-173">Indirizzo di un puntatore a un'interfaccia [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , che rappresenta l'oggetto trama creato.</span><span class="sxs-lookup"><span data-stu-id="9fa58-173">Address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fa58-174">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9fa58-174">Return value</span></span>

<span data-ttu-id="9fa58-175">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9fa58-175">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9fa58-176">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9fa58-176">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9fa58-177">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="9fa58-177">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fa58-178">Commenti</span><span class="sxs-lookup"><span data-stu-id="9fa58-178">Remarks</span></span>

<span data-ttu-id="9fa58-179">L'impostazione del compilatore determina anche la versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="9fa58-179">The compiler setting also determines the function version.</span></span> <span data-ttu-id="9fa58-180">Se è definito Unicode, la chiamata di funzione viene risolta in D3DXCreateTextureFromResourceExW.</span><span class="sxs-lookup"><span data-stu-id="9fa58-180">If Unicode is defined, the function call resolves to D3DXCreateTextureFromResourceExW.</span></span> <span data-ttu-id="9fa58-181">In caso contrario, la chiamata di funzione viene risolta in D3DXCreateTextureFromResourceExA perché vengono utilizzate le stringhe ANSI.</span><span class="sxs-lookup"><span data-stu-id="9fa58-181">Otherwise, the function call resolves to D3DXCreateTextureFromResourceExA because ANSI strings are being used.</span></span>

<span data-ttu-id="9fa58-182">La risorsa da caricare deve essere di tipo RT \_ bitmap o RT \_ RCDATA.</span><span class="sxs-lookup"><span data-stu-id="9fa58-182">The resource being loaded must be of type RT\_BITMAP or RT\_RCDATA.</span></span> <span data-ttu-id="9fa58-183">Il tipo di risorsa RT \_ RCDATA viene usato per caricare formati diversi da bitmap, ad esempio. tga,. jpg e. DDS.</span><span class="sxs-lookup"><span data-stu-id="9fa58-183">Resource type RT\_RCDATA is used to load formats other than bitmaps (such as .tga, .jpg, and .dds).</span></span>

<span data-ttu-id="9fa58-184">Questa funzione supporta i formati di file seguenti:. bmp,. DDS,. DIB,. HDR,. jpg,. PFM,. png,. ppm e. tga.</span><span class="sxs-lookup"><span data-stu-id="9fa58-184">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="9fa58-185">Vedere [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="9fa58-185">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9fa58-186">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9fa58-186">Requirements</span></span>



| <span data-ttu-id="9fa58-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fa58-187">Requirement</span></span> | <span data-ttu-id="9fa58-188">Valore</span><span class="sxs-lookup"><span data-stu-id="9fa58-188">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9fa58-189">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9fa58-189">Header</span></span><br/>  | <dl> <span data-ttu-id="9fa58-190"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="9fa58-190"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="9fa58-191">Libreria</span><span class="sxs-lookup"><span data-stu-id="9fa58-191">Library</span></span><br/> | <dl> <span data-ttu-id="9fa58-192"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9fa58-192"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="9fa58-193">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9fa58-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fa58-194">**D3DXCreateTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="9fa58-194">**D3DXCreateTextureFromResource**</span></span>](d3dxcreatetexturefromresource.md)
</dt> <dt>

[<span data-ttu-id="9fa58-195">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="9fa58-195">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
