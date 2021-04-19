---
description: Metodo del costruttore.
ms.assetid: e8cb5f1d-171f-4bf8-8ab6-6e547c4678d2
title: Costruttore CBasePin. CBasePin (Amfilter. h)
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
ms.openlocfilehash: dd4883d3d8e906e1da2f377344b735037c5e5cd3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332771"
---
# <a name="cbasepincbasepin-constructor"></a><span data-ttu-id="0ca69-103">Costruttore CBasePin. CBasePin</span><span class="sxs-lookup"><span data-stu-id="0ca69-103">CBasePin.CBasePin constructor</span></span>

<span data-ttu-id="0ca69-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="0ca69-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ca69-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0ca69-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="0ca69-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0ca69-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ca69-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="0ca69-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="0ca69-108">Stringa contenente il nome di debug per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0ca69-108">String containing the debug name for the object.</span></span> <span data-ttu-id="0ca69-109">Per ulteriori informazioni, vedere [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="0ca69-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ca69-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="0ca69-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="0ca69-111">Puntatore al filtro che ha creato questo pin.</span><span class="sxs-lookup"><span data-stu-id="0ca69-111">Pointer to the filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="0ca69-112">*pLock*</span><span class="sxs-lookup"><span data-stu-id="0ca69-112">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="0ca69-113">Puntatore a un blocco [**CCritSec**](ccritsec.md) , usato per serializzare le modifiche di stato.</span><span class="sxs-lookup"><span data-stu-id="0ca69-113">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span> <span data-ttu-id="0ca69-114">Può essere la stessa sezione critica del blocco del filtro, [**CBaseFilter:: m \_ pLock**](cbasefilter-m-plock.md).</span><span class="sxs-lookup"><span data-stu-id="0ca69-114">Can be the same critical section as the filter lock, [**CBaseFilter::m\_pLock**](cbasefilter-m-plock.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ca69-115">*PHR*</span><span class="sxs-lookup"><span data-stu-id="0ca69-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="0ca69-116">Puntatore a una variabile che riceve un valore **HRESULT** che indica l'esito positivo o negativo del metodo.</span><span class="sxs-lookup"><span data-stu-id="0ca69-116">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="0ca69-117">Inizializzare il valore su S \_ OK prima di creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0ca69-117">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="0ca69-118">Il valore viene modificato solo se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="0ca69-118">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="0ca69-119">*pName*</span><span class="sxs-lookup"><span data-stu-id="0ca69-119">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="0ca69-120">Stringa di caratteri wide contenente il nome del PIN.</span><span class="sxs-lookup"><span data-stu-id="0ca69-120">Wide-character string containing the name of the pin.</span></span> <span data-ttu-id="0ca69-121">Per ulteriori informazioni, vedere [**CBasePin:: QueryPinInfo**](cbasepin-querypininfo.md).</span><span class="sxs-lookup"><span data-stu-id="0ca69-121">For more information, see [**CBasePin::QueryPinInfo**](cbasepin-querypininfo.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ca69-122">*dir*</span><span class="sxs-lookup"><span data-stu-id="0ca69-122">*dir*</span></span> 
</dt> <dd>

<span data-ttu-id="0ca69-123">Membro dell'enumerazione [**di \_ direzione del pin**](/windows/win32/api/strmif/ne-strmif-pin_direction) che specifica la direzione del PIN.</span><span class="sxs-lookup"><span data-stu-id="0ca69-123">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumeration specifying the direction of the pin.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0ca69-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="0ca69-124">Remarks</span></span>

<span data-ttu-id="0ca69-125">La sezione critica specificata da *pLock* serializza lo stato del PIN, incluso lo stato della connessione, la scelta dell'allocatore, il tipo di supporto e lo stato delle operazioni di scaricamento.</span><span class="sxs-lookup"><span data-stu-id="0ca69-125">The critical section specified by *pLock* serializes the pin's state, including its connection status, choice of allocator, media type, and the status of flush operations.</span></span> <span data-ttu-id="0ca69-126">Non usare questa sezione critica per serializzare le operazioni di streaming.</span><span class="sxs-lookup"><span data-stu-id="0ca69-126">Do not use this critical section to serialize streaming operations.</span></span> <span data-ttu-id="0ca69-127">Per altre informazioni, vedere [flusso di dati nel grafico del filtro](data-flow-in-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="0ca69-127">For more information, see [Data Flow in the Filter Graph](data-flow-in-the-filter-graph.md).</span></span>

<span data-ttu-id="0ca69-128">Un filtro potrebbe creare pin nel metodo del costruttore, pertanto a questo punto il puntatore *pFilter* potrebbe non riferirsi a un oggetto valido.</span><span class="sxs-lookup"><span data-stu-id="0ca69-128">A filter might create pins in its constructor method, so at this point the *pFilter* pointer might not refer to a valid object.</span></span> <span data-ttu-id="0ca69-129">Archiviare il puntatore, ma non dereferenziarlo all'interno del costruttore del PIN.</span><span class="sxs-lookup"><span data-stu-id="0ca69-129">Store the pointer, but do not dereference it while inside the pin's constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ca69-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0ca69-130">Requirements</span></span>



| <span data-ttu-id="0ca69-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ca69-131">Requirement</span></span> | <span data-ttu-id="0ca69-132">Valore</span><span class="sxs-lookup"><span data-stu-id="0ca69-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ca69-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0ca69-133">Header</span></span><br/>  | <dl> <span data-ttu-id="0ca69-134"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0ca69-134"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0ca69-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="0ca69-135">Library</span></span><br/> | <dl> <span data-ttu-id="0ca69-136"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0ca69-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ca69-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0ca69-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ca69-138">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="0ca69-138">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




