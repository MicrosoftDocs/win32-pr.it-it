---
description: "Metodo CTransformInputPin.Receive: il metodo Receive riceve l'esempio multimediale successivo nel flusso. Questo metodo implementa il metodo IMemInputPin::Receive."
ms.assetid: 65e4f8f5-2aa2-435b-84b4-e65af3f51afc
title: Metodo CTransformInputPin.Receive (Transfrm.h)
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
ms.openlocfilehash: 2a6a3c5dd4c9f11d45e1b719498d515a536e5ef8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084969"
---
# <a name="ctransforminputpinreceive-method"></a><span data-ttu-id="c211f-104">Metodo CTransformInputPin.Receive</span><span class="sxs-lookup"><span data-stu-id="c211f-104">CTransformInputPin.Receive method</span></span>

<span data-ttu-id="c211f-105">Il `Receive` metodo riceve l'esempio multimediale successivo nel flusso.</span><span class="sxs-lookup"><span data-stu-id="c211f-105">The `Receive` method receives the next media sample in the stream.</span></span> <span data-ttu-id="c211f-106">Questo metodo implementa il [**metodo IMemInputPin::Receive.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)</span><span class="sxs-lookup"><span data-stu-id="c211f-106">This method implements the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c211f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c211f-107">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="c211f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c211f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c211f-109">*pSample*</span><span class="sxs-lookup"><span data-stu-id="c211f-109">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="c211f-110">Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="c211f-110">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c211f-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c211f-111">Return value</span></span>

<span data-ttu-id="c211f-112">Restituisce un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="c211f-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="c211f-113">I valori possibili includono quelli illustrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="c211f-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="c211f-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="c211f-114">Return code</span></span>                                                                             | <span data-ttu-id="c211f-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c211f-115">Description</span></span>                                                |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="c211f-116"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="c211f-116"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="c211f-117">Il pin è attualmente in fase di scaricamento; L'esempio è stato rifiutato.</span><span class="sxs-lookup"><span data-stu-id="c211f-117">Pin is currently flushing; sample was rejected.</span></span><br/> |
| <dl> <span data-ttu-id="c211f-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c211f-118"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="c211f-119">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="c211f-119">Success.</span></span><br/>                                        |



 

## <a name="remarks"></a><span data-ttu-id="c211f-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="c211f-120">Remarks</span></span>

<span data-ttu-id="c211f-121">Questo metodo chiama il metodo [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) del pin, che controlla lo stato di streaming del pin e verifica le modifiche al formato nel tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="c211f-121">This method calls the pin's [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method, which checks the pin's streaming state and checks for format changes in the media type.</span></span> <span data-ttu-id="c211f-122">Chiama quindi il metodo [**CTransformFilter::Receive**](ctransformfilter-receive.md) del filtro, che elabora l'esempio e lo recapita a valle.</span><span class="sxs-lookup"><span data-stu-id="c211f-122">Then it calls the filter's [**CTransformFilter::Receive**](ctransformfilter-receive.md) method, which processes the sample and delivers it downstream.</span></span>

<span data-ttu-id="c211f-123">Se il filtro deve accedere all'esempio dopo la fine del metodo, deve contenere un conteggio dei riferimenti chiamando il metodo **IUnknown::AddRef** sull'esempio.</span><span class="sxs-lookup"><span data-stu-id="c211f-123">If the filter needs to access the sample after this method returns, it should hold a reference count by calling the **IUnknown::AddRef** method on the sample.</span></span> <span data-ttu-id="c211f-124">Ad esempio, alcuni filtri del decodificatore necessitano del campione corrente per decodificare il campione successivo.</span><span class="sxs-lookup"><span data-stu-id="c211f-124">For example, some decoder filters need the current sample in order to decode the next sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="c211f-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c211f-125">Requirements</span></span>



| <span data-ttu-id="c211f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c211f-126">Requirement</span></span> | <span data-ttu-id="c211f-127">Valore</span><span class="sxs-lookup"><span data-stu-id="c211f-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c211f-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c211f-128">Header</span></span><br/>  | <dl> <span data-ttu-id="c211f-129"><dt>Transfrm.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="c211f-129"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c211f-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="c211f-130">Library</span></span><br/> | <dl> <span data-ttu-id="c211f-131"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c211f-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




