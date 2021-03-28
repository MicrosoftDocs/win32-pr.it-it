---
title: Funzione D3DX11CreateShaderResourceViewFromFile (D3DX11tex. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Nota invece di utilizzare questa funzione, è consigliabile utilizzare la libreria DirectXTK (Runtime), CreateXXXTextureFromFile (dove XXX è DDS o WIC) DirectXTex Library (Tools), LoadFromXXXFile (dove XXX è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine dell'arte comune per i giochi, quindi CreateShaderResourceView crea una visualizzazione risorse shader da un file.
ms.assetid: c6a23503-f511-49dc-a0dc-19932cf8f313
keywords:
- Funzione D3DX11CreateShaderResourceViewFromFile Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateShaderResourceViewFromFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05e7d710b0b379f3027591c2ff9e52c2fdd0d7a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355349"
---
# <a name="d3dx11createshaderresourceviewfromfile-function"></a><span data-ttu-id="2d287-105">D3DX11CreateShaderResourceViewFromFile (funzione)</span><span class="sxs-lookup"><span data-stu-id="2d287-105">D3DX11CreateShaderResourceViewFromFile function</span></span>

> [!Note]  
> <span data-ttu-id="2d287-106">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="2d287-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="2d287-107">Anziché utilizzare questa funzione, è consigliabile utilizzare le seguenti operazioni:</span><span class="sxs-lookup"><span data-stu-id="2d287-107">Instead of using this function, we recommend that you use these:</span></span>
>
> -   <span data-ttu-id="2d287-108">Libreria [DirectXTK](https://github.com/Microsoft/DirectXTK) (Runtime), **CREATEXXXTEXTUREFROMFILE** (dove xxx è DDS o WIC)</span><span class="sxs-lookup"><span data-stu-id="2d287-108">[DirectXTK](https://github.com/Microsoft/DirectXTK) library (runtime), **CreateXXXTextureFromFile** (where XXX is DDS or WIC)</span></span>
> -   <span data-ttu-id="2d287-109">Libreria [DirectXTex](https://github.com/Microsoft/DirectXTex) (strumenti), **LOADFROMXXXFILE** (dove xxx è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine dell'arte comune per i giochi, quindi **CreateShaderResourceView**</span><span class="sxs-lookup"><span data-stu-id="2d287-109">[DirectXTex](https://github.com/Microsoft/DirectXTex) library (tools), **LoadFromXXXFile** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then **CreateShaderResourceView**</span></span>

 

<span data-ttu-id="2d287-110">Creare una visualizzazione risorse shader da un file.</span><span class="sxs-lookup"><span data-stu-id="2d287-110">Create a shader-resource view from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d287-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2d287-111">Syntax</span></span>


```C++
HRESULT D3DX11CreateShaderResourceViewFromFile(
  _In_  ID3D11Device             *pDevice,
  _In_  LPCTSTR                  pSrcFile,
  _In_  D3DX11_IMAGE_LOAD_INFO   *pLoadInfo,
  _In_  ID3DX11ThreadPump        *pPump,
  _Out_ ID3D11ShaderResourceView **ppShaderResourceView,
  _Out_ HRESULT                  *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="2d287-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="2d287-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d287-113">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2d287-113">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d287-114">Tipo: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span><span class="sxs-lookup"><span data-stu-id="2d287-114">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span></span>

<span data-ttu-id="2d287-115">Un puntatore al dispositivo (vedere [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) che utilizzerà la risorsa.</span><span class="sxs-lookup"><span data-stu-id="2d287-115">A pointer to the device (see [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="2d287-116">*pSrcFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2d287-116">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d287-117">Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2d287-117">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2d287-118">Nome del file che contiene la visualizzazione delle risorse dello shader.</span><span class="sxs-lookup"><span data-stu-id="2d287-118">Name of the file that contains the shader-resource view.</span></span> <span data-ttu-id="2d287-119">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="2d287-119">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="2d287-120">In caso contrario, il tipo di dati viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="2d287-120">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="2d287-121">*pLoadInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2d287-121">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d287-122">Tipo: **[ **D3DX11 \_ Image \_ Load \_ info**](d3dx11-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="2d287-122">Type: **[**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)\***</span></span>

<span data-ttu-id="2d287-123">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="2d287-123">Optional.</span></span> <span data-ttu-id="2d287-124">Identifica le caratteristiche di una trama (vedere [**D3DX11 \_ Image \_ Load \_ info**](d3dx11-image-load-info.md)) quando viene creato il processore di dati; impostare questa proprietà su **null** per leggere le caratteristiche di una trama quando viene caricata la trama.</span><span class="sxs-lookup"><span data-stu-id="2d287-124">Identifies the characteristics of a texture (see [**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="2d287-125">*pPump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2d287-125">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d287-126">Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="2d287-126">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="2d287-127">Puntatore a un'interfaccia della pompa di thread (vedere [**interfaccia ID3DX11ThreadPump**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="2d287-127">Pointer to a thread-pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="2d287-128">Se viene specificato **null** , questa funzione verrà comportata in modo sincrono e non verrà restituita finché non viene completata.</span><span class="sxs-lookup"><span data-stu-id="2d287-128">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="2d287-129">*ppShaderResourceView* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2d287-129">*ppShaderResourceView* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d287-130">Tipo: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="2d287-130">Type: **[**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span></span>

<span data-ttu-id="2d287-131">Indirizzo di un puntatore alla visualizzazione risorse shader (vedere [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)).</span><span class="sxs-lookup"><span data-stu-id="2d287-131">Address of a pointer to the shader-resource view (see [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)).</span></span>

</dd> <dt>

<span data-ttu-id="2d287-132">*pHResult* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2d287-132">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d287-133">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="2d287-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="2d287-134">Puntatore al valore restituito.</span><span class="sxs-lookup"><span data-stu-id="2d287-134">A pointer to the return value.</span></span> <span data-ttu-id="2d287-135">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="2d287-135">May be **NULL**.</span></span> <span data-ttu-id="2d287-136">Se *pPump* non è **null**, *pHResult* deve essere una posizione di memoria valida fino al completamento dell'esecuzione asincrona.</span><span class="sxs-lookup"><span data-stu-id="2d287-136">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d287-137">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2d287-137">Return value</span></span>

<span data-ttu-id="2d287-138">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2d287-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2d287-139">Il valore restituito è uno dei valori elencati nei [codici restituiti di Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="2d287-139">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2d287-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="2d287-140">Remarks</span></span>

<span data-ttu-id="2d287-141">Per un elenco dei formati di immagine supportati, vedere [**D3DX11 \_ Image \_ file \_ Format**](d3dx11-image-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="2d287-141">For a list of supported image formats, see [**D3DX11\_IMAGE\_FILE\_FORMAT**](d3dx11-image-file-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2d287-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2d287-142">Requirements</span></span>



| <span data-ttu-id="2d287-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d287-143">Requirement</span></span> | <span data-ttu-id="2d287-144">Valore</span><span class="sxs-lookup"><span data-stu-id="2d287-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d287-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2d287-145">Header</span></span><br/>  | <dl> <span data-ttu-id="2d287-146"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d287-146"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="2d287-147">Libreria</span><span class="sxs-lookup"><span data-stu-id="2d287-147">Library</span></span><br/> | <dl> <span data-ttu-id="2d287-148"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d287-148"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="2d287-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2d287-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d287-150">Funzioni D3DX</span><span class="sxs-lookup"><span data-stu-id="2d287-150">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

