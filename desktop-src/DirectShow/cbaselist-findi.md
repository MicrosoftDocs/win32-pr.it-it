---
description: Il metodo Findi recupera la prima posizione che contiene l'elemento specificato.
ms.assetid: a95fac19-0f93-4bb4-8e76-0da82745a1d2
title: Metodo CBaseList. Findi (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.FindI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2366f8c4c117b8550d91c84bffafb03393801088
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328668"
---
# <a name="cbaselistfindi-method"></a><span data-ttu-id="63f6b-103">Metodo CBaseList. Findi</span><span class="sxs-lookup"><span data-stu-id="63f6b-103">CBaseList.FindI method</span></span>

<span data-ttu-id="63f6b-104">Il `FindI` metodo recupera la prima posizione che include l'elemento specificato.</span><span class="sxs-lookup"><span data-stu-id="63f6b-104">The `FindI` method retrieves the first position that holds the specified item.</span></span>

## <a name="syntax"></a><span data-ttu-id="63f6b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="63f6b-105">Syntax</span></span>


```C++
POSITION FindI(
   void *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="63f6b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="63f6b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63f6b-107">*pObj*</span><span class="sxs-lookup"><span data-stu-id="63f6b-107">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="63f6b-108">Puntatore all'elemento.</span><span class="sxs-lookup"><span data-stu-id="63f6b-108">Pointer to the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63f6b-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="63f6b-109">Return value</span></span>

<span data-ttu-id="63f6b-110">Restituisce un valore di posizione oppure **null** se l'elemento non è presente nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="63f6b-110">Returns a POSITION value, or **NULL** if the item is not in the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="63f6b-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="63f6b-111">Requirements</span></span>



| <span data-ttu-id="63f6b-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="63f6b-112">Requirement</span></span> | <span data-ttu-id="63f6b-113">Valore</span><span class="sxs-lookup"><span data-stu-id="63f6b-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63f6b-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="63f6b-114">Header</span></span><br/>  | <dl> <span data-ttu-id="63f6b-115"><dt>Wxlist. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="63f6b-115"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="63f6b-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="63f6b-116">Library</span></span><br/> | <dl> <span data-ttu-id="63f6b-117"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="63f6b-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63f6b-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="63f6b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63f6b-119">**Classe CBaseList**</span><span class="sxs-lookup"><span data-stu-id="63f6b-119">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




