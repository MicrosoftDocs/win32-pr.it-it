---
description: Caricare una trama da una trama.
ms.assetid: 126e71e1-a3b2-418b-be35-434a2e9472ca
title: Funzione D3DX10LoadTextureFromTexture (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10LoadTextureFromTexture
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: e8dc65c9bff78484f09c355f8eb3d9626372b9b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354434"
---
# <a name="d3dx10loadtexturefromtexture-function"></a><span data-ttu-id="e580d-103">D3DX10LoadTextureFromTexture (funzione)</span><span class="sxs-lookup"><span data-stu-id="e580d-103">D3DX10LoadTextureFromTexture function</span></span>

<span data-ttu-id="e580d-104">Caricare una trama da una trama.</span><span class="sxs-lookup"><span data-stu-id="e580d-104">Load a texture from a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="e580d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e580d-105">Syntax</span></span>


```C++
HRESULT D3DX10LoadTextureFromTexture(
   ID3D10Resource           *pSrcTexture,
   D3DX10_TEXTURE_LOAD_INFO *pLoadInfo,
   ID3D10Resource           *pDstTexture
);
```



## <a name="parameters"></a><span data-ttu-id="e580d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e580d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e580d-107">*pSrcTexture*</span><span class="sxs-lookup"><span data-stu-id="e580d-107">*pSrcTexture*</span></span> 
</dt> <dd>

<span data-ttu-id="e580d-108">Tipo: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span><span class="sxs-lookup"><span data-stu-id="e580d-108">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span></span>

<span data-ttu-id="e580d-109">Puntatore alla trama di origine.</span><span class="sxs-lookup"><span data-stu-id="e580d-109">Pointer to the source texture.</span></span> <span data-ttu-id="e580d-110">Vedere [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span><span class="sxs-lookup"><span data-stu-id="e580d-110">See [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span></span>

</dd> <dt>

<span data-ttu-id="e580d-111">*pLoadInfo*</span><span class="sxs-lookup"><span data-stu-id="e580d-111">*pLoadInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="e580d-112">Tipo: **[ **d3dx10 \_ texture \_ Load \_ info**](d3dx10-texture-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="e580d-112">Type: **[**D3DX10\_TEXTURE\_LOAD\_INFO**](d3dx10-texture-load-info.md)\***</span></span>

<span data-ttu-id="e580d-113">Puntatore ai parametri di caricamento della trama.</span><span class="sxs-lookup"><span data-stu-id="e580d-113">Pointer to texture loading parameters.</span></span> <span data-ttu-id="e580d-114">Vedere [**d3dx10 \_ texture \_ Load \_ info**](d3dx10-texture-load-info.md).</span><span class="sxs-lookup"><span data-stu-id="e580d-114">See [**D3DX10\_TEXTURE\_LOAD\_INFO**](d3dx10-texture-load-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="e580d-115">*pDstTexture*</span><span class="sxs-lookup"><span data-stu-id="e580d-115">*pDstTexture*</span></span> 
</dt> <dd>

<span data-ttu-id="e580d-116">Tipo: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span><span class="sxs-lookup"><span data-stu-id="e580d-116">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span></span>

<span data-ttu-id="e580d-117">Puntatore alla trama di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e580d-117">Pointer to the destination texture.</span></span> <span data-ttu-id="e580d-118">Vedere [**interfaccia ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span><span class="sxs-lookup"><span data-stu-id="e580d-118">See [**ID3D10Resource Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e580d-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e580d-119">Return value</span></span>

<span data-ttu-id="e580d-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e580d-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e580d-121">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="e580d-121">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e580d-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e580d-122">Requirements</span></span>



| <span data-ttu-id="e580d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e580d-123">Requirement</span></span> | <span data-ttu-id="e580d-124">Valore</span><span class="sxs-lookup"><span data-stu-id="e580d-124">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e580d-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e580d-125">Header</span></span><br/> | <dl> <span data-ttu-id="e580d-126"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="e580d-126"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e580d-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e580d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e580d-128">Funzioni di trama in D3DX 10</span><span class="sxs-lookup"><span data-stu-id="e580d-128">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 




