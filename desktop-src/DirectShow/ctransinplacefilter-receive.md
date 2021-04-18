---
description: Il metodo Receive riceve un campione multimediale, lo elabora e lo recapita al filtro downstream.
ms.assetid: 87126353-b73a-45f5-a8e7-b719efdf9d76
title: Metodo CTransInPlaceFilter. Receive (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5e7a1f87617b59c31139cb3d857c83d4470fd709
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331118"
---
# <a name="ctransinplacefilterreceive-method"></a><span data-ttu-id="db78d-103">Metodo CTransInPlaceFilter. Receive</span><span class="sxs-lookup"><span data-stu-id="db78d-103">CTransInPlaceFilter.Receive method</span></span>

<span data-ttu-id="db78d-104">Il `Receive` metodo riceve un campione multimediale, lo elabora e lo recapita al filtro downstream.</span><span class="sxs-lookup"><span data-stu-id="db78d-104">The `Receive` method receives a media sample, processes it, and delivers it to the downstream filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="db78d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="db78d-105">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="db78d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="db78d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db78d-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="db78d-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="db78d-108">Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="db78d-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface on the sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db78d-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="db78d-109">Return value</span></span>

<span data-ttu-id="db78d-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="db78d-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="db78d-111">I valori possibili includono quelli mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="db78d-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="db78d-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="db78d-112">Return code</span></span>                                                                                  | <span data-ttu-id="db78d-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db78d-113">Description</span></span>                 |
|----------------------------------------------------------------------------------------------|-----------------------------|
| <dl> <span data-ttu-id="db78d-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="db78d-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="db78d-115">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="db78d-115">Success</span></span><br/>          |
| <dl> <span data-ttu-id="db78d-116"><dt>**E \_ imprevisto**</dt></span><span class="sxs-lookup"><span data-stu-id="db78d-116"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="db78d-117">Errore imprevisto</span><span class="sxs-lookup"><span data-stu-id="db78d-117">Unexpected error</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="db78d-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="db78d-118">Remarks</span></span>

<span data-ttu-id="db78d-119">Il pin di input del filtro chiama questo metodo quando riceve un campione.</span><span class="sxs-lookup"><span data-stu-id="db78d-119">The filter's input pin calls this method when it receives a sample.</span></span> <span data-ttu-id="db78d-120">Il filtro chiama il metodo [**Transform**](ctransinplacefilter-transform.md) , che deve essere implementato dalla classe derivata.</span><span class="sxs-lookup"><span data-stu-id="db78d-120">The filter calls the [**Transform**](ctransinplacefilter-transform.md) method, which the derived class must implement.</span></span> <span data-ttu-id="db78d-121">Il metodo **Transform** elabora i dati.</span><span class="sxs-lookup"><span data-stu-id="db78d-121">The **Transform** method processes the data.</span></span> <span data-ttu-id="db78d-122">Se il filtro usa un solo allocatore, passa *pSample* direttamente al metodo **Transform** .</span><span class="sxs-lookup"><span data-stu-id="db78d-122">If the filter is using only one allocator, it passes *pSample* directly to the **Transform** method.</span></span> <span data-ttu-id="db78d-123">In caso contrario, copia *pSample* e passa la copia.</span><span class="sxs-lookup"><span data-stu-id="db78d-123">Otherwise, it copies *pSample* and passes the copy.</span></span>

<span data-ttu-id="db78d-124">Se il metodo **Transform** restituisce \_ false, il `Receive` metodo elimina l'esempio.</span><span class="sxs-lookup"><span data-stu-id="db78d-124">If the **Transform** method returns S\_FALSE, the `Receive` method drops the sample.</span></span> <span data-ttu-id="db78d-125">Nel primo esempio eliminato, il filtro Invia un evento [**di \_ \_ modifica della qualità EC**](ec-quality-change.md) al gestore del grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="db78d-125">On the first dropped sample, the filter sends an [**EC\_QUALITY\_CHANGE**](ec-quality-change.md) event to the filter graph manager.</span></span> <span data-ttu-id="db78d-126">In caso contrario, se il metodo **Transform** restituisce S \_ OK, il filtro recapita l'esempio di output.</span><span class="sxs-lookup"><span data-stu-id="db78d-126">Otherwise, if the **Transform** method returns S\_OK, the filter delivers the output sample.</span></span> <span data-ttu-id="db78d-127">A tale scopo, viene chiamato il metodo [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) sul pin di input downstream.</span><span class="sxs-lookup"><span data-stu-id="db78d-127">To do so, it calls the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method on the downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="db78d-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="db78d-128">Requirements</span></span>



| <span data-ttu-id="db78d-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="db78d-129">Requirement</span></span> | <span data-ttu-id="db78d-130">Valore</span><span class="sxs-lookup"><span data-stu-id="db78d-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db78d-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="db78d-131">Header</span></span><br/>  | <dl> <span data-ttu-id="db78d-132"><dt>Transip. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="db78d-132"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="db78d-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="db78d-133">Library</span></span><br/> | <dl> <span data-ttu-id="db78d-134"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="db78d-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db78d-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="db78d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db78d-136">**Classe CTransInPlaceFilter**</span><span class="sxs-lookup"><span data-stu-id="db78d-136">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




