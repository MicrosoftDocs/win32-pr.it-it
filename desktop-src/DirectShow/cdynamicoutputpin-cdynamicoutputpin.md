---
description: 'Costruttore CDynamicOutputPin.CDynamicOutputPin : metodo del costruttore.'
ms.assetid: 996adc69-8727-431e-a7f5-8fbcc0e305ae
title: Costruttore CDynamicOutputPin.CDynamicOutputPin (Amfilter.h)
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
ms.openlocfilehash: 4fe6dad14399b5b124b0146ea8b7ca101c8fa817
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099309"
---
# <a name="cdynamicoutputpincdynamicoutputpin-constructor"></a><span data-ttu-id="1ec50-103">Costruttore CDynamicOutputPin.CDynamicOutputPin</span><span class="sxs-lookup"><span data-stu-id="1ec50-103">CDynamicOutputPin.CDynamicOutputPin constructor</span></span>

<span data-ttu-id="1ec50-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="1ec50-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ec50-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1ec50-105">Syntax</span></span>


```C++
CDynamicOutputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="1ec50-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1ec50-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ec50-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="1ec50-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="1ec50-108">Puntatore a una stringa contenente il nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="1ec50-108">Pointer to a string containing the name of the object.</span></span> <span data-ttu-id="1ec50-109">Per altre informazioni, vedere [**CBaseObject.**](cbaseobject.md)</span><span class="sxs-lookup"><span data-stu-id="1ec50-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ec50-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="1ec50-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="1ec50-111">Puntatore al filtro che ha creato questo segnaposto.</span><span class="sxs-lookup"><span data-stu-id="1ec50-111">Pointer to the filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="1ec50-112">*Plock*</span><span class="sxs-lookup"><span data-stu-id="1ec50-112">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="1ec50-113">Puntatore a un [**blocco CCritSec,**](ccritsec.md) utilizzato per serializzare le modifiche dello stato.</span><span class="sxs-lookup"><span data-stu-id="1ec50-113">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span> <span data-ttu-id="1ec50-114">Usare la stessa sezione critica del blocco del filtro, [ **CBaseFilter::m \_ pLock**](cbasefilter-m-plock.md)</span><span class="sxs-lookup"><span data-stu-id="1ec50-114">Use the same critical section as the filter lock, [**CBaseFilter::m\_pLock**](cbasefilter-m-plock.md)</span></span>

</dd> <dt>

<span data-ttu-id="1ec50-115">*Phr*</span><span class="sxs-lookup"><span data-stu-id="1ec50-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="1ec50-116">Puntatore a una variabile che riceve un **valore HRESULT** che indica l'esito positivo o negativo del metodo.</span><span class="sxs-lookup"><span data-stu-id="1ec50-116">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="1ec50-117">Inizializzare il valore su S \_ OK prima di creare l'oggetto .</span><span class="sxs-lookup"><span data-stu-id="1ec50-117">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="1ec50-118">Il valore viene modificato solo se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="1ec50-118">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="1ec50-119">*Pname*</span><span class="sxs-lookup"><span data-stu-id="1ec50-119">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="1ec50-120">Puntatore a una stringa di caratteri wide contenente l'identificatore pin.</span><span class="sxs-lookup"><span data-stu-id="1ec50-120">Pointer to a wide-character string containing the pin identifier.</span></span> <span data-ttu-id="1ec50-121">Per altre informazioni, vedere [**IPin::QueryId.**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid)</span><span class="sxs-lookup"><span data-stu-id="1ec50-121">For more information, see [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1ec50-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1ec50-122">Requirements</span></span>



| <span data-ttu-id="1ec50-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ec50-123">Requirement</span></span> | <span data-ttu-id="1ec50-124">Valore</span><span class="sxs-lookup"><span data-stu-id="1ec50-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ec50-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1ec50-125">Header</span></span><br/>  | <dl> <span data-ttu-id="1ec50-126"><dt>Amfilter.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="1ec50-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1ec50-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="1ec50-127">Library</span></span><br/> | <dl> <span data-ttu-id="1ec50-128"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1ec50-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ec50-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1ec50-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ec50-130">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="1ec50-130">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




