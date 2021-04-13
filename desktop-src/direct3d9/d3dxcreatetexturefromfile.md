---
description: Crea una trama da un file.
ms.assetid: 247b0ee2-ee31-4090-b94c-41951b46675f
title: Funzione D3DXCreateTextureFromFile (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 19453986405ee4d46a3e72145c2117bb113663bd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401963"
---
# <a name="d3dxcreatetexturefromfile-function"></a><span data-ttu-id="f15ba-103">D3DXCreateTextureFromFile (funzione)</span><span class="sxs-lookup"><span data-stu-id="f15ba-103">D3DXCreateTextureFromFile function</span></span>

<span data-ttu-id="f15ba-104">Crea una trama da un file.</span><span class="sxs-lookup"><span data-stu-id="f15ba-104">Creates a texture from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="f15ba-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f15ba-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureFromFile(
  _In_  LPDIRECT3DDEVICE9  pDevice,
  _In_  LPCTSTR            pSrcFile,
  _Out_ LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a><span data-ttu-id="f15ba-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f15ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f15ba-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f15ba-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f15ba-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="f15ba-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="f15ba-109">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo da associare alla trama.</span><span class="sxs-lookup"><span data-stu-id="f15ba-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="f15ba-110">*pSrcFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f15ba-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f15ba-111">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f15ba-111">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f15ba-112">Puntatore a una stringa che specifica il nome del file.</span><span class="sxs-lookup"><span data-stu-id="f15ba-112">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="f15ba-113">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="f15ba-113">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="f15ba-114">In caso contrario, il tipo di dati String viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="f15ba-114">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="f15ba-115">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="f15ba-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f15ba-116">*ppTexture* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f15ba-116">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f15ba-117">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="f15ba-117">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="f15ba-118">Indirizzo di un puntatore a un'interfaccia [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , che rappresenta l'oggetto trama creato.</span><span class="sxs-lookup"><span data-stu-id="f15ba-118">Address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f15ba-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f15ba-119">Return value</span></span>

<span data-ttu-id="f15ba-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f15ba-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f15ba-121">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f15ba-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f15ba-122">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="f15ba-122">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="f15ba-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="f15ba-123">Remarks</span></span>

<span data-ttu-id="f15ba-124">L'impostazione del compilatore determina anche la versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="f15ba-124">The compiler setting also determines the function version.</span></span> <span data-ttu-id="f15ba-125">Se è definito Unicode, la chiamata di funzione viene risolta in D3DXCreateTextureFromFileW.</span><span class="sxs-lookup"><span data-stu-id="f15ba-125">If Unicode is defined, the function call resolves to D3DXCreateTextureFromFileW.</span></span> <span data-ttu-id="f15ba-126">In caso contrario, la chiamata di funzione viene risolta in D3DXCreateTextureFromFileA perché vengono utilizzate le stringhe ANSI.</span><span class="sxs-lookup"><span data-stu-id="f15ba-126">Otherwise, the function call resolves to D3DXCreateTextureFromFileA because ANSI strings are being used.</span></span>

<span data-ttu-id="f15ba-127">Questa funzione supporta i formati di file seguenti:. bmp,. DDS,. DIB,. HDR,. jpg,. PFM,. png,. ppm e. tga.</span><span class="sxs-lookup"><span data-stu-id="f15ba-127">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="f15ba-128">Vedere [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="f15ba-128">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="f15ba-129">La funzione è equivalente a D3DXCreateTextureFromFileEx (pDevice, pSrcFile, D3DX \_ default, D3DX \_ default, D3DX \_ default, 0, D3DFMT \_ Unknown, D3DPOOL \_ Managed, D3DX \_ default, D3DX \_ default, 0, **null**, **null**, ppTexture).</span><span class="sxs-lookup"><span data-stu-id="f15ba-129">The function is equivalent to D3DXCreateTextureFromFileEx(pDevice, pSrcFile, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppTexture).</span></span>

<span data-ttu-id="f15ba-130">Le trame mipmap dispongono automaticamente di ogni livello riempito con la trama caricata.</span><span class="sxs-lookup"><span data-stu-id="f15ba-130">Mipmapped textures automatically have each level filled with the loaded texture.</span></span>

<span data-ttu-id="f15ba-131">Quando si caricano immagini in trame mipmap, alcuni dispositivi non sono in grado di passare a un'immagine 1x1 e questa funzione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="f15ba-131">When loading images into mipmapped textures, some devices are unable to go to a 1x1 image and this function will fail.</span></span> <span data-ttu-id="f15ba-132">In tal caso, è necessario caricare le immagini manualmente.</span><span class="sxs-lookup"><span data-stu-id="f15ba-132">If this happens, the images need to be loaded manually.</span></span>

<span data-ttu-id="f15ba-133">Si noti che una risorsa creata con questa funzione verrà inserita nella classe di memoria indicata da D3DPOOL \_ gestito.</span><span class="sxs-lookup"><span data-stu-id="f15ba-133">Note that a resource created with this function will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span>

<span data-ttu-id="f15ba-134">Il filtro viene applicato automaticamente a una trama creata utilizzando questo metodo.</span><span class="sxs-lookup"><span data-stu-id="f15ba-134">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="f15ba-135">Il filtro è equivalente a D3DX Filter D3DX del filtro \_ \_ \| \_ \_ di retinazione nel [ \_ filtro D3DX](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="f15ba-135">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

<span data-ttu-id="f15ba-136">Per prestazioni ottimali quando si usa **D3DXCreateTextureFromFile**:</span><span class="sxs-lookup"><span data-stu-id="f15ba-136">For the best performance when using **D3DXCreateTextureFromFile**:</span></span>

1.  <span data-ttu-id="f15ba-137">Il ridimensionamento delle immagini e la conversione del formato in fase di caricamento possono essere lenti.</span><span class="sxs-lookup"><span data-stu-id="f15ba-137">Doing image scaling and format conversion at load time can be slow.</span></span> <span data-ttu-id="f15ba-138">Archiviare le immagini nel formato e nella risoluzione che verranno usate.</span><span class="sxs-lookup"><span data-stu-id="f15ba-138">Store images in the format and resolution they will be used.</span></span> <span data-ttu-id="f15ba-139">Se l'hardware di destinazione richiede una potenza di due dimensioni, creare e archiviare immagini usando la potenza di due dimensioni.</span><span class="sxs-lookup"><span data-stu-id="f15ba-139">If the target hardware requires power of two dimensions, create and store images using power of two dimensions.</span></span>
2.  <span data-ttu-id="f15ba-140">Prendere in considerazione l'uso di file di superficie DirectDraw (DDS).</span><span class="sxs-lookup"><span data-stu-id="f15ba-140">Consider using DirectDraw surface (DDS) files.</span></span> <span data-ttu-id="f15ba-141">Poiché i file DDS possono essere usati per rappresentare qualsiasi formato di trama Direct3D 9, è molto facile per la lettura di D3DX.</span><span class="sxs-lookup"><span data-stu-id="f15ba-141">Because DDS files can be used to represent any Direct3D 9 texture format, they are very easy for D3DX to read.</span></span> <span data-ttu-id="f15ba-142">Inoltre, possono archiviare mipmap, in modo che sia possibile usare qualsiasi algoritmo di generazione mipmap per creare le immagini.</span><span class="sxs-lookup"><span data-stu-id="f15ba-142">Also, they can store mipmaps, so any mipmap-generation algorithms can be used to author the images.</span></span>

## <a name="requirements"></a><span data-ttu-id="f15ba-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f15ba-143">Requirements</span></span>



| <span data-ttu-id="f15ba-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="f15ba-144">Requirement</span></span> | <span data-ttu-id="f15ba-145">Valore</span><span class="sxs-lookup"><span data-stu-id="f15ba-145">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f15ba-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f15ba-146">Header</span></span><br/>  | <dl> <span data-ttu-id="f15ba-147"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="f15ba-147"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="f15ba-148">Libreria</span><span class="sxs-lookup"><span data-stu-id="f15ba-148">Library</span></span><br/> | <dl> <span data-ttu-id="f15ba-149"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f15ba-149"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="f15ba-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f15ba-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f15ba-151">**D3DXCreateTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="f15ba-151">**D3DXCreateTextureFromFileEx**</span></span>](d3dxcreatetexturefromfileex.md)
</dt> <dt>

[<span data-ttu-id="f15ba-152">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="f15ba-152">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
