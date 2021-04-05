---
description: Crea una trama da un file in memoria. Si tratta di una funzione più avanzata rispetto a D3DXCreateTextureFromFileInMemory.
ms.assetid: e515697c-0e24-4d96-b58a-dc4f27683021
title: Funzione D3DXCreateTextureFromFileInMemoryEx (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromFileInMemoryEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: da85af9e70a7971ba0bab1f76e9c3d30c3cc2884
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969362"
---
# <a name="d3dxcreatetexturefromfileinmemoryex-function"></a><span data-ttu-id="dbbba-104">D3DXCreateTextureFromFileInMemoryEx (funzione)</span><span class="sxs-lookup"><span data-stu-id="dbbba-104">D3DXCreateTextureFromFileInMemoryEx function</span></span>

<span data-ttu-id="dbbba-105">Crea una trama da un file in memoria.</span><span class="sxs-lookup"><span data-stu-id="dbbba-105">Creates a texture from a file in memory.</span></span> <span data-ttu-id="dbbba-106">Si tratta di una funzione più avanzata rispetto a [**D3DXCreateTextureFromFileInMemory**](d3dxcreatetexturefromfileinmemory.md).</span><span class="sxs-lookup"><span data-stu-id="dbbba-106">This is a more advanced function than [**D3DXCreateTextureFromFileInMemory**](d3dxcreatetexturefromfileinmemory.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="dbbba-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dbbba-107">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureFromFileInMemoryEx(
  _In_    LPDIRECT3DDEVICE9  pDevice,
  _In_    LPCVOID            pSrcData,
  _In_    UINT               SrcDataSize,
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



## <a name="parameters"></a><span data-ttu-id="dbbba-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="dbbba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbbba-109">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dbbba-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbbba-110">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="dbbba-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="dbbba-111">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo da associare alla trama.</span><span class="sxs-lookup"><span data-stu-id="dbbba-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="dbbba-112">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dbbba-112">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbbba-113">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dbbba-113">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dbbba-114">Puntatore al file in memoria da cui creare la trama.</span><span class="sxs-lookup"><span data-stu-id="dbbba-114">Pointer to the file in memory from which to create the texture.</span></span>

</dd> <dt>

<span data-ttu-id="dbbba-115">*SrcDataSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dbbba-115">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbbba-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dbbba-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dbbba-117">Dimensioni in byte del file in memoria.</span><span class="sxs-lookup"><span data-stu-id="dbbba-117">Size of the file in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="dbbba-118">*Larghezza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dbbba-118">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbbba-119">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dbbba-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dbbba-120">Larghezza in pixel.</span><span class="sxs-lookup"><span data-stu-id="dbbba-120">Width in pixels.</span></span> <span data-ttu-id="dbbba-121">Se questo valore è zero o D3DX \_ default, le dimensioni vengono ricavate dal file.</span><span class="sxs-lookup"><span data-stu-id="dbbba-121">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span>

</dd> <dt>

<span data-ttu-id="dbbba-122">*Altezza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dbbba-122">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbbba-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dbbba-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dbbba-124">Altezza, in pixel.</span><span class="sxs-lookup"><span data-stu-id="dbbba-124">Height, in pixels.</span></span> <span data-ttu-id="dbbba-125">Se questo valore è zero o D3DX \_ default, le dimensioni vengono ricavate dal file.</span><span class="sxs-lookup"><span data-stu-id="dbbba-125">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span>

</dd> <dt>

<span data-ttu-id="dbbba-126">*MipLevels* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dbbba-126">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbbba-127">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dbbba-127">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dbbba-128">Numero di livelli MIP richiesti.</span><span class="sxs-lookup"><span data-stu-id="dbbba-128">Number of mip levels requested.</span></span> <span data-ttu-id="dbbba-129">Se questo valore è zero o D3DX \_ default, viene creata una catena mipmap completa.</span><span class="sxs-lookup"><span data-stu-id="dbbba-129">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="dbbba-130">*Utilizzo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="dbbba-130">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbbba-131">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dbbba-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dbbba-132">0, D3DUSAGE \_ RENDERTARGET o D3DUSAGE \_ Dynamic.</span><span class="sxs-lookup"><span data-stu-id="dbbba-132">0, D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="dbbba-133">L'impostazione di questo flag su D3DUSAGE \_ RENDERTARGET indica che la superficie deve essere utilizzata come destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="dbbba-133">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="dbbba-134">La risorsa può quindi essere passata al parametro *pNewRenderTarget* del metodo [**SetRenderTarget**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="dbbba-134">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="dbbba-135">Se \_ viene specificato D3DUSAGE RENDERTARGET o D3DUSAGE \_ Dynamic, il *pool* deve essere impostato su D3DPOOL \_ default e l'applicazione deve verificare che il dispositivo supporti questa operazione chiamando [**CheckDeviceFormat**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="dbbba-135">If either D3DUSAGE\_RENDERTARGET or D3DUSAGE\_DYNAMIC is specified, *Pool* must be set to D3DPOOL\_DEFAULT, and the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="dbbba-136">Per ulteriori informazioni sull'utilizzo di trame dinamiche, vedere [using Dynamic Textures](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="dbbba-136">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbbba-137">*Formato* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dbbba-137">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbbba-138">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="dbbba-138">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="dbbba-139">Membro del tipo enumerato [D3DFORMAT](d3dformat.md) , che descrive il formato pixel richiesto per la trama.</span><span class="sxs-lookup"><span data-stu-id="dbbba-139">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the texture.</span></span> <span data-ttu-id="dbbba-140">La trama restituita potrebbe avere un formato diverso da quello specificato dal *formato*.</span><span class="sxs-lookup"><span data-stu-id="dbbba-140">The returned texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="dbbba-141">Le applicazioni devono verificare il formato della trama restituita.</span><span class="sxs-lookup"><span data-stu-id="dbbba-141">Applications should check the format of the returned texture.</span></span> <span data-ttu-id="dbbba-142">Se [D3DFMT è \_ sconosciuto](other-d3dx-constants.md), il formato viene ricavato dal file.</span><span class="sxs-lookup"><span data-stu-id="dbbba-142">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="dbbba-143">Se D3DFMT \_ da \_ file, il formato viene considerato esattamente come si trova nel file e la chiamata avrà esito negativo se viola le funzionalità del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dbbba-143">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="dbbba-144">*Pool* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="dbbba-144">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbbba-145">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="dbbba-145">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="dbbba-146">Membro del tipo enumerato [**D3DPOOL**](./d3dpool.md) , che descrive la classe di memoria in cui deve essere posizionata la trama.</span><span class="sxs-lookup"><span data-stu-id="dbbba-146">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="dbbba-147">*Filtro* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="dbbba-147">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbbba-148">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dbbba-148">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dbbba-149">Combinazione di uno o più flag che controllano il modo in cui l'immagine viene filtrata.</span><span class="sxs-lookup"><span data-stu-id="dbbba-149">Combination of one or more flags controlling how the image is filtered.</span></span> <span data-ttu-id="dbbba-150">Specificare \_ il valore predefinito di D3DX per questo parametro equivale a specificare \_ il \_ \| \_ dithering del filtro D3DX del triangolo di filtro D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="dbbba-150">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span> <span data-ttu-id="dbbba-151">Ogni filtro valido deve contenere uno dei flag nel [ \_ filtro D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="dbbba-151">Each valid filter must contain one of the flags in [D3DX\_FILTER](d3dx-filter.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbbba-152">*MipFilter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dbbba-152">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbbba-153">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dbbba-153">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dbbba-154">Combinazione di uno o più flag che controllano il modo in cui l'immagine viene filtrata.</span><span class="sxs-lookup"><span data-stu-id="dbbba-154">Combination of one or more flags controlling how the image is filtered.</span></span> <span data-ttu-id="dbbba-155">La specifica \_ di D3DX default per questo parametro equivale alla specifica della \_ casella di filtro D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="dbbba-155">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="dbbba-156">Ogni filtro valido deve contenere uno dei flag nel [ \_ filtro D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="dbbba-156">Each valid filter must contain one of the flags in [D3DX\_FILTER](d3dx-filter.md).</span></span> <span data-ttu-id="dbbba-157">Usare inoltre bits 27-31 per specificare il numero di livelli MIP da ignorare (dall'inizio della catena mipmap) quando una trama con estensione DDS viene caricata in memoria; Questo consente di saltare fino a 32 livelli.</span><span class="sxs-lookup"><span data-stu-id="dbbba-157">In addition, use bits 27-31 to specify the number of mip levels to be skipped (from the top of the mipmap chain) when a .dds texture is loaded into memory; this allows you to skip up to 32 levels.</span></span>

</dd> <dt>

<span data-ttu-id="dbbba-158">*ColorKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dbbba-158">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbbba-159">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="dbbba-159">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="dbbba-160">Valore [**D3DCOLOR**](d3dcolor.md) da sostituire con nero trasparente oppure 0 per disabilitare il colorkey.</span><span class="sxs-lookup"><span data-stu-id="dbbba-160">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="dbbba-161">Si tratta sempre di un colore ARGB a 32 bit, indipendente dal formato di immagine di origine.</span><span class="sxs-lookup"><span data-stu-id="dbbba-161">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="dbbba-162">Alfa è significativo e in genere deve essere impostato su FF per le chiavi di colore opache.</span><span class="sxs-lookup"><span data-stu-id="dbbba-162">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="dbbba-163">Pertanto, per il nero opaco, il valore sarà uguale a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="dbbba-163">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="dbbba-164">*pSrcInfo* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="dbbba-164">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dbbba-165">Tipo: **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="dbbba-165">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="dbbba-166">Puntatore a una struttura di [**\_ informazioni D3DXIMAGE**](d3dximage-info.md) per la compilazione di una descrizione dei dati nel file di immagine di origine o **null**.</span><span class="sxs-lookup"><span data-stu-id="dbbba-166">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="dbbba-167">*pPalette* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="dbbba-167">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dbbba-168">Tipo: **[ **PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="dbbba-168">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="dbbba-169">Puntatore a una struttura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , che rappresenta una tavolozza dei colori 256 da compilare o **null**.</span><span class="sxs-lookup"><span data-stu-id="dbbba-169">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in, or **NULL**.</span></span> <span data-ttu-id="dbbba-170">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="dbbba-170">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="dbbba-171">*ppTexture* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="dbbba-171">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dbbba-172">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="dbbba-172">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="dbbba-173">Indirizzo di un puntatore a un'interfaccia [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , che rappresenta l'oggetto trama creato.</span><span class="sxs-lookup"><span data-stu-id="dbbba-173">Address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbbba-174">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dbbba-174">Return value</span></span>

<span data-ttu-id="dbbba-175">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dbbba-175">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dbbba-176">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="dbbba-176">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="dbbba-177">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="dbbba-177">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbbba-178">Commenti</span><span class="sxs-lookup"><span data-stu-id="dbbba-178">Remarks</span></span>

<span data-ttu-id="dbbba-179">Questa funzione supporta i formati di file seguenti:. bmp,. DDS,. DIB,. HDR,. jpg,. PFM,. png,. ppm e. tga.</span><span class="sxs-lookup"><span data-stu-id="dbbba-179">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="dbbba-180">Vedere [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="dbbba-180">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="dbbba-181">Per informazioni dettagliate su [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry), vedere Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="dbbba-181">For details about [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry), see the Platform SDK.</span></span> <span data-ttu-id="dbbba-182">Si noti che, a partire da DirectX 8,0, il membro peFlags della struttura **PaletteEntry** non funziona come documentato in Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="dbbba-182">Note that as of DirectX 8.0, the peFlags member of the **PALETTEENTRY** structure does not function as documented in the Platform SDK.</span></span> <span data-ttu-id="dbbba-183">Il membro peFlags è ora il canale alfa per i formati pallettizzati a 8 bit.</span><span class="sxs-lookup"><span data-stu-id="dbbba-183">The peFlags member is now the alpha channel for 8-bit palettized formats.</span></span>

<span data-ttu-id="dbbba-184">Quando si ignorano i livelli di mipmap durante il caricamento di un file con estensione DDS, usare la \_ macro D3DX Skip \_ DDS \_ MIP \_ Levels per generare il valore MipFilter.</span><span class="sxs-lookup"><span data-stu-id="dbbba-184">When skipping mipmap levels while loading a .dds file, use the D3DX\_SKIP\_DDS\_MIP\_LEVELS macro to generate the MipFilter value.</span></span> <span data-ttu-id="dbbba-185">Questa macro accetta il numero di livelli da ignorare e il tipo di filtro e restituisce il valore del filtro, che viene quindi passato al parametro MipFilter.</span><span class="sxs-lookup"><span data-stu-id="dbbba-185">This macro takes the number of levels to skip and the filter type and returns the filter value, which would then be passed into the MipFilter parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbbba-186">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dbbba-186">Requirements</span></span>



| <span data-ttu-id="dbbba-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbbba-187">Requirement</span></span> | <span data-ttu-id="dbbba-188">Valore</span><span class="sxs-lookup"><span data-stu-id="dbbba-188">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dbbba-189">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dbbba-189">Header</span></span><br/>  | <dl> <span data-ttu-id="dbbba-190"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbbba-190"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="dbbba-191">Libreria</span><span class="sxs-lookup"><span data-stu-id="dbbba-191">Library</span></span><br/> | <dl> <span data-ttu-id="dbbba-192"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dbbba-192"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="dbbba-193">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dbbba-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbbba-194">**D3DXCreateTextureFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="dbbba-194">**D3DXCreateTextureFromFileInMemory**</span></span>](d3dxcreatetexturefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="dbbba-195">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="dbbba-195">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
