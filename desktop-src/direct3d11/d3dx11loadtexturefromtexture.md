---
title: Funzione D3DX11LoadTextureFromTexture (D3DX11tex. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Nota invece di utilizzare questa funzione, è consigliabile utilizzare la libreria DirectXTex, ridimensionare, convertire, comprimere, decomprimere e/o CopyRectangle. Caricare una trama da una trama.
ms.assetid: 4e673f73-531d-4df8-8542-798e4e70c481
keywords:
- Funzione D3DX11LoadTextureFromTexture Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11LoadTextureFromTexture
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 246429433dea11fddfd4396f3e59677877081592
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982322"
---
# <a name="d3dx11loadtexturefromtexture-function"></a><span data-ttu-id="fc612-106">D3DX11LoadTextureFromTexture (funzione)</span><span class="sxs-lookup"><span data-stu-id="fc612-106">D3DX11LoadTextureFromTexture function</span></span>

> [!Note]  
> <span data-ttu-id="fc612-107">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="fc612-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="fc612-108">Anziché utilizzare questa funzione, è consigliabile utilizzare la libreria [DirectXTex](https://github.com/Microsoft/DirectXTex) , **ridimensionare**, **convertire**, **comprimere**, **decomprimere** e/o **CopyRectangle**.</span><span class="sxs-lookup"><span data-stu-id="fc612-108">Instead of using this function, we recommend that you use the [DirectXTex](https://github.com/Microsoft/DirectXTex) library, **Resize**, **Convert**, **Compress**, **Decompress**, and/or **CopyRectangle**.</span></span>

 

<span data-ttu-id="fc612-109">Caricare una trama da una trama.</span><span class="sxs-lookup"><span data-stu-id="fc612-109">Load a texture from a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc612-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fc612-110">Syntax</span></span>


```C++
HRESULT D3DX11LoadTextureFromTexture(
   ID3D11DeviceContext      *pContext,
   ID3D11Resource           *pSrcTexture,
   D3DX11_TEXTURE_LOAD_INFO *pLoadInfo,
   ID3D11Resource           *pDstTexture
);
```



## <a name="parameters"></a><span data-ttu-id="fc612-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="fc612-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc612-112">*pContext*</span><span class="sxs-lookup"><span data-stu-id="fc612-112">*pContext*</span></span> 
</dt> <dd>

<span data-ttu-id="fc612-113">Tipo: **[ **sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="fc612-113">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="fc612-114">Puntatore a un oggetto [**sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="fc612-114">A pointer to an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>

</dd> <dt>

<span data-ttu-id="fc612-115">*pSrcTexture*</span><span class="sxs-lookup"><span data-stu-id="fc612-115">*pSrcTexture*</span></span> 
</dt> <dd>

<span data-ttu-id="fc612-116">Tipo: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span><span class="sxs-lookup"><span data-stu-id="fc612-116">Type: **[**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span></span>

<span data-ttu-id="fc612-117">Puntatore alla trama di origine.</span><span class="sxs-lookup"><span data-stu-id="fc612-117">Pointer to the source texture.</span></span> <span data-ttu-id="fc612-118">Vedere [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span><span class="sxs-lookup"><span data-stu-id="fc612-118">See [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span></span>

</dd> <dt>

<span data-ttu-id="fc612-119">*pLoadInfo*</span><span class="sxs-lookup"><span data-stu-id="fc612-119">*pLoadInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="fc612-120">Tipo: **[ **D3DX11 \_ texture \_ Load \_ info**](d3dx11-texture-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="fc612-120">Type: **[**D3DX11\_TEXTURE\_LOAD\_INFO**](d3dx11-texture-load-info.md)\***</span></span>

<span data-ttu-id="fc612-121">Puntatore ai parametri di caricamento della trama.</span><span class="sxs-lookup"><span data-stu-id="fc612-121">Pointer to texture loading parameters.</span></span> <span data-ttu-id="fc612-122">Vedere [**D3DX11 \_ texture \_ Load \_ info**](d3dx11-texture-load-info.md).</span><span class="sxs-lookup"><span data-stu-id="fc612-122">See [**D3DX11\_TEXTURE\_LOAD\_INFO**](d3dx11-texture-load-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc612-123">*pDstTexture*</span><span class="sxs-lookup"><span data-stu-id="fc612-123">*pDstTexture*</span></span> 
</dt> <dd>

<span data-ttu-id="fc612-124">Tipo: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span><span class="sxs-lookup"><span data-stu-id="fc612-124">Type: **[**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span></span>

<span data-ttu-id="fc612-125">Puntatore alla trama di destinazione.</span><span class="sxs-lookup"><span data-stu-id="fc612-125">Pointer to the destination texture.</span></span> <span data-ttu-id="fc612-126">Vedere [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span><span class="sxs-lookup"><span data-stu-id="fc612-126">See [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc612-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fc612-127">Return value</span></span>

<span data-ttu-id="fc612-128">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fc612-128">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fc612-129">Il valore restituito è uno dei valori elencati nei [codici restituiti di Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="fc612-129">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fc612-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc612-130">Requirements</span></span>



| <span data-ttu-id="fc612-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc612-131">Requirement</span></span> | <span data-ttu-id="fc612-132">Valore</span><span class="sxs-lookup"><span data-stu-id="fc612-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc612-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fc612-133">Header</span></span><br/>  | <dl> <span data-ttu-id="fc612-134"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc612-134"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="fc612-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="fc612-135">Library</span></span><br/> | <dl> <span data-ttu-id="fc612-136"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fc612-136"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="fc612-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fc612-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc612-138">Funzioni D3DX</span><span class="sxs-lookup"><span data-stu-id="fc612-138">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

 





