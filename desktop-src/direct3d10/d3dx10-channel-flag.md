---
description: Questi flag vengono usati da funzioni che operano su uno o più canali in una trama.
ms.assetid: 54ecb39a-a36e-43bb-bb51-78b7375716d8
title: Enumerazione D3DX10_CHANNEL_FLAG (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_CHANNEL_FLAG
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: f21958ab964a70116a551c0cb8dadbce6db88f7d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355634"
---
# <a name="d3dx10_channel_flag-enumeration"></a><span data-ttu-id="635ee-103">\_Enumerazione flag del canale d3dx10 \_</span><span class="sxs-lookup"><span data-stu-id="635ee-103">D3DX10\_CHANNEL\_FLAG enumeration</span></span>

<span data-ttu-id="635ee-104">Questi flag vengono usati da funzioni che operano su uno o più canali in una trama.</span><span class="sxs-lookup"><span data-stu-id="635ee-104">These flags are used by functions which operate on one or more channels in a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="635ee-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="635ee-105">Syntax</span></span>


```C++
typedef enum D3DX10_CHANNEL_FLAG { 
  D3DX10_CHANNEL_RED        = (1 << 0),
  D3DX10_CHANNEL_BLUE       = (1 << 1),
  D3DX10_CHANNEL_GREEN      = (1 << 2),
  D3DX10_CHANNEL_ALPHA      = (1 << 3),
  D3DX10_CHANNEL_LUMINANCE  = (1 << 4)
} D3DX10_CHANNEL_FLAG, *LPD3DX10_CHANNEL_FLAG;
```



## <a name="constants"></a><span data-ttu-id="635ee-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="635ee-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="635ee-107"><span id="D3DX10_CHANNEL_RED"></span><span id="d3dx10_channel_red"></span>**\_Canale d3dx10 \_ rosso**</span><span class="sxs-lookup"><span data-stu-id="635ee-107"><span id="D3DX10_CHANNEL_RED"></span><span id="d3dx10_channel_red"></span>**D3DX10\_CHANNEL\_RED**</span></span>
</dt> <dd>

<span data-ttu-id="635ee-108">Indica che deve essere utilizzato il canale rosso.</span><span class="sxs-lookup"><span data-stu-id="635ee-108">Indicates the red channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="635ee-109"><span id="D3DX10_CHANNEL_BLUE"></span><span id="d3dx10_channel_blue"></span>**\_Blu canale \_ d3dx10**</span><span class="sxs-lookup"><span data-stu-id="635ee-109"><span id="D3DX10_CHANNEL_BLUE"></span><span id="d3dx10_channel_blue"></span>**D3DX10\_CHANNEL\_BLUE**</span></span>
</dt> <dd>

<span data-ttu-id="635ee-110">Indica che deve essere utilizzato il canale blu.</span><span class="sxs-lookup"><span data-stu-id="635ee-110">Indicates the blue channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="635ee-111"><span id="D3DX10_CHANNEL_GREEN"></span><span id="d3dx10_channel_green"></span>**\_Canale d3dx10 \_ verde**</span><span class="sxs-lookup"><span data-stu-id="635ee-111"><span id="D3DX10_CHANNEL_GREEN"></span><span id="d3dx10_channel_green"></span>**D3DX10\_CHANNEL\_GREEN**</span></span>
</dt> <dd>

<span data-ttu-id="635ee-112">Indica che deve essere utilizzato il canale verde.</span><span class="sxs-lookup"><span data-stu-id="635ee-112">Indicates the green channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="635ee-113"><span id="D3DX10_CHANNEL_ALPHA"></span><span id="d3dx10_channel_alpha"></span>**\_Alfa canale \_ d3dx10**</span><span class="sxs-lookup"><span data-stu-id="635ee-113"><span id="D3DX10_CHANNEL_ALPHA"></span><span id="d3dx10_channel_alpha"></span>**D3DX10\_CHANNEL\_ALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="635ee-114">Indica che deve essere utilizzato il canale alfa.</span><span class="sxs-lookup"><span data-stu-id="635ee-114">Indicates the alpha channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="635ee-115"><span id="D3DX10_CHANNEL_LUMINANCE"></span><span id="d3dx10_channel_luminance"></span>**\_ \_ Luminanza canale d3dx10**</span><span class="sxs-lookup"><span data-stu-id="635ee-115"><span id="D3DX10_CHANNEL_LUMINANCE"></span><span id="d3dx10_channel_luminance"></span>**D3DX10\_CHANNEL\_LUMINANCE**</span></span>
</dt> <dd>

<span data-ttu-id="635ee-116">Indica che deve essere utilizzato il luminaces dei canali rosso, verde e blu.</span><span class="sxs-lookup"><span data-stu-id="635ee-116">Indicates the luminaces of the red, green, and blue channels should be used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="635ee-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="635ee-117">Requirements</span></span>



| <span data-ttu-id="635ee-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="635ee-118">Requirement</span></span> | <span data-ttu-id="635ee-119">Valore</span><span class="sxs-lookup"><span data-stu-id="635ee-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="635ee-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="635ee-120">Header</span></span><br/> | <dl> <span data-ttu-id="635ee-121"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="635ee-121"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="635ee-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="635ee-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="635ee-123">Enumerazioni D3DX</span><span class="sxs-lookup"><span data-stu-id="635ee-123">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




