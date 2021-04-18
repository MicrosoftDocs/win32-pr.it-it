---
description: Il metodo FillBuffer compila un campione multimediale con i dati.
ms.assetid: dddad8c7-44f1-4ba3-8fb1-7e7e88e40941
title: Metodo CSourceStream. FillBuffer (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.FillBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3611ad8b590bb823abccdecf9d3d138c70441a07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326935"
---
# <a name="csourcestreamfillbuffer-method"></a><span data-ttu-id="3f016-103">CSourceStream. FillBuffer, metodo</span><span class="sxs-lookup"><span data-stu-id="3f016-103">CSourceStream.FillBuffer method</span></span>

<span data-ttu-id="3f016-104">Il `FillBuffer` metodo compila un campione multimediale con i dati.</span><span class="sxs-lookup"><span data-stu-id="3f016-104">The `FillBuffer` method fills a media sample with data.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f016-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3f016-105">Syntax</span></span>


```C++
virtual HRESULT FillBuffer(
   IMediaSample *pSample
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="3f016-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3f016-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f016-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="3f016-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="3f016-108">Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="3f016-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f016-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3f016-109">Return value</span></span>

<span data-ttu-id="3f016-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3f016-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="3f016-111">I valori possibili includono quelli mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="3f016-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="3f016-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="3f016-112">Return code</span></span>                                                                             | <span data-ttu-id="3f016-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3f016-113">Description</span></span>              |
|-----------------------------------------------------------------------------------------|--------------------------|
| <dl> <span data-ttu-id="3f016-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="3f016-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="3f016-115">Fine del flusso</span><span class="sxs-lookup"><span data-stu-id="3f016-115">End of stream</span></span><br/> |
| <dl> <span data-ttu-id="3f016-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3f016-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="3f016-117">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="3f016-117">Success</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="3f016-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="3f016-118">Remarks</span></span>

<span data-ttu-id="3f016-119">La classe derivata deve implementare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="3f016-119">The derived class must implement this method.</span></span>

<span data-ttu-id="3f016-120">Il campione multimediale assegnato a questo metodo non ha timestamp.</span><span class="sxs-lookup"><span data-stu-id="3f016-120">The media sample given to this method has no time stamps.</span></span> <span data-ttu-id="3f016-121">La classe derivata deve chiamare il metodo [**IMediaSample:: setime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) per impostare gli indicatori temporali.</span><span class="sxs-lookup"><span data-stu-id="3f016-121">The derived class should call the [**IMediaSample::SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) method to set the time stamps.</span></span> <span data-ttu-id="3f016-122">Se appropriato per il tipo di supporto, la classe derivata deve impostare anche i tempi dei supporti, chiamando il metodo [**IMediaSample:: SetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) .</span><span class="sxs-lookup"><span data-stu-id="3f016-122">If appropriate for the media type, the derived class should also set the media times, by calling the [**IMediaSample::SetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) method.</span></span> <span data-ttu-id="3f016-123">Per altre informazioni, vedere [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="3f016-123">For more information, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>

<span data-ttu-id="3f016-124">Restituisce \_ false alla fine del flusso.</span><span class="sxs-lookup"><span data-stu-id="3f016-124">Return S\_FALSE at the end of the stream.</span></span> <span data-ttu-id="3f016-125">In questo modo la classe **CSourceStream** Invia la notifica di fine flusso e interrompe il ciclo di elaborazione del buffer.</span><span class="sxs-lookup"><span data-stu-id="3f016-125">This causes the **CSourceStream** class to send the end-of-stream notification and halt the buffer processing loop.</span></span> <span data-ttu-id="3f016-126">Per ulteriori informazioni, vedere [**CSourceStream::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) .</span><span class="sxs-lookup"><span data-stu-id="3f016-126">See [**CSourceStream::DoBufferProcessingLoop**](csourcestream-dobufferprocessingloop.md) for more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f016-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3f016-127">Requirements</span></span>



| <span data-ttu-id="3f016-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f016-128">Requirement</span></span> | <span data-ttu-id="3f016-129">Valore</span><span class="sxs-lookup"><span data-stu-id="3f016-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f016-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3f016-130">Header</span></span><br/>  | <dl> <span data-ttu-id="3f016-131"><dt>Source. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3f016-131"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="3f016-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="3f016-132">Library</span></span><br/> | <dl> <span data-ttu-id="3f016-133"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3f016-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f016-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3f016-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f016-135">**Classe CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="3f016-135">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




