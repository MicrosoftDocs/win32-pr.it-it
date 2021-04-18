---
description: Sezione critica che blocca l'accesso al thread da parte di altri thread.
ms.assetid: 9bc360be-52d6-4db1-b384-8bc9e25c0914
title: 'Membro CAMThread:: m_AccessLock (Wxutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_AccessLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6edb4b58b630cfdcfd6eefc43b908cf6aeb0f084
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330703"
---
# <a name="camthreadm_accesslock-member"></a><span data-ttu-id="bb77a-103">Membro AccessLock di CAMThread:: m \_</span><span class="sxs-lookup"><span data-stu-id="bb77a-103">CAMThread::m\_AccessLock member</span></span>

<span data-ttu-id="bb77a-104">Sezione critica che blocca l'accesso al thread da parte di altri thread.</span><span class="sxs-lookup"><span data-stu-id="bb77a-104">Critical section that locks the thread from being accessed by other threads.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb77a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bb77a-105">Syntax</span></span>


```C++
CCritSec m_AccessLock;
```



## <a name="remarks"></a><span data-ttu-id="bb77a-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="bb77a-106">Remarks</span></span>

<span data-ttu-id="bb77a-107">I metodi [**CAMThread:: create**](camthread-create.md) e [**CAMThread:: CallWorker**](camthread-callworker.md) mantengono questo blocco per serializzare le operazioni sul thread.</span><span class="sxs-lookup"><span data-stu-id="bb77a-107">The [**CAMThread::Create**](camthread-create.md) and [**CAMThread::CallWorker**](camthread-callworker.md) methods hold this lock, to serialize operations on the thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb77a-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb77a-108">Requirements</span></span>



| <span data-ttu-id="bb77a-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb77a-109">Requirement</span></span> | <span data-ttu-id="bb77a-110">Valore</span><span class="sxs-lookup"><span data-stu-id="bb77a-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb77a-111">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bb77a-111">Header</span></span><br/>  | <dl> <span data-ttu-id="bb77a-112"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bb77a-112"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="bb77a-113">Libreria</span><span class="sxs-lookup"><span data-stu-id="bb77a-113">Library</span></span><br/> | <dl> <span data-ttu-id="bb77a-114"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="bb77a-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb77a-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bb77a-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb77a-116">**Classe CAMThread**</span><span class="sxs-lookup"><span data-stu-id="bb77a-116">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




