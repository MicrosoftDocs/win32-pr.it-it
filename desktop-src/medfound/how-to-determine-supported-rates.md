---
description: Come determinare le tariffe supportate
ms.assetid: 7f2b64e1-1062-4f77-b8e0-62b6d962ae8b
title: Come determinare le tariffe supportate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f67e9753604f51e85c641e616e8b69944b96618
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226458"
---
# <a name="how-to-determine-supported-rates"></a><span data-ttu-id="7b59a-103">Come determinare le tariffe supportate</span><span class="sxs-lookup"><span data-stu-id="7b59a-103">How to Determine Supported Rates</span></span>

<span data-ttu-id="7b59a-104">Prima di modificare la velocità di riproduzione, un'applicazione deve controllare se la velocità di riproduzione è supportata dagli oggetti nella pipeline.</span><span class="sxs-lookup"><span data-stu-id="7b59a-104">Before changing the playback rate, an application should check whether the playback rate is supported by the objects in the pipeline.</span></span> <span data-ttu-id="7b59a-105">L'interfaccia [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) fornisce metodi per ottenere la frequenza massima di avanzamento e inversione, la velocità supportata più vicina a una frequenza richiesta e la velocità più lenta.</span><span class="sxs-lookup"><span data-stu-id="7b59a-105">The [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) interface provides methods to get the maximum forward and reverse rates, the supported rate nearest to a requested rate, and the slowest rate.</span></span> <span data-ttu-id="7b59a-106">Ognuna di queste query di frequenza può specificare la direzione di riproduzione e se utilizzare l'assottigliamento.</span><span class="sxs-lookup"><span data-stu-id="7b59a-106">Each of these rate queries can specify the playback direction and whether to use thinning.</span></span> <span data-ttu-id="7b59a-107">Viene eseguita una query sulla frequenza di riproduzione esatta usando l'interfaccia [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) .</span><span class="sxs-lookup"><span data-stu-id="7b59a-107">The exact playback rate is queried by using the [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) interface.</span></span>

<span data-ttu-id="7b59a-108">Per informazioni sulla modifica delle frequenze di riproduzione, vedere [come impostare la velocità di riproduzione nella sessione multimediale](how-to-set-the-playback-rate-on-the-media-session.md).</span><span class="sxs-lookup"><span data-stu-id="7b59a-108">For information about changing playback rates, see [How to Set the Playback Rate on the Media Session](how-to-set-the-playback-rate-on-the-media-session.md).</span></span>

<span data-ttu-id="7b59a-109">Per informazioni generali sulle frequenze di riproduzione, vedere [informazioni sul controllo della frequenza](about-rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="7b59a-109">For general information about playback rates, see [About Rate Control](about-rate-control.md).</span></span>

## <a name="to-determine-the-current-playback-rate"></a><span data-ttu-id="7b59a-110">Per determinare la frequenza di riproduzione corrente</span><span class="sxs-lookup"><span data-stu-id="7b59a-110">To determine the current playback rate</span></span>

1.  <span data-ttu-id="7b59a-111">Ottenere il servizio di controllo della velocità dalla sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="7b59a-111">Get the rate control service from the Media Session.</span></span>

    ```C++
    IMFRateControl *pRateControl = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateControl, 
           (void**) &pRateControl );
    ```

    

    <span data-ttu-id="7b59a-112">Passare un puntatore all'interfaccia [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) inizializzato nel parametro *punkObject* di [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).</span><span class="sxs-lookup"><span data-stu-id="7b59a-112">Pass an initialized [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) interface pointer in the *punkObject* parameter of [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).</span></span>

    <span data-ttu-id="7b59a-113">L'applicazione deve eseguire una query per il servizio di controllo della velocità tramite la sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="7b59a-113">The application must query for the rate control service through the Media Session.</span></span> <span data-ttu-id="7b59a-114">Internamente, la sessione multimediale esegue una query sugli oggetti nella topologia.</span><span class="sxs-lookup"><span data-stu-id="7b59a-114">Internally, the Media Session queries the objects in the topology.</span></span>

2.  <span data-ttu-id="7b59a-115">Chiamare il metodo [**IMFRateControl:: getrate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate) per ottenere la frequenza di riproduzione corrente.</span><span class="sxs-lookup"><span data-stu-id="7b59a-115">Call the [**IMFRateControl::GetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate) method to get the current playback rate.</span></span>

    ```C++
    hr = pRateControl->GetRate(&bThin, &rate);
    ```

    

    <span data-ttu-id="7b59a-116">Il parametro *pfThin* di [**getrate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate) riceve un valore **bool** che indica se il flusso è attualmente in fase di assottigliamento.</span><span class="sxs-lookup"><span data-stu-id="7b59a-116">The *pfThin* parameter of [**GetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate) receives a **BOOL** value that indicates whether the stream is currently being thinned.</span></span> <span data-ttu-id="7b59a-117">L'applicazione deve passare **null** se non si desidera eseguire una query sul supporto di assottigliamento per il flusso.</span><span class="sxs-lookup"><span data-stu-id="7b59a-117">The application must pass **NULL** if it does not want to query thinning support for the stream.</span></span> <span data-ttu-id="7b59a-118">Il parametro *pflRate* riceve la velocità di riproduzione corrente.</span><span class="sxs-lookup"><span data-stu-id="7b59a-118">The *pflRate* parameter receives the current playback rate.</span></span>

## <a name="to-determine-the-nearest-supported-rate"></a><span data-ttu-id="7b59a-119">Per determinare la frequenza supportata più vicina</span><span class="sxs-lookup"><span data-stu-id="7b59a-119">To determine the nearest supported rate</span></span>

1.  <span data-ttu-id="7b59a-120">Ottenere il servizio di supporto della frequenza dalla sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="7b59a-120">Get the rate support service from the Media Session.</span></span>

    ```C++
    IMFRateSupport *pRateSupport = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateSupport, 
           (void**) &pRateSupport );
    ```

    

    <span data-ttu-id="7b59a-121">Passare un puntatore all'interfaccia [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) inizializzato nel parametro *punkObject* di [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).</span><span class="sxs-lookup"><span data-stu-id="7b59a-121">Pass an initialized [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) interface pointer in the *punkObject* parameter of [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).</span></span>

2.  <span data-ttu-id="7b59a-122">Chiamare il metodo [**IMFRateSupport:: IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) per recuperare la velocità supportata più vicina a una velocità di riproduzione richiesta.</span><span class="sxs-lookup"><span data-stu-id="7b59a-122">Call the [**IMFRateSupport::IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) method to retrieve the supported rate nearest to a requested playback rate.</span></span>

    ```C++
    float rateRequested = 4.0;
    float actualRate = 0;
    hr = pRateSupport->IsRateSupported(
           TRUE, 
           rateRequested, 
           &actualRate );
    ```

    

    <span data-ttu-id="7b59a-123">Nell'esempio viene eseguita una query che indica se la frequenza di riproduzione 4,0 è supportata con il diluente.</span><span class="sxs-lookup"><span data-stu-id="7b59a-123">The example queries whether a playback rate of 4.0 is supported with thinning.</span></span> <span data-ttu-id="7b59a-124">Questa operazione viene indicata passando **true** nel parametro *fThin* di [**IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported).</span><span class="sxs-lookup"><span data-stu-id="7b59a-124">This is indicated by passing **TRUE** in the *fThin* parameter of [**IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported).</span></span> <span data-ttu-id="7b59a-125">Se questa frequenza è supportata, *actualRate* contiene la velocità di riproduzione di 4,0 e la chiamata ha esito positivo con un valore restituito di S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7b59a-125">If this rate is supported, *actualRate* contains the playback rate of 4.0, and the call succeeds with a return value of S\_OK.</span></span> <span data-ttu-id="7b59a-126">Se la frequenza di riproduzione esatta non è supportata, in *actualRate* viene ricevuta la frequenza supportata più vicina.</span><span class="sxs-lookup"><span data-stu-id="7b59a-126">If the exact playback rate is not supported, the nearest supported rate is received in *actualRate*.</span></span> <span data-ttu-id="7b59a-127">Se la frequenza non è supportata e non è disponibile una frequenza di riproduzione più vicina, la chiamata restituisce un codice di errore appropriato.</span><span class="sxs-lookup"><span data-stu-id="7b59a-127">If the rate is not supported and there is no available nearest playback rate, the call returns an appropriate error code.</span></span>

    <span data-ttu-id="7b59a-128">Questi valori possono variare a seconda dei componenti della pipeline caricati.</span><span class="sxs-lookup"><span data-stu-id="7b59a-128">These values can change depending on which pipeline components are loaded.</span></span> <span data-ttu-id="7b59a-129">Pertanto, è necessario eseguire di nuovo la query sui valori ogni volta che si carica un nuovo topololgy.</span><span class="sxs-lookup"><span data-stu-id="7b59a-129">Therefore, you should query the values again whenever you load a new topololgy.</span></span>

    <span data-ttu-id="7b59a-130">Se la frequenza di riproduzione desiderata non è supportata, un'opzione consiste nell'eseguire una query su ogni oggetto della topologia singolarmente, per verificare se un particolare componente non supporta la frequenza.</span><span class="sxs-lookup"><span data-stu-id="7b59a-130">If the desired playback rate is not supported, one option is to query each object in the topology individually, to find out if a particular component does not support the rate.</span></span> <span data-ttu-id="7b59a-131">Potrebbe essere possibile ricompilare la topologia senza questo componente, quindi riprodurla alla velocità desiderata.</span><span class="sxs-lookup"><span data-stu-id="7b59a-131">You might be able to rebuild the topology without this component and then play at the desired rate.</span></span> <span data-ttu-id="7b59a-132">Se, ad esempio, ogni componente eccetto il renderer audio supporta una determinata frequenza, è possibile ricompilare la topologia senza il ramo audio e riprodurla alla velocità desiderata senza audio.</span><span class="sxs-lookup"><span data-stu-id="7b59a-132">For example, if every component except the audio renderer supports a given rate, you could rebuild the topology without the audio branch and play at the desired rate without audio.</span></span>

## <a name="to-determine-the-slowest-supported-rate"></a><span data-ttu-id="7b59a-133">Per determinare la velocità più lenta supportata</span><span class="sxs-lookup"><span data-stu-id="7b59a-133">To determine the slowest supported rate</span></span>

1.  <span data-ttu-id="7b59a-134">Ottenere il servizio di supporto della frequenza dalla sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="7b59a-134">Get the rate support service from the Media Session.</span></span>

    ```C++
    IMFRateSupport *pRateSupport = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateSupport, 
           (void**) &pRateSupport );
    ```

    

    <span data-ttu-id="7b59a-135">Passare un puntatore all'interfaccia [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) inizializzato nel parametro *punkObject* di [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).</span><span class="sxs-lookup"><span data-stu-id="7b59a-135">Pass an initialized [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) interface pointer in the *punkObject* parameter of [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).</span></span>

2.  <span data-ttu-id="7b59a-136">Chiamare il metodo [**IMFRateSupport:: GetSlowestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate) per recuperare la velocità supportata più lenta.</span><span class="sxs-lookup"><span data-stu-id="7b59a-136">Call the [**IMFRateSupport::GetSlowestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate) method to retrieve the slowest supported rate.</span></span>

    ```C++
    float slowestRate = 0;
    hr = pRateSupport->GetSlowestRate(
           MFRATE_REVERSE, 
           TRUE, 
           &slowestRate);
    ```

    

    <span data-ttu-id="7b59a-137">Nell'esempio viene eseguita una query per la frequenza di riproduzione inversa più lenta con assottigliamento.</span><span class="sxs-lookup"><span data-stu-id="7b59a-137">The example queries for the slowest reverse playback rate with thinning.</span></span> <span data-ttu-id="7b59a-138">Il tasso di limite inferiore è stato ricevuto nel parametro *slowestRate* di [**GetSlowestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate).</span><span class="sxs-lookup"><span data-stu-id="7b59a-138">The lower bound rate is received in *slowestRate* parameter of [**GetSlowestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate).</span></span>

    <span data-ttu-id="7b59a-139">Se la riproduzione inversa o l'assottigliamento non è supportato, la chiamata restituisce un codice di errore appropriato.</span><span class="sxs-lookup"><span data-stu-id="7b59a-139">If reverse playback or thinning is not supported, the call returns an appropriate error code.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b59a-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7b59a-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b59a-141">Sessione multimediale</span><span class="sxs-lookup"><span data-stu-id="7b59a-141">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="7b59a-142">Controllo della frequenza</span><span class="sxs-lookup"><span data-stu-id="7b59a-142">Rate Control</span></span>](rate-control.md)
</dt> <dt>

[<span data-ttu-id="7b59a-143">Ricerca, avanzamento rapido e riproduzione inversa</span><span class="sxs-lookup"><span data-stu-id="7b59a-143">Seeking, Fast Forward, and Reverse Play</span></span>](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



