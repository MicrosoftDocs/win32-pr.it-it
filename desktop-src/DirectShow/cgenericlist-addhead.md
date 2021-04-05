---
description: Il metodo AddHead aggiunge un elemento all'inizio dell'elenco.
ms.assetid: 8f0012b7-bbc2-407c-ae5a-9843c2f692dc
title: Metodo CGenericList. AddHead (Wxlist. h)-parametro pObj
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62a32eb177c80d10a876a4b163c8a1609104fbea
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "104058706"
---
# <a name="cgenericlistaddhead-method-wxlisth---pobj-parameter"></a><span data-ttu-id="41fd7-103">Metodo CGenericList. AddHead (Wxlist. h)-parametro pObj</span><span class="sxs-lookup"><span data-stu-id="41fd7-103">CGenericList.AddHead method (Wxlist.h) - pObj parameter</span></span>

<span data-ttu-id="41fd7-104">Il `AddHead` metodo aggiunge un elemento all'inizio dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="41fd7-104">The `AddHead` method adds an item to the front of the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="41fd7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="41fd7-105">Syntax</span></span>


```C++
POSITION AddHead(
   OBJECT *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="41fd7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="41fd7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41fd7-107">*pObj*</span><span class="sxs-lookup"><span data-stu-id="41fd7-107">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="41fd7-108">Puntatore a un oggetto di tipo **Object** (il tipo di modello).</span><span class="sxs-lookup"><span data-stu-id="41fd7-108">Pointer to an object of type **OBJECT** (the template type).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41fd7-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="41fd7-109">Return value</span></span>

<span data-ttu-id="41fd7-110">Restituisce un valore di posizione che indica la nuova posizione Head.</span><span class="sxs-lookup"><span data-stu-id="41fd7-110">Returns a POSITION value indicating the new head position.</span></span> <span data-ttu-id="41fd7-111">Se il metodo ha esito negativo, il valore restituito è **null**.</span><span class="sxs-lookup"><span data-stu-id="41fd7-111">If the method fails, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="41fd7-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="41fd7-112">Requirements</span></span>

| <span data-ttu-id="41fd7-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="41fd7-113">Requirement</span></span> | <span data-ttu-id="41fd7-114">Valore</span><span class="sxs-lookup"><span data-stu-id="41fd7-114">Value</span></span> |
|-|-|
| <span data-ttu-id="41fd7-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="41fd7-115">Header</span></span> | <span data-ttu-id="41fd7-116">Wxlist. h (include Streams. h)</span><span class="sxs-lookup"><span data-stu-id="41fd7-116">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="41fd7-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="41fd7-117">Library</span></span>| <span data-ttu-id="41fd7-118">Strmbase. lib (compilazioni finali); Strmbasd. lib (build di debug)</span><span class="sxs-lookup"><span data-stu-id="41fd7-118">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="41fd7-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="41fd7-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41fd7-120">**Classe CGenericList**</span><span class="sxs-lookup"><span data-stu-id="41fd7-120">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




