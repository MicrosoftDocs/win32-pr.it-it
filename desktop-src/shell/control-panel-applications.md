---
description: Gli elementi del pannello di controllo sono file dll o eseguibili (exe) che consentono agli utenti di configurare l'ambiente di Windows. In genere, è possibile accedervi facendo clic su un'icona nel pannello di controllo.
title: Implementazione degli elementi del pannello di controllo
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2e61cbc0-fbb5-4680-8123-f8ffdcf98210
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 310d01f07d40cef69c6be30231bbf4780a1d8838
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977367"
---
# <a name="implementing-control-panel-items"></a><span data-ttu-id="759fe-104">Implementazione degli elementi del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="759fe-104">Implementing Control Panel Items</span></span>

<span data-ttu-id="759fe-105">Gli elementi del pannello di controllo sono file dll o eseguibili (exe) che consentono agli utenti di configurare l'ambiente di Windows.</span><span class="sxs-lookup"><span data-stu-id="759fe-105">Control Panel items are DLLs or executable (.exe) files that let users configure the environment of Windows.</span></span> <span data-ttu-id="759fe-106">In genere, è possibile accedervi facendo clic su un'icona nel pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="759fe-106">They are typically accessed by clicking an icon in the Control Panel.</span></span>

<span data-ttu-id="759fe-107">In questa sezione vengono descritti gli elementi del pannello di controllo e viene illustrato come crearli e registrarli in modo che vengano visualizzati in modo appropriato nel pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="759fe-107">This section describes Control Panel items and explains how to create and register them so that they appear appropriately in the Control Panel.</span></span> <span data-ttu-id="759fe-108">Per Windows Vista, sono incluse informazioni che indicano come aggiungere collegamenti alle attività visualizzate sotto l'elemento del pannello di controllo e nei risultati della ricerca del pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="759fe-108">For Windows Vista, information is included that tells you how to add task links that appear under the Control Panel item and in Control Panel search results.</span></span>

-   [<span data-ttu-id="759fe-109">Linee guida sull'esperienza utente</span><span class="sxs-lookup"><span data-stu-id="759fe-109">User Experience Guidelines</span></span>](user-experience-guidelines.md)
-   [<span data-ttu-id="759fe-110">Registrazione degli elementi del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="759fe-110">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
-   [<span data-ttu-id="759fe-111">Come registrare gli elementi del pannello di controllo eseguibile</span><span class="sxs-lookup"><span data-stu-id="759fe-111">How To Register Executable Control Panel Items</span></span>](how-to-register-an-executable-control-panel-item-registration-.md)
-   [<span data-ttu-id="759fe-112">Come registrare gli elementi del pannello di controllo DLL</span><span class="sxs-lookup"><span data-stu-id="759fe-112">How To Register DLL Control Panel Items</span></span>](how-to-register-dll-control-panel-item-registration-.md)
-   [<span data-ttu-id="759fe-113">Uso di CPLApplet</span><span class="sxs-lookup"><span data-stu-id="759fe-113">Using CPLApplet</span></span>](using-cplapplet.md)
-   [<span data-ttu-id="759fe-114">Elaborazione del messaggio del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="759fe-114">Control Panel Message Processing</span></span>](message-processing.md)
-   [<span data-ttu-id="759fe-115">Esecuzione degli elementi del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="759fe-115">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
-   [<span data-ttu-id="759fe-116">Estensione degli elementi del pannello di controllo di sistema</span><span class="sxs-lookup"><span data-stu-id="759fe-116">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
-   [<span data-ttu-id="759fe-117">Assegnazione delle categorie del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="759fe-117">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
-   [<span data-ttu-id="759fe-118">Creazione di collegamenti alle attività ricercabili per un elemento del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="759fe-118">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
-   [<span data-ttu-id="759fe-119">Accesso al pannello di controllo in modalità provvisoria</span><span class="sxs-lookup"><span data-stu-id="759fe-119">Accessing the Control Panel in Safe Mode</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
-   [<span data-ttu-id="759fe-120">Nomi canonici degli elementi del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="759fe-120">Canonical Names of Control Panel Items</span></span>](controlpanel-canonical-names.md)

 

 



