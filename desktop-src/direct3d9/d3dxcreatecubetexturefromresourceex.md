---
description: Crea una trama del cubo da una risorsa specificata da una stringa. Si tratta di una funzione più avanzata rispetto a D3DXCreateCubeTextureFromResource.
ms.assetid: 4d263386-8270-4967-8ef5-e9ac69e502a5
title: Funzione D3DXCreateCubeTextureFromResourceEx (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromResourceEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4ed77556681e2ad43302b8608dc213b3ad0f0209
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355674"
---
# <a name="d3dxcreatecubetexturefromresourceex-function"></a><span data-ttu-id="5634d-104">D3DXCreateCubeTextureFromResourceEx (funzione)</span><span class="sxs-lookup"><span data-stu-id="5634d-104">D3DXCreateCubeTextureFromResourceEx function</span></span>

<span data-ttu-id="5634d-105">Crea una trama del cubo da una risorsa specificata da una stringa.</span><span class="sxs-lookup"><span data-stu-id="5634d-105">Creates a cube texture from a resource specified by a string.</span></span> <span data-ttu-id="5634d-106">Si tratta di una funzione più avanzata rispetto a [**D3DXCreateCubeTextureFromResource**](d3dxcreatecubetexturefromresource.md).</span><span class="sxs-lookup"><span data-stu-id="5634d-106">This is a more advanced function than [**D3DXCreateCubeTextureFromResource**](d3dxcreatecubetexturefromresource.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5634d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5634d-107">Syntax</span></span>


```C++
HRESULT D3DXCreateCubeTextureFromResourceEx(
  _In_    LPDIRECT3DDEVICE9      pDevice,
  _In_    HMODULE                hSrcModule,
  _In_    LPCTSTR                pSrcResource,
  _In_    UINT                   Size,
  _In_    UINT                   MipLevels,
  _In_    DWORD                  Usage,
  _In_    D3DFORMAT              Format,
  _In_    D3DPOOL                Pool,
  _In_    DWORD                  Filter,
  _In_    DWORD                  MipFilter,
  _In_    D3DCOLOR               ColorKey,
  _Inout_ D3DXIMAGE_INFO         *pSrcInfo,
  _Out_   PALETTEENTRY           *pPalette,
  _Out_   LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="5634d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5634d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5634d-109">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5634d-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5634d-110">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="5634d-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="5634d-111">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo da associare alla trama del cubo.</span><span class="sxs-lookup"><span data-stu-id="5634d-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="5634d-112">*hSrcModule* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5634d-112">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5634d-113">Tipo: **[ **hmodule**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5634d-113">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5634d-114">Handle per il modulo in cui si trova la risorsa o **null** per il modulo associato all'immagine utilizzata dal sistema operativo per creare il processo corrente.</span><span class="sxs-lookup"><span data-stu-id="5634d-114">Handle to the module where the resource is located, or **NULL** for the module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="5634d-115">*pSrcResource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5634d-115">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5634d-116">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5634d-116">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5634d-117">Puntatore a una stringa che specifica il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="5634d-117">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="5634d-118">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="5634d-118">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="5634d-119">In caso contrario, il tipo di dati String viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="5634d-119">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="5634d-120">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="5634d-120">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="5634d-121">*Dimensioni* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5634d-121">*Size* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5634d-122">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5634d-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5634d-123">Larghezza e altezza della trama del cubo, in pixel.</span><span class="sxs-lookup"><span data-stu-id="5634d-123">Width and height of the cube texture, in pixels.</span></span> <span data-ttu-id="5634d-124">Se, ad esempio, la trama del cubo è un cubo da 8 pixel a 8 pixel, il valore di questo parametro deve essere 8.</span><span class="sxs-lookup"><span data-stu-id="5634d-124">For example, if the cube texture is an 8-pixel by 8-pixel cube, the value for this parameter should be 8.</span></span> <span data-ttu-id="5634d-125">Se questo valore è 0 o D3DX \_ predefinito, le dimensioni vengono ricavate dal file.</span><span class="sxs-lookup"><span data-stu-id="5634d-125">If this value is 0 or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span>

</dd> <dt>

<span data-ttu-id="5634d-126">*MipLevels* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5634d-126">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5634d-127">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5634d-127">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5634d-128">Numero di livelli MIP richiesti.</span><span class="sxs-lookup"><span data-stu-id="5634d-128">Number of mip levels requested.</span></span> <span data-ttu-id="5634d-129">Se questo valore è zero o D3DX \_ default, viene creata una catena mipmap completa.</span><span class="sxs-lookup"><span data-stu-id="5634d-129">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="5634d-130">*Utilizzo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="5634d-130">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5634d-131">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5634d-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5634d-132">0 o D3DUSAGE \_ RENDERTARGET o D3DUSAGE \_ Dynamic.</span><span class="sxs-lookup"><span data-stu-id="5634d-132">0 or D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="5634d-133">L'impostazione di questo flag su D3DUSAGE \_ RENDERTARGET indica che la superficie deve essere utilizzata come destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="5634d-133">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="5634d-134">La risorsa può quindi essere passata al parametro *pNewRenderTarget* del metodo [**SetRenderTarget**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="5634d-134">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="5634d-135">Se \_ viene specificato D3DUSAGE RENDERTARGET, l'applicazione deve verificare che il dispositivo supporti questa operazione chiamando [**CheckDeviceFormat**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="5634d-135">If D3DUSAGE\_RENDERTARGET is specified, the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="5634d-136">D3DUSAGE \_ Dynamic indica che la superficie deve essere gestita dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="5634d-136">D3DUSAGE\_DYNAMIC indicates that the surface should be handled dynamically.</span></span> <span data-ttu-id="5634d-137">Per ulteriori informazioni sull'utilizzo di trame dinamiche, vedere [using Dynamic Textures](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="5634d-137">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="5634d-138">*Formato* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5634d-138">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5634d-139">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="5634d-139">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="5634d-140">Membro del tipo enumerato [D3DFORMAT](d3dformat.md) , che descrive il formato pixel richiesto per la trama del cubo.</span><span class="sxs-lookup"><span data-stu-id="5634d-140">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the cube texture.</span></span> <span data-ttu-id="5634d-141">La trama del cubo restituita potrebbe avere un formato diverso da quello specificato dal *formato*.</span><span class="sxs-lookup"><span data-stu-id="5634d-141">The returned cube texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="5634d-142">Le applicazioni devono controllare il formato della trama del cubo restituita.</span><span class="sxs-lookup"><span data-stu-id="5634d-142">Applications should check the format of the returned cube texture.</span></span> <span data-ttu-id="5634d-143">Se [D3DFMT è \_ sconosciuto](other-d3dx-constants.md), il formato viene ricavato dal file.</span><span class="sxs-lookup"><span data-stu-id="5634d-143">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="5634d-144">Se D3DFMT \_ da \_ file, il formato viene considerato esattamente come si trova nel file e la chiamata avrà esito negativo se viola le funzionalità del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5634d-144">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="5634d-145">*Pool* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="5634d-145">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5634d-146">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="5634d-146">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="5634d-147">Membro del tipo enumerato [**D3DPOOL**](./d3dpool.md) , che descrive la classe di memoria in cui deve essere inserita la trama del cubo.</span><span class="sxs-lookup"><span data-stu-id="5634d-147">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the cube texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="5634d-148">*Filtro* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="5634d-148">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5634d-149">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5634d-149">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5634d-150">Combinazione di uno o più [ \_ filtri D3DX](d3dx-filter.md), che controllano il modo in cui l'immagine viene filtrata.</span><span class="sxs-lookup"><span data-stu-id="5634d-150">A combination of one or more [D3DX\_FILTER](d3dx-filter.md), controlling how the image is filtered.</span></span> <span data-ttu-id="5634d-151">Specificare \_ il valore predefinito di D3DX per questo parametro equivale a specificare \_ il \_ \| \_ dithering del filtro D3DX del triangolo di filtro D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="5634d-151">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="5634d-152">*MipFilter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5634d-152">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5634d-153">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5634d-153">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5634d-154">Combinazione di uno o più [ \_ filtri D3DX](d3dx-filter.md) che controllano il modo in cui l'immagine viene filtrata.</span><span class="sxs-lookup"><span data-stu-id="5634d-154">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="5634d-155">La specifica \_ di D3DX default per questo parametro equivale alla specifica della \_ casella di filtro D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="5634d-155">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span>

</dd> <dt>

<span data-ttu-id="5634d-156">*ColorKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5634d-156">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5634d-157">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="5634d-157">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="5634d-158">Valore [**D3DCOLOR**](d3dcolor.md) da sostituire con nero trasparente oppure 0 per disabilitare il colorkey.</span><span class="sxs-lookup"><span data-stu-id="5634d-158">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="5634d-159">Si tratta sempre di un colore ARGB a 32 bit, indipendente dal formato di immagine di origine.</span><span class="sxs-lookup"><span data-stu-id="5634d-159">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="5634d-160">Alfa è significativo e in genere deve essere impostato su FF per le chiavi di colore opache.</span><span class="sxs-lookup"><span data-stu-id="5634d-160">Alpha is significant, and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="5634d-161">Pertanto, per il nero opaco, il valore sarà uguale a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="5634d-161">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="5634d-162">*pSrcInfo* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="5634d-162">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5634d-163">Tipo: **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="5634d-163">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="5634d-164">Puntatore a una struttura di [**\_ informazioni D3DXIMAGE**](d3dximage-info.md) per la compilazione di una descrizione dei dati nel file di immagine di origine o **null**.</span><span class="sxs-lookup"><span data-stu-id="5634d-164">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5634d-165">*pPalette* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5634d-165">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5634d-166">Tipo: **[ **PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="5634d-166">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="5634d-167">Puntatore a una struttura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) che rappresenta una tavolozza dei colori 256 da compilare o **null**.</span><span class="sxs-lookup"><span data-stu-id="5634d-167">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5634d-168">*ppCubeTexture* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5634d-168">*ppCubeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5634d-169">Tipo: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="5634d-169">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span></span>

<span data-ttu-id="5634d-170">Indirizzo di un puntatore a un'interfaccia [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) , che rappresenta l'oggetto trama del cubo creato.</span><span class="sxs-lookup"><span data-stu-id="5634d-170">Address of a pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the created cube texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5634d-171">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5634d-171">Return value</span></span>

<span data-ttu-id="5634d-172">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5634d-172">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5634d-173">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5634d-173">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5634d-174">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="5634d-174">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="5634d-175">Commenti</span><span class="sxs-lookup"><span data-stu-id="5634d-175">Remarks</span></span>

<span data-ttu-id="5634d-176">L'impostazione del compilatore determina la versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="5634d-176">The compiler setting determines the function version.</span></span> <span data-ttu-id="5634d-177">Se è definito Unicode, la chiamata di funzione viene risolta in **D3DXCreateCubeTextureFromResourceExW**.</span><span class="sxs-lookup"><span data-stu-id="5634d-177">If Unicode is defined, the function call resolves to **D3DXCreateCubeTextureFromResourceExW**.</span></span> <span data-ttu-id="5634d-178">In caso contrario, la chiamata di funzione viene risolta in **D3DXCreateCubeTextureFromResourceExA** perché vengono utilizzate le stringhe ANSI.</span><span class="sxs-lookup"><span data-stu-id="5634d-178">Otherwise, the function call resolves to **D3DXCreateCubeTextureFromResourceExA** because ANSI strings are being used.</span></span>

<span data-ttu-id="5634d-179">Questa funzione supporta i formati di file seguenti:. bmp,. DDS,. DIB,. HDR,. jpg,. PFM,. png,. ppm e. tga.</span><span class="sxs-lookup"><span data-stu-id="5634d-179">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="5634d-180">Vedere [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="5634d-180">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="5634d-181">Le trame del cubo differiscono dalle altre superfici perché sono raccolte di superfici.</span><span class="sxs-lookup"><span data-stu-id="5634d-181">Cube textures differ from other surfaces in that they are collections of surfaces.</span></span> <span data-ttu-id="5634d-182">Per chiamare [**SetRenderTarget**](/windows/desktop/api) con una trama del cubo, è necessario selezionare un singolo volto usando [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) e passare la superficie risultante a **SetRenderTarget**.</span><span class="sxs-lookup"><span data-stu-id="5634d-182">To call [**SetRenderTarget**](/windows/desktop/api) with a cube texture, you must select an individual face using [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) and pass the resulting surface to **SetRenderTarget**.</span></span>

<span data-ttu-id="5634d-183">**D3DXCreateCubeTextureFromResourceEx** usa il formato di file DirectDraw Surface (DDS).</span><span class="sxs-lookup"><span data-stu-id="5634d-183">**D3DXCreateCubeTextureFromResourceEx** uses the DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="5634d-184">L'editor di trame DirectX (Dxtex.exe) consente di generare una mappa del cubo da altri formati di file e di salvarli nel formato di file DDS.</span><span class="sxs-lookup"><span data-stu-id="5634d-184">The DirectX Texture Editor (Dxtex.exe) enables you to generate a cube map from other file formats and save it in the DDS file format.</span></span> <span data-ttu-id="5634d-185">È possibile ottenere Dxtex.exe e ottenere informazioni su di esso da DirectX SDK.</span><span class="sxs-lookup"><span data-stu-id="5634d-185">You can get Dxtex.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="5634d-186">Per informazioni su DirectX SDK, vedere [dove è DirectX SDK?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="5634d-186">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5634d-187">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5634d-187">Requirements</span></span>



| <span data-ttu-id="5634d-188">Requisito</span><span class="sxs-lookup"><span data-stu-id="5634d-188">Requirement</span></span> | <span data-ttu-id="5634d-189">Valore</span><span class="sxs-lookup"><span data-stu-id="5634d-189">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5634d-190">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5634d-190">Header</span></span><br/>  | <dl> <span data-ttu-id="5634d-191"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="5634d-191"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="5634d-192">Libreria</span><span class="sxs-lookup"><span data-stu-id="5634d-192">Library</span></span><br/> | <dl> <span data-ttu-id="5634d-193"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5634d-193"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="5634d-194">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5634d-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5634d-195">**D3DXCreateCubeTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="5634d-195">**D3DXCreateCubeTextureFromResource**</span></span>](d3dxcreatecubetexturefromresource.md)
</dt> <dt>

[<span data-ttu-id="5634d-196">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="5634d-196">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
