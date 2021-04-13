---
description: Informazioni sull'origine del sequencer
ms.assetid: 0d7ce9ca-9f34-4842-bd49-9211ae4454de
title: Informazioni sull'origine del sequencer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d8de3e0ff46cab1e68b767294633ecd09ebc161
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526611"
---
# <a name="about-the-sequencer-source"></a><span data-ttu-id="ab7bd-103">Informazioni sull'origine del sequencer</span><span class="sxs-lookup"><span data-stu-id="ab7bd-103">About the Sequencer Source</span></span>

<span data-ttu-id="ab7bd-104">L'origine di Sequencer consente a un'applicazione di riprodurre in sequenza una raccolta di [origini multimediali](media-sources.md) , con transizioni senza problemi tra le origini.</span><span class="sxs-lookup"><span data-stu-id="ab7bd-104">The sequencer source enables an application to play a collection of [Media Sources](media-sources.md) sequentially, with seamless transitions between the sources.</span></span> <span data-ttu-id="ab7bd-105">L'origine di Sequencer può essere usata per gli scenari seguenti:</span><span class="sxs-lookup"><span data-stu-id="ab7bd-105">The sequencer source can be used for the following scenarios:</span></span>

-   <span data-ttu-id="ab7bd-106">Creare una playlist che passa facilmente da un'origine multimediale a quella successiva.</span><span class="sxs-lookup"><span data-stu-id="ab7bd-106">Create a playlist that switches seamlessly from one media source to the next.</span></span>
-   <span data-ttu-id="ab7bd-107">Riprodurre flussi da più origini contemporaneamente; ad esempio, riprodurre l'audio da un file con il video da un altro.</span><span class="sxs-lookup"><span data-stu-id="ab7bd-107">Play streams from multiple sources simultaneously; for example, play the audio from one file with the video from another.</span></span>
-   <span data-ttu-id="ab7bd-108">Passare da un flusso all'altro in diverse origini multimediali in voci consecutive della playlist; ad esempio, una playlist può includere voci che condividono la stessa origine video mentre ogni voce contiene un'origine audio diversa.</span><span class="sxs-lookup"><span data-stu-id="ab7bd-108">Switch between streams in different media sources in consecutive playlist entries; for example, a playlist can have entries that share the same video source while each entry contains a different audio source.</span></span>

<span data-ttu-id="ab7bd-109">Per ogni elemento di una playlist, l'applicazione crea una topologia separata.</span><span class="sxs-lookup"><span data-stu-id="ab7bd-109">For each element of a playlist, the application creates a separate topology.</span></span> <span data-ttu-id="ab7bd-110">Le origini multimediali in queste topologie sono denominate *origini native*, per distinguerle dall'origine del sequencer.</span><span class="sxs-lookup"><span data-stu-id="ab7bd-110">The media sources in these topologies are referred to as *native sources*, to distinguish them from the sequencer source.</span></span> <span data-ttu-id="ab7bd-111">Durante la riproduzione, l'intera sequenza di topologie viene chiamata *presentazione* e ogni topologia all'interno della sequenza viene chiamata *segmento*.</span><span class="sxs-lookup"><span data-stu-id="ab7bd-111">During playback, the entire sequence of topologies is called a *presentation*, and each topology within the sequence is called a *segment*.</span></span>

<span data-ttu-id="ab7bd-112">La riproduzione è controllata dalla [sessione multimediale](media-session.md), che fornisce controlli di trasporto, ad esempio riproduzione, pausa e arresto.</span><span class="sxs-lookup"><span data-stu-id="ab7bd-112">Playback is controlled by the [Media Session](media-session.md), which provides transport controls, such as play, pause, and stop.</span></span> <span data-ttu-id="ab7bd-113">La sessione multimediale gestisce anche l'ora di presentazione e invia gli eventi all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ab7bd-113">The Media Session also manages the presentation time and sends events to the application.</span></span> <span data-ttu-id="ab7bd-114">(Gli eventi dell'origine di Sequencer vengono trasmessi all'applicazione tramite la sessione multimediale).</span><span class="sxs-lookup"><span data-stu-id="ab7bd-114">(Events from the sequencer source are forwarded to the application through the Media Session.)</span></span>

<span data-ttu-id="ab7bd-115">Per creare una playlist, l'applicazione crea una o più topologie di riproduzione e le accoda nell'origine del sequencer nell'ordine di riproduzione desiderato.</span><span class="sxs-lookup"><span data-stu-id="ab7bd-115">To create a playlist, the application creates one or more playback topologies and queues them on the sequencer source in the desired order of playback.</span></span> <span data-ttu-id="ab7bd-116">Internamente, l'origine del sequencer modifica le topologie in modo che i nodi di origine puntino all'origine del sequencer invece che all'origine nativa.</span><span class="sxs-lookup"><span data-stu-id="ab7bd-116">Internally, the sequencer source modifies the topologies so that the source nodes point to the sequencer source instead of the native source.</span></span> <span data-ttu-id="ab7bd-117">L'applicazione invia alla sessione multimediale le topologie modificate, anziché le topologie originali.</span><span class="sxs-lookup"><span data-stu-id="ab7bd-117">The application sends these modified topologies, rather than the original topologies, to the Media Session.</span></span> <span data-ttu-id="ab7bd-118">Ciò consente all'origine del sequencer di aggregare le origini native e di comunicare con la sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="ab7bd-118">This enables the sequencer source to aggregate the native sources and to communicate with the Media Session.</span></span>

<span data-ttu-id="ab7bd-119">Per ottenere transizioni senza problemi tra i segmenti, l'origine del Sequencer esegue il prerolling di ogni segmento.</span><span class="sxs-lookup"><span data-stu-id="ab7bd-119">To achieve seamless transitions between segments, the sequencer source prerolls each segment.</span></span> <span data-ttu-id="ab7bd-120">Mentre un segmento viene riprodotto e prima che sia il momento di riprodurre il segmento seguente, l'origine del sequencer genera un evento [MENewPresentation](menewpresentation.md) che contiene un descrittore di presentazione.</span><span class="sxs-lookup"><span data-stu-id="ab7bd-120">While one segment is playing, and before it is time to play the following segment, the sequencer source fires an [MENewPresentation](menewpresentation.md) event that contains a presentation descriptor.</span></span> <span data-ttu-id="ab7bd-121">L'applicazione utilizza questo descrittore di presentazione per ottenere la topologia per il segmento successivo nella presentazione e accoda la topologia nella sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="ab7bd-121">The application uses this presentation descriptor to get the topology for the next segment in the presentation, and queues the topology on the Media Session.</span></span>

<span data-ttu-id="ab7bd-122">Nella figura seguente viene illustrato il flusso di dati per le voci della playlist tramite l'origine del sequencer.</span><span class="sxs-lookup"><span data-stu-id="ab7bd-122">The following illustration shows the data flow for playlist entries through the sequencer source.</span></span> <span data-ttu-id="ab7bd-123">L'applicazione utilizza il resolver di origine per creare le origini native, compila le topologie per ogni segmento e accoda le topologie nell'origine del sequencer.</span><span class="sxs-lookup"><span data-stu-id="ab7bd-123">The application uses the source resolver to create the native sources, builds topologies for each segment, and queues the topologies on the sequencer source.</span></span>

![diagramma che mostra il flusso di dati dei segmenti imfmediasession, imfsequencersource e playlist che portano a IMFMediaSource](images/dbf41a05-d8cc-4502-9cd3-74e5d1ce04a0.gif)

## <a name="related-topics"></a><span data-ttu-id="ab7bd-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ab7bd-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab7bd-126">Come creare una playlist</span><span class="sxs-lookup"><span data-stu-id="ab7bd-126">How to Create a Playlist</span></span>](how-to-create-a-playlist.md)
</dt> <dt>

[<span data-ttu-id="ab7bd-127">Topologie</span><span class="sxs-lookup"><span data-stu-id="ab7bd-127">Topologies</span></span>](topologies.md)
</dt> <dt>

[<span data-ttu-id="ab7bd-128">Utilizzo dell'origine sequencer</span><span class="sxs-lookup"><span data-stu-id="ab7bd-128">Using the Sequencer Source</span></span>](using-the-sequencer-source.md)
</dt> <dt>

[<span data-ttu-id="ab7bd-129">Origine sequencer</span><span class="sxs-lookup"><span data-stu-id="ab7bd-129">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 



