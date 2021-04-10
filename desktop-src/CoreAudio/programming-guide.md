---
description: Guida per programmatori
ms.assetid: 825c7cd7-dc66-47b6-a1b6-d10101daebb3
title: Guida per programmatori audio Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb99369058983ebac7205053efdf967bbb8c36d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225758"
---
# <a name="core-audio-programming-guide"></a><span data-ttu-id="b9d30-103">Guida per programmatori audio Core</span><span class="sxs-lookup"><span data-stu-id="b9d30-103">Core Audio Programming Guide</span></span>

<span data-ttu-id="b9d30-104">In questa sezione della guida vengono illustrati i concetti e le funzionalità delle principali API audio di Windows Vista e viene descritto come utilizzarli nella programmazione delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="b9d30-104">This guide section explains the concepts and features of the core audio APIs of Windows Vista, and describes how to use them in application programming.</span></span>

<span data-ttu-id="b9d30-105">In questa sezione vengono trattati gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="b9d30-105">This section contains the following topics.</span></span>



| <span data-ttu-id="b9d30-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="b9d30-106">Topic</span></span>                                                                                                                      | <span data-ttu-id="b9d30-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9d30-107">Description</span></span>                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b9d30-108">Componenti audio in modalità utente</span><span class="sxs-lookup"><span data-stu-id="b9d30-108">User-Mode Audio Components</span></span>](user-mode-audio-components.md)                                                               | <span data-ttu-id="b9d30-109">Attraverso le interfacce di basso livello nelle API di base audio, un client può accedere ai componenti di sistema che gestiscono e combinano i flussi audio.</span><span class="sxs-lookup"><span data-stu-id="b9d30-109">Through the low-level interfaces in the core audio APIs, a client can access the system components that manage and mix audio streams.</span></span>                                                                        |
| [<span data-ttu-id="b9d30-110">Audio modalità utente protetto (PUMA)</span><span class="sxs-lookup"><span data-stu-id="b9d30-110">Protected User Mode Audio (PUMA)</span></span>](protected-user-mode-audio--puma-.md)                                                   | <span data-ttu-id="b9d30-111">Vengono descritti gli aggiornamenti dell'audio in modalità utente protetto (PUMA), il motore audio in modalità utente nell'ambiente protetto (PE), che fornisce un ambiente più sicuro per l'elaborazione e il rendering audio.</span><span class="sxs-lookup"><span data-stu-id="b9d30-111">Describes the updates to Protected User Mode Audio (PUMA), the user-mode audio engine in the Protected Environment (PE), which provides a safer environment for audio processing and rendering.</span></span>              |
| [<span data-ttu-id="b9d30-112">Dispositivi endpoint audio</span><span class="sxs-lookup"><span data-stu-id="b9d30-112">Audio Endpoint Devices</span></span>](audio-endpoint-devices.md)                                                                       | <span data-ttu-id="b9d30-113">Un dispositivo endpoint audio è un'astrazione del software che consente interazioni intuitive con dispositivi audio come microfoni e altoparlanti.</span><span class="sxs-lookup"><span data-stu-id="b9d30-113">An audio endpoint device is a software abstraction that enables user-friendly interactions with audio devices such as microphones and speakers.</span></span>                                                              |
| [<span data-ttu-id="b9d30-114">Sessioni audio</span><span class="sxs-lookup"><span data-stu-id="b9d30-114">Audio Sessions</span></span>](audio-sessions.md)                                                                                       | <span data-ttu-id="b9d30-115">Una sessione audio è un'astrazione del software che consente a un client di gestire una raccolta di flussi audio correlati come una singola unità.</span><span class="sxs-lookup"><span data-stu-id="b9d30-115">An audio session is a software abstraction that enables a client to manage a collection of related audio streams as a single unit.</span></span>                                                                           |
| [<span data-ttu-id="b9d30-116">Controlli del volume</span><span class="sxs-lookup"><span data-stu-id="b9d30-116">Volume Controls</span></span>](volume-controls.md)                                                                                     | <span data-ttu-id="b9d30-117">Il sistema integra le impostazioni dei volumi basate su criteri con le impostazioni del volume dell'utente in modo logico e coerente.</span><span class="sxs-lookup"><span data-stu-id="b9d30-117">The system integrates its policy-based volume settings with the user's volume settings in a logical and consistent way.</span></span>                                                                                      |
| [<span data-ttu-id="b9d30-118">Gestione dei flussi</span><span class="sxs-lookup"><span data-stu-id="b9d30-118">Stream Management</span></span>](stream-management.md)                                                                                 | <span data-ttu-id="b9d30-119">L'API di sessione audio di Windows (WASAPI) fornisce un client con un set completo di metodi per la creazione e la gestione di flussi audio.</span><span class="sxs-lookup"><span data-stu-id="b9d30-119">The Windows Audio Session API (WASAPI) provides a client with a complete set of methods for creating and managing audio streams.</span></span>                                                                             |
| [<span data-ttu-id="b9d30-120">Topologie del dispositivo</span><span class="sxs-lookup"><span data-stu-id="b9d30-120">Device Topologies</span></span>](device-topologies.md)                                                                                 | <span data-ttu-id="b9d30-121">L'API DeviceTopology consente a un client di individuare i controlli audio che si trovano lungo i vari percorsi dati nell'hardware audio.</span><span class="sxs-lookup"><span data-stu-id="b9d30-121">The DeviceTopology API enables a client to discover the audio controls that lie along the various data paths in the audio hardware.</span></span>                                                                          |
| [<span data-ttu-id="b9d30-122">Uso dell'interfaccia IKsControl per accedere alle proprietà audio</span><span class="sxs-lookup"><span data-stu-id="b9d30-122">Using the IKsControl Interface to Access Audio Properties</span></span>](using-the-ikscontrol-interface-to-access-audio-properties.md) | <span data-ttu-id="b9d30-123">Un'applicazione audio specializzata potrebbe dover utilizzare l'interfaccia IKsControl per accedere alle proprietà di una scheda audio.</span><span class="sxs-lookup"><span data-stu-id="b9d30-123">A specialized audio application might need to use the IKsControl interface to access the properties of an audio adapter.</span></span>                                                                                     |
| [<span data-ttu-id="b9d30-124">Interoperabilità con le API audio legacy</span><span class="sxs-lookup"><span data-stu-id="b9d30-124">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)                                     | <span data-ttu-id="b9d30-125">Le funzionalità principali delle API audio di base di Windows Vista possono essere incorporate in applicazioni esistenti che utilizzano le funzioni DirectSound, DirectShow e Windows Multimedia **waveOutXxx** e **waveInXxx** .</span><span class="sxs-lookup"><span data-stu-id="b9d30-125">Key features of the core audio APIs in Windows Vista can be incorporated into existing applications that use DirectSound, DirectShow, and the Windows multimedia **waveOutXxx** and **waveInXxx** functions.</span></span> |
| [<span data-ttu-id="b9d30-126">Audio spaziale</span><span class="sxs-lookup"><span data-stu-id="b9d30-126">Spatial Sound</span></span>](spatial-sound.md)                                                                                         | <span data-ttu-id="b9d30-127">Vengono fornite informazioni aggiuntive per l'utilizzo di Windows Sonic, la soluzione a livello di piattaforma Microsoft per il supporto di suoni spaziali in Xbox e Windows, che consente l'uso di segnali audio sia per l'elevazione (sopra o sotto il listener).</span><span class="sxs-lookup"><span data-stu-id="b9d30-127">Provides guidance for using Windows Sonic, Microsoft’s platform-level solution for spatial sound support on Xbox and Windows, enabling both surround and elevation (above or below the listener) audio cues.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b9d30-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b9d30-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9d30-129">API audio Core</span><span class="sxs-lookup"><span data-stu-id="b9d30-129">Core Audio APIs</span></span>](core-audio-apis-in-windows-vista.md)
</dt> </dl>

 

 



