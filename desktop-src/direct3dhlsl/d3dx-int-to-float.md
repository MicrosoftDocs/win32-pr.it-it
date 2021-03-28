---
title: Funzione D3DX_INT_to_FLOAT
description: Converte un valore INT in FLOAT.
ms.assetid: bee2fb3e-ffde-4013-a321-275d6beb5f77
keywords:
- Funzione D3DX_INT_to_FLOAT HLSL
topic_type:
- apiref
api_name:
- D3DX_INT_to_FLOAT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06a4d588661b1b2f5ddc14c7564699c7d2b47b4e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982499"
---
# <a name="d3dx_int_to_float-function"></a><span data-ttu-id="faa6c-104">D3DX \_ int \_ to \_ float-funzione</span><span class="sxs-lookup"><span data-stu-id="faa6c-104">D3DX\_INT\_to\_FLOAT function</span></span>

<span data-ttu-id="faa6c-105">Converte un valore INT in FLOAT.</span><span class="sxs-lookup"><span data-stu-id="faa6c-105">Converts a INT value to FLOAT.</span></span>

## <a name="syntax"></a><span data-ttu-id="faa6c-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="faa6c-106">Syntax</span></span>

``` syntax
FLOAT D3DX_INT_to_FLOAT(
   INT _V,
   FLOAT _Scale
);
```

## <a name="parameters"></a><span data-ttu-id="faa6c-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="faa6c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="faa6c-108">*\_V*</span><span class="sxs-lookup"><span data-stu-id="faa6c-108">*\_V*</span></span> 
</dt> <dd>

<span data-ttu-id="faa6c-109">Valore v.</span><span class="sxs-lookup"><span data-stu-id="faa6c-109">The v value.</span></span>

</dd> <dt>

<span data-ttu-id="faa6c-110">*\_Scalabilità*</span><span class="sxs-lookup"><span data-stu-id="faa6c-110">*\_Scale*</span></span> 
</dt> <dd>

<span data-ttu-id="faa6c-111">Valore della scala.</span><span class="sxs-lookup"><span data-stu-id="faa6c-111">The scale value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="faa6c-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="faa6c-112">Return value</span></span>

<span data-ttu-id="faa6c-113">Valore int convertito.</span><span class="sxs-lookup"><span data-stu-id="faa6c-113">The converted int value.</span></span>

## <a name="requirements"></a><span data-ttu-id="faa6c-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="faa6c-114">Requirements</span></span>



| <span data-ttu-id="faa6c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="faa6c-115">Requirement</span></span> | <span data-ttu-id="faa6c-116">Valore</span><span class="sxs-lookup"><span data-stu-id="faa6c-116">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="faa6c-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="faa6c-117">Header</span></span><br/> | <dl> <span data-ttu-id="faa6c-118"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="faa6c-118"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="faa6c-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="faa6c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="faa6c-120">Funzioni</span><span class="sxs-lookup"><span data-stu-id="faa6c-120">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="faa6c-121">Decompressione e compressione \_ del formato DXGI per la modifica dell'immagine In-Place</span><span class="sxs-lookup"><span data-stu-id="faa6c-121">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





