---
description: 'Il metodo Receive riceve il campione multimediale successivo nel flusso. Questo metodo implementa il metodo IMemInputPin:: Receive.'
ms.assetid: 65e4f8f5-2aa2-435b-84b4-e65af3f51afc
title: Metodo CTransformInputPin. Receive (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 59b087c4b783305b831871a030d1006d576e7d57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333311"
---
# <a name="ctransforminputpinreceive-method"></a><span data-ttu-id="ae13d-104">Metodo CTransformInputPin. Receive</span><span class="sxs-lookup"><span data-stu-id="ae13d-104">CTransformInputPin.Receive method</span></span>

<span data-ttu-id="ae13d-105">Il `Receive` metodo riceve il campione multimediale successivo nel flusso.</span><span class="sxs-lookup"><span data-stu-id="ae13d-105">The `Receive` method receives the next media sample in the stream.</span></span> <span data-ttu-id="ae13d-106">Questo metodo implementa il metodo [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) .</span><span class="sxs-lookup"><span data-stu-id="ae13d-106">This method implements the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae13d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ae13d-107">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="ae13d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ae13d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae13d-109">*pSample*</span><span class="sxs-lookup"><span data-stu-id="ae13d-109">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="ae13d-110">Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="ae13d-110">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae13d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ae13d-111">Return value</span></span>

<span data-ttu-id="ae13d-112">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ae13d-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="ae13d-113">I valori possibili includono quelli mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="ae13d-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="ae13d-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ae13d-114">Return code</span></span>                                                                             | <span data-ttu-id="ae13d-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ae13d-115">Description</span></span>                                                |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="ae13d-116"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="ae13d-116"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="ae13d-117">Il PIN sta attualmente scaricando; esempio rifiutato.</span><span class="sxs-lookup"><span data-stu-id="ae13d-117">Pin is currently flushing; sample was rejected.</span></span><br/> |
| <dl> <span data-ttu-id="ae13d-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ae13d-118"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="ae13d-119">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="ae13d-119">Success.</span></span><br/>                                        |



 

## <a name="remarks"></a><span data-ttu-id="ae13d-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="ae13d-120">Remarks</span></span>

<span data-ttu-id="ae13d-121">Questo metodo chiama il metodo [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) del PIN, che controlla lo stato del flusso del PIN e controlla la presenza di modifiche al formato nel tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="ae13d-121">This method calls the pin's [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method, which checks the pin's streaming state and checks for format changes in the media type.</span></span> <span data-ttu-id="ae13d-122">Chiama quindi il metodo [**CTransformFilter:: Receive**](ctransformfilter-receive.md) del filtro, che elabora l'esempio e lo recapita a valle.</span><span class="sxs-lookup"><span data-stu-id="ae13d-122">Then it calls the filter's [**CTransformFilter::Receive**](ctransformfilter-receive.md) method, which processes the sample and delivers it downstream.</span></span>

<span data-ttu-id="ae13d-123">Se il filtro deve accedere all'esempio dopo la restituzione di questo metodo, deve conservare un conteggio dei riferimenti chiamando il metodo **IUnknown:: AddRef** nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="ae13d-123">If the filter needs to access the sample after this method returns, it should hold a reference count by calling the **IUnknown::AddRef** method on the sample.</span></span> <span data-ttu-id="ae13d-124">Alcuni filtri decodificatori, ad esempio, richiedono l'esempio corrente per decodificare l'esempio successivo.</span><span class="sxs-lookup"><span data-stu-id="ae13d-124">For example, some decoder filters need the current sample in order to decode the next sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae13d-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ae13d-125">Requirements</span></span>



| <span data-ttu-id="ae13d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae13d-126">Requirement</span></span> | <span data-ttu-id="ae13d-127">Valore</span><span class="sxs-lookup"><span data-stu-id="ae13d-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae13d-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ae13d-128">Header</span></span><br/>  | <dl> <span data-ttu-id="ae13d-129"><dt>Transfrm. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ae13d-129"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ae13d-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="ae13d-130">Library</span></span><br/> | <dl> <span data-ttu-id="ae13d-131"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ae13d-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




