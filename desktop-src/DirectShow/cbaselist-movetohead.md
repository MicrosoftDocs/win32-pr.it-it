---
description: Il metodo MoveToHead suddivide l'elenco e inserisce la parte finale all'inizio di un altro elenco.
ms.assetid: 46e4f8fe-6707-44c6-9d49-0168b35d2364
title: Metodo CBaseList. MoveToHead (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.MoveToHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 80adec6c8e2f6d42b5cf2cabd3a83a4c3aededa3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328650"
---
# <a name="cbaselistmovetohead-method"></a><span data-ttu-id="548a4-103">CBaseList. MoveToHead, metodo</span><span class="sxs-lookup"><span data-stu-id="548a4-103">CBaseList.MoveToHead method</span></span>

<span data-ttu-id="548a4-104">Il `MoveToHead` metodo suddivide l'elenco e inserisce la parte finale all'inizio di un altro elenco.</span><span class="sxs-lookup"><span data-stu-id="548a4-104">The `MoveToHead` method splits the list and inserts the tail portion at the head of another list.</span></span>

## <a name="syntax"></a><span data-ttu-id="548a4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="548a4-105">Syntax</span></span>


```C++
BOOL MoveToHead(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a><span data-ttu-id="548a4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="548a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="548a4-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="548a4-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="548a4-108">Indicatore di posizione che contrassegna la suddivisione nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="548a4-108">Position indicator that marks the split in the list.</span></span>

</dd> <dt>

<span data-ttu-id="548a4-109">*pList*</span><span class="sxs-lookup"><span data-stu-id="548a4-109">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="548a4-110">Puntatore a un altro elenco.</span><span class="sxs-lookup"><span data-stu-id="548a4-110">Pointer to another list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="548a4-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="548a4-111">Return value</span></span>

<span data-ttu-id="548a4-112">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="548a4-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="548a4-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="548a4-113">Remarks</span></span>

<span data-ttu-id="548a4-114">Questo metodo suddivide l'elenco prima della posizione specificata dal parametro *pos* .</span><span class="sxs-lookup"><span data-stu-id="548a4-114">This method splits the list before the position specified by the *pos* parameter.</span></span> <span data-ttu-id="548a4-115">La parte Head rimane nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="548a4-115">The head portion remains in the list.</span></span> <span data-ttu-id="548a4-116">La parte finale viene inserita all'inizio dell'altro elenco.</span><span class="sxs-lookup"><span data-stu-id="548a4-116">The tail portion is inserted at the head of the other list.</span></span>

## <a name="requirements"></a><span data-ttu-id="548a4-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="548a4-117">Requirements</span></span>



| <span data-ttu-id="548a4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="548a4-118">Requirement</span></span> | <span data-ttu-id="548a4-119">Valore</span><span class="sxs-lookup"><span data-stu-id="548a4-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="548a4-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="548a4-120">Header</span></span><br/>  | <dl> <span data-ttu-id="548a4-121"><dt>Wxlist. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="548a4-121"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="548a4-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="548a4-122">Library</span></span><br/> | <dl> <span data-ttu-id="548a4-123"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="548a4-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="548a4-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="548a4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="548a4-125">**Classe CBaseList**</span><span class="sxs-lookup"><span data-stu-id="548a4-125">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




