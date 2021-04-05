---
description: Crea una trama del volume da una risorsa specificata da una stringa. Si tratta di una funzione più avanzata rispetto a D3DXCreateVolumeTextureFromResource.
ms.assetid: 02f2cb9e-4750-4854-aa74-202426427af5
title: Funzione D3DXCreateVolumeTextureFromResourceEx (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTextureFromResourceEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 44d842df2da1d5c3db374e838e0ffd2492683961
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969358"
---
# <a name="d3dxcreatevolumetexturefromresourceex-function"></a><span data-ttu-id="8d5de-104">D3DXCreateVolumeTextureFromResourceEx (funzione)</span><span class="sxs-lookup"><span data-stu-id="8d5de-104">D3DXCreateVolumeTextureFromResourceEx function</span></span>

<span data-ttu-id="8d5de-105">Crea una trama del volume da una risorsa specificata da una stringa.</span><span class="sxs-lookup"><span data-stu-id="8d5de-105">Creates a volume texture from a resource specified by a string.</span></span> <span data-ttu-id="8d5de-106">Si tratta di una funzione più avanzata rispetto a [**D3DXCreateVolumeTextureFromResource**](d3dxcreatevolumetexturefromresource.md).</span><span class="sxs-lookup"><span data-stu-id="8d5de-106">This is a more advanced function than [**D3DXCreateVolumeTextureFromResource**](d3dxcreatevolumetexturefromresource.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8d5de-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8d5de-107">Syntax</span></span>


```C++
HRESULT D3DXCreateVolumeTextureFromResourceEx(
  _In_    LPDIRECT3DDEVICE9        pDevice,
  _In_    HMODULE                  hSrcModule,
  _In_    LPCTSTR                  pSrcResource,
  _In_    UINT                     Width,
  _In_    UINT                     Height,
  _In_    UINT                     Depth,
  _In_    UINT                     MipLevels,
  _In_    DWORD                    Usage,
  _In_    D3DFORMAT                Format,
  _In_    D3DPOOL                  Pool,
  _In_    DWORD                    Filter,
  _In_    DWORD                    MipFilter,
  _In_    D3DCOLOR                 ColorKey,
  _Inout_ D3DXIMAGE_INFO           *pSrcInfo,
  _Out_   PALETTEENTRY             *pPalette,
  _Out_   LPDIRECT3DVOLUMETEXTURE9 *ppVolumeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="8d5de-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8d5de-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d5de-109">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8d5de-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d5de-110">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="8d5de-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="8d5de-111">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo da associare alla trama.</span><span class="sxs-lookup"><span data-stu-id="8d5de-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="8d5de-112">*hSrcModule* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8d5de-112">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d5de-113">Tipo: **[ **hmodule**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8d5de-113">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8d5de-114">Handle per il modulo in cui si trova la risorsa o **null** per il modulo associato all'immagine utilizzata dal sistema operativo per creare il processo corrente.</span><span class="sxs-lookup"><span data-stu-id="8d5de-114">Handle to the module where the resource is located, or **NULL** for module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="8d5de-115">*pSrcResource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8d5de-115">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d5de-116">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8d5de-116">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8d5de-117">Puntatore a una stringa che specifica il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="8d5de-117">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="8d5de-118">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="8d5de-118">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="8d5de-119">In caso contrario, il tipo di dati String viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="8d5de-119">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="8d5de-120">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="8d5de-120">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="8d5de-121">*Larghezza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8d5de-121">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d5de-122">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8d5de-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8d5de-123">Larghezza in pixel.</span><span class="sxs-lookup"><span data-stu-id="8d5de-123">Width in pixels.</span></span> <span data-ttu-id="8d5de-124">Se questo valore è zero o D3DX \_ default, le dimensioni vengono ricavate dal file.</span><span class="sxs-lookup"><span data-stu-id="8d5de-124">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="8d5de-125">La dimensione massima supportata da un driver (per larghezza, altezza e profondità) si trova in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="8d5de-125">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="8d5de-126">*Altezza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8d5de-126">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d5de-127">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8d5de-127">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8d5de-128">Altezza, in pixel.</span><span class="sxs-lookup"><span data-stu-id="8d5de-128">Height, in pixels.</span></span> <span data-ttu-id="8d5de-129">Se questo valore è zero o D3DX \_ default, le dimensioni vengono ricavate dal file.</span><span class="sxs-lookup"><span data-stu-id="8d5de-129">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="8d5de-130">La dimensione massima supportata da un driver (per larghezza, altezza e profondità) si trova in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="8d5de-130">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="8d5de-131">*Profondità* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8d5de-131">*Depth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d5de-132">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8d5de-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8d5de-133">Profondità, in pixel.</span><span class="sxs-lookup"><span data-stu-id="8d5de-133">Depth, in pixels.</span></span> <span data-ttu-id="8d5de-134">Se questo valore è zero o D3DX \_ default, le dimensioni vengono ricavate dal file.</span><span class="sxs-lookup"><span data-stu-id="8d5de-134">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="8d5de-135">La dimensione massima supportata da un driver (per larghezza, altezza e profondità) si trova in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="8d5de-135">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="8d5de-136">*MipLevels* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8d5de-136">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d5de-137">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8d5de-137">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8d5de-138">Numero di livelli MIP richiesti.</span><span class="sxs-lookup"><span data-stu-id="8d5de-138">Number of mip levels requested.</span></span> <span data-ttu-id="8d5de-139">Se questo valore è zero o D3DX \_ default, viene creata una catena mipmap completa.</span><span class="sxs-lookup"><span data-stu-id="8d5de-139">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="8d5de-140">*Utilizzo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="8d5de-140">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d5de-141">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8d5de-141">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8d5de-142">0, D3DUSAGE \_ RENDERTARGET o D3DUSAGE \_ Dynamic.</span><span class="sxs-lookup"><span data-stu-id="8d5de-142">0, D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="8d5de-143">L'impostazione di questo flag su D3DUSAGE \_ RENDERTARGET indica che la superficie deve essere utilizzata come destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="8d5de-143">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="8d5de-144">La risorsa può quindi essere passata al parametro *pNewRenderTarget* del metodo [**SetRenderTarget**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="8d5de-144">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="8d5de-145">Se \_ viene specificato D3DUSAGE RENDERTARGET o D3DUSAGE \_ Dynamic, il *pool* deve essere impostato su D3DPOOL \_ default e l'applicazione deve verificare che il dispositivo supporti questa operazione chiamando [**CheckDeviceFormat**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="8d5de-145">If either D3DUSAGE\_RENDERTARGET or D3DUSAGE\_DYNAMIC is specified, *Pool* must be set to D3DPOOL\_DEFAULT, and the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="8d5de-146">D3DUSAGE \_ Dynamic indica che la superficie deve essere gestita dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="8d5de-146">D3DUSAGE\_DYNAMIC indicates that the surface should be handled dynamically.</span></span> <span data-ttu-id="8d5de-147">Per ulteriori informazioni sull'utilizzo di trame dinamiche, vedere [using Dynamic Textures](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="8d5de-147">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="8d5de-148">*Formato* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8d5de-148">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d5de-149">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="8d5de-149">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="8d5de-150">Membro del tipo enumerato [D3DFORMAT](d3dformat.md) , che descrive il formato pixel richiesto per la trama.</span><span class="sxs-lookup"><span data-stu-id="8d5de-150">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the texture.</span></span> <span data-ttu-id="8d5de-151">La trama restituita potrebbe avere un formato diverso da quello specificato dal *formato*.</span><span class="sxs-lookup"><span data-stu-id="8d5de-151">The returned texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="8d5de-152">Le applicazioni devono verificare il formato della trama restituita.</span><span class="sxs-lookup"><span data-stu-id="8d5de-152">Applications should check the format of the returned texture.</span></span> <span data-ttu-id="8d5de-153">Se [D3DFMT è \_ sconosciuto](other-d3dx-constants.md), il formato viene ricavato dal file.</span><span class="sxs-lookup"><span data-stu-id="8d5de-153">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="8d5de-154">Se D3DFMT \_ da \_ file, il formato viene considerato esattamente come si trova nel file e la chiamata avrà esito negativo se viola le funzionalità del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8d5de-154">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="8d5de-155">*Pool* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="8d5de-155">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d5de-156">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="8d5de-156">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="8d5de-157">Membro del tipo enumerato [**D3DPOOL**](./d3dpool.md) , che descrive la classe di memoria in cui deve essere posizionata la trama.</span><span class="sxs-lookup"><span data-stu-id="8d5de-157">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="8d5de-158">*Filtro* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="8d5de-158">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d5de-159">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8d5de-159">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8d5de-160">Combinazione di uno o più [ \_ filtri D3DX](d3dx-filter.md) che controllano il modo in cui l'immagine viene filtrata.</span><span class="sxs-lookup"><span data-stu-id="8d5de-160">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="8d5de-161">Specificare \_ il valore predefinito di D3DX per questo parametro equivale a specificare \_ il \_ \| \_ dithering del filtro D3DX del triangolo di filtro D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="8d5de-161">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="8d5de-162">*MipFilter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8d5de-162">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d5de-163">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8d5de-163">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8d5de-164">Combinazione di uno o più [ \_ filtri D3DX](d3dx-filter.md) che controllano il modo in cui l'immagine viene filtrata.</span><span class="sxs-lookup"><span data-stu-id="8d5de-164">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="8d5de-165">La specifica \_ di D3DX default per questo parametro equivale alla specifica della \_ casella di filtro D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="8d5de-165">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span>

</dd> <dt>

<span data-ttu-id="8d5de-166">*ColorKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8d5de-166">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d5de-167">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="8d5de-167">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="8d5de-168">Valore [**D3DCOLOR**](d3dcolor.md) da sostituire con nero trasparente oppure 0 per disabilitare il colorkey.</span><span class="sxs-lookup"><span data-stu-id="8d5de-168">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="8d5de-169">Si tratta sempre di un colore ARGB a 32 bit, indipendente dal formato di immagine di origine.</span><span class="sxs-lookup"><span data-stu-id="8d5de-169">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="8d5de-170">Alfa è significativo e in genere deve essere impostato su FF per le chiavi di colore opache.</span><span class="sxs-lookup"><span data-stu-id="8d5de-170">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="8d5de-171">Pertanto, per il nero opaco, il valore sarà uguale a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="8d5de-171">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="8d5de-172">*pSrcInfo* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="8d5de-172">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d5de-173">Tipo: **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="8d5de-173">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="8d5de-174">Puntatore a una struttura di [**\_ informazioni D3DXIMAGE**](d3dximage-info.md) da compilare con una descrizione dei dati nel file di immagine di origine o **null**.</span><span class="sxs-lookup"><span data-stu-id="8d5de-174">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled in with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8d5de-175">*pPalette* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8d5de-175">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d5de-176">Tipo: **[ **PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="8d5de-176">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="8d5de-177">Puntatore a una struttura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , che rappresenta una tavolozza dei colori 256 da compilare o **null**.</span><span class="sxs-lookup"><span data-stu-id="8d5de-177">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8d5de-178">*ppVolumeTexture* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8d5de-178">*ppVolumeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d5de-179">Tipo: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="8d5de-179">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span></span>

<span data-ttu-id="8d5de-180">Indirizzo di un puntatore a un'interfaccia [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) , che rappresenta l'oggetto trama creato.</span><span class="sxs-lookup"><span data-stu-id="8d5de-180">Address of a pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d5de-181">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8d5de-181">Return value</span></span>

<span data-ttu-id="8d5de-182">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8d5de-182">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8d5de-183">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8d5de-183">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8d5de-184">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="8d5de-184">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d5de-185">Commenti</span><span class="sxs-lookup"><span data-stu-id="8d5de-185">Remarks</span></span>

<span data-ttu-id="8d5de-186">L'impostazione del compilatore determina anche la versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="8d5de-186">The compiler setting also determines the function version.</span></span> <span data-ttu-id="8d5de-187">Se è definito Unicode, la chiamata di funzione viene risolta in D3DXCreateVolumeTextureFromResourceExW.</span><span class="sxs-lookup"><span data-stu-id="8d5de-187">If Unicode is defined, the function call resolves to D3DXCreateVolumeTextureFromResourceExW.</span></span> <span data-ttu-id="8d5de-188">In caso contrario, la chiamata di funzione viene risolta in D3DXCreateVolumeTextureFromResourceExA perché vengono utilizzate le stringhe ANSI.</span><span class="sxs-lookup"><span data-stu-id="8d5de-188">Otherwise, the function call resolves to D3DXCreateVolumeTextureFromResourceExA because ANSI strings are being used.</span></span>

<span data-ttu-id="8d5de-189">La risorsa da caricare deve essere una risorsa definita dall'applicazione (RT \_ RCDATA).</span><span class="sxs-lookup"><span data-stu-id="8d5de-189">The resource being loaded must be an application-defined resource (RT\_RCDATA).</span></span>

<span data-ttu-id="8d5de-190">Questa funzione supporta i formati di file seguenti:. bmp,. DDS,. DIB,. HDR,. jpg,. PFM,. png,. ppm e. tga.</span><span class="sxs-lookup"><span data-stu-id="8d5de-190">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="8d5de-191">Vedere [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="8d5de-191">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8d5de-192">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8d5de-192">Requirements</span></span>



| <span data-ttu-id="8d5de-193">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d5de-193">Requirement</span></span> | <span data-ttu-id="8d5de-194">Valore</span><span class="sxs-lookup"><span data-stu-id="8d5de-194">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8d5de-195">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8d5de-195">Header</span></span><br/>  | <dl> <span data-ttu-id="8d5de-196"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d5de-196"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="8d5de-197">Libreria</span><span class="sxs-lookup"><span data-stu-id="8d5de-197">Library</span></span><br/> | <dl> <span data-ttu-id="8d5de-198"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8d5de-198"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="8d5de-199">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8d5de-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d5de-200">**D3DXCreateVolumeTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="8d5de-200">**D3DXCreateVolumeTextureFromFile**</span></span>](d3dxcreatevolumetexturefromfile.md)
</dt> <dt>

[<span data-ttu-id="8d5de-201">**D3DXCreateVolumeTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="8d5de-201">**D3DXCreateVolumeTextureFromFileEx**</span></span>](d3dxcreatevolumetexturefromfileex.md)
</dt> <dt>

[<span data-ttu-id="8d5de-202">**D3DXCreateVolumeTextureFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="8d5de-202">**D3DXCreateVolumeTextureFromFileInMemory**</span></span>](d3dxcreatevolumetexturefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="8d5de-203">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="8d5de-203">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span></span>](d3dxcreatevolumetexturefromfileinmemoryex.md)
</dt> <dt>

[<span data-ttu-id="8d5de-204">**D3DXCreateVolumeTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="8d5de-204">**D3DXCreateVolumeTextureFromResource**</span></span>](d3dxcreatevolumetexturefromresource.md)
</dt> <dt>

[<span data-ttu-id="8d5de-205">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="8d5de-205">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
