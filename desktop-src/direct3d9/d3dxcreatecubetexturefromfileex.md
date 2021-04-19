---
description: Crea una trama del cubo da un file. Si tratta di una funzione più avanzata rispetto a D3DXCreateCubeTextureFromFile.
ms.assetid: 77e64b33-9282-42fa-978c-a93fa9ba11fc
title: Funzione D3DXCreateCubeTextureFromFileEx (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromFileEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b4f56ad3f8e314f7ceb5f4efb07562257efab5fa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323421"
---
# <a name="d3dxcreatecubetexturefromfileex-function"></a><span data-ttu-id="ab4ab-104">D3DXCreateCubeTextureFromFileEx (funzione)</span><span class="sxs-lookup"><span data-stu-id="ab4ab-104">D3DXCreateCubeTextureFromFileEx function</span></span>

<span data-ttu-id="ab4ab-105">Crea una trama del cubo da un file.</span><span class="sxs-lookup"><span data-stu-id="ab4ab-105">Creates a cube texture from a file.</span></span> <span data-ttu-id="ab4ab-106">Si tratta di una funzione più avanzata rispetto a [**D3DXCreateCubeTextureFromFile**](d3dxcreatecubetexturefromfile.md).</span><span class="sxs-lookup"><span data-stu-id="ab4ab-106">This is a more advanced function than [**D3DXCreateCubeTextureFromFile**](d3dxcreatecubetexturefromfile.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ab4ab-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ab4ab-107">Syntax</span></span>


```C++
HRESULT D3DXCreateCubeTextureFromFileEx(
  _In_  LPDIRECT3DDEVICE9      pDevice,
  _In_  LPCTSTR                pSrcFile,
  _In_  UINT                   Size,
  _In_  UINT                   MipLevels,
  _In_  DWORD                  Usage,
  _In_  D3DFORMAT              Format,
  _In_  D3DPOOL                Pool,
  _In_  DWORD                  Filter,
  _In_  DWORD                  MipFilter,
  _In_  D3DCOLOR               ColorKey,
  _Out_ D3DXIMAGE_INFO         *pSrcInfo,
  _Out_ PALETTEENTRY           *pPalette,
  _Out_ LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="ab4ab-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ab4ab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab4ab-109">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab4ab-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab4ab-110">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="ab4ab-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="ab4ab-111">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo da associare alla trama del cubo.</span><span class="sxs-lookup"><span data-stu-id="ab4ab-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="ab4ab-112">*pSrcFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab4ab-112">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab4ab-113">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab4ab-113">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ab4ab-114">Puntatore a una stringa che specifica il nome del file.</span><span class="sxs-lookup"><span data-stu-id="ab4ab-114">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="ab4ab-115">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="ab4ab-115">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="ab4ab-116">In caso contrario, il tipo di dati String viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="ab4ab-116">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="ab4ab-117">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="ab4ab-117">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ab4ab-118">*Dimensioni* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab4ab-118">*Size* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab4ab-119">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab4ab-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ab4ab-120">Larghezza e altezza della trama del cubo, in pixel.</span><span class="sxs-lookup"><span data-stu-id="ab4ab-120">Width and height of the cube texture, in pixels.</span></span> <span data-ttu-id="ab4ab-121">Se, ad esempio, la trama del cubo è un cubo da 8 pixel a 8 pixel, il valore di questo parametro deve essere 8.</span><span class="sxs-lookup"><span data-stu-id="ab4ab-121">For example, if the cube texture is an 8-pixel by 8-pixel cube, the value for this parameter should be 8.</span></span> <span data-ttu-id="ab4ab-122">Se questo valore è 0 o D3DX \_ predefinito, le dimensioni vengono ricavate dal file.</span><span class="sxs-lookup"><span data-stu-id="ab4ab-122">If this value is 0 or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span>

</dd> <dt>

<span data-ttu-id="ab4ab-123">*MipLevels* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab4ab-123">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab4ab-124">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab4ab-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ab4ab-125">Numero di livelli MIP richiesti.</span><span class="sxs-lookup"><span data-stu-id="ab4ab-125">Number of mip levels requested.</span></span> <span data-ttu-id="ab4ab-126">Se questo valore è zero o D3DX \_ default, viene creata una catena mipmap completa.</span><span class="sxs-lookup"><span data-stu-id="ab4ab-126">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="ab4ab-127">*Utilizzo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="ab4ab-127">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab4ab-128">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab4ab-128">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ab4ab-129">0 o D3DUSAGE \_ RENDERTARGET o D3DUSAGE \_ Dynamic.</span><span class="sxs-lookup"><span data-stu-id="ab4ab-129">0 or D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="ab4ab-130">L'impostazione di questo flag su D3DUSAGE \_ RENDERTARGET indica che la superficie deve essere utilizzata come destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="ab4ab-130">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="ab4ab-131">La risorsa può quindi essere passata al parametro *pNewRenderTarget* del metodo [**SetRenderTarget**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="ab4ab-131">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="ab4ab-132">Se \_ viene specificato D3DUSAGE RENDERTARGET, l'applicazione deve verificare che il dispositivo supporti questa operazione chiamando [**CheckDeviceFormat**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="ab4ab-132">If D3DUSAGE\_RENDERTARGET is specified, the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="ab4ab-133">D3DUSAGE \_ Dynamic indica che la superficie deve essere gestita dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="ab4ab-133">D3DUSAGE\_DYNAMIC indicates that the surface should be handled dynamically.</span></span> <span data-ttu-id="ab4ab-134">Per ulteriori informazioni sull'utilizzo di trame dinamiche, vedere [using Dynamic Textures](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="ab4ab-134">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="ab4ab-135">*Formato* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab4ab-135">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab4ab-136">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="ab4ab-136">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="ab4ab-137">Membro del tipo enumerato [D3DFORMAT](d3dformat.md) , che descrive il formato pixel richiesto per la trama del cubo.</span><span class="sxs-lookup"><span data-stu-id="ab4ab-137">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the cube texture.</span></span> <span data-ttu-id="ab4ab-138">La trama del cubo restituita potrebbe avere un formato diverso da quello specificato dal *formato*.</span><span class="sxs-lookup"><span data-stu-id="ab4ab-138">The returned cube texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="ab4ab-139">Le applicazioni devono controllare il formato della trama del cubo restituita.</span><span class="sxs-lookup"><span data-stu-id="ab4ab-139">Applications should check the format of the returned cube texture.</span></span> <span data-ttu-id="ab4ab-140">Se [D3DFMT è \_ sconosciuto](other-d3dx-constants.md), il formato viene ricavato dal file.</span><span class="sxs-lookup"><span data-stu-id="ab4ab-140">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="ab4ab-141">Se D3DFMT \_ da \_ file, il formato viene considerato esattamente come si trova nel file e la chiamata avrà esito negativo se viola le funzionalità del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ab4ab-141">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="ab4ab-142">*Pool* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="ab4ab-142">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab4ab-143">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="ab4ab-143">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="ab4ab-144">Membro del tipo enumerato [**D3DPOOL**](./d3dpool.md) , che descrive la classe di memoria in cui deve essere inserita la trama del cubo.</span><span class="sxs-lookup"><span data-stu-id="ab4ab-144">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the cube texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="ab4ab-145">*Filtro* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="ab4ab-145">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab4ab-146">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab4ab-146">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ab4ab-147">Combinazione di una o più costanti [di \_ filtro D3DX](d3dx-filter.md) , che controllano il modo in cui l'immagine viene filtrata.</span><span class="sxs-lookup"><span data-stu-id="ab4ab-147">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) constants, controlling how the image is filtered.</span></span> <span data-ttu-id="ab4ab-148">Specificare \_ il valore predefinito di D3DX per questo parametro equivale a specificare \_ il \_ \| \_ dithering del filtro D3DX del triangolo di filtro D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="ab4ab-148">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="ab4ab-149">*MipFilter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab4ab-149">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab4ab-150">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab4ab-150">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ab4ab-151">Combinazione di una o più costanti [di \_ filtro D3DX](d3dx-filter.md) che controllano il modo in cui l'immagine viene filtrata.</span><span class="sxs-lookup"><span data-stu-id="ab4ab-151">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) constants controlling how the image is filtered.</span></span> <span data-ttu-id="ab4ab-152">La specifica \_ di D3DX default per questo parametro equivale alla specifica della \_ casella di filtro D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="ab4ab-152">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="ab4ab-153">Usare inoltre bits 27-31 per specificare il numero di livelli MIP da ignorare (dall'inizio della catena mipmap) quando una trama con estensione DDS viene caricata in memoria; Questo consente di saltare fino a 32 livelli.</span><span class="sxs-lookup"><span data-stu-id="ab4ab-153">In addition, use bits 27-31 to specify the number of mip levels to be skipped (from the top of the mipmap chain) when a .dds texture is loaded into memory; this allows you to skip up to 32 levels.</span></span>

</dd> <dt>

<span data-ttu-id="ab4ab-154">*ColorKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab4ab-154">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab4ab-155">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="ab4ab-155">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="ab4ab-156">Valore [**D3DCOLOR**](d3dcolor.md) da sostituire con nero trasparente oppure 0 per disabilitare il colorkey.</span><span class="sxs-lookup"><span data-stu-id="ab4ab-156">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="ab4ab-157">Si tratta sempre di un colore ARGB a 32 bit, indipendente dal formato di immagine di origine.</span><span class="sxs-lookup"><span data-stu-id="ab4ab-157">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="ab4ab-158">Alfa è significativo e in genere deve essere impostato su FF per le chiavi di colore opache.</span><span class="sxs-lookup"><span data-stu-id="ab4ab-158">Alpha is significant, and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="ab4ab-159">Pertanto, per il nero opaco, il valore sarà uguale a 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="ab4ab-159">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="ab4ab-160">*pSrcInfo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ab4ab-160">*pSrcInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab4ab-161">Tipo: **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="ab4ab-161">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="ab4ab-162">Puntatore a una struttura di [**\_ informazioni D3DXIMAGE**](d3dximage-info.md) per la compilazione di una descrizione dei dati nel file di immagine di origine o **null**.</span><span class="sxs-lookup"><span data-stu-id="ab4ab-162">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ab4ab-163">*pPalette* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ab4ab-163">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab4ab-164">Tipo: **[ **PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="ab4ab-164">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="ab4ab-165">Puntatore a una struttura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , che rappresenta una tavolozza dei colori 256 da compilare o **null**.</span><span class="sxs-lookup"><span data-stu-id="ab4ab-165">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ab4ab-166">*ppCubeTexture* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ab4ab-166">*ppCubeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab4ab-167">Tipo: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="ab4ab-167">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span></span>

<span data-ttu-id="ab4ab-168">Indirizzo di un puntatore a un'interfaccia [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) , che rappresenta l'oggetto trama del cubo creato.</span><span class="sxs-lookup"><span data-stu-id="ab4ab-168">Address of a pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the created cube texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab4ab-169">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ab4ab-169">Return value</span></span>

<span data-ttu-id="ab4ab-170">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ab4ab-170">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ab4ab-171">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ab4ab-171">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ab4ab-172">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="ab4ab-172">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab4ab-173">Commenti</span><span class="sxs-lookup"><span data-stu-id="ab4ab-173">Remarks</span></span>

<span data-ttu-id="ab4ab-174">L'impostazione del compilatore determina anche la versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="ab4ab-174">The compiler setting also determines the function version.</span></span> <span data-ttu-id="ab4ab-175">Se è definito Unicode, la chiamata di funzione viene risolta in **D3DXCreateCubeTextureFromFileExW**.</span><span class="sxs-lookup"><span data-stu-id="ab4ab-175">If Unicode is defined, the function call resolves to **D3DXCreateCubeTextureFromFileExW**.</span></span> <span data-ttu-id="ab4ab-176">In caso contrario, la chiamata di funzione viene risolta in **D3DXCreateCubeTextureFromFileExA** perché vengono utilizzate le stringhe ANSI.</span><span class="sxs-lookup"><span data-stu-id="ab4ab-176">Otherwise, the function call resolves to **D3DXCreateCubeTextureFromFileExA** because ANSI strings are being used.</span></span>

<span data-ttu-id="ab4ab-177">Questa funzione supporta i formati di file seguenti:. bmp,. DDS,. DIB,. HDR,. jpg,. PFM,. png,. ppm e. tga.</span><span class="sxs-lookup"><span data-stu-id="ab4ab-177">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="ab4ab-178">Vedere [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="ab4ab-178">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="ab4ab-179">Le trame del cubo differiscono dalle altre superfici perché sono raccolte di superfici.</span><span class="sxs-lookup"><span data-stu-id="ab4ab-179">Cube textures differ from other surfaces in that they are collections of surfaces.</span></span> <span data-ttu-id="ab4ab-180">Per chiamare [**SetRenderTarget**](/windows/desktop/api) con una trama del cubo, è necessario selezionare un singolo volto usando [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) e passare la superficie risultante a **SetRenderTarget**.</span><span class="sxs-lookup"><span data-stu-id="ab4ab-180">To call [**SetRenderTarget**](/windows/desktop/api) with a cube texture, you must select an individual face using [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) and pass the resulting surface to **SetRenderTarget**.</span></span>

<span data-ttu-id="ab4ab-181">**D3DXCreateCubeTextureFromFileEx** usa il formato di file DirectDraw Surface (DDS).</span><span class="sxs-lookup"><span data-stu-id="ab4ab-181">**D3DXCreateCubeTextureFromFileEx** uses the DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="ab4ab-182">L'editor di trame DirectX (Dxtex.exe) consente di generare una mappa del cubo da altri formati di file e di salvarli nel formato di file DDS.</span><span class="sxs-lookup"><span data-stu-id="ab4ab-182">The DirectX Texture Editor (Dxtex.exe) enables you to generate a cube map from other file formats and save it in the DDS file format.</span></span> <span data-ttu-id="ab4ab-183">È possibile ottenere Dxtex.exe e ottenere informazioni su di esso da DirectX SDK.</span><span class="sxs-lookup"><span data-stu-id="ab4ab-183">You can get Dxtex.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="ab4ab-184">Per informazioni su DirectX SDK, vedere [dove è DirectX SDK?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="ab4ab-184">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

<span data-ttu-id="ab4ab-185">Quando si ignorano i livelli di mipmap durante il caricamento di un file con estensione DDS, usare la \_ macro D3DX Skip \_ DDS \_ MIP \_ Levels per generare il valore MipFilter.</span><span class="sxs-lookup"><span data-stu-id="ab4ab-185">When skipping mipmap levels while loading a .dds file, use the D3DX\_SKIP\_DDS\_MIP\_LEVELS macro to generate the MipFilter value.</span></span> <span data-ttu-id="ab4ab-186">Questa macro accetta il numero di livelli da ignorare e il tipo di filtro e restituisce il valore del filtro, che viene quindi passato al parametro MipFilter.</span><span class="sxs-lookup"><span data-stu-id="ab4ab-186">This macro takes the number of levels to skip and the filter type and returns the filter value, which would then be passed into the MipFilter parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab4ab-187">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ab4ab-187">Requirements</span></span>



| <span data-ttu-id="ab4ab-188">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab4ab-188">Requirement</span></span> | <span data-ttu-id="ab4ab-189">Valore</span><span class="sxs-lookup"><span data-stu-id="ab4ab-189">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ab4ab-190">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ab4ab-190">Header</span></span><br/>  | <dl> <span data-ttu-id="ab4ab-191"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab4ab-191"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="ab4ab-192">Libreria</span><span class="sxs-lookup"><span data-stu-id="ab4ab-192">Library</span></span><br/> | <dl> <span data-ttu-id="ab4ab-193"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ab4ab-193"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ab4ab-194">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ab4ab-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab4ab-195">**D3DXCreateCubeTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="ab4ab-195">**D3DXCreateCubeTextureFromFile**</span></span>](d3dxcreatecubetexturefromfile.md)
</dt> <dt>

[<span data-ttu-id="ab4ab-196">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="ab4ab-196">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
