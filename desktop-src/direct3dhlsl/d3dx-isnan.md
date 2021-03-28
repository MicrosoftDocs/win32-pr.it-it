---
title: Funzione D3DX_IsNan
description: Determina se il valore è NaN (non un numero).
ms.assetid: 862d1d34-36ab-471e-b3ce-ce71896441e5
keywords:
- Funzione D3DX_IsNan HLSL
topic_type:
- apiref
api_name:
- D3DX_IsNan
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60aac82ebfb145bc11aac8d4ab509a4260767a74
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969486"
---
# <a name="d3dx_isnan-function"></a><span data-ttu-id="780e0-104">D3DX \_ isNaN-funzione</span><span class="sxs-lookup"><span data-stu-id="780e0-104">D3DX\_IsNan function</span></span>

<span data-ttu-id="780e0-105">Determina se il valore è NaN (non un numero).</span><span class="sxs-lookup"><span data-stu-id="780e0-105">Determines if the value is a NaN (Not a Number).</span></span>

## <a name="syntax"></a><span data-ttu-id="780e0-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="780e0-106">Syntax</span></span>

``` syntax
bool D3DX_IsNan(
   FLOAT _V
);
```

## <a name="parameters"></a><span data-ttu-id="780e0-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="780e0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="780e0-108">*\_V*</span><span class="sxs-lookup"><span data-stu-id="780e0-108">*\_V*</span></span> 
</dt> <dd>

<span data-ttu-id="780e0-109">Valore specificato.</span><span class="sxs-lookup"><span data-stu-id="780e0-109">The specified value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="780e0-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="780e0-110">Return value</span></span>

<span data-ttu-id="780e0-111">true se NaN; in caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="780e0-111">true if a NaN; otherwise false.</span></span>

## <a name="requirements"></a><span data-ttu-id="780e0-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="780e0-112">Requirements</span></span>



| <span data-ttu-id="780e0-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="780e0-113">Requirement</span></span> | <span data-ttu-id="780e0-114">Valore</span><span class="sxs-lookup"><span data-stu-id="780e0-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="780e0-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="780e0-115">Header</span></span><br/> | <dl> <span data-ttu-id="780e0-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="780e0-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="780e0-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="780e0-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="780e0-118">Funzioni</span><span class="sxs-lookup"><span data-stu-id="780e0-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="780e0-119">Decompressione e compressione \_ del formato DXGI per la modifica dell'immagine In-Place</span><span class="sxs-lookup"><span data-stu-id="780e0-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





