---
description: Informazioni sulla sessione multimediale
ms.assetid: 09f50b11-0e0a-42b6-a7bf-bb0135343351
title: Informazioni sulla sessione multimediale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc490e63f623fb3c2d5efde5a80f1988566f9345
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103968846"
---
# <a name="about-the-media-session"></a><span data-ttu-id="a4f44-103">Informazioni sulla sessione multimediale</span><span class="sxs-lookup"><span data-stu-id="a4f44-103">About the Media Session</span></span>

<span data-ttu-id="a4f44-104">La sessione multimediale espone l'interfaccia [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) .</span><span class="sxs-lookup"><span data-stu-id="a4f44-104">The Media Session exposes the [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) interface.</span></span> <span data-ttu-id="a4f44-105">Esistono due modi per creare la sessione multimediale, a seconda che l'applicazione supporti il contenuto protetto:</span><span class="sxs-lookup"><span data-stu-id="a4f44-105">There are two ways to create the Media Session, depending on whether your application will support protected content:</span></span>

-   <span data-ttu-id="a4f44-106">Se l'applicazione non supporta il contenuto protetto, è possibile creare la sessione multimediale chiamando [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession).</span><span class="sxs-lookup"><span data-stu-id="a4f44-106">If your application does not support protected content, you can create the Media Session by calling the [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession).</span></span> <span data-ttu-id="a4f44-107">Questa funzione crea la sessione multimediale all'interno del processo dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a4f44-107">This function creates the Media Session inside the application process.</span></span>
-   <span data-ttu-id="a4f44-108">Per supportare il contenuto protetto, creare la sessione multimediale chiamando [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession).</span><span class="sxs-lookup"><span data-stu-id="a4f44-108">To support protected content, create the Media Session by calling [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession).</span></span> <span data-ttu-id="a4f44-109">Questa funzione crea la sessione multimediale all'interno del processo del percorso multimediale protetto (PMP).</span><span class="sxs-lookup"><span data-stu-id="a4f44-109">This function creates the Media Session inside the Protected Media Path (PMP) process.</span></span> <span data-ttu-id="a4f44-110">L'applicazione riceve un puntatore a un oggetto proxy che effettua il marshalling delle chiamate al metodo attraverso il limite di processo.</span><span class="sxs-lookup"><span data-stu-id="a4f44-110">The application receives a pointer to a proxy object that marshals method calls across the process boundary.</span></span> <span data-ttu-id="a4f44-111">Si noti che la sessione multimediale PMP può essere usata per riprodurre contenuto non crittografato, nonché per contenuti protetti.</span><span class="sxs-lookup"><span data-stu-id="a4f44-111">Note that the PMP Media Session can be used to play clear content, as well as protected content.</span></span>

<span data-ttu-id="a4f44-112">Tutte le applicazioni che usano la sessione multimediale seguiranno i passaggi generali seguenti:</span><span class="sxs-lookup"><span data-stu-id="a4f44-112">Any application that uses the Media Session will follow these general steps:</span></span>

1.  <span data-ttu-id="a4f44-113">Creare una topologia.</span><span class="sxs-lookup"><span data-stu-id="a4f44-113">Create a topology.</span></span>
2.  <span data-ttu-id="a4f44-114">Accodare la topologia nella sessione multimediale chiamando [**IMFMediaSession:: Setopologia**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span><span class="sxs-lookup"><span data-stu-id="a4f44-114">Queue the topology on the Media Session by calling [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span>
3.  <span data-ttu-id="a4f44-115">Controllare il flusso di dati chiamando [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start), [**IMFMediaSession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause)o [**IMFMediaSession:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop).</span><span class="sxs-lookup"><span data-stu-id="a4f44-115">Control the flow of data by calling [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start), [**IMFMediaSession::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause), or [**IMFMediaSession::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop).</span></span>
4.  <span data-ttu-id="a4f44-116">Prima di uscire dall'applicazione, chiamare [**IMFMediaSession:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) per chiudere la sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="a4f44-116">Before the application exits, call [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) to close the Media Session.</span></span>
5.  <span data-ttu-id="a4f44-117">Arrestare le origini multimediali create dall'applicazione, chiamando [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span><span class="sxs-lookup"><span data-stu-id="a4f44-117">Shut down any media sources that the application created, by calling [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span></span>
6.  <span data-ttu-id="a4f44-118">Arrestare la sessione multimediale chiamando [**IMFMediaSession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span><span class="sxs-lookup"><span data-stu-id="a4f44-118">Shut down the Media Session by calling [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span></span>

<span data-ttu-id="a4f44-119">Quando si usa la sessione multimediale, l'applicazione non deve avviare, sospendere o arrestare direttamente l'origine del supporto.</span><span class="sxs-lookup"><span data-stu-id="a4f44-119">When using the Media Session, the application should not directly start, pause, or stop the media source.</span></span> <span data-ttu-id="a4f44-120">Tutte le modifiche di stato devono essere avviate chiamando i metodi [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) .</span><span class="sxs-lookup"><span data-stu-id="a4f44-120">All state changes must be initiated by calling [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) methods.</span></span> <span data-ttu-id="a4f44-121">Le modifiche di stato nell'origine supporto vengono gestite dalla sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="a4f44-121">State changes in the media source are handled by the Media Session.</span></span>

<span data-ttu-id="a4f44-122">Molti altri dettagli dipendono dalla funzionalità specifica dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a4f44-122">Many other details will depend on the specific functionality of your application.</span></span>

## <a name="protected-content"></a><span data-ttu-id="a4f44-123">Contenuto protetto</span><span class="sxs-lookup"><span data-stu-id="a4f44-123">Protected Content</span></span>

<span data-ttu-id="a4f44-124">Per riprodurre contenuti protetti, è necessario creare la sessione multimediale all'interno del percorso multimediale protetto (PMP), chiamando [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession).</span><span class="sxs-lookup"><span data-stu-id="a4f44-124">To play protected content, you must create the Media Session inside the protected media path (PMP), by calling [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession).</span></span> <span data-ttu-id="a4f44-125">Questa funzione crea un'istanza della sessione multimediale all'interno di PMP e restituisce un puntatore a un oggetto proxy che effettua il marshalling delle interfacce attraverso il limite del processo.</span><span class="sxs-lookup"><span data-stu-id="a4f44-125">This function creates an instance of the Media Session inside the PMP and returns a pointer to a proxy object that marshals interfaces across the process boundary.</span></span>

<span data-ttu-id="a4f44-126">Nella maggior parte dei casi, l'uso della sessione multimediale all'interno del PMP è trasparente per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a4f44-126">In most respects, using the Media Session inside the PMP is transparent to the application.</span></span> <span data-ttu-id="a4f44-127">Tuttavia, l'applicazione potrebbe dover richiamare determinate azioni che consentono all'utente di riprodurre il contenuto.</span><span class="sxs-lookup"><span data-stu-id="a4f44-127">However, the application might need to invoke certain actions that enable the user to play the content.</span></span> <span data-ttu-id="a4f44-128">È ad esempio possibile che l'utente debba ottenere una licenza DRM.</span><span class="sxs-lookup"><span data-stu-id="a4f44-128">For example, the user might need to obtain a DRM license.</span></span> <span data-ttu-id="a4f44-129">Media Foundation definisce un meccanismo generico per queste azioni usando l'interfaccia [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) .</span><span class="sxs-lookup"><span data-stu-id="a4f44-129">Media Foundation defines a generic mechanism for these actions using the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface.</span></span>

<span data-ttu-id="a4f44-130">Per altre informazioni, vedere i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="a4f44-130">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="a4f44-131">Percorso supporto protetto</span><span class="sxs-lookup"><span data-stu-id="a4f44-131">Protected Media Path</span></span>](protected-media-path.md)
-   [<span data-ttu-id="a4f44-132">Come riprodurre file multimediali protetti</span><span class="sxs-lookup"><span data-stu-id="a4f44-132">How to Play Protected Media Files</span></span>](how-to-play-protected-media-files.md)

## <a name="presentation-clock"></a><span data-ttu-id="a4f44-133">Orologio di presentazione</span><span class="sxs-lookup"><span data-stu-id="a4f44-133">Presentation Clock</span></span>

<span data-ttu-id="a4f44-134">La sessione multimediale gestisce tutti gli aspetti del clock di presentazione:</span><span class="sxs-lookup"><span data-stu-id="a4f44-134">The Media Session manages all aspects of the presentation clock:</span></span>

-   <span data-ttu-id="a4f44-135">Creazione del clock di presentazione.</span><span class="sxs-lookup"><span data-stu-id="a4f44-135">Creating the presentation clock.</span></span>

-   <span data-ttu-id="a4f44-136">Selezione dell'origine dell'ora.</span><span class="sxs-lookup"><span data-stu-id="a4f44-136">Selecting the time source.</span></span>

-   <span data-ttu-id="a4f44-137">Notifica dei sink di supporto sull'orologio</span><span class="sxs-lookup"><span data-stu-id="a4f44-137">Notifying the media sinks about the clock</span></span>

-   <span data-ttu-id="a4f44-138">Avvio, arresto e sospensione dell'orologio secondo necessità.</span><span class="sxs-lookup"><span data-stu-id="a4f44-138">Starting, stopping, and pausing the clock as necessary.</span></span>

-   <span data-ttu-id="a4f44-139">Chiusura dell'orologio.</span><span class="sxs-lookup"><span data-stu-id="a4f44-139">Shutting down the clock.</span></span>

<span data-ttu-id="a4f44-140">Per ottenere un puntatore al clock di presentazione, chiamare [**IMFMediaSession:: getclock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock) nella sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="a4f44-140">To get a pointer to the presentation clock, call [**IMFMediaSession::GetClock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock) on the Media Session.</span></span> <span data-ttu-id="a4f44-141">Il clock di presentazione non restituisce un tempo valido fino a quando la sessione multimediale non invia l'evento [MESessionTopologyStatus](mesessiontopologystatus.md) con il \_ flag MF TOPOSTATUS \_ Ready.</span><span class="sxs-lookup"><span data-stu-id="a4f44-141">The presentation clock does not return a valid time until the Media Session sends the [MESessionTopologyStatus](mesessiontopologystatus.md) event with the MF\_TOPOSTATUS\_READY flag.</span></span> <span data-ttu-id="a4f44-142">Fino ad allora, **getclock** restituisce MF \_ E \_ clock \_ No \_ time \_ source.</span><span class="sxs-lookup"><span data-stu-id="a4f44-142">Until then, **GetClock** returns MF\_E\_CLOCK\_NO\_TIME\_SOURCE.</span></span>

<span data-ttu-id="a4f44-143">Un'applicazione che usa la sessione multimediale non deve mai avviare, arrestare o sospendere il clock di presentazione; modificare la frequenza di clock; o arrestare l'orologio.</span><span class="sxs-lookup"><span data-stu-id="a4f44-143">An application that uses the Media Session should never start, stop, or pause the presentation clock; change the clock rate; or shut down the clock.</span></span>

<span data-ttu-id="a4f44-144">Quando l'applicazione chiama [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start), la sessione multimediale avvia il clock di presentazione con un'ora di inizio uguale alla posizione iniziale specificata nel metodo **Start** .</span><span class="sxs-lookup"><span data-stu-id="a4f44-144">When the application calls [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start), the Media Session starts the presentation clock with a starting time equal to the starting position specified in the **Start** method.</span></span> <span data-ttu-id="a4f44-145">Per ulteriori informazioni sulla sessione multimediale, vedere [media session](media-session.md).</span><span class="sxs-lookup"><span data-stu-id="a4f44-145">For more information about the Media Session, see [Media Session](media-session.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a4f44-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a4f44-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4f44-147">Sessione multimediale</span><span class="sxs-lookup"><span data-stu-id="a4f44-147">Media Session</span></span>](media-session.md)
</dt> </dl>

 

 



