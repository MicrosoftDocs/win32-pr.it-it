---
title: Funzione D3DX_FLOAT_to_INT
description: Converte un valore FLOAT in INT.
ms.assetid: 69b67218-fe25-478f-9f7e-05f94d9f99d5
keywords:
- Funzione D3DX_FLOAT_to_INT HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT_to_INT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c127ef20cdd21cbc83e466f75844b4f80f47f948
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104531063"
---
# <a name="d3dx_float_to_int-function"></a><span data-ttu-id="e4b28-104">\_Funzione D3DX float \_ to \_ int</span><span class="sxs-lookup"><span data-stu-id="e4b28-104">D3DX\_FLOAT\_to\_INT function</span></span>

<span data-ttu-id="e4b28-105">Converte un valore FLOAT in INT.</span><span class="sxs-lookup"><span data-stu-id="e4b28-105">Converts a FLOAT value to INT.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4b28-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e4b28-106">Syntax</span></span>

``` syntax
INT D3DX_FLOAT_to_INT(
   FLOAT _V,
   FLOAT _Scale
);
```

## <a name="parameters"></a><span data-ttu-id="e4b28-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="e4b28-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4b28-108">*\_V*</span><span class="sxs-lookup"><span data-stu-id="e4b28-108">*\_V*</span></span> 
</dt> <dd>

<span data-ttu-id="e4b28-109">Valore v.</span><span class="sxs-lookup"><span data-stu-id="e4b28-109">The v value.</span></span>

</dd> <dt>

<span data-ttu-id="e4b28-110">*\_Scalabilità*</span><span class="sxs-lookup"><span data-stu-id="e4b28-110">*\_Scale*</span></span> 
</dt> <dd>

<span data-ttu-id="e4b28-111">Valore della scala.</span><span class="sxs-lookup"><span data-stu-id="e4b28-111">The scale value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4b28-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e4b28-112">Return value</span></span>

<span data-ttu-id="e4b28-113">Valore FLOAT convertito</span><span class="sxs-lookup"><span data-stu-id="e4b28-113">The converted FLOAT value</span></span>

## <a name="requirements"></a><span data-ttu-id="e4b28-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e4b28-114">Requirements</span></span>



| <span data-ttu-id="e4b28-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4b28-115">Requirement</span></span> | <span data-ttu-id="e4b28-116">Valore</span><span class="sxs-lookup"><span data-stu-id="e4b28-116">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4b28-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e4b28-117">Header</span></span><br/> | <dl> <span data-ttu-id="e4b28-118"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="e4b28-118"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4b28-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e4b28-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4b28-120">Funzioni</span><span class="sxs-lookup"><span data-stu-id="e4b28-120">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="e4b28-121">Decompressione e compressione \_ del formato DXGI per la modifica dell'immagine In-Place</span><span class="sxs-lookup"><span data-stu-id="e4b28-121">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





