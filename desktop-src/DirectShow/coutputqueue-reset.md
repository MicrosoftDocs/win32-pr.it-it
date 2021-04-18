---
description: Il metodo Reset reimposta l'oggetto in modo che possa ricevere più dati.
ms.assetid: 7074ed71-1650-4b21-a9a2-ad74d0e3e882
title: Metodo COutputQueue. Reset (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.Reset
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d380ef738af3b684606e86a7c36dc04217c54b7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324675"
---
# <a name="coutputqueuereset-method"></a><span data-ttu-id="71522-103">Metodo COutputQueue. Reset</span><span class="sxs-lookup"><span data-stu-id="71522-103">COutputQueue.Reset method</span></span>

<span data-ttu-id="71522-104">Il `Reset` metodo reimposta l'oggetto in modo che possa ricevere più dati.</span><span class="sxs-lookup"><span data-stu-id="71522-104">The `Reset` method resets the object so that it can receive more data.</span></span>

## <a name="syntax"></a><span data-ttu-id="71522-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="71522-105">Syntax</span></span>


```C++
void Reset();
```



## <a name="parameters"></a><span data-ttu-id="71522-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="71522-106">Parameters</span></span>

<span data-ttu-id="71522-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="71522-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="71522-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="71522-108">Return value</span></span>

<span data-ttu-id="71522-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="71522-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="71522-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="71522-110">Remarks</span></span>

<span data-ttu-id="71522-111">Questo metodo reimposta la variabile membro [**COutputQueue:: m \_ HR**](coutputqueue-m-hr.md) su S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="71522-111">This method resets the [**COutputQueue::m\_hr**](coutputqueue-m-hr.md) member variable to S\_OK.</span></span> <span data-ttu-id="71522-112">L'oggetto può ricevere nuovamente i campionamenti multimediali; ad esempio, dopo un'operazione di scaricamento.</span><span class="sxs-lookup"><span data-stu-id="71522-112">The object can receive media samples again; for example, after a flush operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="71522-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="71522-113">Requirements</span></span>



| <span data-ttu-id="71522-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="71522-114">Requirement</span></span> | <span data-ttu-id="71522-115">Valore</span><span class="sxs-lookup"><span data-stu-id="71522-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71522-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="71522-116">Header</span></span><br/>  | <dl> <span data-ttu-id="71522-117"><dt>Outputq. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="71522-117"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="71522-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="71522-118">Library</span></span><br/> | <dl> <span data-ttu-id="71522-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="71522-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71522-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="71522-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71522-121">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="71522-121">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




