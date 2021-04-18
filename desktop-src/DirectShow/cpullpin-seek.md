---
description: Il metodo Seek imposta le posizioni di inizio e di fine del flusso.
ms.assetid: d84476f5-688c-429d-a51b-7020a6316e35
title: Metodo CPullPin. Seek (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Seek
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6f1a82ec549b5ceb888acc194a7abc2cd3eace47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331157"
---
# <a name="cpullpinseek-method"></a><span data-ttu-id="96ee7-103">Metodo CPullPin. Seek</span><span class="sxs-lookup"><span data-stu-id="96ee7-103">CPullPin.Seek method</span></span>

<span data-ttu-id="96ee7-104">Il `Seek` metodo imposta le posizioni di inizio e di fine del flusso.</span><span class="sxs-lookup"><span data-stu-id="96ee7-104">The `Seek` method sets the start and stop positions of the stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="96ee7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="96ee7-105">Syntax</span></span>


```C++
HRESULT Seek(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop
);
```



## <a name="parameters"></a><span data-ttu-id="96ee7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="96ee7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96ee7-107">*tStart*</span><span class="sxs-lookup"><span data-stu-id="96ee7-107">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="96ee7-108">Specifica la posizione iniziale, in byte, moltiplicata per 10 milioni.</span><span class="sxs-lookup"><span data-stu-id="96ee7-108">Specifies the start position, in bytes multiplied by 10,000,000.</span></span>

</dd> <dt>

<span data-ttu-id="96ee7-109">*tStop*</span><span class="sxs-lookup"><span data-stu-id="96ee7-109">*tStop*</span></span> 
</dt> <dd>

<span data-ttu-id="96ee7-110">Specifica la posizione di arresto, in byte moltiplicata per 10 milioni.</span><span class="sxs-lookup"><span data-stu-id="96ee7-110">Specifies the stop position, in bytes multiplied by 10,000,000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96ee7-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="96ee7-111">Return value</span></span>

<span data-ttu-id="96ee7-112">Restituisce \_ OK se il metodo ha esito positivo o un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="96ee7-112">Returns S\_OK if the method succeeds, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="96ee7-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="96ee7-113">Remarks</span></span>

<span data-ttu-id="96ee7-114">Se il thread di lavoro è in esecuzione, il metodo sospende il thread, svuota il grafo del filtro e riprende il thread.</span><span class="sxs-lookup"><span data-stu-id="96ee7-114">If the worker thread is running, the method pauses the thread, flushes the filter graph, and resumes the thread.</span></span> <span data-ttu-id="96ee7-115">Il thread inizia a estrarre i dati dalla nuova posizione iniziale.</span><span class="sxs-lookup"><span data-stu-id="96ee7-115">The thread begins pulling data from the new start position.</span></span> <span data-ttu-id="96ee7-116">In caso contrario, i nuovi valori di posizione diventano effettivi ogni volta che il thread viene avviato.</span><span class="sxs-lookup"><span data-stu-id="96ee7-116">Otherwise, the new position values become effective whenever the thread is started.</span></span>

<span data-ttu-id="96ee7-117">Le posizioni sono relative all'inizio dell'origine originale.</span><span class="sxs-lookup"><span data-stu-id="96ee7-117">Positions are relative to the start of the original source.</span></span> <span data-ttu-id="96ee7-118">Moltiplicare gli offset di byte desiderati in base alle unità costanti, definite nella libreria di classi di base come 10 milioni.</span><span class="sxs-lookup"><span data-stu-id="96ee7-118">Multiply the desired byte offsets by the constant UNITS, which is defined in the base class library as 10,000,000.</span></span>

<span data-ttu-id="96ee7-119">Quando il pin si connette per la prima volta, le posizioni di arresto e avvio vengono assegnate per impostazione predefinita all'inizio e alla fine del flusso.</span><span class="sxs-lookup"><span data-stu-id="96ee7-119">When the pin first connects, the stop and start positions default to the beginning and end of the stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="96ee7-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="96ee7-120">Requirements</span></span>



| <span data-ttu-id="96ee7-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="96ee7-121">Requirement</span></span> | <span data-ttu-id="96ee7-122">Valore</span><span class="sxs-lookup"><span data-stu-id="96ee7-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96ee7-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="96ee7-123">Header</span></span><br/>  | <dl> <span data-ttu-id="96ee7-124"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="96ee7-124"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="96ee7-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="96ee7-125">Library</span></span><br/> | <dl> <span data-ttu-id="96ee7-126"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="96ee7-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96ee7-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="96ee7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96ee7-128">**Classe CPullPin**</span><span class="sxs-lookup"><span data-stu-id="96ee7-128">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




