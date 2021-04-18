---
description: La sessione multimediale è un oggetto che gestisce il flusso di dati nella pipeline. Può essere usato sia per la riproduzione che per la codifica dei file.
ms.assetid: dac99908-be90-415d-8837-2f97d573feb5
title: Sessione multimediale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3df4597e5461788f990f620875bce946570ab97
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320747"
---
# <a name="media-session"></a><span data-ttu-id="40ca2-104">Sessione multimediale</span><span class="sxs-lookup"><span data-stu-id="40ca2-104">Media Session</span></span>

<span data-ttu-id="40ca2-105">La sessione multimediale è un oggetto che gestisce il flusso di dati nella pipeline.</span><span class="sxs-lookup"><span data-stu-id="40ca2-105">The Media Session is an object that manages data flow in the pipeline.</span></span> <span data-ttu-id="40ca2-106">Può essere usato sia per la riproduzione che per la codifica dei file.</span><span class="sxs-lookup"><span data-stu-id="40ca2-106">It can be used for both playing and encoding files.</span></span>

<span data-ttu-id="40ca2-107">Questa sezione descrive la sessione multimediale da un punto di vista dell'architettura.</span><span class="sxs-lookup"><span data-stu-id="40ca2-107">This section describes the Media Session from an architectural standpoint.</span></span> <span data-ttu-id="40ca2-108">Contiene le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="40ca2-108">It contains the following sections:</span></span>



| <span data-ttu-id="40ca2-109">Argomento</span><span class="sxs-lookup"><span data-stu-id="40ca2-109">Topic</span></span>                                                                                        | <span data-ttu-id="40ca2-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="40ca2-110">Description</span></span>                                                                                                                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="40ca2-111">Informazioni sulla sessione multimediale</span><span class="sxs-lookup"><span data-stu-id="40ca2-111">About the Media Session</span></span>](about-the-media-session.md)                                       | <span data-ttu-id="40ca2-112">Viene fornita una panoramica della sessione multimediale, il modo in cui un'applicazione può creare la sessione multimediale e il modo in cui la sessione multimediale gestisce il tempo di presentazione.</span><span class="sxs-lookup"><span data-stu-id="40ca2-112">Provides an overview of the Media Session, how an application can create the Media Session, and how the Media Session manages presentation time.</span></span> |
| [<span data-ttu-id="40ca2-113">Topologie</span><span class="sxs-lookup"><span data-stu-id="40ca2-113">Topologies</span></span>](topologies.md)                                                                 | <span data-ttu-id="40ca2-114">Una topologia è un oggetto che rappresenta il flusso di dati nella pipeline.</span><span class="sxs-lookup"><span data-stu-id="40ca2-114">A topology is an object that represents the flow of data in the pipeline.</span></span>                                                                        |
| [<span data-ttu-id="40ca2-115">Eventi della sessione multimediale</span><span class="sxs-lookup"><span data-stu-id="40ca2-115">Media Session Events</span></span>](media-session-events.md)                                             | <span data-ttu-id="40ca2-116">Descrive gli eventi che un'applicazione può ricevere dalla sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="40ca2-116">Describes the events that an application might receive from the Media Session.</span></span>                                                                   |
| [<span data-ttu-id="40ca2-117">Come controllare gli Stati di presentazione</span><span class="sxs-lookup"><span data-stu-id="40ca2-117">How to Control Presentation States</span></span>](how-to-control-presentation-states.md)                 | <span data-ttu-id="40ca2-118">Descrive i controlli di trasporto della sessione multimediale: Play, pause e stop.</span><span class="sxs-lookup"><span data-stu-id="40ca2-118">Describes the Media Session transport controls: Play, Pause, and Stop.</span></span>                                                                           |
| [<span data-ttu-id="40ca2-119">Uso di origini multimediali con la sessione multimediale</span><span class="sxs-lookup"><span data-stu-id="40ca2-119">Using Media Sources with the Media Session</span></span>](using-media-sources-with-the-media-session.md) | <span data-ttu-id="40ca2-120">Come usare le origini multimediali con la sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="40ca2-120">How to use media sources with the Media Session.</span></span>                                                                                                 |
| [<span data-ttu-id="40ca2-121">Controllo della frequenza</span><span class="sxs-lookup"><span data-stu-id="40ca2-121">Rate Control</span></span>](rate-control.md)                                                             | <span data-ttu-id="40ca2-122">Viene descritto come controllare la velocità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="40ca2-122">Describes how to control playback rate.</span></span>                                                                                                          |
| [<span data-ttu-id="40ca2-123">Gestione della qualità dei video</span><span class="sxs-lookup"><span data-stu-id="40ca2-123">Video Quality Management</span></span>](video-quality-management.md)                                     | <span data-ttu-id="40ca2-124">Vengono descritti i miglioramenti apportati alla pipeline video in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="40ca2-124">Describes improvements to the video pipeline in Windows 7.</span></span>                                                                                       |
| [<span data-ttu-id="40ca2-125">Sessione multimediale PMP</span><span class="sxs-lookup"><span data-stu-id="40ca2-125">PMP Media Session</span></span>](pmp-media-session.md)                                                   | <span data-ttu-id="40ca2-126">Viene descritto come creare la sessione multimediale all'interno di un processo del percorso multimediale protetto (PMP).</span><span class="sxs-lookup"><span data-stu-id="40ca2-126">Describes how to create the Media Session inside a Protected Media Path (PMP) process.</span></span>                                                           |



 

<span data-ttu-id="40ca2-127">Negli argomenti seguenti viene descritto come usare la sessione multimediale in scenari di applicazioni specifici:</span><span class="sxs-lookup"><span data-stu-id="40ca2-127">The following topics describe how to use the Media Session in specific application scenarios:</span></span>

-   [<span data-ttu-id="40ca2-128">Riproduzione di audio/video</span><span class="sxs-lookup"><span data-stu-id="40ca2-128">Audio/Video Playback</span></span>](audio-video-playback.md)
-   [<span data-ttu-id="40ca2-129">Codifica e creazione di file</span><span class="sxs-lookup"><span data-stu-id="40ca2-129">Encoding and File Authoring</span></span>](encoding-and-file-authoring.md)

## <a name="related-topics"></a><span data-ttu-id="40ca2-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="40ca2-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40ca2-131">Architettura di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="40ca2-131">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> <dt>

[<span data-ttu-id="40ca2-132">**IMFMediaSession**</span><span class="sxs-lookup"><span data-stu-id="40ca2-132">**IMFMediaSession**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)
</dt> </dl>

 

 



