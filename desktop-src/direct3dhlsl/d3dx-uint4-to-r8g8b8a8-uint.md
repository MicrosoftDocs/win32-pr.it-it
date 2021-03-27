---
title: Funzione D3DX_UINT4_to_R8G8B8A8_UINT
description: Comprime di nuovo il XMUINT4 specificato in un \_ formato DXGI \_ R8G8B8A8 \_ uint.
ms.assetid: d4770dfc-1387-40c3-a4f8-365a1421fa3c
keywords:
- Funzione D3DX_UINT4_to_R8G8B8A8_UINT HLSL
topic_type:
- apiref
api_name:
- D3DX_UINT4_to_R8G8B8A8_UINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44ef8128d2d1989e986d8ff11e2d7e42e85f1fbb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995879"
---
# <a name="d3dx_uint4_to_r8g8b8a8_uint-function"></a><span data-ttu-id="c817b-104">D3DX \_ UINT4 \_ a \_ R8G8B8A8 \_ uint Function</span><span class="sxs-lookup"><span data-stu-id="c817b-104">D3DX\_UINT4\_to\_R8G8B8A8\_UINT function</span></span>

<span data-ttu-id="c817b-105">Comprime di nuovo il XMUINT4 specificato in un \_ formato DXGI \_ R8G8B8A8 \_ uint.</span><span class="sxs-lookup"><span data-stu-id="c817b-105">Packs the given XMUINT4 back into a DXGI\_FORMAT\_R8G8B8A8\_UINT.</span></span>

## <a name="syntax"></a><span data-ttu-id="c817b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c817b-106">Syntax</span></span>

``` syntax
UINT D3DX_UINT4_to_R8G8B8A8_UINT(
   hlsl_precise XMUINT4 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="c817b-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="c817b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c817b-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="c817b-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="c817b-109">Dati dello shader da comprimere.</span><span class="sxs-lookup"><span data-stu-id="c817b-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c817b-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c817b-110">Return value</span></span>

<span data-ttu-id="c817b-111">Dati dello shader compressi.</span><span class="sxs-lookup"><span data-stu-id="c817b-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="c817b-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c817b-112">Requirements</span></span>



| <span data-ttu-id="c817b-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c817b-113">Requirement</span></span> | <span data-ttu-id="c817b-114">Valore</span><span class="sxs-lookup"><span data-stu-id="c817b-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c817b-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c817b-115">Header</span></span><br/> | <dl> <span data-ttu-id="c817b-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="c817b-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c817b-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c817b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c817b-118">Funzioni</span><span class="sxs-lookup"><span data-stu-id="c817b-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="c817b-119">Decompressione e compressione \_ del formato DXGI per la modifica dell'immagine In-Place</span><span class="sxs-lookup"><span data-stu-id="c817b-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





