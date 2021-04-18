---
description: Questa sezione descrive come implementare la riproduzione audio/video nell'applicazione usando Microsoft Media Foundation.
ms.assetid: 6efadfe6-013a-4942-9df5-bed557d9af8b
title: Riproduzione di audio/video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6781c531bc7e5c595125d5353a381cc44c08fd5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305514"
---
# <a name="audiovideo-playback"></a><span data-ttu-id="fd618-103">Riproduzione di audio/video</span><span class="sxs-lookup"><span data-stu-id="fd618-103">Audio/Video Playback</span></span>

<span data-ttu-id="fd618-104">Questa sezione descrive come implementare la riproduzione audio/video nell'applicazione usando Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="fd618-104">This section describes how to implement audio/video playback in your application, using Microsoft Media Foundation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="fd618-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="fd618-105">In this section</span></span>



| <span data-ttu-id="fd618-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="fd618-106">Topic</span></span>                                                                                               | <span data-ttu-id="fd618-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fd618-107">Description</span></span>                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fd618-108">Come riprodurre file multimediali con Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fd618-108">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)<br/> | <span data-ttu-id="fd618-109">Questa esercitazione illustra come riprodurre file multimediali usando l'oggetto della [sessione multimediale](media-session.md) .</span><span class="sxs-lookup"><span data-stu-id="fd618-109">This tutorial shows how to play media files using the [Media Session](media-session.md) object.</span></span> <br/>                                 |
| [<span data-ttu-id="fd618-110">Come riprodurre file multimediali protetti</span><span class="sxs-lookup"><span data-stu-id="fd618-110">How to Play Protected Media Files</span></span>](how-to-play-protected-media-files.md)<br/>               | <span data-ttu-id="fd618-111">Come riprodurre file che contengono supporti protetti da DRM.</span><span class="sxs-lookup"><span data-stu-id="fd618-111">How to play files that contain DRM-protected media.</span></span><br/>                                                                               |
| [<span data-ttu-id="fd618-112">Come individuare la durata di un file multimediale</span><span class="sxs-lookup"><span data-stu-id="fd618-112">How to Find the Duration of a Media File</span></span>](how-to-find-the-duration-of-a-media-file.md)<br/> | <span data-ttu-id="fd618-113">Come individuare la durata di un file multimediale.</span><span class="sxs-lookup"><span data-stu-id="fd618-113">How to find the duration of a media file.</span></span><br/>                                                                                         |
| [<span data-ttu-id="fd618-114">Ricerca, avanzamento rapido e riproduzione inversa</span><span class="sxs-lookup"><span data-stu-id="fd618-114">Seeking, Fast Forward, and Reverse Play</span></span>](seeking--fast-forward--and-reverse-play.md)<br/>   | <span data-ttu-id="fd618-115">Questo argomento illustra il codice di esempio per gestire la ricerca e la frequenza delle modifiche, quando si usa la [sessione multimediale](media-session.md) per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="fd618-115">This topic shows example code to manage seeking and rate changes, when using the [Media Session](media-session.md) for playback.</span></span><br/> |
| [<span data-ttu-id="fd618-116">Come impostare l'ora di arresto della riproduzione</span><span class="sxs-lookup"><span data-stu-id="fd618-116">How to Set the Playback Stop Time</span></span>](how-to-set-the-playback-stop-time-.md)<br/>              | <span data-ttu-id="fd618-117">Questo argomento descrive come impostare un'ora di arresto per la riproduzione quando si usa la [sessione multimediale](media-session.md).</span><span class="sxs-lookup"><span data-stu-id="fd618-117">This topic describes how to set a stop time for playback when using the [Media Session](media-session.md).</span></span><br/>                       |
| [<span data-ttu-id="fd618-118">Renderer video migliorato</span><span class="sxs-lookup"><span data-stu-id="fd618-118">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)<br/>                                   | <span data-ttu-id="fd618-119">Il renderer video avanzato (EVR) è un componente che Visualizza il video sul monitor dell'utente.</span><span class="sxs-lookup"><span data-stu-id="fd618-119">The enhanced video renderer (EVR) is a component that displays video on the user's monitor.</span></span><br/>                                       |
| [<span data-ttu-id="fd618-120">Renderer audio di streaming</span><span class="sxs-lookup"><span data-stu-id="fd618-120">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)<br/>                                 | <span data-ttu-id="fd618-121">Il renderer di streaming audio (SAR) è un sink multimediale che esegue il rendering dell'audio.</span><span class="sxs-lookup"><span data-stu-id="fd618-121">The streaming audio renderer (SAR) is a media sink that renders audio.</span></span><br/>                                                            |
| [<span data-ttu-id="fd618-122">MFPlay</span><span class="sxs-lookup"><span data-stu-id="fd618-122">MFPlay</span></span>](using-mfplay-for-audio-video-playback.md)<br/>                                      | <span data-ttu-id="fd618-123">L'API MFPlay è deprecata.</span><span class="sxs-lookup"><span data-stu-id="fd618-123">The MFPlay API is deprecated.</span></span><br/>                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="fd618-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fd618-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd618-125">Architettura di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fd618-125">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> <dt>

[<span data-ttu-id="fd618-126">Guida alla programmazione di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fd618-126">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> <dt>

[<span data-ttu-id="fd618-127">Supporto MPEG-4 in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fd618-127">MPEG-4 Support in Media Foundation</span></span>](mpeg-4-support-in-media-foundation.md)
</dt> </dl>

 

 




