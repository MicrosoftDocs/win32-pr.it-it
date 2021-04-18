---
description: Il metodo Create crea il thread.
ms.assetid: 453972eb-7cf6-43c6-820e-c1992675260e
title: Metodo CAMThread. Create (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.Create
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0316cf053326d23d45c0d82f3c410d68d68a92dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330548"
---
# <a name="camthreadcreate-method"></a><span data-ttu-id="34f4e-103">Metodo CAMThread. Create</span><span class="sxs-lookup"><span data-stu-id="34f4e-103">CAMThread.Create method</span></span>

<span data-ttu-id="34f4e-104">Il `Create` metodo crea il thread.</span><span class="sxs-lookup"><span data-stu-id="34f4e-104">The `Create` method creates the thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="34f4e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="34f4e-105">Syntax</span></span>


```C++
BOOL Create();
```



## <a name="parameters"></a><span data-ttu-id="34f4e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="34f4e-106">Parameters</span></span>

<span data-ttu-id="34f4e-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="34f4e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="34f4e-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="34f4e-108">Return value</span></span>

<span data-ttu-id="34f4e-109">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="34f4e-109">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="34f4e-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="34f4e-110">Remarks</span></span>

<span data-ttu-id="34f4e-111">Questo metodo crea il thread, usando il metodo [**CAMThread:: InitialThreadProc**](camthread-initialthreadproc.md) per la routine thread e `this` per l'argomento thread.</span><span class="sxs-lookup"><span data-stu-id="34f4e-111">This method creates the thread, using the [**CAMThread::InitialThreadProc**](camthread-initialthreadproc.md) method for the thread procedure and `this` for the thread argument.</span></span>

<span data-ttu-id="34f4e-112">Il metodo ha esito negativo se il thread esiste già.</span><span class="sxs-lookup"><span data-stu-id="34f4e-112">The method fails if the thread already exists.</span></span>

## <a name="requirements"></a><span data-ttu-id="34f4e-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="34f4e-113">Requirements</span></span>



| <span data-ttu-id="34f4e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="34f4e-114">Requirement</span></span> | <span data-ttu-id="34f4e-115">Valore</span><span class="sxs-lookup"><span data-stu-id="34f4e-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34f4e-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="34f4e-116">Header</span></span><br/>  | <dl> <span data-ttu-id="34f4e-117"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="34f4e-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="34f4e-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="34f4e-118">Library</span></span><br/> | <dl> <span data-ttu-id="34f4e-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="34f4e-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34f4e-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="34f4e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34f4e-121">**Classe CAMThread**</span><span class="sxs-lookup"><span data-stu-id="34f4e-121">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




