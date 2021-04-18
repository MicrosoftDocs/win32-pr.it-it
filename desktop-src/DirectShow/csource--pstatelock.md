---
description: Il metodo pStateLock recupera un puntatore all'oggetto sezione critica del filtro.
ms.assetid: 10a2e74b-a5aa-4d68-958e-d86f4b78037e
title: Metodo CSource. pStateLock (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.pStateLock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c0705584a513d64dfd1cd17075d95617234f7f8b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324659"
---
# <a name="csourcepstatelock-method"></a><span data-ttu-id="21694-103">CSource. pStateLock, metodo</span><span class="sxs-lookup"><span data-stu-id="21694-103">CSource.pStateLock method</span></span>

<span data-ttu-id="21694-104">Il metodo **pStateLock** recupera un puntatore all'oggetto sezione critica del filtro.</span><span class="sxs-lookup"><span data-stu-id="21694-104">The **pStateLock** method retrieves a pointer to the filter's critical section object.</span></span>

> [!Note]  
> <span data-ttu-id="21694-105">Anche se denominato come una variabile membro, **pStateLock** è un metodo.</span><span class="sxs-lookup"><span data-stu-id="21694-105">Although named like a member variable, **pStateLock** is a method.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="21694-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="21694-106">Syntax</span></span>


```C++
CCritSec* pStateLock();
```



## <a name="parameters"></a><span data-ttu-id="21694-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="21694-107">Parameters</span></span>

<span data-ttu-id="21694-108">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="21694-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="21694-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="21694-109">Return value</span></span>

<span data-ttu-id="21694-110">Restituisce un puntatore alla variabile membro [**CSource:: m \_ cStateLock**](csource-m-cstatelock.md) .</span><span class="sxs-lookup"><span data-stu-id="21694-110">Returns a pointer to the [**CSource::m\_cStateLock**](csource-m-cstatelock.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="21694-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="21694-111">Requirements</span></span>



| <span data-ttu-id="21694-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="21694-112">Requirement</span></span> | <span data-ttu-id="21694-113">Valore</span><span class="sxs-lookup"><span data-stu-id="21694-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21694-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="21694-114">Header</span></span><br/>  | <dl> <span data-ttu-id="21694-115"><dt>Source. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="21694-115"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="21694-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="21694-116">Library</span></span><br/> | <dl> <span data-ttu-id="21694-117"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="21694-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21694-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="21694-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21694-119">**Classe CSource**</span><span class="sxs-lookup"><span data-stu-id="21694-119">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




