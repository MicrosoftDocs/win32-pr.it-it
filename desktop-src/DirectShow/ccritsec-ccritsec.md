---
description: Metodo del costruttore.
ms.assetid: e8e9138a-6c39-41de-a7f8-d9e9c4fe5ab6
title: Costruttore CCritSec. CCritSec (Wxutil. h)
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
ms.openlocfilehash: 6baeadace7c1f8d8d3ad5dee1ff5c9dace1c6907
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333733"
---
# <a name="ccritsecccritsec-constructor"></a><span data-ttu-id="39c56-103">Costruttore CCritSec. CCritSec</span><span class="sxs-lookup"><span data-stu-id="39c56-103">CCritSec.CCritSec constructor</span></span>

<span data-ttu-id="39c56-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="39c56-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="39c56-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="39c56-105">Syntax</span></span>


```C++
CCritSec();
```



## <a name="parameters"></a><span data-ttu-id="39c56-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="39c56-106">Parameters</span></span>

<span data-ttu-id="39c56-107">Questo costruttore non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="39c56-107">This constructor has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="39c56-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="39c56-108">Remarks</span></span>

<span data-ttu-id="39c56-109">Questo metodo chiama la funzione [**InitializeCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-initializecriticalsection) per inizializzare la sezione critica.</span><span class="sxs-lookup"><span data-stu-id="39c56-109">This method calls the [**InitializeCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-initializecriticalsection) function to initialize the critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="39c56-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="39c56-110">Requirements</span></span>



| <span data-ttu-id="39c56-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="39c56-111">Requirement</span></span> | <span data-ttu-id="39c56-112">Valore</span><span class="sxs-lookup"><span data-stu-id="39c56-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39c56-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="39c56-113">Header</span></span><br/>  | <dl> <span data-ttu-id="39c56-114"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="39c56-114"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="39c56-115">Libreria</span><span class="sxs-lookup"><span data-stu-id="39c56-115">Library</span></span><br/> | <dl> <span data-ttu-id="39c56-116"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="39c56-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39c56-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="39c56-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39c56-118">**Classe CCritSec**</span><span class="sxs-lookup"><span data-stu-id="39c56-118">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

