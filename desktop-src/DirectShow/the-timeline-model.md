---
description: Modello di sequenza temporale
ms.assetid: 53e782a2-0fab-46b4-b029-20017d9905bd
title: Modello di sequenza temporale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac01f90e8ca827bde41f2ad36e1ab32b3d429437
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104549802"
---
# <a name="the-timeline-model"></a><span data-ttu-id="03639-103">Modello di sequenza temporale</span><span class="sxs-lookup"><span data-stu-id="03639-103">The Timeline Model</span></span>

<span data-ttu-id="03639-104">\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]</span><span class="sxs-lookup"><span data-stu-id="03639-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="03639-105">Una *sequenza temporale* è un oggetto usato da [DirectShow editing Services](directshow-editing-services.md) (des) per rappresentare un progetto di modifica video.</span><span class="sxs-lookup"><span data-stu-id="03639-105">A *timeline* is an object that [DirectShow Editing Services](directshow-editing-services.md) (DES) uses to represent a video editing project.</span></span> <span data-ttu-id="03639-106">Un progetto di modifica viene avviato come raccolta di clip di origine, estratti da file video, file audio o file di immagine ancora.</span><span class="sxs-lookup"><span data-stu-id="03639-106">An editing project starts as a collection of source clips, taken from video files, sound files, or still image files.</span></span> <span data-ttu-id="03639-107">Una sequenza lineare di clip costituisce una *traccia*. In DirectShow editing Services (DES), audio e video vengono posizionati in tracce separate.</span><span class="sxs-lookup"><span data-stu-id="03639-107">A linear sequence of clips forms a *track*. In DirectShow Editing Services (DES), audio and video are placed in separate tracks.</span></span>

<span data-ttu-id="03639-108">Le tracce possono anche essere sovrapposte.</span><span class="sxs-lookup"><span data-stu-id="03639-108">Tracks can also be layered.</span></span> <span data-ttu-id="03639-109">Più tracce audio vengono combinate insieme e possono includere effetti audio, ad esempio Fades o Reverb.</span><span class="sxs-lookup"><span data-stu-id="03639-109">Multiple audio tracks are mixed together, and might include audio effects, such as fades or reverb.</span></span> <span data-ttu-id="03639-110">Per la creazione di transizioni vengono usate più tracce video.</span><span class="sxs-lookup"><span data-stu-id="03639-110">Multiple video tracks are used to create transitions.</span></span> <span data-ttu-id="03639-111">Ad esempio, è possibile creare una cancellazione da un clip a un altro.</span><span class="sxs-lookup"><span data-stu-id="03639-111">For example, you can create a wipe from one clip to another.</span></span> <span data-ttu-id="03639-112">Un altro esempio è una chiave Chroma, in cui lo sfondo di una clip viene dismesso e sostituito da un'altra traccia. (Il Forecaster Meteo davanti a un'immagine satellite è un esempio di chiave Chroma).</span><span class="sxs-lookup"><span data-stu-id="03639-112">Another example is a chroma key, in which the background of one clip is keyed out and replaced by a different track. (The weather forecaster in front of a satelite image is an example of chroma keying.)</span></span>

<span data-ttu-id="03639-113">DES usa una struttura ad albero per rappresentare una modifica:</span><span class="sxs-lookup"><span data-stu-id="03639-113">DES uses a tree structure to represent an editing:</span></span>

-   <span data-ttu-id="03639-114">I clip audio e video formano i nodi foglia o gli oggetti di *origine* .</span><span class="sxs-lookup"><span data-stu-id="03639-114">Audio and video clips form the leaf nodes, or *source* objects.</span></span>
-   <span data-ttu-id="03639-115">Una raccolta di origini con un tipo di supporto uniforme (audio o video) è una *traccia*.</span><span class="sxs-lookup"><span data-stu-id="03639-115">A collection of sources with a uniform media type (audio or video) is a *track*.</span></span>
-   <span data-ttu-id="03639-116">Una raccolta di tracce è una *composizione*.</span><span class="sxs-lookup"><span data-stu-id="03639-116">A collection of tracks is a *composition*.</span></span> <span data-ttu-id="03639-117">Viene eseguito il rendering di una composizione come composto di tutte le tracce in esso contenute.</span><span class="sxs-lookup"><span data-stu-id="03639-117">A composition is rendered as the composite of all the tracks it contains.</span></span> <span data-ttu-id="03639-118">Le composizioni possono contenere altre composizioni, che consentono di organizzare in modo complesso le tracce.</span><span class="sxs-lookup"><span data-stu-id="03639-118">Compositions can contain other compositions, which allows for complex arrangements of tracks.</span></span>
-   <span data-ttu-id="03639-119">Una raccolta di livello superiore di composizioni e tracce (tutti che rappresentano lo stesso tipo di supporto) è un *gruppo*.</span><span class="sxs-lookup"><span data-stu-id="03639-119">A top-level collection of compositions and tracks (all representing the same media type) is a *group*.</span></span>
-   <span data-ttu-id="03639-120">Un set di uno o più gruppi costituisce una *sequenza temporale*.</span><span class="sxs-lookup"><span data-stu-id="03639-120">A set of one or more groups forms a *timeline*.</span></span> <span data-ttu-id="03639-121">La sequenza temporale è il nodo radice nell'albero.</span><span class="sxs-lookup"><span data-stu-id="03639-121">The timeline is the root node in the tree.</span></span>

<span data-ttu-id="03639-122">Una sequenza temporale deve contenere almeno un gruppo.</span><span class="sxs-lookup"><span data-stu-id="03639-122">A timeline must contain at least one group.</span></span> <span data-ttu-id="03639-123">Ogni gruppo rappresenta un singolo flusso nell'ambiente di produzione finale.</span><span class="sxs-lookup"><span data-stu-id="03639-123">Each group represents a single stream in the final production.</span></span> <span data-ttu-id="03639-124">Un progetto tipico include un gruppo video e un gruppo audio.</span><span class="sxs-lookup"><span data-stu-id="03639-124">A typical project includes one video group and one audio group.</span></span> <span data-ttu-id="03639-125">Le composizioni sono facoltative; esistono per fornire una maggiore struttura, se necessario.</span><span class="sxs-lookup"><span data-stu-id="03639-125">Compositions are optional; they exist to provide more structure if needed.</span></span>

<span data-ttu-id="03639-126">Nella figura seguente sono illustrate le relazioni padre-figlio che costituiscono una sequenza temporale:</span><span class="sxs-lookup"><span data-stu-id="03639-126">The following illustration shows the child-parent relations that make up a timeline:</span></span>

![struttura del nodo](images/timeline1.png)

<span data-ttu-id="03639-128">Di seguito viene illustrata una sequenza temporale come sequenza temporale:</span><span class="sxs-lookup"><span data-stu-id="03639-128">The following shows a timeline as a temporal sequence:</span></span>

![illustrazione della sequenza temporale](images/timeline2.png)

<span data-ttu-id="03639-130">La freccia nella parte superiore rappresenta la direzione della sequenza temporale, a partire dal tempo zero.</span><span class="sxs-lookup"><span data-stu-id="03639-130">The arrow at the top represents the direction of the timeline, starting from time zero.</span></span> <span data-ttu-id="03639-131">All'interno del gruppo video, Track 1 ha una priorità più alta rispetto a Track 0.</span><span class="sxs-lookup"><span data-stu-id="03639-131">Within the video group, track 1 has a higher priority than track 0.</span></span> <span data-ttu-id="03639-132">Gli oggetti di origine in Track 1 nascondono quelli nella traccia 0.</span><span class="sxs-lookup"><span data-stu-id="03639-132">The source objects in track 1 obscure those in track 0.</span></span> <span data-ttu-id="03639-133">Dove Track 1 è vuoto, Track 0 "shows through".</span><span class="sxs-lookup"><span data-stu-id="03639-133">Where track 1 is empty, track 0 "shows through."</span></span> <span data-ttu-id="03639-134">Come indicato in precedenza, le tracce audio sono semplicemente combinate.</span><span class="sxs-lookup"><span data-stu-id="03639-134">As mentioned earlier, audio tracks are simply mixed together.</span></span>

## <a name="related-topics"></a><span data-ttu-id="03639-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="03639-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03639-136">Introduzione con i servizi di modifica DirectShow</span><span class="sxs-lookup"><span data-stu-id="03639-136">Getting Started with DirectShow Editing Services</span></span>](getting-started-with-directshow-editing-services.md)
</dt> <dt>

[<span data-ttu-id="03639-137">Creazione di una sequenza temporale</span><span class="sxs-lookup"><span data-stu-id="03639-137">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 



