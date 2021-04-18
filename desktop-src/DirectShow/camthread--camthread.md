---
description: Metodo del distruttore.
ms.assetid: eed6c566-8a03-4a97-9d99-8e500ce2954c
title: Distruttore CAMThread. ~ CAMThread (Wxutil. h)
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
ms.openlocfilehash: b0b0a4dde858811a75347105b9fccd2f499c4faa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329164"
---
# <a name="camthreadcamthread-destructor"></a><span data-ttu-id="24a13-103">Distruttore CAMThread. ~ CAMThread</span><span class="sxs-lookup"><span data-stu-id="24a13-103">CAMThread.~CAMThread destructor</span></span>

<span data-ttu-id="24a13-104">Metodo del distruttore.</span><span class="sxs-lookup"><span data-stu-id="24a13-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="24a13-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="24a13-105">Syntax</span></span>


```C++
virtual ~CAMThread();
```



## <a name="remarks"></a><span data-ttu-id="24a13-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="24a13-106">Remarks</span></span>

<span data-ttu-id="24a13-107">Il distruttore chiama il metodo [**CAMThread:: Close**](camthread-close.md) , che attende la chiusura del thread.</span><span class="sxs-lookup"><span data-stu-id="24a13-107">The destructor calls the [**CAMThread::Close**](camthread-close.md) method, which waits for the thread to exit.</span></span>

## <a name="requirements"></a><span data-ttu-id="24a13-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="24a13-108">Requirements</span></span>



| <span data-ttu-id="24a13-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="24a13-109">Requirement</span></span> | <span data-ttu-id="24a13-110">Valore</span><span class="sxs-lookup"><span data-stu-id="24a13-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24a13-111">Intestazione</span><span class="sxs-lookup"><span data-stu-id="24a13-111">Header</span></span><br/>  | <dl> <span data-ttu-id="24a13-112"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="24a13-112"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="24a13-113">Libreria</span><span class="sxs-lookup"><span data-stu-id="24a13-113">Library</span></span><br/> | <dl> <span data-ttu-id="24a13-114"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="24a13-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24a13-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="24a13-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24a13-116">**Classe CAMThread**</span><span class="sxs-lookup"><span data-stu-id="24a13-116">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




