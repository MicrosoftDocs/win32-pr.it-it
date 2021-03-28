---
title: Funzione D3DX_R10G10B10A2_UNORM_to_FLOAT4
description: Decomprime \_ \_ \_ i dati di DXGI Format R10G10B10A2 UNORM shader in un XMFLOAT4.
ms.assetid: 36efd611-1450-421a-a34f-fd874589de2a
keywords:
- Funzione D3DX_R10G10B10A2_UNORM_to_FLOAT4 HLSL
topic_type:
- apiref
api_name:
- D3DX_R10G10B10A2_UNORM_to_FLOAT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6c93bd6fb9cce07ee13a873b4fade91bd322824
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982486"
---
# <a name="d3dx_r10g10b10a2_unorm_to_float4-function"></a><span data-ttu-id="179ac-104">D3DX \_ R10G10B10A2 \_ UNORM \_ to \_ float4 Function</span><span class="sxs-lookup"><span data-stu-id="179ac-104">D3DX\_R10G10B10A2\_UNORM\_to\_FLOAT4 function</span></span>

<span data-ttu-id="179ac-105">Decomprime \_ \_ \_ i dati di DXGI Format R10G10B10A2 UNORM shader in un XMFLOAT4.</span><span class="sxs-lookup"><span data-stu-id="179ac-105">Unpacks DXGI\_FORMAT\_R10G10B10A2\_UNORM shader data to an XMFLOAT4.</span></span>

## <a name="syntax"></a><span data-ttu-id="179ac-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="179ac-106">Syntax</span></span>

``` syntax
XMFLOAT4 D3DX_R10G10B10A2_UNORM_to_FLOAT4(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="179ac-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="179ac-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="179ac-108">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="179ac-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="179ac-109">Dati dello shader compressi.</span><span class="sxs-lookup"><span data-stu-id="179ac-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="179ac-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="179ac-110">Return value</span></span>

<span data-ttu-id="179ac-111">Dati dello shader decompressi.</span><span class="sxs-lookup"><span data-stu-id="179ac-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="179ac-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="179ac-112">Requirements</span></span>



| <span data-ttu-id="179ac-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="179ac-113">Requirement</span></span> | <span data-ttu-id="179ac-114">Valore</span><span class="sxs-lookup"><span data-stu-id="179ac-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="179ac-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="179ac-115">Header</span></span><br/> | <dl> <span data-ttu-id="179ac-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="179ac-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="179ac-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="179ac-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="179ac-118">Funzioni</span><span class="sxs-lookup"><span data-stu-id="179ac-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="179ac-119">Decompressione e compressione \_ del formato DXGI per la modifica dell'immagine In-Place</span><span class="sxs-lookup"><span data-stu-id="179ac-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





