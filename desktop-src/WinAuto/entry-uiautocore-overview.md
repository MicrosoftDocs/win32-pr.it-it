---
title: Nozioni fondamentali sull'automazione interfaccia utente
description: In questa sezione vengono illustrati i concetti fondamentali su cui si basa l'automazione dell'interfaccia utente.
ms.assetid: 109f113f-9ed0-4a57-b3af-90e831e53c42
keywords:
- Automazione interfaccia utente, API Microsoft Win32
- Automazione interfaccia utente, API Win32
- Automazione interfaccia utente, provider
- Automazione interfaccia utente, applicazioni client
- client, automazione interfaccia utente Microsoft per l'API Microsoft Win32
- client, automazione interfaccia utente per l'API Microsoft Win32
- API Win32
- API Microsoft Win32
- Automazione interfaccia utente per l'API Microsoft Win32
- Automazione interfaccia utente Microsoft per l'API Microsoft Win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ba8147a8dd7f8d03340fad43465c225a174e606
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396415"
---
# <a name="ui-automation-fundamentals"></a><span data-ttu-id="48475-113">Nozioni fondamentali sull'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="48475-113">UI Automation Fundamentals</span></span>

<span data-ttu-id="48475-114">Automazione interfaccia utente Microsoft consente alle applicazioni per la tecnologia per l'accessibilità e agli strumenti di test automatici di interagire con i controlli dell'interfaccia utente di altre applicazioni.</span><span class="sxs-lookup"><span data-stu-id="48475-114">Microsoft UI Automation enables assistive technology applications and automated testing tools to interact with the UI controls of other applications.</span></span> <span data-ttu-id="48475-115">In questa sezione vengono illustrati i concetti fondamentali su cui si basa l'automazione dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="48475-115">This section explains the fundamental concepts that UI Automation is based on.</span></span>

<span data-ttu-id="48475-116">L'API di automazione interfaccia utente è in due parti.</span><span class="sxs-lookup"><span data-stu-id="48475-116">The UI Automation API is in two parts.</span></span> <span data-ttu-id="48475-117">Una parte viene usata dalle applicazioni del *provider di automazione interfaccia utente* e l'altra viene usata dalle applicazioni *client di automazione interfaccia utente* .</span><span class="sxs-lookup"><span data-stu-id="48475-117">One part is used by *UI Automation provider* applications, and the other is used by *UI Automation client* applications.</span></span> <span data-ttu-id="48475-118">L'API del provider consente agli sviluppatori di controlli personalizzati di Microsoft Win32 e ad altri Framework di controllo di esporre tali controlli all'automazione interfaccia utente e di renderli visibili alle applicazioni client.</span><span class="sxs-lookup"><span data-stu-id="48475-118">The provider API enables developers of Microsoft Win32 custom control and other control frameworks to expose those controls to UI Automation and make them visible to client applications.</span></span> <span data-ttu-id="48475-119">L'API client consente alle applicazioni di interagire con i controlli in altre applicazioni e di recuperare le relative informazioni.</span><span class="sxs-lookup"><span data-stu-id="48475-119">The client API enables applications to interact with controls in other applications and retrieve information about them.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="48475-120">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="48475-120">In this section</span></span>

-   [<span data-ttu-id="48475-121">Cenni preliminari su automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="48475-121">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
-   [<span data-ttu-id="48475-122">Automazione interfaccia utente e Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="48475-122">UI Automation and Active Accessibility</span></span>](uiauto-msaa.md)
-   [<span data-ttu-id="48475-123">Panoramica dell'albero di automazione dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="48475-123">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
-   [<span data-ttu-id="48475-124">Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="48475-124">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
-   [<span data-ttu-id="48475-125">Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="48475-125">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
-   [<span data-ttu-id="48475-126">Cenni preliminari sulle proprietà di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="48475-126">UI Automation Properties Overview</span></span>](uiauto-propertiesoverview.md)
-   [<span data-ttu-id="48475-127">Cenni preliminari sugli eventi di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="48475-127">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
-   [<span data-ttu-id="48475-128">Proprietà, eventi e pattern di controllo personalizzati</span><span class="sxs-lookup"><span data-stu-id="48475-128">Custom Properties, Events, and Control Patterns</span></span>](uiauto-custompropertieseventscontrolpatterns.md)
-   [<span data-ttu-id="48475-129">Supporto di automazione interfaccia utente per contenuto testuale</span><span class="sxs-lookup"><span data-stu-id="48475-129">UI Automation Support for Textual Content</span></span>](uiauto-ui-automation-textpattern-overview.md)
-   [<span data-ttu-id="48475-130">Supporto di automazione interfaccia utente per il trascinamento della selezione</span><span class="sxs-lookup"><span data-stu-id="48475-130">UI Automation Support for Drag-and-Drop</span></span>](ui-automation-support-for-drag-and-drop.md)
-   [<span data-ttu-id="48475-131">Considerazioni sulla sicurezza per le tecnologie per l'accesso facilitato</span><span class="sxs-lookup"><span data-stu-id="48475-131">Security Considerations for Assistive Technologies</span></span>](uiauto-securityoverview.md)
-   [<span data-ttu-id="48475-132">Procedure consigliate per l'utilizzo di matrici sicure</span><span class="sxs-lookup"><span data-stu-id="48475-132">Best Practices for Using Safe Arrays</span></span>](uiauto-workingwithsafearrays.md)
-   [<span data-ttu-id="48475-133">Specifiche di Automazione interfaccia utente e impegno della community</span><span class="sxs-lookup"><span data-stu-id="48475-133">UI Automation Specification and Community Promise</span></span>](uiauto-specandcommunitypromise.md)

## <a name="related-topics"></a><span data-ttu-id="48475-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="48475-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48475-135">Automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="48475-135">UI Automation</span></span>](entry-uiauto-win32.md)
</dt> </dl>

 

 




