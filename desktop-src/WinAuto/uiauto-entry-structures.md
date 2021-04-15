---
title: Strutture di automazione interfaccia utente
description: Questa sezione descrive le strutture usate dalle applicazioni client di automazione interfaccia utente e dal provider di automazione interfaccia utente per Microsoft Win32.
ms.assetid: 37d6a7c0-6925-443b-aa21-da2a14a9ddad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c55ddf9086f0714665c944a5a80e53e63eb3a91a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471030"
---
# <a name="ui-automation-structures"></a><span data-ttu-id="cfdc3-103">Strutture di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="cfdc3-103">UI Automation Structures</span></span>

<span data-ttu-id="cfdc3-104">Questa sezione descrive le strutture usate dalle applicazioni client di automazione interfaccia utente e dal provider di automazione interfaccia utente per Microsoft Win32.</span><span class="sxs-lookup"><span data-stu-id="cfdc3-104">This section describes the structures used by UI Automation client applications and UI Automation provider for Microsoft Win32.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="cfdc3-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="cfdc3-105">In this section</span></span>



| <span data-ttu-id="cfdc3-106">Struttura</span><span class="sxs-lookup"><span data-stu-id="cfdc3-106">Structure</span></span>                                                                            | <span data-ttu-id="cfdc3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cfdc3-107">Description</span></span>                                                                                   |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cfdc3-108">**ExtendedProperty**</span><span class="sxs-lookup"><span data-stu-id="cfdc3-108">**ExtendedProperty**</span></span>](/windows/desktop/api/UIAutomationClient/ns-uiautomationclient-extendedproperty)<br/>                       | <span data-ttu-id="cfdc3-109">Contiene informazioni su una proprietà estesa.</span><span class="sxs-lookup"><span data-stu-id="cfdc3-109">Contains information about an extended property.</span></span> <br/>                                  |
| [<span data-ttu-id="cfdc3-110">**UIAutomationEventInfo**</span><span class="sxs-lookup"><span data-stu-id="cfdc3-110">**UIAutomationEventInfo**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo)<br/>       | <span data-ttu-id="cfdc3-111">Contiene informazioni su un evento personalizzato.</span><span class="sxs-lookup"><span data-stu-id="cfdc3-111">Contains information about a custom event.</span></span><br/>                                         |
| [<span data-ttu-id="cfdc3-112">**UIAutomationMethodInfo**</span><span class="sxs-lookup"><span data-stu-id="cfdc3-112">**UIAutomationMethodInfo**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationmethodinfo)<br/>     | <span data-ttu-id="cfdc3-113">Contiene informazioni su un metodo supportato da un pattern di controllo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="cfdc3-113">Contains information about a method that is supported by a custom control pattern.</span></span><br/> |
| [<span data-ttu-id="cfdc3-114">**UIAutomationParameter**</span><span class="sxs-lookup"><span data-stu-id="cfdc3-114">**UIAutomationParameter**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationparameter)<br/>       | <span data-ttu-id="cfdc3-115">Contiene informazioni su un parametro di un pattern di controllo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="cfdc3-115">Contains information about a parameter of a custom control pattern.</span></span><br/>                |
| [<span data-ttu-id="cfdc3-116">**UIAutomationPatternInfo**</span><span class="sxs-lookup"><span data-stu-id="cfdc3-116">**UIAutomationPatternInfo**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo)<br/>   | <span data-ttu-id="cfdc3-117">Contiene informazioni su un pattern di controllo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="cfdc3-117">Contains information about a custom control pattern.</span></span><br/>                               |
| [<span data-ttu-id="cfdc3-118">**UIAutomationPropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="cfdc3-118">**UIAutomationPropertyInfo**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo)<br/> | <span data-ttu-id="cfdc3-119">Contiene informazioni su una proprietà personalizzata.</span><span class="sxs-lookup"><span data-stu-id="cfdc3-119">Contains information about a custom property.</span></span><br/>                                      |
| [<span data-ttu-id="cfdc3-120">**UiaChangeInfo**</span><span class="sxs-lookup"><span data-stu-id="cfdc3-120">**UiaChangeInfo**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiachangeinfo)<br/>                                    | <span data-ttu-id="cfdc3-121">Contiene i dati relativi a una modifica di automazione interfaccia utente eseguita.</span><span class="sxs-lookup"><span data-stu-id="cfdc3-121">Contains data about a UI Automation change that occurred.</span></span><br/>                          |
| [<span data-ttu-id="cfdc3-122">**UiaPoint**</span><span class="sxs-lookup"><span data-stu-id="cfdc3-122">**UiaPoint**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiapoint)<br/>                                 | <span data-ttu-id="cfdc3-123">Contiene le coordinate di un punto.</span><span class="sxs-lookup"><span data-stu-id="cfdc3-123">Contains the coordinates of a point.</span></span> <br/>                                              |
| [<span data-ttu-id="cfdc3-124">**UiaRect**</span><span class="sxs-lookup"><span data-stu-id="cfdc3-124">**UiaRect**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect)<br/>                                   | <span data-ttu-id="cfdc3-125">Contiene la posizione e le dimensioni di un rettangolo, in coordinate dello schermo.</span><span class="sxs-lookup"><span data-stu-id="cfdc3-125">Contains the position and size of a rectangle, in screen coordinates.</span></span><br/>              |



 

 

 





