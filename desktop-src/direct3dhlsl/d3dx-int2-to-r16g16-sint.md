---
title: Funzione D3DX_INT2_to_R16G16_SINT
description: Comprime di nuovo il XMINT2 specificato in un \_ formato DXGI \_ R16G16 \_ Sint.
ms.assetid: dc37e8a3-31d4-4af6-9bc3-9aa5062c066a
keywords:
- Funzione D3DX_INT2_to_R16G16_SINT HLSL
topic_type:
- apiref
api_name:
- D3DX_INT2_to_R16G16_SINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a97d60ba29b2451dea973b4ec0453f3a4df2ecdd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982531"
---
# <a name="d3dx_int2_to_r16g16_sint-function"></a><span data-ttu-id="b65f9-104">D3DX \_ int2 \_ to \_ R16G16 \_ Sint Function</span><span class="sxs-lookup"><span data-stu-id="b65f9-104">D3DX\_INT2\_to\_R16G16\_SINT function</span></span>

<span data-ttu-id="b65f9-105">Comprime di nuovo il XMINT2 specificato in un \_ formato DXGI \_ R16G16 \_ Sint.</span><span class="sxs-lookup"><span data-stu-id="b65f9-105">Packs the given XMINT2 back into a DXGI\_FORMAT\_R16G16\_SINT.</span></span>

## <a name="syntax"></a><span data-ttu-id="b65f9-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b65f9-106">Syntax</span></span>

``` syntax
UINT D3DX_INT2_to_R16G16_SINT(
   hlsl_precise XMINT2 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="b65f9-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="b65f9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b65f9-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="b65f9-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="b65f9-109">Dati dello shader da comprimere.</span><span class="sxs-lookup"><span data-stu-id="b65f9-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b65f9-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b65f9-110">Return value</span></span>

<span data-ttu-id="b65f9-111">Dati dello shader compressi.</span><span class="sxs-lookup"><span data-stu-id="b65f9-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="b65f9-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b65f9-112">Requirements</span></span>



| <span data-ttu-id="b65f9-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="b65f9-113">Requirement</span></span> | <span data-ttu-id="b65f9-114">Valore</span><span class="sxs-lookup"><span data-stu-id="b65f9-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b65f9-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b65f9-115">Header</span></span><br/> | <dl> <span data-ttu-id="b65f9-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="b65f9-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b65f9-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b65f9-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b65f9-118">Funzioni</span><span class="sxs-lookup"><span data-stu-id="b65f9-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="b65f9-119">Decompressione e compressione \_ del formato DXGI per la modifica dell'immagine In-Place</span><span class="sxs-lookup"><span data-stu-id="b65f9-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





