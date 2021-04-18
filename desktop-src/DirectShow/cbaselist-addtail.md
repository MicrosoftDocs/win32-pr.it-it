---
description: Il metodo AddTail aggiunge un altro elenco alla fine dell'elenco.
ms.assetid: 996523cd-d9ba-406a-afdf-494d328dc9dd
title: Metodo CBaseList. AddTail (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36d42f0b80703457032e5dde37f6d1549da089c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328672"
---
# <a name="cbaselistaddtail-method"></a><span data-ttu-id="ddc33-103">CBaseList. AddTail, metodo</span><span class="sxs-lookup"><span data-stu-id="ddc33-103">CBaseList.AddTail method</span></span>

<span data-ttu-id="ddc33-104">Il `AddTail` metodo aggiunge un altro elenco alla fine dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="ddc33-104">The `AddTail` method appends another list to the end of this list.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddc33-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ddc33-105">Syntax</span></span>


```C++
BOOL AddTail(
   CBaseList *pList
);
```



## <a name="parameters"></a><span data-ttu-id="ddc33-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ddc33-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddc33-107">*pList*</span><span class="sxs-lookup"><span data-stu-id="ddc33-107">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="ddc33-108">Puntatore all'elenco da accodare.</span><span class="sxs-lookup"><span data-stu-id="ddc33-108">Pointer to the list to append.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ddc33-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ddc33-109">Return value</span></span>

<span data-ttu-id="ddc33-110">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="ddc33-110">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ddc33-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="ddc33-111">Remarks</span></span>

<span data-ttu-id="ddc33-112">Se il metodo ha esito negativo, è possibile che alcuni elementi siano stati aggiunti all'elenco.</span><span class="sxs-lookup"><span data-stu-id="ddc33-112">If the method fails, some items may have been added to the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddc33-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ddc33-113">Requirements</span></span>



| <span data-ttu-id="ddc33-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ddc33-114">Requirement</span></span> | <span data-ttu-id="ddc33-115">Valore</span><span class="sxs-lookup"><span data-stu-id="ddc33-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddc33-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ddc33-116">Header</span></span><br/>  | <dl> <span data-ttu-id="ddc33-117"><dt>Wxlist. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ddc33-117"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="ddc33-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="ddc33-118">Library</span></span><br/> | <dl> <span data-ttu-id="ddc33-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ddc33-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddc33-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ddc33-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddc33-121">**Classe CBaseList**</span><span class="sxs-lookup"><span data-stu-id="ddc33-121">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




