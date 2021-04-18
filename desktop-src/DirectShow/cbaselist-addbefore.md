---
description: Il metodo AddBefore inserisce un elenco prima della posizione specificata.
ms.assetid: a4c0dbec-64a0-445b-95e5-000603cc0264
title: Metodo CBaseList. AddBefore (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddBefore
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6a3c25b2dd545b3e6698404bf00f82d1086bfb81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328681"
---
# <a name="cbaselistaddbefore-method"></a><span data-ttu-id="86662-103">CBaseList. AddBefore, metodo</span><span class="sxs-lookup"><span data-stu-id="86662-103">CBaseList.AddBefore method</span></span>

<span data-ttu-id="86662-104">Il `AddBefore` metodo inserisce un elenco prima della posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="86662-104">The `AddBefore` method inserts a list before the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="86662-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="86662-105">Syntax</span></span>


```C++
BOOL AddBefore(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a><span data-ttu-id="86662-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="86662-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86662-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="86662-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="86662-108">Posizione prima della quale inserire l'elenco.</span><span class="sxs-lookup"><span data-stu-id="86662-108">Position before which to insert the list.</span></span>

</dd> <dt>

<span data-ttu-id="86662-109">*pList*</span><span class="sxs-lookup"><span data-stu-id="86662-109">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="86662-110">Puntatore all'elenco da inserire.</span><span class="sxs-lookup"><span data-stu-id="86662-110">Pointer to the list to insert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86662-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="86662-111">Return value</span></span>

<span data-ttu-id="86662-112">Restituisce **true** se l'operazione ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="86662-112">Returns **TRUE** if successful.</span></span> <span data-ttu-id="86662-113">In caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="86662-113">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="86662-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="86662-114">Remarks</span></span>

<span data-ttu-id="86662-115">Gli indicatori di posizione esistenti, incluso quello specificato nel parametro *pos* , rimangono validi.</span><span class="sxs-lookup"><span data-stu-id="86662-115">Existing position indicators, including the one specified in the *pos* parameter, remain valid.</span></span> <span data-ttu-id="86662-116">Se il metodo ha esito negativo, è possibile che alcuni elementi siano stati aggiunti.</span><span class="sxs-lookup"><span data-stu-id="86662-116">If the method fails, some of the items might have been added.</span></span>

## <a name="requirements"></a><span data-ttu-id="86662-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="86662-117">Requirements</span></span>



| <span data-ttu-id="86662-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="86662-118">Requirement</span></span> | <span data-ttu-id="86662-119">Valore</span><span class="sxs-lookup"><span data-stu-id="86662-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86662-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="86662-120">Header</span></span><br/>  | <dl> <span data-ttu-id="86662-121"><dt>Wxlist. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="86662-121"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="86662-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="86662-122">Library</span></span><br/> | <dl> <span data-ttu-id="86662-123"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="86662-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86662-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="86662-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86662-125">**Classe CBaseList**</span><span class="sxs-lookup"><span data-stu-id="86662-125">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




