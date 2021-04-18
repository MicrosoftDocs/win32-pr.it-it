---
description: Il metodo Connect completa una connessione al pin di output.
ms.assetid: fb20ef5d-e00a-4154-a6da-25bef663c0e7
title: Metodo CPullPin. Connect (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Connect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 97e3b0b676e02dee0e3ebd82de9def56edc2ea28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331181"
---
# <a name="cpullpinconnect-method"></a><span data-ttu-id="b74a8-103">Metodo CPullPin. Connect</span><span class="sxs-lookup"><span data-stu-id="b74a8-103">CPullPin.Connect method</span></span>

<span data-ttu-id="b74a8-104">Il `Connect` metodo completa una connessione al pin di output.</span><span class="sxs-lookup"><span data-stu-id="b74a8-104">The `Connect` method completes a connection to the output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="b74a8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b74a8-105">Syntax</span></span>


```C++
HRESULT Connect(
   IUnknown      *pUnk,
   IMemAllocator *pAlloc,
   BOOL          bSync
);
```



## <a name="parameters"></a><span data-ttu-id="b74a8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b74a8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b74a8-107">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="b74a8-107">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="b74a8-108">Puntatore all'interfaccia **IUnknown** del PIN di output.</span><span class="sxs-lookup"><span data-stu-id="b74a8-108">Pointer to the **IUnknown** interface of the output pin.</span></span>

</dd> <dt>

<span data-ttu-id="b74a8-109">*pAlloc*</span><span class="sxs-lookup"><span data-stu-id="b74a8-109">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="b74a8-110">Puntatore all'interfaccia [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) dell'allocatore preferito del PIN di input o **null**.</span><span class="sxs-lookup"><span data-stu-id="b74a8-110">Pointer to the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface of the input pin's preferred allocator, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b74a8-111">*bSync*</span><span class="sxs-lookup"><span data-stu-id="b74a8-111">*bSync*</span></span> 
</dt> <dd>

<span data-ttu-id="b74a8-112">Valore booleano che specifica se utilizzare le letture sincrone.</span><span class="sxs-lookup"><span data-stu-id="b74a8-112">Boolean value that specifies whether to use synchronous reads.</span></span> <span data-ttu-id="b74a8-113">Se **true**, il pin esegue operazioni di lettura sincrone sul pin di output.</span><span class="sxs-lookup"><span data-stu-id="b74a8-113">If **TRUE**, the pin performs synchronous read operations on the output pin.</span></span> <span data-ttu-id="b74a8-114">Se **false**, il pin esegue richieste di lettura asincrone.</span><span class="sxs-lookup"><span data-stu-id="b74a8-114">If **FALSE**, the pin makes asynchronous read requests.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b74a8-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b74a8-115">Return value</span></span>

<span data-ttu-id="b74a8-116">Restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="b74a8-116">Returns an **HRESULT**.</span></span> <span data-ttu-id="b74a8-117">Di seguito sono indicati alcuni valori possibili.</span><span class="sxs-lookup"><span data-stu-id="b74a8-117">Possible values include the following.</span></span>



| <span data-ttu-id="b74a8-118">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="b74a8-118">Return code</span></span>                                                                                               | <span data-ttu-id="b74a8-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b74a8-119">Description</span></span>                                                                     |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b74a8-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b74a8-120"><dt>**S\_OK**</dt></span></span> </dl>                      | <span data-ttu-id="b74a8-121">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="b74a8-121">Success.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="b74a8-122"><dt>**VFW \_ E \_ già \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="b74a8-122"><dt>**VFW\_E\_ALREADY\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="b74a8-123">Il pin di input è già connesso.</span><span class="sxs-lookup"><span data-stu-id="b74a8-123">The input pin is already connected.</span></span><br/>                                  |
| <dl> <span data-ttu-id="b74a8-124"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="b74a8-124"><dt>**E\_NOINTERFACE**</dt></span></span> </dl>             | <span data-ttu-id="b74a8-125">Il pin di output non espone [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader).</span><span class="sxs-lookup"><span data-stu-id="b74a8-125">The output pin does not expose [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b74a8-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="b74a8-126">Remarks</span></span>

<span data-ttu-id="b74a8-127">Chiamare questo metodo durante il processo di connessione del PIN di input.</span><span class="sxs-lookup"><span data-stu-id="b74a8-127">Call this method during the input pin's connection process.</span></span> <span data-ttu-id="b74a8-128">Se il metodo ha esito negativo, il PIN dovrebbe interrompere la connessione.</span><span class="sxs-lookup"><span data-stu-id="b74a8-128">If the method fails, the pin should fail the connection.</span></span>

<span data-ttu-id="b74a8-129">Questo metodo esegue una query sul pin di output per l'interfaccia **IAsyncReader** .</span><span class="sxs-lookup"><span data-stu-id="b74a8-129">This method queries the output pin for the **IAsyncReader** interface.</span></span> <span data-ttu-id="b74a8-130">Se ha esito positivo, viene chiamato [**CPullPin::D ecideallocator**](cpullpin-decideallocator.md) per negoziare l'allocatore per la connessione.</span><span class="sxs-lookup"><span data-stu-id="b74a8-130">If successful, it calls [**CPullPin::DecideAllocator**](cpullpin-decideallocator.md) to negotiate the allocator for the connection.</span></span> <span data-ttu-id="b74a8-131">Se il pin di input ha un allocatore preferito, specificarlo nel parametro *pAlloc* . il metodo **DecideAllocator** passa questo puntatore al metodo [**IAsyncReader:: RequestAllocator**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) del PIN di output.</span><span class="sxs-lookup"><span data-stu-id="b74a8-131">If your input pin has a preferred allocator, specify it in the *pAlloc* parameter; the **DecideAllocator** method passes this pointer to the output pin's [**IAsyncReader::RequestAllocator**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) method.</span></span> <span data-ttu-id="b74a8-132">In caso contrario, impostare *pAlloc* su **null**.</span><span class="sxs-lookup"><span data-stu-id="b74a8-132">Otherwise, set *pAlloc* to **NULL**.</span></span>

<span data-ttu-id="b74a8-133">Se il valore di *bSync* è **true**, l'oggetto **CPullPin** esegue richieste di lettura sincrone, chiamando il pin di output [**IAsyncReader:: SyncReadAligned**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned).</span><span class="sxs-lookup"><span data-stu-id="b74a8-133">If the value of *bSync* is **TRUE**, the **CPullPin** object makes synchronous read requests, by calling the output pin's [**IAsyncReader::SyncReadAligned**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned).</span></span> <span data-ttu-id="b74a8-134">In caso contrario, chiama il metodo [**IAsyncReader:: Request**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-request) per eseguire richieste di lettura sovrapposte.</span><span class="sxs-lookup"><span data-stu-id="b74a8-134">Otherwise, it calls the [**IAsyncReader::Request**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-request) method to make overlapping read requests.</span></span>

## <a name="requirements"></a><span data-ttu-id="b74a8-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b74a8-135">Requirements</span></span>



| <span data-ttu-id="b74a8-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="b74a8-136">Requirement</span></span> | <span data-ttu-id="b74a8-137">Valore</span><span class="sxs-lookup"><span data-stu-id="b74a8-137">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b74a8-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b74a8-138">Header</span></span><br/>  | <dl> <span data-ttu-id="b74a8-139"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="b74a8-139"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="b74a8-140">Libreria</span><span class="sxs-lookup"><span data-stu-id="b74a8-140">Library</span></span><br/> | <dl> <span data-ttu-id="b74a8-141"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b74a8-141"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b74a8-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b74a8-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b74a8-143">**Classe CPullPin**</span><span class="sxs-lookup"><span data-stu-id="b74a8-143">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




