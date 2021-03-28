---
title: Struttura XMINT4
description: Descrive un vettore di Integer 4D.
ms.assetid: 1f21727d-fcb4-4514-b30e-d8ef0e36c256
keywords:
- Struttura XMINT4 HLSL
topic_type:
- apiref
api_name:
- XMINT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 302d820428fafb1561bd38850c4f75240ce9094f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355379"
---
# <a name="xmint4-structure"></a><span data-ttu-id="54b06-104">Struttura XMINT4</span><span class="sxs-lookup"><span data-stu-id="54b06-104">XMINT4 structure</span></span>

<span data-ttu-id="54b06-105">Descrive un vettore di Integer 4D.</span><span class="sxs-lookup"><span data-stu-id="54b06-105">Describes an 4D integer vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="54b06-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="54b06-106">Syntax</span></span>


``` syntax
typedef struct _XMINT4 {
  INT x;
  INT {
    INT {
      INT w;
    }z;
  }y;
} XMINT4;
```



## <a name="members"></a><span data-ttu-id="54b06-107">Members</span><span class="sxs-lookup"><span data-stu-id="54b06-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="54b06-108">**x**</span><span class="sxs-lookup"><span data-stu-id="54b06-108">**x**</span></span>
</dt> <dd>

<span data-ttu-id="54b06-109">componente x del vettore.</span><span class="sxs-lookup"><span data-stu-id="54b06-109">x-component of the vector.</span></span>

</dd> <dt>

<span data-ttu-id="54b06-110">**y**</span><span class="sxs-lookup"><span data-stu-id="54b06-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="54b06-111">componente y del vettore.</span><span class="sxs-lookup"><span data-stu-id="54b06-111">y-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="54b06-112">**z**</span><span class="sxs-lookup"><span data-stu-id="54b06-112">**z**</span></span>
</dt> <dd>

<span data-ttu-id="54b06-113">componente z del vettore.</span><span class="sxs-lookup"><span data-stu-id="54b06-113">z-component of the vector.</span></span>

<dl> <dt>

<span data-ttu-id="54b06-114">**w**</span><span class="sxs-lookup"><span data-stu-id="54b06-114">**w**</span></span>
</dt> <dd>

<span data-ttu-id="54b06-115">componente w del vettore.</span><span class="sxs-lookup"><span data-stu-id="54b06-115">w-component of the vector.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="54b06-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="54b06-116">Requirements</span></span>



| <span data-ttu-id="54b06-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="54b06-117">Requirement</span></span> | <span data-ttu-id="54b06-118">Valore</span><span class="sxs-lookup"><span data-stu-id="54b06-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54b06-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="54b06-119">Header</span></span><br/> | <dl> <span data-ttu-id="54b06-120"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="54b06-120"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54b06-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="54b06-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54b06-122">Strutture</span><span class="sxs-lookup"><span data-stu-id="54b06-122">Structures</span></span>](format-conversion-structures.md)
</dt> <dt>

[<span data-ttu-id="54b06-123">Decompressione e compressione \_ del formato DXGI per la modifica dell'immagine In-Place</span><span class="sxs-lookup"><span data-stu-id="54b06-123">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





