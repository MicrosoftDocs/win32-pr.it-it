---
description: Metodo del costruttore.
ms.assetid: 996adc69-8727-431e-a7f5-8fbcc0e305ae
title: Costruttore CDynamicOutputPin. CDynamicOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.CDynamicOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7f45a2fee25796f39c7d8b358b1ac83e4a5b1daa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333454"
---
# <a name="cdynamicoutputpincdynamicoutputpin-constructor"></a><span data-ttu-id="3330a-103">Costruttore CDynamicOutputPin. CDynamicOutputPin</span><span class="sxs-lookup"><span data-stu-id="3330a-103">CDynamicOutputPin.CDynamicOutputPin constructor</span></span>

<span data-ttu-id="3330a-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="3330a-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3330a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3330a-105">Syntax</span></span>


```C++
CDynamicOutputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="3330a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3330a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3330a-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="3330a-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="3330a-108">Puntatore a una stringa che contiene il nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3330a-108">Pointer to a string containing the name of the object.</span></span> <span data-ttu-id="3330a-109">Per ulteriori informazioni, vedere [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="3330a-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="3330a-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="3330a-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="3330a-111">Puntatore al filtro che ha creato questo pin.</span><span class="sxs-lookup"><span data-stu-id="3330a-111">Pointer to the filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="3330a-112">*pLock*</span><span class="sxs-lookup"><span data-stu-id="3330a-112">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="3330a-113">Puntatore a un blocco [**CCritSec**](ccritsec.md) , usato per serializzare le modifiche di stato.</span><span class="sxs-lookup"><span data-stu-id="3330a-113">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span> <span data-ttu-id="3330a-114">Usare la stessa sezione critica del blocco del filtro, [ **CBaseFilter:: m \_ pLock**](cbasefilter-m-plock.md)</span><span class="sxs-lookup"><span data-stu-id="3330a-114">Use the same critical section as the filter lock, [**CBaseFilter::m\_pLock**](cbasefilter-m-plock.md)</span></span>

</dd> <dt>

<span data-ttu-id="3330a-115">*PHR*</span><span class="sxs-lookup"><span data-stu-id="3330a-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="3330a-116">Puntatore a una variabile che riceve un valore **HRESULT** che indica l'esito positivo o negativo del metodo.</span><span class="sxs-lookup"><span data-stu-id="3330a-116">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="3330a-117">Inizializzare il valore su S \_ OK prima di creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3330a-117">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="3330a-118">Il valore viene modificato solo se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="3330a-118">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="3330a-119">*pName*</span><span class="sxs-lookup"><span data-stu-id="3330a-119">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="3330a-120">Puntatore a una stringa di caratteri wide contenente l'identificatore del PIN.</span><span class="sxs-lookup"><span data-stu-id="3330a-120">Pointer to a wide-character string containing the pin identifier.</span></span> <span data-ttu-id="3330a-121">Per ulteriori informazioni, vedere [**Ipin:: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid).</span><span class="sxs-lookup"><span data-stu-id="3330a-121">For more information, see [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3330a-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3330a-122">Requirements</span></span>



| <span data-ttu-id="3330a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="3330a-123">Requirement</span></span> | <span data-ttu-id="3330a-124">Valore</span><span class="sxs-lookup"><span data-stu-id="3330a-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3330a-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3330a-125">Header</span></span><br/>  | <dl> <span data-ttu-id="3330a-126"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3330a-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3330a-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="3330a-127">Library</span></span><br/> | <dl> <span data-ttu-id="3330a-128"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3330a-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3330a-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3330a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3330a-130">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="3330a-130">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




