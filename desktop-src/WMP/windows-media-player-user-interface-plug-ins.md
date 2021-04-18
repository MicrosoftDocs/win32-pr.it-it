---
title: Plug-in di interfaccia utente di Windows Media Player
description: Plug-in di interfaccia utente di Windows Media Player
ms.assetid: 71f53abe-310f-429a-bb23-5291bebdc432
keywords:
- Windows Media Player, plug-in
- Windows Media Player, plug-in dell'interfaccia utente
- Plug-in di Windows Media Player, interfaccia utente
- plug-in, interfaccia utente
- plug-in dell'interfaccia utente, informazioni
- Plug-in dell'interfaccia utente, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24050f24ef4412d3de9efd5faac6c2af90451dc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298039"
---
# <a name="windows-media-player-user-interface-plug-ins"></a><span data-ttu-id="6cc92-109">Plug-in di interfaccia utente di Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="6cc92-109">Windows Media Player User Interface Plug-ins</span></span>

<span data-ttu-id="6cc92-110">Microsoft Windows Media Player offre un'architettura che consente all'utente di installare e attivare programmi plug-in che aggiungono funzionalità dell'interfaccia utente alla modalità completa del lettore.</span><span class="sxs-lookup"><span data-stu-id="6cc92-110">Microsoft Windows Media Player provides an architecture that enables the user to install and activate plug-in programs that add user interface (UI) functionality to the full mode of the player.</span></span> <span data-ttu-id="6cc92-111">Un plug-in di interfaccia utente tipico potrebbe consentire a un utente di acquistare il CD che contiene la traccia attualmente in riproduzione o di accedere a informazioni aggiuntive sull'artista.</span><span class="sxs-lookup"><span data-stu-id="6cc92-111">A typical UI plug-in might allow a user to buy the CD that contains the currently playing track or to access additional information about the artist.</span></span> <span data-ttu-id="6cc92-112">Questa sezione di Windows Media Player Software Development Kit (SDK) fornisce le informazioni di programmazione necessarie per creare il plug-in dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="6cc92-112">This section of the Windows Media Player Software Development Kit (SDK) provides you with the programming information you need to create your own UI plug-in.</span></span>

<span data-ttu-id="6cc92-113">La documentazione del plug-in dell'interfaccia utente è divisa in tre sezioni:</span><span class="sxs-lookup"><span data-stu-id="6cc92-113">The UI plug-in documentation is divided into three sections:</span></span>



| <span data-ttu-id="6cc92-114">Sezione</span><span class="sxs-lookup"><span data-stu-id="6cc92-114">Section</span></span>                                                                                            | <span data-ttu-id="6cc92-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6cc92-115">Description</span></span>                                                                                                                                   |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6cc92-116">Informazioni sui plug-in dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="6cc92-116">About User Interface Plug-ins</span></span>](about-user-interface-plug-ins.md)                                 | <span data-ttu-id="6cc92-117">Viene fornita una panoramica dell'architettura utilizzata per i plug-in dell'interfaccia utente. Leggere questa sezione per informazioni sui concetti generali relativi a questa tecnologia.</span><span class="sxs-lookup"><span data-stu-id="6cc92-117">Provides an overview of the architecture used for UI plug-ins. Read this section to learn the general concepts involved with this technology.</span></span> |
| [<span data-ttu-id="6cc92-118">Guida alla programmazione di plug-in dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="6cc92-118">User Interface Plug-ins Programming Guide</span></span>](user-interface-plug-ins-programming-guide.md)         | <span data-ttu-id="6cc92-119">Vengono illustrate le operazioni necessarie per creare un plug-in dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="6cc92-119">Explains what you need to do to create a UI plug-in.</span></span> <span data-ttu-id="6cc92-120">In questa sezione sono contenuti esempi di codice e procedure dettagliate.</span><span class="sxs-lookup"><span data-stu-id="6cc92-120">This section contains example code and step-by-step procedures.</span></span>                          |
| [<span data-ttu-id="6cc92-121">Guida di riferimento alla programmazione di plug-in dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="6cc92-121">User Interface Plug-ins Programming Reference</span></span>](user-interface-plug-ins-programming-reference.md) | <span data-ttu-id="6cc92-122">Fornisce un riferimento dettagliato per l'interfaccia COM e i metodi supportati dai plug-in Windows Media Player SDK per l'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="6cc92-122">Provides a detailed reference for the COM interface and methods supported by the Windows Media Player SDK for UI plug-ins.</span></span>                    |



 

> [!Note]  
> <span data-ttu-id="6cc92-123">Windows Media Player 10 Mobile fornisce lo stesso modello di plug-in di Windows Desktop Media Player.</span><span class="sxs-lookup"><span data-stu-id="6cc92-123">Windows Media Player 10 Mobile provides the same plug-in model as the desktop Windows Media Player.</span></span> <span data-ttu-id="6cc92-124">Questo modello di plug-in consente di usare i plug-in in background per monitorare gli eventi, visualizzare lo stato delle proprietà e così via.</span><span class="sxs-lookup"><span data-stu-id="6cc92-124">This plug-in model enables you to use background plug-ins for monitoring events, displaying the status of properties, and so on.</span></span> <span data-ttu-id="6cc92-125">La Guida di programmazione di questa sezione descrive come creare un plug-in di interfaccia utente in background per Windows Media Player 10 mobile usando la procedura guidata plug-in per desktop Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="6cc92-125">The programming guide in this section describes how to create a background UI plug-in for Windows Media Player 10 Mobile by using the desktop Windows Media Player Plug-in Wizard.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6cc92-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6cc92-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6cc92-127">**Plug-in di Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="6cc92-127">**Windows Media Player Plug-ins**</span></span>](windows-media-player-plug-ins.md)
</dt> </dl>

 

 




