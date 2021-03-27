---
title: Funzione D3DX_FLOAT4_to_R8G8B8A8_UNORM
description: Decomprime \_ \_ \_ i dati di DXGI Format R8G8B8A8 UNORM shader in un XMFLOAT4. | Funzione D3DX_FLOAT4_to_R8G8B8A8_UNORM
ms.assetid: c589c1e5-24ee-4fd7-b18d-5ede52f9f05d
keywords:
- Funzione D3DX_FLOAT4_to_R8G8B8A8_UNORM HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_R8G8B8A8_UNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 603fa1e887ed54e62502b70602e89f97c7cdffa0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762323"
---
# <a name="d3dx_float4_to_r8g8b8a8_unorm-function"></a><span data-ttu-id="d9687-105">D3DX \_ float4 \_ to \_ R8G8B8A8 \_ UNORM Function</span><span class="sxs-lookup"><span data-stu-id="d9687-105">D3DX\_FLOAT4\_to\_R8G8B8A8\_UNORM function</span></span>

<span data-ttu-id="d9687-106">Decomprime \_ \_ \_ i dati di DXGI Format R8G8B8A8 UNORM shader in un XMFLOAT4.</span><span class="sxs-lookup"><span data-stu-id="d9687-106">Unpacks DXGI\_FORMAT\_R8G8B8A8\_UNORM shader data to an XMFLOAT4.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9687-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d9687-107">Syntax</span></span>

``` syntax
XMFLOAT4 D3DX_FLOAT4_to_R8G8B8A8_UNORM(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="d9687-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d9687-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9687-109">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="d9687-109">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="d9687-110">Dati dello shader compressi.</span><span class="sxs-lookup"><span data-stu-id="d9687-110">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9687-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d9687-111">Return value</span></span>

<span data-ttu-id="d9687-112">Dati dello shader decompressi.</span><span class="sxs-lookup"><span data-stu-id="d9687-112">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9687-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d9687-113">Requirements</span></span>



| <span data-ttu-id="d9687-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9687-114">Requirement</span></span> | <span data-ttu-id="d9687-115">Valore</span><span class="sxs-lookup"><span data-stu-id="d9687-115">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9687-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d9687-116">Header</span></span><br/> | <dl> <span data-ttu-id="d9687-117"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="d9687-117"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9687-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d9687-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9687-119">Funzioni</span><span class="sxs-lookup"><span data-stu-id="d9687-119">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="d9687-120">Decompressione e compressione \_ del formato DXGI per la modifica dell'immagine In-Place</span><span class="sxs-lookup"><span data-stu-id="d9687-120">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





