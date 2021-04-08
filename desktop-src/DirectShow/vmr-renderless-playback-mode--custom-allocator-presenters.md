---
description: Modalità di riproduzione con rendering VMR (allocatore personalizzato-Presenter)
ms.assetid: 0381f862-2f16-4b4d-be48-40f7fe151585
title: Modalità di riproduzione con rendering VMR (allocatore personalizzato-Presenter)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ad9cd4dcb5e5b2f1965d49c7f31b4ef8c9ebd78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757667"
---
# <a name="vmr-renderless-playback-mode-custom-allocator-presenters"></a><span data-ttu-id="c05b3-103">Modalità di riproduzione con rendering VMR (allocatore personalizzato-Presenter)</span><span class="sxs-lookup"><span data-stu-id="c05b3-103">VMR Renderless Playback Mode (Custom Allocator-Presenters)</span></span>

<span data-ttu-id="c05b3-104">In modalità di riproduzione senza rendering, VMR non esegue il rendering.</span><span class="sxs-lookup"><span data-stu-id="c05b3-104">In renderless playback mode, the VMR does not perform the rendering.</span></span> <span data-ttu-id="c05b3-105">USA invece un allocatore-Presenter personalizzato fornito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c05b3-105">Instead, it uses a custom allocator-presenter supplied by the application.</span></span> <span data-ttu-id="c05b3-106">Questa modalità è utile per giochi e altri tipi di applicazioni con effetti video avanzati.</span><span class="sxs-lookup"><span data-stu-id="c05b3-106">This mode is useful for games and other types of applications that have sophisticated video effects.</span></span> <span data-ttu-id="c05b3-107">La modalità di riproduzione con rendering consente alle applicazioni di creare e controllare la propria superficie DirectDraw (VMR-7) o la superficie Direct3D (VMR-9) e di accedere ai bit video in fase di presentazione.</span><span class="sxs-lookup"><span data-stu-id="c05b3-107">Renderless playback mode enables the applications to create and control its own DirectDraw surface (VMR-7) or Direct3D surface (VMR-9), and to access the video bits at presentation time.</span></span>

<span data-ttu-id="c05b3-108">In modalità senza rendering, VMR-9 non carica automaticamente il componente mixer.</span><span class="sxs-lookup"><span data-stu-id="c05b3-108">In renderless mode, the VMR-9 does not automatically load its mixer component.</span></span>

<span data-ttu-id="c05b3-109">In modalità di riproduzione senza rendering, l'applicazione esegue le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="c05b3-109">In renderless playback mode, the application does the following tasks:</span></span>

-   <span data-ttu-id="c05b3-110">Gestisce la finestra di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="c05b3-110">Manages the playback window.</span></span>
-   <span data-ttu-id="c05b3-111">Alloca l'oggetto DirectDraw o Direct3D e il buffer del frame finale.</span><span class="sxs-lookup"><span data-stu-id="c05b3-111">Allocates the DirectDraw or Direct3D object and the final frame buffer.</span></span>
-   <span data-ttu-id="c05b3-112">Notifica al resto del sistema di riproduzione l'oggetto in uso.</span><span class="sxs-lookup"><span data-stu-id="c05b3-112">Notifies the rest of the playback system of the object being used.</span></span>
-   <span data-ttu-id="c05b3-113">Visualizza il buffer dei frame all'ora corretta.</span><span class="sxs-lookup"><span data-stu-id="c05b3-113">Presents the frame buffer at the correct time.</span></span>
-   <span data-ttu-id="c05b3-114">Gestisce tutte le modifiche in modalità di risoluzione, monitora le modifiche e le perdite di superficie.</span><span class="sxs-lookup"><span data-stu-id="c05b3-114">Handles all resolution-mode changes, monitor changes, and surface losses.</span></span> <span data-ttu-id="c05b3-115">Deve consigliare il resto del sistema di riproduzione di questi eventi.</span><span class="sxs-lookup"><span data-stu-id="c05b3-115">It must advise the rest of the playback system of these events.</span></span>

<span data-ttu-id="c05b3-116">VMR esegue le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="c05b3-116">The VMR does the following:</span></span>

-   <span data-ttu-id="c05b3-117">Gestisce tutte le tempistiche correlate alla presentazione del fotogramma video.</span><span class="sxs-lookup"><span data-stu-id="c05b3-117">Handles all timing related to presenting the video frame.</span></span>
-   <span data-ttu-id="c05b3-118">Fornisce informazioni sul controllo di qualità per l'applicazione e il resto del sistema di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="c05b3-118">Provides quality-control information to the application and the rest of the playback system.</span></span>
-   <span data-ttu-id="c05b3-119">Presenta un'interfaccia coerente con i componenti upstream del sistema di riproduzione, che non sono consapevoli del fatto che l'applicazione fornisce l'allocazione del buffer di frame e l'esecuzione del rendering.</span><span class="sxs-lookup"><span data-stu-id="c05b3-119">Presents a consistent interface to the upstream components of the playback system, which are not aware that the application is providing the frame buffer allocation and performing the rendering.</span></span>
-   <span data-ttu-id="c05b3-120">Fornisce qualsiasi combinazione di flussi video che potrebbero essere necessari prima del rendering.</span><span class="sxs-lookup"><span data-stu-id="c05b3-120">Provides any mixing of video streams that may be required prior to rendering.</span></span>

<span data-ttu-id="c05b3-121">Poiché il deinterlacciamento viene eseguito dal mixer, Allocator-Presenter riceve sempre i frame deinterlacciati.</span><span class="sxs-lookup"><span data-stu-id="c05b3-121">Because deinterlacing is performed by the mixer, the allocator-presenter always received deinterlaced frames.</span></span> <span data-ttu-id="c05b3-122">Per ulteriori informazioni, vedere [impostazione delle preferenze di deinterlacciamento](setting-deinterlace-preferences.md).</span><span class="sxs-lookup"><span data-stu-id="c05b3-122">For more information, see [Setting Deinterlace Preferences](setting-deinterlace-preferences.md).</span></span>

<span data-ttu-id="c05b3-123">Per ulteriori informazioni sulla specifica di un allocatore-Presenter personalizzato, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="c05b3-123">For more information about providing a custom allocator-presenter, see the following topics:</span></span>

-   [<span data-ttu-id="c05b3-124">Specifica di un Allocator-Presenter personalizzato per VMR-7</span><span class="sxs-lookup"><span data-stu-id="c05b3-124">Supplying a Custom Allocator-Presenter for VMR-7</span></span>](supplying-a-custom-allocator-presenter-for-vmr-7.md)
-   [<span data-ttu-id="c05b3-125">Specifica di un Allocator-Presenter personalizzato per VMR-9</span><span class="sxs-lookup"><span data-stu-id="c05b3-125">Supplying a Custom Allocator-Presenter for VMR-9</span></span>](supplying-a-custom-allocator-presenter-for-vmr-9.md)
-   [<span data-ttu-id="c05b3-126">Sincronizzazione di VMR alla frequenza di aggiornamento del monitoraggio</span><span class="sxs-lookup"><span data-stu-id="c05b3-126">Synchronizing the VMR to the Monitor's Refresh Rate</span></span>](synchronizing-the-vmr-to-the-monitors-refresh-rate.md)

 

 



