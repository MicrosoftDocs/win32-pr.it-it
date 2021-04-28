---
description: 'Funzione D3DXCreateVolumeTextureFromFileEx: crea una trama del volume da un file.'
ms.assetid: fa11706a-83cc-4795-957d-6d0e1faf2a8f
title: Funzione D3DXCreateVolumeTextureFromFileEx (D3dx9tex.h)
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
ms.openlocfilehash: 11be9da24be7fc9a03bab8e761e55a601715bd75
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102749"
---
# <a name="d3dxcreatevolumetexturefromfileex-function"></a><span data-ttu-id="206b5-103">Funzione D3DXCreateVolumeTextureFromFileEx</span><span class="sxs-lookup"><span data-stu-id="206b5-103">D3DXCreateVolumeTextureFromFileEx function</span></span>

<span data-ttu-id="206b5-104">Crea una trama del volume da un file.</span><span class="sxs-lookup"><span data-stu-id="206b5-104">Creates a volume texture from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="206b5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="206b5-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="206b5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="206b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="206b5-107">*pDevice* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="206b5-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="206b5-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="206b5-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="206b5-109">Puntatore a [**un'interfaccia IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) che rappresenta il dispositivo da associare alla trama.</span><span class="sxs-lookup"><span data-stu-id="206b5-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="206b5-110">*pSrcFile* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="206b5-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="206b5-111">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="206b5-111">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="206b5-112">Puntatore a una stringa che specifica il nome file.</span><span class="sxs-lookup"><span data-stu-id="206b5-112">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="206b5-113">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="206b5-113">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="206b5-114">In caso contrario, il tipo di dati stringa viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="206b5-114">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="206b5-115">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="206b5-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="206b5-116">*Larghezza* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="206b5-116">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="206b5-117">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="206b5-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="206b5-118">Larghezza in pixel.</span><span class="sxs-lookup"><span data-stu-id="206b5-118">Width in pixels.</span></span> <span data-ttu-id="206b5-119">Se questo valore è zero o D3DX \_ DEFAULT, le dimensioni vengono prese dal file.</span><span class="sxs-lookup"><span data-stu-id="206b5-119">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="206b5-120">La dimensione massima che un driver supporta (per larghezza, altezza e profondità) è disponibile in MaxVolumeExtent in [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)</span><span class="sxs-lookup"><span data-stu-id="206b5-120">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="206b5-121">*Altezza* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="206b5-121">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="206b5-122">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="206b5-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="206b5-123">Altezza, in pixel.</span><span class="sxs-lookup"><span data-stu-id="206b5-123">Height, in pixels.</span></span> <span data-ttu-id="206b5-124">Se questo valore è zero o D3DX \_ DEFAULT, le dimensioni vengono prelevate dal file.</span><span class="sxs-lookup"><span data-stu-id="206b5-124">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="206b5-125">La dimensione massima che un driver supporta (per larghezza, altezza e profondità) è disponibile in MaxVolumeExtent in [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)</span><span class="sxs-lookup"><span data-stu-id="206b5-125">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="206b5-126">*Profondità* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="206b5-126">*Depth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="206b5-127">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="206b5-127">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="206b5-128">Profondità, in pixel.</span><span class="sxs-lookup"><span data-stu-id="206b5-128">Depth, in pixels.</span></span> <span data-ttu-id="206b5-129">Se questo valore è zero o D3DX \_ DEFAULT, le dimensioni vengono prelevate dal file.</span><span class="sxs-lookup"><span data-stu-id="206b5-129">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="206b5-130">La dimensione massima che un driver supporta (per larghezza, altezza e profondità) è disponibile in MaxVolumeExtent in [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)</span><span class="sxs-lookup"><span data-stu-id="206b5-130">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="206b5-131">*MipLevels* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="206b5-131">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="206b5-132">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="206b5-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="206b5-133">Numero di livelli mip richiesti.</span><span class="sxs-lookup"><span data-stu-id="206b5-133">Number of mip levels requested.</span></span> <span data-ttu-id="206b5-134">Se questo valore è zero o D3DX DEFAULT, viene creata una catena \_ mipmap completa.</span><span class="sxs-lookup"><span data-stu-id="206b5-134">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="206b5-135">*Utilizzo* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="206b5-135">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="206b5-136">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="206b5-136">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="206b5-137">0, D3DUSAGE \_ RENDERTARGET o D3DUSAGE \_ DYNAMIC.</span><span class="sxs-lookup"><span data-stu-id="206b5-137">0, D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="206b5-138">L'impostazione di questo flag su D3DUSAGE RENDERTARGET indica che la \_ superficie deve essere usata come destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="206b5-138">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="206b5-139">La risorsa può quindi essere passata al *parametro pNewRenderTarget* del [**metodo SetRenderTarget.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget)</span><span class="sxs-lookup"><span data-stu-id="206b5-139">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) method.</span></span> <span data-ttu-id="206b5-140">Se si specifica D3DUSAGE RENDERTARGET o D3DUSAGE DYNAMIC, il pool deve essere impostato su D3DPOOL DEFAULT e l'applicazione deve verificare che il dispositivo supporti questa operazione chiamando \_ \_  \_ [**CheckDeviceFormat.**](/windows/desktop/api)</span><span class="sxs-lookup"><span data-stu-id="206b5-140">If either D3DUSAGE\_RENDERTARGET or D3DUSAGE\_DYNAMIC is specified, *Pool* must be set to D3DPOOL\_DEFAULT, and the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="206b5-141">D3DUSAGE \_ DYNAMIC indica che la superficie deve essere gestita dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="206b5-141">D3DUSAGE\_DYNAMIC indicates that the surface should be handled dynamically.</span></span> <span data-ttu-id="206b5-142">Per altre informazioni sull'uso di trame dinamiche, vedere [Uso di trame dinamiche.](performance-optimizations.md)</span><span class="sxs-lookup"><span data-stu-id="206b5-142">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="206b5-143">*Formato*</span><span class="sxs-lookup"><span data-stu-id="206b5-143">*Format*</span></span> 
</dt> <dd>

<span data-ttu-id="206b5-144">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="206b5-144">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="206b5-145">Membro del [tipo enumerato D3DFORMAT,](d3dformat.md) che descrive il formato pixel richiesto per la trama.</span><span class="sxs-lookup"><span data-stu-id="206b5-145">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the texture.</span></span> <span data-ttu-id="206b5-146">La trama restituita potrebbe avere un formato diverso da quello specificato da *Format*.</span><span class="sxs-lookup"><span data-stu-id="206b5-146">The returned texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="206b5-147">Le applicazioni devono controllare il formato della trama restituita.</span><span class="sxs-lookup"><span data-stu-id="206b5-147">Applications should check the format of the returned texture.</span></span> <span data-ttu-id="206b5-148">Se [D3DFMT \_ UNKNOWN](other-d3dx-constants.md), il formato viene tratto dal file.</span><span class="sxs-lookup"><span data-stu-id="206b5-148">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="206b5-149">Se D3DFMT FROM FILE, il formato viene preso esattamente come si trova nel file e la chiamata avrà esito negativo se viola le funzionalità \_ \_ del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="206b5-149">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="206b5-150">*Pool* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="206b5-150">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="206b5-151">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="206b5-151">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="206b5-152">Membro del [**tipo enumerato D3DPOOL,**](./d3dpool.md) che descrive la classe di memoria in cui deve essere inserita la trama.</span><span class="sxs-lookup"><span data-stu-id="206b5-152">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="206b5-153">*Filtro* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="206b5-153">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="206b5-154">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="206b5-154">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="206b5-155">Combinazione di uno o più [filtri D3DX \_ che](d3dx-filter.md) controllano la modalità di filtro dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="206b5-155">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="206b5-156">Specificare D3DX DEFAULT per questo parametro equivale a specificare \_ D3DX \_ FILTER \_ TRIANGLE \| D3DX \_ FILTER \_ DITHER.</span><span class="sxs-lookup"><span data-stu-id="206b5-156">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="206b5-157">*MipFilter* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="206b5-157">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="206b5-158">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="206b5-158">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="206b5-159">Combinazione di uno o più [filtri D3DX \_ che](d3dx-filter.md) controllano la modalità di filtro dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="206b5-159">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="206b5-160">Specificare D3DX DEFAULT per questo parametro equivale a \_ specificare D3DX \_ FILTER \_ BOX.</span><span class="sxs-lookup"><span data-stu-id="206b5-160">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="206b5-161">Usare anche i bit da 27 a 31 per specificare il numero di livelli mip da ignorare (dall'inizio della catena mipmap) quando una trama .dds viene caricata in memoria. In questo modo è possibile ignorare fino a 32 livelli.</span><span class="sxs-lookup"><span data-stu-id="206b5-161">In addition, use bits 27-31 to specify the number of mip levels to be skipped (from the top of the mipmap chain) when a .dds texture is loaded into memory; this allows you to skip up to 32 levels.</span></span>

</dd> <dt>

<span data-ttu-id="206b5-162">*ColorKey* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="206b5-162">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="206b5-163">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="206b5-163">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="206b5-164">[**Valore D3DCOLOR**](d3dcolor.md) da sostituire con nero trasparente oppure 0 per disabilitare la chiave di colore.</span><span class="sxs-lookup"><span data-stu-id="206b5-164">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="206b5-165">Si tratta sempre di un colore ARGB a 32 bit, indipendentemente dal formato dell'immagine di origine.</span><span class="sxs-lookup"><span data-stu-id="206b5-165">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="206b5-166">Il valore alfa è significativo e in genere deve essere impostato su FF per le chiavi di colore opache.</span><span class="sxs-lookup"><span data-stu-id="206b5-166">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="206b5-167">Pertanto, per il nero opaco, il valore sarebbe uguale a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="206b5-167">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="206b5-168">*pSrcInfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="206b5-168">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="206b5-169">Tipo: **[ **D3DXIMAGE \_ INFO**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="206b5-169">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="206b5-170">Puntatore a [**una struttura D3DXIMAGE \_ INFO**](d3dximage-info.md) da riempire con una descrizione dei dati nel file di immagine di origine oppure **NULL.**</span><span class="sxs-lookup"><span data-stu-id="206b5-170">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled in with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="206b5-171">*pPalette* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="206b5-171">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="206b5-172">Tipo: **[ **PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="206b5-172">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="206b5-173">Puntatore a [**una struttura PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) che rappresenta una tavolozza di 256 colori da compilare oppure **NULL.**</span><span class="sxs-lookup"><span data-stu-id="206b5-173">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="206b5-174">*ppTexture* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="206b5-174">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="206b5-175">Tipo: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="206b5-175">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span></span>

<span data-ttu-id="206b5-176">Indirizzo di un puntatore a [**un'interfaccia IDirect3DVolumeTexture9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) che rappresenta l'oggetto trama creato.</span><span class="sxs-lookup"><span data-stu-id="206b5-176">Address of a pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="206b5-177">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="206b5-177">Return value</span></span>

<span data-ttu-id="206b5-178">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="206b5-178">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="206b5-179">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="206b5-179">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="206b5-180">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="206b5-180">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="206b5-181">Commenti</span><span class="sxs-lookup"><span data-stu-id="206b5-181">Remarks</span></span>

<span data-ttu-id="206b5-182">L'impostazione del compilatore determina anche la versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="206b5-182">The compiler setting also determines the function version.</span></span> <span data-ttu-id="206b5-183">Se è definito Unicode, la chiamata di funzione viene risolta in D3DXCreateVolumeTextureFromFileExW.</span><span class="sxs-lookup"><span data-stu-id="206b5-183">If Unicode is defined, the function call resolves to D3DXCreateVolumeTextureFromFileExW.</span></span> <span data-ttu-id="206b5-184">In caso contrario, la chiamata di funzione viene risolta in D3DXCreateVolumeTextureFromFileExA perché vengono usate stringhe ANSI.</span><span class="sxs-lookup"><span data-stu-id="206b5-184">Otherwise, the function call resolves to D3DXCreateVolumeTextureFromFileExA because ANSI strings are being used.</span></span>

<span data-ttu-id="206b5-185">Questa funzione supporta i formati di file seguenti: bmp, dds, dib, hdr, jpg, pfm, png, ppm e tga.</span><span class="sxs-lookup"><span data-stu-id="206b5-185">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="206b5-186">Vedere [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="206b5-186">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="206b5-187">Le trame mipmapped hanno automaticamente ogni livello riempito con la trama del volume caricata.</span><span class="sxs-lookup"><span data-stu-id="206b5-187">Mipmapped textures automatically have each level filled with the loaded volume texture.</span></span> <span data-ttu-id="206b5-188">Quando si caricano immagini in trame mipmapped, alcuni dispositivi non sono in grado di passare a un'immagine 1x1 e questa funzione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="206b5-188">When loading images into mipmapped textures, some devices are unable to go to a 1x1 image and this function will fail.</span></span> <span data-ttu-id="206b5-189">In questo caso, le immagini devono essere caricate manualmente.</span><span class="sxs-lookup"><span data-stu-id="206b5-189">If this happens, then the images need to be loaded manually.</span></span>

<span data-ttu-id="206b5-190">Quando si ignorano i livelli mipmap durante il caricamento di un file DDS, usare la macro D3DX SKIP DDS MIP LEVELS per generare \_ \_ il valore \_ \_ *MipFilter.*</span><span class="sxs-lookup"><span data-stu-id="206b5-190">When skipping mipmap levels while loading a .dds file, use the D3DX\_SKIP\_DDS\_MIP\_LEVELS macro to generate the *MipFilter* value.</span></span> <span data-ttu-id="206b5-191">Questa macro accetta il numero di livelli da ignorare e il tipo di filtro e restituisce il valore del filtro, che verrà quindi passato nel *parametro MipFilter.*</span><span class="sxs-lookup"><span data-stu-id="206b5-191">This macro takes the number of levels to skip and the filter type and returns the filter value, which would then be passed into the *MipFilter* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="206b5-192">Requisiti</span><span class="sxs-lookup"><span data-stu-id="206b5-192">Requirements</span></span>



| <span data-ttu-id="206b5-193">Requisito</span><span class="sxs-lookup"><span data-stu-id="206b5-193">Requirement</span></span> | <span data-ttu-id="206b5-194">Valore</span><span class="sxs-lookup"><span data-stu-id="206b5-194">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="206b5-195">Intestazione</span><span class="sxs-lookup"><span data-stu-id="206b5-195">Header</span></span><br/>  | <dl> <span data-ttu-id="206b5-196"><dt>D3dx9tex.h</dt></span><span class="sxs-lookup"><span data-stu-id="206b5-196"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="206b5-197">Libreria</span><span class="sxs-lookup"><span data-stu-id="206b5-197">Library</span></span><br/> | <dl> <span data-ttu-id="206b5-198"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="206b5-198"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="206b5-199">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="206b5-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="206b5-200">**D3DXCreateVolumeTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="206b5-200">**D3DXCreateVolumeTextureFromFile**</span></span>](d3dxcreatevolumetexturefromfile.md)
</dt> <dt>

[<span data-ttu-id="206b5-201">**D3DXCreateVolumeTextureFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="206b5-201">**D3DXCreateVolumeTextureFromFileInMemory**</span></span>](d3dxcreatevolumetexturefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="206b5-202">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="206b5-202">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span></span>](d3dxcreatevolumetexturefromfileinmemoryex.md)
</dt> <dt>

[<span data-ttu-id="206b5-203">**D3DXCreateVolumeTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="206b5-203">**D3DXCreateVolumeTextureFromResource**</span></span>](d3dxcreatevolumetexturefromresource.md)
</dt> <dt>

[<span data-ttu-id="206b5-204">**D3DXCreateVolumeTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="206b5-204">**D3DXCreateVolumeTextureFromResourceEx**</span></span>](d3dxcreatevolumetexturefromresourceex.md)
</dt> <dt>

[<span data-ttu-id="206b5-205">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="206b5-205">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
