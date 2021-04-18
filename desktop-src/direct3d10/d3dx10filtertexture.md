---
description: Genera la catena mipmap usando un filtro di trama particolare.
ms.assetid: 19e651dd-dc34-405b-8769-00d91c097a1f
title: Funzione D3DX10FilterTexture (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10FilterTexture
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: e2f500bcd7f7465ca1c24f1adaab3a77dd5cb7b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322089"
---
# <a name="d3dx10filtertexture-function"></a><span data-ttu-id="546a9-103">D3DX10FilterTexture (funzione)</span><span class="sxs-lookup"><span data-stu-id="546a9-103">D3DX10FilterTexture function</span></span>

<span data-ttu-id="546a9-104">Genera la catena mipmap usando un filtro di trama particolare.</span><span class="sxs-lookup"><span data-stu-id="546a9-104">Generates mipmap chain using a particular texture filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="546a9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="546a9-105">Syntax</span></span>


```C++
HRESULT D3DX10FilterTexture(
   ID3D10Resource *pTexture,
   UINT           SrcLevel,
   UINT           MipFilter
);
```



## <a name="parameters"></a><span data-ttu-id="546a9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="546a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="546a9-107">*pTexture*</span><span class="sxs-lookup"><span data-stu-id="546a9-107">*pTexture*</span></span> 
</dt> <dd>

<span data-ttu-id="546a9-108">Tipo: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span><span class="sxs-lookup"><span data-stu-id="546a9-108">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span></span>

<span data-ttu-id="546a9-109">Oggetto texture da filtrare.</span><span class="sxs-lookup"><span data-stu-id="546a9-109">The texture object to be filtered.</span></span> <span data-ttu-id="546a9-110">Vedere [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span><span class="sxs-lookup"><span data-stu-id="546a9-110">See [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span></span>

</dd> <dt>

<span data-ttu-id="546a9-111">*SrcLevel*</span><span class="sxs-lookup"><span data-stu-id="546a9-111">*SrcLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="546a9-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="546a9-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="546a9-113">Livello mipmap i cui dati vengono usati per generare il resto della catena mipmap.</span><span class="sxs-lookup"><span data-stu-id="546a9-113">The mipmap level whose data is used to generate the rest of the mipmap chain.</span></span>

</dd> <dt>

<span data-ttu-id="546a9-114">*MipFilter*</span><span class="sxs-lookup"><span data-stu-id="546a9-114">*MipFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="546a9-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="546a9-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="546a9-116">Flag che controllano il modo in cui ogni miplevel è filtrato (o D3DX10 \_ predefinito per la \_ casella di filtro d3dx10 \_ ).</span><span class="sxs-lookup"><span data-stu-id="546a9-116">Flags controlling how each miplevel is filtered (or D3DX10\_DEFAULT for D3DX10\_FILTER\_BOX).</span></span> <span data-ttu-id="546a9-117">Vedere [**\_ \_ flag di filtro d3dx10**](d3dx10-filter-flag.md).</span><span class="sxs-lookup"><span data-stu-id="546a9-117">See [**D3DX10\_FILTER\_FLAG**](d3dx10-filter-flag.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="546a9-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="546a9-118">Return value</span></span>

<span data-ttu-id="546a9-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="546a9-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="546a9-120">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="546a9-120">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="546a9-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="546a9-121">Requirements</span></span>



| <span data-ttu-id="546a9-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="546a9-122">Requirement</span></span> | <span data-ttu-id="546a9-123">Valore</span><span class="sxs-lookup"><span data-stu-id="546a9-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="546a9-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="546a9-124">Header</span></span><br/> | <dl> <span data-ttu-id="546a9-125"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="546a9-125"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="546a9-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="546a9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="546a9-127">Funzioni di trama in D3DX 10</span><span class="sxs-lookup"><span data-stu-id="546a9-127">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
