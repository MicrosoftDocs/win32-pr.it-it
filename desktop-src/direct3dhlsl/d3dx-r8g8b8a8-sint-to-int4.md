---
title: Funzione D3DX_R8G8B8A8_SINT_to_INT4
description: Decomprime \_ \_ \_ i dati di DXGI Format R8G8B8A8 Sint shader in un XMINT4.
ms.assetid: 144bd296-02b5-4307-b785-860680db2d52
keywords:
- Funzione D3DX_R8G8B8A8_SINT_to_INT4 HLSL
topic_type:
- apiref
api_name:
- D3DX_R8G8B8A8_SINT_to_INT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d129982db5535d91b38dc9d3630f78192c4b1fbc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132362"
---
# <a name="d3dx_r8g8b8a8_sint_to_int4-function"></a><span data-ttu-id="babdb-104">D3DX \_ R8G8B8A8 \_ \_ -funzione da Sint a \_ INT4</span><span class="sxs-lookup"><span data-stu-id="babdb-104">D3DX\_R8G8B8A8\_SINT\_to\_INT4 function</span></span>

<span data-ttu-id="babdb-105">Decomprime \_ \_ \_ i dati di DXGI Format R8G8B8A8 Sint shader in un XMINT4.</span><span class="sxs-lookup"><span data-stu-id="babdb-105">Unpacks DXGI\_FORMAT\_R8G8B8A8\_SINT shader data to an XMINT4.</span></span>

## <a name="syntax"></a><span data-ttu-id="babdb-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="babdb-106">Syntax</span></span>

``` syntax
XMINT4 D3DX_R8G8B8A8_SINT_to_INT4(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="babdb-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="babdb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="babdb-108">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="babdb-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="babdb-109">Dati dello shader compressi.</span><span class="sxs-lookup"><span data-stu-id="babdb-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="babdb-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="babdb-110">Return value</span></span>

<span data-ttu-id="babdb-111">Dati dello shader decompressi.</span><span class="sxs-lookup"><span data-stu-id="babdb-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="babdb-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="babdb-112">Requirements</span></span>



| <span data-ttu-id="babdb-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="babdb-113">Requirement</span></span> | <span data-ttu-id="babdb-114">Valore</span><span class="sxs-lookup"><span data-stu-id="babdb-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="babdb-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="babdb-115">Header</span></span><br/> | <dl> <span data-ttu-id="babdb-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="babdb-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="babdb-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="babdb-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="babdb-118">Funzioni</span><span class="sxs-lookup"><span data-stu-id="babdb-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="babdb-119">Decompressione e compressione \_ del formato DXGI per la modifica dell'immagine In-Place</span><span class="sxs-lookup"><span data-stu-id="babdb-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





