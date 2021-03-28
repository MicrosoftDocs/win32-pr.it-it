---
title: Funzione D3DX11CreateShaderResourceViewFromResource (D3DX11tex. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Nota invece di utilizzare questa funzione, è consigliabile utilizzare le funzioni delle risorse, quindi la libreria DirectXTK (Runtime), CreateXXXTextureFromMemory (dove XXX è DDS o WIC) DirectXTex Library (Tools), LoadFromXXXMemory (dove XXX è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine dell'arte comune per i giochi, quindi CreateShaderResourceView crea una visualizzazione delle risorse shader da una risorsa.
ms.assetid: 64620e6d-fc0d-4411-8744-d9d8ffe6ccb8
keywords:
- Funzione D3DX11CreateShaderResourceViewFromResource Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateShaderResourceViewFromResource
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb374bd569cb58451461a7fe269c58c200895b7a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996005"
---
# <a name="d3dx11createshaderresourceviewfromresource-function"></a><span data-ttu-id="ae267-105">D3DX11CreateShaderResourceViewFromResource (funzione)</span><span class="sxs-lookup"><span data-stu-id="ae267-105">D3DX11CreateShaderResourceViewFromResource function</span></span>

> [!Note]  
> <span data-ttu-id="ae267-106">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="ae267-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="ae267-107">Anziché utilizzare questa funzione, è consigliabile utilizzare le funzioni della [risorsa](/windows/desktop/menurc/resources-functions), quindi:</span><span class="sxs-lookup"><span data-stu-id="ae267-107">Instead of using this function, we recommend that you use [resource functions](/windows/desktop/menurc/resources-functions), then these:</span></span>
>
> -   <span data-ttu-id="ae267-108">Libreria [DirectXTK](https://github.com/Microsoft/DirectXTK) (Runtime), **CREATEXXXTEXTUREFROMMEMORY** (dove xxx è DDS o WIC)</span><span class="sxs-lookup"><span data-stu-id="ae267-108">[DirectXTK](https://github.com/Microsoft/DirectXTK) library (runtime), **CreateXXXTextureFromMemory** (where XXX is DDS or WIC)</span></span>
> -   <span data-ttu-id="ae267-109">Libreria [DirectXTex](https://github.com/Microsoft/DirectXTex) (strumenti), **LOADFROMXXXMEMORY** (dove xxx è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine dell'arte comune per i giochi, quindi **CreateShaderResourceView**</span><span class="sxs-lookup"><span data-stu-id="ae267-109">[DirectXTex](https://github.com/Microsoft/DirectXTex) library (tools), **LoadFromXXXMemory** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then **CreateShaderResourceView**</span></span>

 

<span data-ttu-id="ae267-110">Creare una visualizzazione risorse shader da una risorsa.</span><span class="sxs-lookup"><span data-stu-id="ae267-110">Create a shader-resource view from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae267-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ae267-111">Syntax</span></span>


```C++
HRESULT D3DX11CreateShaderResourceViewFromResource(
  _In_  ID3D11Device             *pDevice,
  _In_  HMODULE                  hSrcModule,
  _In_  LPCTSTR                  pSrcResource,
  _In_  D3DX11_IMAGE_LOAD_INFO   *pLoadInfo,
  _In_  ID3DX11ThreadPump        *pPump,
  _Out_ ID3D11ShaderResourceView **ppShaderResourceView,
  _Out_ HRESULT                  *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="ae267-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="ae267-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae267-113">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ae267-113">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae267-114">Tipo: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span><span class="sxs-lookup"><span data-stu-id="ae267-114">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span></span>

<span data-ttu-id="ae267-115">Un puntatore al dispositivo (vedere [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) che utilizzerà la risorsa.</span><span class="sxs-lookup"><span data-stu-id="ae267-115">A pointer to the device (see [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="ae267-116">*hSrcModule* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ae267-116">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae267-117">Tipo: **[ **hmodule**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ae267-117">Type: **[**HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ae267-118">Handle per il modulo della risorsa che contiene la visualizzazione delle risorse dello shader.</span><span class="sxs-lookup"><span data-stu-id="ae267-118">Handle to the resource module containing the shader-resource view.</span></span> <span data-ttu-id="ae267-119">HMODULE può essere ottenuto con la [funzione GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span><span class="sxs-lookup"><span data-stu-id="ae267-119">HMODULE can be obtained with [GetModuleHandle Function](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="ae267-120">*pSrcResource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ae267-120">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae267-121">Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ae267-121">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ae267-122">Nome della visualizzazione risorse dello shader in hSrcModule.</span><span class="sxs-lookup"><span data-stu-id="ae267-122">Name of the shader resource view in hSrcModule.</span></span> <span data-ttu-id="ae267-123">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="ae267-123">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="ae267-124">In caso contrario, il tipo di dati viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="ae267-124">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="ae267-125">*pLoadInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ae267-125">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae267-126">Tipo: **[ **D3DX11 \_ Image \_ Load \_ info**](d3dx11-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="ae267-126">Type: **[**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)\***</span></span>

<span data-ttu-id="ae267-127">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="ae267-127">Optional.</span></span> <span data-ttu-id="ae267-128">Identifica le caratteristiche di una trama (vedere [**D3DX11 \_ Image \_ Load \_ info**](d3dx11-image-load-info.md)) quando viene creato il processore di dati; impostare questa proprietà su **null** per leggere le caratteristiche di una trama quando viene caricata la trama.</span><span class="sxs-lookup"><span data-stu-id="ae267-128">Identifies the characteristics of a texture (see [**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="ae267-129">*pPump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ae267-129">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae267-130">Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="ae267-130">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="ae267-131">Puntatore a un'interfaccia della pompa di thread (vedere [**interfaccia ID3DX11ThreadPump**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="ae267-131">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="ae267-132">Se viene specificato **null** , questa funzione verrà comportata in modo sincrono e non verrà restituita finché non viene completata.</span><span class="sxs-lookup"><span data-stu-id="ae267-132">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="ae267-133">*ppShaderResourceView* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ae267-133">*ppShaderResourceView* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae267-134">Tipo: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="ae267-134">Type: **[**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span></span>

<span data-ttu-id="ae267-135">Indirizzo di un puntatore alla visualizzazione risorse shader (vedere [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)).</span><span class="sxs-lookup"><span data-stu-id="ae267-135">Address of a pointer to the shader-resource view (see [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)).</span></span>

</dd> <dt>

<span data-ttu-id="ae267-136">*pHResult* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ae267-136">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae267-137">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="ae267-137">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="ae267-138">Puntatore al valore restituito.</span><span class="sxs-lookup"><span data-stu-id="ae267-138">A pointer to the return value.</span></span> <span data-ttu-id="ae267-139">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="ae267-139">May be **NULL**.</span></span> <span data-ttu-id="ae267-140">Se *pPump* non è **null**, *pHResult* deve essere una posizione di memoria valida fino al completamento dell'esecuzione asincrona.</span><span class="sxs-lookup"><span data-stu-id="ae267-140">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae267-141">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ae267-141">Return value</span></span>

<span data-ttu-id="ae267-142">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ae267-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ae267-143">Il valore restituito è uno dei valori elencati nei [codici restituiti di Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="ae267-143">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ae267-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ae267-144">Requirements</span></span>



| <span data-ttu-id="ae267-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae267-145">Requirement</span></span> | <span data-ttu-id="ae267-146">Valore</span><span class="sxs-lookup"><span data-stu-id="ae267-146">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae267-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ae267-147">Header</span></span><br/>  | <dl> <span data-ttu-id="ae267-148"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae267-148"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="ae267-149">Libreria</span><span class="sxs-lookup"><span data-stu-id="ae267-149">Library</span></span><br/> | <dl> <span data-ttu-id="ae267-150"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ae267-150"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ae267-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ae267-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae267-152">Funzioni D3DX</span><span class="sxs-lookup"><span data-stu-id="ae267-152">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

