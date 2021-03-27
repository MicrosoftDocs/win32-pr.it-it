---
title: Funzione D3DX_FLOAT_to_UINT
description: Converte un valore FLOAT in UINT.
ms.assetid: 05c5de72-8915-4541-a82d-242e46bfa883
keywords:
- Funzione D3DX_FLOAT_to_UINT HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT_to_UINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e729ba805d63068844192a134236722288fe8a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354294"
---
# <a name="d3dx_float_to_uint-function"></a><span data-ttu-id="4a865-104">\_Funzione float D3DX \_ a \_ uint</span><span class="sxs-lookup"><span data-stu-id="4a865-104">D3DX\_FLOAT\_to\_UINT function</span></span>

<span data-ttu-id="4a865-105">Converte un valore FLOAT in UINT.</span><span class="sxs-lookup"><span data-stu-id="4a865-105">Converts a FLOAT value to UINT.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a865-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4a865-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT_to_UINT(
   FLOAT _V,
   FLOAT _Scale
);
```

## <a name="parameters"></a><span data-ttu-id="4a865-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="4a865-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a865-108">*\_V*</span><span class="sxs-lookup"><span data-stu-id="4a865-108">*\_V*</span></span> 
</dt> <dd>

<span data-ttu-id="4a865-109">Vettore v.</span><span class="sxs-lookup"><span data-stu-id="4a865-109">The v vector.</span></span>

</dd> <dt>

<span data-ttu-id="4a865-110">*\_Scalabilità*</span><span class="sxs-lookup"><span data-stu-id="4a865-110">*\_Scale*</span></span> 
</dt> <dd>

<span data-ttu-id="4a865-111">Valore della scala.</span><span class="sxs-lookup"><span data-stu-id="4a865-111">The scale value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a865-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4a865-112">Return value</span></span>

<span data-ttu-id="4a865-113">Valore FLOAT convertito</span><span class="sxs-lookup"><span data-stu-id="4a865-113">The converted FLOAT value</span></span>

## <a name="requirements"></a><span data-ttu-id="4a865-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4a865-114">Requirements</span></span>



| <span data-ttu-id="4a865-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a865-115">Requirement</span></span> | <span data-ttu-id="4a865-116">Valore</span><span class="sxs-lookup"><span data-stu-id="4a865-116">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a865-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4a865-117">Header</span></span><br/> | <dl> <span data-ttu-id="4a865-118"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="4a865-118"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a865-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4a865-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a865-120">Funzioni</span><span class="sxs-lookup"><span data-stu-id="4a865-120">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="4a865-121">Decompressione e compressione \_ del formato DXGI per la modifica dell'immagine In-Place</span><span class="sxs-lookup"><span data-stu-id="4a865-121">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





