---
description: 'Costruttore CBasePin.CBasePin : metodo costruttore.'
ms.assetid: e8cb5f1d-171f-4bf8-8ab6-6e547c4678d2
title: Costruttore CBasePin.CBasePin (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CBasePin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f11dea6bd5bc3f766e5f93a04022dab5ba6e51a5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099429"
---
# <a name="cbasepincbasepin-constructor"></a><span data-ttu-id="cbb47-103">Costruttore CBasePin.CBasePin</span><span class="sxs-lookup"><span data-stu-id="cbb47-103">CBasePin.CBasePin constructor</span></span>

<span data-ttu-id="cbb47-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="cbb47-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbb47-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cbb47-105">Syntax</span></span>


```C++
CBasePin(
   TCHAR         *pObjectName,
   CBaseFilter   *pFilter,
   CCritSec      *pLock,
   HRESULT       *phr,
   LPCWSTR       pName,
   PIN_DIRECTION dir
);
```



## <a name="parameters"></a><span data-ttu-id="cbb47-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cbb47-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbb47-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="cbb47-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="cbb47-108">Stringa contenente il nome di debug per l'oggetto .</span><span class="sxs-lookup"><span data-stu-id="cbb47-108">String containing the debug name for the object.</span></span> <span data-ttu-id="cbb47-109">Per altre informazioni, vedere [**CBaseObject.**](cbaseobject.md)</span><span class="sxs-lookup"><span data-stu-id="cbb47-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="cbb47-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="cbb47-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="cbb47-111">Puntatore al filtro che ha creato questo segnaposto.</span><span class="sxs-lookup"><span data-stu-id="cbb47-111">Pointer to the filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="cbb47-112">*Plock*</span><span class="sxs-lookup"><span data-stu-id="cbb47-112">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="cbb47-113">Puntatore a un [**blocco CCritSec,**](ccritsec.md) utilizzato per serializzare le modifiche dello stato.</span><span class="sxs-lookup"><span data-stu-id="cbb47-113">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span> <span data-ttu-id="cbb47-114">Può essere la stessa sezione critica del blocco del filtro, [**CBaseFilter::m \_ pLock**](cbasefilter-m-plock.md).</span><span class="sxs-lookup"><span data-stu-id="cbb47-114">Can be the same critical section as the filter lock, [**CBaseFilter::m\_pLock**](cbasefilter-m-plock.md).</span></span>

</dd> <dt>

<span data-ttu-id="cbb47-115">*Phr*</span><span class="sxs-lookup"><span data-stu-id="cbb47-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="cbb47-116">Puntatore a una variabile che riceve un **valore HRESULT** che indica l'esito positivo o negativo del metodo.</span><span class="sxs-lookup"><span data-stu-id="cbb47-116">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="cbb47-117">Inizializzare il valore su S \_ OK prima di creare l'oggetto .</span><span class="sxs-lookup"><span data-stu-id="cbb47-117">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="cbb47-118">Il valore viene modificato solo se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="cbb47-118">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="cbb47-119">*Pname*</span><span class="sxs-lookup"><span data-stu-id="cbb47-119">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="cbb47-120">Stringa di caratteri wide contenente il nome del segnaposto.</span><span class="sxs-lookup"><span data-stu-id="cbb47-120">Wide-character string containing the name of the pin.</span></span> <span data-ttu-id="cbb47-121">Per altre informazioni, vedere [**CBasePin::QueryPinInfo.**](cbasepin-querypininfo.md)</span><span class="sxs-lookup"><span data-stu-id="cbb47-121">For more information, see [**CBasePin::QueryPinInfo**](cbasepin-querypininfo.md).</span></span>

</dd> <dt>

<span data-ttu-id="cbb47-122">*dir*</span><span class="sxs-lookup"><span data-stu-id="cbb47-122">*dir*</span></span> 
</dt> <dd>

<span data-ttu-id="cbb47-123">Membro [**dell'enumerazione \_ DIRECTION del PIN**](/windows/win32/api/strmif/ne-strmif-pin_direction) che specifica la direzione del segnaposto.</span><span class="sxs-lookup"><span data-stu-id="cbb47-123">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumeration specifying the direction of the pin.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cbb47-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="cbb47-124">Remarks</span></span>

<span data-ttu-id="cbb47-125">La sezione critica specificata da *pLock* serializza lo stato del pin, inclusi lo stato della connessione, la scelta dell'allocatore, il tipo di supporto e lo stato delle operazioni di scaricamento.</span><span class="sxs-lookup"><span data-stu-id="cbb47-125">The critical section specified by *pLock* serializes the pin's state, including its connection status, choice of allocator, media type, and the status of flush operations.</span></span> <span data-ttu-id="cbb47-126">Non usare questa sezione critica per serializzare le operazioni di streaming.</span><span class="sxs-lookup"><span data-stu-id="cbb47-126">Do not use this critical section to serialize streaming operations.</span></span> <span data-ttu-id="cbb47-127">Per altre informazioni, vedere [Flusso di dati in Filter Graph](data-flow-in-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="cbb47-127">For more information, see [Data Flow in the Filter Graph](data-flow-in-the-filter-graph.md).</span></span>

<span data-ttu-id="cbb47-128">Un filtro potrebbe creare pin nel metodo del costruttore, pertanto a questo punto il puntatore *pFilter* potrebbe non fare riferimento a un oggetto valido.</span><span class="sxs-lookup"><span data-stu-id="cbb47-128">A filter might create pins in its constructor method, so at this point the *pFilter* pointer might not refer to a valid object.</span></span> <span data-ttu-id="cbb47-129">Archiviare il puntatore, ma non dereferenziarlo all'interno del costruttore del segnaposto.</span><span class="sxs-lookup"><span data-stu-id="cbb47-129">Store the pointer, but do not dereference it while inside the pin's constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbb47-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cbb47-130">Requirements</span></span>



| <span data-ttu-id="cbb47-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbb47-131">Requirement</span></span> | <span data-ttu-id="cbb47-132">Valore</span><span class="sxs-lookup"><span data-stu-id="cbb47-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbb47-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cbb47-133">Header</span></span><br/>  | <dl> <span data-ttu-id="cbb47-134"><dt>Amfilter.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="cbb47-134"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="cbb47-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="cbb47-135">Library</span></span><br/> | <dl> <span data-ttu-id="cbb47-136"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="cbb47-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbb47-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cbb47-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbb47-138">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="cbb47-138">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




