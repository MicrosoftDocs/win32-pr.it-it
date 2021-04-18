---
description: La \_ struttura dell'elemento KSMULTIPLE descrive le dimensioni e il numero di proprietà a lunghezza variabile nei pin della modalità kernel.
ms.assetid: aedbf7bc-393d-4ab5-afcd-d8822b925f07
title: Struttura KSMULTIPLE_ITEM (KS. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KSMULTIPLE_ITEM
api_type:
- HeaderDef
api_location:
- ks.h
ms.openlocfilehash: 62e26b1aa8804514588e66c1d02e1f0643e97bcb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330393"
---
# <a name="ksmultiple_item-structure"></a><span data-ttu-id="d41e2-103">\_Struttura dell'elemento KSMULTIPLE</span><span class="sxs-lookup"><span data-stu-id="d41e2-103">KSMULTIPLE\_ITEM structure</span></span>

<span data-ttu-id="d41e2-104">La `KSMULTIPLE_ITEM` struttura descrive le dimensioni e il numero di proprietà a lunghezza variabile nei pin della modalità kernel.</span><span class="sxs-lookup"><span data-stu-id="d41e2-104">The `KSMULTIPLE_ITEM` structure describes the size and count of variable-length properties on kernel-mode pins.</span></span>

## <a name="syntax"></a><span data-ttu-id="d41e2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d41e2-105">Syntax</span></span>


```C++
typedef struct {
  ULONG Size;
  ULONG Count;
} KSMULTIPLE_ITEM, *PKSMULTIPLE_ITEM;
```



## <a name="members"></a><span data-ttu-id="d41e2-106">Members</span><span class="sxs-lookup"><span data-stu-id="d41e2-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d41e2-107">**Dimensioni**</span><span class="sxs-lookup"><span data-stu-id="d41e2-107">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="d41e2-108">Dimensioni in byte del blocco di memoria restituito.</span><span class="sxs-lookup"><span data-stu-id="d41e2-108">Size of the returned memory block, in bytes.</span></span> <span data-ttu-id="d41e2-109">La dimensione include la struttura dell' **\_ elemento KSMULTIPLE** e gli elementi che lo seguono.</span><span class="sxs-lookup"><span data-stu-id="d41e2-109">The size includes the **KSMULTIPLE\_ITEM** structure and the items that follow it.</span></span>

</dd> <dt>

<span data-ttu-id="d41e2-110">**Count**</span><span class="sxs-lookup"><span data-stu-id="d41e2-110">**Count**</span></span>
</dt> <dd>

<span data-ttu-id="d41e2-111">Specifica il numero totale di elementi che seguono la struttura.</span><span class="sxs-lookup"><span data-stu-id="d41e2-111">Specifies the total number of items that follow this structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d41e2-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d41e2-112">Requirements</span></span>



| <span data-ttu-id="d41e2-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="d41e2-113">Requirement</span></span> | <span data-ttu-id="d41e2-114">Valore</span><span class="sxs-lookup"><span data-stu-id="d41e2-114">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="d41e2-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d41e2-115">Header</span></span><br/> | <dl> <span data-ttu-id="d41e2-116"><dt>KS. h</dt></span><span class="sxs-lookup"><span data-stu-id="d41e2-116"><dt>Ks.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d41e2-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d41e2-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d41e2-118">Strutture DirectShow</span><span class="sxs-lookup"><span data-stu-id="d41e2-118">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="d41e2-119">**IKsPin::KsQueryMediums**</span><span class="sxs-lookup"><span data-stu-id="d41e2-119">**IKsPin::KsQueryMediums**</span></span>](ikspin-ksquerymediums.md)
</dt> <dt>

[<span data-ttu-id="d41e2-120">**REGPINMEDIUM**</span><span class="sxs-lookup"><span data-stu-id="d41e2-120">**REGPINMEDIUM**</span></span>](/windows/desktop/api/strmif/ns-strmif-regpinmedium)
</dt> </dl>

 

 




