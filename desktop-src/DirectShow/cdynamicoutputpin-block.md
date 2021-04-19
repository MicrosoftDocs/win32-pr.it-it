---
description: 'Il metodo Block blocca o Sblocca il flusso di dati dal pin. Questo metodo implementa il metodo IPinFlowControl:: Block.'
ms.assetid: 8281cd8c-7543-42b5-9a4a-11bdfcb659e3
title: Metodo CDynamicOutputPin. Block (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Block
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6b10e9dfd43f3ad98adf8f6abb0eb7c2223d5970
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333458"
---
# <a name="cdynamicoutputpinblock-method"></a><span data-ttu-id="93e23-104">Metodo CDynamicOutputPin. Block</span><span class="sxs-lookup"><span data-stu-id="93e23-104">CDynamicOutputPin.Block method</span></span>

<span data-ttu-id="93e23-105">Il `Block` metodo blocca o Sblocca il flusso di dati dal pin.</span><span class="sxs-lookup"><span data-stu-id="93e23-105">The `Block` method blocks or unblocks the flow of data from the pin.</span></span> <span data-ttu-id="93e23-106">Questo metodo implementa il metodo [**IPinFlowControl:: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) .</span><span class="sxs-lookup"><span data-stu-id="93e23-106">This method implements the [**IPinFlowControl::Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="93e23-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="93e23-107">Syntax</span></span>


```C++
HRESULT Block(
   DWORD  dwBlockFlags,
   HANDLE hEvent
);
```



## <a name="parameters"></a><span data-ttu-id="93e23-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="93e23-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93e23-109">*dwBlockFlags*</span><span class="sxs-lookup"><span data-stu-id="93e23-109">*dwBlockFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="93e23-110">Flag che indica se bloccare o sbloccare il PIN.</span><span class="sxs-lookup"><span data-stu-id="93e23-110">Flag that indicates whether to block or unblock the pin.</span></span> <span data-ttu-id="93e23-111">Deve essere uno dei valori seguenti: </span><span class="sxs-lookup"><span data-stu-id="93e23-111">Must be one of the following values:</span></span>

<span data-ttu-id="93e23-112">Zero: Sblocca il flusso di dati dal pin.</span><span class="sxs-lookup"><span data-stu-id="93e23-112">Zero: Unblock data flow from the pin.</span></span>

<span data-ttu-id="93e23-113">\_ \_ \_ \_ Blocco di controllo del flusso del pin am: blocca il flusso di dati dal pin.</span><span class="sxs-lookup"><span data-stu-id="93e23-113">AM\_PIN\_FLOW\_CONTROL\_BLOCK: Block data flow from the pin.</span></span>

</dd> <dt>

<span data-ttu-id="93e23-114">*hEvent*</span><span class="sxs-lookup"><span data-stu-id="93e23-114">*hEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="93e23-115">Handle per un oggetto evento o **null**.</span><span class="sxs-lookup"><span data-stu-id="93e23-115">Handle to an event object, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93e23-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="93e23-116">Return value</span></span>

<span data-ttu-id="93e23-117">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="93e23-117">Returns an **HRESULT** value.</span></span> <span data-ttu-id="93e23-118">I valori possibili includono quelli mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="93e23-118">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="93e23-119">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="93e23-119">Return code</span></span>                                                                                                                    | <span data-ttu-id="93e23-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="93e23-120">Description</span></span>                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="93e23-121"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="93e23-121"><dt>**S\_FALSE**</dt></span></span> </dl>                                        | <span data-ttu-id="93e23-122">PIN già sbloccato.</span><span class="sxs-lookup"><span data-stu-id="93e23-122">Pin is already unblocked.</span></span><br/>                     |
| <dl> <span data-ttu-id="93e23-123"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="93e23-123"><dt>**S\_OK**</dt></span></span> </dl>                                           | <span data-ttu-id="93e23-124">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="93e23-124">Success.</span></span><br/>                                      |
| <dl> <span data-ttu-id="93e23-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="93e23-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                                   | <span data-ttu-id="93e23-126">Argomento non valido.</span><span class="sxs-lookup"><span data-stu-id="93e23-126">Invalid argument.</span></span><br/>                             |
| <dl> <span data-ttu-id="93e23-127"><dt>**\_pin VFW \_ E \_ già \_ bloccato**</dt></span><span class="sxs-lookup"><span data-stu-id="93e23-127"><dt>**VFW\_E\_PIN\_ALREADY\_BLOCKED**</dt></span></span> </dl>                   | <span data-ttu-id="93e23-128">Il PIN è già bloccato in un altro thread.</span><span class="sxs-lookup"><span data-stu-id="93e23-128">Pin is already blocked on another thread.</span></span><br/>     |
| <dl> <span data-ttu-id="93e23-129"><dt>**\_pin VFW \_ E \_ già \_ bloccato \_ in \_ questo \_ thread**</dt></span><span class="sxs-lookup"><span data-stu-id="93e23-129"><dt>**VFW\_E\_PIN\_ALREADY\_BLOCKED\_ON\_THIS\_THREAD**</dt></span></span> </dl> | <span data-ttu-id="93e23-130">Il PIN è già bloccato nel thread chiamante.</span><span class="sxs-lookup"><span data-stu-id="93e23-130">Pin is already blocked on the calling thread.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="93e23-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="93e23-131">Remarks</span></span>

<span data-ttu-id="93e23-132">Per ulteriori informazioni su questo metodo, vedere [**IPinFlowControl:: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block).</span><span class="sxs-lookup"><span data-stu-id="93e23-132">For more information about this method, see [**IPinFlowControl::Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block).</span></span> <span data-ttu-id="93e23-133">Internamente, questo metodo chiama uno dei metodi protetti seguenti:</span><span class="sxs-lookup"><span data-stu-id="93e23-133">Internally, this method calls one of the following protected methods:</span></span>

-   <span data-ttu-id="93e23-134">Block (asincrono): [ **CDynamicOutputPin:: AsynchronousBlockOutputPin**](cdynamicoutputpin-asynchronousblockoutputpin.md)</span><span class="sxs-lookup"><span data-stu-id="93e23-134">Block (asynchronous): [**CDynamicOutputPin::AsynchronousBlockOutputPin**](cdynamicoutputpin-asynchronousblockoutputpin.md)</span></span>
-   <span data-ttu-id="93e23-135">Blocco (sincrono): [ **CDynamicOutputPin:: SynchronousBlockOutputPin**](cdynamicoutputpin-synchronousblockoutputpin.md)</span><span class="sxs-lookup"><span data-stu-id="93e23-135">Block (synchronous): [**CDynamicOutputPin::SynchronousBlockOutputPin**](cdynamicoutputpin-synchronousblockoutputpin.md)</span></span>
-   <span data-ttu-id="93e23-136">Sblocco: [ **CDynamicOutputPin:: UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md)</span><span class="sxs-lookup"><span data-stu-id="93e23-136">Unblock: [**CDynamicOutputPin::UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md)</span></span>

<span data-ttu-id="93e23-137">Lo sblocco viene sempre eseguito in modo sincrono.</span><span class="sxs-lookup"><span data-stu-id="93e23-137">Unblocking is always performed synchronously.</span></span>

## <a name="requirements"></a><span data-ttu-id="93e23-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="93e23-138">Requirements</span></span>



| <span data-ttu-id="93e23-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="93e23-139">Requirement</span></span> | <span data-ttu-id="93e23-140">Valore</span><span class="sxs-lookup"><span data-stu-id="93e23-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93e23-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="93e23-141">Header</span></span><br/>  | <dl> <span data-ttu-id="93e23-142"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="93e23-142"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="93e23-143">Libreria</span><span class="sxs-lookup"><span data-stu-id="93e23-143">Library</span></span><br/> | <dl> <span data-ttu-id="93e23-144"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="93e23-144"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93e23-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="93e23-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93e23-146">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="93e23-146">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




