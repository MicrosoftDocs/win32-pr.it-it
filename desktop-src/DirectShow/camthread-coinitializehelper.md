---
description: Il metodo CoInitializeHelper chiama la funzione CoInitializeEx all'inizio del thread.
ms.assetid: 1a981e1e-c059-4e51-81d8-33bcb39ee580
title: Metodo CAMThread. CoInitializeHelper (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CoInitializeHelper
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6c3eb7fbcb9e4abada43098339a29d208ded0d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326943"
---
# <a name="camthreadcoinitializehelper-method"></a><span data-ttu-id="4c918-103">CAMThread. CoInitializeHelper, metodo</span><span class="sxs-lookup"><span data-stu-id="4c918-103">CAMThread.CoInitializeHelper method</span></span>

<span data-ttu-id="4c918-104">Il `CoInitializeHelper` metodo chiama la funzione CoInitializeEx all'inizio del thread.</span><span class="sxs-lookup"><span data-stu-id="4c918-104">The `CoInitializeHelper` method calls the CoInitializeEx function at the start of the thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c918-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4c918-105">Syntax</span></span>


```C++
static HRESULT CoInitializeHelper();
```



## <a name="parameters"></a><span data-ttu-id="4c918-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4c918-106">Parameters</span></span>

<span data-ttu-id="4c918-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="4c918-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4c918-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4c918-108">Return value</span></span>

<span data-ttu-id="4c918-109">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4c918-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="4c918-110">Di seguito sono riportati i valori possibili.</span><span class="sxs-lookup"><span data-stu-id="4c918-110">The following are possible values.</span></span>



| <span data-ttu-id="4c918-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="4c918-111">Return code</span></span>                                                                             | <span data-ttu-id="4c918-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4c918-112">Description</span></span>                                              |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="4c918-113"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="4c918-113"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="4c918-114">La funzione CoInitializeEx non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="4c918-114">The CoInitializeEx function is not available.</span></span><br/> |
| <dl> <span data-ttu-id="4c918-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4c918-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="4c918-116">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="4c918-116">Success.</span></span><br/>                                      |
| <dl> <span data-ttu-id="4c918-117"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="4c918-117"><dt>**E\_FAIL**</dt></span></span> </dl>  | <span data-ttu-id="4c918-118">Esito negativo.</span><span class="sxs-lookup"><span data-stu-id="4c918-118">Failure.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="4c918-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="4c918-119">Remarks</span></span>

<span data-ttu-id="4c918-120">Il metodo [**CAMThread:: InitialThreadProc**](camthread-initialthreadproc.md) chiama questo metodo helper, che chiama la funzione CoInitializeEx.</span><span class="sxs-lookup"><span data-stu-id="4c918-120">The [**CAMThread::InitialThreadProc**](camthread-initialthreadproc.md) method calls this helper method, which calls the CoInitializeEx function.</span></span> <span data-ttu-id="4c918-121">Usa il flag CoInit \_ Disable \_ OLE1DDE per disabilitare Dynamic Data Exchange (DDE).</span><span class="sxs-lookup"><span data-stu-id="4c918-121">It uses the COINIT\_DISABLE\_OLE1DDE flag, to disable Dynamic Data Exchange (DDE).</span></span> <span data-ttu-id="4c918-122">Per ulteriori informazioni, vedere Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="4c918-122">For more information, see the Platform SDK.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c918-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4c918-123">Requirements</span></span>



| <span data-ttu-id="4c918-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c918-124">Requirement</span></span> | <span data-ttu-id="4c918-125">Valore</span><span class="sxs-lookup"><span data-stu-id="4c918-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c918-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4c918-126">Header</span></span><br/>  | <dl> <span data-ttu-id="4c918-127"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4c918-127"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="4c918-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="4c918-128">Library</span></span><br/> | <dl> <span data-ttu-id="4c918-129"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4c918-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c918-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4c918-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c918-131">**Classe CAMThread**</span><span class="sxs-lookup"><span data-stu-id="4c918-131">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




