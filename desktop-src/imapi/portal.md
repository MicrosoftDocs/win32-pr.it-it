---
title: API per la creazione di immagini master
description: .
ms.assetid: 4902d3fb-3195-4909-ab64-28f8a77ba14c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc23c972cf111dee5edf3cb014a52351eda3605e
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "103963536"
---
# <a name="image-mastering-api"></a><span data-ttu-id="6b713-103">API per la creazione di immagini master</span><span class="sxs-lookup"><span data-stu-id="6b713-103">Image Mastering API</span></span>

## <a name="purpose"></a><span data-ttu-id="6b713-104">Scopo</span><span class="sxs-lookup"><span data-stu-id="6b713-104">Purpose</span></span>

<span data-ttu-id="6b713-105">L'API per la gestione delle immagini di Microsoft Windows consente alle applicazioni di organizzare e masterizzare immagini in supporti di archiviazione ottica CD, DVD e blu-ray.</span><span class="sxs-lookup"><span data-stu-id="6b713-105">The Microsoft Windows image mastering API enables applications to stage and burn images to CD, DVD, and Blu-ray optical storage media.</span></span> <span data-ttu-id="6b713-106">Anche altri supporti di tipo disco che dispongono di immagini nello stesso modo possono usare questa API.</span><span class="sxs-lookup"><span data-stu-id="6b713-106">Other disc-like media that lay images in the same manner can also use this API.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="6b713-107">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="6b713-107">Developer audience</span></span>

<span data-ttu-id="6b713-108">IMAPi è progettato per C/C++ e Visual Basic gli sviluppatori e per quelli che scrivono script che usano VBScript.</span><span class="sxs-lookup"><span data-stu-id="6b713-108">IMAPI is designed for C/C++ and Visual Basic developers and those writing scripts using VBScript.</span></span>

<span data-ttu-id="6b713-109">È consigliabile conoscere le tecnologie CD, DVD e blu-ray e i file System.</span><span class="sxs-lookup"><span data-stu-id="6b713-109">Knowledge of CD, DVD, and Blu-ray technologies and file systems is recommended.</span></span> <span data-ttu-id="6b713-110">Gli sviluppatori possono trarre vantaggio da una certa familiarità con la revisione più recente del comando multimediale (MMC) in [FTP://FTP.T10.org/T10/Drafts/MMC6](https://www.microsoft.com/?ref=go).</span><span class="sxs-lookup"><span data-stu-id="6b713-110">Developers may benefit from a familiarity with the latest revision of Multimedia Command (MMC) at [ftp://ftp.t10.org/t10/drafts/mmc6](https://www.microsoft.com/?ref=go).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="6b713-111">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="6b713-111">Run-time requirements</span></span>

<span data-ttu-id="6b713-112">IMAPi 2,0 è supportato a livello nativo a partire da Windows Vista e Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="6b713-112">IMAPI 2.0 is supported natively starting with Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="6b713-113">Per abilitare la funzionalità IMAPi 2,0 per Windows XP e Windows Server 2003, è necessario installare il pacchetto di aggiornamento [KB932716](https://support.microsoft.com/kb/932716) .</span><span class="sxs-lookup"><span data-stu-id="6b713-113">Enabling IMAPI 2.0 functionality for Windows XP and Windows Server 2003 requires the installation of the [KB932716](https://support.microsoft.com/kb/932716) update package.</span></span> <span data-ttu-id="6b713-114">Se il pacchetto non è installato, Windows XP supporta ancora in modo nativo [imapi 1,0](imapiv1.md).</span><span class="sxs-lookup"><span data-stu-id="6b713-114">If this package is not installed, Windows XP still natively supports [IMAPI 1.0](imapiv1.md).</span></span>

> [!Note]  
> <span data-ttu-id="6b713-115">Il Feature Pack di Windows per l'archiviazione è disponibile per il pubblico tramite l' [area download Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05).</span><span class="sxs-lookup"><span data-stu-id="6b713-115">The Windows Feature Pack for Storage is available to the public via the [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05).</span></span> <span data-ttu-id="6b713-116">Ulteriori informazioni relative alle modifiche specifiche dell'API sono disponibili nella sezione [novità](what-s-new.md) .</span><span class="sxs-lookup"><span data-stu-id="6b713-116">Additional information regarding specific API changes can be found in the [What's New](what-s-new.md) section.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="6b713-117">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="6b713-117">In this section</span></span>



| <span data-ttu-id="6b713-118">Argomento</span><span class="sxs-lookup"><span data-stu-id="6b713-118">Topic</span></span>                                             | <span data-ttu-id="6b713-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6b713-119">Description</span></span>                                                                           |
|---------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="6b713-120">Novità</span><span class="sxs-lookup"><span data-stu-id="6b713-120">What's New</span></span>](what-s-new.md)<br/>           | <span data-ttu-id="6b713-121">Informazioni che descrivono in dettaglio ogni versione significativa dell'API per la creazione di immagini master.</span><span class="sxs-lookup"><span data-stu-id="6b713-121">Information detailing each significant release of the Image Mastering API.</span></span><br/> |
| [<span data-ttu-id="6b713-122">Informazioni su IMAPi</span><span class="sxs-lookup"><span data-stu-id="6b713-122">About IMAPI</span></span>](about-imapi.md)<br/>         | <span data-ttu-id="6b713-123">Informazioni generali sull'API per la creazione di immagini master.</span><span class="sxs-lookup"><span data-stu-id="6b713-123">General information about the Image Mastering API.</span></span><br/>                         |
| [<span data-ttu-id="6b713-124">Uso di IMAPi</span><span class="sxs-lookup"><span data-stu-id="6b713-124">Using IMAPI</span></span>](using-imapi.md)<br/>         | <span data-ttu-id="6b713-125">Argomenti correlati alle attività che illustrano come usare l'API per la creazione di immagini master.</span><span class="sxs-lookup"><span data-stu-id="6b713-125">Task-related topics that demonstrate how to use the Image Mastering API.</span></span><br/>   |
| [<span data-ttu-id="6b713-126">Riferimento a IMAPi</span><span class="sxs-lookup"><span data-stu-id="6b713-126">IMAPI Reference</span></span>](imapi-reference.md)<br/> | <span data-ttu-id="6b713-127">Descrizioni dettagliate delle interfacce IMAPi e altri elementi di programmazione.</span><span class="sxs-lookup"><span data-stu-id="6b713-127">Detailed descriptions of IMAPI interfaces and other programming elements.</span></span><br/>  |



 

## <a name="additional-resources"></a><span data-ttu-id="6b713-128">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="6b713-128">Additional resources</span></span>

<span data-ttu-id="6b713-129">Altre informazioni su IMAPi e altri argomenti correlati sono disponibili nelle posizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="6b713-129">Further information regarding IMAPI and other related subjects can be found at the following locations:</span></span>



|                                                                                                  |                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6b713-130">Blog di Microsoft Optical Storage</span><span class="sxs-lookup"><span data-stu-id="6b713-130">Microsoft Optical Storage Blog</span></span>](/archive/blogs/opticalstorage/)                | <span data-ttu-id="6b713-131">Mette in evidenza gli argomenti che si concentrano sull'implementazione dell'API Master immagini negli scenari di sviluppo reali.</span><span class="sxs-lookup"><span data-stu-id="6b713-131">Highlights topics that focus on the implementation of the Image Mastering API in real world development scenarios.</span></span>                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="6b713-132">Forum di discussione sulla piattaforma ottica</span><span class="sxs-lookup"><span data-stu-id="6b713-132">Optical Platform Discussion Forum</span></span>](https://social.msdn.microsoft.com/forums/windowsopticalplatform/threads/)              | <span data-ttu-id="6b713-133">Esaminare CDROM.SYS, IMAPIv2 e i problemi del file System Live.</span><span class="sxs-lookup"><span data-stu-id="6b713-133">Discuss CDROM.SYS, IMAPIv2 and Live File System issues.</span></span> <span data-ttu-id="6b713-134">Questo forum è incentrato sugli argomenti a livello di sistema ed è destinato agli sviluppatori di applicazioni invece che agli sviluppatori.</span><span class="sxs-lookup"><span data-stu-id="6b713-134">This forum focuses on system-level topics and is intended for application developers rather than endusers.</span></span>                                                                                                                                                                                                 |
| [<span data-ttu-id="6b713-135">Comitato tecnico T10</span><span class="sxs-lookup"><span data-stu-id="6b713-135">T10 Technical Committee</span></span>](https://www.t10.org/)                       | <span data-ttu-id="6b713-136">Un comitato tecnico del Comitato internazionale per gli standard Information Technology (INCIs), pronunciato "Insights".</span><span class="sxs-lookup"><span data-stu-id="6b713-136">A Technical Committee of the InterNational Committee on Information Technology Standards (INCITS, pronounced "insights").</span></span> <span data-ttu-id="6b713-137">Gli INCI sono accreditati da e operano con regole approvate da, il American National Standards Institute (ANSI).</span><span class="sxs-lookup"><span data-stu-id="6b713-137">INCITS is accredited by, and operates under rules that are approved by, the American National Standards Institute (ANSI).</span></span> <span data-ttu-id="6b713-138">Queste regole sono progettate per garantire che gli standard volontari siano sviluppati dal consenso dei gruppi di settore.</span><span class="sxs-lookup"><span data-stu-id="6b713-138">These rules are designed to ensure that voluntary standards are developed by the consensus of industry groups.</span></span> |
| [<span data-ttu-id="6b713-139">Associazione di tecnologie di archiviazione ottica (OSTA)</span><span class="sxs-lookup"><span data-stu-id="6b713-139">Optical Storage Technology Association (OSTA)</span></span>](http://www.osta.org/) | <span data-ttu-id="6b713-140">Funziona per definire il futuro del settore attraverso riunioni regolari di applicazioni di archiviazione ottica (COSA), compatibilità dei DVD, marketing, MPV (MusicPhotoVideo), comitati UDF e un nuovo comitato di laser Blue ad hoc.</span><span class="sxs-lookup"><span data-stu-id="6b713-140">Works to shape the future of the industry through regular meetings of Commercial Optical Storage Applications (COSA), DVD Compatibility, Marketing, MPV (MusicPhotoVideo), UDF committees, and a new adhoc Blue Laser committee.</span></span> <span data-ttu-id="6b713-141">Le aziende interessate in tutto il mondo sono invitati a partecipare all'organizzazione e a partecipare ai suoi comitati e programmi.</span><span class="sxs-lookup"><span data-stu-id="6b713-141">Interested companies worldwide are invited to join the organization and participate in its committees and programs.</span></span>               |



 

 

