---
title: Interfacce di gestione degli eventi per i client
description: Questa sezione descrive le interfacce di gestione degli eventi per le applicazioni client di automazione interfaccia utente non gestite.
ms.assetid: ce9c4044-f46b-42b7-af44-05aee728a0e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 458be6fcf5ce47f285d46c0e61f80e0897f15613
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298759"
---
# <a name="event-handling-interfaces-for-clients"></a><span data-ttu-id="992c4-103">Interfacce di gestione degli eventi per i client</span><span class="sxs-lookup"><span data-stu-id="992c4-103">Event Handling Interfaces for Clients</span></span>

<span data-ttu-id="992c4-104">Questa sezione descrive le interfacce di gestione degli eventi per le applicazioni client di automazione interfaccia utente non gestite.</span><span class="sxs-lookup"><span data-stu-id="992c4-104">This section describes the event handling interfaces for unmanaged UI Automation client applications.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="992c4-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="992c4-105">In this section</span></span>



| <span data-ttu-id="992c4-106">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="992c4-106">Interface</span></span>                                                                                                              | <span data-ttu-id="992c4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="992c4-107">Description</span></span>                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="992c4-108">**IUIAutomationChangesEventHandler**</span><span class="sxs-lookup"><span data-stu-id="992c4-108">**IUIAutomationChangesEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationchangeseventhandler)<br/>                         | <span data-ttu-id="992c4-109">Espone un metodo per gestire gli eventi di automazione interfaccia utente Microsoft che si verificano quando una proprietà viene modificata.</span><span class="sxs-lookup"><span data-stu-id="992c4-109">Exposes a method to handle Microsoft UI Automation events that occur when a property is changed.</span></span><br/>                      |
| [<span data-ttu-id="992c4-110">**IUIAutomationEventHandler**</span><span class="sxs-lookup"><span data-stu-id="992c4-110">**IUIAutomationEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationeventhandler)<br/>                                       | <span data-ttu-id="992c4-111">Espone un metodo per gestire gli eventi di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="992c4-111">Exposes a method to handle UI Automation events.</span></span><br/>                                                                      |
| [<span data-ttu-id="992c4-112">**IUIAutomationFocusChangedEventHandler**</span><span class="sxs-lookup"><span data-stu-id="992c4-112">**IUIAutomationFocusChangedEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler)<br/>               | <span data-ttu-id="992c4-113">Espone un metodo per gestire gli eventi generati quando lo stato attivo della tastiera si sposta su un altro elemento di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="992c4-113">Exposes a method to handle events that are raised when the keyboard focus moves to another UI Automation element.</span></span><br/>     |
| [<span data-ttu-id="992c4-114">**IUIAutomationNotificationEventHandler**</span><span class="sxs-lookup"><span data-stu-id="992c4-114">**IUIAutomationNotificationEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationnotificationeventhandler)<br/>               | <span data-ttu-id="992c4-115">Espone un metodo per gestire gli eventi di notifica di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="992c4-115">Exposes a method to handle UI Automation notification events.</span></span><br/>                                                         |
| [<span data-ttu-id="992c4-116">**IUIAutomationPropertyChangedEventHandler**</span><span class="sxs-lookup"><span data-stu-id="992c4-116">**IUIAutomationPropertyChangedEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler)<br/>         | <span data-ttu-id="992c4-117">Espone un metodo per gestire gli eventi di automazione interfaccia utente che si verificano quando una proprietà viene modificata.</span><span class="sxs-lookup"><span data-stu-id="992c4-117">Exposes a method to handle UI Automation events that occur when a property is changed.</span></span><br/>                                |
| [<span data-ttu-id="992c4-118">**IUIAutomationStructureChangedEventHandler**</span><span class="sxs-lookup"><span data-stu-id="992c4-118">**IUIAutomationStructureChangedEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationstructurechangedeventhandler)<br/>       | <span data-ttu-id="992c4-119">Espone un metodo per gestire gli eventi che si verificano quando viene modificata la struttura ad albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="992c4-119">Exposes a method to handle events that occur when the UI Automation tree structure is changed.</span></span><br/>                        |
| [<span data-ttu-id="992c4-120">**IUIAutomationTextEditTextChangedEventHandler**</span><span class="sxs-lookup"><span data-stu-id="992c4-120">**IUIAutomationTextEditTextChangedEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextedittextchangedeventhandler)<br/> | <span data-ttu-id="992c4-121">Espone un metodo per gestire gli eventi che si verificano quando l'automazione interfaccia utente segnala un evento di modifica del testo dai controlli di modifica del testo.</span><span class="sxs-lookup"><span data-stu-id="992c4-121">Exposes a method to handle events that occur when UI Automation reports a text-changed event from text edit controls.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="992c4-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="992c4-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="992c4-123">Client di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="992c4-123">UI Automation Clients</span></span>](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

 





