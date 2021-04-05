---
title: Architettura e interoperabilità
description: Questo argomento descrive brevemente l'architettura di Microsoft Active Accessibility e l'automazione dell'interfaccia utente Microsoft e i componenti che consentono l'interoperabilità tra applicazioni basate su due tecnologie diverse.
ms.assetid: 7309819c-7c72-4bb3-ab9c-608a27c56d42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f318e46a6a0ad833b7aedb114974240fc4e52c08
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "104117295"
---
# <a name="architecture-and-interoperability"></a><span data-ttu-id="e2faf-103">Architettura e interoperabilità</span><span class="sxs-lookup"><span data-stu-id="e2faf-103">Architecture and Interoperability</span></span>

<span data-ttu-id="e2faf-104">Questo argomento descrive brevemente l'architettura di Microsoft Active Accessibility e l'automazione dell'interfaccia utente Microsoft e i componenti che consentono l'interoperabilità tra applicazioni basate su due tecnologie diverse.</span><span class="sxs-lookup"><span data-stu-id="e2faf-104">This topic briefly describes the architecture of Microsoft Active Accessibility and Microsoft UI Automation, and the components that allow interoperability between applications based on the two different technologies.</span></span>

<span data-ttu-id="e2faf-105">Per ulteriori informazioni sull'interoperabilità di Microsoft Active Accessibility e automazione interfaccia utente, vedere [infrastruttura comune](common-infrastructure.md).</span><span class="sxs-lookup"><span data-stu-id="e2faf-105">For more information about Microsoft Active Accessibility and UI Automation interoperability, see [Common Infrastructure](common-infrastructure.md).</span></span>

<span data-ttu-id="e2faf-106">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="e2faf-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="e2faf-107">Architettura di Microsoft Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="e2faf-107">Microsoft Active Accessibility Architecture</span></span>](#microsoft-active-accessibility-architecture)
-   [<span data-ttu-id="e2faf-108">Architettura di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="e2faf-108">UI Automation Architecture</span></span>](#ui-automation-architecture)
-   [<span data-ttu-id="e2faf-109">Interoperabilità di Microsoft Active Accessibility e automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="e2faf-109">Microsoft Active Accessibility and UI Automation Interoperability</span></span>](#microsoft-active-accessibility-and-ui-automation-interoperability)
-   [<span data-ttu-id="e2faf-110">Interfaccia IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="e2faf-110">The IAccessibleEx Interface</span></span>](#the-iaccessibleex-interface)
-   [<span data-ttu-id="e2faf-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e2faf-111">Related topics</span></span>](#related-topics)

## <a name="microsoft-active-accessibility-architecture"></a><span data-ttu-id="e2faf-112">Architettura di Microsoft Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="e2faf-112">Microsoft Active Accessibility Architecture</span></span>

<span data-ttu-id="e2faf-113">Microsoft Active Accessibility espone informazioni di base sui controlli, ad esempio il nome del controllo, la posizione sullo schermo e il tipo di controllo, nonché informazioni sullo stato, ad esempio la visibilità e lo stato di abilitazione/disabilitazione.</span><span class="sxs-lookup"><span data-stu-id="e2faf-113">Microsoft Active Accessibility exposes basic information about controls such as control name, location on screen, and type of control, as well as state information such as visibility and enabled/disabled status.</span></span> <span data-ttu-id="e2faf-114">L'interfaccia utente è rappresentata come una gerarchia di oggetti accessibili; le modifiche e le azioni sono rappresentate come WinEvents.</span><span class="sxs-lookup"><span data-stu-id="e2faf-114">The UI is represented as a hierarchy of accessible objects; changes and actions are represented as WinEvents.</span></span>

<span data-ttu-id="e2faf-115">Microsoft Active Accessibility è costituito dai componenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="e2faf-115">Microsoft Active Accessibility consists of the following components:</span></span>

-   <span data-ttu-id="e2faf-116">Oggetto accessibile: elemento dell'interfaccia utente logico, ad esempio un pulsante, rappresentato da un'interfaccia di Component Object Model [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) (com) e da un identificatore figlio Integer (childID).</span><span class="sxs-lookup"><span data-stu-id="e2faf-116">Accessible object—A logical UI element (such as a button) that is represented by an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Component Object Model (COM) interface and an integer child identifier (ChildID).</span></span>
-   <span data-ttu-id="e2faf-117">WinEvents: un sistema di eventi che consente ai server di notificare ai client quando un oggetto accessibile viene modificato.</span><span class="sxs-lookup"><span data-stu-id="e2faf-117">WinEvents—An event system that enables servers to notify clients when an accessible object changes.</span></span> <span data-ttu-id="e2faf-118">Per ulteriori informazioni, vedere [winEvents](winevents-infrastructure.md).</span><span class="sxs-lookup"><span data-stu-id="e2faf-118">For more information, see [WinEvents](winevents-infrastructure.md).</span></span>
-   <span data-ttu-id="e2faf-119">OLEACC.dll: la libreria a collegamento dinamico in fase di esecuzione che fornisce l'API Microsoft Active Accessibility e il Framework di sistema di accessibilità.</span><span class="sxs-lookup"><span data-stu-id="e2faf-119">OLEACC.dll—The run-time, dynamic-link library that provides the Microsoft Active Accessibility API and the accessibility system framework.</span></span> <span data-ttu-id="e2faf-120">OLEACC implementa oggetti proxy che forniscono informazioni di accessibilità predefinite per gli elementi dell'interfaccia utente standard, inclusi i controlli utente, i menu utente e i controlli comuni.</span><span class="sxs-lookup"><span data-stu-id="e2faf-120">OLEACC implements proxy objects that provide default accessibility information for standard UI elements, including USER controls, USER menus, and common controls.</span></span>

<span data-ttu-id="e2faf-121">Per Microsoft Active Accessibility, il componente di sistema di OLEACC (Accessibility Framework) consente la comunicazione tra le tecnologie per l'accesso facilitato (strumenti di accessibilità) e le applicazioni, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="e2faf-121">For Microsoft Active Accessibility, the system component of the accessibility framework (OLEACC) helps the communication between assistive technologies (accessibility tools) and applications, as the following illustration shows.</span></span>

![illustrazione che Mostra come gli strumenti di accessibilità interagiscono con le applicazioni](images/msaaarch.gif)

<span data-ttu-id="e2faf-123">Le applicazioni (server Microsoft Active Accessibility) forniscono informazioni di accessibilità dell'interfaccia utente agli strumenti (Microsoft Active Accessibility client), che interagiscono con l'interfaccia utente per conto degli utenti.</span><span class="sxs-lookup"><span data-stu-id="e2faf-123">The applications (Microsoft Active Accessibility servers) provide UI accessibility information to tools (Microsoft Active Accessibility clients), which interact with the UI on behalf of users.</span></span> <span data-ttu-id="e2faf-124">Il limite del codice è un limite programmatico e un processo.</span><span class="sxs-lookup"><span data-stu-id="e2faf-124">The code boundary is both a programmatic and a process boundary.</span></span>

## <a name="ui-automation-architecture"></a><span data-ttu-id="e2faf-125">Architettura di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="e2faf-125">UI Automation Architecture</span></span>

<span data-ttu-id="e2faf-126">Con l'automazione dell'interfaccia utente, il componente principale di automazione interfaccia utente (UIAutomationCore.dll) viene caricato sia nei processi degli strumenti di accessibilità che nelle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="e2faf-126">With UI Automation, the UI Automation core component (UIAutomationCore.dll) is loaded into both the accessibility tools' and applications' processes.</span></span> <span data-ttu-id="e2faf-127">Il componente di base gestisce la comunicazione tra processi, fornisce servizi di livello superiore, ad esempio la ricerca di elementi in base ai valori delle proprietà, e consente il recupero o la memorizzazione nella cache delle proprietà, che offre prestazioni migliori rispetto all'implementazione di Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="e2faf-127">The core component manages cross-process communication, provides higher level services such as searching for elements by property values, and enables bulk fetching or caching of properties, which provides better performance than the Microsoft Active Accessibility implementation.</span></span>

<span data-ttu-id="e2faf-128">Automazione interfaccia utente include oggetti proxy che forniscono informazioni sull'interfaccia utente sugli elementi standard dell'interfaccia utente, ad esempio controlli utente, menu utente e controlli comuni.</span><span class="sxs-lookup"><span data-stu-id="e2faf-128">UI Automation includes proxy objects that provide UI information about standard UI elements such as USER controls, USER menus, and common controls.</span></span> <span data-ttu-id="e2faf-129">Include anche proxy che consentono ai client di automazione interfaccia utente di ottenere informazioni sull'interfaccia utente da Microsoft Active Accessibility server.</span><span class="sxs-lookup"><span data-stu-id="e2faf-129">It also includes proxies that enable UI Automation clients to get UI information from Microsoft Active Accessibility servers.</span></span>

<span data-ttu-id="e2faf-130">Nella figura seguente sono illustrate le relazioni tra i diversi Compontents di automazione interfaccia utente utilizzati negli strumenti di accessibilità (client) e nelle applicazioni (provider).</span><span class="sxs-lookup"><span data-stu-id="e2faf-130">The following illustration shows the relationships among the various UI Automation compontents used in accessibility tools (clients) and in applications (providers).</span></span>

![illustrazione che Mostra come i componenti degli strumenti di accessibilità interagiscono con quelli delle applicazioni](images/uiaarch.gif)

## <a name="microsoft-active-accessibility-and-ui-automation-interoperability"></a><span data-ttu-id="e2faf-132">Interoperabilità di Microsoft Active Accessibility e automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="e2faf-132">Microsoft Active Accessibility and UI Automation Interoperability</span></span>

<span data-ttu-id="e2faf-133">L'automazione interfaccia utente di Microsoft Active Accessibility Bridge consente ai client Microsoft Active Accessibility di accedere ai provider di automazione interfaccia utente convertendo il modello a oggetti di automazione interfaccia utente in un modello a oggetti di Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="e2faf-133">The UI Automation to Microsoft Active Accessibility Bridge enables Microsoft Active Accessibility clients to access UI Automation providers by converting the UI Automation object model to a Microsoft Active Accessibility object model.</span></span> <span data-ttu-id="e2faf-134">La figura seguente mostra il ruolo del Bridge di automazione interfaccia utente-a-Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="e2faf-134">The following illustration shows the role of the UI Automation-to-Microsoft Active Accessibility Bridge.</span></span>

![illustrazione che illustra il funzionamento dell'automazione interfaccia utente con gli strumenti e le applicazioni di accessibilità](images/uiatomsaabridge.gif)

<span data-ttu-id="e2faf-136">Analogamente, il proxy di automazione da Active Accessibility a interfaccia utente Microsoft converte i modelli a oggetti server basati su Microsoft Active Accessibility per i client di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="e2faf-136">Similarly, the Microsoft Active Accessibility-to-UI Automation Proxy translates Microsoft Active Accessibility-based server object models for UI Automation clients.</span></span> <span data-ttu-id="e2faf-137">La figura seguente mostra il ruolo del proxy di automazione da Active Accessibility a interfaccia utente Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e2faf-137">The following illustration shows the role of the Microsoft Active Accessibility-to-UI Automation Proxy.</span></span>

![illustrazione che illustra il funzionamento del proxy di automazione interfaccia utente con strumenti e applicazioni per l'accessibilità](images/msaatouiaproxy.gif)

## <a name="the-iaccessibleex-interface"></a><span data-ttu-id="e2faf-139">Interfaccia IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="e2faf-139">The IAccessibleEx Interface</span></span>

<span data-ttu-id="e2faf-140">L'interfaccia [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) consente alle applicazioni esistenti o alle librerie dell'interfaccia utente di estendere il modello a oggetti di Microsoft Active Accessibility per supportare l'automazione dell'interfaccia utente senza riscrivere l'implementazione da zero.</span><span class="sxs-lookup"><span data-stu-id="e2faf-140">The [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface enables existing applications or UI libraries to extend their Microsoft Active Accessibility object model to support UI Automation without rewriting the implementation from scratch.</span></span> <span data-ttu-id="e2faf-141">Con **IAccessibleEx** è possibile implementare solo le proprietà aggiuntive di automazione interfaccia utente e i pattern di controllo necessari per descrivere completamente l'interfaccia utente e le relative funzionalità.</span><span class="sxs-lookup"><span data-stu-id="e2faf-141">With **IAccessibleEx**, you can implement only the additional UI Automation properties and control patterns needed to fully describe the UI and its functionality.</span></span>

<span data-ttu-id="e2faf-142">Poiché il proxy di automazione da Active Accessibility a interfaccia utente di Microsoft converte i modelli a oggetti di Microsoft Active Accessibility server abilitati per [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)come modelli a oggetti di automazione interfaccia utente, i client di automazione interfaccia utente non devono eseguire operazioni aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="e2faf-142">Because the Microsoft Active Accessibility-to-UI Automation Proxy translates the object models of [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)-enabled Microsoft Active Accessibility servers as UI Automation object models, UI Automation clients do not need to do any extra work.</span></span> <span data-ttu-id="e2faf-143">L'interfaccia **IAccessibleEx** può inoltre consentire ai client Microsoft Active Accessibility in-process di interagire direttamente con i provider di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="e2faf-143">The **IAccessibleEx** interface can also enable in-process Microsoft Active Accessibility clients to interact directly with UI Automation providers.</span></span>

<span data-ttu-id="e2faf-144">Per ulteriori informazioni, vedere [l'interfaccia IAccessibleEx](iaccessibleex.md).</span><span class="sxs-lookup"><span data-stu-id="e2faf-144">For more information, see [The IAccessibleEx Interface](iaccessibleex.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2faf-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e2faf-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2faf-146">Panoramica dell'API di automazione di Windows</span><span class="sxs-lookup"><span data-stu-id="e2faf-146">Windows Automation API Overview</span></span>](windows-automation-api-overview.md)
</dt> <dt>

[<span data-ttu-id="e2faf-147">Interfaccia IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="e2faf-147">The IAccessibleEx Interface</span></span>](iaccessibleex.md)
</dt> <dt>

[<span data-ttu-id="e2faf-148">Considerazioni sulla sicurezza per le tecnologie per l'accesso facilitato</span><span class="sxs-lookup"><span data-stu-id="e2faf-148">Security Considerations for Assistive Technologies</span></span>](uiauto-securityoverview.md)
</dt> </dl>

 

 




