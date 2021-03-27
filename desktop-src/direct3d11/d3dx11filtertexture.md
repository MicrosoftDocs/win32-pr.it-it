---
title: Funzione D3DX11FilterTexture (D3DX11tex. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Nota invece di utilizzare questa funzione, è consigliabile utilizzare la libreria DirectXTex, GenerateMipMaps e GenerateMipMaps3D. Genera la catena mipmap usando un filtro di trama particolare.
ms.assetid: 52ae3228-f9d7-4944-b49c-55df1816f1f7
keywords:
- Funzione D3DX11FilterTexture Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11FilterTexture
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71e74e60e9d66e2a5251c161e4df6451266d3fb5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982334"
---
# <a name="d3dx11filtertexture-function"></a><span data-ttu-id="fbebb-106">D3DX11FilterTexture (funzione)</span><span class="sxs-lookup"><span data-stu-id="fbebb-106">D3DX11FilterTexture function</span></span>

> [!Note]  
> <span data-ttu-id="fbebb-107">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="fbebb-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="fbebb-108">Anziché utilizzare questa funzione, è consigliabile utilizzare la libreria [DirectXTex](https://github.com/Microsoft/DirectXTex) , **GenerateMipMaps** e **GenerateMipMaps3D**.</span><span class="sxs-lookup"><span data-stu-id="fbebb-108">Instead of using this function, we recommend that you use the [DirectXTex](https://github.com/Microsoft/DirectXTex) library, **GenerateMipMaps** and **GenerateMipMaps3D**.</span></span>

 

<span data-ttu-id="fbebb-109">Genera la catena mipmap usando un filtro di trama particolare.</span><span class="sxs-lookup"><span data-stu-id="fbebb-109">Generates mipmap chain using a particular texture filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbebb-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fbebb-110">Syntax</span></span>


```C++
HRESULT D3DX11FilterTexture(
   ID3D11DeviceContext *pContext,
   ID3D11Resource      *pTexture,
   UINT                SrcLevel,
   UINT                MipFilter
);
```



## <a name="parameters"></a><span data-ttu-id="fbebb-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="fbebb-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbebb-112">*pContext*</span><span class="sxs-lookup"><span data-stu-id="fbebb-112">*pContext*</span></span> 
</dt> <dd>

<span data-ttu-id="fbebb-113">Tipo: **[ **sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="fbebb-113">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="fbebb-114">Puntatore a un oggetto [**sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="fbebb-114">A pointer to an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>

</dd> <dt>

<span data-ttu-id="fbebb-115">*pTexture*</span><span class="sxs-lookup"><span data-stu-id="fbebb-115">*pTexture*</span></span> 
</dt> <dd>

<span data-ttu-id="fbebb-116">Tipo: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span><span class="sxs-lookup"><span data-stu-id="fbebb-116">Type: **[**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span></span>

<span data-ttu-id="fbebb-117">Oggetto texture da filtrare.</span><span class="sxs-lookup"><span data-stu-id="fbebb-117">The texture object to be filtered.</span></span> <span data-ttu-id="fbebb-118">Vedere [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span><span class="sxs-lookup"><span data-stu-id="fbebb-118">See [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span></span>

</dd> <dt>

<span data-ttu-id="fbebb-119">*SrcLevel*</span><span class="sxs-lookup"><span data-stu-id="fbebb-119">*SrcLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="fbebb-120">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fbebb-120">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fbebb-121">Livello mipmap i cui dati vengono usati per generare il resto della catena mipmap.</span><span class="sxs-lookup"><span data-stu-id="fbebb-121">The mipmap level whose data is used to generate the rest of the mipmap chain.</span></span>

</dd> <dt>

<span data-ttu-id="fbebb-122">*MipFilter*</span><span class="sxs-lookup"><span data-stu-id="fbebb-122">*MipFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="fbebb-123">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fbebb-123">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fbebb-124">Flag che controllano il modo in cui ogni miplevel è filtrato (o D3DX11 \_ predefinito per il \_ filtro D3DX11 \_ lineare).</span><span class="sxs-lookup"><span data-stu-id="fbebb-124">Flags controlling how each miplevel is filtered (or D3DX11\_DEFAULT for D3DX11\_FILTER\_LINEAR).</span></span> <span data-ttu-id="fbebb-125">Vedere [**\_ \_ flag di filtro D3DX11**](d3dx11-filter-flag.md).</span><span class="sxs-lookup"><span data-stu-id="fbebb-125">See [**D3DX11\_FILTER\_FLAG**](d3dx11-filter-flag.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbebb-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fbebb-126">Return value</span></span>

<span data-ttu-id="fbebb-127">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fbebb-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fbebb-128">Il valore restituito è uno dei valori elencati nei [codici restituiti di Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="fbebb-128">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fbebb-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fbebb-129">Requirements</span></span>



| <span data-ttu-id="fbebb-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbebb-130">Requirement</span></span> | <span data-ttu-id="fbebb-131">Valore</span><span class="sxs-lookup"><span data-stu-id="fbebb-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fbebb-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fbebb-132">Header</span></span><br/>  | <dl> <span data-ttu-id="fbebb-133"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbebb-133"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="fbebb-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="fbebb-134">Library</span></span><br/> | <dl> <span data-ttu-id="fbebb-135"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fbebb-135"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="fbebb-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fbebb-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbebb-137">Funzioni D3DX</span><span class="sxs-lookup"><span data-stu-id="fbebb-137">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

