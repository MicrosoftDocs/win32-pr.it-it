---
description: Crea una trama del volume da un file.
ms.assetid: fa11706a-83cc-4795-957d-6d0e1faf2a8f
title: Funzione D3DXCreateVolumeTextureFromFileEx (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTextureFromFileEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4d63377394dc123defac565cd11a0d40324a28a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354899"
---
# <a name="d3dxcreatevolumetexturefromfileex-function"></a><span data-ttu-id="ce999-103">D3DXCreateVolumeTextureFromFileEx (funzione)</span><span class="sxs-lookup"><span data-stu-id="ce999-103">D3DXCreateVolumeTextureFromFileEx function</span></span>

<span data-ttu-id="ce999-104">Crea una trama del volume da un file.</span><span class="sxs-lookup"><span data-stu-id="ce999-104">Creates a volume texture from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce999-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ce999-105">Syntax</span></span>


```C++
HRESULT D3DXCreateVolumeTextureFromFileEx(
  _In_    LPDIRECT3DDEVICE9        pDevice,
  _In_    LPCTSTR                  pSrcFile,
  _In_    UINT                     Width,
  _In_    UINT                     Height,
  _In_    UINT                     Depth,
  _In_    UINT                     MipLevels,
  _In_    DWORD                    Usage,
          D3DFORMAT                Format,
  _In_    D3DPOOL                  Pool,
  _In_    DWORD                    Filter,
  _In_    DWORD                    MipFilter,
  _In_    D3DCOLOR                 ColorKey,
  _Inout_ D3DXIMAGE_INFO           *pSrcInfo,
  _Out_   PALETTEENTRY             *pPalette,
  _Out_   LPDIRECT3DVOLUMETEXTURE9 *ppTexture
);
```



## <a name="parameters"></a><span data-ttu-id="ce999-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ce999-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce999-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ce999-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce999-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="ce999-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="ce999-109">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo da associare alla trama.</span><span class="sxs-lookup"><span data-stu-id="ce999-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="ce999-110">*pSrcFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ce999-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce999-111">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ce999-111">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ce999-112">Puntatore a una stringa che specifica il nome del file.</span><span class="sxs-lookup"><span data-stu-id="ce999-112">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="ce999-113">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="ce999-113">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="ce999-114">In caso contrario, il tipo di dati String viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="ce999-114">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="ce999-115">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="ce999-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ce999-116">*Larghezza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ce999-116">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce999-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ce999-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ce999-118">Larghezza in pixel.</span><span class="sxs-lookup"><span data-stu-id="ce999-118">Width in pixels.</span></span> <span data-ttu-id="ce999-119">Se questo valore è zero o D3DX \_ default, le dimensioni vengono ricavate dal file.</span><span class="sxs-lookup"><span data-stu-id="ce999-119">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="ce999-120">La dimensione massima supportata da un driver (per larghezza, altezza e profondità) si trova in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="ce999-120">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="ce999-121">*Altezza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ce999-121">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce999-122">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ce999-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ce999-123">Altezza, in pixel.</span><span class="sxs-lookup"><span data-stu-id="ce999-123">Height, in pixels.</span></span> <span data-ttu-id="ce999-124">Se questo valore è zero o D3DX \_ default, le dimensioni vengono ricavate dal file.</span><span class="sxs-lookup"><span data-stu-id="ce999-124">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="ce999-125">La dimensione massima supportata da un driver (per larghezza, altezza e profondità) si trova in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="ce999-125">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="ce999-126">*Profondità* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ce999-126">*Depth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce999-127">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ce999-127">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ce999-128">Profondità, in pixel.</span><span class="sxs-lookup"><span data-stu-id="ce999-128">Depth, in pixels.</span></span> <span data-ttu-id="ce999-129">Se questo valore è zero o D3DX \_ default, le dimensioni vengono ricavate dal file.</span><span class="sxs-lookup"><span data-stu-id="ce999-129">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="ce999-130">La dimensione massima supportata da un driver (per larghezza, altezza e profondità) si trova in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="ce999-130">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="ce999-131">*MipLevels* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ce999-131">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce999-132">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ce999-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ce999-133">Numero di livelli MIP richiesti.</span><span class="sxs-lookup"><span data-stu-id="ce999-133">Number of mip levels requested.</span></span> <span data-ttu-id="ce999-134">Se questo valore è zero o D3DX \_ default, viene creata una catena mipmap completa.</span><span class="sxs-lookup"><span data-stu-id="ce999-134">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="ce999-135">*Utilizzo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="ce999-135">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce999-136">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ce999-136">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ce999-137">0, D3DUSAGE \_ RENDERTARGET o D3DUSAGE \_ Dynamic.</span><span class="sxs-lookup"><span data-stu-id="ce999-137">0, D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="ce999-138">L'impostazione di questo flag su D3DUSAGE \_ RENDERTARGET indica che la superficie deve essere utilizzata come destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="ce999-138">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="ce999-139">La risorsa può quindi essere passata al parametro *pNewRenderTarget* del metodo [**SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) .</span><span class="sxs-lookup"><span data-stu-id="ce999-139">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) method.</span></span> <span data-ttu-id="ce999-140">Se \_ viene specificato D3DUSAGE RENDERTARGET o D3DUSAGE \_ Dynamic, il *pool* deve essere impostato su D3DPOOL \_ default e l'applicazione deve verificare che il dispositivo supporti questa operazione chiamando [**CheckDeviceFormat**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="ce999-140">If either D3DUSAGE\_RENDERTARGET or D3DUSAGE\_DYNAMIC is specified, *Pool* must be set to D3DPOOL\_DEFAULT, and the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="ce999-141">D3DUSAGE \_ Dynamic indica che la superficie deve essere gestita dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="ce999-141">D3DUSAGE\_DYNAMIC indicates that the surface should be handled dynamically.</span></span> <span data-ttu-id="ce999-142">Per ulteriori informazioni sull'utilizzo di trame dinamiche, vedere [using Dynamic Textures](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="ce999-142">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce999-143">*Formato*</span><span class="sxs-lookup"><span data-stu-id="ce999-143">*Format*</span></span> 
</dt> <dd>

<span data-ttu-id="ce999-144">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="ce999-144">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="ce999-145">Membro del tipo enumerato [D3DFORMAT](d3dformat.md) , che descrive il formato pixel richiesto per la trama.</span><span class="sxs-lookup"><span data-stu-id="ce999-145">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the texture.</span></span> <span data-ttu-id="ce999-146">La trama restituita potrebbe avere un formato diverso da quello specificato dal *formato*.</span><span class="sxs-lookup"><span data-stu-id="ce999-146">The returned texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="ce999-147">Le applicazioni devono verificare il formato della trama restituita.</span><span class="sxs-lookup"><span data-stu-id="ce999-147">Applications should check the format of the returned texture.</span></span> <span data-ttu-id="ce999-148">Se [D3DFMT è \_ sconosciuto](other-d3dx-constants.md), il formato viene ricavato dal file.</span><span class="sxs-lookup"><span data-stu-id="ce999-148">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="ce999-149">Se D3DFMT \_ da \_ file, il formato viene considerato esattamente come si trova nel file e la chiamata avrà esito negativo se viola le funzionalità del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ce999-149">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="ce999-150">*Pool* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="ce999-150">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce999-151">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="ce999-151">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="ce999-152">Membro del tipo enumerato [**D3DPOOL**](./d3dpool.md) , che descrive la classe di memoria in cui deve essere posizionata la trama.</span><span class="sxs-lookup"><span data-stu-id="ce999-152">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="ce999-153">*Filtro* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="ce999-153">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce999-154">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ce999-154">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ce999-155">Combinazione di uno o più [ \_ filtri D3DX](d3dx-filter.md) che controllano il modo in cui l'immagine viene filtrata.</span><span class="sxs-lookup"><span data-stu-id="ce999-155">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="ce999-156">Specificare \_ il valore predefinito di D3DX per questo parametro equivale a specificare \_ il \_ \| \_ dithering del filtro D3DX del triangolo di filtro D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="ce999-156">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="ce999-157">*MipFilter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ce999-157">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce999-158">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ce999-158">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ce999-159">Combinazione di uno o più [ \_ filtri D3DX](d3dx-filter.md) che controllano il modo in cui l'immagine viene filtrata.</span><span class="sxs-lookup"><span data-stu-id="ce999-159">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="ce999-160">La specifica \_ di D3DX default per questo parametro equivale alla specifica della \_ casella di filtro D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="ce999-160">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="ce999-161">Usare inoltre bits 27-31 per specificare il numero di livelli MIP da ignorare (dall'inizio della catena mipmap) quando una trama con estensione DDS viene caricata in memoria; Questo consente di saltare fino a 32 livelli.</span><span class="sxs-lookup"><span data-stu-id="ce999-161">In addition, use bits 27-31 to specify the number of mip levels to be skipped (from the top of the mipmap chain) when a .dds texture is loaded into memory; this allows you to skip up to 32 levels.</span></span>

</dd> <dt>

<span data-ttu-id="ce999-162">*ColorKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ce999-162">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce999-163">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="ce999-163">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="ce999-164">Valore [**D3DCOLOR**](d3dcolor.md) da sostituire con nero trasparente oppure 0 per disabilitare il colorkey.</span><span class="sxs-lookup"><span data-stu-id="ce999-164">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="ce999-165">Si tratta sempre di un colore ARGB a 32 bit, indipendente dal formato di immagine di origine.</span><span class="sxs-lookup"><span data-stu-id="ce999-165">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="ce999-166">Alfa è significativo e in genere deve essere impostato su FF per le chiavi di colore opache.</span><span class="sxs-lookup"><span data-stu-id="ce999-166">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="ce999-167">Pertanto, per il nero opaco, il valore sarà uguale a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="ce999-167">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="ce999-168">*pSrcInfo* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="ce999-168">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce999-169">Tipo: **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="ce999-169">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="ce999-170">Puntatore a una struttura di [**\_ informazioni D3DXIMAGE**](d3dximage-info.md) da compilare con una descrizione dei dati nel file di immagine di origine o **null**.</span><span class="sxs-lookup"><span data-stu-id="ce999-170">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled in with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ce999-171">*pPalette* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ce999-171">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce999-172">Tipo: **[ **PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="ce999-172">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="ce999-173">Puntatore a una struttura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , che rappresenta una tavolozza dei colori 256 da compilare o **null**.</span><span class="sxs-lookup"><span data-stu-id="ce999-173">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ce999-174">*ppTexture* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ce999-174">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce999-175">Tipo: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="ce999-175">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span></span>

<span data-ttu-id="ce999-176">Indirizzo di un puntatore a un'interfaccia [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) , che rappresenta l'oggetto trama creato.</span><span class="sxs-lookup"><span data-stu-id="ce999-176">Address of a pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce999-177">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ce999-177">Return value</span></span>

<span data-ttu-id="ce999-178">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ce999-178">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ce999-179">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ce999-179">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ce999-180">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="ce999-180">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce999-181">Commenti</span><span class="sxs-lookup"><span data-stu-id="ce999-181">Remarks</span></span>

<span data-ttu-id="ce999-182">L'impostazione del compilatore determina anche la versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="ce999-182">The compiler setting also determines the function version.</span></span> <span data-ttu-id="ce999-183">Se è definito Unicode, la chiamata di funzione viene risolta in D3DXCreateVolumeTextureFromFileExW.</span><span class="sxs-lookup"><span data-stu-id="ce999-183">If Unicode is defined, the function call resolves to D3DXCreateVolumeTextureFromFileExW.</span></span> <span data-ttu-id="ce999-184">In caso contrario, la chiamata di funzione viene risolta in D3DXCreateVolumeTextureFromFileExA perché vengono utilizzate le stringhe ANSI.</span><span class="sxs-lookup"><span data-stu-id="ce999-184">Otherwise, the function call resolves to D3DXCreateVolumeTextureFromFileExA because ANSI strings are being used.</span></span>

<span data-ttu-id="ce999-185">Questa funzione supporta i formati di file seguenti:. bmp,. DDS,. DIB,. HDR,. jpg,. PFM,. png,. ppm e. tga.</span><span class="sxs-lookup"><span data-stu-id="ce999-185">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="ce999-186">Vedere [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="ce999-186">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="ce999-187">Le trame mipmap dispongono automaticamente di ogni livello riempito con la trama del volume caricato.</span><span class="sxs-lookup"><span data-stu-id="ce999-187">Mipmapped textures automatically have each level filled with the loaded volume texture.</span></span> <span data-ttu-id="ce999-188">Quando si caricano immagini in trame mipmap, alcuni dispositivi non sono in grado di passare a un'immagine 1x1 e questa funzione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="ce999-188">When loading images into mipmapped textures, some devices are unable to go to a 1x1 image and this function will fail.</span></span> <span data-ttu-id="ce999-189">In tal caso, è necessario caricare le immagini manualmente.</span><span class="sxs-lookup"><span data-stu-id="ce999-189">If this happens, then the images need to be loaded manually.</span></span>

<span data-ttu-id="ce999-190">Quando si ignorano i livelli di mipmap durante il caricamento di un file con estensione DDS, usare la \_ macro D3DX Skip \_ DDS \_ MIP \_ Levels per generare il valore *MipFilter* .</span><span class="sxs-lookup"><span data-stu-id="ce999-190">When skipping mipmap levels while loading a .dds file, use the D3DX\_SKIP\_DDS\_MIP\_LEVELS macro to generate the *MipFilter* value.</span></span> <span data-ttu-id="ce999-191">Questa macro accetta il numero di livelli da ignorare e il tipo di filtro e restituisce il valore del filtro, che viene quindi passato al parametro *MipFilter* .</span><span class="sxs-lookup"><span data-stu-id="ce999-191">This macro takes the number of levels to skip and the filter type and returns the filter value, which would then be passed into the *MipFilter* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce999-192">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ce999-192">Requirements</span></span>



| <span data-ttu-id="ce999-193">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce999-193">Requirement</span></span> | <span data-ttu-id="ce999-194">Valore</span><span class="sxs-lookup"><span data-stu-id="ce999-194">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ce999-195">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ce999-195">Header</span></span><br/>  | <dl> <span data-ttu-id="ce999-196"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce999-196"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="ce999-197">Libreria</span><span class="sxs-lookup"><span data-stu-id="ce999-197">Library</span></span><br/> | <dl> <span data-ttu-id="ce999-198"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ce999-198"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ce999-199">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ce999-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce999-200">**D3DXCreateVolumeTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="ce999-200">**D3DXCreateVolumeTextureFromFile**</span></span>](d3dxcreatevolumetexturefromfile.md)
</dt> <dt>

[<span data-ttu-id="ce999-201">**D3DXCreateVolumeTextureFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="ce999-201">**D3DXCreateVolumeTextureFromFileInMemory**</span></span>](d3dxcreatevolumetexturefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="ce999-202">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="ce999-202">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span></span>](d3dxcreatevolumetexturefromfileinmemoryex.md)
</dt> <dt>

[<span data-ttu-id="ce999-203">**D3DXCreateVolumeTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="ce999-203">**D3DXCreateVolumeTextureFromResource**</span></span>](d3dxcreatevolumetexturefromresource.md)
</dt> <dt>

[<span data-ttu-id="ce999-204">**D3DXCreateVolumeTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="ce999-204">**D3DXCreateVolumeTextureFromResourceEx**</span></span>](d3dxcreatevolumetexturefromresourceex.md)
</dt> <dt>

[<span data-ttu-id="ce999-205">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="ce999-205">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
