---
description: La responsabilità principale di qualsiasi elemento del pannello di controllo consiste nel visualizzare una finestra che consente all'utente di visualizzare e modificare le impostazioni.
title: Linee guida sull'esperienza utente
ms.topic: article
ms.date: 09/24/2020
ms.assetid: f03a154b-9781-4718-8244-3d57fee0755e
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e25f8885c2444a51d5d5d8cc917121c7f3b26a09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995101"
---
# <a name="user-experience-guidelines"></a><span data-ttu-id="cf526-103">Linee guida sull'esperienza utente</span><span class="sxs-lookup"><span data-stu-id="cf526-103">User Experience Guidelines</span></span>

<span data-ttu-id="cf526-104">La responsabilità principale di qualsiasi elemento del pannello di controllo consiste nel visualizzare una finestra che consente all'utente di visualizzare e modificare le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="cf526-104">The primary responsibility of any Control Panel item is to display a window that allows the user to view and manipulate settings.</span></span> <span data-ttu-id="cf526-105">Vedere le [linee guida sull'esperienza utente dei pannelli di controllo](../uxguide/winenv-ctrl-panels.md) per il comportamento e la progettazione degli elementi del pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="cf526-105">See the [Control Panels user experience (UX) guidelines](../uxguide/winenv-ctrl-panels.md) for the behavior and design of Control Panel items.</span></span> <span data-ttu-id="cf526-106">Le linee guida descritte in questo argomento mostrano un metodo del flusso di attività per organizzare un elemento del pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="cf526-106">The guidelines discussed in that topic show a task flow method of organizing a Control Panel item.</span></span> <span data-ttu-id="cf526-107">Questa operazione inserisce le impostazioni più importanti in un home page.</span><span class="sxs-lookup"><span data-stu-id="cf526-107">This places the most important settings on a home page.</span></span> <span data-ttu-id="cf526-108">Le impostazioni usate meno di frequente vengono inserite nelle pagine spoke o a cui è possibile accedere dai collegamenti in un riquadro laterale.</span><span class="sxs-lookup"><span data-stu-id="cf526-108">Less frequently used settings are placed on spoke pages or accessed from links in a side pane.</span></span>

<span data-ttu-id="cf526-109">Il pannello di controllo include molti elementi che seguono queste linee guida, ad esempio la facilità di accesso al centro e la rete e la condivisione.</span><span class="sxs-lookup"><span data-stu-id="cf526-109">The Control Panel includes many items that follow these guidelines, such as Ease of Access Center and Network and Sharing Center.</span></span> <span data-ttu-id="cf526-110">Gli altri elementi del pannello di controllo usano il formato della finestra delle proprietà della finestra di dialogo a schede come nelle versioni precedenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="cf526-110">Other Control Panel items use the tabbed dialog property sheet format as in earlier versions of Windows.</span></span> <span data-ttu-id="cf526-111">Gli esempi includono l'elemento del mouse e le opzioni Internet.</span><span class="sxs-lookup"><span data-stu-id="cf526-111">Examples include the Mouse item and Internet Options.</span></span> <span data-ttu-id="cf526-112">L'utilizzo del formato della finestra delle proprietà deve essere sospeso.</span><span class="sxs-lookup"><span data-stu-id="cf526-112">Use of the property sheet format should be discontinued.</span></span> <span data-ttu-id="cf526-113">Se si creano nuovi elementi del pannello di controllo, è necessario seguire le linee guida per il flusso di attività.</span><span class="sxs-lookup"><span data-stu-id="cf526-113">If you create new Control Panel items, you should follow the task flow guidelines.</span></span>

<span data-ttu-id="cf526-114">In passato, gli elementi del pannello di controllo venivano inclusi in un pacchetto come file con estensione CPL.</span><span class="sxs-lookup"><span data-stu-id="cf526-114">In the past, Control Panel items were packaged as .cpl files.</span></span> <span data-ttu-id="cf526-115">Non è più necessario.</span><span class="sxs-lookup"><span data-stu-id="cf526-115">That is no longer necessary.</span></span> <span data-ttu-id="cf526-116">È necessario implementare nuovi elementi del pannello di controllo come file exe autonomo o come opzione di flag della riga di comando per il file eseguibile principale dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cf526-116">New Control Panel items should be implemented as a standalone .exe file or as a command-line flag option for the application's main executable file.</span></span>

> [!Note]  
> <span data-ttu-id="cf526-117">Nei sistemi a 64 bit gli elementi del pannello di controllo a 32 bit vengono visualizzati nel pannello di controllo quando è selezionata l'opzione **Visualizza cartella elementi del pannello di controllo 32-bit** .</span><span class="sxs-lookup"><span data-stu-id="cf526-117">On 64-bit systems, 32-bit Control Panel items are displayed in the Control Panel when the **View 32-bit Control Panel Items folder** option is selected.</span></span> <span data-ttu-id="cf526-118">Gli elementi a 32 bit devono trovarsi nella cartella% SystemRoot% \\ SysWow64 da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="cf526-118">The 32-bit items must be located in the %SystemRoot%\\SysWOW64 folder to be displayed.</span></span> <span data-ttu-id="cf526-119">Non richiedono ulteriori registrazioni.</span><span class="sxs-lookup"><span data-stu-id="cf526-119">They do not require any further registration.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="cf526-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cf526-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf526-121">Elementi del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="cf526-121">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="cf526-122">Registrazione degli elementi del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="cf526-122">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="cf526-123">Uso di CPLApplet</span><span class="sxs-lookup"><span data-stu-id="cf526-123">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="cf526-124">Elaborazione del messaggio del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="cf526-124">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="cf526-125">Esecuzione degli elementi del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="cf526-125">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="cf526-126">Estensione degli elementi del pannello di controllo di sistema</span><span class="sxs-lookup"><span data-stu-id="cf526-126">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="cf526-127">Assegnazione delle categorie del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="cf526-127">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
</dt> <dt>

[<span data-ttu-id="cf526-128">Creazione di collegamenti alle attività ricercabili per un elemento del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="cf526-128">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
</dt> <dt>

[<span data-ttu-id="cf526-129">Accesso al pannello di controllo in modalità provvisoria</span><span class="sxs-lookup"><span data-stu-id="cf526-129">Accessing the Control Panel in Safe Mode</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 



