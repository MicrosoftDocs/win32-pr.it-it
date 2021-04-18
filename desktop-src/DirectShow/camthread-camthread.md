---
description: Metodo del costruttore.
ms.assetid: 0057adfe-e397-476b-90f9-7edbf7377b65
title: Costruttore CAMThread. CAMThread (Wxutil. h)
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
ms.openlocfilehash: abaac0c3b0330cd41db7ecd21f894733de10a1b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331946"
---
# <a name="camthreadcamthread-constructor"></a><span data-ttu-id="51b8f-103">Costruttore CAMThread. CAMThread</span><span class="sxs-lookup"><span data-stu-id="51b8f-103">CAMThread.CAMThread constructor</span></span>

<span data-ttu-id="51b8f-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="51b8f-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="51b8f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="51b8f-105">Syntax</span></span>


```C++
CAMThread(
   HRESULT *phr = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="51b8f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="51b8f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51b8f-107">*PHR*</span><span class="sxs-lookup"><span data-stu-id="51b8f-107">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="51b8f-108">Puntatore a un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="51b8f-108">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="51b8f-109">Se il costruttore ha esito negativo, questo parametro riceve un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="51b8f-109">If the constructor fails, this parameter receives an error code.</span></span> <span data-ttu-id="51b8f-110">In tal caso, lo stato dell'oggetto non è valido.</span><span class="sxs-lookup"><span data-stu-id="51b8f-110">If this occurs, the object is not in a valid state.</span></span>

<span data-ttu-id="51b8f-111">Per la compatibilità con le versioni precedenti di strmbase. lib, il valore predefinito di questo parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="51b8f-111">For backward compatibility with earlier versions of strmbase.lib, this parameter defaults to **NULL**.</span></span> <span data-ttu-id="51b8f-112">Tuttavia, è preferibile passare un valore non **null** , in modo che il chiamante possa controllare lo stato dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="51b8f-112">However, passing a non-**NULL** value is preferred, so that the caller can check the status of the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="51b8f-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="51b8f-113">Remarks</span></span>

<span data-ttu-id="51b8f-114">Il metodo del costruttore non crea il thread.</span><span class="sxs-lookup"><span data-stu-id="51b8f-114">The constructor method does not create the thread.</span></span> <span data-ttu-id="51b8f-115">Per creare il thread, chiamare il metodo [**CAMThread:: create**](camthread-create.md) .</span><span class="sxs-lookup"><span data-stu-id="51b8f-115">To create the thread, call the [**CAMThread::Create**](camthread-create.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="51b8f-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="51b8f-116">Requirements</span></span>



| <span data-ttu-id="51b8f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="51b8f-117">Requirement</span></span> | <span data-ttu-id="51b8f-118">Valore</span><span class="sxs-lookup"><span data-stu-id="51b8f-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51b8f-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="51b8f-119">Header</span></span><br/>  | <dl> <span data-ttu-id="51b8f-120"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="51b8f-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="51b8f-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="51b8f-121">Library</span></span><br/> | <dl> <span data-ttu-id="51b8f-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="51b8f-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51b8f-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="51b8f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51b8f-124">**Classe CAMThread**</span><span class="sxs-lookup"><span data-stu-id="51b8f-124">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




