---
description: 'Il metodo EndOfStream notifica al pin che non sono previsti dati aggiuntivi. Questo metodo implementa il metodo IPin:: EndOfStream.'
ms.assetid: db9896eb-3db2-4d58-a787-4d80ce8f0d0e
title: Metodo CTransformInputPin. EndOfStream (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bc39770f081499be720c433301823cbc60f37d17
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328800"
---
# <a name="ctransforminputpinendofstream-method"></a><span data-ttu-id="66dc7-104">CTransformInputPin. EndOfStream, metodo</span><span class="sxs-lookup"><span data-stu-id="66dc7-104">CTransformInputPin.EndOfStream method</span></span>

<span data-ttu-id="66dc7-105">Il `EndOfStream` metodo notifica al pin che non sono previsti dati aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="66dc7-105">The `EndOfStream` method notifies the pin that no additional data is expected.</span></span> <span data-ttu-id="66dc7-106">Questo metodo implementa il metodo [**Ipin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) .</span><span class="sxs-lookup"><span data-stu-id="66dc7-106">This method implements the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="66dc7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="66dc7-107">Syntax</span></span>


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="66dc7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="66dc7-108">Parameters</span></span>

<span data-ttu-id="66dc7-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="66dc7-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="66dc7-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="66dc7-110">Return value</span></span>

<span data-ttu-id="66dc7-111">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="66dc7-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="66dc7-112">I valori possibili includono quelli mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="66dc7-112">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="66dc7-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="66dc7-113">Return code</span></span>                                                                                           | <span data-ttu-id="66dc7-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="66dc7-114">Description</span></span>                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="66dc7-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="66dc7-115"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="66dc7-116">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="66dc7-116">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="66dc7-117"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="66dc7-117"><dt>**S\_FALSE**</dt></span></span> </dl>               | <span data-ttu-id="66dc7-118">È in corso lo scaricamento del PIN.</span><span class="sxs-lookup"><span data-stu-id="66dc7-118">Pin is currently flushing.</span></span><br/>       |
| <dl> <span data-ttu-id="66dc7-119"><dt>**VFW \_ E \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="66dc7-119"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="66dc7-120">Il pin di output non è connesso.</span><span class="sxs-lookup"><span data-stu-id="66dc7-120">The output pin is not connected.</span></span><br/> |
| <dl> <span data-ttu-id="66dc7-121"><dt>**errore di runtime di VFW \_ E \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="66dc7-121"><dt>**VFW\_E\_RUNTIME\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="66dc7-122">Si è verificato un errore in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="66dc7-122">A run-time error occurred.</span></span><br/>       |
| <dl> <span data-ttu-id="66dc7-123"><dt>**\_ \_ stato non corretto di VFW E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="66dc7-123"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl>   | <span data-ttu-id="66dc7-124">Il PIN è stato arrestato.</span><span class="sxs-lookup"><span data-stu-id="66dc7-124">The pin is stopped.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="66dc7-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="66dc7-125">Remarks</span></span>

<span data-ttu-id="66dc7-126">Questo metodo chiama il metodo [**CTransformFilter:: EndOfStream**](ctransformfilter-endofstream.md) del filtro per fornire la notifica di fine flusso downstream.</span><span class="sxs-lookup"><span data-stu-id="66dc7-126">This method calls the filter's [**CTransformFilter::EndOfStream**](ctransformfilter-endofstream.md) method to deliver the end-of-stream notification downstream.</span></span>

## <a name="requirements"></a><span data-ttu-id="66dc7-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="66dc7-127">Requirements</span></span>



| <span data-ttu-id="66dc7-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="66dc7-128">Requirement</span></span> | <span data-ttu-id="66dc7-129">Valore</span><span class="sxs-lookup"><span data-stu-id="66dc7-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66dc7-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="66dc7-130">Header</span></span><br/>  | <dl> <span data-ttu-id="66dc7-131"><dt>Transfrm. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="66dc7-131"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="66dc7-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="66dc7-132">Library</span></span><br/> | <dl> <span data-ttu-id="66dc7-133"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="66dc7-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




