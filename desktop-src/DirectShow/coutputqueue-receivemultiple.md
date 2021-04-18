---
description: Il metodo ReceiveMultiple recapita un batch di esempi di supporti al pin di input.
ms.assetid: e9c7d6ed-fbf9-4c90-8e1e-3bad66cb5d4f
title: Metodo COutputQueue. ReceiveMultiple (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.ReceiveMultiple
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e17e0a8a4856b067907622ec3c8437f5e73a7e38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324678"
---
# <a name="coutputqueuereceivemultiple-method"></a><span data-ttu-id="2beec-103">COutputQueue. ReceiveMultiple, metodo</span><span class="sxs-lookup"><span data-stu-id="2beec-103">COutputQueue.ReceiveMultiple method</span></span>

<span data-ttu-id="2beec-104">Il `ReceiveMultiple` Metodo recapita un batch di campioni multimediali al pin di input.</span><span class="sxs-lookup"><span data-stu-id="2beec-104">The `ReceiveMultiple` method delivers a batch of media samples to the input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="2beec-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2beec-105">Syntax</span></span>


```C++
HRESULT ReceiveMultiple(
   IMediaSample **ppSamples,
   long         nSamples,
   long         *nSamplesProcessed
);
```



## <a name="parameters"></a><span data-ttu-id="2beec-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2beec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2beec-107">*ppSamples*</span><span class="sxs-lookup"><span data-stu-id="2beec-107">*ppSamples*</span></span> 
</dt> <dd>

<span data-ttu-id="2beec-108">Indirizzo di un puntatore a una matrice di campioni.</span><span class="sxs-lookup"><span data-stu-id="2beec-108">Address of a pointer to an array of samples.</span></span>

</dd> <dt>

<span data-ttu-id="2beec-109">*nSamples*</span><span class="sxs-lookup"><span data-stu-id="2beec-109">*nSamples*</span></span> 
</dt> <dd>

<span data-ttu-id="2beec-110">Numero di campioni nella matrice.</span><span class="sxs-lookup"><span data-stu-id="2beec-110">Number of samples in the array.</span></span>

</dd> <dt>

<span data-ttu-id="2beec-111">*nSamplesProcessed*</span><span class="sxs-lookup"><span data-stu-id="2beec-111">*nSamplesProcessed*</span></span> 
</dt> <dd>

<span data-ttu-id="2beec-112">Puntatore a una variabile che riceve il numero di campioni recapitati correttamente.</span><span class="sxs-lookup"><span data-stu-id="2beec-112">Pointer to a variable that receives the number of samples delivered successfully.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2beec-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2beec-113">Return value</span></span>

<span data-ttu-id="2beec-114">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2beec-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="2beec-115">I valori possibili includono quelli mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="2beec-115">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="2beec-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="2beec-116">Return code</span></span>                                                                             | <span data-ttu-id="2beec-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2beec-117">Description</span></span>                                                                   |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2beec-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="2beec-118"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="2beec-119">Notifica di fine del flusso ricevuta prima di elaborare l'esempio.</span><span class="sxs-lookup"><span data-stu-id="2beec-119">End-of-stream notification received before processing this sample.</span></span><br/> |
| <dl> <span data-ttu-id="2beec-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2beec-120"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="2beec-121">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="2beec-121">Success.</span></span><br/>                                                           |



 

## <a name="remarks"></a><span data-ttu-id="2beec-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="2beec-122">Remarks</span></span>

<span data-ttu-id="2beec-123">Se l'oggetto utilizza un thread, questo metodo Accoda tutti gli esempi passati nella matrice.</span><span class="sxs-lookup"><span data-stu-id="2beec-123">If the object is using a thread, this method queues all of the samples passed in the array.</span></span> <span data-ttu-id="2beec-124">In caso contrario, il metodo chiama il metodo [**IMemInputPin:: ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) sul pin di input.</span><span class="sxs-lookup"><span data-stu-id="2beec-124">Otherwise, the method calls the [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="2beec-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2beec-125">Requirements</span></span>



| <span data-ttu-id="2beec-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="2beec-126">Requirement</span></span> | <span data-ttu-id="2beec-127">Valore</span><span class="sxs-lookup"><span data-stu-id="2beec-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2beec-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2beec-128">Header</span></span><br/>  | <dl> <span data-ttu-id="2beec-129"><dt>Outputq. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2beec-129"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2beec-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="2beec-130">Library</span></span><br/> | <dl> <span data-ttu-id="2beec-131"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2beec-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2beec-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2beec-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2beec-133">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="2beec-133">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




