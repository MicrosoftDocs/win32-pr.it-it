---
description: Crea un oggetto del tipo di carattere. Nota invece di usare questa funzione, è consigliabile usare DirectWrite e la libreria DirectXTK, SpriteFont Class.
ms.assetid: 057ee033-37d8-4fc1-9f35-776393fff008
title: Funzione D3DX10CreateFontIndirect (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateFontIndirect
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ae69b02483a94a80a06ef52ee4857eb081cfcfb2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354484"
---
# <a name="d3dx10createfontindirect-function"></a><span data-ttu-id="c4f1c-103">D3DX10CreateFontIndirect (funzione)</span><span class="sxs-lookup"><span data-stu-id="c4f1c-103">D3DX10CreateFontIndirect function</span></span>

<span data-ttu-id="c4f1c-104">Crea un oggetto del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="c4f1c-104">Creates a font object.</span></span>

> [!Note]  
> <span data-ttu-id="c4f1c-105">Invece di usare questa funzione, è consigliabile usare [DirectWrite](../directwrite/direct-write-portal.md) e la libreria [DirectXTK](https://github.com/Microsoft/DirectXTK) , la classe **SpriteFont** .</span><span class="sxs-lookup"><span data-stu-id="c4f1c-105">Instead of using this function, we recommend that you use [DirectWrite](../directwrite/direct-write-portal.md) and the [DirectXTK](https://github.com/Microsoft/DirectXTK) library, **SpriteFont** class.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="c4f1c-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c4f1c-106">Syntax</span></span>


```C++
HRESULT D3DX10CreateFontIndirect(
  _In_        ID3D10Device     *pDevice,
  _In_  const D3DX10_FONT_DESC *pDesc,
  _Out_       LPD3DX10FONT     *ppFont
);
```



## <a name="parameters"></a><span data-ttu-id="c4f1c-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="c4f1c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4f1c-108">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4f1c-108">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4f1c-109">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="c4f1c-109">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="c4f1c-110">Puntatore a un'interfaccia di [**interfaccia ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) .</span><span class="sxs-lookup"><span data-stu-id="c4f1c-110">Pointer to an [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) interface.</span></span>

</dd> <dt>

<span data-ttu-id="c4f1c-111">*pDesc* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4f1c-111">*pDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4f1c-112">Tipo: **const [**d3dx10 \_ Font \_ desc**](d3dx10-font-desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="c4f1c-112">Type: **const [**D3DX10\_FONT\_DESC**](d3dx10-font-desc.md)\***</span></span>

<span data-ttu-id="c4f1c-113">Puntatore a una struttura [**d3dx10 del \_ tipo di carattere \_ Descrizione**](d3dx10-font-desc.md) , che descrive gli attributi dell'oggetto tipo di carattere da creare.</span><span class="sxs-lookup"><span data-stu-id="c4f1c-113">Pointer to a [**D3DX10\_FONT\_DESC**](d3dx10-font-desc.md) structure, describing the attributes of the font object to create.</span></span> <span data-ttu-id="c4f1c-114">Se è definito Unicode, la chiamata di funzione viene risolta in D3DXCreateFontIndirectW.</span><span class="sxs-lookup"><span data-stu-id="c4f1c-114">If Unicode is defined, the function call resolves to D3DXCreateFontIndirectW.</span></span> <span data-ttu-id="c4f1c-115">In caso contrario, la chiamata di funzione viene risolta in D3DXCreateFontIndirectA perché vengono utilizzate le stringhe ANSI.</span><span class="sxs-lookup"><span data-stu-id="c4f1c-115">Otherwise, the function call resolves to D3DXCreateFontIndirectA because ANSI strings are being used.</span></span>

</dd> <dt>

<span data-ttu-id="c4f1c-116">*ppFont* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c4f1c-116">*ppFont* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c4f1c-117">Tipo: **[ **LPD3DX10FONT**](id3dx10font.md)\***</span><span class="sxs-lookup"><span data-stu-id="c4f1c-117">Type: **[**LPD3DX10FONT**](id3dx10font.md)\***</span></span>

<span data-ttu-id="c4f1c-118">Restituisce un puntatore a un' [**interfaccia ID3DX10Font**](id3dx10font.md).</span><span class="sxs-lookup"><span data-stu-id="c4f1c-118">Returns a pointer to an [**ID3DX10Font Interface**](id3dx10font.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4f1c-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c4f1c-119">Return value</span></span>

<span data-ttu-id="c4f1c-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c4f1c-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c4f1c-121">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="c4f1c-121">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c4f1c-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c4f1c-122">Requirements</span></span>



| <span data-ttu-id="c4f1c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4f1c-123">Requirement</span></span> | <span data-ttu-id="c4f1c-124">Valore</span><span class="sxs-lookup"><span data-stu-id="c4f1c-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4f1c-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c4f1c-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c4f1c-126"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4f1c-126"><dt>D3DX10Core.h</dt></span></span> </dl> |
| <span data-ttu-id="c4f1c-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="c4f1c-127">Library</span></span><br/> | <dl> <span data-ttu-id="c4f1c-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4f1c-128"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c4f1c-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c4f1c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4f1c-130">Funzioni per utilizzo generico</span><span class="sxs-lookup"><span data-stu-id="c4f1c-130">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
