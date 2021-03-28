---
title: Funzione D3DX_R16G16_SNORM_to_FLOAT2
description: Decomprime \_ \_ \_ i dati di DXGI Format R16G16 russar shader in un XMFLOAT2.
ms.assetid: b54df555-b71f-46cd-8be7-34de785d15e2
keywords:
- Funzione D3DX_R16G16_SNORM_to_FLOAT2 HLSL
topic_type:
- apiref
api_name:
- D3DX_R16G16_SNORM_to_FLOAT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d3d45f486d2c44e2cbe319e920ab4bdec764fd8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995900"
---
# <a name="d3dx_r16g16_snorm_to_float2-function"></a><span data-ttu-id="fbce3-104">D3DX \_ R16G16 \_ russa \_ to \_ FLOAT2 Function</span><span class="sxs-lookup"><span data-stu-id="fbce3-104">D3DX\_R16G16\_SNORM\_to\_FLOAT2 function</span></span>

<span data-ttu-id="fbce3-105">Decomprime \_ \_ \_ i dati di DXGI Format R16G16 russar shader in un XMFLOAT2.</span><span class="sxs-lookup"><span data-stu-id="fbce3-105">Unpacks DXGI\_FORMAT\_R16G16\_SNORM shader data to an XMFLOAT2.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbce3-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fbce3-106">Syntax</span></span>

``` syntax
XMFLOAT2 D3DX_R16G16_SNORM_to_FLOAT2(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="fbce3-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="fbce3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbce3-108">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="fbce3-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="fbce3-109">Dati dello shader compressi.</span><span class="sxs-lookup"><span data-stu-id="fbce3-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbce3-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fbce3-110">Return value</span></span>

<span data-ttu-id="fbce3-111">Dati dello shader decompressi.</span><span class="sxs-lookup"><span data-stu-id="fbce3-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbce3-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fbce3-112">Requirements</span></span>



| <span data-ttu-id="fbce3-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbce3-113">Requirement</span></span> | <span data-ttu-id="fbce3-114">Valore</span><span class="sxs-lookup"><span data-stu-id="fbce3-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbce3-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fbce3-115">Header</span></span><br/> | <dl> <span data-ttu-id="fbce3-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="fbce3-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbce3-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fbce3-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbce3-118">Funzioni</span><span class="sxs-lookup"><span data-stu-id="fbce3-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="fbce3-119">Decompressione e compressione \_ del formato DXGI per la modifica dell'immagine In-Place</span><span class="sxs-lookup"><span data-stu-id="fbce3-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





