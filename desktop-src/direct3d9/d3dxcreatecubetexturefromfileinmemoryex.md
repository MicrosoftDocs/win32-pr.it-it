---
description: Crea una trama del cubo da un file in memoria. Si tratta di una funzione più avanzata rispetto a D3DXCreateCubeTextureFromFileInMemory.
ms.assetid: 598016eb-9ea9-4dca-a297-5708a957da6a
title: Funzione D3DXCreateCubeTextureFromFileInMemoryEx (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromFileInMemoryEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7813d4532bbde18a5fc7fd7d1d090dc72eccd61f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058672"
---
# <a name="d3dxcreatecubetexturefromfileinmemoryex-function"></a><span data-ttu-id="984ed-104">D3DXCreateCubeTextureFromFileInMemoryEx (funzione)</span><span class="sxs-lookup"><span data-stu-id="984ed-104">D3DXCreateCubeTextureFromFileInMemoryEx function</span></span>

<span data-ttu-id="984ed-105">Crea una trama del cubo da un file in memoria.</span><span class="sxs-lookup"><span data-stu-id="984ed-105">Creates a cube texture from a file in memory.</span></span> <span data-ttu-id="984ed-106">Si tratta di una funzione più avanzata rispetto a [**D3DXCreateCubeTextureFromFileInMemory**](d3dxcreatecubetexturefromfileinmemory.md).</span><span class="sxs-lookup"><span data-stu-id="984ed-106">This is a more advanced function than [**D3DXCreateCubeTextureFromFileInMemory**](d3dxcreatecubetexturefromfileinmemory.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="984ed-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="984ed-107">Syntax</span></span>


```C++
HRESULT D3DXCreateCubeTextureFromFileInMemoryEx(
  _In_    LPDIRECT3DDEVICE9      pDevice,
  _In_    LPCVOID                pSrcData,
  _In_    UINT                   SrcDataSize,
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



## <a name="parameters"></a><span data-ttu-id="984ed-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="984ed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="984ed-109">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="984ed-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="984ed-110">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="984ed-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="984ed-111">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo da associare alla trama del cubo.</span><span class="sxs-lookup"><span data-stu-id="984ed-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="984ed-112">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="984ed-112">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="984ed-113">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="984ed-113">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="984ed-114">Puntatore al file in memoria da cui creare la trama del cubo.</span><span class="sxs-lookup"><span data-stu-id="984ed-114">Pointer to the file in memory from which to create the cube texture.</span></span> <span data-ttu-id="984ed-115">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="984ed-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="984ed-116">*SrcDataSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="984ed-116">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="984ed-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="984ed-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="984ed-118">Dimensioni in byte del file in memoria.</span><span class="sxs-lookup"><span data-stu-id="984ed-118">Size of the file in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="984ed-119">*Dimensioni* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="984ed-119">*Size* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="984ed-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="984ed-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="984ed-121">Larghezza (o altezza) in pixel.</span><span class="sxs-lookup"><span data-stu-id="984ed-121">Width (or height) in pixels.</span></span> <span data-ttu-id="984ed-122">Se questo valore è zero o D3DX \_ default, le dimensioni vengono ricavate dal file.</span><span class="sxs-lookup"><span data-stu-id="984ed-122">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span>

</dd> <dt>

<span data-ttu-id="984ed-123">*MipLevels* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="984ed-123">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="984ed-124">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="984ed-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="984ed-125">Numero di livelli MIP richiesti.</span><span class="sxs-lookup"><span data-stu-id="984ed-125">Number of mip levels requested.</span></span> <span data-ttu-id="984ed-126">Se questo valore è zero o D3DX \_ default, viene creata una catena mipmap completa.</span><span class="sxs-lookup"><span data-stu-id="984ed-126">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="984ed-127">*Utilizzo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="984ed-127">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="984ed-128">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="984ed-128">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="984ed-129">0, D3DUSAGE \_ RENDERTARGET o D3DUSAGE \_ Dynamic.</span><span class="sxs-lookup"><span data-stu-id="984ed-129">0, D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="984ed-130">L'impostazione di questo flag su D3DUSAGE \_ RENDERTARGET indica che la superficie deve essere utilizzata come destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="984ed-130">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="984ed-131">La risorsa può quindi essere passata al parametro *pNewRenderTarget* del metodo [**SetRenderTarget**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="984ed-131">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="984ed-132">Se \_ viene specificato D3DUSAGE RENDERTARGET, l'applicazione deve verificare che il dispositivo supporti questa operazione chiamando [**CheckDeviceFormat**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="984ed-132">If D3DUSAGE\_RENDERTARGET is specified, the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="984ed-133">Per ulteriori informazioni sull'utilizzo di trame dinamiche, vedere [using Dynamic Textures](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="984ed-133">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="984ed-134">*Formato* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="984ed-134">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="984ed-135">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="984ed-135">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="984ed-136">Membro del tipo enumerato [D3DFORMAT](d3dformat.md) , che descrive il formato pixel richiesto per la trama del cubo.</span><span class="sxs-lookup"><span data-stu-id="984ed-136">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the cube texture.</span></span> <span data-ttu-id="984ed-137">La trama restituita potrebbe avere un formato diverso da quello specificato dal *formato*.</span><span class="sxs-lookup"><span data-stu-id="984ed-137">The returned texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="984ed-138">Le applicazioni devono verificare il formato della trama restituita.</span><span class="sxs-lookup"><span data-stu-id="984ed-138">Applications should check the format of the returned texture.</span></span> <span data-ttu-id="984ed-139">Se [D3DFMT è \_ sconosciuto](other-d3dx-constants.md), il formato viene ricavato dal file.</span><span class="sxs-lookup"><span data-stu-id="984ed-139">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="984ed-140">Se D3DFMT \_ da \_ file, il formato viene considerato esattamente come si trova nel file e la chiamata avrà esito negativo se viola le funzionalità del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="984ed-140">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="984ed-141">*Pool* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="984ed-141">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="984ed-142">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="984ed-142">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="984ed-143">Membro del tipo enumerato [**D3DPOOL**](./d3dpool.md) , che descrive la classe di memoria in cui deve essere inserita la trama del cubo.</span><span class="sxs-lookup"><span data-stu-id="984ed-143">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the cube texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="984ed-144">*Filtro* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="984ed-144">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="984ed-145">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="984ed-145">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="984ed-146">Combinazione di uno o più [ \_ filtri D3DX](d3dx-filter.md) che controllano il modo in cui l'immagine viene filtrata.</span><span class="sxs-lookup"><span data-stu-id="984ed-146">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="984ed-147">Specificare \_ il valore predefinito di D3DX per questo parametro equivale a specificare \_ il \_ \| \_ dithering del filtro D3DX del triangolo di filtro D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="984ed-147">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="984ed-148">*MipFilter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="984ed-148">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="984ed-149">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="984ed-149">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="984ed-150">Combinazione di uno o più [ \_ filtri D3DX](d3dx-filter.md) che controllano il modo in cui l'immagine viene filtrata.</span><span class="sxs-lookup"><span data-stu-id="984ed-150">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="984ed-151">La specifica \_ di D3DX default per questo parametro equivale alla specifica della \_ casella di filtro D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="984ed-151">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="984ed-152">Usare inoltre bits 27-31 per specificare il numero di livelli MIP da ignorare (dall'inizio della catena mipmap) quando una trama con estensione DDS viene caricata in memoria; Questo consente di saltare fino a 32 livelli.</span><span class="sxs-lookup"><span data-stu-id="984ed-152">In addition, use bits 27-31 to specify the number of mip levels to be skipped (from the top of the mipmap chain) when a .dds texture is loaded into memory; this allows you to skip up to 32 levels.</span></span>

</dd> <dt>

<span data-ttu-id="984ed-153">*ColorKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="984ed-153">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="984ed-154">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="984ed-154">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="984ed-155">Valore [**D3DCOLOR**](d3dcolor.md) da sostituire con nero trasparente oppure 0 per disabilitare il colorkey.</span><span class="sxs-lookup"><span data-stu-id="984ed-155">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="984ed-156">Si tratta sempre di un colore ARGB a 32 bit, indipendente dal formato di immagine di origine.</span><span class="sxs-lookup"><span data-stu-id="984ed-156">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="984ed-157">Alfa è significativo e in genere deve essere impostato su FF per le chiavi di colore opache.</span><span class="sxs-lookup"><span data-stu-id="984ed-157">Alpha is significant, and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="984ed-158">Pertanto, per il nero opaco, il valore sarà uguale a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="984ed-158">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="984ed-159">*pSrcInfo* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="984ed-159">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="984ed-160">Tipo: **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="984ed-160">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="984ed-161">Puntatore a una struttura di [**\_ informazioni D3DXIMAGE**](d3dximage-info.md) per la compilazione di una descrizione dei dati nel file di immagine di origine o **null**.</span><span class="sxs-lookup"><span data-stu-id="984ed-161">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="984ed-162">*pPalette* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="984ed-162">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="984ed-163">Tipo: **[ **PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="984ed-163">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="984ed-164">Puntatore a una struttura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , che rappresenta una tavolozza dei colori 256 da compilare o **null**.</span><span class="sxs-lookup"><span data-stu-id="984ed-164">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in, or **NULL**.</span></span> <span data-ttu-id="984ed-165">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="984ed-165">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="984ed-166">*ppCubeTexture* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="984ed-166">*ppCubeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="984ed-167">Tipo: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="984ed-167">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span></span>

<span data-ttu-id="984ed-168">Indirizzo di un puntatore a un'interfaccia [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) , che rappresenta l'oggetto trama del cubo creato.</span><span class="sxs-lookup"><span data-stu-id="984ed-168">Address of a pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the created cube texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="984ed-169">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="984ed-169">Return value</span></span>

<span data-ttu-id="984ed-170">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="984ed-170">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="984ed-171">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="984ed-171">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="984ed-172">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="984ed-172">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="984ed-173">Commenti</span><span class="sxs-lookup"><span data-stu-id="984ed-173">Remarks</span></span>

<span data-ttu-id="984ed-174">Questa funzione supporta i formati di file seguenti:. bmp,. DDS,. DIB,. HDR,. jpg,. PFM,. png,. ppm e. tga.</span><span class="sxs-lookup"><span data-stu-id="984ed-174">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="984ed-175">Vedere [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="984ed-175">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="984ed-176">Le trame del cubo differiscono dalle altre superfici perché sono raccolte di superfici.</span><span class="sxs-lookup"><span data-stu-id="984ed-176">Cube textures differ from other surfaces in that they are collections of surfaces.</span></span> <span data-ttu-id="984ed-177">Per chiamare [**SetRenderTarget**](/windows/desktop/api) con una trama del cubo, è necessario selezionare un singolo volto usando [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) e passare la superficie risultante a **SetRenderTarget** .</span><span class="sxs-lookup"><span data-stu-id="984ed-177">To call [**SetRenderTarget**](/windows/desktop/api) with a cube texture, you must select an individual face using [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) and pass the resulting surface to **SetRenderTarget** .</span></span>

<span data-ttu-id="984ed-178">Questo metodo è progettato per essere usato per il caricamento di file di immagine archiviati come RT \_ RCDATA, ovvero una risorsa definita dall'applicazione (dati non elaborati).</span><span class="sxs-lookup"><span data-stu-id="984ed-178">This method is designed to be used for loading image files stored as RT\_RCDATA, which is an application-defined resource (raw data).</span></span> <span data-ttu-id="984ed-179">In caso contrario, questo metodo avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="984ed-179">Otherwise this method will fail.</span></span>

<span data-ttu-id="984ed-180">Per informazioni dettagliate su [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry), vedere Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="984ed-180">For details on [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry), see the Platform SDK.</span></span> <span data-ttu-id="984ed-181">Si noti che, a partire da DirectX 8,0, il membro peFlags della struttura **PaletteEntry** non funziona come documentato in Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="984ed-181">Note that as of DirectX 8.0, the peFlags member of the **PALETTEENTRY** structure does not function as documented in the Platform SDK.</span></span> <span data-ttu-id="984ed-182">Il membro peFlags è ora il canale alfa per i formati pallettizzati a 8 bit.</span><span class="sxs-lookup"><span data-stu-id="984ed-182">The peFlags member is now the alpha channel for 8-bit palettized formats.</span></span>

<span data-ttu-id="984ed-183">**D3DXCreateCubeTextureFromFileInMemoryEx** usa il formato di file DirectDraw Surface (DDS).</span><span class="sxs-lookup"><span data-stu-id="984ed-183">**D3DXCreateCubeTextureFromFileInMemoryEx** uses the DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="984ed-184">L'editor di trame DirectX (Dxtex.exe) consente di generare una mappa del cubo da altri formati di file e di salvarli nel formato di file DDS.</span><span class="sxs-lookup"><span data-stu-id="984ed-184">The DirectX Texture Editor (Dxtex.exe) enables you to generate a cube map from other file formats and save it in the DDS file format.</span></span> <span data-ttu-id="984ed-185">È possibile ottenere Dxtex.exe e ottenere informazioni su di esso da DirectX SDK.</span><span class="sxs-lookup"><span data-stu-id="984ed-185">You can get Dxtex.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="984ed-186">Per informazioni su DirectX SDK, vedere [dove è DirectX SDK?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="984ed-186">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

<span data-ttu-id="984ed-187">Quando si ignorano i livelli di mipmap durante il caricamento di un file con estensione DDS, usare la \_ macro D3DX Skip \_ DDS \_ MIP \_ Levels per generare il valore MipFilter.</span><span class="sxs-lookup"><span data-stu-id="984ed-187">When skipping mipmap levels while loading a .dds file, use the D3DX\_SKIP\_DDS\_MIP\_LEVELS macro to generate the MipFilter value.</span></span> <span data-ttu-id="984ed-188">Questa macro accetta il numero di livelli da ignorare e il tipo di filtro e restituisce il valore del filtro, che viene quindi passato al parametro MipFilter.</span><span class="sxs-lookup"><span data-stu-id="984ed-188">This macro takes the number of levels to skip and the filter type and returns the filter value, which would then be passed into the MipFilter parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="984ed-189">Requisiti</span><span class="sxs-lookup"><span data-stu-id="984ed-189">Requirements</span></span>



| <span data-ttu-id="984ed-190">Requisito</span><span class="sxs-lookup"><span data-stu-id="984ed-190">Requirement</span></span> | <span data-ttu-id="984ed-191">Valore</span><span class="sxs-lookup"><span data-stu-id="984ed-191">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="984ed-192">Intestazione</span><span class="sxs-lookup"><span data-stu-id="984ed-192">Header</span></span><br/>  | <dl> <span data-ttu-id="984ed-193"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="984ed-193"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="984ed-194">Libreria</span><span class="sxs-lookup"><span data-stu-id="984ed-194">Library</span></span><br/> | <dl> <span data-ttu-id="984ed-195"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="984ed-195"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="984ed-196">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="984ed-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="984ed-197">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="984ed-197">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
