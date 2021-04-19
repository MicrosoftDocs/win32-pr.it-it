---
description: Il metodo PrepareReceive prepara il filtro per il rendering di un campione.
ms.assetid: 873b6b3b-623e-4cec-91ea-fa628618348d
title: Metodo CBaseRenderer. PrepareReceive (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.PrepareReceive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2b15f2a83d8cb20f7204e58dd12d5f94491904c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333342"
---
# <a name="cbaserendererpreparereceive-method"></a><span data-ttu-id="812c3-103">CBaseRenderer. PrepareReceive, metodo</span><span class="sxs-lookup"><span data-stu-id="812c3-103">CBaseRenderer.PrepareReceive method</span></span>

<span data-ttu-id="812c3-104">Il `PrepareReceive` metodo prepara il filtro per il rendering di un campione.</span><span class="sxs-lookup"><span data-stu-id="812c3-104">The `PrepareReceive` method prepares the filter to render a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="812c3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="812c3-105">Syntax</span></span>


```C++
virtual HRESULT PrepareReceive(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="812c3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="812c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="812c3-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="812c3-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="812c3-108">Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="812c3-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="812c3-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="812c3-109">Return value</span></span>

<span data-ttu-id="812c3-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="812c3-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="812c3-111">I valori possibili includono quelli nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="812c3-111">Possible values include those in the following table.</span></span>



| <span data-ttu-id="812c3-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="812c3-112">Return code</span></span>                                                                                             | <span data-ttu-id="812c3-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="812c3-113">Description</span></span>                                |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <span data-ttu-id="812c3-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="812c3-114"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="812c3-115">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="812c3-115">Success.</span></span><br/>                        |
| <dl> <span data-ttu-id="812c3-116"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="812c3-116"><dt>**E\_FAIL**</dt></span></span> </dl>                  | <span data-ttu-id="812c3-117">non riuscito.</span><span class="sxs-lookup"><span data-stu-id="812c3-117">Failed.</span></span><br/>                         |
| <dl> <span data-ttu-id="812c3-118"><dt>**E \_ imprevisto**</dt></span><span class="sxs-lookup"><span data-stu-id="812c3-118"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>            | <span data-ttu-id="812c3-119">Errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="812c3-119">Unexpected error.</span></span><br/>               |
| <dl> <span data-ttu-id="812c3-120"><dt>**esempio di VFW \_ E \_ \_ rifiutato**</dt></span><span class="sxs-lookup"><span data-stu-id="812c3-120"><dt>**VFW\_E\_SAMPLE\_REJECTED**</dt></span></span> </dl> | <span data-ttu-id="812c3-121">Il filtro sta eliminando l'esempio.</span><span class="sxs-lookup"><span data-stu-id="812c3-121">Filter is dropping this sample.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="812c3-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="812c3-122">Remarks</span></span>

<span data-ttu-id="812c3-123">Il filtro chiama questo metodo dall'interno del metodo [**CBaseRenderer:: Receive**](cbaserenderer-receive.md) , prima di eseguire il rendering di un campione.</span><span class="sxs-lookup"><span data-stu-id="812c3-123">The filter calls this method from inside the [**CBaseRenderer::Receive**](cbaserenderer-receive.md) method, before it renders a sample.</span></span> <span data-ttu-id="812c3-124">Se il filtro è in esecuzione, questo metodo pianifica l'esempio per il rendering.</span><span class="sxs-lookup"><span data-stu-id="812c3-124">If the filter is running, this method schedules the sample for rendering.</span></span>

<span data-ttu-id="812c3-125">Se il filtro dispone già di un campione in sospeso o se è già stata raggiunta la fine del flusso, il metodo restituisce E \_ imprevisto.</span><span class="sxs-lookup"><span data-stu-id="812c3-125">If the filter already has a pending sample, or if the end-of-stream was already reached, the method returns E\_UNEXPECTED.</span></span> <span data-ttu-id="812c3-126">Probabilmente il filtro upstream non sta serializzando correttamente le chiamate di streaming.</span><span class="sxs-lookup"><span data-stu-id="812c3-126">Possibly the upstream filter is not serializing its streaming calls correctly.</span></span>

<span data-ttu-id="812c3-127">Se l'algoritmo di pianificazione determina che l'esempio deve essere eliminato (vedere [**CBaseRenderer:: ScheduleSample**](cbaserenderer-schedulesample.md)), il metodo restituisce l' \_ esempio VFW E \_ \_ rifiutato.</span><span class="sxs-lookup"><span data-stu-id="812c3-127">If the scheduling algorithm determines that the sample should be dropped (see [**CBaseRenderer::ScheduleSample**](cbaserenderer-schedulesample.md)), the method returns VFW\_E\_SAMPLE\_REJECTED.</span></span> <span data-ttu-id="812c3-128">Tuttavia, il metodo [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) del PIN di input non passa questo codice di errore al filtro upstream, perché l'eliminazione di un campione non è un errore.</span><span class="sxs-lookup"><span data-stu-id="812c3-128">However, the input pin's [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method does not pass this error code to the upstream filter, because dropping a sample is not an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="812c3-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="812c3-129">Requirements</span></span>



| <span data-ttu-id="812c3-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="812c3-130">Requirement</span></span> | <span data-ttu-id="812c3-131">Valore</span><span class="sxs-lookup"><span data-stu-id="812c3-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="812c3-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="812c3-132">Header</span></span><br/>  | <dl> <span data-ttu-id="812c3-133"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="812c3-133"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="812c3-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="812c3-134">Library</span></span><br/> | <dl> <span data-ttu-id="812c3-135"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="812c3-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="812c3-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="812c3-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="812c3-137">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="812c3-137">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




