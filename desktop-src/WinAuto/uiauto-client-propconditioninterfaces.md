---
title: Interfacce di condizione delle proprietà per i client
description: Questa sezione descrive le interfacce della condizione di proprietà per i client di automazione interfaccia utente per le applicazioni Microsoft Win32.
ms.assetid: cea34e47-03a9-4ff9-9019-427a2a3e13d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00f840706d4f9e340cae86813a4992400791dccd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046833"
---
# <a name="property-condition-interfaces-for-clients"></a><span data-ttu-id="65508-103">Interfacce di condizione delle proprietà per i client</span><span class="sxs-lookup"><span data-stu-id="65508-103">Property Condition Interfaces for Clients</span></span>

<span data-ttu-id="65508-104">Questa sezione descrive le interfacce della condizione di proprietà per i client di automazione interfaccia utente per le applicazioni Microsoft Win32.</span><span class="sxs-lookup"><span data-stu-id="65508-104">This section describes property condition interfaces for UI Automation clients for Microsoft Win32 applications.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="65508-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="65508-105">In this section</span></span>



| <span data-ttu-id="65508-106">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="65508-106">Interface</span></span>                                                                                  | <span data-ttu-id="65508-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="65508-107">Description</span></span>                                                                                                                                                        |
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="65508-108">**IUIAutomationAndCondition**</span><span class="sxs-lookup"><span data-stu-id="65508-108">**IUIAutomationAndCondition**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationandcondition)<br/>           | <span data-ttu-id="65508-109">Espone proprietà e metodi che possono essere usati dalle applicazioni client di automazione interfaccia utente Microsoft per recuperare informazioni su una condizione di proprietà basata su e.</span><span class="sxs-lookup"><span data-stu-id="65508-109">Exposes properties and methods that Microsoft UI Automation client applications can use to retrieve information about an AND-based property condition.</span></span> <br/> |
| [<span data-ttu-id="65508-110">**IUIAutomationBoolCondition**</span><span class="sxs-lookup"><span data-stu-id="65508-110">**IUIAutomationBoolCondition**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationboolcondition)<br/>         | <span data-ttu-id="65508-111">Rappresenta una condizione che può essere **true** (Seleziona tutti gli elementi) o **false** (non seleziona elementi).</span><span class="sxs-lookup"><span data-stu-id="65508-111">Represents a condition that can be either **TRUE** (selects all elements) or **FALSE** (selects no elements).</span></span><br/>                                           |
| [<span data-ttu-id="65508-112">**IUIAutomationCondition**</span><span class="sxs-lookup"><span data-stu-id="65508-112">**IUIAutomationCondition**</span></span>](/windows/win32/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition)<br/>                 | <span data-ttu-id="65508-113">Si tratta dell'interfaccia principale per le condizioni utilizzate nel filtro durante la ricerca di elementi nell'albero di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="65508-113">This is the primary interface for conditions used in filtering when searching for elements in the UI Automation tree.</span></span><br/>                                   |
| [<span data-ttu-id="65508-114">**IUIAutomationNotCondition**</span><span class="sxs-lookup"><span data-stu-id="65508-114">**IUIAutomationNotCondition**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationnotcondition)<br/>           | <span data-ttu-id="65508-115">Rappresenta una condizione negativa di un'altra condizione.</span><span class="sxs-lookup"><span data-stu-id="65508-115">Represents a condition that is the negative of another condition.</span></span><br/>                                                                                       |
| [<span data-ttu-id="65508-116">**IUIAutomationOrCondition**</span><span class="sxs-lookup"><span data-stu-id="65508-116">**IUIAutomationOrCondition**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationorcondition)<br/>             | <span data-ttu-id="65508-117">Rappresenta una condizione costituita da più condizioni, almeno una delle quali deve essere true.</span><span class="sxs-lookup"><span data-stu-id="65508-117">Represents a condition made up of multiple conditions, at least one of which must be true.</span></span><br/>                                                              |
| [<span data-ttu-id="65508-118">**IUIAutomationPropertyCondition**</span><span class="sxs-lookup"><span data-stu-id="65508-118">**IUIAutomationPropertyCondition**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertycondition)<br/> | <span data-ttu-id="65508-119">Rappresenta una condizione basata su un valore della proprietà usato per trovare gli elementi di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="65508-119">Represents a condition based on a property value that is used to find UI Automation elements.</span></span><br/>                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="65508-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="65508-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65508-121">Client di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="65508-121">UI Automation Clients</span></span>](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

