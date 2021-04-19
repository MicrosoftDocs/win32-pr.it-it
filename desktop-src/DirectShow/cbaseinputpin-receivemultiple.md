---
description: 'Il metodo ReceiveMultiple riceve una matrice di esempi. Questo metodo implementa il metodo IMemInputPin:: ReceiveMultiple.'
ms.assetid: 21e757c7-f623-4ccb-8e37-512ee4dd7aa7
title: Metodo CBaseInputPin. ReceiveMultiple (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.ReceiveMultiple
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5725b7d8b70c8f7c61eb44231812997a903ba41a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333213"
---
# <a name="cbaseinputpinreceivemultiple-method"></a><span data-ttu-id="44eac-104">CBaseInputPin. ReceiveMultiple, metodo</span><span class="sxs-lookup"><span data-stu-id="44eac-104">CBaseInputPin.ReceiveMultiple method</span></span>

<span data-ttu-id="44eac-105">Il `ReceiveMultiple` metodo riceve una matrice di campioni.</span><span class="sxs-lookup"><span data-stu-id="44eac-105">The `ReceiveMultiple` method receives an array of samples.</span></span> <span data-ttu-id="44eac-106">Questo metodo implementa il metodo [**IMemInputPin:: ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) .</span><span class="sxs-lookup"><span data-stu-id="44eac-106">This method implements the [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="44eac-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="44eac-107">Syntax</span></span>


```C++
HRESULT ReceiveMultiple(
   IMediaSample **pSamples,
   long         nSamples,
   long         *nSamplesProcessed
);
```



## <a name="parameters"></a><span data-ttu-id="44eac-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="44eac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44eac-109">*pSamples*</span><span class="sxs-lookup"><span data-stu-id="44eac-109">*pSamples*</span></span> 
</dt> <dd>

<span data-ttu-id="44eac-110">Indirizzo di una matrice di puntatori [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) , di dimensioni *nSamples*.</span><span class="sxs-lookup"><span data-stu-id="44eac-110">Address of an array of [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) pointers, of size *nSamples*.</span></span>

</dd> <dt>

<span data-ttu-id="44eac-111">*nSamples*</span><span class="sxs-lookup"><span data-stu-id="44eac-111">*nSamples*</span></span> 
</dt> <dd>

<span data-ttu-id="44eac-112">Numero di campioni da elaborare.</span><span class="sxs-lookup"><span data-stu-id="44eac-112">Number of samples to process.</span></span>

</dd> <dt>

<span data-ttu-id="44eac-113">*nSamplesProcessed*</span><span class="sxs-lookup"><span data-stu-id="44eac-113">*nSamplesProcessed*</span></span> 
</dt> <dd>

<span data-ttu-id="44eac-114">Puntatore a una variabile che riceve il numero di campioni elaborati.</span><span class="sxs-lookup"><span data-stu-id="44eac-114">Pointer to a variable that receives the number of samples that were processed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44eac-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="44eac-115">Return value</span></span>

<span data-ttu-id="44eac-116">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="44eac-116">Returns an **HRESULT** value.</span></span> <span data-ttu-id="44eac-117">I valori possibili includono quelli elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="44eac-117">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="44eac-118">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="44eac-118">Return code</span></span>                                                                                             | <span data-ttu-id="44eac-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="44eac-119">Description</span></span>                                                |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="44eac-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="44eac-120"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="44eac-121">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="44eac-121">Success.</span></span><br/>                                        |
| <dl> <span data-ttu-id="44eac-122"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="44eac-122"><dt>**S\_FALSE**</dt></span></span> </dl>                 | <span data-ttu-id="44eac-123">Il PIN sta attualmente scaricando; esempio rifiutato.</span><span class="sxs-lookup"><span data-stu-id="44eac-123">Pin is currently flushing; sample was rejected.</span></span><br/> |
| <dl> <span data-ttu-id="44eac-124"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="44eac-124"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="44eac-125">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="44eac-125">**NULL** pointer argument.</span></span><br/>                      |
| <dl> <span data-ttu-id="44eac-126"><dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt></span><span class="sxs-lookup"><span data-stu-id="44eac-126"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="44eac-127">Tipo di supporto non valido.</span><span class="sxs-lookup"><span data-stu-id="44eac-127">Invalid media type.</span></span><br/>                             |
| <dl> <span data-ttu-id="44eac-128"><dt>**errore di runtime di VFW \_ E \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="44eac-128"><dt>**VFW\_E\_RUNTIME\_ERROR**</dt></span></span> </dl>   | <span data-ttu-id="44eac-129">Si è verificato un errore in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="44eac-129">A run-time error occurred.</span></span><br/>                      |
| <dl> <span data-ttu-id="44eac-130"><dt>**\_ \_ stato non corretto di VFW E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="44eac-130"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl>     | <span data-ttu-id="44eac-131">Il PIN è stato arrestato.</span><span class="sxs-lookup"><span data-stu-id="44eac-131">The pin is stopped.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="44eac-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="44eac-132">Remarks</span></span>

<span data-ttu-id="44eac-133">Questo metodo si comporta come il metodo [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) , ma riceve una matrice di esempi.</span><span class="sxs-lookup"><span data-stu-id="44eac-133">This method behaves like the [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method, but receives an array of samples.</span></span> <span data-ttu-id="44eac-134">Nella classe di base il metodo scorre la matrice e chiama **Receive** con ogni campione.</span><span class="sxs-lookup"><span data-stu-id="44eac-134">In the base class, the method loops through the array and calls **Receive** with each sample.</span></span> <span data-ttu-id="44eac-135">Eseguire l'override di questa funzione se il filtro è in grado di elaborare batch di campioni in modo più efficiente rispetto all'elaborazione uno alla volta.</span><span class="sxs-lookup"><span data-stu-id="44eac-135">Override this function if your filter can process batches of samples more efficiently than processing them one at a time.</span></span>

## <a name="requirements"></a><span data-ttu-id="44eac-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="44eac-136">Requirements</span></span>



| <span data-ttu-id="44eac-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="44eac-137">Requirement</span></span> | <span data-ttu-id="44eac-138">Valore</span><span class="sxs-lookup"><span data-stu-id="44eac-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44eac-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="44eac-139">Header</span></span><br/>  | <dl> <span data-ttu-id="44eac-140"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="44eac-140"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="44eac-141">Libreria</span><span class="sxs-lookup"><span data-stu-id="44eac-141">Library</span></span><br/> | <dl> <span data-ttu-id="44eac-142"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="44eac-142"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44eac-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="44eac-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44eac-144">**Classe CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="44eac-144">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




