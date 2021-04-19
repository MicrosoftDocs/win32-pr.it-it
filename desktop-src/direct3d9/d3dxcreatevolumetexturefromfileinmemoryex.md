---
description: Crea una trama del volume da un file. Si tratta di una funzione più avanzata rispetto a D3DXCreateVolumeTextureFromFileInMemory.
ms.assetid: 1a43f906-1826-40a3-a7a9-a0536c977164
title: Funzione D3DXCreateVolumeTextureFromFileInMemoryEx (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTextureFromFileInMemoryEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f09439be9410b59ccaa446c2f00ee79963a21cc6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322718"
---
# <a name="d3dxcreatevolumetexturefromfileinmemoryex-function"></a><span data-ttu-id="6a346-104">D3DXCreateVolumeTextureFromFileInMemoryEx (funzione)</span><span class="sxs-lookup"><span data-stu-id="6a346-104">D3DXCreateVolumeTextureFromFileInMemoryEx function</span></span>

<span data-ttu-id="6a346-105">Crea una trama del volume da un file.</span><span class="sxs-lookup"><span data-stu-id="6a346-105">Creates a volume texture from a file.</span></span> <span data-ttu-id="6a346-106">Si tratta di una funzione più avanzata rispetto a [**D3DXCreateVolumeTextureFromFileInMemory**](d3dxcreatevolumetexturefromfileinmemory.md).</span><span class="sxs-lookup"><span data-stu-id="6a346-106">This is a more advanced function than [**D3DXCreateVolumeTextureFromFileInMemory**](d3dxcreatevolumetexturefromfileinmemory.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6a346-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6a346-107">Syntax</span></span>


```C++
HRESULT D3DXCreateVolumeTextureFromFileInMemoryEx(
  _In_    LPDIRECT3DDEVICE9        pDevice,
  _In_    LPCVOID                  pSrcData,
  _In_    UINT                     SrcDataSize,
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



## <a name="parameters"></a><span data-ttu-id="6a346-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6a346-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a346-109">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a346-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a346-110">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="6a346-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="6a346-111">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo da associare alla trama.</span><span class="sxs-lookup"><span data-stu-id="6a346-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="6a346-112">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a346-112">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a346-113">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a346-113">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a346-114">Puntatore al file in memoria da cui creare la trama del volume.</span><span class="sxs-lookup"><span data-stu-id="6a346-114">Pointer to the file in memory from which to create the volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="6a346-115">*SrcDataSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a346-115">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a346-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a346-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a346-117">Dimensioni in byte del file in memoria.</span><span class="sxs-lookup"><span data-stu-id="6a346-117">Size of the file in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="6a346-118">*Larghezza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a346-118">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a346-119">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a346-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a346-120">Larghezza in pixel.</span><span class="sxs-lookup"><span data-stu-id="6a346-120">Width in pixels.</span></span> <span data-ttu-id="6a346-121">Se questo valore è zero o D3DX \_ default, le dimensioni vengono ricavate dal file.</span><span class="sxs-lookup"><span data-stu-id="6a346-121">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="6a346-122">La dimensione massima supportata da un driver (per larghezza, altezza e profondità) si trova in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="6a346-122">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="6a346-123">*Altezza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a346-123">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a346-124">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a346-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a346-125">Altezza, in pixel.</span><span class="sxs-lookup"><span data-stu-id="6a346-125">Height, in pixels.</span></span> <span data-ttu-id="6a346-126">Se questo valore è zero o D3DX \_ default, le dimensioni vengono ricavate dal file.</span><span class="sxs-lookup"><span data-stu-id="6a346-126">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="6a346-127">La dimensione massima supportata da un driver (per larghezza, altezza e profondità) si trova in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="6a346-127">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="6a346-128">*Profondità* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a346-128">*Depth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a346-129">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a346-129">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a346-130">Profondità, in pixel.</span><span class="sxs-lookup"><span data-stu-id="6a346-130">Depth, in pixels.</span></span> <span data-ttu-id="6a346-131">Se questo valore è zero o D3DX \_ default, le dimensioni vengono ricavate dal file.</span><span class="sxs-lookup"><span data-stu-id="6a346-131">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="6a346-132">La dimensione massima supportata da un driver (per larghezza, altezza e profondità) si trova in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="6a346-132">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="6a346-133">*MipLevels* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a346-133">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a346-134">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a346-134">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a346-135">Numero di livelli MIP richiesti.</span><span class="sxs-lookup"><span data-stu-id="6a346-135">Number of mip levels requested.</span></span> <span data-ttu-id="6a346-136">Se questo valore è zero o D3DX \_ default, viene creata una catena mipmap completa.</span><span class="sxs-lookup"><span data-stu-id="6a346-136">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="6a346-137">*Utilizzo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="6a346-137">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a346-138">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a346-138">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a346-139">0, D3DUSAGE \_ RENDERTARGET o D3DUSAGE \_ Dynamic.</span><span class="sxs-lookup"><span data-stu-id="6a346-139">0, D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="6a346-140">L'impostazione di questo flag su D3DUSAGE \_ RENDERTARGET indica che la superficie deve essere utilizzata come destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="6a346-140">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="6a346-141">La risorsa può quindi essere passata al parametro *pNewRenderTarget* del metodo [**SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) .</span><span class="sxs-lookup"><span data-stu-id="6a346-141">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) method.</span></span> <span data-ttu-id="6a346-142">Se \_ viene specificato D3DUSAGE RENDERTARGET o D3DUSAGE \_ Dynamic, il *pool* deve essere impostato su D3DPOOL \_ default e l'applicazione deve verificare che il dispositivo supporti questa operazione chiamando [**CheckDeviceFormat**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="6a346-142">If either D3DUSAGE\_RENDERTARGET or D3DUSAGE\_DYNAMIC is specified, *Pool* must be set to D3DPOOL\_DEFAULT, and the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="6a346-143">D3DUSAGE \_ Dynamic indica che la superficie deve essere gestita dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="6a346-143">D3DUSAGE\_DYNAMIC indicates that the surface should be handled dynamically.</span></span> <span data-ttu-id="6a346-144">Per ulteriori informazioni sull'utilizzo di trame dinamiche, vedere [using Dynamic Textures](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="6a346-144">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="6a346-145">*Formato* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a346-145">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a346-146">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="6a346-146">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="6a346-147">Membro del tipo enumerato [D3DFORMAT](d3dformat.md) , che descrive il formato pixel richiesto per la trama.</span><span class="sxs-lookup"><span data-stu-id="6a346-147">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the texture.</span></span> <span data-ttu-id="6a346-148">La trama restituita potrebbe avere un formato diverso da quello specificato dal *formato*.</span><span class="sxs-lookup"><span data-stu-id="6a346-148">The returned texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="6a346-149">Le applicazioni devono verificare il formato della trama restituita.</span><span class="sxs-lookup"><span data-stu-id="6a346-149">Applications should check the format of the returned texture.</span></span> <span data-ttu-id="6a346-150">Se [D3DFMT è \_ sconosciuto](other-d3dx-constants.md), il formato viene ricavato dal file.</span><span class="sxs-lookup"><span data-stu-id="6a346-150">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="6a346-151">Se D3DFMT \_ da \_ file, il formato viene considerato esattamente come si trova nel file e la chiamata avrà esito negativo se viola le funzionalità del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6a346-151">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="6a346-152">*Pool* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="6a346-152">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a346-153">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="6a346-153">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="6a346-154">Membro del tipo enumerato [**D3DPOOL**](./d3dpool.md) , che descrive la classe di memoria in cui deve essere posizionata la trama.</span><span class="sxs-lookup"><span data-stu-id="6a346-154">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="6a346-155">*Filtro* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="6a346-155">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a346-156">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a346-156">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a346-157">Combinazione di uno o più [ \_ filtri D3DX](d3dx-filter.md) che controllano il modo in cui l'immagine viene filtrata.</span><span class="sxs-lookup"><span data-stu-id="6a346-157">Combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="6a346-158">Specificare \_ il valore predefinito di D3DX per questo parametro equivale a specificare \_ il \_ \| \_ dithering del filtro D3DX del triangolo di filtro D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="6a346-158">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="6a346-159">*MipFilter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a346-159">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a346-160">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a346-160">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a346-161">Combinazione di uno o più [ \_ filtri D3DX](d3dx-filter.md) che controllano il modo in cui l'immagine viene filtrata.</span><span class="sxs-lookup"><span data-stu-id="6a346-161">Combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="6a346-162">La specifica \_ di D3DX default per questo parametro equivale alla specifica della \_ casella di filtro D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="6a346-162">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="6a346-163">Usare inoltre bits 27-31 per specificare il numero di livelli MIP da ignorare (dall'inizio della catena mipmap) quando una trama con estensione DDS viene caricata in memoria; Questo consente di saltare fino a 32 livelli.</span><span class="sxs-lookup"><span data-stu-id="6a346-163">In addition, use bits 27-31 to specify the number of mip levels to be skipped (from the top of the mipmap chain) when a .dds texture is loaded into memory; this allows you to skip up to 32 levels.</span></span>

</dd> <dt>

<span data-ttu-id="6a346-164">*ColorKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a346-164">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a346-165">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="6a346-165">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="6a346-166">Valore [**D3DCOLOR**](d3dcolor.md) da sostituire con nero trasparente oppure 0 per disabilitare il colorkey.</span><span class="sxs-lookup"><span data-stu-id="6a346-166">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="6a346-167">Si tratta sempre di un colore ARGB a 32 bit, indipendente dal formato di immagine di origine.</span><span class="sxs-lookup"><span data-stu-id="6a346-167">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="6a346-168">Alfa è significativo e in genere deve essere impostato su FF per le chiavi di colore opache.</span><span class="sxs-lookup"><span data-stu-id="6a346-168">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="6a346-169">Pertanto, per il nero opaco, il valore sarà uguale a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="6a346-169">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="6a346-170">*pSrcInfo* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="6a346-170">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a346-171">Tipo: **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="6a346-171">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="6a346-172">Puntatore a una struttura di [**\_ informazioni D3DXIMAGE**](d3dximage-info.md) da compilare con una descrizione dei dati nel file di immagine di origine o **null**.</span><span class="sxs-lookup"><span data-stu-id="6a346-172">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled in with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6a346-173">*pPalette* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6a346-173">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a346-174">Tipo: **[ **PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="6a346-174">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="6a346-175">Puntatore a una struttura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , che rappresenta una tavolozza dei colori 256 da compilare o **null**.</span><span class="sxs-lookup"><span data-stu-id="6a346-175">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6a346-176">*ppVolumeTexture* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6a346-176">*ppVolumeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a346-177">Tipo: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="6a346-177">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span></span>

<span data-ttu-id="6a346-178">Indirizzo di un puntatore a un'interfaccia [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) , che rappresenta l'oggetto trama creato.</span><span class="sxs-lookup"><span data-stu-id="6a346-178">Address of a pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a346-179">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6a346-179">Return value</span></span>

<span data-ttu-id="6a346-180">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6a346-180">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6a346-181">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6a346-181">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6a346-182">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="6a346-182">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a346-183">Commenti</span><span class="sxs-lookup"><span data-stu-id="6a346-183">Remarks</span></span>

<span data-ttu-id="6a346-184">Questa funzione supporta i formati di file seguenti:. bmp,. DDS,. DIB,. HDR,. jpg,. PFM,. png,. ppm e. tga.</span><span class="sxs-lookup"><span data-stu-id="6a346-184">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="6a346-185">Vedere [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="6a346-185">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="6a346-186">Quando si ignorano i livelli di mipmap durante il caricamento di un file con estensione DDS, usare la \_ macro D3DX Skip \_ DDS \_ MIP \_ Levels per generare il valore *MipFilter* .</span><span class="sxs-lookup"><span data-stu-id="6a346-186">When skipping mipmap levels while loading a .dds file, use the D3DX\_SKIP\_DDS\_MIP\_LEVELS macro to generate the *MipFilter* value.</span></span> <span data-ttu-id="6a346-187">Questa macro accetta il numero di livelli da ignorare e il tipo di filtro e restituisce il valore del filtro, che viene quindi passato al parametro *MipFilter* .</span><span class="sxs-lookup"><span data-stu-id="6a346-187">This macro takes the number of levels to skip and the filter type and returns the filter value, which would then be passed into the *MipFilter* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a346-188">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6a346-188">Requirements</span></span>



| <span data-ttu-id="6a346-189">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a346-189">Requirement</span></span> | <span data-ttu-id="6a346-190">Valore</span><span class="sxs-lookup"><span data-stu-id="6a346-190">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6a346-191">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6a346-191">Header</span></span><br/>  | <dl> <span data-ttu-id="6a346-192"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a346-192"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="6a346-193">Libreria</span><span class="sxs-lookup"><span data-stu-id="6a346-193">Library</span></span><br/> | <dl> <span data-ttu-id="6a346-194"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6a346-194"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="6a346-195">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6a346-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a346-196">**D3DXCreateVolumeTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="6a346-196">**D3DXCreateVolumeTextureFromFile**</span></span>](d3dxcreatevolumetexturefromfile.md)
</dt> <dt>

[<span data-ttu-id="6a346-197">**D3DXCreateVolumeTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="6a346-197">**D3DXCreateVolumeTextureFromFileEx**</span></span>](d3dxcreatevolumetexturefromfileex.md)
</dt> <dt>

[<span data-ttu-id="6a346-198">**D3DXCreateVolumeTextureFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="6a346-198">**D3DXCreateVolumeTextureFromFileInMemory**</span></span>](d3dxcreatevolumetexturefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="6a346-199">**D3DXCreateVolumeTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="6a346-199">**D3DXCreateVolumeTextureFromResource**</span></span>](d3dxcreatevolumetexturefromresource.md)
</dt> <dt>

[<span data-ttu-id="6a346-200">**D3DXCreateVolumeTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="6a346-200">**D3DXCreateVolumeTextureFromResourceEx**</span></span>](d3dxcreatevolumetexturefromresourceex.md)
</dt> <dt>

[<span data-ttu-id="6a346-201">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="6a346-201">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
