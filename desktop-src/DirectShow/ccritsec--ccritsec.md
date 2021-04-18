---
description: Metodo del distruttore.
ms.assetid: cade850c-391c-41dc-adfe-56de8b2bbfff
title: Distruttore CCritSec. ~ CCritSec (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.~CCritSec
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21029e2d53fd03ded2be4faa98e8b3e27681600c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330858"
---
# <a name="ccritsecccritsec-destructor"></a><span data-ttu-id="73b6d-103">Distruttore CCritSec. ~ CCritSec</span><span class="sxs-lookup"><span data-stu-id="73b6d-103">CCritSec.~CCritSec destructor</span></span>

<span data-ttu-id="73b6d-104">Metodo del distruttore.</span><span class="sxs-lookup"><span data-stu-id="73b6d-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="73b6d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="73b6d-105">Syntax</span></span>


```C++
~CCritSec();
```



## <a name="remarks"></a><span data-ttu-id="73b6d-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="73b6d-106">Remarks</span></span>

<span data-ttu-id="73b6d-107">Questo metodo chiama la funzione [**DeleteCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-deletecriticalsection) per eliminare la sezione critica.</span><span class="sxs-lookup"><span data-stu-id="73b6d-107">This method calls the [**DeleteCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-deletecriticalsection) function to delete the critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="73b6d-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="73b6d-108">Requirements</span></span>



| <span data-ttu-id="73b6d-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="73b6d-109">Requirement</span></span> | <span data-ttu-id="73b6d-110">Valore</span><span class="sxs-lookup"><span data-stu-id="73b6d-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73b6d-111">Intestazione</span><span class="sxs-lookup"><span data-stu-id="73b6d-111">Header</span></span><br/>  | <dl> <span data-ttu-id="73b6d-112"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="73b6d-112"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="73b6d-113">Libreria</span><span class="sxs-lookup"><span data-stu-id="73b6d-113">Library</span></span><br/> | <dl> <span data-ttu-id="73b6d-114"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="73b6d-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73b6d-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="73b6d-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73b6d-116">**Classe CCritSec**</span><span class="sxs-lookup"><span data-stu-id="73b6d-116">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

