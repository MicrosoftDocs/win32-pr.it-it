---
description: 'Distruttore CCritSec.~CCritSec: metodo del distruttore.'
ms.assetid: cade850c-391c-41dc-adfe-56de8b2bbfff
title: Distruttore CCritSec.~CCritSec (Wxutil.h)
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
ms.openlocfilehash: 6f282bfe6ea6bca8cb8553572c18cfbc85db6c77
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095809"
---
# <a name="ccritsecccritsec-destructor"></a><span data-ttu-id="38882-103">Distruttore CCritSec.~CCritSec</span><span class="sxs-lookup"><span data-stu-id="38882-103">CCritSec.~CCritSec destructor</span></span>

<span data-ttu-id="38882-104">Metodo del distruttore.</span><span class="sxs-lookup"><span data-stu-id="38882-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="38882-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="38882-105">Syntax</span></span>


```C++
~CCritSec();
```



## <a name="remarks"></a><span data-ttu-id="38882-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="38882-106">Remarks</span></span>

<span data-ttu-id="38882-107">Questo metodo chiama la [**funzione DeleteCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-deletecriticalsection) per eliminare la sezione critica.</span><span class="sxs-lookup"><span data-stu-id="38882-107">This method calls the [**DeleteCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-deletecriticalsection) function to delete the critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="38882-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="38882-108">Requirements</span></span>



| <span data-ttu-id="38882-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="38882-109">Requirement</span></span> | <span data-ttu-id="38882-110">Valore</span><span class="sxs-lookup"><span data-stu-id="38882-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38882-111">Intestazione</span><span class="sxs-lookup"><span data-stu-id="38882-111">Header</span></span><br/>  | <dl> <span data-ttu-id="38882-112"><dt>Wxutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="38882-112"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="38882-113">Libreria</span><span class="sxs-lookup"><span data-stu-id="38882-113">Library</span></span><br/> | <dl> <span data-ttu-id="38882-114"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="38882-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38882-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="38882-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38882-116">**Classe CCritSec**</span><span class="sxs-lookup"><span data-stu-id="38882-116">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

