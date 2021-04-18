---
description: Il metodo RemoveTailI rimuove l'ultimo elemento dell'elenco.
ms.assetid: 3e9f88a5-a681-4494-8977-d9a6ec62a849
title: Metodo CBaseList. RemoveTailI (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.RemoveTailI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 17c4e151426b54667ea3b9e4cb88be9526e2054b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330699"
---
# <a name="cbaselistremovetaili-method"></a><span data-ttu-id="d88a8-103">CBaseList. RemoveTailI, metodo</span><span class="sxs-lookup"><span data-stu-id="d88a8-103">CBaseList.RemoveTailI method</span></span>

<span data-ttu-id="d88a8-104">Il `RemoveTailI` metodo rimuove l'ultimo elemento dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="d88a8-104">The `RemoveTailI` method removes the last item in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="d88a8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d88a8-105">Syntax</span></span>


```C++
void* RemoveTailI();
```



## <a name="parameters"></a><span data-ttu-id="d88a8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d88a8-106">Parameters</span></span>

<span data-ttu-id="d88a8-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="d88a8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d88a8-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d88a8-108">Return value</span></span>

<span data-ttu-id="d88a8-109">Restituisce un puntatore all'elemento o **null** se l'elenco è vuoto.</span><span class="sxs-lookup"><span data-stu-id="d88a8-109">Returns a pointer to the item, or **NULL** if the list is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="d88a8-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="d88a8-110">Remarks</span></span>

<span data-ttu-id="d88a8-111">Questo metodo elimina il nodo elenco, ma non l'elemento contenuto nel nodo.</span><span class="sxs-lookup"><span data-stu-id="d88a8-111">This method deletes the list node, but not the item that is contained in the node.</span></span>

## <a name="requirements"></a><span data-ttu-id="d88a8-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d88a8-112">Requirements</span></span>



| <span data-ttu-id="d88a8-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="d88a8-113">Requirement</span></span> | <span data-ttu-id="d88a8-114">Valore</span><span class="sxs-lookup"><span data-stu-id="d88a8-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d88a8-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d88a8-115">Header</span></span><br/>  | <dl> <span data-ttu-id="d88a8-116"><dt>Wxlist. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d88a8-116"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="d88a8-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="d88a8-117">Library</span></span><br/> | <dl> <span data-ttu-id="d88a8-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d88a8-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d88a8-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d88a8-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d88a8-120">**Classe CBaseList**</span><span class="sxs-lookup"><span data-stu-id="d88a8-120">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




