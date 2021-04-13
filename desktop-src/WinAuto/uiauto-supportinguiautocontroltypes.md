---
title: Supporto di tipi di controllo di automazione interfaccia utente
description: Questa sezione contiene informazioni dettagliate sulla struttura ad albero, le proprietà, i pattern di controllo e gli eventi necessari per supportare ogni tipo di controllo di automazione interfaccia utente Microsoft.
ms.assetid: 35232907-6c54-47cd-b82a-0daee279ef17
keywords:
- Automazione interfaccia utente, informazioni sui tipi di controllo
- Automazione interfaccia utente, panoramica del tipo di controllo
- supporto per il tipo di controllo
- tipi di controllo, supporto
- tipi di controllo, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26ac6f857da87691428c747cfe5dbff5102218f6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399532"
---
# <a name="supporting-ui-automation-control-types"></a><span data-ttu-id="78185-108">Supporto di tipi di controllo di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="78185-108">Supporting UI Automation Control Types</span></span>

<span data-ttu-id="78185-109">Questa sezione contiene informazioni dettagliate sulla struttura ad albero, le proprietà, i pattern di controllo e gli eventi necessari per supportare ogni tipo di controllo di automazione interfaccia utente Microsoft.</span><span class="sxs-lookup"><span data-stu-id="78185-109">This section contains detailed information about the tree structure, properties, control patterns, and events that each Microsoft UI Automation control type is required to support.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="78185-110">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="78185-110">In this section</span></span>

-   [<span data-ttu-id="78185-111">Tipo di controllo AppBar</span><span class="sxs-lookup"><span data-stu-id="78185-111">AppBar Control Type</span></span>](uiauto-supportappbarcontroltype.md)
-   [<span data-ttu-id="78185-112">Tipo di controllo Button</span><span class="sxs-lookup"><span data-stu-id="78185-112">Button Control Type</span></span>](uiauto-supportbuttoncontroltype.md)
-   [<span data-ttu-id="78185-113">Tipo di controllo Calendar</span><span class="sxs-lookup"><span data-stu-id="78185-113">Calendar Control Type</span></span>](uiauto-supportcalendarcontroltype.md)
-   [<span data-ttu-id="78185-114">Tipo di controllo CheckBox</span><span class="sxs-lookup"><span data-stu-id="78185-114">CheckBox Control Type</span></span>](uiauto-supportcheckboxcontroltype.md)
-   [<span data-ttu-id="78185-115">Tipo di controllo ComboBox</span><span class="sxs-lookup"><span data-stu-id="78185-115">ComboBox Control Type</span></span>](uiauto-supportcomboboxcontroltype.md)
-   [<span data-ttu-id="78185-116">Tipo di controllo DataGrid</span><span class="sxs-lookup"><span data-stu-id="78185-116">DataGrid Control Type</span></span>](uiauto-supportdatagridcontroltype.md)
-   [<span data-ttu-id="78185-117">Tipo di controllo DataItem</span><span class="sxs-lookup"><span data-stu-id="78185-117">DataItem Control Type</span></span>](uiauto-supportdataitemcontroltype.md)
-   [<span data-ttu-id="78185-118">Tipo di controllo Document</span><span class="sxs-lookup"><span data-stu-id="78185-118">Document Control Type</span></span>](uiauto-supportdocumentcontroltype.md)
-   [<span data-ttu-id="78185-119">Modificare il tipo di controllo</span><span class="sxs-lookup"><span data-stu-id="78185-119">Edit Control Type</span></span>](uiauto-supporteditcontroltype.md)
-   [<span data-ttu-id="78185-120">Tipo di controllo gruppo</span><span class="sxs-lookup"><span data-stu-id="78185-120">Group Control Type</span></span>](uiauto-supportgroupcontroltype.md)
-   [<span data-ttu-id="78185-121">Tipo di controllo Header</span><span class="sxs-lookup"><span data-stu-id="78185-121">Header Control Type</span></span>](uiauto-supportheadercontroltype.md)
-   [<span data-ttu-id="78185-122">Tipo di controllo HeaderItem</span><span class="sxs-lookup"><span data-stu-id="78185-122">HeaderItem Control Type</span></span>](uiauto-supportheaderitemcontroltype.md)
-   [<span data-ttu-id="78185-123">Tipo di controllo HyperLink</span><span class="sxs-lookup"><span data-stu-id="78185-123">Hyperlink Control Type</span></span>](uiauto-supporthyperlinkcontroltype.md)
-   [<span data-ttu-id="78185-124">Tipo di controllo Image</span><span class="sxs-lookup"><span data-stu-id="78185-124">Image Control Type</span></span>](uiauto-supportimagecontroltype.md)
-   [<span data-ttu-id="78185-125">Tipo di controllo List</span><span class="sxs-lookup"><span data-stu-id="78185-125">List Control Type</span></span>](uiauto-supportlistcontroltype.md)
-   [<span data-ttu-id="78185-126">Tipo di controllo ListItem</span><span class="sxs-lookup"><span data-stu-id="78185-126">ListItem Control Type</span></span>](uiauto-supportlistitemcontroltype.md)
-   [<span data-ttu-id="78185-127">Tipo di controllo menu</span><span class="sxs-lookup"><span data-stu-id="78185-127">Menu Control Type</span></span>](uiauto-supportmenucontroltype.md)
-   [<span data-ttu-id="78185-128">Tipo di controllo barra dei menu</span><span class="sxs-lookup"><span data-stu-id="78185-128">MenuBar Control Type</span></span>](uiauto-supportmenubarcontroltype.md)
-   [<span data-ttu-id="78185-129">Tipo di controllo MenuItem</span><span class="sxs-lookup"><span data-stu-id="78185-129">MenuItem Control Type</span></span>](uiauto-supportmenuitemcontroltype.md)
-   [<span data-ttu-id="78185-130">Tipo di controllo pane</span><span class="sxs-lookup"><span data-stu-id="78185-130">Pane Control Type</span></span>](uiauto-supportpanecontroltype.md)
-   [<span data-ttu-id="78185-131">Tipo di controllo ProgressBar</span><span class="sxs-lookup"><span data-stu-id="78185-131">ProgressBar Control Type</span></span>](uiauto-supportprogressbarcontroltype.md)
-   [<span data-ttu-id="78185-132">RadioButton (tipo di controllo)</span><span class="sxs-lookup"><span data-stu-id="78185-132">RadioButton Control Type</span></span>](uiauto-supportradiobuttoncontroltype.md)
-   [<span data-ttu-id="78185-133">Tipo di controllo ScrollBar</span><span class="sxs-lookup"><span data-stu-id="78185-133">ScrollBar Control Type</span></span>](uiauto-supportscrollbarcontroltype.md)
-   [<span data-ttu-id="78185-134">Tipo di controllo SemanticZoom</span><span class="sxs-lookup"><span data-stu-id="78185-134">SemanticZoom Control Type</span></span>](/windows/desktop/WinAuto/uiauto-supportsemanticzoomcontroltype)
-   [<span data-ttu-id="78185-135">Tipo di controllo Separator</span><span class="sxs-lookup"><span data-stu-id="78185-135">Separator Control Type</span></span>](uiauto-supportseparatorcontroltype.md)
-   [<span data-ttu-id="78185-136">Tipo di controllo Slider</span><span class="sxs-lookup"><span data-stu-id="78185-136">Slider Control Type</span></span>](uiauto-supportslidercontroltype.md)
-   [<span data-ttu-id="78185-137">Tipo di controllo Spinner</span><span class="sxs-lookup"><span data-stu-id="78185-137">Spinner Control Type</span></span>](uiauto-supportspinnercontroltype.md)
-   [<span data-ttu-id="78185-138">Tipo di controllo SplitButton</span><span class="sxs-lookup"><span data-stu-id="78185-138">SplitButton Control Type</span></span>](uiauto-supportsplitbuttoncontroltype.md)
-   [<span data-ttu-id="78185-139">Tipo di controllo StatusBar</span><span class="sxs-lookup"><span data-stu-id="78185-139">StatusBar Control Type</span></span>](uiauto-supportstatusbarcontroltype.md)
-   [<span data-ttu-id="78185-140">Tipo di controllo Tab</span><span class="sxs-lookup"><span data-stu-id="78185-140">Tab Control Type</span></span>](uiauto-supporttabcontroltype.md)
-   [<span data-ttu-id="78185-141">Tipo di controllo TabItem</span><span class="sxs-lookup"><span data-stu-id="78185-141">TabItem Control Type</span></span>](uiauto-supporttabitemcontroltype.md)
-   [<span data-ttu-id="78185-142">Tipo di controllo Table</span><span class="sxs-lookup"><span data-stu-id="78185-142">Table Control Type</span></span>](uiauto-supporttablecontroltype.md)
-   [<span data-ttu-id="78185-143">Tipo di controllo Text</span><span class="sxs-lookup"><span data-stu-id="78185-143">Text Control Type</span></span>](uiauto-supporttextcontroltype.md)
-   [<span data-ttu-id="78185-144">Tipo di controllo Thumb</span><span class="sxs-lookup"><span data-stu-id="78185-144">Thumb Control Type</span></span>](uiauto-supportthumbcontroltype.md)
-   [<span data-ttu-id="78185-145">Tipo di controllo barra di titolo</span><span class="sxs-lookup"><span data-stu-id="78185-145">TitleBar Control Type</span></span>](uiauto-supporttitlebarcontroltype.md)
-   [<span data-ttu-id="78185-146">Tipo di controllo ToolBar</span><span class="sxs-lookup"><span data-stu-id="78185-146">ToolBar Control Type</span></span>](uiauto-supporttoolbarcontroltype.md)
-   [<span data-ttu-id="78185-147">Tipo di controllo ToolTip</span><span class="sxs-lookup"><span data-stu-id="78185-147">ToolTip Control Type</span></span>](uiauto-supporttooltipcontroltype.md)
-   [<span data-ttu-id="78185-148">Tipo di controllo Tree</span><span class="sxs-lookup"><span data-stu-id="78185-148">Tree Control Type</span></span>](uiauto-supporttreecontroltype.md)
-   [<span data-ttu-id="78185-149">Tipo di controllo TreeItem</span><span class="sxs-lookup"><span data-stu-id="78185-149">TreeItem Control Type</span></span>](uiauto-supporttreeitemcontroltype.md)
-   [<span data-ttu-id="78185-150">Tipo di controllo Window</span><span class="sxs-lookup"><span data-stu-id="78185-150">Window Control Type</span></span>](uiauto-supportwindowcontroltype.md)

## <a name="related-topics"></a><span data-ttu-id="78185-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="78185-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78185-152">Guida per programmatori del provider di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="78185-152">UI Automation Provider Programmer's Guide</span></span>](uiauto-providerportal.md)
</dt> </dl>

 

 