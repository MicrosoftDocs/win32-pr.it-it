---
description: Recupera l'elemento successivo dalla coda.
ms.assetid: 406ae640-5903-427d-91f9-8b01beb1aaa7
title: Metodo CQueue. GetQueueObject (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CQueue.GetQueueObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c3ae68c0564c7f76f38e91b7d27c8c3deb5ef2b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331326"
---
# <a name="cqueuegetqueueobject-method"></a><span data-ttu-id="ebe3f-103">CQueue. GetQueueObject, metodo</span><span class="sxs-lookup"><span data-stu-id="ebe3f-103">CQueue.GetQueueObject method</span></span>

<span data-ttu-id="ebe3f-104">Recupera l'elemento successivo dalla coda.</span><span class="sxs-lookup"><span data-stu-id="ebe3f-104">Retrieves the next item from the queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebe3f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ebe3f-105">Syntax</span></span>


```C++
T GetQueueObject();
```



## <a name="parameters"></a><span data-ttu-id="ebe3f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ebe3f-106">Parameters</span></span>

<span data-ttu-id="ebe3f-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="ebe3f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ebe3f-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ebe3f-108">Return value</span></span>

<span data-ttu-id="ebe3f-109">Restituisce un oggetto di tipo **T** (il tipo di modello).</span><span class="sxs-lookup"><span data-stu-id="ebe3f-109">Returns an object of type **T** (the template type).</span></span>

## <a name="remarks"></a><span data-ttu-id="ebe3f-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="ebe3f-110">Remarks</span></span>

<span data-ttu-id="ebe3f-111">Questo metodo si blocca fino a quando un elemento non è disponibile nella coda.</span><span class="sxs-lookup"><span data-stu-id="ebe3f-111">This method blocks until an item is available on the queue.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebe3f-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ebe3f-112">Requirements</span></span>



| <span data-ttu-id="ebe3f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebe3f-113">Requirement</span></span> | <span data-ttu-id="ebe3f-114">Valore</span><span class="sxs-lookup"><span data-stu-id="ebe3f-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebe3f-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ebe3f-115">Header</span></span><br/>  | <dl> <span data-ttu-id="ebe3f-116"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ebe3f-116"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="ebe3f-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="ebe3f-117">Library</span></span><br/> | <dl> <span data-ttu-id="ebe3f-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ebe3f-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebe3f-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ebe3f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebe3f-120">**Classe CQueue**</span><span class="sxs-lookup"><span data-stu-id="ebe3f-120">**CQueue Class**</span></span>](cqueue.md)
</dt> </dl>

 

 




