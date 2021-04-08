---
title: Interfacce Factory proxy per i client
description: Questa sezione descrive le interfacce di Factory proxy per le applicazioni client di automazione interfaccia utente non gestite.
ms.assetid: 46c6720a-19c2-4ddd-893c-1a46af0642fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fc1827ab36a221dcd7f27e5b2a05de91931b0ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045210"
---
# <a name="proxy-factory-interfaces-for-clients"></a><span data-ttu-id="355a4-103">Interfacce Factory proxy per i client</span><span class="sxs-lookup"><span data-stu-id="355a4-103">Proxy Factory Interfaces for Clients</span></span>

<span data-ttu-id="355a4-104">Questa sezione descrive le interfacce di Factory proxy per le applicazioni client di automazione interfaccia utente non gestite.</span><span class="sxs-lookup"><span data-stu-id="355a4-104">This section describes the proxy factory interfaces for unmanaged UI Automation client applications.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="355a4-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="355a4-105">In this section</span></span>



| <span data-ttu-id="355a4-106">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="355a4-106">Interface</span></span>                                                                                      | <span data-ttu-id="355a4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="355a4-107">Description</span></span>                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="355a4-108">**IUIAutomationProxyFactory**</span><span class="sxs-lookup"><span data-stu-id="355a4-108">**IUIAutomationProxyFactory**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory)<br/>               | <span data-ttu-id="355a4-109">Espone le proprietà e i metodi di un oggetto che crea un provider di automazione interfaccia utente Microsoft per gli elementi dell'interfaccia utente che non dispongono del supporto nativo per l'automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="355a4-109">Exposes properties and methods of an object that creates a Microsoft UI Automation provider for UI elements that do not have native support for UI Automation.</span></span> <span data-ttu-id="355a4-110">Questa interfaccia viene implementata dai proxy.</span><span class="sxs-lookup"><span data-stu-id="355a4-110">This interface is implemented by proxies.</span></span><br/>                                                                          |
| [<span data-ttu-id="355a4-111">**IUIAutomationProxyFactoryEntry**</span><span class="sxs-lookup"><span data-stu-id="355a4-111">**IUIAutomationProxyFactoryEntry**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry)<br/>     | <span data-ttu-id="355a4-112">Rappresenta una factory proxy nella tabella gestita dall'automazione interfaccia utente ed espone proprietà e metodi che possono essere utilizzati dalle applicazioni client per interagire con gli oggetti [**IUIAutomationProxyFactory**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory) .</span><span class="sxs-lookup"><span data-stu-id="355a4-112">Represents a proxy factory in the table maintained by UI Automation, and exposes properties and methods that can be used by client applications to interact with [**IUIAutomationProxyFactory**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory) objects.</span></span><br/>                                   |
| [<span data-ttu-id="355a4-113">**IUIAutomationProxyFactoryMapping**</span><span class="sxs-lookup"><span data-stu-id="355a4-113">**IUIAutomationProxyFactoryMapping**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactorymapping)<br/> | <span data-ttu-id="355a4-114">Espone proprietà e metodi per una tabella di Factory proxy.</span><span class="sxs-lookup"><span data-stu-id="355a4-114">Exposes properties and methods for a table of proxy factories.</span></span> <span data-ttu-id="355a4-115">Ogni voce di tabella è rappresentata da un'interfaccia [**IUIAutomationProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) .</span><span class="sxs-lookup"><span data-stu-id="355a4-115">Each table entry is represented by an [**IUIAutomationProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) interface.</span></span> <span data-ttu-id="355a4-116">Le voci si trovano nell'ordine in cui il sistema tenterà di utilizzare i proxy.</span><span class="sxs-lookup"><span data-stu-id="355a4-116">The entries are in the order in which the system will attempt to use the proxies.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="355a4-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="355a4-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="355a4-118">Client di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="355a4-118">UI Automation Clients</span></span>](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

 





