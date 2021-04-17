---
title: Funzione D3DX_FLOAT4_to_R8G8B8A8_SNORM
description: Comprime di nuovo il XMFLOAT4 specificato in un \_ formato DXGI \_ R8G8B8A8 \_ russar.
ms.assetid: 425aeabd-6249-4777-8935-827691abef24
keywords:
- Funzione D3DX_FLOAT4_to_R8G8B8A8_SNORM HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_R8G8B8A8_SNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 194835ef126a3441dc2b842784dfa841ae1d7d6c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355779"
---
# <a name="d3dx_float4_to_r8g8b8a8_snorm-function"></a><span data-ttu-id="05748-104">D3DX \_ float4 \_ to \_ R8G8B8A8 \_ russat Function</span><span class="sxs-lookup"><span data-stu-id="05748-104">D3DX\_FLOAT4\_to\_R8G8B8A8\_SNORM function</span></span>

<span data-ttu-id="05748-105">Comprime di nuovo il XMFLOAT4 specificato in un \_ formato DXGI \_ R8G8B8A8 \_ russar.</span><span class="sxs-lookup"><span data-stu-id="05748-105">Packs the given XMFLOAT4 back into a DXGI\_FORMAT\_R8G8B8A8\_SNORM.</span></span>

## <a name="syntax"></a><span data-ttu-id="05748-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="05748-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT4_to_R8G8B8A8_SNORM(
   hlsl_precise XMFLOAT4 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="05748-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="05748-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05748-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="05748-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="05748-109">Dati dello shader da comprimere.</span><span class="sxs-lookup"><span data-stu-id="05748-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05748-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="05748-110">Return value</span></span>

<span data-ttu-id="05748-111">Dati dello shader compressi.</span><span class="sxs-lookup"><span data-stu-id="05748-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="05748-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="05748-112">Requirements</span></span>



| <span data-ttu-id="05748-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="05748-113">Requirement</span></span> | <span data-ttu-id="05748-114">Valore</span><span class="sxs-lookup"><span data-stu-id="05748-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05748-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="05748-115">Header</span></span><br/> | <dl> <span data-ttu-id="05748-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="05748-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05748-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="05748-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05748-118">Funzioni</span><span class="sxs-lookup"><span data-stu-id="05748-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="05748-119">Decompressione e compressione \_ del formato DXGI per la modifica dell'immagine In-Place</span><span class="sxs-lookup"><span data-stu-id="05748-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





