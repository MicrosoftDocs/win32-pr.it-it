---
description: 'Costruttore CCritSec.CCritSec : metodo costruttore.'
ms.assetid: e8e9138a-6c39-41de-a7f8-d9e9c4fe5ab6
title: Costruttore CCritSec.CCritSec (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.CCritSec
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: de2b852ffc9a12622a4560ae834a3347b1e07552
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119799"
---
# <a name="ccritsecccritsec-constructor"></a><span data-ttu-id="7f23f-103">Costruttore CCritSec.CCritSec</span><span class="sxs-lookup"><span data-stu-id="7f23f-103">CCritSec.CCritSec constructor</span></span>

<span data-ttu-id="7f23f-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="7f23f-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f23f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7f23f-105">Syntax</span></span>


```C++
CCritSec();
```



## <a name="parameters"></a><span data-ttu-id="7f23f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7f23f-106">Parameters</span></span>

<span data-ttu-id="7f23f-107">Questo costruttore non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="7f23f-107">This constructor has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f23f-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="7f23f-108">Remarks</span></span>

<span data-ttu-id="7f23f-109">Questo metodo chiama la [**funzione InitializeCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-initializecriticalsection) per inizializzare la sezione critica.</span><span class="sxs-lookup"><span data-stu-id="7f23f-109">This method calls the [**InitializeCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-initializecriticalsection) function to initialize the critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f23f-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7f23f-110">Requirements</span></span>



| <span data-ttu-id="7f23f-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f23f-111">Requirement</span></span> | <span data-ttu-id="7f23f-112">Valore</span><span class="sxs-lookup"><span data-stu-id="7f23f-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f23f-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7f23f-113">Header</span></span><br/>  | <dl> <span data-ttu-id="7f23f-114"><dt>Wxutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="7f23f-114"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="7f23f-115">Libreria</span><span class="sxs-lookup"><span data-stu-id="7f23f-115">Library</span></span><br/> | <dl> <span data-ttu-id="7f23f-116"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7f23f-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f23f-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7f23f-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f23f-118">**Classe CCritSec**</span><span class="sxs-lookup"><span data-stu-id="7f23f-118">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

