---
title: Funzione D3DX_Saturate_FLOAT
description: Recupera il valore saturo del FLOAT specificato.
ms.assetid: 659df450-3535-44eb-b867-89529369f903
keywords:
- Funzione D3DX_Saturate_FLOAT HLSL
topic_type:
- apiref
api_name:
- D3DX_Saturate_FLOAT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3deabf5140d4f3f3bdfc2d6cce52f32385987ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103886299"
---
# <a name="d3dx_saturate_float-function"></a><span data-ttu-id="48106-104">\_Funzione D3DX saturate \_ float</span><span class="sxs-lookup"><span data-stu-id="48106-104">D3DX\_Saturate\_FLOAT function</span></span>

<span data-ttu-id="48106-105">Recupera il valore saturo del FLOAT specificato.</span><span class="sxs-lookup"><span data-stu-id="48106-105">Retrieves the saturated value of the given FLOAT.</span></span>

## <a name="syntax"></a><span data-ttu-id="48106-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="48106-106">Syntax</span></span>

``` syntax
FLOAT D3DX_Saturate_FLOAT(
   FLOAT _V
);
```

## <a name="parameters"></a><span data-ttu-id="48106-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="48106-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48106-108">*\_V*</span><span class="sxs-lookup"><span data-stu-id="48106-108">*\_V*</span></span> 
</dt> <dd>

<span data-ttu-id="48106-109">Valore da saturare.</span><span class="sxs-lookup"><span data-stu-id="48106-109">The value to saturate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48106-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="48106-110">Return value</span></span>

<span data-ttu-id="48106-111">Valore saturato.</span><span class="sxs-lookup"><span data-stu-id="48106-111">The saturated value.</span></span>

## <a name="requirements"></a><span data-ttu-id="48106-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="48106-112">Requirements</span></span>



| <span data-ttu-id="48106-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="48106-113">Requirement</span></span> | <span data-ttu-id="48106-114">Valore</span><span class="sxs-lookup"><span data-stu-id="48106-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48106-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="48106-115">Header</span></span><br/> | <dl> <span data-ttu-id="48106-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="48106-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48106-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="48106-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48106-118">Funzioni</span><span class="sxs-lookup"><span data-stu-id="48106-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="48106-119">Decompressione e compressione \_ del formato DXGI per la modifica dell'immagine In-Place</span><span class="sxs-lookup"><span data-stu-id="48106-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





