---
title: Guida alla creazione dell'interfaccia
description: Guida alla creazione dell'interfaccia
ms.assetid: 86c77764-5c8c-4493-ac2d-15268c1ba564
keywords:
- Windows Media Player, interfacce
- Windows Media Player Skin, Guida alla creazione
- interfacce, Guida alla creazione
- creazione di interfacce, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7214accedf24bd80449bf8952bc9268f9b9bf49d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298119"
---
# <a name="skin-creation-guide"></a><span data-ttu-id="fd453-107">Guida alla creazione dell'interfaccia</span><span class="sxs-lookup"><span data-stu-id="fd453-107">Skin Creation Guide</span></span>

<span data-ttu-id="fd453-108">Questa guida è una serie di spiegazioni dettagliate su come creare tipi diversi di interfacce.</span><span class="sxs-lookup"><span data-stu-id="fd453-108">This guide is a series of detailed explanations of how to create different kinds of skins.</span></span> <span data-ttu-id="fd453-109">Per informazioni più generali sulle interfacce, vedere [informazioni sulle interfacce](about-skins.md).</span><span class="sxs-lookup"><span data-stu-id="fd453-109">For more general information on skins, see [About Skins](about-skins.md).</span></span> <span data-ttu-id="fd453-110">Per dettagli specifici su ogni attributo, metodo e evento usato nelle interfacce, vedere la Guida di riferimento per la [programmazione dell'interfaccia](skin-programming-reference.md).</span><span class="sxs-lookup"><span data-stu-id="fd453-110">For specific details about every attribute, method, and event used in skins, see the [Skin Programming Reference](skin-programming-reference.md).</span></span> <span data-ttu-id="fd453-111">Quando si è maggiormente interessati alla programmazione dell'interfaccia, può essere utile leggere la parte di questo SDK coprendo il modello a [oggetti di Windows Media Player](windows-media-player-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="fd453-111">As you get more involved in the programming of your skin, you may want to read the part of this SDK covering the [Windows Media Player Object Model](windows-media-player-object-model.md).</span></span>

<span data-ttu-id="fd453-112">In questa guida vengono fornite le istruzioni per la creazione dell'arte per Adobe Photoshop 5,5, un programma di manipolazione dell'arte comune.</span><span class="sxs-lookup"><span data-stu-id="fd453-112">In this guide, instructions for creating the art will be given for Adobe Photoshop 5.5, a popular art manipulation program.</span></span> <span data-ttu-id="fd453-113">Le istruzioni specifiche possono essere diverse se si ha un programma di grafica simile, ad esempio Jasc Paint Shop Pro o la viscosità di Sonic Foundry, ma i concetti saranno gli stessi.</span><span class="sxs-lookup"><span data-stu-id="fd453-113">The specific instructions may be different if you have a similar art program such as Jasc Paint Shop Pro or Sonic Foundry Viscosity, but the concepts will be the same.</span></span> <span data-ttu-id="fd453-114">Photoshop è stato scelto per due motivi: è un programma di arte popolare per gli artisti commerciali e funziona con i livelli.</span><span class="sxs-lookup"><span data-stu-id="fd453-114">Photoshop was chosen for two reasons: it is a popular art program for commercial artists, and it works with layers.</span></span> <span data-ttu-id="fd453-115">Come si vedrà nelle esercitazioni, i livelli sono molto utili per la creazione di interfacce.</span><span class="sxs-lookup"><span data-stu-id="fd453-115">As you will see in the tutorials, layers are very useful for skin creation.</span></span>

<span data-ttu-id="fd453-116">In questa guida vengono illustrate le attività seguenti.</span><span class="sxs-lookup"><span data-stu-id="fd453-116">This guide will cover the following tasks.</span></span>



| <span data-ttu-id="fd453-117">Attività</span><span class="sxs-lookup"><span data-stu-id="fd453-117">Task</span></span>                                                     | <span data-ttu-id="fd453-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fd453-118">Description</span></span>                                                                                     |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fd453-119">Creazione della prima interfaccia</span><span class="sxs-lookup"><span data-stu-id="fd453-119">Building Your First Skin</span></span>](building-your-first-skin.md) | <span data-ttu-id="fd453-120">Una procedura dettagliata di un'interfaccia semplice che avvia e arresta Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="fd453-120">A walk-through of a simple skin that starts and stops Windows Media Player.</span></span>                     |
| [<span data-ttu-id="fd453-121">Aggiunta di una playlist</span><span class="sxs-lookup"><span data-stu-id="fd453-121">Adding a Playlist</span></span>](adding-a-playlist.md)               | <span data-ttu-id="fd453-122">Come usare una playlist semplice.</span><span class="sxs-lookup"><span data-stu-id="fd453-122">How to use a simple playlist.</span></span>                                                                   |
| [<span data-ttu-id="fd453-123">Scelta di file</span><span class="sxs-lookup"><span data-stu-id="fd453-123">Choosing Files</span></span>](choosing-files.md)                     | <span data-ttu-id="fd453-124">Come selezionare i file con una finestra di dialogo Apri file.</span><span class="sxs-lookup"><span data-stu-id="fd453-124">How to pick files with an open file dialog box.</span></span>                                                 |
| [<span data-ttu-id="fd453-125">Aggiunta di video</span><span class="sxs-lookup"><span data-stu-id="fd453-125">Adding Video</span></span>](adding-video.md)                         | <span data-ttu-id="fd453-126">Come inserire una finestra video nell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="fd453-126">How to put a video window into your skin.</span></span>                                                       |
| [<span data-ttu-id="fd453-127">Aggiunta di visualizzazioni</span><span class="sxs-lookup"><span data-stu-id="fd453-127">Adding Visualizations</span></span>](adding-visualizations.md)       | <span data-ttu-id="fd453-128">Come aggiungere visualizzazioni.</span><span class="sxs-lookup"><span data-stu-id="fd453-128">How to add visualizations.</span></span>                                                                      |
| [<span data-ttu-id="fd453-129">Aggiunta di un dispositivo di scorrimento</span><span class="sxs-lookup"><span data-stu-id="fd453-129">Adding a Slider</span></span>](adding-a-slider.md)                   | <span data-ttu-id="fd453-130">Come usare un dispositivo di scorrimento per tenere traccia dello stato di avanzamento del contenuto multimediale... e consentire all'utente di modificarlo.</span><span class="sxs-lookup"><span data-stu-id="fd453-130">How to use a slider to track the progress of your media content ... and let the user change it!</span></span> |
| [<span data-ttu-id="fd453-131">Creazione di dispositivi di scorrimento personalizzati</span><span class="sxs-lookup"><span data-stu-id="fd453-131">Creating Custom Sliders</span></span>](creating-custom-sliders.md)   | <span data-ttu-id="fd453-132">Come controllare il volume con un dispositivo di scorrimento personalizzato.</span><span class="sxs-lookup"><span data-stu-id="fd453-132">How to control the volume with a custom slider.</span></span>                                                 |
| [<span data-ttu-id="fd453-133">Altri esempi di Skin</span><span class="sxs-lookup"><span data-stu-id="fd453-133">Other Skin Samples</span></span>](other-skin-samples.md)             | <span data-ttu-id="fd453-134">Vedere la sezione relativa agli esempi dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="fd453-134">See the samples section of the SDK.</span></span>                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="fd453-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fd453-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd453-136">**Interfacce di Media Player Windows**</span><span class="sxs-lookup"><span data-stu-id="fd453-136">**Windows Media Player Skins**</span></span>](windows-media-player-skins.md)
</dt> </dl>

 

 




