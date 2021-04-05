---
title: DuplicateSiblingNames
description: DuplicateSiblingNames
ms.assetid: 4E9FFD16-EAC0-4778-8DEB-D179E2197411
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aed5a7caeadc34519988fe8a4a1f12ec4e05ce13
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714512"
---
# <a name="duplicatesiblingnames"></a><span data-ttu-id="b76c9-103">DuplicateSiblingNames</span><span class="sxs-lookup"><span data-stu-id="b76c9-103">DuplicateSiblingNames</span></span>

## <a name="text"></a><span data-ttu-id="b76c9-104">Testo</span><span class="sxs-lookup"><span data-stu-id="b76c9-104">Text</span></span>

<span data-ttu-id="b76c9-105">Il nome di pari livello e il ruolo \\ "" duplicati {0} \\ provocheranno ambiguità tra gli elementi.</span><span class="sxs-lookup"><span data-stu-id="b76c9-105">Duplicate sibling Name+Role \\"{0}\\" will cause ambiguity between elements.</span></span>

## <a name="type"></a><span data-ttu-id="b76c9-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="b76c9-106">Type</span></span>

<span data-ttu-id="b76c9-107">Errore</span><span class="sxs-lookup"><span data-stu-id="b76c9-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="b76c9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b76c9-108">Description</span></span>

<span data-ttu-id="b76c9-109">Un elemento ha lo stesso nome e lo stesso ruolo/ControlType di un altro elemento.</span><span class="sxs-lookup"><span data-stu-id="b76c9-109">An element has the same Name and Role/ControlType as another element.</span></span>

<span data-ttu-id="b76c9-110">Questo problema può causare confusione perché le utilità per la lettura dello schermo leggono lo stesso testo per tutti gli elementi con lo stesso nome e lo stesso ruolo/ControlType.</span><span class="sxs-lookup"><span data-stu-id="b76c9-110">This issue can cause confusion because screen readers will read the same text for all the elements with the same Name and Role/ControlType.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="b76c9-111">Possibili cause</span><span class="sxs-lookup"><span data-stu-id="b76c9-111">Possible causes</span></span>

-   <span data-ttu-id="b76c9-112">Il nome dell'elemento contiene il testo Role/ControlType.</span><span class="sxs-lookup"><span data-stu-id="b76c9-112">Element’s name contain Role/ControlType text.</span></span>
-   <span data-ttu-id="b76c9-113">Il nome dell'elemento o il nome dell'elemento padre non è impostato o è impostato in modo errato.</span><span class="sxs-lookup"><span data-stu-id="b76c9-113">Element’s name or the name of its parent is not set or is set incorrectly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b76c9-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b76c9-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b76c9-115">**IAccessible:: Get \_ accName**</span><span class="sxs-lookup"><span data-stu-id="b76c9-115">**IAccessible::get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[<span data-ttu-id="b76c9-116">Proprietà Name</span><span class="sxs-lookup"><span data-stu-id="b76c9-116">Name Property</span></span>](name-property.md)
</dt> <dt>

[<span data-ttu-id="b76c9-117">**\_NAMEPROPERTYID UIA**</span><span class="sxs-lookup"><span data-stu-id="b76c9-117">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)
</dt> <dt>

[<span data-ttu-id="b76c9-118">**IUIAutomationElement. currentname**</span><span class="sxs-lookup"><span data-stu-id="b76c9-118">**IUIAutomationElement.CurrentName**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




