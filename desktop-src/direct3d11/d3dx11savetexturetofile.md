---
title: Funzione D3DX11SaveTextureToFile (D3DX11tex. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Nota invece di utilizzare questa funzione, è consigliabile utilizzare la libreria DirectXTex, CaptureTexture quindi SaveToXXXFile (dove XXX è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine dell'arte comune per i giochi. Per lo scenario semplificato della creazione di una schermata da una trama di destinazione di rendering, è consigliabile usare la libreria DirectXTK, SaveDDSTextureToFile o SaveWICTextureToFile. Salva una trama in un file.
ms.assetid: da161268-fb68-42dd-ba31-b090a993f369
keywords:
- Funzione D3DX11SaveTextureToFile Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11SaveTextureToFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d87188c3e58a8bea36b1cffb675c229aed71677
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982316"
---
# <a name="d3dx11savetexturetofile-function"></a><span data-ttu-id="6edf7-107">D3DX11SaveTextureToFile (funzione)</span><span class="sxs-lookup"><span data-stu-id="6edf7-107">D3DX11SaveTextureToFile function</span></span>

> [!Note]  
> <span data-ttu-id="6edf7-108">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="6edf7-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="6edf7-109">Anziché utilizzare questa funzione, è consigliabile utilizzare la libreria [DirectXTex](https://github.com/Microsoft/DirectXTex) , **CaptureTexture** quindi **SAVETOXXXFILE** (dove xxx è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine dell'arte comune per i giochi.</span><span class="sxs-lookup"><span data-stu-id="6edf7-109">Instead of using this function, we recommend that you use the [DirectXTex](https://github.com/Microsoft/DirectXTex) library, **CaptureTexture** then **SaveToXXXFile** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span> <span data-ttu-id="6edf7-110">Per lo scenario semplificato della creazione di una schermata da una trama di destinazione di rendering, è consigliabile usare la libreria [DirectXTK](https://github.com/Microsoft/DirectXTK) , **SaveDDSTextureToFile** o **SaveWICTextureToFile**.</span><span class="sxs-lookup"><span data-stu-id="6edf7-110">For the simplified scenario of creating a screen shot from a render target texture, we recommend that you use the [DirectXTK](https://github.com/Microsoft/DirectXTK) library, **SaveDDSTextureToFile** or **SaveWICTextureToFile**.</span></span>

 

<span data-ttu-id="6edf7-111">Salva una trama in un file.</span><span class="sxs-lookup"><span data-stu-id="6edf7-111">Save a texture to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="6edf7-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6edf7-112">Syntax</span></span>


```C++
HRESULT D3DX11SaveTextureToFile(
       ID3D11DeviceContext      *pContext,
  _In_ ID3D11Resource           *pSrcTexture,
  _In_ D3DX11_IMAGE_FILE_FORMAT DestFormat,
  _In_ LPCTSTR                  pDestFile
);
```



## <a name="parameters"></a><span data-ttu-id="6edf7-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="6edf7-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6edf7-114">*pContext*</span><span class="sxs-lookup"><span data-stu-id="6edf7-114">*pContext*</span></span> 
</dt> <dd>

<span data-ttu-id="6edf7-115">Tipo: **[ **sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="6edf7-115">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="6edf7-116">Puntatore a un oggetto [**sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="6edf7-116">A pointer to an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>

</dd> <dt>

<span data-ttu-id="6edf7-117">*pSrcTexture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6edf7-117">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6edf7-118">Tipo: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span><span class="sxs-lookup"><span data-stu-id="6edf7-118">Type: **[**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span></span>

<span data-ttu-id="6edf7-119">Puntatore alla trama da salvare.</span><span class="sxs-lookup"><span data-stu-id="6edf7-119">Pointer to the texture to be saved.</span></span> <span data-ttu-id="6edf7-120">Vedere [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span><span class="sxs-lookup"><span data-stu-id="6edf7-120">See [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span></span>

</dd> <dt>

<span data-ttu-id="6edf7-121">*DestFormat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6edf7-121">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6edf7-122">Tipo: **[ **D3DX11 \_ Image \_ file \_ Format**](d3dx11-image-file-format.md)**</span><span class="sxs-lookup"><span data-stu-id="6edf7-122">Type: **[**D3DX11\_IMAGE\_FILE\_FORMAT**](d3dx11-image-file-format.md)**</span></span>

<span data-ttu-id="6edf7-123">Il formato in cui verrà salvata la trama (vedere il [**\_ formato del \_ file \_ di immagine D3DX11**](d3dx11-image-file-format.md)).</span><span class="sxs-lookup"><span data-stu-id="6edf7-123">The format the texture will be saved as (see [**D3DX11\_IMAGE\_FILE\_FORMAT**](d3dx11-image-file-format.md)).</span></span> <span data-ttu-id="6edf7-124">D3DX11 \_ IFF \_ DDS è il formato preferito perché è l'unica opzione che supporta tutti i formati nel [**\_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="6edf7-124">D3DX11\_IFF\_DDS is the preferred format since it is the only option that supports all the formats in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

</dd> <dt>

<span data-ttu-id="6edf7-125">*pDestFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6edf7-125">*pDestFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6edf7-126">Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6edf7-126">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="6edf7-127">Nome del file di output di destinazione in cui verrà salvata la trama.</span><span class="sxs-lookup"><span data-stu-id="6edf7-127">Name of the destination output file where the texture will be saved.</span></span> <span data-ttu-id="6edf7-128">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="6edf7-128">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="6edf7-129">In caso contrario, il tipo di dati viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="6edf7-129">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6edf7-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6edf7-130">Return value</span></span>

<span data-ttu-id="6edf7-131">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6edf7-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6edf7-132">Il valore restituito è uno dei valori elencati in [Direct3D 11 Return code](d3d11-graphics-reference-returnvalues.md); usare il valore restituito per verificare se il *DestFormat* è supportato.</span><span class="sxs-lookup"><span data-stu-id="6edf7-132">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md); use the return value to see if the *DestFormat* is supported.</span></span>

## <a name="remarks"></a><span data-ttu-id="6edf7-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="6edf7-133">Remarks</span></span>

<span data-ttu-id="6edf7-134">**D3DX11SaveTextureToFile** scrive la struttura [**DXT10 dell' \_ intestazione \_ DDS**](/windows/desktop/direct3ddds/dds-header-dxt10) aggiuntiva per la trama di input solo se necessario, ad esempio perché la trama di input è in formato RGB standard.</span><span class="sxs-lookup"><span data-stu-id="6edf7-134">**D3DX11SaveTextureToFile** writes out the extra [**DDS\_HEADER\_DXT10**](/windows/desktop/direct3ddds/dds-header-dxt10) structure for the input texture only if necessary (for example, because the input texture is in standard RGB (sRGB) format).</span></span> <span data-ttu-id="6edf7-135">Se **D3DX11SaveTextureToFile** scrive l' **intestazione DDS \_ \_ DXT10** structure, imposta il membro **dwFourCC** della struttura [**DDS \_ PIXELFORMAT**](/windows/desktop/direct3ddds/dds-pixelformat) per la trama su **DX10** per indicare la prescense dell'intestazione **DDS \_ \_ DXT10** Extended header.</span><span class="sxs-lookup"><span data-stu-id="6edf7-135">If **D3DX11SaveTextureToFile** writes out the **DDS\_HEADER\_DXT10** structure, it sets the **dwFourCC** member of the [**DDS\_PIXELFORMAT**](/windows/desktop/direct3ddds/dds-pixelformat) structure for the texture to **DX10** to indicate the prescense of the **DDS\_HEADER\_DXT10** extended header.</span></span>

## <a name="requirements"></a><span data-ttu-id="6edf7-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6edf7-136">Requirements</span></span>



| <span data-ttu-id="6edf7-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="6edf7-137">Requirement</span></span> | <span data-ttu-id="6edf7-138">Valore</span><span class="sxs-lookup"><span data-stu-id="6edf7-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6edf7-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6edf7-139">Header</span></span><br/>  | <dl> <span data-ttu-id="6edf7-140"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="6edf7-140"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="6edf7-141">Libreria</span><span class="sxs-lookup"><span data-stu-id="6edf7-141">Library</span></span><br/> | <dl> <span data-ttu-id="6edf7-142"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6edf7-142"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="6edf7-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6edf7-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6edf7-144">Funzioni D3DX</span><span class="sxs-lookup"><span data-stu-id="6edf7-144">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

