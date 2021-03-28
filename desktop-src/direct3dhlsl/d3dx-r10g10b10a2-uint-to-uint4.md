---
title: Funzione D3DX_R10G10B10A2_UINT_to_UINT4
description: Decomprime \_ \_ \_ i dati di DXGI Format R10G10B10A2 uint shader in un XMINT4.
ms.assetid: 47c4f11f-936a-46d5-9533-1a4f9fce6168
keywords:
- Funzione D3DX_R10G10B10A2_UINT_to_UINT4 HLSL
topic_type:
- apiref
api_name:
- D3DX_R10G10B10A2_UINT_to_UINT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 378b013ad077c787253b4a58f24082d1c64b416f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982491"
---
# <a name="d3dx_r10g10b10a2_uint_to_uint4-function"></a><span data-ttu-id="5a242-104">D3DX \_ R10G10B10A2 \_ uint \_ to \_ UINT4 Function</span><span class="sxs-lookup"><span data-stu-id="5a242-104">D3DX\_R10G10B10A2\_UINT\_to\_UINT4 function</span></span>

<span data-ttu-id="5a242-105">Decomprime \_ \_ \_ i dati di DXGI Format R10G10B10A2 uint shader in un XMINT4.</span><span class="sxs-lookup"><span data-stu-id="5a242-105">Unpacks DXGI\_FORMAT\_R10G10B10A2\_UINT shader data to an XMINT4.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a242-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5a242-106">Syntax</span></span>

``` syntax
XMINT4 D3DX_R10G10B10A2_UINT_to_UINT4(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="5a242-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="5a242-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a242-108">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="5a242-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="5a242-109">Dati dello shader compressi.</span><span class="sxs-lookup"><span data-stu-id="5a242-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a242-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5a242-110">Return value</span></span>

<span data-ttu-id="5a242-111">Dati dello shader decompressi.</span><span class="sxs-lookup"><span data-stu-id="5a242-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a242-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5a242-112">Requirements</span></span>



| <span data-ttu-id="5a242-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a242-113">Requirement</span></span> | <span data-ttu-id="5a242-114">Valore</span><span class="sxs-lookup"><span data-stu-id="5a242-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a242-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5a242-115">Header</span></span><br/> | <dl> <span data-ttu-id="5a242-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="5a242-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a242-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5a242-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a242-118">Funzioni</span><span class="sxs-lookup"><span data-stu-id="5a242-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="5a242-119">Decompressione e compressione \_ del formato DXGI per la modifica dell'immagine In-Place</span><span class="sxs-lookup"><span data-stu-id="5a242-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





