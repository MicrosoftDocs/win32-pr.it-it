---
description: Inserisce un elemento nella coda.
ms.assetid: 8ac41d80-e7d5-4b3f-9f09-c3d39c94c490
title: Metodo CQueue. PutQueueObject (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CQueue.PutQueueObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5371c843bb348f50539535a3df9a0f6aed00893e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331324"
---
# <a name="cqueueputqueueobject-method"></a><span data-ttu-id="3cbb4-103">CQueue. PutQueueObject, metodo</span><span class="sxs-lookup"><span data-stu-id="3cbb4-103">CQueue.PutQueueObject method</span></span>

<span data-ttu-id="3cbb4-104">Inserisce un elemento nella coda.</span><span class="sxs-lookup"><span data-stu-id="3cbb4-104">Puts an item onto the queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cbb4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3cbb4-105">Syntax</span></span>


```C++
void PutQueueObject(
   T object
);
```



## <a name="parameters"></a><span data-ttu-id="3cbb4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3cbb4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cbb4-107">*object*</span><span class="sxs-lookup"><span data-stu-id="3cbb4-107">*object*</span></span> 
</dt> <dd>

<span data-ttu-id="3cbb4-108">Oggetto di tipo **T** (il tipo di modello).</span><span class="sxs-lookup"><span data-stu-id="3cbb4-108">Object of type **T** (the template type).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cbb4-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3cbb4-109">Return value</span></span>

<span data-ttu-id="3cbb4-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="3cbb4-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3cbb4-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="3cbb4-111">Remarks</span></span>

<span data-ttu-id="3cbb4-112">Questo metodo si blocca fino a quando non è presente spazio nella coda per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="3cbb4-112">This method blocks until there is space in the queue for the item.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cbb4-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3cbb4-113">Requirements</span></span>



| <span data-ttu-id="3cbb4-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3cbb4-114">Requirement</span></span> | <span data-ttu-id="3cbb4-115">Valore</span><span class="sxs-lookup"><span data-stu-id="3cbb4-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cbb4-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3cbb4-116">Header</span></span><br/>  | <dl> <span data-ttu-id="3cbb4-117"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3cbb4-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="3cbb4-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="3cbb4-118">Library</span></span><br/> | <dl> <span data-ttu-id="3cbb4-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3cbb4-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cbb4-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3cbb4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cbb4-121">**Classe CQueue**</span><span class="sxs-lookup"><span data-stu-id="3cbb4-121">**CQueue Class**</span></span>](cqueue.md)
</dt> </dl>

 

 




