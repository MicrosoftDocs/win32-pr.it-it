---
description: Il metodo AddHead inserisce un altro elenco all'inizio dell'elenco.
ms.assetid: 10999d93-2eb0-481f-8909-6f1184137786
title: Metodo CBaseList. AddHead (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a262f2bcfb7c40671fd472ecd7d3f887b1db4224
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328675"
---
# <a name="cbaselistaddhead-method"></a><span data-ttu-id="1a3f4-103">CBaseList. AddHead, metodo</span><span class="sxs-lookup"><span data-stu-id="1a3f4-103">CBaseList.AddHead method</span></span>

<span data-ttu-id="1a3f4-104">Il `AddHead` metodo inserisce un altro elenco all'inizio dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="1a3f4-104">The `AddHead` method inserts another list at the front of this list.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a3f4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a3f4-105">Syntax</span></span>


```C++
BOOL AddHead(
   CBaseList *pList
);
```



## <a name="parameters"></a><span data-ttu-id="1a3f4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1a3f4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a3f4-107">*pList*</span><span class="sxs-lookup"><span data-stu-id="1a3f4-107">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="1a3f4-108">Puntatore all'elenco di elementi da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="1a3f4-108">Pointer to the list of items to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a3f4-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1a3f4-109">Return value</span></span>

<span data-ttu-id="1a3f4-110">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="1a3f4-110">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a3f4-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="1a3f4-111">Remarks</span></span>

<span data-ttu-id="1a3f4-112">Se il metodo ha esito negativo, è possibile che alcuni elementi siano stati aggiunti all'elenco.</span><span class="sxs-lookup"><span data-stu-id="1a3f4-112">If the method fails, some items might have been added to the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a3f4-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1a3f4-113">Requirements</span></span>



| <span data-ttu-id="1a3f4-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a3f4-114">Requirement</span></span> | <span data-ttu-id="1a3f4-115">Valore</span><span class="sxs-lookup"><span data-stu-id="1a3f4-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a3f4-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1a3f4-116">Header</span></span><br/>  | <dl> <span data-ttu-id="1a3f4-117"><dt>Wxlist. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1a3f4-117"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="1a3f4-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="1a3f4-118">Library</span></span><br/> | <dl> <span data-ttu-id="1a3f4-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1a3f4-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a3f4-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1a3f4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a3f4-121">**Classe CBaseList**</span><span class="sxs-lookup"><span data-stu-id="1a3f4-121">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




