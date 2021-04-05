---
title: Gli elementi DragPattern/DragDropPattern richiedono un DropEffect valido
description: Gli elementi DragPattern/DragDropPattern richiedono un DropEffect valido
ms.assetid: 508DD4F3-4878-4A9E-859D-06BBDA505708
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33acda19732e2ebd96182023fce9641012b50d6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707165"
---
# <a name="dragpatterndragdroppattern-elements-requires-valid-dropeffect"></a><span data-ttu-id="7cf24-103">Gli elementi DragPattern/DragDropPattern richiedono un DropEffect valido</span><span class="sxs-lookup"><span data-stu-id="7cf24-103">DragPattern/DragDropPattern elements requires valid DropEffect</span></span>

## <a name="text"></a><span data-ttu-id="7cf24-104">Testo</span><span class="sxs-lookup"><span data-stu-id="7cf24-104">Text</span></span>

<span data-ttu-id="7cf24-105">Gli elementi che supportano il trascinamento della selezione devono avere un set ' DropEffect ' valido</span><span class="sxs-lookup"><span data-stu-id="7cf24-105">Elements that support Drag/Drop should have a valid 'DropEffect' set</span></span>

## <a name="type"></a><span data-ttu-id="7cf24-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="7cf24-106">Type</span></span>

<span data-ttu-id="7cf24-107">Errore</span><span class="sxs-lookup"><span data-stu-id="7cf24-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="7cf24-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7cf24-108">Description</span></span>

<span data-ttu-id="7cf24-109">L'elemento supporta [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) o [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern), ma non ha un set di proprietà [**DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) valido.</span><span class="sxs-lookup"><span data-stu-id="7cf24-109">The element supports either [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) or [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern), but does not have a valid [**DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) property set.</span></span>

<span data-ttu-id="7cf24-110">Questo problema causa problemi per gli utenti che si affidano a un lettore di schermate.</span><span class="sxs-lookup"><span data-stu-id="7cf24-110">This issue causes problems for people who rely on a screen-reader.</span></span> <span data-ttu-id="7cf24-111">L'utente non sarà in grado di stabilire l'effetto di questo oggetto durante il trascinamento.</span><span class="sxs-lookup"><span data-stu-id="7cf24-111">The user will not be able to tell what effect this object has when dragging.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="7cf24-112">Possibili cause</span><span class="sxs-lookup"><span data-stu-id="7cf24-112">Possible causes</span></span>

-   <span data-ttu-id="7cf24-113">L'elemento, o il relativo padre, non ha creato [**DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) o [**DropEffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffects) un'etichetta o un nome assegnato erroneamente.</span><span class="sxs-lookup"><span data-stu-id="7cf24-113">The element, or its parent, has not created the [**DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) or [**DropEffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffects) an incorrectly assigned name or label.</span></span>
-   <span data-ttu-id="7cf24-114">Uno sviluppatore non è A conoscenza del DropEffect di lettura dello schermo.</span><span class="sxs-lookup"><span data-stu-id="7cf24-114">A developer is not aware that screen readers read DropEffect(s).</span></span>

 

 




