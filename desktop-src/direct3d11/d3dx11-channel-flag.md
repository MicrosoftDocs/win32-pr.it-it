---
title: Enumerazione D3DX11_CHANNEL_FLAG (D3DX11tex. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Questi flag vengono usati da funzioni che operano su uno o più canali in una trama.
ms.assetid: 058a0a1e-3c1b-4397-a41a-2e47d878cd92
keywords:
- Enumerazione D3DX11_CHANNEL_FLAG Direct3D 11
- Puntatore di enumerazione LPD3DX11_CHANNEL_FLAG Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_CHANNEL_FLAG
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2e3097552637ce96663671dda443684ebda2b65
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104402026"
---
# <a name="d3dx11_channel_flag-enumeration"></a><span data-ttu-id="51970-106">\_Enumerazione flag del canale D3DX11 \_</span><span class="sxs-lookup"><span data-stu-id="51970-106">D3DX11\_CHANNEL\_FLAG enumeration</span></span>

> [!Note]  
> <span data-ttu-id="51970-107">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="51970-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="51970-108">Questi flag vengono usati da funzioni che operano su uno o più canali in una trama.</span><span class="sxs-lookup"><span data-stu-id="51970-108">These flags are used by functions which operate on one or more channels in a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="51970-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="51970-109">Syntax</span></span>


```C++
typedef enum D3DX11_CHANNEL_FLAG { 
  D3DX11_CHANNEL_RED        = (1 << 0),
  D3DX11_CHANNEL_BLUE       = (1 << 1),
  D3DX11_CHANNEL_GREEN      = (1 << 2),
  D3DX11_CHANNEL_ALPHA      = (1 << 3),
  D3DX11_CHANNEL_LUMINANCE  = (1 << 4)
} D3DX11_CHANNEL_FLAG, *LPD3DX11_CHANNEL_FLAG;
```



## <a name="constants"></a><span data-ttu-id="51970-110">Costanti</span><span class="sxs-lookup"><span data-stu-id="51970-110">Constants</span></span>

<dl> <dt>

<span data-ttu-id="51970-111"><span id="D3DX11_CHANNEL_RED"></span><span id="d3dx11_channel_red"></span>**\_Canale D3DX11 \_ rosso**</span><span class="sxs-lookup"><span data-stu-id="51970-111"><span id="D3DX11_CHANNEL_RED"></span><span id="d3dx11_channel_red"></span>**D3DX11\_CHANNEL\_RED**</span></span>
</dt> <dd>

<span data-ttu-id="51970-112">Indica che deve essere utilizzato il canale rosso.</span><span class="sxs-lookup"><span data-stu-id="51970-112">Indicates the red channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="51970-113"><span id="D3DX11_CHANNEL_BLUE"></span><span id="d3dx11_channel_blue"></span>**\_Blu canale \_ D3DX11**</span><span class="sxs-lookup"><span data-stu-id="51970-113"><span id="D3DX11_CHANNEL_BLUE"></span><span id="d3dx11_channel_blue"></span>**D3DX11\_CHANNEL\_BLUE**</span></span>
</dt> <dd>

<span data-ttu-id="51970-114">Indica che deve essere utilizzato il canale blu.</span><span class="sxs-lookup"><span data-stu-id="51970-114">Indicates the blue channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="51970-115"><span id="D3DX11_CHANNEL_GREEN"></span><span id="d3dx11_channel_green"></span>**\_Canale D3DX11 \_ verde**</span><span class="sxs-lookup"><span data-stu-id="51970-115"><span id="D3DX11_CHANNEL_GREEN"></span><span id="d3dx11_channel_green"></span>**D3DX11\_CHANNEL\_GREEN**</span></span>
</dt> <dd>

<span data-ttu-id="51970-116">Indica che deve essere utilizzato il canale verde.</span><span class="sxs-lookup"><span data-stu-id="51970-116">Indicates the green channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="51970-117"><span id="D3DX11_CHANNEL_ALPHA"></span><span id="d3dx11_channel_alpha"></span>**\_Alfa canale \_ D3DX11**</span><span class="sxs-lookup"><span data-stu-id="51970-117"><span id="D3DX11_CHANNEL_ALPHA"></span><span id="d3dx11_channel_alpha"></span>**D3DX11\_CHANNEL\_ALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="51970-118">Indica che deve essere utilizzato il canale alfa.</span><span class="sxs-lookup"><span data-stu-id="51970-118">Indicates the alpha channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="51970-119"><span id="D3DX11_CHANNEL_LUMINANCE"></span><span id="d3dx11_channel_luminance"></span>**\_ \_ Luminanza canale D3DX11**</span><span class="sxs-lookup"><span data-stu-id="51970-119"><span id="D3DX11_CHANNEL_LUMINANCE"></span><span id="d3dx11_channel_luminance"></span>**D3DX11\_CHANNEL\_LUMINANCE**</span></span>
</dt> <dd>

<span data-ttu-id="51970-120">Indica che deve essere utilizzato il luminaces dei canali rosso, verde e blu.</span><span class="sxs-lookup"><span data-stu-id="51970-120">Indicates the luminaces of the red, green, and blue channels should be used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="51970-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="51970-121">Requirements</span></span>



| <span data-ttu-id="51970-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="51970-122">Requirement</span></span> | <span data-ttu-id="51970-123">Valore</span><span class="sxs-lookup"><span data-stu-id="51970-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="51970-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="51970-124">Header</span></span><br/> | <dl> <span data-ttu-id="51970-125"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="51970-125"><dt>D3DX11tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51970-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="51970-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51970-127">Enumerazioni D3DX</span><span class="sxs-lookup"><span data-stu-id="51970-127">D3DX Enumerations</span></span>](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





