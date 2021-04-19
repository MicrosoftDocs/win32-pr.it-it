---
description: Il metodo RemoveHeadI rimuove il primo elemento nell'elenco.
ms.assetid: 7e448e32-ea31-4015-9219-1f990bf8763d
title: Metodo CBaseList. RemoveHeadI (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.RemoveHeadI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2d9b99dbac1d99587145aa2eba293ffa7ace959c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330236"
---
# <a name="cbaselistremoveheadi-method"></a><span data-ttu-id="39d65-103">CBaseList. RemoveHeadI, metodo</span><span class="sxs-lookup"><span data-stu-id="39d65-103">CBaseList.RemoveHeadI method</span></span>

<span data-ttu-id="39d65-104">Il `RemoveHeadI` metodo rimuove il primo elemento nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="39d65-104">The `RemoveHeadI` method removes the first item in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="39d65-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="39d65-105">Syntax</span></span>


```C++
void* RemoveHeadI();
```



## <a name="parameters"></a><span data-ttu-id="39d65-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="39d65-106">Parameters</span></span>

<span data-ttu-id="39d65-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="39d65-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="39d65-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="39d65-108">Return value</span></span>

<span data-ttu-id="39d65-109">Restituisce un puntatore all'elemento o **null** se l'elenco è vuoto.</span><span class="sxs-lookup"><span data-stu-id="39d65-109">Returns a pointer to the item, or **NULL** if the list is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="39d65-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="39d65-110">Remarks</span></span>

<span data-ttu-id="39d65-111">Questo metodo elimina il nodo elenco, ma non l'elemento contenuto nel nodo.</span><span class="sxs-lookup"><span data-stu-id="39d65-111">This method deletes the list node, but not the item that the node contains.</span></span>

## <a name="requirements"></a><span data-ttu-id="39d65-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="39d65-112">Requirements</span></span>



| <span data-ttu-id="39d65-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="39d65-113">Requirement</span></span> | <span data-ttu-id="39d65-114">Valore</span><span class="sxs-lookup"><span data-stu-id="39d65-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39d65-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="39d65-115">Header</span></span><br/>  | <dl> <span data-ttu-id="39d65-116"><dt>Wxlist. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="39d65-116"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="39d65-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="39d65-117">Library</span></span><br/> | <dl> <span data-ttu-id="39d65-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="39d65-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39d65-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="39d65-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39d65-120">**Classe CBaseList**</span><span class="sxs-lookup"><span data-stu-id="39d65-120">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




