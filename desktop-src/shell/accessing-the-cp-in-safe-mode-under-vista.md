---
description: Per impostazione predefinita, a partire da gli elementi del pannello di controllo di Windows Vista non vengono visualizzati quando Windows viene eseguito in modalità provvisoria.
title: Accesso al pannello di controllo in modalità provvisoria
ms.topic: article
ms.date: 05/31/2018
ms.assetid: f37bcb0f-9417-4cc4-a57d-4f67a9ccda19
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 0f7a401bbc22a7f8de3618f844bfe463fa3baa50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977415"
---
# <a name="accessing-the-control-panel-in-safe-mode"></a><span data-ttu-id="b7048-103">Accesso al pannello di controllo in modalità provvisoria</span><span class="sxs-lookup"><span data-stu-id="b7048-103">Accessing the Control Panel in Safe Mode</span></span>

<span data-ttu-id="b7048-104">Per impostazione predefinita, a partire da gli elementi del pannello di controllo di Windows Vista non vengono visualizzati quando Windows viene eseguito in modalità provvisoria.</span><span class="sxs-lookup"><span data-stu-id="b7048-104">By default, as of Windows Vista Control Panel items are not shown when Windows is run in safe mode.</span></span> <span data-ttu-id="b7048-105">Per consentire la visualizzazione di un nuovo elemento del pannello di controllo in modalità provvisoria, è possibile impostare i valori del registro di sistema appropriati per il tipo di elemento.</span><span class="sxs-lookup"><span data-stu-id="b7048-105">To allow a new Control Panel item to be viewed in safe mode, registry values appropriate to the item type can be set.</span></span> <span data-ttu-id="b7048-106">I valori vengono interpretati nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="b7048-106">The values are interpreted as follows:</span></span>



| <span data-ttu-id="b7048-107">Valore</span><span class="sxs-lookup"><span data-stu-id="b7048-107">Value</span></span> | <span data-ttu-id="b7048-108">Significato</span><span class="sxs-lookup"><span data-stu-id="b7048-108">Meaning</span></span>                                                            |
|-------|--------------------------------------------------------------------|
| <span data-ttu-id="b7048-109">1</span><span class="sxs-lookup"><span data-stu-id="b7048-109">1</span></span>     | <span data-ttu-id="b7048-110">L'elemento deve essere visualizzato solo in modalità provvisoria minima.</span><span class="sxs-lookup"><span data-stu-id="b7048-110">The item should appear in minimal safe mode only.</span></span>                  |
| <span data-ttu-id="b7048-111">2</span><span class="sxs-lookup"><span data-stu-id="b7048-111">2</span></span>     | <span data-ttu-id="b7048-112">L'elemento deve essere visualizzato in modalità provvisoria solo se la rete è abilitata.</span><span class="sxs-lookup"><span data-stu-id="b7048-112">The item should appear in safe mode only if networking is enabled.</span></span> |
| <span data-ttu-id="b7048-113">3</span><span class="sxs-lookup"><span data-stu-id="b7048-113">3</span></span>     | <span data-ttu-id="b7048-114">L'elemento deve essere sempre visualizzato in qualsiasi forma di modalità provvisoria.</span><span class="sxs-lookup"><span data-stu-id="b7048-114">The item should always appear in any form of safe mode.</span></span>            |



 

<span data-ttu-id="b7048-115">Questo esempio mostra le voci necessarie per un elemento implementato come file con estensione CPL o dll.</span><span class="sxs-lookup"><span data-stu-id="b7048-115">This example shows the entries required for an item implemented as a .cpl or .dll file.</span></span> <span data-ttu-id="b7048-116">Specifica che l'elemento deve essere visualizzato in modalità provvisoria con la rete.</span><span class="sxs-lookup"><span data-stu-id="b7048-116">It specifies that the item should appear in safe mode with networking.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.ControlPanel.EnableInSafeMode
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_DWORD] 2
```

<span data-ttu-id="b7048-117">Questo esempio mostra le voci necessarie per un elemento implementato come file con estensione exe.</span><span class="sxs-lookup"><span data-stu-id="b7048-117">This example shows the entries required for an item implemented as a .exe file.</span></span> <span data-ttu-id="b7048-118">Specifica che l'elemento deve essere visualizzato in qualsiasi forma di modalità provvisoria.</span><span class="sxs-lookup"><span data-stu-id="b7048-118">It specifies that the item should appear in any form of safe mode.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         System.ControlPanel.EnableInSafeMode = [REG_DWORD] 3
```

## <a name="related-topics"></a><span data-ttu-id="b7048-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b7048-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7048-120">Elementi del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="b7048-120">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="b7048-121">Linee guida sull'esperienza utente</span><span class="sxs-lookup"><span data-stu-id="b7048-121">User Experience Guidelines</span></span>](user-experience-guidelines.md)
</dt> <dt>

[<span data-ttu-id="b7048-122">Registrazione degli elementi del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="b7048-122">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="b7048-123">Uso di CPLApplet</span><span class="sxs-lookup"><span data-stu-id="b7048-123">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="b7048-124">Elaborazione del messaggio del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="b7048-124">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="b7048-125">Esecuzione degli elementi del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="b7048-125">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="b7048-126">Estensione degli elementi del pannello di controllo di sistema</span><span class="sxs-lookup"><span data-stu-id="b7048-126">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="b7048-127">Assegnazione delle categorie del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="b7048-127">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
</dt> <dt>

[<span data-ttu-id="b7048-128">Creazione di collegamenti alle attività ricercabili per un elemento del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="b7048-128">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
</dt> </dl>

 

 



