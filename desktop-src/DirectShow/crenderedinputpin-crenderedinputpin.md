---
description: 'Costruttore CRenderedInputPin.CRenderedInputPin : metodo costruttore.'
ms.assetid: bf335750-b776-47bc-978d-e84e8b5259f7
title: Costruttore CRenderedInputPin.CRenderedInputPin (Amextra.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.CRenderedInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4bd8e864531604fb36c2abe0bcd57ac5b3a9c869
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085399"
---
# <a name="crenderedinputpincrenderedinputpin-constructor"></a><span data-ttu-id="ff7db-103">Costruttore CRenderedInputPin.CRenderedInputPin</span><span class="sxs-lookup"><span data-stu-id="ff7db-103">CRenderedInputPin.CRenderedInputPin constructor</span></span>

<span data-ttu-id="ff7db-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="ff7db-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff7db-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ff7db-105">Syntax</span></span>


```C++
CRenderedInputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="ff7db-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ff7db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff7db-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="ff7db-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="ff7db-108">Stringa contenente il nome di debug dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="ff7db-108">String containing the debug name of the object.</span></span> <span data-ttu-id="ff7db-109">Per altre informazioni, vedere [**Classe CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="ff7db-109">For more information, see [**CBaseObject Class**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="ff7db-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="ff7db-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="ff7db-111">Puntatore al filtro che ha creato questo segnaposto.</span><span class="sxs-lookup"><span data-stu-id="ff7db-111">Pointer to the filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="ff7db-112">*Plock*</span><span class="sxs-lookup"><span data-stu-id="ff7db-112">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="ff7db-113">Puntatore a un [**blocco CCritSec,**](ccritsec.md) utilizzato per serializzare le modifiche dello stato.</span><span class="sxs-lookup"><span data-stu-id="ff7db-113">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span> <span data-ttu-id="ff7db-114">Può trattarsi della stessa sezione critica del blocco del filtro, [**CBaseFilter::m \_ pLock**](cbasefilter-m-plock.md).</span><span class="sxs-lookup"><span data-stu-id="ff7db-114">This can be the same critical section as the filter lock, [**CBaseFilter::m\_pLock**](cbasefilter-m-plock.md).</span></span>

</dd> <dt>

<span data-ttu-id="ff7db-115">*Phr*</span><span class="sxs-lookup"><span data-stu-id="ff7db-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="ff7db-116">Puntatore a una variabile che riceve un **valore HRESULT** che indica l'esito positivo o negativo del metodo.</span><span class="sxs-lookup"><span data-stu-id="ff7db-116">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> <dt>

<span data-ttu-id="ff7db-117">*Pname*</span><span class="sxs-lookup"><span data-stu-id="ff7db-117">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="ff7db-118">Stringa di caratteri wide contenente il nome del pin (usato anche come identificatore pin).</span><span class="sxs-lookup"><span data-stu-id="ff7db-118">Wide-character string containing the pin name (also used as the pin identifier).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ff7db-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ff7db-119">Requirements</span></span>



| <span data-ttu-id="ff7db-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff7db-120">Requirement</span></span> | <span data-ttu-id="ff7db-121">Valore</span><span class="sxs-lookup"><span data-stu-id="ff7db-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff7db-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ff7db-122">Header</span></span><br/>  | <dl> <span data-ttu-id="ff7db-123"><dt>Amextra.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="ff7db-123"><dt>Amextra.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ff7db-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="ff7db-124">Library</span></span><br/> | <dl> <span data-ttu-id="ff7db-125"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ff7db-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff7db-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ff7db-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff7db-127">**Classe CRenderedInputPin**</span><span class="sxs-lookup"><span data-stu-id="ff7db-127">**CRenderedInputPin Class**</span></span>](crenderedinputpin.md)
</dt> </dl>

 

 




