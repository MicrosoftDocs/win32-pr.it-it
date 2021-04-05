---
title: Uso di PlaySound per riprodurre suoni di sistema
description: Uso di PlaySound per riprodurre suoni di sistema
ms.assetid: b645c488-8b76-4886-8909-75f0342263db
keywords:
- audio Waveform, funzione PlaySound
- audio Waveform, riproduzione di suoni di sistema
- audio Waveform, eventi audio
- Funzione PlaySound, riproduzione di suoni di sistema
- Funzione PlaySound, eventi audio
- riproduzione di suoni di sistema Waveform
- eventi audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1940ee9f207213c4337c9b6bb0a0d58b0f471000
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872513"
---
# <a name="using-playsound-to-play-system-sounds"></a><span data-ttu-id="e177d-110">Uso di PlaySound per riprodurre suoni di sistema</span><span class="sxs-lookup"><span data-stu-id="e177d-110">Using PlaySound to Play System Sounds</span></span>

<span data-ttu-id="e177d-111">La funzione [**PlaySound**](/previous-versions//dd743680(v=vs.85)) riprodurrà anche i suoni a cui fa riferimento un nome di chiave nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="e177d-111">The [**PlaySound**](/previous-versions//dd743680(v=vs.85)) function will also play sounds referred to by a keyname in the registry.</span></span> <span data-ttu-id="e177d-112">Gli utenti possono assegnare i propri suoni agli avvisi e agli avvisi di sistema o alle azioni dell'utente, ad esempio un clic del pulsante del mouse.</span><span class="sxs-lookup"><span data-stu-id="e177d-112">Users can assign their own sounds to system alerts and warnings, or to user actions, such as a mouse button click.</span></span> <span data-ttu-id="e177d-113">I suoni associati a avvisi di sistema e avvisi sono detti *eventi audio*.</span><span class="sxs-lookup"><span data-stu-id="e177d-113">Sounds that are associated with system alerts and warnings are called *sound events*.</span></span>

<span data-ttu-id="e177d-114">Per riprodurre un evento audio, chiamare **PlaySound** con il parametro *pszSound* che punta a una stringa contenente il nome della voce del registro di sistema che identifica il suono.</span><span class="sxs-lookup"><span data-stu-id="e177d-114">To play a sound event, call **PlaySound** with the *pszSound* parameter pointing to a string containing the name of the registry entry that identifies the sound.</span></span> <span data-ttu-id="e177d-115">Ad esempio, per riprodurre il suono associato alla voce "click-through" e attendere il completamento del suono prima della restituzione, utilizzare l'istruzione seguente:</span><span class="sxs-lookup"><span data-stu-id="e177d-115">For example, to play the sound associated with the "MouseClick" entry and to wait for the sound to complete before returning, use the following statement:</span></span>


```C++
PlaySound("MouseClick", NULL, SND_SYNC); 
```



<span data-ttu-id="e177d-116">Se la voce del registro di sistema specificata o il file audio di forma d'onda identificato non esiste o se il file non rientra nella memoria disponibile, **PlaySound** riproduce il suono di sistema predefinito.</span><span class="sxs-lookup"><span data-stu-id="e177d-116">If the specified registry entry or the waveform-audio file it identifies does not exist, or if the file does not fit into the available memory, **PlaySound** plays the default system sound.</span></span>

<span data-ttu-id="e177d-117">Gli eventi audio predefiniti dal sistema possono variare in base alla piattaforma.</span><span class="sxs-lookup"><span data-stu-id="e177d-117">The sound events that are predefined by the system can vary with the platform.</span></span> <span data-ttu-id="e177d-118">L'elenco seguente fornisce gli eventi audio definiti per tutte le implementazioni dell'API Win32:</span><span class="sxs-lookup"><span data-stu-id="e177d-118">The following list gives the sound events that are defined for all implementations of the Win32 API:</span></span>

-   <span data-ttu-id="e177d-119">SystemAsterisk</span><span class="sxs-lookup"><span data-stu-id="e177d-119">SystemAsterisk</span></span>
-   <span data-ttu-id="e177d-120">SystemExclamation</span><span class="sxs-lookup"><span data-stu-id="e177d-120">SystemExclamation</span></span>
-   <span data-ttu-id="e177d-121">SystemExit</span><span class="sxs-lookup"><span data-stu-id="e177d-121">SystemExit</span></span>
-   <span data-ttu-id="e177d-122">SystemHand</span><span class="sxs-lookup"><span data-stu-id="e177d-122">SystemHand</span></span>
-   <span data-ttu-id="e177d-123">SystemQuestion</span><span class="sxs-lookup"><span data-stu-id="e177d-123">SystemQuestion</span></span>
-   <span data-ttu-id="e177d-124">SystemStart</span><span class="sxs-lookup"><span data-stu-id="e177d-124">SystemStart</span></span>

<span data-ttu-id="e177d-125">Se un'applicazione registra i propri eventi audio, l'utente può configurare l'evento audio usando l'interfaccia del pannello di controllo standard.</span><span class="sxs-lookup"><span data-stu-id="e177d-125">If an application registers its own sound events, the user can configure the sound event by using the standard Control Panel interface.</span></span> <span data-ttu-id="e177d-126">L'applicazione deve registrare l'evento audio usando le funzioni del registro di sistema standard. Per ulteriori informazioni, vedere [Registro di sistema](../sysinfo/registry.md).</span><span class="sxs-lookup"><span data-stu-id="e177d-126">The application should register the sound event by using the standard registry functions; for more information, see [Registry](../sysinfo/registry.md).</span></span> <span data-ttu-id="e177d-127">Le voci appartengono alla stessa posizione della gerarchia del registro di sistema come il resto degli eventi audio.</span><span class="sxs-lookup"><span data-stu-id="e177d-127">The entries belong at the same position in the registry hierarchy as the rest of the sound events.</span></span> <span data-ttu-id="e177d-128">Questa posizione varia in base all'implementazione di Win32.</span><span class="sxs-lookup"><span data-stu-id="e177d-128">This position varies with the Win32 implementation.</span></span> <span data-ttu-id="e177d-129">Il valore di dati appropriato varia anche con l'implementazione di.</span><span class="sxs-lookup"><span data-stu-id="e177d-129">The appropriate data value also varies with the implementation.</span></span>

<span data-ttu-id="e177d-130">La funzione [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) cerca sempre nel registro di sistema un nome di chiave corrispondente a *lpszSound* prima di provare a caricare un file con questo nome.</span><span class="sxs-lookup"><span data-stu-id="e177d-130">The [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) function always searches the registry for a keyname matching *lpszSound* before attempting to load a file with this name.</span></span> <span data-ttu-id="e177d-131">La funzione [**PlaySound**](/previous-versions//dd743680(v=vs.85)) accetta flag che specificano la posizione del suono.</span><span class="sxs-lookup"><span data-stu-id="e177d-131">The [**PlaySound**](/previous-versions//dd743680(v=vs.85)) function accepts flags that specify the location of the sound.</span></span>

 

 