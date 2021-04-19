---
description: Il metodo GetNext recupera l'elemento in corrispondenza della posizione specificata e fa avanzare la posizione.
ms.assetid: d24d3388-1af9-4a62-bdb6-d3d3f5b0b97a
title: Metodo CGenericList. GetNext (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.GetNext
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9491e58d817ce2c9dc4fb59fafa9bf96812a013a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329800"
---
# <a name="cgenericlistgetnext-method"></a><span data-ttu-id="2fee4-103">Metodo CGenericList. GetNext</span><span class="sxs-lookup"><span data-stu-id="2fee4-103">CGenericList.GetNext method</span></span>

<span data-ttu-id="2fee4-104">Il `GetNext` metodo recupera l'elemento in corrispondenza della posizione specificata e fa avanzare la posizione.</span><span class="sxs-lookup"><span data-stu-id="2fee4-104">The `GetNext` method retrieves the item at the specified position, and advances the position.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fee4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2fee4-105">Syntax</span></span>


```C++
OBJECT* GetNext(
  [ref] POSITION &rp
);
```



## <a name="parameters"></a><span data-ttu-id="2fee4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2fee4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fee4-107">*componente* \[ di Ref\]</span><span class="sxs-lookup"><span data-stu-id="2fee4-107">*rp* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="2fee4-108">Riferimento a un valore di posizione.</span><span class="sxs-lookup"><span data-stu-id="2fee4-108">Reference to a POSITION value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fee4-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2fee4-109">Return value</span></span>

<span data-ttu-id="2fee4-110">Restituisce un puntatore a un oggetto di tipo **Object** (il tipo di modello).</span><span class="sxs-lookup"><span data-stu-id="2fee4-110">Returns a pointer to an object of type **OBJECT** (the template type).</span></span>

## <a name="remarks"></a><span data-ttu-id="2fee4-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="2fee4-111">Remarks</span></span>

<span data-ttu-id="2fee4-112">Questo metodo sposta l'indicatore di posizione nella posizione successiva.</span><span class="sxs-lookup"><span data-stu-id="2fee4-112">This method advances the position indicator to the next position.</span></span> <span data-ttu-id="2fee4-113">Se l'indicatore di posizione si sposta oltre la fine dell'elenco, il metodo lo imposta su **null**.</span><span class="sxs-lookup"><span data-stu-id="2fee4-113">If the position indicator moves past the end of the list, the method sets it to **NULL**.</span></span>

<span data-ttu-id="2fee4-114">Se *RP* è **null**, il metodo restituisce **null**.</span><span class="sxs-lookup"><span data-stu-id="2fee4-114">If *rp* is **NULL**, the method returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fee4-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2fee4-115">Requirements</span></span>



| <span data-ttu-id="2fee4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fee4-116">Requirement</span></span> | <span data-ttu-id="2fee4-117">Valore</span><span class="sxs-lookup"><span data-stu-id="2fee4-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fee4-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2fee4-118">Header</span></span><br/>  | <dl> <span data-ttu-id="2fee4-119"><dt>Wxlist. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2fee4-119"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="2fee4-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="2fee4-120">Library</span></span><br/> | <dl> <span data-ttu-id="2fee4-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2fee4-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fee4-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2fee4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fee4-123">**Classe CGenericList**</span><span class="sxs-lookup"><span data-stu-id="2fee4-123">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




