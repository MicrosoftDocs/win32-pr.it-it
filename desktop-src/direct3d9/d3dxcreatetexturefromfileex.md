---
description: Crea una trama da un file. Si tratta di una funzione più avanzata rispetto a D3DXCreateTextureFromFile.
ms.assetid: 820bbd77-98af-4051-a22e-825fa4dd87d8
title: Funzione D3DXCreateTextureFromFileEx (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromFileEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f4dba1424f98389a9282fdebf9dae55c7e1601f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103886280"
---
# <a name="d3dxcreatetexturefromfileex-function"></a><span data-ttu-id="97c99-104">D3DXCreateTextureFromFileEx (funzione)</span><span class="sxs-lookup"><span data-stu-id="97c99-104">D3DXCreateTextureFromFileEx function</span></span>

<span data-ttu-id="97c99-105">Crea una trama da un file.</span><span class="sxs-lookup"><span data-stu-id="97c99-105">Creates a texture from a file.</span></span> <span data-ttu-id="97c99-106">Si tratta di una funzione più avanzata rispetto a [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md).</span><span class="sxs-lookup"><span data-stu-id="97c99-106">This is a more advanced function than [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="97c99-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="97c99-107">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureFromFileEx(
  _In_    LPDIRECT3DDEVICE9  pDevice,
  _In_    LPCTSTR            pSrcFile,
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



## <a name="parameters"></a><span data-ttu-id="97c99-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="97c99-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97c99-109">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97c99-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97c99-110">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="97c99-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="97c99-111">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo da associare alla trama.</span><span class="sxs-lookup"><span data-stu-id="97c99-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="97c99-112">*pSrcFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97c99-112">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97c99-113">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="97c99-113">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="97c99-114">Puntatore a una stringa che specifica il nome del file.</span><span class="sxs-lookup"><span data-stu-id="97c99-114">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="97c99-115">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="97c99-115">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="97c99-116">In caso contrario, il tipo di dati String viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="97c99-116">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="97c99-117">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="97c99-117">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="97c99-118">*Larghezza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97c99-118">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97c99-119">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="97c99-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="97c99-120">Larghezza in pixel.</span><span class="sxs-lookup"><span data-stu-id="97c99-120">Width in pixels.</span></span> <span data-ttu-id="97c99-121">Se questo valore è zero o D3DX \_ default, le dimensioni vengono ricavate dal file e arrotondate per eccesso a una potenza di due.</span><span class="sxs-lookup"><span data-stu-id="97c99-121">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file and rounded up to a power of two.</span></span> <span data-ttu-id="97c99-122">Se il dispositivo supporta una non potenza di 2 trame e viene specificato il [ \_ valore predefinito D3DX \_ NONPOW2](other-d3dx-constants.md) , la dimensione non verrà arrotondata.</span><span class="sxs-lookup"><span data-stu-id="97c99-122">If the device supports non-power of 2 textures and [D3DX\_DEFAULT\_NONPOW2](other-d3dx-constants.md) is specified, the size will not be rounded.</span></span>

</dd> <dt>

<span data-ttu-id="97c99-123">*Altezza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97c99-123">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97c99-124">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="97c99-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="97c99-125">Altezza, in pixel.</span><span class="sxs-lookup"><span data-stu-id="97c99-125">Height, in pixels.</span></span> <span data-ttu-id="97c99-126">Se questo valore è zero o D3DX \_ default, le dimensioni vengono ricavate dal file e arrotondate per eccesso a una potenza di due.</span><span class="sxs-lookup"><span data-stu-id="97c99-126">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file and rounded up to a power of two.</span></span> <span data-ttu-id="97c99-127">Se il dispositivo supporta una non potenza di 2 trame e [il \_ valore \_ predefinito di D3DX](other-d3dx-constants.md) è sepcified, la dimensione non verrà arrotondata.</span><span class="sxs-lookup"><span data-stu-id="97c99-127">If the device supports non-power of 2 textures and [D3DX\_DEFAULT\_NONPOW2](other-d3dx-constants.md) is sepcified, the size will not be rounded.</span></span>

</dd> <dt>

<span data-ttu-id="97c99-128">*MipLevels* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97c99-128">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97c99-129">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="97c99-129">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="97c99-130">Numero di livelli MIP richiesti.</span><span class="sxs-lookup"><span data-stu-id="97c99-130">Number of mip levels requested.</span></span> <span data-ttu-id="97c99-131">Se questo valore è zero o D3DX \_ default, viene creata una catena mipmap completa.</span><span class="sxs-lookup"><span data-stu-id="97c99-131">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span> <span data-ttu-id="97c99-132">Se D3DX \_ da \_ file, le dimensioni verranno eseguite esattamente come sono nel file e la chiamata avrà esito negativo se viola le funzionalità del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="97c99-132">If D3DX\_FROM\_FILE, the size will be taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="97c99-133">*Utilizzo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="97c99-133">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97c99-134">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="97c99-134">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="97c99-135">0, [**D3DUSAGE \_ RENDERTARGET**](d3dusage.md)o **D3DUSAGE \_ Dynamic**.</span><span class="sxs-lookup"><span data-stu-id="97c99-135">0, [**D3DUSAGE\_RENDERTARGET**](d3dusage.md), or **D3DUSAGE\_DYNAMIC**.</span></span> <span data-ttu-id="97c99-136">L'impostazione di questo flag su **D3DUSAGE \_ RENDERTARGET** indica che la superficie deve essere utilizzata come destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="97c99-136">Setting this flag to **D3DUSAGE\_RENDERTARGET** indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="97c99-137">La risorsa può quindi essere passata al parametro *pNewRenderTarget* del metodo [**SetRenderTarget**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="97c99-137">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="97c99-138">Se viene specificato **D3DUSAGE \_ RENDERTARGET** o **D3DUSAGE \_ Dynamic** , il *pool* deve essere impostato su D3DPOOL \_ default e l'applicazione deve verificare che il dispositivo supporti questa operazione chiamando [**CheckDeviceFormat**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="97c99-138">If either **D3DUSAGE\_RENDERTARGET** or **D3DUSAGE\_DYNAMIC** is specified, *Pool* must be set to D3DPOOL\_DEFAULT, and the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="97c99-139">**D3DUSAGE \_ DYNAMIC** indica che la superficie deve essere gestita dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="97c99-139">**D3DUSAGE\_DYNAMIC** indicates that the surface should be handled dynamically.</span></span> <span data-ttu-id="97c99-140">Vedere [uso di trame dinamiche](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="97c99-140">See [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="97c99-141">*Formato* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97c99-141">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97c99-142">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="97c99-142">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="97c99-143">Membro del tipo enumerato [D3DFORMAT](d3dformat.md) , che descrive il formato pixel richiesto per la trama.</span><span class="sxs-lookup"><span data-stu-id="97c99-143">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the texture.</span></span> <span data-ttu-id="97c99-144">La trama restituita potrebbe avere un formato diverso da quello specificato dal *formato*.</span><span class="sxs-lookup"><span data-stu-id="97c99-144">The returned texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="97c99-145">Le applicazioni devono verificare il formato della trama restituita.</span><span class="sxs-lookup"><span data-stu-id="97c99-145">Applications should check the format of the returned texture.</span></span> <span data-ttu-id="97c99-146">Se D3DFMT \_ è sconosciuto, il formato viene ricavato dal file.</span><span class="sxs-lookup"><span data-stu-id="97c99-146">If D3DFMT\_UNKNOWN, the format is taken from the file.</span></span> <span data-ttu-id="97c99-147">Se D3DFMT \_ da \_ file, il formato viene considerato esattamente come si trova nel file e la chiamata avrà esito negativo se viola le funzionalità del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="97c99-147">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="97c99-148">*Pool* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="97c99-148">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97c99-149">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="97c99-149">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="97c99-150">Membro del tipo enumerato [**D3DPOOL**](./d3dpool.md) , che descrive la classe di memoria in cui deve essere posizionata la trama.</span><span class="sxs-lookup"><span data-stu-id="97c99-150">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="97c99-151">*Filtro* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="97c99-151">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97c99-152">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="97c99-152">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="97c99-153">Combinazione di una o più costanti [di \_ filtro D3DX](d3dx-filter.md) che controllano il modo in cui l'immagine viene filtrata.</span><span class="sxs-lookup"><span data-stu-id="97c99-153">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) constants controlling how the image is filtered.</span></span> <span data-ttu-id="97c99-154">Specificare [il \_ valore predefinito di D3DX](other-d3dx-constants.md) per questo parametro equivale a specificare \_ il \_ \| \_ dithering del filtro D3DX del triangolo di filtro D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="97c99-154">Specifying [D3DX\_DEFAULT](other-d3dx-constants.md) for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="97c99-155">*MipFilter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97c99-155">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97c99-156">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="97c99-156">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="97c99-157">Combinazione di una o più costanti [di \_ filtro D3DX](d3dx-filter.md) che controllano il modo in cui l'immagine viene filtrata.</span><span class="sxs-lookup"><span data-stu-id="97c99-157">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) constants controlling how the image is filtered.</span></span> <span data-ttu-id="97c99-158">La specifica \_ di D3DX default per questo parametro equivale alla specifica della \_ casella di filtro D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="97c99-158">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="97c99-159">Usare inoltre bits 27-31 per specificare il numero di livelli MIP da ignorare (dall'inizio della catena mipmap) quando una trama con estensione DDS viene caricata in memoria; Questo consente di saltare fino a 32 livelli.</span><span class="sxs-lookup"><span data-stu-id="97c99-159">In addition, use bits 27-31 to specify the number of mip levels to be skipped (from the top of the mipmap chain) when a .dds texture is loaded into memory; this allows you to skip up to 32 levels.</span></span>

</dd> <dt>

<span data-ttu-id="97c99-160">*ColorKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97c99-160">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97c99-161">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="97c99-161">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="97c99-162">Valore [**D3DCOLOR**](d3dcolor.md) da sostituire con nero trasparente oppure 0 per disabilitare la chiave di colore.</span><span class="sxs-lookup"><span data-stu-id="97c99-162">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the color key.</span></span> <span data-ttu-id="97c99-163">Si tratta sempre di un colore ARGB a 32 bit, indipendente dal formato di immagine di origine.</span><span class="sxs-lookup"><span data-stu-id="97c99-163">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="97c99-164">Alfa è significativo e in genere deve essere impostato su FF per le chiavi di colore opache.</span><span class="sxs-lookup"><span data-stu-id="97c99-164">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="97c99-165">Pertanto, per il nero opaco, il valore sarà uguale a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="97c99-165">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="97c99-166">*pSrcInfo* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="97c99-166">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="97c99-167">Tipo: **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="97c99-167">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="97c99-168">Puntatore a una struttura di [**\_ informazioni D3DXIMAGE**](d3dximage-info.md) da compilare con una descrizione dei dati nel file di immagine di origine o **null**.</span><span class="sxs-lookup"><span data-stu-id="97c99-168">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled in with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="97c99-169">*pPalette* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="97c99-169">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="97c99-170">Tipo: **[ **PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="97c99-170">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="97c99-171">Puntatore a una struttura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , che rappresenta una tavolozza dei colori 256 da compilare o **null**.</span><span class="sxs-lookup"><span data-stu-id="97c99-171">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="97c99-172">*ppTexture* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="97c99-172">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="97c99-173">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="97c99-173">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="97c99-174">Indirizzo di un puntatore a un'interfaccia [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , che rappresenta l'oggetto trama creato.</span><span class="sxs-lookup"><span data-stu-id="97c99-174">Address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97c99-175">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="97c99-175">Return value</span></span>

<span data-ttu-id="97c99-176">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="97c99-176">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="97c99-177">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="97c99-177">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="97c99-178">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="97c99-178">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="97c99-179">Commenti</span><span class="sxs-lookup"><span data-stu-id="97c99-179">Remarks</span></span>

<span data-ttu-id="97c99-180">L'impostazione del compilatore determina anche la versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="97c99-180">The compiler setting also determines the function version.</span></span> <span data-ttu-id="97c99-181">Se è definito Unicode, la chiamata di funzione viene risolta in D3DXCreateTextureFromFileExW.</span><span class="sxs-lookup"><span data-stu-id="97c99-181">If Unicode is defined, the function call resolves to D3DXCreateTextureFromFileExW.</span></span> <span data-ttu-id="97c99-182">In caso contrario, la chiamata di funzione viene risolta in D3DXCreateTextureFromFileExA perché vengono utilizzate le stringhe ANSI.</span><span class="sxs-lookup"><span data-stu-id="97c99-182">Otherwise, the function call resolves to D3DXCreateTextureFromFileExA because ANSI strings are being used.</span></span>

<span data-ttu-id="97c99-183">Usare [**D3DXCheckTextureRequirements**](d3dxchecktexturerequirements.md) per determinare se il dispositivo è in grado di supportare la trama in base allo stato corrente.</span><span class="sxs-lookup"><span data-stu-id="97c99-183">Use [**D3DXCheckTextureRequirements**](d3dxchecktexturerequirements.md) to determine if your device can support the texture given the current state.</span></span>

<span data-ttu-id="97c99-184">Questa funzione supporta i formati di file seguenti:. bmp,. DDS,. DIB,. HDR,. jpg,. PFM,. png,. ppm e. tga.</span><span class="sxs-lookup"><span data-stu-id="97c99-184">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="97c99-185">Vedere [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="97c99-185">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="97c99-186">Le trame mipmap dispongono automaticamente di ogni livello riempito con la trama caricata.</span><span class="sxs-lookup"><span data-stu-id="97c99-186">Mipmapped textures automatically have each level filled with the loaded texture.</span></span> <span data-ttu-id="97c99-187">Quando si caricano immagini in trame mipmap, alcuni dispositivi non sono in grado di passare a un'immagine 1x1 e questa funzione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="97c99-187">When loading images into mipmapped textures, some devices are unable to go to a 1x1 image and this function will fail.</span></span> <span data-ttu-id="97c99-188">In tal caso, è necessario caricare le immagini manualmente.</span><span class="sxs-lookup"><span data-stu-id="97c99-188">If this happens, then the images need to be loaded manually.</span></span>

<span data-ttu-id="97c99-189">Per prestazioni ottimali quando si usa **D3DXCreateTextureFromFileEx**:</span><span class="sxs-lookup"><span data-stu-id="97c99-189">For the best performance when using **D3DXCreateTextureFromFileEx**:</span></span>

1.  <span data-ttu-id="97c99-190">Il ridimensionamento delle immagini e la conversione del formato in fase di caricamento possono essere lenti.</span><span class="sxs-lookup"><span data-stu-id="97c99-190">Doing image scaling and format conversion at load time can be slow.</span></span> <span data-ttu-id="97c99-191">Archiviare le immagini nel formato e nella risoluzione che verranno usate.</span><span class="sxs-lookup"><span data-stu-id="97c99-191">Store images in the format and resolution they will be used.</span></span> <span data-ttu-id="97c99-192">Se l'hardware di destinazione richiede una potenza di 2 dimensioni, creare e archiviare immagini usando la potenza di 2 dimensioni.</span><span class="sxs-lookup"><span data-stu-id="97c99-192">If the target hardware requires power of 2 dimensions, then create and store images using power of 2 dimensions.</span></span>
2.  <span data-ttu-id="97c99-193">Per la creazione di un'immagine mipmap in fase di caricamento, filtrare usando la [ \_ \_ casella filtro D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="97c99-193">For mipmap image creation at load time, filter using [D3DX\_FILTER\_BOX](d3dx-filter.md).</span></span> <span data-ttu-id="97c99-194">Un filtro Box è molto più veloce di altri tipi di filtro, ad esempio il \_ triangolo di filtro D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="97c99-194">A box filter is much faster than other filter types such as D3DX\_FILTER\_TRIANGLE.</span></span>
3.  <span data-ttu-id="97c99-195">Prendere in considerazione l'uso di file DDS.</span><span class="sxs-lookup"><span data-stu-id="97c99-195">Consider using DDS files.</span></span> <span data-ttu-id="97c99-196">Poiché i file DDS possono essere usati per rappresentare qualsiasi formato di trama Direct3D 9, è molto facile per la lettura di D3DX.</span><span class="sxs-lookup"><span data-stu-id="97c99-196">Since DDS files can be used to represent any Direct3D 9 texture format, they are very easy for D3DX to read.</span></span> <span data-ttu-id="97c99-197">Inoltre, possono archiviare mipmap, in modo che sia possibile usare qualsiasi algoritmo di generazione mipmap per creare le immagini.</span><span class="sxs-lookup"><span data-stu-id="97c99-197">Also, they can store mipmaps, so any mipmap-generation algorithms can be used to author the images.</span></span>

<span data-ttu-id="97c99-198">Quando si ignorano i livelli di mipmap durante il caricamento di un file con estensione DDS, usare la \_ macro D3DX Skip \_ DDS \_ MIP \_ Levels per generare il valore MipFilter.</span><span class="sxs-lookup"><span data-stu-id="97c99-198">When skipping mipmap levels while loading a .dds file, use the D3DX\_SKIP\_DDS\_MIP\_LEVELS macro to generate the MipFilter value.</span></span> <span data-ttu-id="97c99-199">Questa macro accetta il numero di livelli da ignorare e il tipo di filtro e restituisce il valore del filtro, che viene quindi passato al parametro MipFilter.</span><span class="sxs-lookup"><span data-stu-id="97c99-199">This macro takes the number of levels to skip and the filter type and returns the filter value, which would then be passed into the MipFilter parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="97c99-200">Requisiti</span><span class="sxs-lookup"><span data-stu-id="97c99-200">Requirements</span></span>



| <span data-ttu-id="97c99-201">Requisito</span><span class="sxs-lookup"><span data-stu-id="97c99-201">Requirement</span></span> | <span data-ttu-id="97c99-202">Valore</span><span class="sxs-lookup"><span data-stu-id="97c99-202">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="97c99-203">Intestazione</span><span class="sxs-lookup"><span data-stu-id="97c99-203">Header</span></span><br/>  | <dl> <span data-ttu-id="97c99-204"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="97c99-204"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="97c99-205">Libreria</span><span class="sxs-lookup"><span data-stu-id="97c99-205">Library</span></span><br/> | <dl> <span data-ttu-id="97c99-206"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="97c99-206"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="97c99-207">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="97c99-207">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97c99-208">**D3DXCreateTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="97c99-208">**D3DXCreateTextureFromFile**</span></span>](d3dxcreatetexturefromfile.md)
</dt> <dt>

[<span data-ttu-id="97c99-209">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="97c99-209">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
