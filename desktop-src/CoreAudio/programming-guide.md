---
description: Informazioni sui concetti e sulle funzionalità delle API audio principali di Windows Vista e su come usarle nella programmazione di applicazioni.
ms.assetid: 825c7cd7-dc66-47b6-a1b6-d10101daebb3
title: Guida alla programmazione audio di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02f02e27206c70cca69abf263cfa49dfd439c480
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405874"
---
# <a name="core-audio-programming-guide"></a><span data-ttu-id="b12e7-103">Guida alla programmazione audio di base</span><span class="sxs-lookup"><span data-stu-id="b12e7-103">Core Audio Programming Guide</span></span>

<span data-ttu-id="b12e7-104">Questa sezione della guida illustra i concetti e le funzionalità delle API audio di base di Windows Vista e descrive come usarle nella programmazione di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="b12e7-104">This guide section explains the concepts and features of the core audio APIs of Windows Vista, and describes how to use them in application programming.</span></span>

<span data-ttu-id="b12e7-105">In questa sezione vengono trattati gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="b12e7-105">This section contains the following topics.</span></span>



| <span data-ttu-id="b12e7-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="b12e7-106">Topic</span></span>                                                                                                                      | <span data-ttu-id="b12e7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b12e7-107">Description</span></span>                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b12e7-108">Componenti audio in modalità utente</span><span class="sxs-lookup"><span data-stu-id="b12e7-108">User-Mode Audio Components</span></span>](user-mode-audio-components.md)                                                               | <span data-ttu-id="b12e7-109">Tramite le interfacce di basso livello nelle API audio di base, un client può accedere ai componenti di sistema che gestiscono e combinano flussi audio.</span><span class="sxs-lookup"><span data-stu-id="b12e7-109">Through the low-level interfaces in the core audio APIs, a client can access the system components that manage and mix audio streams.</span></span>                                                                        |
| [<span data-ttu-id="b12e7-110">PuMA (Protected User Mode Audio)</span><span class="sxs-lookup"><span data-stu-id="b12e7-110">Protected User Mode Audio (PUMA)</span></span>](protected-user-mode-audio--puma-.md)                                                   | <span data-ttu-id="b12e7-111">Descrive gli aggiornamenti di PUMA (Protected User Mode Audio), il motore audio in modalità utente nell'ambiente protetto (PE), che offre un ambiente più sicuro per l'elaborazione e il rendering audio.</span><span class="sxs-lookup"><span data-stu-id="b12e7-111">Describes the updates to Protected User Mode Audio (PUMA), the user-mode audio engine in the Protected Environment (PE), which provides a safer environment for audio processing and rendering.</span></span>              |
| [<span data-ttu-id="b12e7-112">Dispositivi endpoint audio</span><span class="sxs-lookup"><span data-stu-id="b12e7-112">Audio Endpoint Devices</span></span>](audio-endpoint-devices.md)                                                                       | <span data-ttu-id="b12e7-113">Un dispositivo endpoint audio è un'astrazione software che consente interazioni descrittive con dispositivi audio, ad esempio microfoni e altoparlanti.</span><span class="sxs-lookup"><span data-stu-id="b12e7-113">An audio endpoint device is a software abstraction that enables user-friendly interactions with audio devices such as microphones and speakers.</span></span>                                                              |
| [<span data-ttu-id="b12e7-114">Sessioni audio</span><span class="sxs-lookup"><span data-stu-id="b12e7-114">Audio Sessions</span></span>](audio-sessions.md)                                                                                       | <span data-ttu-id="b12e7-115">Una sessione audio è un'astrazione software che consente a un client di gestire una raccolta di flussi audio correlati come singola unità.</span><span class="sxs-lookup"><span data-stu-id="b12e7-115">An audio session is a software abstraction that enables a client to manage a collection of related audio streams as a single unit.</span></span>                                                                           |
| [<span data-ttu-id="b12e7-116">Controlli del volume</span><span class="sxs-lookup"><span data-stu-id="b12e7-116">Volume Controls</span></span>](volume-controls.md)                                                                                     | <span data-ttu-id="b12e7-117">Il sistema integra le impostazioni del volume basate su criteri con le impostazioni del volume dell'utente in modo logico e coerente.</span><span class="sxs-lookup"><span data-stu-id="b12e7-117">The system integrates its policy-based volume settings with the user's volume settings in a logical and consistent way.</span></span>                                                                                      |
| [<span data-ttu-id="b12e7-118">Gestione dei flussi</span><span class="sxs-lookup"><span data-stu-id="b12e7-118">Stream Management</span></span>](stream-management.md)                                                                                 | <span data-ttu-id="b12e7-119">L'API della sessione audio di Windows (WASAPI) fornisce a un client un set completo di metodi per la creazione e la gestione dei flussi audio.</span><span class="sxs-lookup"><span data-stu-id="b12e7-119">The Windows Audio Session API (WASAPI) provides a client with a complete set of methods for creating and managing audio streams.</span></span>                                                                             |
| [<span data-ttu-id="b12e7-120">Topologie di dispositivi</span><span class="sxs-lookup"><span data-stu-id="b12e7-120">Device Topologies</span></span>](device-topologies.md)                                                                                 | <span data-ttu-id="b12e7-121">L'API DeviceTopology consente a un client di individuare i controlli audio che si trovano lungo i vari percorsi dati nell'hardware audio.</span><span class="sxs-lookup"><span data-stu-id="b12e7-121">The DeviceTopology API enables a client to discover the audio controls that lie along the various data paths in the audio hardware.</span></span>                                                                          |
| [<span data-ttu-id="b12e7-122">Uso dell'interfaccia IKsControl per accedere alle proprietà audio</span><span class="sxs-lookup"><span data-stu-id="b12e7-122">Using the IKsControl Interface to Access Audio Properties</span></span>](using-the-ikscontrol-interface-to-access-audio-properties.md) | <span data-ttu-id="b12e7-123">Un'applicazione audio specializzata potrebbe dover usare l'interfaccia IKsControl per accedere alle proprietà di un adattatore audio.</span><span class="sxs-lookup"><span data-stu-id="b12e7-123">A specialized audio application might need to use the IKsControl interface to access the properties of an audio adapter.</span></span>                                                                                     |
| [<span data-ttu-id="b12e7-124">Interoperabilità con LE API audio legacy</span><span class="sxs-lookup"><span data-stu-id="b12e7-124">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)                                     | <span data-ttu-id="b12e7-125">Le funzionalità principali delle API audio principali in Windows Vista possono essere incorporate nelle applicazioni esistenti che usano DirectSound, DirectShow e le funzioni **waveOutXxx** e **waveInXxx** multimediali di Windows.</span><span class="sxs-lookup"><span data-stu-id="b12e7-125">Key features of the core audio APIs in Windows Vista can be incorporated into existing applications that use DirectSound, DirectShow, and the Windows multimedia **waveOutXxx** and **waveInXxx** functions.</span></span> |
| [<span data-ttu-id="b12e7-126">Audio spaziale</span><span class="sxs-lookup"><span data-stu-id="b12e7-126">Spatial Sound</span></span>](spatial-sound.md)                                                                                         | <span data-ttu-id="b12e7-127">Fornisce indicazioni per l'uso di Windows Sonic, la soluzione microsoft a livello di piattaforma per il supporto dell'audio spaziale in Xbox e Windows, abilitando segnali audio sia di surround che di elevazione (sopra o sotto il listener).</span><span class="sxs-lookup"><span data-stu-id="b12e7-127">Provides guidance for using Windows Sonic, Microsoft’s platform-level solution for spatial sound support on Xbox and Windows, enabling both surround and elevation (above or below the listener) audio cues.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b12e7-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b12e7-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b12e7-129">API audio di base</span><span class="sxs-lookup"><span data-stu-id="b12e7-129">Core Audio APIs</span></span>](core-audio-apis-in-windows-vista.md)
</dt> </dl>

 

 



