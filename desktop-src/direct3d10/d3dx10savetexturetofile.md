---
description: Salva una trama in un file.
ms.assetid: c1718903-039a-4132-b128-82e03078ef62
title: Funzione D3DX10SaveTextureToFile (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10SaveTextureToFile
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c760876160d8ce1cbc0423639a59218c79716481
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323739"
---
# <a name="d3dx10savetexturetofile-function"></a><span data-ttu-id="3b624-103">D3DX10SaveTextureToFile (funzione)</span><span class="sxs-lookup"><span data-stu-id="3b624-103">D3DX10SaveTextureToFile function</span></span>

<span data-ttu-id="3b624-104">Salva una trama in un file.</span><span class="sxs-lookup"><span data-stu-id="3b624-104">Save a texture to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b624-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3b624-105">Syntax</span></span>


```C++
HRESULT D3DX10SaveTextureToFile(
  _In_ ID3D10Resource           *pSrcTexture,
  _In_ D3DX10_IMAGE_FILE_FORMAT DestFormat,
  _In_ LPCTSTR                  pDestFile
);
```



## <a name="parameters"></a><span data-ttu-id="3b624-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3b624-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b624-107">*pSrcTexture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3b624-107">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b624-108">Tipo: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span><span class="sxs-lookup"><span data-stu-id="3b624-108">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span></span>

<span data-ttu-id="3b624-109">Puntatore alla trama da salvare.</span><span class="sxs-lookup"><span data-stu-id="3b624-109">Pointer to the texture to be saved.</span></span> <span data-ttu-id="3b624-110">Vedere [**interfaccia ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span><span class="sxs-lookup"><span data-stu-id="3b624-110">See [**ID3D10Resource Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span></span>

</dd> <dt>

<span data-ttu-id="3b624-111">*DestFormat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3b624-111">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b624-112">Tipo: **[ **d3dx10 \_ Image \_ file \_ Format**](d3dx10-image-file-format.md)**</span><span class="sxs-lookup"><span data-stu-id="3b624-112">Type: **[**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md)**</span></span>

<span data-ttu-id="3b624-113">Il formato in cui verrà salvata la trama (vedere il [**\_ formato del \_ file \_ di immagine d3dx10**](d3dx10-image-file-format.md)).</span><span class="sxs-lookup"><span data-stu-id="3b624-113">The format the texture will be saved as (see [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md)).</span></span> <span data-ttu-id="3b624-114">D3DX10 \_ IFF \_ DDS è il formato preferito perché è l'unica opzione che supporta tutti i formati nel [**\_ formato DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="3b624-114">D3DX10\_IFF\_DDS is the preferred format since it is the only option that supports all the formats in [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

</dd> <dt>

<span data-ttu-id="3b624-115">*pDestFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3b624-115">*pDestFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b624-116">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3b624-116">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3b624-117">Nome del file di output di destinazione in cui verrà salvata la trama.</span><span class="sxs-lookup"><span data-stu-id="3b624-117">Name of the destination output file where the texture will be saved.</span></span> <span data-ttu-id="3b624-118">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="3b624-118">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="3b624-119">In caso contrario, il tipo di dati viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="3b624-119">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b624-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3b624-120">Return value</span></span>

<span data-ttu-id="3b624-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3b624-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3b624-122">Il valore restituito è uno dei valori elencati nei [codici restituiti di Direct3D 10](d3d10-graphics-reference-returnvalues.md); usare il valore restituito per verificare se il *DestFormat* è supportato.</span><span class="sxs-lookup"><span data-stu-id="3b624-122">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md); use the return value to see if the *DestFormat* is supported.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b624-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="3b624-123">Remarks</span></span>

<span data-ttu-id="3b624-124">**D3DX10SaveTextureToFile** scrive la struttura [**DXT10 dell' \_ intestazione \_ DDS**](../direct3ddds/dds-header-dxt10.md) aggiuntiva per la trama di input solo se necessario, ad esempio perché la trama di input è in formato RGB standard.</span><span class="sxs-lookup"><span data-stu-id="3b624-124">**D3DX10SaveTextureToFile** writes out the extra [**DDS\_HEADER\_DXT10**](../direct3ddds/dds-header-dxt10.md) structure for the input texture only if necessary (for example, because the input texture is in standard RGB (sRGB) format).</span></span> <span data-ttu-id="3b624-125">Se **D3DX10SaveTextureToFile** scrive l' **intestazione DDS \_ \_ DXT10** structure, imposta il membro **dwFourCC** della struttura [**DDS \_ PIXELFORMAT**](../direct3ddds/dds-pixelformat.md) per la trama su **DX10** per indicare la prescense dell'intestazione **DDS \_ \_ DXT10** Extended header.</span><span class="sxs-lookup"><span data-stu-id="3b624-125">If **D3DX10SaveTextureToFile** writes out the **DDS\_HEADER\_DXT10** structure, it sets the **dwFourCC** member of the [**DDS\_PIXELFORMAT**](../direct3ddds/dds-pixelformat.md) structure for the texture to **DX10** to indicate the prescense of the **DDS\_HEADER\_DXT10** extended header.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b624-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3b624-126">Requirements</span></span>



| <span data-ttu-id="3b624-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b624-127">Requirement</span></span> | <span data-ttu-id="3b624-128">Valore</span><span class="sxs-lookup"><span data-stu-id="3b624-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b624-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3b624-129">Header</span></span><br/>  | <dl> <span data-ttu-id="3b624-130"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b624-130"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="3b624-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="3b624-131">Library</span></span><br/> | <dl> <span data-ttu-id="3b624-132"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3b624-132"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="3b624-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3b624-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b624-134">Funzioni di trama in D3DX 10</span><span class="sxs-lookup"><span data-stu-id="3b624-134">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="3b624-135">Funzioni per utilizzo generico</span><span class="sxs-lookup"><span data-stu-id="3b624-135">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
