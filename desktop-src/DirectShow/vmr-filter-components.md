---
description: Componenti del filtro VMR
ms.assetid: 86fd8d6f-a742-457d-bb30-d04542431a0a
title: Componenti del filtro VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b597f6ac1b52f81ddc26d18e3fe0c6d16bae9515
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529509"
---
# <a name="vmr-filter-components"></a><span data-ttu-id="d72b0-103">Componenti del filtro VMR</span><span class="sxs-lookup"><span data-stu-id="d72b0-103">VMR Filter Components</span></span>

<span data-ttu-id="d72b0-104">VMR usa una progettazione modulare che consente alle applicazioni di configurarla per molti scenari di rendering diversi.</span><span class="sxs-lookup"><span data-stu-id="d72b0-104">The VMR employs a modular design that enables applications to configure it for many different rendering scenarios.</span></span> <span data-ttu-id="d72b0-105">A seconda della configurazione, il VMR contiene da due a cinque sottocomponenti (oltre ai pin di input).</span><span class="sxs-lookup"><span data-stu-id="d72b0-105">Depending on its configuration, the VMR contains from two to five subcomponents (in addition to its input pins).</span></span>

![VMR in modalità finestra con più flussi](images/vmr-multiple-streams.png)

<span data-ttu-id="d72b0-107">**Mixer:** Il mixer è un oggetto COM responsabile della combinazione di più flussi.</span><span class="sxs-lookup"><span data-stu-id="d72b0-107">**Mixer:** The mixer is a COM object responsible for mixing multiple streams.</span></span> <span data-ttu-id="d72b0-108">Il deinterlacciamento si verifica anche all'interno del mixer.</span><span class="sxs-lookup"><span data-stu-id="d72b0-108">Deinterlacing also occurs inside the mixer.</span></span> <span data-ttu-id="d72b0-109">Il mixer viene caricato da VMR quando vengono rilevati più flussi di input o quando il video di input è interlacciato.</span><span class="sxs-lookup"><span data-stu-id="d72b0-109">The mixer is loaded by the VMR when multiple input streams are detected, or when the input video is interlaced.</span></span> <span data-ttu-id="d72b0-110">Il mixer raccoglie informazioni su ogni flusso di input e ordina i flussi nell'ordine Z corretto.</span><span class="sxs-lookup"><span data-stu-id="d72b0-110">The mixer collects information about each input stream and sorts the streams into the correct Z-order.</span></span> <span data-ttu-id="d72b0-111">È responsabile di determinare quando ogni pin di input riceve un campione e per istruire il compositore dell'immagine al momento giusto per eseguire la fusione effettiva.</span><span class="sxs-lookup"><span data-stu-id="d72b0-111">It is responsible for determining when each input pin receives a sample, and for instructing the image compositor at the proper time to perform the actual blending.</span></span> <span data-ttu-id="d72b0-112">Il mixer calcola anche il timestamp da applicare a ogni immagine di output.</span><span class="sxs-lookup"><span data-stu-id="d72b0-112">The mixer also calculates the time stamp to be applied to each output image.</span></span> <span data-ttu-id="d72b0-113">Quando l'applicazione fornisce una bitmap da visualizzare sopra l'immagine composita, il mixer è responsabile di garantire che la bitmap venga visualizzata in cima anche se viene modificato l'ordine Z dei flussi di input.</span><span class="sxs-lookup"><span data-stu-id="d72b0-113">When the application is supplying a bitmap to be displayed on top of the composited image, the mixer is responsible for ensuring that the bitmap is displayed on top even if the Z-order of the input streams is modified.</span></span>

<span data-ttu-id="d72b0-114">**Compositor immagine:** Il compositor dell'immagine è un oggetto COM che esegue la fusione effettiva dei flussi di input su una singola superficie DirectDraw o Direct3D fornita da Allocator-Presenter.</span><span class="sxs-lookup"><span data-stu-id="d72b0-114">**Image Compositor:** The Image Compositor is a COM object that performs the actual blending of the input streams onto a single DirectDraw or Direct3D surface provided by the allocator-presenter.</span></span> <span data-ttu-id="d72b0-115">VMR fornisce un compositor di immagini predefinito che consente alle applicazioni di eseguire effetti di fusione alfa 2D.</span><span class="sxs-lookup"><span data-stu-id="d72b0-115">The VMR provides a default image compositor that enables applications to perform 2-D alpha-blending effects.</span></span> <span data-ttu-id="d72b0-116">Le applicazioni possono fornire un compositor di immagini personalizzato per abilitare altri effetti 2D e 3D, ad esempio l'applicazione di trame a parti dell'immagine, la fusione alfa per pixel, il mapping dell'immagine a oggetti fissi o mobili e così via.</span><span class="sxs-lookup"><span data-stu-id="d72b0-116">Applications can provide a custom image compositor to enable other 2-D and 3-D effects, such as applying textures to portions of the image, per-pixel alpha blending, mapping the image to stationary or moving 3-D objects, and so on.</span></span>

<span data-ttu-id="d72b0-117">**Allocatore-Presenter:** Allocator-Presenter è un oggetto COM che alloca l'oggetto DirectDraw o Direct3D e gestisce la comunicazione con la scheda grafica.</span><span class="sxs-lookup"><span data-stu-id="d72b0-117">**Allocator-Presenter:** The allocator-presenter is a COM object that allocates the DirectDraw or Direct3D object and handles the communication with the graphics card.</span></span> <span data-ttu-id="d72b0-118">Il disegno può essere eseguito come un flip o come blit.</span><span class="sxs-lookup"><span data-stu-id="d72b0-118">The drawing can be performed either as a flip or as a blit.</span></span> <span data-ttu-id="d72b0-119">È possibile collegare il proprio allocatore-Presenter per creare e controllare l'oggetto DirectDraw o Direct3D e/o per ottenere l'accesso ai bit video in fase di presentazione.</span><span class="sxs-lookup"><span data-stu-id="d72b0-119">You can plug in your own allocator-presenter in order to create and control the DirectDraw or Direct3D object, and/or to obtain access to the video bits at presentation time.</span></span>

<span data-ttu-id="d72b0-120">**Gestione finestre:** Gestione finestre viene utilizzato solo in modalità finestra.</span><span class="sxs-lookup"><span data-stu-id="d72b0-120">**Window Manager:** The Window Manager is used only in windowed mode.</span></span> <span data-ttu-id="d72b0-121">Gestione finestre supporta le interfacce legacy [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) e [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) per la compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="d72b0-121">The Window Manager supports the legacy [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) and [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interfaces for backward-compatibility.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d72b0-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d72b0-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d72b0-123">Informazioni sul rendering del mixaggio video</span><span class="sxs-lookup"><span data-stu-id="d72b0-123">About the Video Mixing Render</span></span>](about-the-video-mixing-render.md)
</dt> </dl>

 

 



