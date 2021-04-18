---
description: Il metodo MoveToTail suddivide l'elenco e aggiunge la parte Head alla parte finale di un altro elenco.
ms.assetid: f5cefe7c-075c-433b-9ece-aa10217344fa
title: Metodo CBaseList. MoveToTail (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.MoveToTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1c28e1051c08884e70e56b25b0fb2707ccd55ed1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328649"
---
# <a name="cbaselistmovetotail-method"></a><span data-ttu-id="7ac8d-103">CBaseList. MoveToTail, metodo</span><span class="sxs-lookup"><span data-stu-id="7ac8d-103">CBaseList.MoveToTail method</span></span>

<span data-ttu-id="7ac8d-104">Il `MoveToTail` metodo suddivide l'elenco e aggiunge la parte Head alla parte finale di un altro elenco.</span><span class="sxs-lookup"><span data-stu-id="7ac8d-104">The `MoveToTail` method splits the list and appends the head portion to the tail of another list.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ac8d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7ac8d-105">Syntax</span></span>


```C++
BOOL MoveToTail(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a><span data-ttu-id="7ac8d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7ac8d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ac8d-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="7ac8d-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="7ac8d-108">Indicatore di posizione che contrassegna la suddivisione nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="7ac8d-108">Position indicator that marks the split in the list.</span></span>

</dd> <dt>

<span data-ttu-id="7ac8d-109">*pList*</span><span class="sxs-lookup"><span data-stu-id="7ac8d-109">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="7ac8d-110">Puntatore a un altro elenco.</span><span class="sxs-lookup"><span data-stu-id="7ac8d-110">Pointer to another list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ac8d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7ac8d-111">Return value</span></span>

<span data-ttu-id="7ac8d-112">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="7ac8d-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ac8d-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="7ac8d-113">Remarks</span></span>

<span data-ttu-id="7ac8d-114">Questo metodo suddivide l'elenco dopo la posizione specificata dal parametro *pos* .</span><span class="sxs-lookup"><span data-stu-id="7ac8d-114">This method splits the list after the position specified by the *pos* parameter.</span></span> <span data-ttu-id="7ac8d-115">La parte finale rimane nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="7ac8d-115">The tail portion remains in the list.</span></span> <span data-ttu-id="7ac8d-116">La parte Head viene aggiunta alla parte finale dell'altro elenco.</span><span class="sxs-lookup"><span data-stu-id="7ac8d-116">The head portion is appended to the tail of the other list.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ac8d-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7ac8d-117">Requirements</span></span>



| <span data-ttu-id="7ac8d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ac8d-118">Requirement</span></span> | <span data-ttu-id="7ac8d-119">Valore</span><span class="sxs-lookup"><span data-stu-id="7ac8d-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ac8d-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7ac8d-120">Header</span></span><br/>  | <dl> <span data-ttu-id="7ac8d-121"><dt>Wxlist. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7ac8d-121"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="7ac8d-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="7ac8d-122">Library</span></span><br/> | <dl> <span data-ttu-id="7ac8d-123"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7ac8d-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ac8d-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7ac8d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ac8d-125">**Classe CBaseList**</span><span class="sxs-lookup"><span data-stu-id="7ac8d-125">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




