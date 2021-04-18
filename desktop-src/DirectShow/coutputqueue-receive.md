---
description: Il metodo Receive recapita un campione multimediale al pin di input.
ms.assetid: a8ee0988-8955-48d0-be1b-24eea72d560d
title: Metodo COutputQueue. Receive (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0ce8a0d44730fa35b38cf6d738edd26168284a46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324679"
---
# <a name="coutputqueuereceive-method"></a><span data-ttu-id="24c1c-103">Metodo COutputQueue. Receive</span><span class="sxs-lookup"><span data-stu-id="24c1c-103">COutputQueue.Receive method</span></span>

<span data-ttu-id="24c1c-104">Il `Receive` Metodo recapita un campione multimediale al pin di input.</span><span class="sxs-lookup"><span data-stu-id="24c1c-104">The `Receive` method delivers a media sample to the input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="24c1c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="24c1c-105">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="24c1c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="24c1c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24c1c-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="24c1c-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="24c1c-108">Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="24c1c-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24c1c-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="24c1c-109">Return value</span></span>

<span data-ttu-id="24c1c-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="24c1c-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="24c1c-111">I valori possibili includono quelli mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="24c1c-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="24c1c-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="24c1c-112">Return code</span></span>                                                                             | <span data-ttu-id="24c1c-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="24c1c-113">Description</span></span>                                                                   |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="24c1c-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="24c1c-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="24c1c-115">Notifica di fine del flusso ricevuta prima di elaborare l'esempio.</span><span class="sxs-lookup"><span data-stu-id="24c1c-115">End-of-stream notification received before processing this sample.</span></span><br/> |
| <dl> <span data-ttu-id="24c1c-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="24c1c-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="24c1c-117">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="24c1c-117">Success.</span></span><br/>                                                           |



 

## <a name="remarks"></a><span data-ttu-id="24c1c-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="24c1c-118">Remarks</span></span>

<span data-ttu-id="24c1c-119">Questo metodo chiama il metodo [**COutputQueue:: ReceiveMultiple**](coutputqueue-receivemultiple.md) .</span><span class="sxs-lookup"><span data-stu-id="24c1c-119">This method calls the [**COutputQueue::ReceiveMultiple**](coutputqueue-receivemultiple.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="24c1c-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="24c1c-120">Requirements</span></span>



| <span data-ttu-id="24c1c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="24c1c-121">Requirement</span></span> | <span data-ttu-id="24c1c-122">Valore</span><span class="sxs-lookup"><span data-stu-id="24c1c-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24c1c-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="24c1c-123">Header</span></span><br/>  | <dl> <span data-ttu-id="24c1c-124"><dt>Outputq. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="24c1c-124"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="24c1c-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="24c1c-125">Library</span></span><br/> | <dl> <span data-ttu-id="24c1c-126"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="24c1c-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24c1c-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="24c1c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24c1c-128">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="24c1c-128">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




