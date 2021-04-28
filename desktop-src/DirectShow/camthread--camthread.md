---
description: Distruttore CAMThread.~CAMThread - Metodo distruttore.
ms.assetid: eed6c566-8a03-4a97-9d99-8e500ce2954c
title: Distruttore CAMThread.~CAMThread (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.~CAMThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 84a40205fc93677f20256676ad09a18357d46acb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096439"
---
# <a name="camthreadcamthread-destructor"></a><span data-ttu-id="60c48-103">Distruttore CAMThread.~CAMThread</span><span class="sxs-lookup"><span data-stu-id="60c48-103">CAMThread.~CAMThread destructor</span></span>

<span data-ttu-id="60c48-104">Metodo del distruttore.</span><span class="sxs-lookup"><span data-stu-id="60c48-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="60c48-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="60c48-105">Syntax</span></span>


```C++
virtual ~CAMThread();
```



## <a name="remarks"></a><span data-ttu-id="60c48-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="60c48-106">Remarks</span></span>

<span data-ttu-id="60c48-107">Il distruttore chiama il [**metodo CAMThread::Close,**](camthread-close.md) che attende la chiusura del thread.</span><span class="sxs-lookup"><span data-stu-id="60c48-107">The destructor calls the [**CAMThread::Close**](camthread-close.md) method, which waits for the thread to exit.</span></span>

## <a name="requirements"></a><span data-ttu-id="60c48-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="60c48-108">Requirements</span></span>



| <span data-ttu-id="60c48-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="60c48-109">Requirement</span></span> | <span data-ttu-id="60c48-110">Valore</span><span class="sxs-lookup"><span data-stu-id="60c48-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60c48-111">Intestazione</span><span class="sxs-lookup"><span data-stu-id="60c48-111">Header</span></span><br/>  | <dl> <span data-ttu-id="60c48-112"><dt>Wxutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="60c48-112"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="60c48-113">Libreria</span><span class="sxs-lookup"><span data-stu-id="60c48-113">Library</span></span><br/> | <dl> <span data-ttu-id="60c48-114"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="60c48-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60c48-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="60c48-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60c48-116">**Classe CAMThread**</span><span class="sxs-lookup"><span data-stu-id="60c48-116">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




