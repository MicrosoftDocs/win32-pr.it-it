---
description: La classe CBaseOutputPin è una classe di base astratta che implementa un pin di output.
ms.assetid: 5279c8aa-6ec0-4a89-a1b3-6904d7b69a93
title: Classe CBaseOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21949d772c44f02e364013dd98c905b8f59ccdc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330542"
---
# <a name="cbaseoutputpin-class"></a><span data-ttu-id="7bb3b-103">Classe CBaseOutputPin</span><span class="sxs-lookup"><span data-stu-id="7bb3b-103">CBaseOutputPin class</span></span>

![gerarchia di classi cbaseoutputpin](images/filter06.png)

<span data-ttu-id="7bb3b-105">La `CBaseOutputPin` classe è una classe di base astratta che implementa un pin di output.</span><span class="sxs-lookup"><span data-stu-id="7bb3b-105">The `CBaseOutputPin` class is an abstract base class that implements an output pin.</span></span>

<span data-ttu-id="7bb3b-106">Questa classe deriva da [**CBasePin**](cbasepin.md).</span><span class="sxs-lookup"><span data-stu-id="7bb3b-106">This class derives from [**CBasePin**](cbasepin.md).</span></span> <span data-ttu-id="7bb3b-107">Si differenzia da **CBasePin** nei seguenti aspetti:</span><span class="sxs-lookup"><span data-stu-id="7bb3b-107">It differs from **CBasePin** in the following respects:</span></span>

-   <span data-ttu-id="7bb3b-108">Si connette solo ai pin di input che supportano l'interfaccia [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .</span><span class="sxs-lookup"><span data-stu-id="7bb3b-108">It connects only to input pins that support the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>
-   <span data-ttu-id="7bb3b-109">Supporta il trasporto di memoria locale tramite l'interfaccia [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .</span><span class="sxs-lookup"><span data-stu-id="7bb3b-109">It supports local memory transport through the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>
-   <span data-ttu-id="7bb3b-110">Rifiuta le notifiche di fine flusso, svuotamento e nuovo segmento.</span><span class="sxs-lookup"><span data-stu-id="7bb3b-110">It rejects end-of-stream, flush, and new-segment notifications.</span></span> <span data-ttu-id="7bb3b-111">Questi non devono essere inviati a un pin di output.</span><span class="sxs-lookup"><span data-stu-id="7bb3b-111">(These should not be sent to an output pin.)</span></span>
-   <span data-ttu-id="7bb3b-112">Fornisce metodi per la distribuzione di esempi downstream.</span><span class="sxs-lookup"><span data-stu-id="7bb3b-112">It provides methods for delivering samples downstream.</span></span>

<span data-ttu-id="7bb3b-113">Quando il pin si connette, richiede un allocatore di memoria dal pin di input.</span><span class="sxs-lookup"><span data-stu-id="7bb3b-113">When the pin connects, it requests a memory allocator from the input pin.</span></span> <span data-ttu-id="7bb3b-114">In caso contrario, viene creato un nuovo oggetto allocatore.</span><span class="sxs-lookup"><span data-stu-id="7bb3b-114">Failing that, it creates a new allocator object.</span></span> <span data-ttu-id="7bb3b-115">Il pin di output è responsabile dell'impostazione delle proprietà dell'allocatore.</span><span class="sxs-lookup"><span data-stu-id="7bb3b-115">The output pin is responsible for setting the allocator properties.</span></span> <span data-ttu-id="7bb3b-116">Questa operazione viene eseguita tramite il metodo virtuale pure [**CBaseOutputPin::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md).</span><span class="sxs-lookup"><span data-stu-id="7bb3b-116">It does this through the pure virtual method [**CBaseOutputPin::DecideBufferSize**](cbaseoutputpin-decidebuffersize.md).</span></span> <span data-ttu-id="7bb3b-117">Eseguire l'override di questo metodo nella classe derivata.</span><span class="sxs-lookup"><span data-stu-id="7bb3b-117">Override this method in your derived class.</span></span> <span data-ttu-id="7bb3b-118">Se il pin di input presenta requisiti del buffer, questi vengono passati al metodo **DecideBufferSize** .</span><span class="sxs-lookup"><span data-stu-id="7bb3b-118">If the input pin has any buffer requirements, they are passed to the **DecideBufferSize** method.</span></span>

<span data-ttu-id="7bb3b-119">Chiamare il metodo [**CBaseOutputPin:: GetDeliveryBuffer**](cbaseoutputpin-getdeliverybuffer.md) per ottenere un esempio di supporto vuoto.</span><span class="sxs-lookup"><span data-stu-id="7bb3b-119">Call the [**CBaseOutputPin::GetDeliveryBuffer**](cbaseoutputpin-getdeliverybuffer.md) method to obtain an empty media sample.</span></span> <span data-ttu-id="7bb3b-120">Chiamare il metodo [**CBaseOutputPin::D Eliver**](cbaseoutputpin-deliver.md) per fornire esempi downstream.</span><span class="sxs-lookup"><span data-stu-id="7bb3b-120">Call the [**CBaseOutputPin::Deliver**](cbaseoutputpin-deliver.md) method to deliver samples downstream.</span></span>

<span data-ttu-id="7bb3b-121">La classe derivata deve eseguire l'override del metodo [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) virtuale pure per convalidare il tipo di supporto durante le connessioni pin.</span><span class="sxs-lookup"><span data-stu-id="7bb3b-121">Your derived class must override the pure virtual [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method to validate the media type during pin connections.</span></span>



| <span data-ttu-id="7bb3b-122">Variabili membro protette</span><span class="sxs-lookup"><span data-stu-id="7bb3b-122">Protected Member Variables</span></span>                                      | <span data-ttu-id="7bb3b-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7bb3b-123">Description</span></span>                                                                |
|-----------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="7bb3b-124">**\_pAllocator m**</span><span class="sxs-lookup"><span data-stu-id="7bb3b-124">**m\_pAllocator**</span></span>](cbaseoutputpin-m-pallocator.md)            | <span data-ttu-id="7bb3b-125">Puntatore all'allocatore di memoria.</span><span class="sxs-lookup"><span data-stu-id="7bb3b-125">Pointer to the memory allocator.</span></span>                                           |
| [<span data-ttu-id="7bb3b-126">**\_pInputPin m**</span><span class="sxs-lookup"><span data-stu-id="7bb3b-126">**m\_pInputPin**</span></span>](cbaseoutputpin-m-pinputpin.md)              | <span data-ttu-id="7bb3b-127">Puntatore al pin di input connesso a questo pin.</span><span class="sxs-lookup"><span data-stu-id="7bb3b-127">Pointer to the input pin connected to this pin.</span></span>                            |
| <span data-ttu-id="7bb3b-128">Metodi pubblici</span><span class="sxs-lookup"><span data-stu-id="7bb3b-128">Public Methods</span></span>                                                  | <span data-ttu-id="7bb3b-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7bb3b-129">Description</span></span>                                                                |
| [<span data-ttu-id="7bb3b-130">**CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="7bb3b-130">**CBaseOutputPin**</span></span>](cbaseoutputpin-cbaseoutputpin.md)         | <span data-ttu-id="7bb3b-131">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="7bb3b-131">Constructor method.</span></span>                                                        |
| [<span data-ttu-id="7bb3b-132">**CompleteConnect**</span><span class="sxs-lookup"><span data-stu-id="7bb3b-132">**CompleteConnect**</span></span>](cbaseoutputpin-completeconnect.md)       | <span data-ttu-id="7bb3b-133">Completa una connessione a un pin di input.</span><span class="sxs-lookup"><span data-stu-id="7bb3b-133">Completes a connection to an input pin.</span></span> <span data-ttu-id="7bb3b-134">Virtuale.</span><span class="sxs-lookup"><span data-stu-id="7bb3b-134">Virtual.</span></span>                           |
| [<span data-ttu-id="7bb3b-135">**DecideAllocator**</span><span class="sxs-lookup"><span data-stu-id="7bb3b-135">**DecideAllocator**</span></span>](cbaseoutputpin-decideallocator.md)       | <span data-ttu-id="7bb3b-136">Seleziona un allocatore di memoria.</span><span class="sxs-lookup"><span data-stu-id="7bb3b-136">Selects a memory allocator.</span></span> <span data-ttu-id="7bb3b-137">Virtuale.</span><span class="sxs-lookup"><span data-stu-id="7bb3b-137">Virtual.</span></span>                                       |
| [<span data-ttu-id="7bb3b-138">**GetDeliveryBuffer**</span><span class="sxs-lookup"><span data-stu-id="7bb3b-138">**GetDeliveryBuffer**</span></span>](cbaseoutputpin-getdeliverybuffer.md)   | <span data-ttu-id="7bb3b-139">Recupera un esempio multimediale che contiene un buffer vuoto.</span><span class="sxs-lookup"><span data-stu-id="7bb3b-139">Retrieves a media sample that contains an empty buffer.</span></span> <span data-ttu-id="7bb3b-140">Virtuale.</span><span class="sxs-lookup"><span data-stu-id="7bb3b-140">Virtual.</span></span>           |
| [<span data-ttu-id="7bb3b-141">**Distribuzione**</span><span class="sxs-lookup"><span data-stu-id="7bb3b-141">**Deliver**</span></span>](cbaseoutputpin-deliver.md)                       | <span data-ttu-id="7bb3b-142">Recapita un campione multimediale al pin di input connesso.</span><span class="sxs-lookup"><span data-stu-id="7bb3b-142">Delivers a media sample to the connected input pin.</span></span> <span data-ttu-id="7bb3b-143">Virtuale.</span><span class="sxs-lookup"><span data-stu-id="7bb3b-143">Virtual.</span></span>               |
| [<span data-ttu-id="7bb3b-144">**InitAllocator**</span><span class="sxs-lookup"><span data-stu-id="7bb3b-144">**InitAllocator**</span></span>](cbaseoutputpin-initallocator.md)           | <span data-ttu-id="7bb3b-145">Crea un allocatore di memoria.</span><span class="sxs-lookup"><span data-stu-id="7bb3b-145">Creates a memory allocator.</span></span> <span data-ttu-id="7bb3b-146">Virtuale.</span><span class="sxs-lookup"><span data-stu-id="7bb3b-146">Virtual.</span></span>                                       |
| [<span data-ttu-id="7bb3b-147">**CheckConnect**</span><span class="sxs-lookup"><span data-stu-id="7bb3b-147">**CheckConnect**</span></span>](cbaseoutputpin-checkconnect.md)             | <span data-ttu-id="7bb3b-148">Determina se una connessione pin è adatta.</span><span class="sxs-lookup"><span data-stu-id="7bb3b-148">Determines whether a pin connection is suitable.</span></span>                           |
| [<span data-ttu-id="7bb3b-149">**BreakConnect**</span><span class="sxs-lookup"><span data-stu-id="7bb3b-149">**BreakConnect**</span></span>](cbaseoutputpin-breakconnect.md)             | <span data-ttu-id="7bb3b-150">Rilascia il pin da una connessione.</span><span class="sxs-lookup"><span data-stu-id="7bb3b-150">Releases the pin from a connection.</span></span>                                        |
| [<span data-ttu-id="7bb3b-151">**Attivo**</span><span class="sxs-lookup"><span data-stu-id="7bb3b-151">**Active**</span></span>](cbaseoutputpin-active.md)                         | <span data-ttu-id="7bb3b-152">Notifica al pin che il filtro è ora attivo.</span><span class="sxs-lookup"><span data-stu-id="7bb3b-152">Notifies the pin that the filter is now active.</span></span>                            |
| [<span data-ttu-id="7bb3b-153">**Inattivo**</span><span class="sxs-lookup"><span data-stu-id="7bb3b-153">**Inactive**</span></span>](cbaseoutputpin-inactive.md)                     | <span data-ttu-id="7bb3b-154">Notifica al pin che il filtro non è più attivo.</span><span class="sxs-lookup"><span data-stu-id="7bb3b-154">Notifies the pin that the filter is no longer active.</span></span>                      |
| [<span data-ttu-id="7bb3b-155">**DeliverEndOfStream**</span><span class="sxs-lookup"><span data-stu-id="7bb3b-155">**DeliverEndOfStream**</span></span>](cbaseoutputpin-deliverendofstream.md) | <span data-ttu-id="7bb3b-156">Recapita una notifica di fine del flusso al pin di input connesso. Virtuale.</span><span class="sxs-lookup"><span data-stu-id="7bb3b-156">Delivers an end-of-stream notification to the connected input pin.Virtual.</span></span> |
| [<span data-ttu-id="7bb3b-157">**DeliverBeginFlush**</span><span class="sxs-lookup"><span data-stu-id="7bb3b-157">**DeliverBeginFlush**</span></span>](cbaseoutputpin-deliverbeginflush.md)   | <span data-ttu-id="7bb3b-158">Richiede al pin di input connesso di iniziare un'operazione di svuotamento.</span><span class="sxs-lookup"><span data-stu-id="7bb3b-158">Requests the connected input pin to begin a flush operation.</span></span> <span data-ttu-id="7bb3b-159">Virtuale.</span><span class="sxs-lookup"><span data-stu-id="7bb3b-159">Virtual.</span></span>      |
| [<span data-ttu-id="7bb3b-160">**DeliverEndFlush**</span><span class="sxs-lookup"><span data-stu-id="7bb3b-160">**DeliverEndFlush**</span></span>](cbaseoutputpin-deliverendflush.md)       | <span data-ttu-id="7bb3b-161">Richiede al pin di input connesso di terminare un'operazione di svuotamento.</span><span class="sxs-lookup"><span data-stu-id="7bb3b-161">Requests the connected input pin to end a flush operation.</span></span> <span data-ttu-id="7bb3b-162">Virtuale.</span><span class="sxs-lookup"><span data-stu-id="7bb3b-162">Virtual.</span></span>        |
| [<span data-ttu-id="7bb3b-163">**DeliverNewSegment**</span><span class="sxs-lookup"><span data-stu-id="7bb3b-163">**DeliverNewSegment**</span></span>](cbaseoutputpin-delivernewsegment.md)   | <span data-ttu-id="7bb3b-164">Recapita una notifica del nuovo segmento al pin di input connesso.</span><span class="sxs-lookup"><span data-stu-id="7bb3b-164">Delivers a new-segment notification to the connected input pin.</span></span> <span data-ttu-id="7bb3b-165">Virtuale.</span><span class="sxs-lookup"><span data-stu-id="7bb3b-165">Virtual.</span></span>   |
| <span data-ttu-id="7bb3b-166">Metodi virtuali puri</span><span class="sxs-lookup"><span data-stu-id="7bb3b-166">Pure Virtual Methods</span></span>                                            | <span data-ttu-id="7bb3b-167">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7bb3b-167">Description</span></span>                                                                |
| [<span data-ttu-id="7bb3b-168">**DecideBufferSize**</span><span class="sxs-lookup"><span data-stu-id="7bb3b-168">**DecideBufferSize**</span></span>](cbaseoutputpin-decidebuffersize.md)     | <span data-ttu-id="7bb3b-169">Imposta i requisiti del buffer.</span><span class="sxs-lookup"><span data-stu-id="7bb3b-169">Sets the buffer requirements.</span></span>                                              |
| <span data-ttu-id="7bb3b-170">Metodi IPin</span><span class="sxs-lookup"><span data-stu-id="7bb3b-170">IPin Methods</span></span>                                                    | <span data-ttu-id="7bb3b-171">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7bb3b-171">Description</span></span>                                                                |
| [<span data-ttu-id="7bb3b-172">**BeginFlush**</span><span class="sxs-lookup"><span data-stu-id="7bb3b-172">**BeginFlush**</span></span>](cbaseoutputpin-beginflush.md)                 | <span data-ttu-id="7bb3b-173">Avvia un'operazione di svuotamento.</span><span class="sxs-lookup"><span data-stu-id="7bb3b-173">Begins a flush operation.</span></span>                                                  |
| [<span data-ttu-id="7bb3b-174">**EndFlush**</span><span class="sxs-lookup"><span data-stu-id="7bb3b-174">**EndFlush**</span></span>](cbaseoutputpin-endflush.md)                     | <span data-ttu-id="7bb3b-175">Termina un'operazione di svuotamento.</span><span class="sxs-lookup"><span data-stu-id="7bb3b-175">Ends a flush operation.</span></span>                                                    |
| [<span data-ttu-id="7bb3b-176">**EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="7bb3b-176">**EndOfStream**</span></span>](cbaseoutputpin-endofstream.md)               | <span data-ttu-id="7bb3b-177">Notifica al pin che non sono previsti dati aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="7bb3b-177">Notifies the pin that no additional data is expected.</span></span>                      |



 

## <a name="requirements"></a><span data-ttu-id="7bb3b-178">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7bb3b-178">Requirements</span></span>



| <span data-ttu-id="7bb3b-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="7bb3b-179">Requirement</span></span> | <span data-ttu-id="7bb3b-180">Valore</span><span class="sxs-lookup"><span data-stu-id="7bb3b-180">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bb3b-181">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7bb3b-181">Header</span></span><br/>  | <dl> <span data-ttu-id="7bb3b-182"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7bb3b-182"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7bb3b-183">Libreria</span><span class="sxs-lookup"><span data-stu-id="7bb3b-183">Library</span></span><br/> | <dl> <span data-ttu-id="7bb3b-184"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7bb3b-184"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




