---
description: API della piattaforma Media Foundation
ms.assetid: 1eb20c44-58cb-4e34-a108-1b3c27d54ff1
title: API della piattaforma Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed1e8d8aa0dcd5d7b1184a406e09910a98892f4f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320495"
---
# <a name="media-foundation-platform-apis"></a><span data-ttu-id="84265-103">API della piattaforma Media Foundation</span><span class="sxs-lookup"><span data-stu-id="84265-103">Media Foundation Platform APIs</span></span>

<span data-ttu-id="84265-104">Il livello piattaforma di Media Foundation contiene primitive e oggetti helper usati dagli altri livelli.</span><span class="sxs-lookup"><span data-stu-id="84265-104">The platform layer of Media Foundation contains primitives and helper objects used by the other layers.</span></span>

<span data-ttu-id="84265-105">Questa sezione contiene i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="84265-105">This section contains the following topics:</span></span>



| <span data-ttu-id="84265-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="84265-106">Topic</span></span>                                                                           | <span data-ttu-id="84265-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84265-107">Description</span></span>                                                                                                                                                       |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="84265-108">Inizializzazione della piattaforma Media Foundation</span><span class="sxs-lookup"><span data-stu-id="84265-108">Initializing the Media Foundation Platform</span></span>](initializing-media-foundation.md) | <span data-ttu-id="84265-109">Come inizializzare la piattaforma Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="84265-109">How to initialize the Media Foundation platform.</span></span>                                                                                                                  |
| [<span data-ttu-id="84265-110">Media Foundation e COM</span><span class="sxs-lookup"><span data-stu-id="84265-110">Media Foundation and COM</span></span>](media-foundation-and-com.md)                        | <span data-ttu-id="84265-111">Viene descritta l'interazione tra COM e Microsoft Media Foundation e vengono definite alcune procedure consigliate da utilizzare per lo sviluppo di Media Foundation componenti plug-in.</span><span class="sxs-lookup"><span data-stu-id="84265-111">Describes the interaction between COM and Microsoft Media Foundation, and defines some best practices to use when developing Media Foundation plug-in components.</span></span> |
| [<span data-ttu-id="84265-112">Metodi di callback asincroni</span><span class="sxs-lookup"><span data-stu-id="84265-112">Asynchronous Callback Methods</span></span>](asynchronous-callback-methods.md)              | <span data-ttu-id="84265-113">Come chiamare metodi asincroni e come implementare operazioni asincrone in Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="84265-113">How to call asynchronous methods and how to implement asynchronous operations in Media Foundation.</span></span>                                                                |
| [<span data-ttu-id="84265-114">Code di lavoro</span><span class="sxs-lookup"><span data-stu-id="84265-114">Work Queues</span></span>](work-queues.md)                                                  | <span data-ttu-id="84265-115">Una coda di lavoro è un modo efficiente per eseguire operazioni asincrone su un altro thread.</span><span class="sxs-lookup"><span data-stu-id="84265-115">A work queue is an efficient way to perform asynchronous operations on another thread.</span></span>                                                                            |
| [<span data-ttu-id="84265-116">Generatori di eventi multimediali</span><span class="sxs-lookup"><span data-stu-id="84265-116">Media Event Generators</span></span>](media-event-generators.md)                            | <span data-ttu-id="84265-117">Come ricevere eventi asincroni e come generare eventi in Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="84265-117">How to receive asynchronous events and how to raise events in Media Foundation.</span></span>                                                                                   |
| [<span data-ttu-id="84265-118">Interfacce del servizio</span><span class="sxs-lookup"><span data-stu-id="84265-118">Service Interfaces</span></span>](service-interfaces.md)                                    | <span data-ttu-id="84265-119">Un'interfaccia del servizio è un'interfaccia COM fornita da un oggetto, ma esposta all'applicazione tramite un altro oggetto.</span><span class="sxs-lookup"><span data-stu-id="84265-119">A service interface is a COM interface provided by one object, but exposed to the application through another object.</span></span>                                             |
| [<span data-ttu-id="84265-120">Oggetti attivazione</span><span class="sxs-lookup"><span data-stu-id="84265-120">Activation Objects</span></span>](activation-objects.md)                                    | <span data-ttu-id="84265-121">Un oggetto Activation è un oggetto che crea un altro oggetto.</span><span class="sxs-lookup"><span data-stu-id="84265-121">An activation object is an object that creates another object.</span></span>                                                                                                    |
| [<span data-ttu-id="84265-122">Orologio di presentazione</span><span class="sxs-lookup"><span data-stu-id="84265-122">Presentation Clock</span></span>](presentation-clock.md)                                    | <span data-ttu-id="84265-123">Il clock di presentazione genera il tempo di clock usato per controllare la riproduzione e anche per i flussi audio e video sincroni.</span><span class="sxs-lookup"><span data-stu-id="84265-123">The presentation clock generates the clock time that is used to control playback, and also to synchronous audio and video streams.</span></span>                                |



 

## <a name="related-topics"></a><span data-ttu-id="84265-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="84265-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84265-125">Architettura di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="84265-125">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> <dt>

[<span data-ttu-id="84265-126">Guida alla programmazione di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="84265-126">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> </dl>

 

 



