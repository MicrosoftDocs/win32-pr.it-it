---
description: 'Il metodo successivo recupera un numero specificato di pin nella sequenza di enumerazione. Questo metodo implementa il metodo IEnumPins:: Next.'
ms.assetid: c38fbd32-7d83-43ec-a105-4a7cb515b471
title: Metodo CEnumPins. Next (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.Next
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 612dcd638939b34803b7296babf7445a07cdad22
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329837"
---
# <a name="cenumpinsnext-method"></a><span data-ttu-id="71ea1-104">Metodo CEnumPins. Next</span><span class="sxs-lookup"><span data-stu-id="71ea1-104">CEnumPins.Next method</span></span>

<span data-ttu-id="71ea1-105">Il metodo successivo recupera un numero specificato di pin nella sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="71ea1-105">The Next method retrieves a specified number of pins in the enumeration sequence.</span></span> <span data-ttu-id="71ea1-106">Questo metodo implementa il metodo [**IEnumPins:: Next**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-next) .</span><span class="sxs-lookup"><span data-stu-id="71ea1-106">This method implements the [**IEnumPins::Next**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-next) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="71ea1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="71ea1-107">Syntax</span></span>


```C++
HRESULT Next(
   ULONG cPins,
   IPin  **ppPins,
   ULONG *pcFetched
);
```



## <a name="parameters"></a><span data-ttu-id="71ea1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="71ea1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71ea1-109">*cPins*</span><span class="sxs-lookup"><span data-stu-id="71ea1-109">*cPins*</span></span> 
</dt> <dd>

<span data-ttu-id="71ea1-110">Numero di pin da recuperare.</span><span class="sxs-lookup"><span data-stu-id="71ea1-110">Number of pins to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="71ea1-111">*ppPins*</span><span class="sxs-lookup"><span data-stu-id="71ea1-111">*ppPins*</span></span> 
</dt> <dd>

<span data-ttu-id="71ea1-112">Matrice di dimensioni *cPins* riempite con puntatori [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) .</span><span class="sxs-lookup"><span data-stu-id="71ea1-112">Array of size *cPins* that is filled with [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) pointers.</span></span>

</dd> <dt>

<span data-ttu-id="71ea1-113">*pcFetched*</span><span class="sxs-lookup"><span data-stu-id="71ea1-113">*pcFetched*</span></span> 
</dt> <dd>

<span data-ttu-id="71ea1-114">Puntatore a una variabile che riceve il numero di pin recuperati.</span><span class="sxs-lookup"><span data-stu-id="71ea1-114">Pointer to a variable that receives the number of pins retrieved.</span></span> <span data-ttu-id="71ea1-115">Può essere **null** se *cPins* è 1.</span><span class="sxs-lookup"><span data-stu-id="71ea1-115">Can be **NULL** if *cPins* is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71ea1-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="71ea1-116">Return value</span></span>

<span data-ttu-id="71ea1-117">Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="71ea1-117">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="71ea1-118">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="71ea1-118">Return code</span></span>                                                                                                | <span data-ttu-id="71ea1-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="71ea1-119">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="71ea1-120"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="71ea1-120"><dt>**S\_FALSE**</dt></span></span> </dl>                    | <span data-ttu-id="71ea1-121">Non è stato possibile recuperare tutti i pin richiesti.</span><span class="sxs-lookup"><span data-stu-id="71ea1-121">Did not retrieve as many pins as requested.</span></span><br/>                                 |
| <dl> <span data-ttu-id="71ea1-122"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="71ea1-122"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="71ea1-123">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="71ea1-123">Success.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="71ea1-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="71ea1-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>               | <span data-ttu-id="71ea1-125">Argomento non valido.</span><span class="sxs-lookup"><span data-stu-id="71ea1-125">Invalid argument.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="71ea1-126"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="71ea1-126"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="71ea1-127">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="71ea1-127">**NULL** pointer argument.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="71ea1-128"><dt>**non \_ \_ \_ \_ sincronizzato con VFW E enum \_**</dt></span><span class="sxs-lookup"><span data-stu-id="71ea1-128"><dt>**VFW\_E\_ENUM\_OUT\_OF\_SYNC**</dt></span></span> </dl> | <span data-ttu-id="71ea1-129">Lo stato del filtro è stato modificato ed è ora incoerente con l'enumeratore.</span><span class="sxs-lookup"><span data-stu-id="71ea1-129">The filter's state has changed and is now inconsistent with the enumerator.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="71ea1-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="71ea1-130">Remarks</span></span>

<span data-ttu-id="71ea1-131">Questo metodo recupera i puntatori al numero di PIN specificato, a partire dalla posizione corrente nell'enumerazione e li inserisce nella matrice specificata.</span><span class="sxs-lookup"><span data-stu-id="71ea1-131">This method retrieves pointers to the specified number of pins, starting at the current position in the enumeration, and places them in the specified array.</span></span>

<span data-ttu-id="71ea1-132">Questo metodo chiama il metodo [**CBaseFilter:: GetPin**](cbasefilter-getpin.md) del filtro per recuperare i pin.</span><span class="sxs-lookup"><span data-stu-id="71ea1-132">This method calls the filter's [**CBaseFilter::GetPin**](cbasefilter-getpin.md) method to retrieve the pins.</span></span>

<span data-ttu-id="71ea1-133">Se il metodo ha esito positivo, i puntatori **Ipin** hanno tutti i conteggi dei riferimenti in attesa.</span><span class="sxs-lookup"><span data-stu-id="71ea1-133">If the method succeeds, the **IPin** pointers all have outstanding reference counts.</span></span> <span data-ttu-id="71ea1-134">Assicurarsi di rilasciarli al termine dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="71ea1-134">Be sure to release them when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="71ea1-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="71ea1-135">Requirements</span></span>



| <span data-ttu-id="71ea1-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="71ea1-136">Requirement</span></span> | <span data-ttu-id="71ea1-137">Valore</span><span class="sxs-lookup"><span data-stu-id="71ea1-137">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71ea1-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="71ea1-138">Header</span></span><br/>  | <dl> <span data-ttu-id="71ea1-139"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="71ea1-139"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="71ea1-140">Libreria</span><span class="sxs-lookup"><span data-stu-id="71ea1-140">Library</span></span><br/> | <dl> <span data-ttu-id="71ea1-141"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="71ea1-141"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71ea1-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="71ea1-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71ea1-143">**Classe CEnumPins**</span><span class="sxs-lookup"><span data-stu-id="71ea1-143">**CEnumPins Class**</span></span>](cenumpins.md)
</dt> </dl>

 

 




