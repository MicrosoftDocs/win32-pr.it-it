---
title: Funzione D3DX_UINT4_to_R10G10B10A2_UINT
description: Comprime di nuovo il XMINT4 specificato in un \_ formato DXGI \_ R10G10B10A2 \_ uint.
ms.assetid: fe10c62e-2d84-4f6b-886b-247ee344f6c7
keywords:
- Funzione D3DX_UINT4_to_R10G10B10A2_UINT HLSL
topic_type:
- apiref
api_name:
- D3DX_UINT4_to_R10G10B10A2_UINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfc7076b9e44ab1491bb8abbf8d4edb82158282c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995882"
---
# <a name="d3dx_uint4_to_r10g10b10a2_uint-function"></a><span data-ttu-id="06766-104">D3DX \_ UINT4 \_ a \_ R10G10B10A2 \_ uint Function</span><span class="sxs-lookup"><span data-stu-id="06766-104">D3DX\_UINT4\_to\_R10G10B10A2\_UINT function</span></span>

<span data-ttu-id="06766-105">Comprime di nuovo il XMINT4 specificato in un \_ formato DXGI \_ R10G10B10A2 \_ uint.</span><span class="sxs-lookup"><span data-stu-id="06766-105">Packs the given XMINT4 back into a DXGI\_FORMAT\_R10G10B10A2\_UINT.</span></span>

## <a name="syntax"></a><span data-ttu-id="06766-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="06766-106">Syntax</span></span>

``` syntax
UINT D3DX_UINT4_to_R10G10B10A2_UINT(
   hlsl_precise XMINT4 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="06766-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="06766-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06766-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="06766-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="06766-109">Dati dello shader da comprimere.</span><span class="sxs-lookup"><span data-stu-id="06766-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06766-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="06766-110">Return value</span></span>

<span data-ttu-id="06766-111">Dati dello shader compressi.</span><span class="sxs-lookup"><span data-stu-id="06766-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="06766-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06766-112">Requirements</span></span>



| <span data-ttu-id="06766-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="06766-113">Requirement</span></span> | <span data-ttu-id="06766-114">Valore</span><span class="sxs-lookup"><span data-stu-id="06766-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06766-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="06766-115">Header</span></span><br/> | <dl> <span data-ttu-id="06766-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="06766-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06766-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="06766-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06766-118">Funzioni</span><span class="sxs-lookup"><span data-stu-id="06766-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="06766-119">Decompressione e compressione \_ del formato DXGI per la modifica dell'immagine In-Place</span><span class="sxs-lookup"><span data-stu-id="06766-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





