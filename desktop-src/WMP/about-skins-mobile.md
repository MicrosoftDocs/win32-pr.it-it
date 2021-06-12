---
title: Informazioni sulle interfaccia (dispositivi mobili)
description: Informazioni sulle interfaccia per lettori mobili. Un'interfaccia è un'interfaccia utente personalizzata da Windows Media Player.
ms.assetid: 105c11ce-705b-4a0c-8982-d0f9dd9ae3ac
keywords:
- Windows Media Player Mobile, skin
- Windows Media Player per dispositivi mobili, informazioni
- Windows Media Player per dispositivi mobili, creazione
- skins, Windows Media Player Mobile
- creazione di interfaccia, Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebdffdc4075456c6cb7ccf9d1940c5253c732cd3
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011224"
---
# <a name="about-skins-mobile"></a><span data-ttu-id="bf8d0-109">Informazioni sulle interfaccia (dispositivi mobili)</span><span class="sxs-lookup"><span data-stu-id="bf8d0-109">About Skins (Mobile)</span></span>

<span data-ttu-id="bf8d0-110">Un'interfaccia è un'interfaccia utente personalizzata da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="bf8d0-110">A skin is a customized user interface to Windows Media Player.</span></span> <span data-ttu-id="bf8d0-111">È possibile creare pulsanti personalizzati per avviare e arrestare la riproduzione di file multimediali digitali, aggiungere dispositivi di scorrimento per modificare il volume e la posizione di riproduzione nell'elemento multimediale e fornire all'utente informazioni di testo, ad esempio il nome di un brano.</span><span class="sxs-lookup"><span data-stu-id="bf8d0-111">You can create your own buttons to start and stop playback of digital media, add sliders to change volume and playback position in the media item, and provide the user with text information such as the name of a song.</span></span> <span data-ttu-id="bf8d0-112">Soprattutto, è possibile aggiungere elementi grafici personalizzati o usare oggetti grafici esistenti per creare un aspetto univoco per l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="bf8d0-112">Best of all, you can add your own artwork or use existing art to create a unique appearance for your skin.</span></span>

<span data-ttu-id="bf8d0-113">I passaggi di base per la creazione di un'interfaccia sono:</span><span class="sxs-lookup"><span data-stu-id="bf8d0-113">The basic steps in creating a skin are:</span></span>

1.  <span data-ttu-id="bf8d0-114">**Progettare** l'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="bf8d0-114">**Design** your user interface.</span></span> <span data-ttu-id="bf8d0-115">Decidere quali pulsanti, caselle di testo e trackbar si desidera fornire all'utente in modo che possa controllare le funzioni scelte nel passaggio 1.</span><span class="sxs-lookup"><span data-stu-id="bf8d0-115">Decide which buttons, text boxes, and trackbars you want to provide to the user so that they can control the functions you chose in step 1.</span></span> <span data-ttu-id="bf8d0-116">È possibile delineare le proprie idee per vedere come si adattano alle dimensioni dell'immagine che si intende usare.</span><span class="sxs-lookup"><span data-stu-id="bf8d0-116">You may want to sketch out your ideas to see how they fit on the image size you will be working with.</span></span>
2.  <span data-ttu-id="bf8d0-117">**Creare** l'immagine che si vuole mostrare all'utente.</span><span class="sxs-lookup"><span data-stu-id="bf8d0-117">**Create** the art you want to show the user.</span></span> <span data-ttu-id="bf8d0-118">Sarà costituita da diverse immagini che mostrano le immagini di sfondo, altre immagini che è possibile visualizzare e immagini di mapping se si usano i pulsanti di area.</span><span class="sxs-lookup"><span data-stu-id="bf8d0-118">This will consist of several images that show the background images, other images you may want to display, and mapping images if you use region buttons.</span></span>
3.  <span data-ttu-id="bf8d0-119">**Scrivere** il file di definizione dell'interfaccia che collega le funzioni multimediali digitali, l'interfaccia utente e le immagini.</span><span class="sxs-lookup"><span data-stu-id="bf8d0-119">**Write** the skin definition file that will link together the digital media functions, user interface, and images.</span></span> <span data-ttu-id="bf8d0-120">È necessario seguire determinate regole per l'immissione dei dati di testo nel file, ma è possibile esaminare l'interfaccia predefinita come guida.</span><span class="sxs-lookup"><span data-stu-id="bf8d0-120">You must follow certain rules for entering the text data into the file, but you can look at the default skin as a guide.</span></span>

<span data-ttu-id="bf8d0-121">Non è necessario seguire questi passaggi nell'ordine indicato, ma una buona progettazione deriva dalla conoscenza di tutte le possibilità e dalla cura di tutti i dettagli.</span><span class="sxs-lookup"><span data-stu-id="bf8d0-121">You do not need to follow these steps in the order given, but a good design will come from being aware of all the possibilities and taking care of all the details.</span></span>

<span data-ttu-id="bf8d0-122">Le sezioni seguenti forniscono informazioni dettagliate sulle interfaccia.</span><span class="sxs-lookup"><span data-stu-id="bf8d0-122">The following sections provide detailed information about skins.</span></span>



| <span data-ttu-id="bf8d0-123">Sezione</span><span class="sxs-lookup"><span data-stu-id="bf8d0-123">Section</span></span>                                                                                    | <span data-ttu-id="bf8d0-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bf8d0-124">Description</span></span>                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bf8d0-125">Informazioni sulla compatibilità</span><span class="sxs-lookup"><span data-stu-id="bf8d0-125">About Compatibility</span></span>](about-compatibility.md)                                             | <span data-ttu-id="bf8d0-126">Elenca le diverse versioni di Windows Media Player Mobile, i requisiti hardware, la disponibilità di Windows Media Player e le funzionalità dell'interfaccia introdotte per ogni versione del software.</span><span class="sxs-lookup"><span data-stu-id="bf8d0-126">Lists the different versions of Windows Media Player Mobile, the hardware requirements, availability of Windows Media Player, and the skin features introduced for each version of the software.</span></span> |
| [<span data-ttu-id="bf8d0-127">Windows Media Player per dispositivi mobili</span><span class="sxs-lookup"><span data-stu-id="bf8d0-127">Windows Media Player Mobile Functionality</span></span>](windows-media-player-mobile-functionality.md) | <span data-ttu-id="bf8d0-128">Descrive le funzionalità che l'interfaccia può supportare.</span><span class="sxs-lookup"><span data-stu-id="bf8d0-128">Describes the features your skin can support.</span></span>                                                                                                                                                    |
| [<span data-ttu-id="bf8d0-129">Interfaccia utente elementi</span><span class="sxs-lookup"><span data-stu-id="bf8d0-129">User Interface Elements</span></span>](user-interface-elements.md)                                     | <span data-ttu-id="bf8d0-130">Descrive gli elementi dell'interfaccia utente che è possibile creare per l'interfaccia, ad esempio pulsanti, trackbar e schermi video.</span><span class="sxs-lookup"><span data-stu-id="bf8d0-130">Describes the user interface elements you can create for your skin, such as buttons, trackbars, and video displays.</span></span>                                                                              |
| [<span data-ttu-id="bf8d0-131">File di grafica</span><span class="sxs-lookup"><span data-stu-id="bf8d0-131">Art Files</span></span>](art-files-mobile.md)                                                          | <span data-ttu-id="bf8d0-132">Descrive i file di grafica creati per l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="bf8d0-132">Describes the art files you create for your skin.</span></span>                                                                                                                                                |
| [<span data-ttu-id="bf8d0-133">File di definizione dell'interfaccia</span><span class="sxs-lookup"><span data-stu-id="bf8d0-133">Skin Definition File</span></span>](skin-definition-file-mobile.md)                                    | <span data-ttu-id="bf8d0-134">Descrive il file che è necessario creare per descrivere l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="bf8d0-134">Describes the file you must create to describe your skin.</span></span>                                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="bf8d0-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bf8d0-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf8d0-136">**Windows Media Player per dispositivi mobili**</span><span class="sxs-lookup"><span data-stu-id="bf8d0-136">**Windows Media Player Mobile Skins**</span></span>](windows-media-player-mobile-skins.md)
</dt> </dl>

 

 




