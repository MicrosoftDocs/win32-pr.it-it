---
description: Il metodo SendAnyway recapita tutti gli esempi in sospeso.
ms.assetid: b4e3a0c6-0f72-4a00-963e-65ceed265f01
title: Metodo COutputQueue. SendAnyway (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.SendAnyway
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6fa5495371e020310e2367aea7e7bed9ef113f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324671"
---
# <a name="coutputqueuesendanyway-method"></a><span data-ttu-id="b7bdd-103">COutputQueue. SendAnyway, metodo</span><span class="sxs-lookup"><span data-stu-id="b7bdd-103">COutputQueue.SendAnyway method</span></span>

<span data-ttu-id="b7bdd-104">Il `SendAnyway` Metodo recapita tutti gli esempi in sospeso.</span><span class="sxs-lookup"><span data-stu-id="b7bdd-104">The `SendAnyway` method delivers any pending samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7bdd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b7bdd-105">Syntax</span></span>


```C++
void SendAnyway();
```



## <a name="parameters"></a><span data-ttu-id="b7bdd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b7bdd-106">Parameters</span></span>

<span data-ttu-id="b7bdd-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="b7bdd-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b7bdd-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b7bdd-108">Return value</span></span>

<span data-ttu-id="b7bdd-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="b7bdd-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7bdd-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="b7bdd-110">Remarks</span></span>

<span data-ttu-id="b7bdd-111">Se la variabile membro [**COutputQueue:: m \_ BBatchExact**](coutputqueue-m-bbatchexact.md) è **true**, l'oggetto riempie la matrice [**COutputQueue:: m \_ ppSamples**](coutputqueue-m-ppsamples.md) prima di recapitare un batch di campioni.</span><span class="sxs-lookup"><span data-stu-id="b7bdd-111">If the [**COutputQueue::m\_bBatchExact**](coutputqueue-m-bbatchexact.md) member variable is **TRUE**, the object fills the [**COutputQueue::m\_ppSamples**](coutputqueue-m-ppsamples.md) array before it delivers a batch of samples.</span></span> <span data-ttu-id="b7bdd-112">Chiamare questo metodo per recapitare un batch parziale.</span><span class="sxs-lookup"><span data-stu-id="b7bdd-112">Call this method to deliver a partial batch.</span></span> <span data-ttu-id="b7bdd-113">Ad esempio, il metodo [**COutputQueue:: EOS**](coutputqueue-eos.md) chiama `SendAnyway` per serializzare i messaggi di fine flusso.</span><span class="sxs-lookup"><span data-stu-id="b7bdd-113">For example, the [**COutputQueue::EOS**](coutputqueue-eos.md) method calls `SendAnyway` to serialize end-of-stream messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7bdd-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b7bdd-114">Requirements</span></span>



| <span data-ttu-id="b7bdd-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7bdd-115">Requirement</span></span> | <span data-ttu-id="b7bdd-116">Valore</span><span class="sxs-lookup"><span data-stu-id="b7bdd-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7bdd-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b7bdd-117">Header</span></span><br/>  | <dl> <span data-ttu-id="b7bdd-118"><dt>Outputq. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b7bdd-118"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b7bdd-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="b7bdd-119">Library</span></span><br/> | <dl> <span data-ttu-id="b7bdd-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b7bdd-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7bdd-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b7bdd-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7bdd-122">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="b7bdd-122">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




