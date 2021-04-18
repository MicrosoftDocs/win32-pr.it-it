---
description: Informazioni sul controllo della frequenza
ms.assetid: 509b2cc8-6017-41a9-ae80-9af21dce9367
title: Informazioni sul controllo della frequenza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3757e4d1d8a374061ff0c0e7fe02ba3c62243c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306765"
---
# <a name="about-rate-control"></a><span data-ttu-id="eeaf1-103">Informazioni sul controllo della frequenza</span><span class="sxs-lookup"><span data-stu-id="eeaf1-103">About Rate Control</span></span>

<span data-ttu-id="eeaf1-104">In Media Foundation la *velocità di riproduzione* viene espressa come rapporto tra la velocità di riproduzione corrente e la frequenza di riproduzione normale.</span><span class="sxs-lookup"><span data-stu-id="eeaf1-104">In Media Foundation, the *playback rate* is expressed as the ratio of the current playback rate to the normal playback rate.</span></span> <span data-ttu-id="eeaf1-105">Ad esempio, una frequenza di 2,0 è due volte la velocità normale e 0,5 è la velocità della metà normale.</span><span class="sxs-lookup"><span data-stu-id="eeaf1-105">For example, a rate of 2.0 is twice normal speed, and 0.5 is half normal speed.</span></span> <span data-ttu-id="eeaf1-106">I valori negativi indicano la riproduzione inversa.</span><span class="sxs-lookup"><span data-stu-id="eeaf1-106">Negative values indicate reverse playback.</span></span> <span data-ttu-id="eeaf1-107">Una velocità di riproduzione di-2,0 viene riprodotta all'indietro nel flusso al doppio della velocità normale.</span><span class="sxs-lookup"><span data-stu-id="eeaf1-107">A playback rate of -2.0 plays backward through the stream at twice the normal speed.</span></span> <span data-ttu-id="eeaf1-108">Una frequenza pari a zero causa il rendering di un frame; Successivamente, il clock di presentazione non avanza.</span><span class="sxs-lookup"><span data-stu-id="eeaf1-108">A rate of zero causes one frame to be rendered; after that, the presentation clock does not advance.</span></span> <span data-ttu-id="eeaf1-109">Per ottenere un altro frame alla velocità pari a zero, è necessario che l'applicazione cerchi una nuova posizione.</span><span class="sxs-lookup"><span data-stu-id="eeaf1-109">To get another frame at the rate of zero, the application must seek to a new position.</span></span>

<span data-ttu-id="eeaf1-110">Le applicazioni utilizzano le interfacce seguenti per controllare la velocità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="eeaf1-110">Applications use the following interfaces to control the playback rate.</span></span>

-   <span data-ttu-id="eeaf1-111">[**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport).</span><span class="sxs-lookup"><span data-stu-id="eeaf1-111">[**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport).</span></span> <span data-ttu-id="eeaf1-112">Usato per individuare le frequenze di riproduzione più veloci e più lente possibili.</span><span class="sxs-lookup"><span data-stu-id="eeaf1-112">Used to find out the fastest and slowest playback rates that are possible.</span></span>
-   <span data-ttu-id="eeaf1-113">[**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol).</span><span class="sxs-lookup"><span data-stu-id="eeaf1-113">[**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol).</span></span> <span data-ttu-id="eeaf1-114">Usato per modificare la velocità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="eeaf1-114">Used to change the playback rate.</span></span>

<span data-ttu-id="eeaf1-115">Per ottenere queste due interfacce, chiamare [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) nella sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="eeaf1-115">To get these two interfaces, call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the Media Session.</span></span> <span data-ttu-id="eeaf1-116">L'identificatore del servizio è MF \_ rate \_ Control \_ Service.</span><span class="sxs-lookup"><span data-stu-id="eeaf1-116">The service identifier is MF\_RATE\_CONTROL\_SERVICE.</span></span>

<span data-ttu-id="eeaf1-117">Tramite il servizio di controllo della velocità, un'applicazione può implementare una riproduzione veloce e inversa.</span><span class="sxs-lookup"><span data-stu-id="eeaf1-117">By using the rate control service, an application can implement fast forward and reverse playback.</span></span>

## <a name="thinning"></a><span data-ttu-id="eeaf1-118">Diradamento</span><span class="sxs-lookup"><span data-stu-id="eeaf1-118">Thinning</span></span>

<span data-ttu-id="eeaf1-119">L' *assottigliamento* è un processo che riduce il numero di campioni in un flusso, per ridurre la velocità complessiva dei bit.</span><span class="sxs-lookup"><span data-stu-id="eeaf1-119">*Thinning* is any process that reduces the number of samples in a stream, to reduce the overall bit rate.</span></span> <span data-ttu-id="eeaf1-120">Per i video, il assottigliamento viene in genere eseguito eliminando i frame Delta e distribuendo solo i fotogrammi chiave.</span><span class="sxs-lookup"><span data-stu-id="eeaf1-120">For video, thinning is generally accomplished by dropping the delta frames and delivering only the key frames.</span></span> <span data-ttu-id="eeaf1-121">Spesso la pipeline è in grado di supportare frequenze di riproduzione più veloci usando la riproduzione diluita, perché la velocità dei dati è inferiore perché i frame Delta non sono decodificati.</span><span class="sxs-lookup"><span data-stu-id="eeaf1-121">Often the pipeline can support faster playback rates using thinned playback, because the data rate is lower because delta frames are not decoded.</span></span>

<span data-ttu-id="eeaf1-122">Il assottigliamento non modifica i timestamp o le durate degli esempi.</span><span class="sxs-lookup"><span data-stu-id="eeaf1-122">Thinning does not change the time stamps or durations on the samples.</span></span> <span data-ttu-id="eeaf1-123">Se, ad esempio, la velocità nominale del flusso video è 25 fotogrammi al secondo, la durata di ogni fotogramma viene comunque contrassegnata come 40 millisecondi, anche se l'origine del supporto sta eliminando tutti i frame Delta.</span><span class="sxs-lookup"><span data-stu-id="eeaf1-123">For example, if the nominal rate of the video stream is 25 frames per second, the duration of each frame is still marked as 40 milliseconds, even if the media source is dropping all of the delta frames.</span></span> <span data-ttu-id="eeaf1-124">Ciò significa che ci sarà un gap di tempo tra la fine di un frame e l'inizio del successivo.</span><span class="sxs-lookup"><span data-stu-id="eeaf1-124">That means there will be a time gap between the end of one frame and the start of the next.</span></span>

## <a name="scrubbing"></a><span data-ttu-id="eeaf1-125">Pulitura</span><span class="sxs-lookup"><span data-stu-id="eeaf1-125">Scrubbing</span></span>

<span data-ttu-id="eeaf1-126">Lo *scrubbing* è il processo di ricerca immediata di punti specifici nel flusso interagendo con una barra di scorrimento, una sequenza temporale o un'altra rappresentazione visiva del tempo.</span><span class="sxs-lookup"><span data-stu-id="eeaf1-126">*Scrubbing* is the process of instantaneously seeking to specific points in the stream by interacting with a scrollbar, timeline, or other visual representation of time.</span></span> <span data-ttu-id="eeaf1-127">Il termine deriva dall'era dei lettori di nastri da bobina a bobina quando il dondolo di una bobina per individuare una sezione era come la pulitura della testa di riproduzione con il nastro.</span><span class="sxs-lookup"><span data-stu-id="eeaf1-127">The term comes from the era of reel-to-reel tape players when rocking a reel back and forth to locate a section was like scrubbing the playback head with the tape.</span></span>

<span data-ttu-id="eeaf1-128">Lo scrubbing viene implementato in Media Foundation impostando la velocità di riproduzione su zero.</span><span class="sxs-lookup"><span data-stu-id="eeaf1-128">Scrubbing is implemented in Media Foundation by setting the playback rate to zero.</span></span> <span data-ttu-id="eeaf1-129">Per ulteriori informazioni, vedere [come eseguire lo scrubbing](how-to-perform-scrubbing.md).</span><span class="sxs-lookup"><span data-stu-id="eeaf1-129">For more information, see [How to Perform Scrubbing](how-to-perform-scrubbing.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="eeaf1-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eeaf1-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eeaf1-131">Controllo della frequenza</span><span class="sxs-lookup"><span data-stu-id="eeaf1-131">Rate Control</span></span>](rate-control.md)
</dt> <dt>

[<span data-ttu-id="eeaf1-132">Ricerca, avanzamento rapido e riproduzione inversa</span><span class="sxs-lookup"><span data-stu-id="eeaf1-132">Seeking, Fast Forward, and Reverse Play</span></span>](seeking--fast-forward--and-reverse-play.md)
</dt> <dt>

[<span data-ttu-id="eeaf1-133">Interfacce del servizio</span><span class="sxs-lookup"><span data-stu-id="eeaf1-133">Service Interfaces</span></span>](service-interfaces.md)
</dt> </dl>

 

 



