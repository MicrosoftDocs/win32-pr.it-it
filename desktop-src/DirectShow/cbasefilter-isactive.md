---
description: Il metodo IsValid determina se il filtro è attualmente attivo (in esecuzione o in pausa).
ms.assetid: 3bbb50d5-6a07-4932-940c-4466b95e6412
title: Metodo CBaseFilter. IsValid (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.IsActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 63cf2cd78bb61562c9b4d6a09de3d88c88d4c643
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331541"
---
# <a name="cbasefilterisactive-method"></a><span data-ttu-id="b3206-103">Metodo CBaseFilter. IsValid</span><span class="sxs-lookup"><span data-stu-id="b3206-103">CBaseFilter.IsActive method</span></span>

<span data-ttu-id="b3206-104">Il `IsActive` metodo determina se il filtro è attualmente attivo (in esecuzione o in pausa).</span><span class="sxs-lookup"><span data-stu-id="b3206-104">The `IsActive` method determines whether the filter is currently active (running or paused).</span></span>

## <a name="syntax"></a><span data-ttu-id="b3206-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b3206-105">Syntax</span></span>


```C++
BOOL IsActive();
```



## <a name="parameters"></a><span data-ttu-id="b3206-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b3206-106">Parameters</span></span>

<span data-ttu-id="b3206-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="b3206-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b3206-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b3206-108">Return value</span></span>

<span data-ttu-id="b3206-109">Restituisce **true** se il filtro è in pausa o in esecuzione oppure **false** se è stato arrestato.</span><span class="sxs-lookup"><span data-stu-id="b3206-109">Returns **TRUE** if the filter is paused or running, or **FALSE** if it is stopped.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3206-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3206-110">Requirements</span></span>



| <span data-ttu-id="b3206-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3206-111">Requirement</span></span> | <span data-ttu-id="b3206-112">Valore</span><span class="sxs-lookup"><span data-stu-id="b3206-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3206-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b3206-113">Header</span></span><br/>  | <dl> <span data-ttu-id="b3206-114"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b3206-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b3206-115">Libreria</span><span class="sxs-lookup"><span data-stu-id="b3206-115">Library</span></span><br/> | <dl> <span data-ttu-id="b3206-116"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b3206-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3206-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b3206-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3206-118">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="b3206-118">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




