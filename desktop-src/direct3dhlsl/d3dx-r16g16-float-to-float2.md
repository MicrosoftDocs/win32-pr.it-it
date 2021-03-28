---
title: Funzione D3DX_R16G16_FLOAT_to_FLOAT2
description: Decomprime \_ \_ \_ i dati di DXGI Format B8G8R8X8 UNORM \_ sRGB shader in un XMFLOAT2.
ms.assetid: 6c57dc86-d034-4b54-8572-44ac3738beb9
keywords:
- Funzione D3DX_R16G16_FLOAT_to_FLOAT2 HLSL
topic_type:
- apiref
api_name:
- D3DX_R16G16_FLOAT_to_FLOAT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e6fb721e59a63415f98216b6e3f81a92e7598f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132394"
---
# <a name="d3dx_r16g16_float_to_float2-function"></a><span data-ttu-id="be910-104">D3DX \_ R16G16 \_ float \_ to \_ FLOAT2 Function</span><span class="sxs-lookup"><span data-stu-id="be910-104">D3DX\_R16G16\_FLOAT\_to\_FLOAT2 function</span></span>

<span data-ttu-id="be910-105">Decomprime \_ \_ \_ i dati di DXGI Format B8G8R8X8 UNORM \_ sRGB shader in un XMFLOAT2.</span><span class="sxs-lookup"><span data-stu-id="be910-105">Unpacks DXGI\_FORMAT\_B8G8R8X8\_UNORM\_SRGB shader data to an XMFLOAT2.</span></span>

## <a name="syntax"></a><span data-ttu-id="be910-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="be910-106">Syntax</span></span>

``` syntax
XMFLOAT2 D3DX_R16G16_FLOAT_to_FLOAT2(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="be910-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="be910-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be910-108">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="be910-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="be910-109">Dati dello shader compressi.</span><span class="sxs-lookup"><span data-stu-id="be910-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be910-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="be910-110">Return value</span></span>

<span data-ttu-id="be910-111">Dati dello shader decompressi.</span><span class="sxs-lookup"><span data-stu-id="be910-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="be910-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="be910-112">Requirements</span></span>



| <span data-ttu-id="be910-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="be910-113">Requirement</span></span> | <span data-ttu-id="be910-114">Valore</span><span class="sxs-lookup"><span data-stu-id="be910-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be910-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="be910-115">Header</span></span><br/> | <dl> <span data-ttu-id="be910-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="be910-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be910-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="be910-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be910-118">Funzioni</span><span class="sxs-lookup"><span data-stu-id="be910-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="be910-119">Decompressione e compressione \_ del formato DXGI per la modifica dell'immagine In-Place</span><span class="sxs-lookup"><span data-stu-id="be910-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





