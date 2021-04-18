---
title: File di immagine
description: File di immagine
ms.assetid: 93893610-de8d-4b9a-b23d-75ddb3e1e557
keywords:
- Interfacce di Media Player di Windows, file di immagine
- interfacce, file di immagine
- file per Skins, Art
- file di immagine per le interfacce, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a246ac411a3dfe2c5bab529ddcccce5596434617
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298865"
---
# <a name="art-files"></a><span data-ttu-id="0d42c-107">File di immagine</span><span class="sxs-lookup"><span data-stu-id="0d42c-107">Art Files</span></span>

<span data-ttu-id="0d42c-108">È necessario creare uno o più file di immagine per l'interfaccia personalizzata.</span><span class="sxs-lookup"><span data-stu-id="0d42c-108">You must create one or more art files for your skin.</span></span> <span data-ttu-id="0d42c-109">Senza l'arte, l'utente non avrà nulla da considerare.</span><span class="sxs-lookup"><span data-stu-id="0d42c-109">Without art, the user will have nothing to look at.</span></span> <span data-ttu-id="0d42c-110">È possibile creare un'interfaccia invisibile, ma non ne verrebbe visualizzata alcuna.</span><span class="sxs-lookup"><span data-stu-id="0d42c-110">You could create an invisible skin, but no one would see it!</span></span> <span data-ttu-id="0d42c-111">Anche in questo caso, è necessario creare file di immagine per contenere le immagini invisibili, perché il file di definizione dell'interfaccia richiede file di immagine per elementi specifici.</span><span class="sxs-lookup"><span data-stu-id="0d42c-111">And even then, you would still have to create art files to hold your invisible images, because the skin definition file requires art files for specific elements.</span></span>

<span data-ttu-id="0d42c-112">Sono disponibili tre usi per l'arte negli Skin: immagini primarie, immagini di mapping e immagini alternative.</span><span class="sxs-lookup"><span data-stu-id="0d42c-112">There are three uses for art in skins: primary images, mapping images, and alternate images.</span></span>

## <a name="primary-images"></a><span data-ttu-id="0d42c-113">Immagini primarie</span><span class="sxs-lookup"><span data-stu-id="0d42c-113">Primary Images</span></span>

<span data-ttu-id="0d42c-114">È necessario creare un'immagine primaria per l'interfaccia personalizzata.</span><span class="sxs-lookup"><span data-stu-id="0d42c-114">You must create a primary image for your skin.</span></span> <span data-ttu-id="0d42c-115">Questo è ciò che gli utenti visualizzeranno durante l'installazione dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="0d42c-115">This is what the users will see when they install your skin.</span></span> <span data-ttu-id="0d42c-116">L'immagine principale è costituita da una o più immagini create da specifici controlli di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="0d42c-116">The primary image is composed of one or more images that are created by specific skin controls.</span></span>

<span data-ttu-id="0d42c-117">Se si dispone di più di un controllo, è necessario specificare l'ordine z, che definisce i controlli che vengono visualizzati davanti ad altri controlli.</span><span class="sxs-lookup"><span data-stu-id="0d42c-117">If you have more than one control, you must specify the z-order, which defines which controls are displayed in front of other controls.</span></span> <span data-ttu-id="0d42c-118">Ogni elemento di **visualizzazione** avrà un'immagine di sfondo a cui è possibile aggiungere altre immagini di elementi, consentendo di creare un'immagine composita primaria.</span><span class="sxs-lookup"><span data-stu-id="0d42c-118">Each **View** element will have a background image that you can add other element images to, allowing you to create a primary composite image.</span></span>

<span data-ttu-id="0d42c-119">È anche possibile avere immagini secondarie, ad esempio una barra di scorrimento, che non vengono visualizzate quando l'interfaccia viene visualizzata per la prima volta, ma che vengono visualizzate quando l'utente esegue un'azione.</span><span class="sxs-lookup"><span data-stu-id="0d42c-119">You also may have secondary images, such as a sliding tray, that do not display when your skin first appears, but that show up when the user takes some action.</span></span> <span data-ttu-id="0d42c-120">Seguono le stesse regole delle immagini primarie, in quanto vengono create con un set di controlli.</span><span class="sxs-lookup"><span data-stu-id="0d42c-120">These follow the same rules as primary images, in that they are created with a set of controls.</span></span>

## <a name="mapping-images"></a><span data-ttu-id="0d42c-121">Mapping di immagini</span><span class="sxs-lookup"><span data-stu-id="0d42c-121">Mapping Images</span></span>

<span data-ttu-id="0d42c-122">Una delle funzionalità più potenti di Windows Media Player Skin è che è possibile usare il mapping delle immagini per attivare gli eventi per l'interfaccia personalizzata.</span><span class="sxs-lookup"><span data-stu-id="0d42c-122">One of the most powerful features of Windows Media Player skins is that you can use image mapping to trigger events for your skin.</span></span> <span data-ttu-id="0d42c-123">Le mappe immagine sono file che contengono immagini speciali.</span><span class="sxs-lookup"><span data-stu-id="0d42c-123">Image maps are files that contain special images.</span></span> <span data-ttu-id="0d42c-124">Le immagini in un file di mappa immagine, tuttavia, non sono pensate per essere visualizzate dall'utente, ma vengono usate da Windows Media Player per eseguire un'azione quando l'utente fa clic sull'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="0d42c-124">The images in an image map file, however, are not meant to be viewed by the user, but are used by Windows Media Player to take action when the user clicks on your skin.</span></span>

<span data-ttu-id="0d42c-125">Per i diversi controlli sono necessari tipi diversi di mappe immagine.</span><span class="sxs-lookup"><span data-stu-id="0d42c-125">Different controls need different kinds of image maps.</span></span> <span data-ttu-id="0d42c-126">Se, ad esempio, si colora parte di un'immagine con un valore rosso specifico e l'utente fa clic sull'area corrispondente dell'immagine primaria, un pulsante genererà un evento.</span><span class="sxs-lookup"><span data-stu-id="0d42c-126">For example, if you color part of an image map a specific red value, and the user clicks on the corresponding area of your primary image, a button will fire an event.</span></span> <span data-ttu-id="0d42c-127">Il colore viene utilizzato per definire quali eventi vengono attivati facendo clic in una particolare area dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="0d42c-127">Color is used to define which events are triggered by clicking in a particular area of the skin.</span></span>

## <a name="alternate-images"></a><span data-ttu-id="0d42c-128">Immagini alternative</span><span class="sxs-lookup"><span data-stu-id="0d42c-128">Alternate Images</span></span>

<span data-ttu-id="0d42c-129">È anche possibile configurare immagini alternative da visualizzare quando un utente esegue un'operazione.</span><span class="sxs-lookup"><span data-stu-id="0d42c-129">You can also set up alternate images to display when a user does something.</span></span> <span data-ttu-id="0d42c-130">Ad esempio, è possibile creare un'immagine alternativa di un pulsante che verrà visualizzato solo quando il mouse viene posizionato sul pulsante.</span><span class="sxs-lookup"><span data-stu-id="0d42c-130">For example, you can create an alternate image of a button that will be displayed only when the mouse hovers over the button.</span></span> <span data-ttu-id="0d42c-131">Si tratta di un metodo efficace per consentire agli utenti di sapere cosa possono fare e anche di un'interfaccia utente altamente individuabile.</span><span class="sxs-lookup"><span data-stu-id="0d42c-131">This is a good way to let users know what they can do, and also allows for a highly discoverable user interface.</span></span> <span data-ttu-id="0d42c-132">Utilizzando con attenzione le descrizioni comandi e le immagini del passaggio del mouse, è possibile creare interfacce utente insolite che forniscono comunque commenti e suggerimenti sugli utenti sulle opzioni disponibili.</span><span class="sxs-lookup"><span data-stu-id="0d42c-132">By using ToolTips and hover images carefully, you can create unusual user interfaces that still give the user feedback about what options are available.</span></span>

<span data-ttu-id="0d42c-133">Nelle sezioni seguenti vengono fornite ulteriori informazioni sui file di immagine:</span><span class="sxs-lookup"><span data-stu-id="0d42c-133">The following sections provide more information about art files:</span></span>

-   [<span data-ttu-id="0d42c-134">Immagini primarie</span><span class="sxs-lookup"><span data-stu-id="0d42c-134">Primary Images</span></span>](primary-images.md)
-   [<span data-ttu-id="0d42c-135">Mapping di immagini</span><span class="sxs-lookup"><span data-stu-id="0d42c-135">Mapping Images</span></span>](mapping-images.md)
-   [<span data-ttu-id="0d42c-136">Immagini alternative</span><span class="sxs-lookup"><span data-stu-id="0d42c-136">Alternate Images</span></span>](alternate-images.md)
-   [<span data-ttu-id="0d42c-137">Formati di file di immagine</span><span class="sxs-lookup"><span data-stu-id="0d42c-137">Art File Formats</span></span>](art-file-formats.md)
-   [<span data-ttu-id="0d42c-138">Esempio di arte semplice</span><span class="sxs-lookup"><span data-stu-id="0d42c-138">Simple Art Example</span></span>](simple-art-example.md)

## <a name="related-topics"></a><span data-ttu-id="0d42c-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0d42c-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d42c-140">**File di interfaccia**</span><span class="sxs-lookup"><span data-stu-id="0d42c-140">**Skin Files**</span></span>](skin-files.md)
</dt> </dl>

 

 




