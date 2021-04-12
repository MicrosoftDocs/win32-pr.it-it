---
title: Metafile di Windows Media
description: Metafile di Windows Media
ms.assetid: 77af7d15-52ac-496c-8037-51827adf0250
keywords:
- Metafile di Windows Media, informazioni
- Windows Media Player, metafile
- Windows Media Player, metafile di Windows Media
- Metafile, informazioni
- Windows Media, metafile
- Playlist Windows Media Metafile, informazioni
- playlist, informazioni
- playlist di metafile, informazioni
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 385b149e07e9d30df4e11a21f8e7aa4b05e06910
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330052"
---
# <a name="windows-media-metafiles"></a><span data-ttu-id="766da-111">Metafile di Windows Media</span><span class="sxs-lookup"><span data-stu-id="766da-111">Windows Media Metafiles</span></span>

<span data-ttu-id="766da-112">Questo documento di riferimento illustra i metafile di Windows Media, che usano le estensioni di file. Wax,. wvx,. WMX e. asx.</span><span class="sxs-lookup"><span data-stu-id="766da-112">This reference documents Windows Media metafiles, which use the .wax, .wvx, .wmx, and .asx file name extensions.</span></span> <span data-ttu-id="766da-113">Contiene le sezioni Panoramica e guida alla programmazione e una sezione di riferimento completa sui tag dell'elemento metafile, i relativi attributi e valori e le condizioni speciali correlate a ogni elemento.</span><span class="sxs-lookup"><span data-stu-id="766da-113">It contains overview and programming guide sections, and a full reference section on metafile element tags, their attributes and values, and special conditions related to each element.</span></span>

<span data-ttu-id="766da-114">Un metafile è un file che contiene informazioni su altri file.</span><span class="sxs-lookup"><span data-stu-id="766da-114">A metafile is a file that contains information about other files.</span></span> <span data-ttu-id="766da-115">Un metafile può essere usato per elencare un gruppo di file di contenuto multimediale che devono essere riprodotti nell'ordine.</span><span class="sxs-lookup"><span data-stu-id="766da-115">A metafile can be used to list a group of media content files that are to be played in order.</span></span> <span data-ttu-id="766da-116">Le playlist Windows Media Metafile, denominate semplicemente playlist in questo documento di riferimento, sono una delle funzionalità più potenti delle tecnologie Microsoft Windows Media.</span><span class="sxs-lookup"><span data-stu-id="766da-116">Windows Media metafile playlists, simply referred to as playlists in this reference document, are one of the most powerful features of Microsoft Windows Media Technologies.</span></span> <span data-ttu-id="766da-117">Le playlist consentono di controllare e personalizzare il contenuto multimediale.</span><span class="sxs-lookup"><span data-stu-id="766da-117">Playlists allow you to control and customize your media content.</span></span> <span data-ttu-id="766da-118">Ad esempio, con le playlist è possibile pianificare il contenuto per la riproduzione in successione o inserire clip pubblicitari o di interesse speciale in una presentazione.</span><span class="sxs-lookup"><span data-stu-id="766da-118">For instance, with playlists you can schedule content to play in succession or insert advertising or special interest clips into a presentation.</span></span> <span data-ttu-id="766da-119">Un ulteriore vantaggio delle playlist è che, anziché riprodurre un flusso, arrestare, avviare il flusso successivo e quindi attendere il completamento del buffer, servizi Windows Media e Windows Media Player interagiscono per riprodurre i clip uno dopo l'altro con un tempo minimo di buffering o un'interruzione tra di essi.</span><span class="sxs-lookup"><span data-stu-id="766da-119">A further advantage of playlists is that instead of playing a stream, stopping, starting the next stream, and then waiting for it to finish buffering, Windows Media Services and Windows Media Player work together to play the clips one after the other with minimal buffering time or interruption between them.</span></span>

<span data-ttu-id="766da-120">Le tecnologie Windows Media e altri prodotti Internet forniscono gli strumenti per comprendere i dati demografici degli utenti e personalizzare dinamicamente una trasmissione o un messaggio per singoli utenti.</span><span class="sxs-lookup"><span data-stu-id="766da-120">Windows Media Technologies and other Internet products provide you with the tools to understand user demographics and dynamically customize a broadcast or message for individual users.</span></span>

<span data-ttu-id="766da-121">Questo riferimento è suddiviso nelle sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="766da-121">This reference is divided into the following sections.</span></span>



| <span data-ttu-id="766da-122">Sezione</span><span class="sxs-lookup"><span data-stu-id="766da-122">Section</span></span>                                                                  | <span data-ttu-id="766da-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="766da-123">Description</span></span>                                                                                                                                                                         |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="766da-124">Informazioni sui metafile di Windows Media</span><span class="sxs-lookup"><span data-stu-id="766da-124">About Windows Media Metafiles</span></span>](about-windows-media-metafiles.md)       | <span data-ttu-id="766da-125">Introduce gli elementi metafile di Windows Media e ne illustra lo scopo.</span><span class="sxs-lookup"><span data-stu-id="766da-125">Introduces Windows Media metafile elements and discusses their purpose.</span></span>                                                                                                             |
| [<span data-ttu-id="766da-126">Guida ai metafile di Windows Media</span><span class="sxs-lookup"><span data-stu-id="766da-126">Windows Media Metafile Guide</span></span>](windows-media-metafile-guide.md)         | <span data-ttu-id="766da-127">Descrive i passaggi necessari per la creazione di metafile.</span><span class="sxs-lookup"><span data-stu-id="766da-127">Details the steps necessary for creating metafiles.</span></span> <span data-ttu-id="766da-128">Gli esempi illustrano come usare i tag di elemento per attività specifiche.</span><span class="sxs-lookup"><span data-stu-id="766da-128">Examples illustrate how to use element tags for specific tasks.</span></span>                                                                 |
| [<span data-ttu-id="766da-129">Informazioni di riferimento sui metafile di Windows Media</span><span class="sxs-lookup"><span data-stu-id="766da-129">Windows Media Metafile Reference</span></span>](windows-media-metafile-reference.md) | <span data-ttu-id="766da-130">Vengono illustrati in dettaglio ogni elemento metafile, i relativi attributi e valori e le condizioni speciali correlate a ciascuna di esse.</span><span class="sxs-lookup"><span data-stu-id="766da-130">Explains in detail each of the metafile elements, their attributes and values, and special conditions related to each.</span></span> <span data-ttu-id="766da-131">Vengono illustrate le estensioni dei nomi di file di metafile e l'utilizzo appropriato.</span><span class="sxs-lookup"><span data-stu-id="766da-131">Explains metafile file name extensions and their proper use.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="766da-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="766da-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="766da-133">**Windows Media Player SDK**</span><span class="sxs-lookup"><span data-stu-id="766da-133">**Windows Media Player SDK**</span></span>](windows-media-player-sdk.md)
</dt> </dl>

 

 




