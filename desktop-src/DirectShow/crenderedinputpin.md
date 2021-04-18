---
description: La classe CRenderedInputPin è una classe di base per l'implementazione di un pin di input in un renderer.
ms.assetid: 644dc6ef-eefa-4dfa-a27e-cab690b6e1db
title: Classe CRenderedInputPin (Amextra. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3fc00b4aa0ce1fc6c8a93fb2fbda2118ad6bb40e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328824"
---
# <a name="crenderedinputpin-class"></a><span data-ttu-id="6ed02-103">Classe CRenderedInputPin</span><span class="sxs-lookup"><span data-stu-id="6ed02-103">CRenderedInputPin class</span></span>

![gerarchia di classi crenderedinputpin](images/rbase04.png)

<span data-ttu-id="6ed02-105">La classe **CRenderedInputPin** è una classe di base per l'implementazione di un pin di input in un renderer.</span><span class="sxs-lookup"><span data-stu-id="6ed02-105">The **CRenderedInputPin** class is a base class for implementing an input pin on a renderer.</span></span> <span data-ttu-id="6ed02-106">Questa classe è progettata per i filtri renderer che non derivano dalla classe [**CBaseRenderer**](cbaserenderer.md) .</span><span class="sxs-lookup"><span data-stu-id="6ed02-106">This class is designed for renderer filters that do not derive from the [**CBaseRenderer**](cbaserenderer.md) class.</span></span> <span data-ttu-id="6ed02-107">I filtri che derivano da **CBaseRenderer** devono usare la classe [**CRendererInputPin**](crendererinputpin.md) per il pin di input.</span><span class="sxs-lookup"><span data-stu-id="6ed02-107">(Filters that derive from **CBaseRenderer** should use the [**CRendererInputPin**](crendererinputpin.md) class for the input pin.)</span></span>

<span data-ttu-id="6ed02-108">Per utilizzare questa classe, è necessario eseguire almeno le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="6ed02-108">To use this class, you must do at least the following:</span></span>

-   <span data-ttu-id="6ed02-109">Dichiarare una nuova classe pin che eredita **CRenderedInputPin**.</span><span class="sxs-lookup"><span data-stu-id="6ed02-109">Declare a new pin class that inherits **CRenderedInputPin**.</span></span>
-   <span data-ttu-id="6ed02-110">Nella classe pin, dichiarare un oggetto sezione critica per mantenere il blocco di streaming.</span><span class="sxs-lookup"><span data-stu-id="6ed02-110">In your pin class, declare a critical section object to hold the streaming lock.</span></span> <span data-ttu-id="6ed02-111">A questo scopo, è possibile usare la classe [**CCritSec**](ccritsec.md) .</span><span class="sxs-lookup"><span data-stu-id="6ed02-111">You can use the [**CCritSec**](ccritsec.md) class for this purpose.</span></span> <span data-ttu-id="6ed02-112">Per altre informazioni, vedere [thread e sezioni critiche](threads-and-critical-sections.md).</span><span class="sxs-lookup"><span data-stu-id="6ed02-112">For more information, see [Threads and Critical Sections](threads-and-critical-sections.md).</span></span>
-   <span data-ttu-id="6ed02-113">Eseguire l'override di [**CRenderedInputPin:: EndOfStream**](crenderedinputpin-endofstream.md) per mantenere il blocco di streaming.</span><span class="sxs-lookup"><span data-stu-id="6ed02-113">Override [**CRenderedInputPin::EndOfStream**](crenderedinputpin-endofstream.md) to hold the streaming lock.</span></span>
-   <span data-ttu-id="6ed02-114">Implementare i metodi [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive), [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md)e [**CBasePin:: GetMediaType**](cbasepin-getmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="6ed02-114">Implement the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive), [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md), and [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) methods.</span></span>
-   <span data-ttu-id="6ed02-115">Nel filtro implementare [**CBaseFilter:: GetPin**](cbasefilter-getpin.md) per restituire un'istanza della classe pin.</span><span class="sxs-lookup"><span data-stu-id="6ed02-115">In your filter, implement [**CBaseFilter::GetPin**](cbasefilter-getpin.md) to return an instance of your pin class.</span></span>

<span data-ttu-id="6ed02-116">È possibile usare questa classe in un renderer con più di un pin di input.</span><span class="sxs-lookup"><span data-stu-id="6ed02-116">You can use this class in a renderer that has more than one input pin.</span></span> <span data-ttu-id="6ed02-117">Questa classe eredita la classe [**CBaseInputPin**](cbaseinputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="6ed02-117">This class inherits the [**CBaseInputPin**](cbaseinputpin.md) class.</span></span>



| <span data-ttu-id="6ed02-118">Variabili membro protette</span><span class="sxs-lookup"><span data-stu-id="6ed02-118">Protected Member Variables</span></span>                                            | <span data-ttu-id="6ed02-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6ed02-119">Description</span></span>                                                                                                  |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6ed02-120">**\_bAtEndOfStream m**</span><span class="sxs-lookup"><span data-stu-id="6ed02-120">**m\_bAtEndOfStream**</span></span>](crenderedinputpin-m-batendofstream.md)       | <span data-ttu-id="6ed02-121">Indica se è stata raggiunta la fine del flusso.</span><span class="sxs-lookup"><span data-stu-id="6ed02-121">Indicates whether the end of the stream was reached.</span></span>                                                         |
| [<span data-ttu-id="6ed02-122">**\_bCompleteNotified m**</span><span class="sxs-lookup"><span data-stu-id="6ed02-122">**m\_bCompleteNotified**</span></span>](crenderedinputpin-m-bcompletenotified.md) | <span data-ttu-id="6ed02-123">Indica se il pin ha inviato un evento [**EC \_ complete**](ec-complete.md) al gestore del grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="6ed02-123">Indicates whether the pin has sent an [**EC\_COMPLETE**](ec-complete.md) event to the Filter Graph Manager.</span></span> |
| <span data-ttu-id="6ed02-124">Metodi pubblici</span><span class="sxs-lookup"><span data-stu-id="6ed02-124">Public Methods</span></span>                                                        | <span data-ttu-id="6ed02-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6ed02-125">Description</span></span>                                                                                                  |
| [<span data-ttu-id="6ed02-126">**Attivo**</span><span class="sxs-lookup"><span data-stu-id="6ed02-126">**Active**</span></span>](crenderedinputpin-active.md)                            | <span data-ttu-id="6ed02-127">Notifica al pin che il filtro è ora attivo.</span><span class="sxs-lookup"><span data-stu-id="6ed02-127">Notifies the pin that the filter is now active.</span></span>                                                              |
| [<span data-ttu-id="6ed02-128">**CRenderedInputPin**</span><span class="sxs-lookup"><span data-stu-id="6ed02-128">**CRenderedInputPin**</span></span>](crenderedinputpin-crenderedinputpin.md)      | <span data-ttu-id="6ed02-129">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="6ed02-129">Constructor method.</span></span>                                                                                          |
| [<span data-ttu-id="6ed02-130">**Correre**</span><span class="sxs-lookup"><span data-stu-id="6ed02-130">**Run**</span></span>](crenderedinputpin-run.md)                                  | <span data-ttu-id="6ed02-131">Notifica al pin che il filtro è ora in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="6ed02-131">Notifies the pin that the filter is now running.</span></span>                                                             |
| <span data-ttu-id="6ed02-132">Metodi IPin</span><span class="sxs-lookup"><span data-stu-id="6ed02-132">IPin Methods</span></span>                                                          | <span data-ttu-id="6ed02-133">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6ed02-133">Description</span></span>                                                                                                  |
| [<span data-ttu-id="6ed02-134">**EndFlush**</span><span class="sxs-lookup"><span data-stu-id="6ed02-134">**EndFlush**</span></span>](crenderedinputpin-endflush.md)                        | <span data-ttu-id="6ed02-135">Termina un'operazione di svuotamento.</span><span class="sxs-lookup"><span data-stu-id="6ed02-135">Ends a flush operation.</span></span>                                                                                      |
| [<span data-ttu-id="6ed02-136">**EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="6ed02-136">**EndOfStream**</span></span>](crenderedinputpin-endofstream.md)                  | <span data-ttu-id="6ed02-137">Notifica al pin che non sono previsti dati aggiuntivi fino a quando il filtro non riceve un nuovo comando Run.</span><span class="sxs-lookup"><span data-stu-id="6ed02-137">Notifies the pin that no additional data is expected until the filter receives a new run command.</span></span>            |



 

## <a name="requirements"></a><span data-ttu-id="6ed02-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6ed02-138">Requirements</span></span>



| <span data-ttu-id="6ed02-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ed02-139">Requirement</span></span> | <span data-ttu-id="6ed02-140">Valore</span><span class="sxs-lookup"><span data-stu-id="6ed02-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ed02-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6ed02-141">Header</span></span><br/>  | <dl> <span data-ttu-id="6ed02-142"><dt>Amextra. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6ed02-142"><dt>Amextra.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6ed02-143">Libreria</span><span class="sxs-lookup"><span data-stu-id="6ed02-143">Library</span></span><br/> | <dl> <span data-ttu-id="6ed02-144"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6ed02-144"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




