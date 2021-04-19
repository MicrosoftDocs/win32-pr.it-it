---
description: Il metodo GetDeliveryBuffer recupera un esempio di supporto che contiene un buffer vuoto.
ms.assetid: 5a20c11b-50f8-443e-a4d5-6bcffde741d5
title: Metodo CBaseOutputPin. GetDeliveryBuffer (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.GetDeliveryBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 332fad740c1ea904feee1a437273f21eb4c1def0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332061"
---
# <a name="cbaseoutputpingetdeliverybuffer-method"></a><span data-ttu-id="87e6f-103">CBaseOutputPin. GetDeliveryBuffer, metodo</span><span class="sxs-lookup"><span data-stu-id="87e6f-103">CBaseOutputPin.GetDeliveryBuffer method</span></span>

<span data-ttu-id="87e6f-104">Il `GetDeliveryBuffer` metodo recupera un esempio di supporto che contiene un buffer vuoto.</span><span class="sxs-lookup"><span data-stu-id="87e6f-104">The `GetDeliveryBuffer` method retrieves a media sample that contains an empty buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="87e6f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="87e6f-105">Syntax</span></span>


```C++
virtual HRESULT GetDeliveryBuffer(
   IMediaSample   **ppSample,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime,
   DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="87e6f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="87e6f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87e6f-107">*ppSample*</span><span class="sxs-lookup"><span data-stu-id="87e6f-107">*ppSample*</span></span> 
</dt> <dd>

<span data-ttu-id="87e6f-108">Indirizzo di una variabile che riceve un puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del buffer.</span><span class="sxs-lookup"><span data-stu-id="87e6f-108">Address of a variable that receives a pointer to the buffer's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> <dt>

<span data-ttu-id="87e6f-109">*pStartTime*</span><span class="sxs-lookup"><span data-stu-id="87e6f-109">*pStartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="87e6f-110">Puntatore all'ora di inizio dell'esempio, o **null**.</span><span class="sxs-lookup"><span data-stu-id="87e6f-110">Pointer to the start time of the sample, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="87e6f-111">*pEndTime*</span><span class="sxs-lookup"><span data-stu-id="87e6f-111">*pEndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="87e6f-112">Puntatore all'ora di fine dell'esempio, o **null**.</span><span class="sxs-lookup"><span data-stu-id="87e6f-112">Pointer to the ending time of the sample, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="87e6f-113">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="87e6f-113">*dwFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="87e6f-114">Combinazione bit per bit di flag supportati dall'interfaccia [**IMemAllocator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) .</span><span class="sxs-lookup"><span data-stu-id="87e6f-114">Bitwise combination of flags supported by the [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87e6f-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="87e6f-115">Return value</span></span>

<span data-ttu-id="87e6f-116">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="87e6f-116">Returns an **HRESULT** value.</span></span> <span data-ttu-id="87e6f-117">I valori possibili includono quelli elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="87e6f-117">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="87e6f-118">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="87e6f-118">Return code</span></span>                                                                                   | <span data-ttu-id="87e6f-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="87e6f-119">Description</span></span>                        |
|-----------------------------------------------------------------------------------------------|------------------------------------|
| <dl> <span data-ttu-id="87e6f-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="87e6f-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="87e6f-121">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="87e6f-121">Success.</span></span><br/>                |
| <dl> <span data-ttu-id="87e6f-122"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="87e6f-122"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="87e6f-123">Nessun allocatore disponibile.</span><span class="sxs-lookup"><span data-stu-id="87e6f-123">No allocator available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="87e6f-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="87e6f-124">Remarks</span></span>

<span data-ttu-id="87e6f-125">Questo metodo chiama il metodo **IMemAllocator:: GetBuffer** nell'allocatore e passa i parametri al metodo.</span><span class="sxs-lookup"><span data-stu-id="87e6f-125">This method calls the **IMemAllocator::GetBuffer** method on the allocator, and passes the parameters to that method.</span></span>

## <a name="requirements"></a><span data-ttu-id="87e6f-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="87e6f-126">Requirements</span></span>



| <span data-ttu-id="87e6f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="87e6f-127">Requirement</span></span> | <span data-ttu-id="87e6f-128">Valore</span><span class="sxs-lookup"><span data-stu-id="87e6f-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87e6f-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="87e6f-129">Header</span></span><br/>  | <dl> <span data-ttu-id="87e6f-130"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="87e6f-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="87e6f-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="87e6f-131">Library</span></span><br/> | <dl> <span data-ttu-id="87e6f-132"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="87e6f-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87e6f-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="87e6f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87e6f-134">**Classe CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="87e6f-134">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




