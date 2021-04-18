---
description: Il metodo IsValid determina se l'oggetto è attivo (in esecuzione o in pausa).
ms.assetid: 6531cf1f-e057-4094-9354-d5a32371c83c
title: Metodo CBaseMediaFilter. IsValid (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.IsActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6438850b90309b47fbe1fb76b1fd4f7baea8f48
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325377"
---
# <a name="cbasemediafilterisactive-method"></a><span data-ttu-id="d1b49-103">Metodo CBaseMediaFilter. IsValid</span><span class="sxs-lookup"><span data-stu-id="d1b49-103">CBaseMediaFilter.IsActive method</span></span>

<span data-ttu-id="d1b49-104">Il `IsActive` metodo determina se l'oggetto è attivo (in esecuzione o in pausa).</span><span class="sxs-lookup"><span data-stu-id="d1b49-104">The `IsActive` method determines whether the object is active (running or paused).</span></span>

## <a name="syntax"></a><span data-ttu-id="d1b49-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d1b49-105">Syntax</span></span>


```C++
BOOL IsActive();
```



## <a name="parameters"></a><span data-ttu-id="d1b49-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d1b49-106">Parameters</span></span>

<span data-ttu-id="d1b49-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="d1b49-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d1b49-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d1b49-108">Return value</span></span>

<span data-ttu-id="d1b49-109">Restituisce **true** se l'oggetto è in pausa o in esecuzione oppure **false** se è stato arrestato.</span><span class="sxs-lookup"><span data-stu-id="d1b49-109">Returns **TRUE** if the object is paused or running, or **FALSE** if it is stopped.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1b49-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d1b49-110">Requirements</span></span>



| <span data-ttu-id="d1b49-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1b49-111">Requirement</span></span> | <span data-ttu-id="d1b49-112">Valore</span><span class="sxs-lookup"><span data-stu-id="d1b49-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1b49-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d1b49-113">Header</span></span><br/>  | <dl> <span data-ttu-id="d1b49-114"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d1b49-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d1b49-115">Libreria</span><span class="sxs-lookup"><span data-stu-id="d1b49-115">Library</span></span><br/> | <dl> <span data-ttu-id="d1b49-116"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d1b49-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1b49-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d1b49-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1b49-118">**Classe CBaseMediaFilter**</span><span class="sxs-lookup"><span data-stu-id="d1b49-118">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




