---
description: Il metodo FreeSamples libera tutti gli esempi in sospeso.
ms.assetid: 61b7fe6e-41cc-4d5e-b083-bbc400d04e39
title: Metodo COutputQueue. FreeSamples (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.FreeSamples
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 70d0680d2a1a3ac020be84f244e1cc02bb6efad0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330207"
---
# <a name="coutputqueuefreesamples-method"></a><span data-ttu-id="9aaf7-103">COutputQueue. FreeSamples, metodo</span><span class="sxs-lookup"><span data-stu-id="9aaf7-103">COutputQueue.FreeSamples method</span></span>

<span data-ttu-id="9aaf7-104">Il `FreeSamples` metodo libera tutti gli esempi in sospeso.</span><span class="sxs-lookup"><span data-stu-id="9aaf7-104">The `FreeSamples` method frees all pending samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="9aaf7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9aaf7-105">Syntax</span></span>


```C++
void FreeSamples();
```



## <a name="parameters"></a><span data-ttu-id="9aaf7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9aaf7-106">Parameters</span></span>

<span data-ttu-id="9aaf7-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="9aaf7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9aaf7-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9aaf7-108">Return value</span></span>

<span data-ttu-id="9aaf7-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="9aaf7-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9aaf7-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="9aaf7-110">Remarks</span></span>

<span data-ttu-id="9aaf7-111">Questo metodo rimuove tutti gli esempi in sospeso dalla coda e dalla matrice di esempio.</span><span class="sxs-lookup"><span data-stu-id="9aaf7-111">This method removes any pending samples from the queue and from the sample array.</span></span>

## <a name="requirements"></a><span data-ttu-id="9aaf7-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9aaf7-112">Requirements</span></span>



| <span data-ttu-id="9aaf7-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="9aaf7-113">Requirement</span></span> | <span data-ttu-id="9aaf7-114">Valore</span><span class="sxs-lookup"><span data-stu-id="9aaf7-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9aaf7-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9aaf7-115">Header</span></span><br/>  | <dl> <span data-ttu-id="9aaf7-116"><dt>Outputq. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9aaf7-116"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9aaf7-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="9aaf7-117">Library</span></span><br/> | <dl> <span data-ttu-id="9aaf7-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9aaf7-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9aaf7-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9aaf7-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9aaf7-120">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="9aaf7-120">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




