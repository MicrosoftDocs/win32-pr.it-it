---
description: 'Costruttore CAMThread.CAMThread : metodo costruttore.'
ms.assetid: 0057adfe-e397-476b-90f9-7edbf7377b65
title: Costruttore CAMThread.CAMThread (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CAMThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0c4b9c5f80e131ce089b6a2da924e9cca41a84f6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096409"
---
# <a name="camthreadcamthread-constructor"></a><span data-ttu-id="43a41-103">Costruttore CAMThread.CAMThread</span><span class="sxs-lookup"><span data-stu-id="43a41-103">CAMThread.CAMThread constructor</span></span>

<span data-ttu-id="43a41-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="43a41-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="43a41-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="43a41-105">Syntax</span></span>


```C++
CAMThread(
   HRESULT *phr = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="43a41-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="43a41-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43a41-107">*Phr*</span><span class="sxs-lookup"><span data-stu-id="43a41-107">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="43a41-108">Puntatore a un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="43a41-108">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="43a41-109">Se il costruttore ha esito negativo, questo parametro riceve un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="43a41-109">If the constructor fails, this parameter receives an error code.</span></span> <span data-ttu-id="43a41-110">In questo caso, l'oggetto non è in uno stato valido.</span><span class="sxs-lookup"><span data-stu-id="43a41-110">If this occurs, the object is not in a valid state.</span></span>

<span data-ttu-id="43a41-111">Per la compatibilità con le versioni precedenti di strmbase.lib, il valore predefinito di questo parametro è **NULL.**</span><span class="sxs-lookup"><span data-stu-id="43a41-111">For backward compatibility with earlier versions of strmbase.lib, this parameter defaults to **NULL**.</span></span> <span data-ttu-id="43a41-112">Tuttavia, è preferibile passare un valore non **NULL,** in modo che il chiamante possa controllare lo stato dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="43a41-112">However, passing a non-**NULL** value is preferred, so that the caller can check the status of the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="43a41-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="43a41-113">Remarks</span></span>

<span data-ttu-id="43a41-114">Il metodo del costruttore non crea il thread.</span><span class="sxs-lookup"><span data-stu-id="43a41-114">The constructor method does not create the thread.</span></span> <span data-ttu-id="43a41-115">Per creare il thread, chiamare il [**metodo CAMThread::Create.**](camthread-create.md)</span><span class="sxs-lookup"><span data-stu-id="43a41-115">To create the thread, call the [**CAMThread::Create**](camthread-create.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="43a41-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="43a41-116">Requirements</span></span>



| <span data-ttu-id="43a41-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="43a41-117">Requirement</span></span> | <span data-ttu-id="43a41-118">Valore</span><span class="sxs-lookup"><span data-stu-id="43a41-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43a41-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="43a41-119">Header</span></span><br/>  | <dl> <span data-ttu-id="43a41-120"><dt>Wxutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="43a41-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="43a41-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="43a41-121">Library</span></span><br/> | <dl> <span data-ttu-id="43a41-122"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="43a41-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43a41-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="43a41-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43a41-124">**Classe CAMThread**</span><span class="sxs-lookup"><span data-stu-id="43a41-124">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




