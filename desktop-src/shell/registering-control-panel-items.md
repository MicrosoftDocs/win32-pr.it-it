---
description: Gli elementi del pannello di controllo devono essere registrati per poter essere visualizzati nella finestra del pannello di controllo.
title: Registrazione degli elementi del pannello di controllo
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 6f21f223-a293-47b5-95e9-06b7a4ff1652
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 05c2a652314babc212e17b48198e9441f4d3465d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131843"
---
# <a name="registering-control-panel-items"></a><span data-ttu-id="36c4e-103">Registrazione degli elementi del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="36c4e-103">Registering Control Panel Items</span></span>

<span data-ttu-id="36c4e-104">Gli elementi del pannello di controllo devono essere registrati per poter essere visualizzati nella finestra del pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="36c4e-104">Control Panel items must be registered in order to appear in the Control Panel window.</span></span> <span data-ttu-id="36c4e-105">Se l'elemento del pannello di controllo viene implementato come parte di un file con estensione exe, viene registrato come oggetto Command.</span><span class="sxs-lookup"><span data-stu-id="36c4e-105">If the Control Panel item is implemented as part of a .exe file then it is registered as a command object.</span></span> <span data-ttu-id="36c4e-106">La registrazione è diversa se l'elemento viene implementato come un file con estensione dll che esporta la funzione [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) .</span><span class="sxs-lookup"><span data-stu-id="36c4e-106">Registration differs if the item is implemented as a .dll file that exports the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function.</span></span>

<span data-ttu-id="36c4e-107">Gli argomenti seguenti illustrano i requisiti specifici:</span><span class="sxs-lookup"><span data-stu-id="36c4e-107">Specific requirements are discussed in these topics:</span></span>

-   [<span data-ttu-id="36c4e-108">Come registrare gli elementi del pannello di controllo eseguibile</span><span class="sxs-lookup"><span data-stu-id="36c4e-108">How To Register Executable Control Panel Items</span></span>](how-to-register-an-executable-control-panel-item-registration-.md)
-   [<span data-ttu-id="36c4e-109">Come registrare gli elementi del pannello di controllo DLL</span><span class="sxs-lookup"><span data-stu-id="36c4e-109">How To Register DLL Control Panel Items</span></span>](how-to-register-dll-control-panel-item-registration-.md)

## <a name="related-topics"></a><span data-ttu-id="36c4e-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="36c4e-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36c4e-111">Elementi del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="36c4e-111">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="36c4e-112">Linee guida sull'esperienza utente</span><span class="sxs-lookup"><span data-stu-id="36c4e-112">User Experience Guidelines</span></span>](user-experience-guidelines.md)
</dt> <dt>

[<span data-ttu-id="36c4e-113">Uso di CPLApplet</span><span class="sxs-lookup"><span data-stu-id="36c4e-113">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="36c4e-114">Elaborazione del messaggio del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="36c4e-114">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="36c4e-115">Esecuzione degli elementi del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="36c4e-115">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="36c4e-116">Estensione degli elementi del pannello di controllo di sistema</span><span class="sxs-lookup"><span data-stu-id="36c4e-116">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="36c4e-117">Assegnazione delle categorie del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="36c4e-117">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
</dt> <dt>

[<span data-ttu-id="36c4e-118">Creazione di collegamenti alle attività ricercabili per un elemento del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="36c4e-118">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
</dt> <dt>

[<span data-ttu-id="36c4e-119">Accesso al pannello di controllo in modalità provvisoria in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="36c4e-119">Accessing the Control Panel in Safe Mode under Windows Vista</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
