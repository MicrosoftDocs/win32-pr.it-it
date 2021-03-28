---
title: Funzione D3DX11SaveTextureToMemory (D3DX11tex. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Nota invece di utilizzare questa funzione, è consigliabile utilizzare la libreria DirectXTex, CaptureTexture quindi SaveToXXXMemory (dove XXX è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine dell'arte comune per i giochi. Salva una trama in memoria.
ms.assetid: 3b54d8e1-6474-48fd-8348-a3baac406101
keywords:
- Funzione D3DX11SaveTextureToMemory Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11SaveTextureToMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4718f32f8d8288f83b30e3d742ebbe619421dc48
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235130"
---
# <a name="d3dx11savetexturetomemory-function"></a><span data-ttu-id="f9fea-106">D3DX11SaveTextureToMemory (funzione)</span><span class="sxs-lookup"><span data-stu-id="f9fea-106">D3DX11SaveTextureToMemory function</span></span>

> [!Note]  
> <span data-ttu-id="f9fea-107">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="f9fea-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="f9fea-108">Anziché utilizzare questa funzione, è consigliabile utilizzare la libreria [DirectXTex](https://github.com/Microsoft/DirectXTex) , **CaptureTexture** quindi **SAVETOXXXMEMORY** (dove xxx è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine dell'arte comune per i giochi.</span><span class="sxs-lookup"><span data-stu-id="f9fea-108">Instead of using this function, we recommend that you use the [DirectXTex](https://github.com/Microsoft/DirectXTex) library, **CaptureTexture** then **SaveToXXXMemory** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span>

 

<span data-ttu-id="f9fea-109">Salva una trama in memoria.</span><span class="sxs-lookup"><span data-stu-id="f9fea-109">Save a texture to memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9fea-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f9fea-110">Syntax</span></span>


```C++
HRESULT D3DX11SaveTextureToMemory(
        ID3D11DeviceContext      *pContext,
  _In_  ID3D11Resource           *pSrcTexture,
  _In_  D3DX11_IMAGE_FILE_FORMAT DestFormat,
  _Out_ LPD3D10BLOB              *ppDestBuf,
  _In_  UINT                     Flags
);
```



## <a name="parameters"></a><span data-ttu-id="f9fea-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="f9fea-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9fea-112">*pContext*</span><span class="sxs-lookup"><span data-stu-id="f9fea-112">*pContext*</span></span> 
</dt> <dd>

<span data-ttu-id="f9fea-113">Tipo: **[ **sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="f9fea-113">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="f9fea-114">Puntatore a un oggetto [**sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="f9fea-114">A pointer to an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>

</dd> <dt>

<span data-ttu-id="f9fea-115">*pSrcTexture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f9fea-115">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9fea-116">Tipo: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span><span class="sxs-lookup"><span data-stu-id="f9fea-116">Type: **[**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span></span>

<span data-ttu-id="f9fea-117">Puntatore alla trama da salvare.</span><span class="sxs-lookup"><span data-stu-id="f9fea-117">Pointer to the texture to be saved.</span></span> <span data-ttu-id="f9fea-118">Vedere [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span><span class="sxs-lookup"><span data-stu-id="f9fea-118">See [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span></span>

</dd> <dt>

<span data-ttu-id="f9fea-119">*DestFormat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f9fea-119">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9fea-120">Tipo: **[ **D3DX11 \_ Image \_ file \_ Format**](d3dx11-image-file-format.md)**</span><span class="sxs-lookup"><span data-stu-id="f9fea-120">Type: **[**D3DX11\_IMAGE\_FILE\_FORMAT**](d3dx11-image-file-format.md)**</span></span>

<span data-ttu-id="f9fea-121">Il formato in cui verrà salvata la trama.</span><span class="sxs-lookup"><span data-stu-id="f9fea-121">The format the texture will be saved as.</span></span> <span data-ttu-id="f9fea-122">Vedere [**D3DX11 \_ Image \_ file \_ Format**](d3dx11-image-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="f9fea-122">See [**D3DX11\_IMAGE\_FILE\_FORMAT**](d3dx11-image-file-format.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9fea-123">*ppDestBuf* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f9fea-123">*ppDestBuf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9fea-124">Tipo: **[ **LPD3D10BLOB**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\***</span><span class="sxs-lookup"><span data-stu-id="f9fea-124">Type: **[**LPD3D10BLOB**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\***</span></span>

<span data-ttu-id="f9fea-125">Indirizzo di un puntatore alla memoria contenente la trama salvata.</span><span class="sxs-lookup"><span data-stu-id="f9fea-125">Address of a pointer to the memory containing the saved texture.</span></span>

</dd> <dt>

<span data-ttu-id="f9fea-126">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f9fea-126">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9fea-127">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f9fea-127">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f9fea-128">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f9fea-128">Optional.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9fea-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f9fea-129">Return value</span></span>

<span data-ttu-id="f9fea-130">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f9fea-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f9fea-131">Il valore restituito è uno dei valori elencati nei [codici restituiti di Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="f9fea-131">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f9fea-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f9fea-132">Requirements</span></span>



| <span data-ttu-id="f9fea-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9fea-133">Requirement</span></span> | <span data-ttu-id="f9fea-134">Valore</span><span class="sxs-lookup"><span data-stu-id="f9fea-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9fea-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f9fea-135">Header</span></span><br/>  | <dl> <span data-ttu-id="f9fea-136"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9fea-136"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="f9fea-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="f9fea-137">Library</span></span><br/> | <dl> <span data-ttu-id="f9fea-138"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f9fea-138"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="f9fea-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f9fea-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9fea-140">Funzioni D3DX</span><span class="sxs-lookup"><span data-stu-id="f9fea-140">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

