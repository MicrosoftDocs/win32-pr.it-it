---
title: Implementazione di pattern di controllo di automazione interfaccia utente
description: In questa sezione vengono fornite informazioni dettagliate sull'implementazione delle interfacce del provider di automazione interfaccia utente Microsoft che supportano i pattern di controllo.
ms.assetid: d1baa245-62a1-40b1-a671-e227dd3df60a
keywords:
- Automazione interfaccia utente, implementazione di pattern di controllo
- Automazione interfaccia utente, pattern di controllo
- implementazione di pattern di controllo di automazione interfaccia utente
- pattern di controllo, implementazione dell'automazione interfaccia utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bfb75b6b275fee9230eb25d9a0b02e1da26ad4d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300121"
---
# <a name="implementing-ui-automation-control-patterns"></a><span data-ttu-id="4856a-107">Implementazione di pattern di controllo di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="4856a-107">Implementing UI Automation Control Patterns</span></span>

<span data-ttu-id="4856a-108">In questa sezione vengono fornite informazioni dettagliate sull'implementazione delle interfacce del provider di automazione interfaccia utente Microsoft che supportano i pattern di controllo.</span><span class="sxs-lookup"><span data-stu-id="4856a-108">This section provides detailed information about implementing the Microsoft UI Automation provider interfaces that support control patterns.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4856a-109">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="4856a-109">In this section</span></span>

-   [<span data-ttu-id="4856a-110">Pattern di controllo Annotation</span><span class="sxs-lookup"><span data-stu-id="4856a-110">Annotation Control Pattern</span></span>](uiauto-implementingannotation.md)
-   [<span data-ttu-id="4856a-111">Pattern di controllo CustomNavigation</span><span class="sxs-lookup"><span data-stu-id="4856a-111">CustomNavigation Control Pattern</span></span>](uiauto-implementingcustomnavigation.md)
-   [<span data-ttu-id="4856a-112">Pattern di controllo Dock</span><span class="sxs-lookup"><span data-stu-id="4856a-112">Dock Control Pattern</span></span>](uiauto-implementingdock.md)
-   [<span data-ttu-id="4856a-113">Trascinare il pattern di controllo</span><span class="sxs-lookup"><span data-stu-id="4856a-113">Drag Control Pattern</span></span>](/windows/desktop/WinAuto/uiauto-implementingdrag)
-   [<span data-ttu-id="4856a-114">Pattern di controllo DropTarget</span><span class="sxs-lookup"><span data-stu-id="4856a-114">DropTarget Control Pattern</span></span>](/windows/desktop/WinAuto/uiauto-implementingdroptarget)
-   [<span data-ttu-id="4856a-115">Pattern di controllo ExpandCollapse</span><span class="sxs-lookup"><span data-stu-id="4856a-115">ExpandCollapse Control Pattern</span></span>](uiauto-implementingexpandcollapse.md)
-   [<span data-ttu-id="4856a-116">Pattern di controllo Grid</span><span class="sxs-lookup"><span data-stu-id="4856a-116">Grid Control Pattern</span></span>](uiauto-implementinggrid.md)
-   [<span data-ttu-id="4856a-117">Pattern di controllo GridItem</span><span class="sxs-lookup"><span data-stu-id="4856a-117">GridItem Control Pattern</span></span>](uiauto-implementinggriditem.md)
-   [<span data-ttu-id="4856a-118">Pattern di controllo Invoke</span><span class="sxs-lookup"><span data-stu-id="4856a-118">Invoke Control Pattern</span></span>](uiauto-implementinginvoke.md)
-   [<span data-ttu-id="4856a-119">Pattern di controllo ItemContainer</span><span class="sxs-lookup"><span data-stu-id="4856a-119">ItemContainer Control Pattern</span></span>](uiauto-implementingitemcontainer.md)
-   [<span data-ttu-id="4856a-120">Pattern di controllo LegacyIAccessible</span><span class="sxs-lookup"><span data-stu-id="4856a-120">LegacyIAccessible Control Pattern</span></span>](uiauto-implementinglegacyiaccessible.md)
-   [<span data-ttu-id="4856a-121">Pattern di controllo MultipleView</span><span class="sxs-lookup"><span data-stu-id="4856a-121">MultipleView Control Pattern</span></span>](uiauto-implementingmultipleview.md)
-   [<span data-ttu-id="4856a-122">Pattern di controllo ObjectModel</span><span class="sxs-lookup"><span data-stu-id="4856a-122">ObjectModel Control Pattern</span></span>](uiauto-implementingobjectmodel.md)
-   [<span data-ttu-id="4856a-123">Pattern di controllo RangeValue</span><span class="sxs-lookup"><span data-stu-id="4856a-123">RangeValue Control Pattern</span></span>](uiauto-implementingrangevalue.md)
-   [<span data-ttu-id="4856a-124">Pattern di controllo Scroll</span><span class="sxs-lookup"><span data-stu-id="4856a-124">Scroll Control Pattern</span></span>](uiauto-implementingscroll.md)
-   [<span data-ttu-id="4856a-125">Pattern di controllo ScrollItem</span><span class="sxs-lookup"><span data-stu-id="4856a-125">ScrollItem Control Pattern</span></span>](uiauto-implementingscrollitem.md)
-   [<span data-ttu-id="4856a-126">Pattern di controllo Selection</span><span class="sxs-lookup"><span data-stu-id="4856a-126">Selection Control Pattern</span></span>](uiauto-implementingselection.md)
-   [<span data-ttu-id="4856a-127">Pattern di controllo SelectionItem</span><span class="sxs-lookup"><span data-stu-id="4856a-127">SelectionItem Control Pattern</span></span>](uiauto-implementingselectionitem.md)
-   [<span data-ttu-id="4856a-128">Pattern di controllo foglio di calcolo</span><span class="sxs-lookup"><span data-stu-id="4856a-128">Spreadsheet Control Pattern</span></span>](uiauto-implementingspreadsheet.md)
-   [<span data-ttu-id="4856a-129">Pattern di controllo SpreadsheetItem</span><span class="sxs-lookup"><span data-stu-id="4856a-129">SpreadsheetItem Control Pattern</span></span>](uiauto-implementingspreadsheetitem.md)
-   [<span data-ttu-id="4856a-130">Pattern di controllo Styles</span><span class="sxs-lookup"><span data-stu-id="4856a-130">Styles Control Pattern</span></span>](/windows/desktop/WinAuto/uiauto-implementingstyles)
-   [<span data-ttu-id="4856a-131">Pattern di controllo SynchronizedInput</span><span class="sxs-lookup"><span data-stu-id="4856a-131">SynchronizedInput Control Pattern</span></span>](uiauto-implementingsynchronizedinput.md)
-   [<span data-ttu-id="4856a-132">Pattern di controllo Table</span><span class="sxs-lookup"><span data-stu-id="4856a-132">Table Control Pattern</span></span>](uiauto-implementingtable.md)
-   [<span data-ttu-id="4856a-133">Pattern di controllo TableItem</span><span class="sxs-lookup"><span data-stu-id="4856a-133">TableItem Control Pattern</span></span>](uiauto-implementingtableitem.md)
-   [<span data-ttu-id="4856a-134">Pattern di controllo Text e TextRange</span><span class="sxs-lookup"><span data-stu-id="4856a-134">Text and TextRange Control Patterns</span></span>](uiauto-implementingtextandtextrange.md)
-   [<span data-ttu-id="4856a-135">Pattern di controllo TextChild</span><span class="sxs-lookup"><span data-stu-id="4856a-135">TextChild Control Pattern</span></span>](textchild-control-pattern.md)
-   [<span data-ttu-id="4856a-136">Pattern di controllo TextEdit</span><span class="sxs-lookup"><span data-stu-id="4856a-136">TextEdit Control Pattern</span></span>](textedit-control-pattern.md)
-   [<span data-ttu-id="4856a-137">Mostra/Nascondi pattern di controllo</span><span class="sxs-lookup"><span data-stu-id="4856a-137">Toggle Control Pattern</span></span>](uiauto-implementingtoggle.md)
-   [<span data-ttu-id="4856a-138">Pattern di controllo Transform</span><span class="sxs-lookup"><span data-stu-id="4856a-138">Transform Control Pattern</span></span>](uiauto-implementingtransform.md)
-   [<span data-ttu-id="4856a-139">Pattern di controllo value</span><span class="sxs-lookup"><span data-stu-id="4856a-139">Value Control Pattern</span></span>](uiauto-implementingvalue.md)
-   [<span data-ttu-id="4856a-140">Pattern di controllo VirtualizedItem</span><span class="sxs-lookup"><span data-stu-id="4856a-140">VirtualizedItem Control Pattern</span></span>](uiauto-implementingvirtualizeditem.md)
-   [<span data-ttu-id="4856a-141">Pattern di controllo Window</span><span class="sxs-lookup"><span data-stu-id="4856a-141">Window Control Pattern</span></span>](uiauto-implementingwindow.md)

## <a name="related-topics"></a><span data-ttu-id="4856a-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4856a-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4856a-143">Guida per programmatori del provider di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="4856a-143">UI Automation Provider Programmer's Guide</span></span>](uiauto-providerportal.md)
</dt> <dt>

[<span data-ttu-id="4856a-144">Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="4856a-144">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="4856a-145">Supporto di tipi di controllo di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="4856a-145">Supporting UI Automation Control Types</span></span>](uiauto-supportinguiautocontroltypes.md)
</dt> </dl>

 

 