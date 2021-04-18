---
description: Il metodo QueryId recupera un identificatore per il PIN.
ms.assetid: 6050292e-6203-4a79-87bf-47394624cb32
title: Metodo CSourceStream. QueryId (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 267748fe4ce1eeec4650544a2f72069df897a366
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330662"
---
# <a name="csourcestreamqueryid-method"></a><span data-ttu-id="ebe01-103">CSourceStream. QueryId, metodo</span><span class="sxs-lookup"><span data-stu-id="ebe01-103">CSourceStream.QueryId method</span></span>

<span data-ttu-id="ebe01-104">Il `QueryId` metodo recupera un identificatore per il PIN.</span><span class="sxs-lookup"><span data-stu-id="ebe01-104">The `QueryId` method retrieves an identifier for the pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebe01-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ebe01-105">Syntax</span></span>


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a><span data-ttu-id="ebe01-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ebe01-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebe01-107">*Id*</span><span class="sxs-lookup"><span data-stu-id="ebe01-107">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="ebe01-108">Puntatore a una variabile che riceve una stringa che contiene l'identificatore del PIN.</span><span class="sxs-lookup"><span data-stu-id="ebe01-108">Pointer to a variable that receives a string containing the pin identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebe01-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ebe01-109">Return value</span></span>

<span data-ttu-id="ebe01-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ebe01-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="ebe01-111">I valori possibili includono quelli mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="ebe01-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="ebe01-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ebe01-112">Return code</span></span>                                                                                       | <span data-ttu-id="ebe01-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ebe01-113">Description</span></span>                                 |
|---------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="ebe01-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ebe01-114"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="ebe01-115">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="ebe01-115">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="ebe01-116"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="ebe01-116"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>     | <span data-ttu-id="ebe01-117">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="ebe01-117">Insufficient memory.</span></span><br/>             |
| <dl> <span data-ttu-id="ebe01-118"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="ebe01-118"><dt>**E\_POINTER**</dt></span></span> </dl>         | <span data-ttu-id="ebe01-119">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="ebe01-119">**NULL** pointer argument.</span></span><br/>       |
| <dl> <span data-ttu-id="ebe01-120"><dt>**VFW \_ E \_ non \_ trovato**</dt></span><span class="sxs-lookup"><span data-stu-id="ebe01-120"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="ebe01-121">Il PIN non è stato trovato nel filtro.</span><span class="sxs-lookup"><span data-stu-id="ebe01-121">Pin was not found on the filter.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ebe01-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="ebe01-122">Remarks</span></span>

<span data-ttu-id="ebe01-123">Questo metodo implementa il metodo [**Ipin:: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) .</span><span class="sxs-lookup"><span data-stu-id="ebe01-123">This method implements the [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) method.</span></span> <span data-ttu-id="ebe01-124">Per costruire una stringa dell'identificatore, il pin chiama il metodo [**CSource:: FindPinNumber**](csource-findpinnumber.md) con se stesso come parametro.</span><span class="sxs-lookup"><span data-stu-id="ebe01-124">To construct an identifier string, the pin calls the [**CSource::FindPinNumber**](csource-findpinnumber.md) method with itself as the parameter.</span></span> <span data-ttu-id="ebe01-125">Il metodo **FindPinNumber** restituisce il numero del PIN, indicizzato da zero.</span><span class="sxs-lookup"><span data-stu-id="ebe01-125">The **FindPinNumber** method returns the pin number, indexed from zero.</span></span> <span data-ttu-id="ebe01-126">`QueryId` incrementa il valore restituito di uno e converte il risultato in una stringa.</span><span class="sxs-lookup"><span data-stu-id="ebe01-126">`QueryId` increments the return value by one and converts the result to a string.</span></span> <span data-ttu-id="ebe01-127">Ad esempio, il primo pin diventa "1"; il secondo pin diventa "2"; e così via.</span><span class="sxs-lookup"><span data-stu-id="ebe01-127">For example, the first pin becomes "1"; the second pin becomes "2"; and so forth.</span></span>

<span data-ttu-id="ebe01-128">Se questo metodo restituisce VFW \_ E \_ non \_ trovato, significa che la matrice di pin del filtro non è valida, presumibilmente causata da un bug nel filtro.</span><span class="sxs-lookup"><span data-stu-id="ebe01-128">If this method returns VFW\_E\_NOT\_FOUND, it indicates that the filter's array of pins is invalid, presumably caused by a bug in the filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebe01-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ebe01-129">Requirements</span></span>



| <span data-ttu-id="ebe01-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebe01-130">Requirement</span></span> | <span data-ttu-id="ebe01-131">Valore</span><span class="sxs-lookup"><span data-stu-id="ebe01-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebe01-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ebe01-132">Header</span></span><br/>  | <dl> <span data-ttu-id="ebe01-133"><dt>Source. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ebe01-133"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="ebe01-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="ebe01-134">Library</span></span><br/> | <dl> <span data-ttu-id="ebe01-135"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ebe01-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebe01-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ebe01-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebe01-137">**Classe CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="ebe01-137">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




