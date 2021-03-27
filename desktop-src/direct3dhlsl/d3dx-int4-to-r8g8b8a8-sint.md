---
title: Funzione D3DX_INT4_to_R8G8B8A8_SINT
description: Comprime di nuovo il XMINT4 specificato in un \_ formato DXGI \_ R8G8B8A8 \_ Sint.
ms.assetid: ab9c5454-1673-43a9-ab76-bcd7b510b9a8
keywords:
- Funzione D3DX_INT4_to_R8G8B8A8_SINT HLSL
topic_type:
- apiref
api_name:
- D3DX_INT4_to_R8G8B8A8_SINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9df4e4094ac96e7da2ccbff1da08e7aa1f7c4de
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995822"
---
# <a name="d3dx_int4_to_r8g8b8a8_sint-function"></a><span data-ttu-id="19994-104">D3DX \_ INT4 \_ to \_ R8G8B8A8 \_ Sint Function</span><span class="sxs-lookup"><span data-stu-id="19994-104">D3DX\_INT4\_to\_R8G8B8A8\_SINT function</span></span>

<span data-ttu-id="19994-105">Comprime di nuovo il XMINT4 specificato in un \_ formato DXGI \_ R8G8B8A8 \_ Sint.</span><span class="sxs-lookup"><span data-stu-id="19994-105">Packs the given XMINT4 back into a DXGI\_FORMAT\_R8G8B8A8\_SINT.</span></span>

## <a name="syntax"></a><span data-ttu-id="19994-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="19994-106">Syntax</span></span>

``` syntax
UINT D3DX_INT4_to_R8G8B8A8_SINT(
   hlsl_precise XMINT4 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="19994-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="19994-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19994-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="19994-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="19994-109">Dati dello shader da comprimere.</span><span class="sxs-lookup"><span data-stu-id="19994-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19994-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="19994-110">Return value</span></span>

<span data-ttu-id="19994-111">Dati dello shader compressi.</span><span class="sxs-lookup"><span data-stu-id="19994-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="19994-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="19994-112">Requirements</span></span>



| <span data-ttu-id="19994-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="19994-113">Requirement</span></span> | <span data-ttu-id="19994-114">Valore</span><span class="sxs-lookup"><span data-stu-id="19994-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19994-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="19994-115">Header</span></span><br/> | <dl> <span data-ttu-id="19994-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="19994-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19994-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="19994-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19994-118">Funzioni</span><span class="sxs-lookup"><span data-stu-id="19994-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="19994-119">Decompressione e compressione \_ del formato DXGI per la modifica dell'immagine In-Place</span><span class="sxs-lookup"><span data-stu-id="19994-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





