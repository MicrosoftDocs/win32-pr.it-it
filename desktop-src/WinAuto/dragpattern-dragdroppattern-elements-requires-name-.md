---
title: Per gli elementi DragPattern/DragDropPattern è necessario il nome
description: Per gli elementi DragPattern/DragDropPattern è necessario il nome
ms.assetid: DEF58FB2-5830-4162-87D0-40DEC1237529
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ecc60eeca59f4754f9c160696cdfa2556c36a5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297613"
---
# <a name="dragpatterndragdroppattern-elements-requires-name"></a><span data-ttu-id="2256f-103">Per gli elementi DragPattern/DragDropPattern è necessario il nome</span><span class="sxs-lookup"><span data-stu-id="2256f-103">DragPattern/DragDropPattern elements requires Name</span></span>

## <a name="text"></a><span data-ttu-id="2256f-104">Testo</span><span class="sxs-lookup"><span data-stu-id="2256f-104">Text</span></span>

<span data-ttu-id="2256f-105">Gli elementi che supportano il trascinamento della selezione devono avere un set ' name ' valido</span><span class="sxs-lookup"><span data-stu-id="2256f-105">Elements that support Drag/Drop should have a valid 'Name' set</span></span>

## <a name="type"></a><span data-ttu-id="2256f-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="2256f-106">Type</span></span>

<span data-ttu-id="2256f-107">Errore</span><span class="sxs-lookup"><span data-stu-id="2256f-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="2256f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2256f-108">Description</span></span>

<span data-ttu-id="2256f-109">L'elemento supporta [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) o [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern), ma non è impostato un nome valido.</span><span class="sxs-lookup"><span data-stu-id="2256f-109">The element supports either [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) or [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern), but does not have a valid Name set.</span></span>

<span data-ttu-id="2256f-110">Questo problema causa problemi per gli utenti che si affidano a un lettore di schermate.</span><span class="sxs-lookup"><span data-stu-id="2256f-110">This issue causes problems for people who rely on a screen-reader.</span></span> <span data-ttu-id="2256f-111">L'utente non sarà in grado di stabilire quale sia l'oggetto perché la lettura dello schermo non consente di leggere un nome valido per distinguere l'elemento durante il trascinamento.</span><span class="sxs-lookup"><span data-stu-id="2256f-111">The user will not be able to tell what this object is since the screen read will not read out a valid name to distinguish what this element is when dragging.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="2256f-112">Possibili cause</span><span class="sxs-lookup"><span data-stu-id="2256f-112">Possible causes</span></span>

-   <span data-ttu-id="2256f-113">All'elemento o al relativo padre è assegnato un nome o un'etichetta non correttamente assegnati.</span><span class="sxs-lookup"><span data-stu-id="2256f-113">The element, or its parent, has an incorrectly assigned name or label.</span></span>
-   <span data-ttu-id="2256f-114">Uno sviluppatore non è A conoscenza dello schermo che legge i nomi e i tipi di controllo.</span><span class="sxs-lookup"><span data-stu-id="2256f-114">A developer is not aware that screen readers read names and control types.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2256f-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2256f-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2256f-116">**IAccessible:: Get \_ accName**</span><span class="sxs-lookup"><span data-stu-id="2256f-116">**IAccessible::get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[<span data-ttu-id="2256f-117">Proprietà Name</span><span class="sxs-lookup"><span data-stu-id="2256f-117">Name Property</span></span>](name-property.md)
</dt> <dt>

[<span data-ttu-id="2256f-118">**\_NAMEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="2256f-118">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)
</dt> <dt>

[<span data-ttu-id="2256f-119">**IUIAutomationElement:: currentname**</span><span class="sxs-lookup"><span data-stu-id="2256f-119">**IUIAutomationElement::CurrentName**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




