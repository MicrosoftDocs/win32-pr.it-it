---
title: Funzione D3DX11CreateShaderResourceViewFromMemory (D3DX11tex. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Nota invece di utilizzare questa funzione, è consigliabile utilizzare la libreria DirectXTK (Runtime), CreateXXXTextureFromMemory (dove XXX è DDS o WIC) DirectXTex Library (Tools), LoadFromXXXMemory (dove XXX è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine dell'arte comune per i giochi, quindi CreateShaderResourceView crea una visualizzazione risorse shader da un file in memoria.
ms.assetid: fd75b187-2c9c-403c-8327-c312c4cda238
keywords:
- Funzione D3DX11CreateShaderResourceViewFromMemory Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateShaderResourceViewFromMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c0730fafdeb85cc22944f282eaaf556a1cdb12d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996008"
---
# <a name="d3dx11createshaderresourceviewfrommemory-function"></a><span data-ttu-id="b8d75-105">D3DX11CreateShaderResourceViewFromMemory (funzione)</span><span class="sxs-lookup"><span data-stu-id="b8d75-105">D3DX11CreateShaderResourceViewFromMemory function</span></span>

> [!Note]  
> <span data-ttu-id="b8d75-106">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="b8d75-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="b8d75-107">Anziché utilizzare questa funzione, è consigliabile utilizzare le seguenti operazioni:</span><span class="sxs-lookup"><span data-stu-id="b8d75-107">Instead of using this function, we recommend that you use these:</span></span>
>
> -   <span data-ttu-id="b8d75-108">Libreria [DirectXTK](https://github.com/Microsoft/DirectXTK) (Runtime), **CREATEXXXTEXTUREFROMMEMORY** (dove xxx è DDS o WIC)</span><span class="sxs-lookup"><span data-stu-id="b8d75-108">[DirectXTK](https://github.com/Microsoft/DirectXTK) library (runtime), **CreateXXXTextureFromMemory** (where XXX is DDS or WIC)</span></span>
> -   <span data-ttu-id="b8d75-109">Libreria [DirectXTex](https://github.com/Microsoft/DirectXTex) (strumenti), **LOADFROMXXXMEMORY** (dove xxx è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine dell'arte comune per i giochi, quindi **CreateShaderResourceView**</span><span class="sxs-lookup"><span data-stu-id="b8d75-109">[DirectXTex](https://github.com/Microsoft/DirectXTex) library (tools), **LoadFromXXXMemory** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then **CreateShaderResourceView**</span></span>

 

<span data-ttu-id="b8d75-110">Creare una visualizzazione risorse shader da un file in memoria.</span><span class="sxs-lookup"><span data-stu-id="b8d75-110">Create a shader-resource view from a file in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8d75-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b8d75-111">Syntax</span></span>


```C++
HRESULT D3DX11CreateShaderResourceViewFromMemory(
  _In_  ID3D11Device             *pDevice,
  _In_  LPCVOID                  pSrcData,
  _In_  SIZE_T                   SrcDataSize,
  _In_  D3DX11_IMAGE_LOAD_INFO   *pLoadInfo,
  _In_  ID3DX11ThreadPump        *pPump,
  _Out_ ID3D11ShaderResourceView **ppShaderResourceView,
  _Out_ HRESULT                  *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="b8d75-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="b8d75-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8d75-113">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b8d75-113">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8d75-114">Tipo: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span><span class="sxs-lookup"><span data-stu-id="b8d75-114">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span></span>

<span data-ttu-id="b8d75-115">Un puntatore al dispositivo (vedere [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) che utilizzerà la risorsa.</span><span class="sxs-lookup"><span data-stu-id="b8d75-115">A pointer to the device (see [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="b8d75-116">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b8d75-116">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8d75-117">Tipo: **[ **LPCVOID**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b8d75-117">Type: **[**LPCVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b8d75-118">Puntatore al file in memoria che contiene la visualizzazione delle risorse dello shader.</span><span class="sxs-lookup"><span data-stu-id="b8d75-118">Pointer to the file in memory that contains the shader-resource view.</span></span>

</dd> <dt>

<span data-ttu-id="b8d75-119">*SrcDataSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b8d75-119">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8d75-120">Tipo: **[ **size \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b8d75-120">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b8d75-121">Dimensioni del file in memoria.</span><span class="sxs-lookup"><span data-stu-id="b8d75-121">Size of the file in memory.</span></span>

</dd> <dt>

<span data-ttu-id="b8d75-122">*pLoadInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b8d75-122">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8d75-123">Tipo: **[ **D3DX11 \_ Image \_ Load \_ info**](d3dx11-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="b8d75-123">Type: **[**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)\***</span></span>

<span data-ttu-id="b8d75-124">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b8d75-124">Optional.</span></span> <span data-ttu-id="b8d75-125">Identifica le caratteristiche di una trama (vedere [**D3DX11 \_ Image \_ Load \_ info**](d3dx11-image-load-info.md)) quando viene creato il processore di dati; impostare questa proprietà su **null** per leggere le caratteristiche di una trama quando viene caricata la trama.</span><span class="sxs-lookup"><span data-stu-id="b8d75-125">Identifies the characteristics of a texture (see [**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="b8d75-126">*pPump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b8d75-126">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8d75-127">Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="b8d75-127">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="b8d75-128">Puntatore a un'interfaccia della pompa di thread (vedere [**interfaccia ID3DX11ThreadPump**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="b8d75-128">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="b8d75-129">Se viene specificato **null** , questa funzione verrà comportata in modo sincrono e non verrà restituita finché non viene completata.</span><span class="sxs-lookup"><span data-stu-id="b8d75-129">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="b8d75-130">*ppShaderResourceView* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b8d75-130">*ppShaderResourceView* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b8d75-131">Tipo: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="b8d75-131">Type: **[**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span></span>

<span data-ttu-id="b8d75-132">Indirizzo di un puntatore alla visualizzazione delle risorse dello shader appena creata.</span><span class="sxs-lookup"><span data-stu-id="b8d75-132">Address of a pointer to the newly created shader resource view.</span></span> <span data-ttu-id="b8d75-133">Vedere [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).</span><span class="sxs-lookup"><span data-stu-id="b8d75-133">See [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).</span></span>

</dd> <dt>

<span data-ttu-id="b8d75-134">*pHResult* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b8d75-134">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b8d75-135">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="b8d75-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="b8d75-136">Puntatore al valore restituito.</span><span class="sxs-lookup"><span data-stu-id="b8d75-136">A pointer to the return value.</span></span> <span data-ttu-id="b8d75-137">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="b8d75-137">May be **NULL**.</span></span> <span data-ttu-id="b8d75-138">Se *pPump* non è **null**, *pHResult* deve essere una posizione di memoria valida fino al completamento dell'esecuzione asincrona.</span><span class="sxs-lookup"><span data-stu-id="b8d75-138">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8d75-139">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b8d75-139">Return value</span></span>

<span data-ttu-id="b8d75-140">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b8d75-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b8d75-141">Il valore restituito è uno dei valori elencati nei [codici restituiti di Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="b8d75-141">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b8d75-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b8d75-142">Requirements</span></span>



| <span data-ttu-id="b8d75-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8d75-143">Requirement</span></span> | <span data-ttu-id="b8d75-144">Valore</span><span class="sxs-lookup"><span data-stu-id="b8d75-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8d75-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b8d75-145">Header</span></span><br/>  | <dl> <span data-ttu-id="b8d75-146"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8d75-146"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="b8d75-147">Libreria</span><span class="sxs-lookup"><span data-stu-id="b8d75-147">Library</span></span><br/> | <dl> <span data-ttu-id="b8d75-148"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b8d75-148"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="b8d75-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b8d75-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8d75-150">Funzioni D3DX</span><span class="sxs-lookup"><span data-stu-id="b8d75-150">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

