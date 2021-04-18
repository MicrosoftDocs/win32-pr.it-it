---
description: Come controllare gli Stati di presentazione
ms.assetid: 978373ef-b2a4-4035-b889-e28a037c0ab5
title: Come controllare gli Stati di presentazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7a82fe0363a27b9c6f5c054b73ca409835a3dff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308765"
---
# <a name="how-to-control-presentation-states"></a><span data-ttu-id="77a67-103">Come controllare gli Stati di presentazione</span><span class="sxs-lookup"><span data-stu-id="77a67-103">How to Control Presentation States</span></span>

<span data-ttu-id="77a67-104">La sessione multimediale fornisce il controllo del trasporto, ad esempio la modifica degli Stati di presentazione (riproduzione, pausa e arresto in uno scenario di riproduzione in stile playlist).</span><span class="sxs-lookup"><span data-stu-id="77a67-104">The Media Session provides transport control such as changing presentation states (Play, Pause, and Stop in a playlist-style playback scenario).</span></span> <span data-ttu-id="77a67-105">In questo argomento vengono descritti i metodi della sessione multimediale che devono essere chiamati da un'applicazione per modificare lo stato di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="77a67-105">This topic describes Media Session methods that an application should call to change the playback state.</span></span>

<span data-ttu-id="77a67-106">Nella tabella seguente vengono illustrate le transizioni di stato di presentazione valide.</span><span class="sxs-lookup"><span data-stu-id="77a67-106">The following table shows the valid presentation state transitions.</span></span>



| <span data-ttu-id="77a67-107">Transizione dello stato</span><span class="sxs-lookup"><span data-stu-id="77a67-107">State transition</span></span> | <span data-ttu-id="77a67-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="77a67-108">Description</span></span>                                                                                |
|------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="77a67-109">Pausa di riproduzione ></span><span class="sxs-lookup"><span data-stu-id="77a67-109">Play -> Pause</span></span> | <span data-ttu-id="77a67-110">Il clock di presentazione si blocca.</span><span class="sxs-lookup"><span data-stu-id="77a67-110">The presentation clock freezes.</span></span>                                                            |
| <span data-ttu-id="77a67-111">Play-> stop</span><span class="sxs-lookup"><span data-stu-id="77a67-111">Play -> Stop</span></span>  | <span data-ttu-id="77a67-112">Il clock di presentazione viene reimpostato.</span><span class="sxs-lookup"><span data-stu-id="77a67-112">The presentation clock is reset.</span></span>                                                           |
| <span data-ttu-id="77a67-113">Pausa-> riproduzione</span><span class="sxs-lookup"><span data-stu-id="77a67-113">Pause -> Play</span></span> | <span data-ttu-id="77a67-114">Il clock di presentazione riprende dal momento in cui si è bloccato durante il ciclo di riproduzione per sospendere la transizione.</span><span class="sxs-lookup"><span data-stu-id="77a67-114">The presentation clock resumes from the time it froze during the Play to Pause transition.</span></span> |
| <span data-ttu-id="77a67-115">Sospendi-> arrestare</span><span class="sxs-lookup"><span data-stu-id="77a67-115">Pause -> Stop</span></span> | <span data-ttu-id="77a67-116">Il clock di presentazione viene reimpostato.</span><span class="sxs-lookup"><span data-stu-id="77a67-116">The presentation clock is reset.</span></span>                                                           |
| <span data-ttu-id="77a67-117">Stop-> Play</span><span class="sxs-lookup"><span data-stu-id="77a67-117">Stop -> Play</span></span>  | <span data-ttu-id="77a67-118">Il clock di presentazione inizia dall'inizio della presentazione.</span><span class="sxs-lookup"><span data-stu-id="77a67-118">The presentation clock starts from the beginning of the presentation.</span></span>                      |
| <span data-ttu-id="77a67-119">Interrompi-> pausa</span><span class="sxs-lookup"><span data-stu-id="77a67-119">Stop -> Pause</span></span> | <span data-ttu-id="77a67-120">Non consentiti.</span><span class="sxs-lookup"><span data-stu-id="77a67-120">Not allowed.</span></span>                                                                               |



 

## <a name="to-change-presentation-states"></a><span data-ttu-id="77a67-121">Per modificare gli Stati di presentazione</span><span class="sxs-lookup"><span data-stu-id="77a67-121">To change presentation states</span></span>

-   <span data-ttu-id="77a67-122">Chiamare il metodo [**IMFMediaSession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) per sospendere la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="77a67-122">Call the [**IMFMediaSession::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) method to pause playback.</span></span>

    ```C++
    hr = pMediaSession->Pause();
    ```

    

    <span data-ttu-id="77a67-123">Prima di chiamare questo metodo, l'applicazione deve chiamare il metodo [**IMFMediaSession:: GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities) per individuare se l'origine supporto supporta lo stato di sospensione.</span><span class="sxs-lookup"><span data-stu-id="77a67-123">Before calling this method, the application must call the [**IMFMediaSession::GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities) method to discover whether the media source supports the Pause state.</span></span> <span data-ttu-id="77a67-124">In caso contrario, questo metodo restituisce **MFSESSIONCAP \_ pause** nel parametro *pdwCaps* .</span><span class="sxs-lookup"><span data-stu-id="77a67-124">If it does, this method returns **MFSESSIONCAP\_PAUSE** in the *pdwCaps* parameter.</span></span>

    <span data-ttu-id="77a67-125">Pausa interrompe temporaneamente la sessione multimediale, il clock di presentazione e il sink di flusso per la presentazione corrente.</span><span class="sxs-lookup"><span data-stu-id="77a67-125">Pause temporarily stops the Media Session, the presentation clock, and the stream sink for the current presentation.</span></span> <span data-ttu-id="77a67-126">Una volta completata la chiamata, l'applicazione riceve un evento [MESessionPaused](mesessionpaused.md) .</span><span class="sxs-lookup"><span data-stu-id="77a67-126">After the call completes successfully, the application receives a [MESessionPaused](mesessionpaused.md) event.</span></span>

-   <span data-ttu-id="77a67-127">Chiamare il metodo [**IMFMediaSession:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop) per arrestare la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="77a67-127">Call the [**IMFMediaSession::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop) method to stop playback.</span></span>

    ```C++
    hr = pMediaSession->Stop();
    ```

    

    <span data-ttu-id="77a67-128">Questo metodo arresta la sessione multimediale interrompendo l'origine del supporto, gli orologi corrispondenti e i sink di flusso.</span><span class="sxs-lookup"><span data-stu-id="77a67-128">This method stops the Media Session by stopping the media source, the corresponding clocks, and stream sinks.</span></span> <span data-ttu-id="77a67-129">Se la sessione multimediale controlla l' [origine del sequencer](sequencer-source.md), le origini native sottostanti vengono arrestate dall'origine del sequencer.</span><span class="sxs-lookup"><span data-stu-id="77a67-129">If the Media Session is controlling the [Sequencer Source](sequencer-source.md), the underlying native sources are stopped by the sequencer source.</span></span> <span data-ttu-id="77a67-130">Dopo che la sessione multimediale è stata arrestata, l'applicazione riceve un evento [MESessionStopped](mesessionstopped.md) .</span><span class="sxs-lookup"><span data-stu-id="77a67-130">After the Media Session is stopped, the application receives a [MESessionStopped](mesessionstopped.md) event.</span></span>

-   <span data-ttu-id="77a67-131">Chiamare il metodo [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) per avviare la riproduzione o cercare una nuova posizione.</span><span class="sxs-lookup"><span data-stu-id="77a67-131">Call the [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) method to start playback or seek to a new position.</span></span>

    ```C++
    hr = pMediaSession->Start(NULL, &var);
    ```

    

    <span data-ttu-id="77a67-132">Questo metodo avvia la sessione multimediale dagli Stati pause e stop.</span><span class="sxs-lookup"><span data-stu-id="77a67-132">This method starts the Media Session from Pause and Stop states.</span></span> <span data-ttu-id="77a67-133">La sessione multimediale è responsabile della configurazione del flusso di dati nella pipeline.</span><span class="sxs-lookup"><span data-stu-id="77a67-133">The Media Session is responsible for setting up the data flow in the pipeline.</span></span> <span data-ttu-id="77a67-134">Questo metodo indica alla sessione multimediale di avviare il clock di presentazione.</span><span class="sxs-lookup"><span data-stu-id="77a67-134">This method instructs the Media Session to start the presentation clock.</span></span> <span data-ttu-id="77a67-135">Dopo questa chiamata, la sessione multimediale Invia un evento [MESessionStarted](mesessionstarted.md) all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="77a67-135">After this call, Media Session sends a [MESessionStarted](mesessionstarted.md) event to the application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="77a67-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="77a67-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77a67-137">Sessione multimediale</span><span class="sxs-lookup"><span data-stu-id="77a67-137">Media Session</span></span>](media-session.md)
</dt> </dl>

 

 



