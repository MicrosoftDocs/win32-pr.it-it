---
title: Struttura XMUINT4
description: Descrive un vettore di Unsigned Integer 4D.
ms.assetid: 289293e5-882e-479c-886e-82c802f824b5
keywords:
- Struttura XMUINT4 HLSL
topic_type:
- apiref
api_name:
- XMUINT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f0b02ffe64e7b4c4479723b4e36abd87f6bd03b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982097"
---
# <a name="xmuint4-structure"></a><span data-ttu-id="a550a-104">Struttura XMUINT4</span><span class="sxs-lookup"><span data-stu-id="a550a-104">XMUINT4 structure</span></span>

<span data-ttu-id="a550a-105">Descrive un vettore di Unsigned Integer 4D.</span><span class="sxs-lookup"><span data-stu-id="a550a-105">Describes an 4D unsigned integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="a550a-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a550a-106">Syntax</span></span>


``` syntax
typedef struct _XMUINT4 {
  UINT x;
  UINT {
    UINT {
      UINT w;
    }z;
  }y;
} XMUINT4;
```



## <a name="members"></a><span data-ttu-id="a550a-107">Members</span><span class="sxs-lookup"><span data-stu-id="a550a-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="a550a-108">**x**</span><span class="sxs-lookup"><span data-stu-id="a550a-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="a550a-109">componente x del vettore.</span><span class="sxs-lookup"><span data-stu-id="a550a-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="a550a-110">**y**</span><span class="sxs-lookup"><span data-stu-id="a550a-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="a550a-111">componente y del vettore.</span><span class="sxs-lookup"><span data-stu-id="a550a-111">y-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="a550a-112">**z**</span><span class="sxs-lookup"><span data-stu-id="a550a-112">**z**</span></span>
</dt> <dd>

<span data-ttu-id="a550a-113">componente z del vettore.</span><span class="sxs-lookup"><span data-stu-id="a550a-113">z-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="a550a-114">**w**</span><span class="sxs-lookup"><span data-stu-id="a550a-114">**w**</span></span>
</dt> <dd>

<span data-ttu-id="a550a-115">componente w del vettore.</span><span class="sxs-lookup"><span data-stu-id="a550a-115">w-component of the vector.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a550a-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a550a-116">Requirements</span></span>



| <span data-ttu-id="a550a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a550a-117">Requirement</span></span> | <span data-ttu-id="a550a-118">Valore</span><span class="sxs-lookup"><span data-stu-id="a550a-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a550a-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a550a-119">Header</span></span><br/> | <dl> <span data-ttu-id="a550a-120"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="a550a-120"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a550a-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a550a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a550a-122">Strutture</span><span class="sxs-lookup"><span data-stu-id="a550a-122">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="a550a-123">Decompressione e compressione \_ del formato DXGI per la modifica dell'immagine In-Place</span><span class="sxs-lookup"><span data-stu-id="a550a-123">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





