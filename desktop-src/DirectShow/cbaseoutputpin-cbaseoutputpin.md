---
description: 'Costruttore CBaseOutputPin.CBaseOutputPin : metodo del costruttore.'
ms.assetid: 1105c951-a51d-49ab-a69d-f3d482d61233
title: Costruttore CBaseOutputPin.CBaseOutputPin (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.CBaseOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9901591be32d431ebe53a2098456446a0126d26b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099569"
---
# <a name="cbaseoutputpincbaseoutputpin-constructor"></a><span data-ttu-id="c43b0-103">Costruttore CBaseOutputPin.CBaseOutputPin</span><span class="sxs-lookup"><span data-stu-id="c43b0-103">CBaseOutputPin.CBaseOutputPin constructor</span></span>

<span data-ttu-id="c43b0-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="c43b0-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c43b0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c43b0-105">Syntax</span></span>


```C++
CBaseOutputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="c43b0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c43b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c43b0-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="c43b0-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="c43b0-108">Stringa contenente il nome di debug dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c43b0-108">String containing the debug name of the object.</span></span> <span data-ttu-id="c43b0-109">Per altre informazioni, vedere [**CBaseObject.**](cbaseobject.md)</span><span class="sxs-lookup"><span data-stu-id="c43b0-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="c43b0-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="c43b0-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="c43b0-111">Puntatore al filtro che ha creato questo segnaposto.</span><span class="sxs-lookup"><span data-stu-id="c43b0-111">Pointer to the filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="c43b0-112">*Plock*</span><span class="sxs-lookup"><span data-stu-id="c43b0-112">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="c43b0-113">Puntatore a un [**blocco CCritSec,**](ccritsec.md) utilizzato per serializzare le modifiche dello stato.</span><span class="sxs-lookup"><span data-stu-id="c43b0-113">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span> <span data-ttu-id="c43b0-114">Può trattarsi della stessa sezione critica del blocco del filtro, [**CBaseFilter::m \_ pLock**](cbasefilter-m-plock.md).</span><span class="sxs-lookup"><span data-stu-id="c43b0-114">This can be the same critical section as the filter lock, [**CBaseFilter::m\_pLock**](cbasefilter-m-plock.md).</span></span>

</dd> <dt>

<span data-ttu-id="c43b0-115">*Phr*</span><span class="sxs-lookup"><span data-stu-id="c43b0-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="c43b0-116">Puntatore a una variabile che riceve un **valore HRESULT** che indica l'esito positivo o negativo del metodo.</span><span class="sxs-lookup"><span data-stu-id="c43b0-116">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> <dt>

<span data-ttu-id="c43b0-117">*Pname*</span><span class="sxs-lookup"><span data-stu-id="c43b0-117">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="c43b0-118">Stringa di caratteri wide contenente il nome del segnaposto (usato anche come identificatore pin).</span><span class="sxs-lookup"><span data-stu-id="c43b0-118">Wide-character string containing the pin name (also used as the pin identifier).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c43b0-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="c43b0-119">Remarks</span></span>

<span data-ttu-id="c43b0-120">Tutti i parametri vengono passati direttamente al [**costruttore CBasePin.**](cbasepin.md)</span><span class="sxs-lookup"><span data-stu-id="c43b0-120">All of the parameters are passed directly to the [**CBasePin**](cbasepin.md) constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="c43b0-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c43b0-121">Requirements</span></span>



| <span data-ttu-id="c43b0-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c43b0-122">Requirement</span></span> | <span data-ttu-id="c43b0-123">Valore</span><span class="sxs-lookup"><span data-stu-id="c43b0-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c43b0-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c43b0-124">Header</span></span><br/>  | <dl> <span data-ttu-id="c43b0-125"><dt>Amfilter.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="c43b0-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c43b0-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="c43b0-126">Library</span></span><br/> | <dl> <span data-ttu-id="c43b0-127"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c43b0-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c43b0-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c43b0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c43b0-129">**Classe CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="c43b0-129">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




