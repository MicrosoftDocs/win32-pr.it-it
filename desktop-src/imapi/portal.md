---
title: Image Mastering API
description: Image Mastering API
ms.assetid: 4902d3fb-3195-4909-ab64-28f8a77ba14c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 641d9357496eb82a7e30f25a711928b16eeee2bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117579"
---
# <a name="image-mastering-api"></a><span data-ttu-id="a9498-103">Image Mastering API</span><span class="sxs-lookup"><span data-stu-id="a9498-103">Image Mastering API</span></span>

## <a name="purpose"></a><span data-ttu-id="a9498-104">Scopo</span><span class="sxs-lookup"><span data-stu-id="a9498-104">Purpose</span></span>

<span data-ttu-id="a9498-105">L'API di mastering immagini di Microsoft Windows consente alle applicazioni di eseguire lo stageing e masterizzare le immagini su supporti di archiviazione ottico CD, DVD e Blu-ray.</span><span class="sxs-lookup"><span data-stu-id="a9498-105">The Microsoft Windows image mastering API enables applications to stage and burn images to CD, DVD, and Blu-ray optical storage media.</span></span> <span data-ttu-id="a9498-106">Questa API può essere utilizzata anche da altri supporti simili a dischi in cui le immagini sono disponibili nello stesso modo.</span><span class="sxs-lookup"><span data-stu-id="a9498-106">Other disc-like media that lay images in the same manner can also use this API.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="a9498-107">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="a9498-107">Developer audience</span></span>

<span data-ttu-id="a9498-108">IMAPI è progettato per C/C++ e per Visual Basic sviluppatori e per coloro che scrivono script con VBScript.</span><span class="sxs-lookup"><span data-stu-id="a9498-108">IMAPI is designed for C/C++ and Visual Basic developers and those writing scripts using VBScript.</span></span>

<span data-ttu-id="a9498-109">È consigliabile conoscere le tecnologie e i file system CD, DVD e Blu-ray.</span><span class="sxs-lookup"><span data-stu-id="a9498-109">Knowledge of CD, DVD, and Blu-ray technologies and file systems is recommended.</span></span> <span data-ttu-id="a9498-110">Gli sviluppatori possono trarre vantaggio da una familiarità con la revisione più recente di Multimedia Command (MMC) [in ftp://ftp.t10.org/t10/drafts/mmc6](https://www.microsoft.com/?ref=go).</span><span class="sxs-lookup"><span data-stu-id="a9498-110">Developers may benefit from a familiarity with the latest revision of Multimedia Command (MMC) at [ftp://ftp.t10.org/t10/drafts/mmc6](https://www.microsoft.com/?ref=go).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="a9498-111">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="a9498-111">Run-time requirements</span></span>

<span data-ttu-id="a9498-112">IMAPI 2.0 è supportato in modo nativo a partire da Windows Vista e Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="a9498-112">IMAPI 2.0 is supported natively starting with Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="a9498-113">L'abilitazione della funzionalità IMAPI 2.0 per Windows XP e Windows Server 2003 richiede l'installazione del pacchetto di aggiornamento [KB932716.](https://support.microsoft.com/kb/932716)</span><span class="sxs-lookup"><span data-stu-id="a9498-113">Enabling IMAPI 2.0 functionality for Windows XP and Windows Server 2003 requires the installation of the [KB932716](https://support.microsoft.com/kb/932716) update package.</span></span> <span data-ttu-id="a9498-114">Se questo pacchetto non è installato, Windows XP supporta ancora in modo nativo [IMAPI 1.0.](imapiv1.md)</span><span class="sxs-lookup"><span data-stu-id="a9498-114">If this package is not installed, Windows XP still natively supports [IMAPI 1.0](imapiv1.md).</span></span>

> [!Note]  
> <span data-ttu-id="a9498-115">Il Feature Pack di Windows per l'archiviazione è disponibile al pubblico tramite [l'Area download Microsoft.](https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05)</span><span class="sxs-lookup"><span data-stu-id="a9498-115">The Windows Feature Pack for Storage is available to the public via the [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05).</span></span> <span data-ttu-id="a9498-116">Altre informazioni sulle modifiche specifiche [dell'API](what-s-new.md) sono disponibili nella sezione Novità.</span><span class="sxs-lookup"><span data-stu-id="a9498-116">Additional information regarding specific API changes can be found in the [What's New](what-s-new.md) section.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="a9498-117">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="a9498-117">In this section</span></span>



| <span data-ttu-id="a9498-118">Argomento</span><span class="sxs-lookup"><span data-stu-id="a9498-118">Topic</span></span>                                             | <span data-ttu-id="a9498-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a9498-119">Description</span></span>                                                                           |
|---------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="a9498-120">Novità</span><span class="sxs-lookup"><span data-stu-id="a9498-120">What's New</span></span>](what-s-new.md)<br/>           | <span data-ttu-id="a9498-121">Informazioni dettagliate su ogni versione significativa dell'API Image Mastering.</span><span class="sxs-lookup"><span data-stu-id="a9498-121">Information detailing each significant release of the Image Mastering API.</span></span><br/> |
| [<span data-ttu-id="a9498-122">Informazioni su IMAPI</span><span class="sxs-lookup"><span data-stu-id="a9498-122">About IMAPI</span></span>](about-imapi.md)<br/>         | <span data-ttu-id="a9498-123">Informazioni generali sull'API Image Mastering.</span><span class="sxs-lookup"><span data-stu-id="a9498-123">General information about the Image Mastering API.</span></span><br/>                         |
| [<span data-ttu-id="a9498-124">Uso di IMAPI</span><span class="sxs-lookup"><span data-stu-id="a9498-124">Using IMAPI</span></span>](using-imapi.md)<br/>         | <span data-ttu-id="a9498-125">Argomenti relativi alle attività che illustrano come usare l'API Image Mastering.</span><span class="sxs-lookup"><span data-stu-id="a9498-125">Task-related topics that demonstrate how to use the Image Mastering API.</span></span><br/>   |
| [<span data-ttu-id="a9498-126">Informazioni di riferimento su IMAPI</span><span class="sxs-lookup"><span data-stu-id="a9498-126">IMAPI Reference</span></span>](imapi-reference.md)<br/> | <span data-ttu-id="a9498-127">Descrizioni dettagliate delle interfacce IMAPI e di altri elementi di programmazione.</span><span class="sxs-lookup"><span data-stu-id="a9498-127">Detailed descriptions of IMAPI interfaces and other programming elements.</span></span><br/>  |



 

## <a name="additional-resources"></a><span data-ttu-id="a9498-128">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="a9498-128">Additional resources</span></span>

<span data-ttu-id="a9498-129">Altre informazioni su IMAPI e altri argomenti correlati sono disponibili nelle posizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="a9498-129">Further information regarding IMAPI and other related subjects can be found at the following locations:</span></span>



|                                                                                                  |                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a9498-130">Microsoft Optical Storage Blog</span><span class="sxs-lookup"><span data-stu-id="a9498-130">Microsoft Optical Storage Blog</span></span>](/archive/blogs/opticalstorage/)                | <span data-ttu-id="a9498-131">Vengono evidenziati argomenti incentrati sull'implementazione dell'API Image Mastering negli scenari di sviluppo reali.</span><span class="sxs-lookup"><span data-stu-id="a9498-131">Highlights topics that focus on the implementation of the Image Mastering API in real world development scenarios.</span></span>                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="a9498-132">Forum di discussione sulla piattaforma ottica</span><span class="sxs-lookup"><span data-stu-id="a9498-132">Optical Platform Discussion Forum</span></span>](https://social.msdn.microsoft.com/forums/windowsopticalplatform/threads/)              | <span data-ttu-id="a9498-133">Illustrare CDROM.SYS, IMAPIv2 e Live File System problemi.</span><span class="sxs-lookup"><span data-stu-id="a9498-133">Discuss CDROM.SYS, IMAPIv2 and Live File System issues.</span></span> <span data-ttu-id="a9498-134">Questo forum è in particolare sugli argomenti a livello di sistema ed è destinato agli sviluppatori di applicazioni anziché agli utenti finali.</span><span class="sxs-lookup"><span data-stu-id="a9498-134">This forum focuses on system-level topics and is intended for application developers rather than endusers.</span></span>                                                                                                                                                                                                 |
| [<span data-ttu-id="a9498-135">Comitato tecnico T10</span><span class="sxs-lookup"><span data-stu-id="a9498-135">T10 Technical Committee</span></span>](https://www.t10.org/)                       | <span data-ttu-id="a9498-136">Un comitato tecnico del comitato internazionale per gli standard di information technology (INCITS, pronunciato "insights").</span><span class="sxs-lookup"><span data-stu-id="a9498-136">A Technical Committee of the InterNational Committee on Information Technology Standards (INCITS, pronounced "insights").</span></span> <span data-ttu-id="a9498-137">INCITS è accreditato da e opera in base alle regole approvate da, American National Standards Institute (ANSI).</span><span class="sxs-lookup"><span data-stu-id="a9498-137">INCITS is accredited by, and operates under rules that are approved by, the American National Standards Institute (ANSI).</span></span> <span data-ttu-id="a9498-138">Queste regole sono progettate per garantire che gli standard volontari siano sviluppati dal consenso dei gruppi di settore.</span><span class="sxs-lookup"><span data-stu-id="a9498-138">These rules are designed to ensure that voluntary standards are developed by the consensus of industry groups.</span></span> |
| [<span data-ttu-id="a9498-139">OSTA (Optical Storage Technology Association)</span><span class="sxs-lookup"><span data-stu-id="a9498-139">Optical Storage Technology Association (OSTA)</span></span>](http://www.osta.org/) | <span data-ttu-id="a9498-140">Funziona per modellare il futuro del settore tramite riunioni regolari di commercial optical storage applications (COSA), compatibilità DVD, marketing, MPV (MusicPhotoVideo), i comitato UDF e un nuovo comitato adhoc Blue Laser.</span><span class="sxs-lookup"><span data-stu-id="a9498-140">Works to shape the future of the industry through regular meetings of Commercial Optical Storage Applications (COSA), DVD Compatibility, Marketing, MPV (MusicPhotoVideo), UDF committees, and a new adhoc Blue Laser committee.</span></span> <span data-ttu-id="a9498-141">Le aziende interessate in tutto il mondo sono invitate a unirsi all'organizzazione e a partecipare ai relativi programmi e commissioni.</span><span class="sxs-lookup"><span data-stu-id="a9498-141">Interested companies worldwide are invited to join the organization and participate in its committees and programs.</span></span>               |



 

 

