---
description: Microsoft Media Foundation è la piattaforma multimediale di nuova generazione per Windows che consente a sviluppatori, consumer e provider di contenuti di adottare la nuova onda di contenuti Premium con affidabilità avanzata, qualità impareggiabile e interoperabilità senza problemi.
ms.assetid: 3f933e39-8f9b-4c62-b528-4f1bba4b45d1
title: Informazioni su Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a166482bbb0291f702a0e402441e292109a3e10
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320465"
---
# <a name="about-media-foundation"></a><span data-ttu-id="e2195-103">Informazioni su Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e2195-103">About Media Foundation</span></span>

<span data-ttu-id="e2195-104">Microsoft Media Foundation è la piattaforma multimediale di nuova generazione per Windows che consente a sviluppatori, consumer e provider di contenuti di adottare la nuova onda di contenuti Premium con affidabilità avanzata, qualità impareggiabile e interoperabilità senza problemi.</span><span class="sxs-lookup"><span data-stu-id="e2195-104">Microsoft Media Foundation is the next generation multimedia platform for Windows that enables developers, consumers, and content providers to embrace the new wave of premium content with enhanced robustness, unparalleled quality, and seamless interoperability.</span></span>

<span data-ttu-id="e2195-105">Media Foundation richiede Windows Vista o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="e2195-105">Media Foundation requires Windows Vista or later.</span></span> <span data-ttu-id="e2195-106">Usa il modello COM (Component Object Model) e richiede C/C++.</span><span class="sxs-lookup"><span data-stu-id="e2195-106">It uses the component object model (COM) and requires C/C++.</span></span> <span data-ttu-id="e2195-107">Microsoft non fornisce un'API gestita per Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="e2195-107">Microsoft does not provide a managed API for Media Foundation.</span></span>

<span data-ttu-id="e2195-108">Le API Media Foundation fanno parte del [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e2195-108">The Media Foundation APIs are part of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e2195-109">Per sviluppare un'applicazione Media Foundation, installare la versione più recente del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="e2195-109">To develop a Media Foundation application, install the latest version of the Windows SDK.</span></span>

## <a name="audio-and-video-quality"></a><span data-ttu-id="e2195-110">Qualità audio e video</span><span class="sxs-lookup"><span data-stu-id="e2195-110">Audio and Video Quality</span></span>

<span data-ttu-id="e2195-111">Media Foundation è stato progettato per soddisfare le sfide poste dal contenuto ad alta definizione.</span><span class="sxs-lookup"><span data-stu-id="e2195-111">Media Foundation has been designed to meet the challenges posed by high-definition content.</span></span> <span data-ttu-id="e2195-112">I miglioramenti apportati alla qualità audio e video in tutta la piattaforma consentono ora di offrire un'esperienza ottimale per il contenuto ad alta definizione di prossima generazione.</span><span class="sxs-lookup"><span data-stu-id="e2195-112">Audio and video quality enhancements made throughout the platform now make it possible to deliver a great experience for next generation high-definition content.</span></span>

-   <span data-ttu-id="e2195-113">DirectX Video Acceleration (DXVA) 2,0 offre un'accelerazione video più efficiente, rispetto a DXVA 1,0, con la decodifica video più solida e semplificata e l'uso esteso dell'hardware nell'elaborazione video.</span><span class="sxs-lookup"><span data-stu-id="e2195-113">DirectX Video Acceleration (DXVA) 2.0 offers more efficient video acceleration, compared with DXVA 1.0, with more robust and streamlined video decoding and extended use of hardware in video processing.</span></span> <span data-ttu-id="e2195-114">Con DXVA 2,0, Windows è in grado di gestire alcuni dei più complessi contenuti ad alta definizione con elevata qualità e una resilienza migliorata.</span><span class="sxs-lookup"><span data-stu-id="e2195-114">With DXVA 2.0, Windows can handle some of the most demanding high-definition content with high quality and improved glitch-resilience.</span></span>

-   <span data-ttu-id="e2195-115">Le informazioni sullo spazio dei colori vengono mantenute in tutta la pipeline video.</span><span class="sxs-lookup"><span data-stu-id="e2195-115">Color-space information is preserved throughout the video pipeline.</span></span> <span data-ttu-id="e2195-116">Gli utenti possono usufruire di contenuti video con la massima fedeltà.</span><span class="sxs-lookup"><span data-stu-id="e2195-116">Users can enjoy video content with full fidelity.</span></span> <span data-ttu-id="e2195-117">Le informazioni sul colore e le immagini interlacciate vengono ora passate all'hardware per le composizioni a singolo passaggio.</span><span class="sxs-lookup"><span data-stu-id="e2195-117">Color information and interlaced images are now passed to hardware for single-pass compositions.</span></span> <span data-ttu-id="e2195-118">La conservazione delle informazioni sullo spazio dei colori riduce anche le conversioni dello spazio dei colori non necessarie, che consente di liberare più cicli per elaborare contenuti HD complessi.</span><span class="sxs-lookup"><span data-stu-id="e2195-118">Preserving color-space information also reduces unnecessary color space conversions, which frees more cycles to process demanding HD content.</span></span>
-   <span data-ttu-id="e2195-119">Il renderer video avanzato (EVR) offre supporto temporizzato migliore, elaborazione video avanzata e resilienza migliorata.</span><span class="sxs-lookup"><span data-stu-id="e2195-119">The enhanced video renderer (EVR) offers better timing support, enhanced video processing, and improved glitch-resilience.</span></span> <span data-ttu-id="e2195-120">Il supporto per la riproduzione a schermo intero è stato migliorato e la rimozione dei video in modalità finestra è stata ridotta a icona.</span><span class="sxs-lookup"><span data-stu-id="e2195-120">Full-screen playback support has been enhanced, and video tearing in windowed mode has been minimized.</span></span>
-   <span data-ttu-id="e2195-121">Media Foundation usa il servizio Utilità di pianificazione classi multimediali (MMCSS), un nuovo servizio di sistema in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e2195-121">Media Foundation uses the Multimedia Class Scheduler Service (MMCSS), a new system service in Windows Vista.</span></span> <span data-ttu-id="e2195-122">MMCSS consente alle applicazioni multimediali di garantire che l'elaborazione sensibile al tempo riceva l'accesso in ordine di priorità alle risorse della CPU.</span><span class="sxs-lookup"><span data-stu-id="e2195-122">MMCSS enables multimedia applications to ensure that their time-sensitive processing receives prioritized access to CPU resources.</span></span>

## <a name="content-access"></a><span data-ttu-id="e2195-123">Accesso al contenuto</span><span class="sxs-lookup"><span data-stu-id="e2195-123">Content Access</span></span>

<span data-ttu-id="e2195-124">Quando l'intrattenimento digitale passa all'era e il contenuto di definizione elevata diventa più portabile e onnipresente, la protezione del contenuto diventerà parte integrante dei prodotti multimediali digitali.</span><span class="sxs-lookup"><span data-stu-id="e2195-124">As digital entertainment moves into the high-definition era and content becomes more portable and ubiquitous, content protection will become an integral part of digital media products.</span></span> <span data-ttu-id="e2195-125">L'estendibilità di Media Foundation garantisce che sia in grado di supportare tali tendenze.</span><span class="sxs-lookup"><span data-stu-id="e2195-125">The extensibility of Media Foundation ensures that it can support these trends.</span></span>

<span data-ttu-id="e2195-126">Inoltre, Media Foundation estensibilità consente il funzionamento combinato di diversi sistemi di protezione del contenuto.</span><span class="sxs-lookup"><span data-stu-id="e2195-126">In addition, Media Foundation extensibility enables different content protection systems to operate together.</span></span>

## <a name="about-media-foundation"></a><span data-ttu-id="e2195-127">Informazioni su Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e2195-127">About Media Foundation</span></span>

<span data-ttu-id="e2195-128">Questa sezione contiene informazioni generali sulle API Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="e2195-128">This section contains general information about the Media Foundation APIs.</span></span> <span data-ttu-id="e2195-129">Informazioni dettagliate sulla programmazione sono disponibili nella [Guida alla programmazione di Media Foundation](media-foundation-programming-guide.md).</span><span class="sxs-lookup"><span data-stu-id="e2195-129">Detailed programming information can be found in the [Media Foundation Programming Guide](media-foundation-programming-guide.md).</span></span>



| <span data-ttu-id="e2195-130">Sezione</span><span class="sxs-lookup"><span data-stu-id="e2195-130">Section</span></span>                                                                              | <span data-ttu-id="e2195-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e2195-131">Description</span></span>                                                               |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="e2195-132">Novità di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e2195-132">What's New for Media Foundation</span></span>](whats-new-for-media-foundation.md)                | <span data-ttu-id="e2195-133">Vengono descritte le nuove funzionalità di Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="e2195-133">Describes new features in Media Foundation.</span></span>                               |
| [<span data-ttu-id="e2195-134">Intestazioni e librerie Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e2195-134">Media Foundation Headers and Libraries</span></span>](media-foundation-headers-and-libraries.md) | <span data-ttu-id="e2195-135">Elenca i file di intestazione e di libreria che definiscono le API Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="e2195-135">Lists the header and library files that define the Media Foundation APIs.</span></span> |
| [<span data-ttu-id="e2195-136">Strumenti di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e2195-136">Media Foundation Tools</span></span>](media-foundation-tools.md)                                 | <span data-ttu-id="e2195-137">Vengono descritti gli strumenti di sviluppo disponibili per Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="e2195-137">Describes the development tools that are available for Media Foundation.</span></span>  |



 

<span data-ttu-id="e2195-138">Media Foundation non è incluso nelle edizioni N e KN di Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e2195-138">Media Foundation is not included with the N and KN editions of Windows 8.</span></span> <span data-ttu-id="e2195-139">Per ulteriori informazioni, vedere [Microsoft Windows Media Feature Pack per le versioni N e KN di tutte le edizioni di Windows 8](https://support.microsoft.com/kb/2703761).</span><span class="sxs-lookup"><span data-stu-id="e2195-139">For more information, see [Microsoft Windows Media Feature Pack for N and KN Versions of all Windows 8 Editions](https://support.microsoft.com/kb/2703761).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2195-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e2195-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2195-141">Microsoft Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e2195-141">Microsoft Media Foundation</span></span>](microsoft-media-foundation-sdk.md)
</dt> </dl>

 

 



