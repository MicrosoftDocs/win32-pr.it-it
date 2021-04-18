---
description: La classe CBaseInputPin è una classe di base astratta per l'implementazione di pin di input. Questa classe aggiunge il supporto per l'interfaccia IMemInputPin, oltre al supporto dell'interfaccia IPin fornito da CBasePin.
ms.assetid: 5a2b7f09-8c8b-45da-a4b7-afeb8d5548c1
title: Classe CBaseInputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba55006438a8484b0bf10b95ac8b9d8bbdb56e0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328689"
---
# <a name="cbaseinputpin-class"></a><span data-ttu-id="56810-104">Classe CBaseInputPin</span><span class="sxs-lookup"><span data-stu-id="56810-104">CBaseInputPin class</span></span>

![gerarchia di classi cbaseinputpin](images/filter07.png)

<span data-ttu-id="56810-106">La `CBaseInputPin` classe è una classe di base astratta per l'implementazione di pin di input.</span><span class="sxs-lookup"><span data-stu-id="56810-106">The `CBaseInputPin` class is an abstract base class for implementing input pins.</span></span> <span data-ttu-id="56810-107">Questa classe aggiunge il supporto per l'interfaccia [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) , oltre al supporto dell'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) fornito da [**CBasePin**](cbasepin.md).</span><span class="sxs-lookup"><span data-stu-id="56810-107">This class adds support for the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface, in addition to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface support provided by [**CBasePin**](cbasepin.md).</span></span>

<span data-ttu-id="56810-108">Per usare questa classe, derivare una nuova classe ed eseguire l'override di almeno i metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="56810-108">To use this class, derive a new class and override at least the following methods:</span></span>

-   [<span data-ttu-id="56810-109">**CBaseInputPin:: BeginFlush**</span><span class="sxs-lookup"><span data-stu-id="56810-109">**CBaseInputPin::BeginFlush**</span></span>](cbaseinputpin-beginflush.md)
-   [<span data-ttu-id="56810-110">**CBaseInputPin:: EndFlush**</span><span class="sxs-lookup"><span data-stu-id="56810-110">**CBaseInputPin::EndFlush**</span></span>](cbaseinputpin-endflush.md)
-   [<span data-ttu-id="56810-111">**CBaseInputPin:: Receive**</span><span class="sxs-lookup"><span data-stu-id="56810-111">**CBaseInputPin::Receive**</span></span>](cbaseinputpin-receive.md)
-   [<span data-ttu-id="56810-112">**CBasePin::CheckMediaType**</span><span class="sxs-lookup"><span data-stu-id="56810-112">**CBasePin::CheckMediaType**</span></span>](cbasepin-checkmediatype.md)
-   [<span data-ttu-id="56810-113">**CBasePin::GetMediaType**</span><span class="sxs-lookup"><span data-stu-id="56810-113">**CBasePin::GetMediaType**</span></span>](cbasepin-getmediatype.md)

<span data-ttu-id="56810-114">A seconda della funzione del PIN, potrebbe essere necessario eseguire l'override di metodi aggiuntivi in `CBaseInputPin` o **CBasePin**.</span><span class="sxs-lookup"><span data-stu-id="56810-114">Depending on the function of the pin, you might need to override additional methods in `CBaseInputPin` or **CBasePin**.</span></span>



| <span data-ttu-id="56810-115">Variabili membro protette</span><span class="sxs-lookup"><span data-stu-id="56810-115">Protected Member Variables</span></span>                                                 | <span data-ttu-id="56810-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="56810-116">Description</span></span>                                                                                                 |
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="56810-117">**\_pAllocator m**</span><span class="sxs-lookup"><span data-stu-id="56810-117">**m\_pAllocator**</span></span>](cbaseinputpin-m-pallocator.md)                        | <span data-ttu-id="56810-118">Puntatore all'allocatore di memoria.</span><span class="sxs-lookup"><span data-stu-id="56810-118">Pointer to the memory allocator.</span></span>                                                                            |
| [<span data-ttu-id="56810-119">**\_bReadOnly m**</span><span class="sxs-lookup"><span data-stu-id="56810-119">**m\_bReadOnly**</span></span>](cbaseinputpin-m-breadonly.md)                          | <span data-ttu-id="56810-120">Flag che indica se l'allocatore produce esempi di supporti di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="56810-120">Flag that indicates whether the allocator produces read-only media samples.</span></span>                                 |
| [<span data-ttu-id="56810-121">**\_bFlushing m**</span><span class="sxs-lookup"><span data-stu-id="56810-121">**m\_bFlushing**</span></span>](cbaseinputpin-m-bflushing.md)                          | <span data-ttu-id="56810-122">Flag che indica se il PIN sta attualmente scaricando.</span><span class="sxs-lookup"><span data-stu-id="56810-122">Flag that indicates whether the pin is currently flushing.</span></span>                                                  |
| [<span data-ttu-id="56810-123">**\_SampleProps m**</span><span class="sxs-lookup"><span data-stu-id="56810-123">**m\_SampleProps**</span></span>](cbaseinputpin-m-sampleprops.md)                      | <span data-ttu-id="56810-124">Proprietà dell'esempio più recente.</span><span class="sxs-lookup"><span data-stu-id="56810-124">Properties of the most recent sample.</span></span>                                                                       |
| <span data-ttu-id="56810-125">Metodi pubblici</span><span class="sxs-lookup"><span data-stu-id="56810-125">Public Methods</span></span>                                                             | <span data-ttu-id="56810-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="56810-126">Description</span></span>                                                                                                 |
| [<span data-ttu-id="56810-127">**CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="56810-127">**CBaseInputPin**</span></span>](cbaseinputpin-cbaseinputpin.md)                       | <span data-ttu-id="56810-128">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="56810-128">Constructor method.</span></span>                                                                                         |
| [<span data-ttu-id="56810-129">**~ CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="56810-129">**~CBaseInputPin**</span></span>](cbaseinputpin--cbaseinputpin.md)                     | <span data-ttu-id="56810-130">Metodo del distruttore.</span><span class="sxs-lookup"><span data-stu-id="56810-130">Destructor method.</span></span>                                                                                          |
| [<span data-ttu-id="56810-131">**BreakConnect**</span><span class="sxs-lookup"><span data-stu-id="56810-131">**BreakConnect**</span></span>](cbaseinputpin-breakconnect.md)                         | <span data-ttu-id="56810-132">Rilascia il pin da una connessione.</span><span class="sxs-lookup"><span data-stu-id="56810-132">Releases the pin from a connection.</span></span>                                                                         |
| [<span data-ttu-id="56810-133">**IsReadOnly**</span><span class="sxs-lookup"><span data-stu-id="56810-133">**IsReadOnly**</span></span>](cbaseinputpin-isreadonly.md)                             | <span data-ttu-id="56810-134">Esegue una query se l'allocatore usa esempi di supporti di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="56810-134">Queries whether the allocator uses read-only media samples.</span></span>                                                 |
| [<span data-ttu-id="56810-135">**Scaricamento**</span><span class="sxs-lookup"><span data-stu-id="56810-135">**IsFlushing**</span></span>](cbaseinputpin-isflushing.md)                             | <span data-ttu-id="56810-136">Esegue una query per determinare se il filtro sta attualmente scaricando.</span><span class="sxs-lookup"><span data-stu-id="56810-136">Queries whether the filter is currently flushing.</span></span>                                                           |
| [<span data-ttu-id="56810-137">**CheckStreaming**</span><span class="sxs-lookup"><span data-stu-id="56810-137">**CheckStreaming**</span></span>](cbaseinputpin-checkstreaming.md)                     | <span data-ttu-id="56810-138">Determina se il pin può accettare esempi.</span><span class="sxs-lookup"><span data-stu-id="56810-138">Determines whether the pin can accept samples.</span></span> <span data-ttu-id="56810-139">Virtuale.</span><span class="sxs-lookup"><span data-stu-id="56810-139">Virtual.</span></span>                                                     |
| [<span data-ttu-id="56810-140">**PassNotify**</span><span class="sxs-lookup"><span data-stu-id="56810-140">**PassNotify**</span></span>](cbaseinputpin-passnotify.md)                             | <span data-ttu-id="56810-141">Passa un messaggio di controllo di qualità all'oggetto appropriato.</span><span class="sxs-lookup"><span data-stu-id="56810-141">Passes a quality-control message to the appropriate object.</span></span>                                                 |
| [<span data-ttu-id="56810-142">**Inattivo**</span><span class="sxs-lookup"><span data-stu-id="56810-142">**Inactive**</span></span>](cbaseinputpin-inactive.md)                                 | <span data-ttu-id="56810-143">Notifica al pin che il filtro non è più attivo.</span><span class="sxs-lookup"><span data-stu-id="56810-143">Notifies the pin that the filter is no longer active.</span></span> <span data-ttu-id="56810-144">Virtuale.</span><span class="sxs-lookup"><span data-stu-id="56810-144">Virtual.</span></span>                                              |
| [<span data-ttu-id="56810-145">**SampleProps**</span><span class="sxs-lookup"><span data-stu-id="56810-145">**SampleProps**</span></span>](cbaseinputpin-sampleprops.md)                           | <span data-ttu-id="56810-146">Recupera le proprietà dell'esempio più recente.</span><span class="sxs-lookup"><span data-stu-id="56810-146">Retrieves the properties of the most recent sample.</span></span>                                                         |
| <span data-ttu-id="56810-147">Metodi IPin</span><span class="sxs-lookup"><span data-stu-id="56810-147">IPin Methods</span></span>                                                               | <span data-ttu-id="56810-148">Descrizione</span><span class="sxs-lookup"><span data-stu-id="56810-148">Description</span></span>                                                                                                 |
| [<span data-ttu-id="56810-149">**BeginFlush**</span><span class="sxs-lookup"><span data-stu-id="56810-149">**BeginFlush**</span></span>](cbaseinputpin-beginflush.md)                             | <span data-ttu-id="56810-150">Avvia un'operazione di svuotamento.</span><span class="sxs-lookup"><span data-stu-id="56810-150">Begins a flush operation.</span></span>                                                                                   |
| [<span data-ttu-id="56810-151">**EndFlush**</span><span class="sxs-lookup"><span data-stu-id="56810-151">**EndFlush**</span></span>](cbaseinputpin-endflush.md)                                 | <span data-ttu-id="56810-152">Termina un'operazione di svuotamento.</span><span class="sxs-lookup"><span data-stu-id="56810-152">Ends a flush operation.</span></span>                                                                                     |
| <span data-ttu-id="56810-153">Metodi IMemInputPin</span><span class="sxs-lookup"><span data-stu-id="56810-153">IMemInputPin Methods</span></span>                                                       | <span data-ttu-id="56810-154">Descrizione</span><span class="sxs-lookup"><span data-stu-id="56810-154">Description</span></span>                                                                                                 |
| [<span data-ttu-id="56810-155">**Getallocator**</span><span class="sxs-lookup"><span data-stu-id="56810-155">**GetAllocator**</span></span>](cbaseinputpin-getallocator.md)                         | <span data-ttu-id="56810-156">Recupera l'allocatore di memoria proposto da questo pin.</span><span class="sxs-lookup"><span data-stu-id="56810-156">Retrieves the memory allocator proposed by this pin.</span></span>                                                        |
| [<span data-ttu-id="56810-157">**NotifyAllocator**</span><span class="sxs-lookup"><span data-stu-id="56810-157">**NotifyAllocator**</span></span>](cbaseinputpin-notifyallocator.md)                   | <span data-ttu-id="56810-158">Specifica un allocatore per la connessione.</span><span class="sxs-lookup"><span data-stu-id="56810-158">Specifies an allocator for the connection.</span></span>                                                                  |
| [<span data-ttu-id="56810-159">**GetAllocatorRequirements**</span><span class="sxs-lookup"><span data-stu-id="56810-159">**GetAllocatorRequirements**</span></span>](cbaseinputpin-getallocatorrequirements.md) | <span data-ttu-id="56810-160">Recupera le proprietà dell'allocatore richieste dal pin di input.</span><span class="sxs-lookup"><span data-stu-id="56810-160">Retrieves the allocator properties requested by the input pin.</span></span>                                              |
| [<span data-ttu-id="56810-161">**Ricevere**</span><span class="sxs-lookup"><span data-stu-id="56810-161">**Receive**</span></span>](cbaseinputpin-receive.md)                                   | <span data-ttu-id="56810-162">Riceve il campione multimediale successivo nel flusso.</span><span class="sxs-lookup"><span data-stu-id="56810-162">Receives the next media sample in the stream.</span></span>                                                               |
| [<span data-ttu-id="56810-163">**ReceiveMultiple**</span><span class="sxs-lookup"><span data-stu-id="56810-163">**ReceiveMultiple**</span></span>](cbaseinputpin-receivemultiple.md)                   | <span data-ttu-id="56810-164">Riceve più campioni nel flusso.</span><span class="sxs-lookup"><span data-stu-id="56810-164">Receives multiple samples in the stream.</span></span>                                                                    |
| [<span data-ttu-id="56810-165">**ReceiveCanBlock**</span><span class="sxs-lookup"><span data-stu-id="56810-165">**ReceiveCanBlock**</span></span>](cbaseinputpin-receivecanblock.md)                   | <span data-ttu-id="56810-166">Determina se le chiamate al metodo [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) potrebbero bloccarsi.</span><span class="sxs-lookup"><span data-stu-id="56810-166">Determines whether calls to the [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method might block.</span></span> |
| <span data-ttu-id="56810-167">Metodi IQualityControl</span><span class="sxs-lookup"><span data-stu-id="56810-167">IQualityControl Methods</span></span>                                                    | <span data-ttu-id="56810-168">Descrizione</span><span class="sxs-lookup"><span data-stu-id="56810-168">Description</span></span>                                                                                                 |
| [<span data-ttu-id="56810-169">**Notifica**</span><span class="sxs-lookup"><span data-stu-id="56810-169">**Notify**</span></span>](cbaseinputpin-notify.md)                                     | <span data-ttu-id="56810-170">Riceve un messaggio di controllo di qualità.</span><span class="sxs-lookup"><span data-stu-id="56810-170">Receives a quality-control message.</span></span>                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="56810-171">Requisiti</span><span class="sxs-lookup"><span data-stu-id="56810-171">Requirements</span></span>



| <span data-ttu-id="56810-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="56810-172">Requirement</span></span> | <span data-ttu-id="56810-173">Valore</span><span class="sxs-lookup"><span data-stu-id="56810-173">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56810-174">Intestazione</span><span class="sxs-lookup"><span data-stu-id="56810-174">Header</span></span><br/>  | <dl> <span data-ttu-id="56810-175"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="56810-175"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="56810-176">Libreria</span><span class="sxs-lookup"><span data-stu-id="56810-176">Library</span></span><br/> | <dl> <span data-ttu-id="56810-177"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="56810-177"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




