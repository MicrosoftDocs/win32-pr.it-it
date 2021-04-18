---
title: Supporto per automazione interfaccia utente dei controlli standard
description: Questo argomento identifica i controlli Windows standard supportati dall'automazione interfaccia utente Microsoft. Il supporto completo viene fornito solo per i controlli della versione 6 di ComCtrl32.dll (disponibile in Windows XP e versioni successive).
ms.assetid: 4821684c-8a90-413c-8ddc-699926e3bb09
keywords:
- client, supporto di automazione interfaccia utente per i controlli standard
- client, supporto del controllo standard
- client, controlli Win32
- Automazione interfaccia utente, supporto per controlli standard
- Automazione interfaccia utente, supporto del controllo standard
- Automazione interfaccia utente, controlli Win32
- supporto per i controlli standard
- supporto del controllo standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae6e384b9ee0fd72fd8a41aa3f791a5c996fe6d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515535"
---
# <a name="ui-automation-support-for-standard-controls"></a><span data-ttu-id="d1be9-112">Supporto per automazione interfaccia utente dei controlli standard</span><span class="sxs-lookup"><span data-stu-id="d1be9-112">UI Automation Support for Standard Controls</span></span>

<span data-ttu-id="d1be9-113">Questo argomento identifica i controlli Windows standard supportati dall'automazione interfaccia utente Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d1be9-113">This topic identifies the standard Windows controls that are supported by Microsoft UI Automation.</span></span> <span data-ttu-id="d1be9-114">Il supporto completo viene fornito solo per i controlli della versione 6 di ComCtrl32.dll (disponibile in Windows XP e versioni successive).</span><span class="sxs-lookup"><span data-stu-id="d1be9-114">Full support is provided only for controls from version 6 of ComCtrl32.dll (available with Windows XP and later).</span></span>

> [!Note]  
> <span data-ttu-id="d1be9-115">Il controllo RichEdit è supportato solo per le versioni fornite con Windows Vista (in RichEd20.dll versione 3,1 e successive e MsftEdit.dll versione 4,1 e successive).</span><span class="sxs-lookup"><span data-stu-id="d1be9-115">The RichEdit control is supported only for versions shipped with Windows Vista (in RichEd20.dll version 3.1 and later, and MsftEdit.dll version 4.1 and later).</span></span>

 

<span data-ttu-id="d1be9-116">La tabella seguente elenca i nomi delle classi dei controlli standard supportati, insieme ai corrispondenti tipi di controllo di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="d1be9-116">The following table lists the class names of the supported standard controls, along with the corresponding UI Automation control types.</span></span>



| <span data-ttu-id="d1be9-117">Nome della classe</span><span class="sxs-lookup"><span data-stu-id="d1be9-117">Class Name</span></span>          | <span data-ttu-id="d1be9-118">Tipo di controllo</span><span class="sxs-lookup"><span data-stu-id="d1be9-118">Control Type</span></span>        |
|---------------------|---------------------|
| <span data-ttu-id="d1be9-119">Button</span><span class="sxs-lookup"><span data-stu-id="d1be9-119">Button</span></span>              | <span data-ttu-id="d1be9-120">Button</span><span class="sxs-lookup"><span data-stu-id="d1be9-120">Button</span></span>              |
| <span data-ttu-id="d1be9-121">Button</span><span class="sxs-lookup"><span data-stu-id="d1be9-121">Button</span></span>              | <span data-ttu-id="d1be9-122">RadioButton</span><span class="sxs-lookup"><span data-stu-id="d1be9-122">RadioButton</span></span>         |
| <span data-ttu-id="d1be9-123">Pulsante</span><span class="sxs-lookup"><span data-stu-id="d1be9-123">Button</span></span>              | <span data-ttu-id="d1be9-124">Group</span><span class="sxs-lookup"><span data-stu-id="d1be9-124">Group</span></span>               |
| <span data-ttu-id="d1be9-125">Pulsante</span><span class="sxs-lookup"><span data-stu-id="d1be9-125">Button</span></span>              | <span data-ttu-id="d1be9-126">CheckBox</span><span class="sxs-lookup"><span data-stu-id="d1be9-126">CheckBox</span></span>            |
| <span data-ttu-id="d1be9-127">Pulsante</span><span class="sxs-lookup"><span data-stu-id="d1be9-127">Button</span></span>              | <span data-ttu-id="d1be9-128">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="d1be9-128">Hyperlink</span></span>           |
| <span data-ttu-id="d1be9-129">Pulsante</span><span class="sxs-lookup"><span data-stu-id="d1be9-129">Button</span></span>              | <span data-ttu-id="d1be9-130">SplitButton</span><span class="sxs-lookup"><span data-stu-id="d1be9-130">SplitButton</span></span>         |
| <span data-ttu-id="d1be9-131">Pulsante</span><span class="sxs-lookup"><span data-stu-id="d1be9-131">Button</span></span>              | <span data-ttu-id="d1be9-132">CheckBox</span><span class="sxs-lookup"><span data-stu-id="d1be9-132">CheckBox</span></span>            |
| <span data-ttu-id="d1be9-133">ComboBoxEx32</span><span class="sxs-lookup"><span data-stu-id="d1be9-133">ComboBoxEx32</span></span>        | <span data-ttu-id="d1be9-134">ComboBox</span><span class="sxs-lookup"><span data-stu-id="d1be9-134">ComboBox</span></span>            |
| <span data-ttu-id="d1be9-135">ComboBox</span><span class="sxs-lookup"><span data-stu-id="d1be9-135">ComboBox</span></span>            | <span data-ttu-id="d1be9-136">ComboBox</span><span class="sxs-lookup"><span data-stu-id="d1be9-136">ComboBox</span></span>            |
| <span data-ttu-id="d1be9-137">Modifica</span><span class="sxs-lookup"><span data-stu-id="d1be9-137">Edit</span></span>                | <span data-ttu-id="d1be9-138">Documento</span><span class="sxs-lookup"><span data-stu-id="d1be9-138">Document</span></span>            |
| <span data-ttu-id="d1be9-139">Modifica</span><span class="sxs-lookup"><span data-stu-id="d1be9-139">Edit</span></span>                | <span data-ttu-id="d1be9-140">Modifica</span><span class="sxs-lookup"><span data-stu-id="d1be9-140">Edit</span></span>                |
| <span data-ttu-id="d1be9-141">SysLink</span><span class="sxs-lookup"><span data-stu-id="d1be9-141">SysLink</span></span>             | <span data-ttu-id="d1be9-142">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="d1be9-142">Hyperlink</span></span>           |
| <span data-ttu-id="d1be9-143">Static</span><span class="sxs-lookup"><span data-stu-id="d1be9-143">Static</span></span>              | <span data-ttu-id="d1be9-144">Testo</span><span class="sxs-lookup"><span data-stu-id="d1be9-144">Text</span></span>                |
| <span data-ttu-id="d1be9-145">Static</span><span class="sxs-lookup"><span data-stu-id="d1be9-145">Static</span></span>              | <span data-ttu-id="d1be9-146">Immagine</span><span class="sxs-lookup"><span data-stu-id="d1be9-146">Image</span></span>               |
| <span data-ttu-id="d1be9-147">SysIPAddress32</span><span class="sxs-lookup"><span data-stu-id="d1be9-147">SysIPAddress32</span></span>      | <span data-ttu-id="d1be9-148">Personalizzato</span><span class="sxs-lookup"><span data-stu-id="d1be9-148">Custom</span></span>              |
| <span data-ttu-id="d1be9-149">SysHeader32</span><span class="sxs-lookup"><span data-stu-id="d1be9-149">SysHeader32</span></span>         | <span data-ttu-id="d1be9-150">Header/HeaderItem</span><span class="sxs-lookup"><span data-stu-id="d1be9-150">Header/HeaderItem</span></span>   |
| <span data-ttu-id="d1be9-151">SysListView32</span><span class="sxs-lookup"><span data-stu-id="d1be9-151">SysListView32</span></span>       | <span data-ttu-id="d1be9-152">DataGrid</span><span class="sxs-lookup"><span data-stu-id="d1be9-152">DataGrid</span></span>            |
| <span data-ttu-id="d1be9-153">SysListView32</span><span class="sxs-lookup"><span data-stu-id="d1be9-153">SysListView32</span></span>       | <span data-ttu-id="d1be9-154">Elenco</span><span class="sxs-lookup"><span data-stu-id="d1be9-154">List</span></span>                |
| <span data-ttu-id="d1be9-155">ListBox</span><span class="sxs-lookup"><span data-stu-id="d1be9-155">ListBox</span></span>             | <span data-ttu-id="d1be9-156">Elenco</span><span class="sxs-lookup"><span data-stu-id="d1be9-156">List</span></span>                |
| <span data-ttu-id="d1be9-157">ListBox</span><span class="sxs-lookup"><span data-stu-id="d1be9-157">ListBox</span></span>             | <span data-ttu-id="d1be9-158">ListItem</span><span class="sxs-lookup"><span data-stu-id="d1be9-158">ListItem</span></span>            |
| <span data-ttu-id="d1be9-159">\#32768</span><span class="sxs-lookup"><span data-stu-id="d1be9-159">\#32768</span></span>             | <span data-ttu-id="d1be9-160">Menu</span><span class="sxs-lookup"><span data-stu-id="d1be9-160">Menu</span></span>                |
| <span data-ttu-id="d1be9-161">\#32768</span><span class="sxs-lookup"><span data-stu-id="d1be9-161">\#32768</span></span>             | <span data-ttu-id="d1be9-162">MenuItem</span><span class="sxs-lookup"><span data-stu-id="d1be9-162">MenuItem</span></span>            |
| <span data-ttu-id="d1be9-163">\_progress32 msctls</span><span class="sxs-lookup"><span data-stu-id="d1be9-163">msctls\_progress32</span></span>  | <span data-ttu-id="d1be9-164">ProgressBar</span><span class="sxs-lookup"><span data-stu-id="d1be9-164">ProgressBar</span></span>         |
| <span data-ttu-id="d1be9-165">RichEdit</span><span class="sxs-lookup"><span data-stu-id="d1be9-165">RichEdit</span></span>            | <span data-ttu-id="d1be9-166">Documento.</span><span class="sxs-lookup"><span data-stu-id="d1be9-166">Document.</span></span> <span data-ttu-id="d1be9-167">Vedere la nota.</span><span class="sxs-lookup"><span data-stu-id="d1be9-167">See note.</span></span> |
| <span data-ttu-id="d1be9-168">RichEdit20A</span><span class="sxs-lookup"><span data-stu-id="d1be9-168">RichEdit20A</span></span>         | <span data-ttu-id="d1be9-169">Documento</span><span class="sxs-lookup"><span data-stu-id="d1be9-169">Document</span></span>            |
| <span data-ttu-id="d1be9-170">RichEdit20W</span><span class="sxs-lookup"><span data-stu-id="d1be9-170">RichEdit20W</span></span>         | <span data-ttu-id="d1be9-171">Documento</span><span class="sxs-lookup"><span data-stu-id="d1be9-171">Document</span></span>            |
| <span data-ttu-id="d1be9-172">RichEdit50W</span><span class="sxs-lookup"><span data-stu-id="d1be9-172">RichEdit50W</span></span>         | <span data-ttu-id="d1be9-173">Documento</span><span class="sxs-lookup"><span data-stu-id="d1be9-173">Document</span></span>            |
| <span data-ttu-id="d1be9-174">ScrollBar</span><span class="sxs-lookup"><span data-stu-id="d1be9-174">ScrollBar</span></span>           | <span data-ttu-id="d1be9-175">Slider</span><span class="sxs-lookup"><span data-stu-id="d1be9-175">Slider</span></span>              |
| <span data-ttu-id="d1be9-176">\_trackbar32 msctls</span><span class="sxs-lookup"><span data-stu-id="d1be9-176">msctls\_trackbar32</span></span>  | <span data-ttu-id="d1be9-177">Slider</span><span class="sxs-lookup"><span data-stu-id="d1be9-177">Slider</span></span>              |
| <span data-ttu-id="d1be9-178">\_updown32 msctls</span><span class="sxs-lookup"><span data-stu-id="d1be9-178">msctls\_updown32</span></span>    | <span data-ttu-id="d1be9-179">Spinner</span><span class="sxs-lookup"><span data-stu-id="d1be9-179">Spinner</span></span>             |
| <span data-ttu-id="d1be9-180">\_statusbar32 msctls</span><span class="sxs-lookup"><span data-stu-id="d1be9-180">msctls\_statusbar32</span></span> | <span data-ttu-id="d1be9-181">StatusBar</span><span class="sxs-lookup"><span data-stu-id="d1be9-181">StatusBar</span></span>           |
| <span data-ttu-id="d1be9-182">SysTabControl32</span><span class="sxs-lookup"><span data-stu-id="d1be9-182">SysTabControl32</span></span>     | <span data-ttu-id="d1be9-183">Scheda</span><span class="sxs-lookup"><span data-stu-id="d1be9-183">Tab</span></span>                 |
| <span data-ttu-id="d1be9-184">SysTabControl32</span><span class="sxs-lookup"><span data-stu-id="d1be9-184">SysTabControl32</span></span>     | <span data-ttu-id="d1be9-185">TabItem</span><span class="sxs-lookup"><span data-stu-id="d1be9-185">TabItem</span></span>             |
| <span data-ttu-id="d1be9-186">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="d1be9-186">ToolbarWindow32</span></span>     | <span data-ttu-id="d1be9-187">ToolBar</span><span class="sxs-lookup"><span data-stu-id="d1be9-187">ToolBar</span></span>             |
| <span data-ttu-id="d1be9-188">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="d1be9-188">ToolbarWindow32</span></span>     | <span data-ttu-id="d1be9-189">MenuItem</span><span class="sxs-lookup"><span data-stu-id="d1be9-189">MenuItem</span></span>            |
| <span data-ttu-id="d1be9-190">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="d1be9-190">ToolbarWindow32</span></span>     | <span data-ttu-id="d1be9-191">Pulsante</span><span class="sxs-lookup"><span data-stu-id="d1be9-191">Button</span></span>              |
| <span data-ttu-id="d1be9-192">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="d1be9-192">ToolbarWindow32</span></span>     | <span data-ttu-id="d1be9-193">CheckBox</span><span class="sxs-lookup"><span data-stu-id="d1be9-193">CheckBox</span></span>            |
| <span data-ttu-id="d1be9-194">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="d1be9-194">ToolbarWindow32</span></span>     | <span data-ttu-id="d1be9-195">RadioButton</span><span class="sxs-lookup"><span data-stu-id="d1be9-195">RadioButton</span></span>         |
| <span data-ttu-id="d1be9-196">ToolbarWindow32</span><span class="sxs-lookup"><span data-stu-id="d1be9-196">ToolbarWindow32</span></span>     | <span data-ttu-id="d1be9-197">Separatore</span><span class="sxs-lookup"><span data-stu-id="d1be9-197">Separator</span></span>           |
| <span data-ttu-id="d1be9-198">descrizioni comandi \_ class32</span><span class="sxs-lookup"><span data-stu-id="d1be9-198">tooltips\_class32</span></span>   | <span data-ttu-id="d1be9-199">ToolTip</span><span class="sxs-lookup"><span data-stu-id="d1be9-199">ToolTip</span></span>             |
| <span data-ttu-id="d1be9-200">\#32774</span><span class="sxs-lookup"><span data-stu-id="d1be9-200">\#32774</span></span>             | <span data-ttu-id="d1be9-201">ToolTip</span><span class="sxs-lookup"><span data-stu-id="d1be9-201">ToolTip</span></span>             |
| <span data-ttu-id="d1be9-202">ReBarWindow32</span><span class="sxs-lookup"><span data-stu-id="d1be9-202">ReBarWindow32</span></span>       | <span data-ttu-id="d1be9-203">Barra degli strumenti</span><span class="sxs-lookup"><span data-stu-id="d1be9-203">Toolbar</span></span>             |
| <span data-ttu-id="d1be9-204">SysTreeView32</span><span class="sxs-lookup"><span data-stu-id="d1be9-204">SysTreeView32</span></span>       | <span data-ttu-id="d1be9-205">Albero</span><span class="sxs-lookup"><span data-stu-id="d1be9-205">Tree</span></span>                |
| <span data-ttu-id="d1be9-206">SysTreeView32</span><span class="sxs-lookup"><span data-stu-id="d1be9-206">SysTreeView32</span></span>       | <span data-ttu-id="d1be9-207">TreeItem</span><span class="sxs-lookup"><span data-stu-id="d1be9-207">TreeItem</span></span>            |



 

<span data-ttu-id="d1be9-208">I controlli elencati nella tabella seguente non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="d1be9-208">The controls listed in the following table are not supported.</span></span>



| <span data-ttu-id="d1be9-209">Nome della classe</span><span class="sxs-lookup"><span data-stu-id="d1be9-209">Class Name</span></span>                                    | <span data-ttu-id="d1be9-210">Tipo di controllo</span><span class="sxs-lookup"><span data-stu-id="d1be9-210">Control Type</span></span> |
|-----------------------------------------------|--------------|
| <span data-ttu-id="d1be9-211">SysAnimate32</span><span class="sxs-lookup"><span data-stu-id="d1be9-211">SysAnimate32</span></span>                                  | <span data-ttu-id="d1be9-212">Immagine</span><span class="sxs-lookup"><span data-stu-id="d1be9-212">Image</span></span>        |
| <span data-ttu-id="d1be9-213">SysPager</span><span class="sxs-lookup"><span data-stu-id="d1be9-213">SysPager</span></span>                                      | <span data-ttu-id="d1be9-214">Spinner</span><span class="sxs-lookup"><span data-stu-id="d1be9-214">Spinner</span></span>      |
| <span data-ttu-id="d1be9-215">SysDateTimePick32</span><span class="sxs-lookup"><span data-stu-id="d1be9-215">SysDateTimePick32</span></span>                             | <span data-ttu-id="d1be9-216">Personalizzato</span><span class="sxs-lookup"><span data-stu-id="d1be9-216">Custom</span></span>       |
| <span data-ttu-id="d1be9-217">SysMonthCal32</span><span class="sxs-lookup"><span data-stu-id="d1be9-217">SysMonthCal32</span></span>                                 | <span data-ttu-id="d1be9-218">Calendario</span><span class="sxs-lookup"><span data-stu-id="d1be9-218">Calendar</span></span>     |
| <span data-ttu-id="d1be9-219">MS \_ WINNOTE</span><span class="sxs-lookup"><span data-stu-id="d1be9-219">MS\_WINNOTE</span></span>                                   | <span data-ttu-id="d1be9-220">Descrizione comando</span><span class="sxs-lookup"><span data-stu-id="d1be9-220">Tooltip</span></span>      |
| <span data-ttu-id="d1be9-221">VBBubble</span><span class="sxs-lookup"><span data-stu-id="d1be9-221">VBBubble</span></span>                                      | <span data-ttu-id="d1be9-222">Descrizione comando</span><span class="sxs-lookup"><span data-stu-id="d1be9-222">Tooltip</span></span>      |
| <span data-ttu-id="d1be9-223">ScrollBar (se usato come controllo autonomo)</span><span class="sxs-lookup"><span data-stu-id="d1be9-223">ScrollBar (when used as a standalone control)</span></span> | <span data-ttu-id="d1be9-224">Slider</span><span class="sxs-lookup"><span data-stu-id="d1be9-224">Slider</span></span>       |
| <span data-ttu-id="d1be9-225">SuperGrid</span><span class="sxs-lookup"><span data-stu-id="d1be9-225">SuperGrid</span></span>                                     | <span data-ttu-id="d1be9-226">Personalizzato</span><span class="sxs-lookup"><span data-stu-id="d1be9-226">Custom</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="d1be9-227">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d1be9-227">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1be9-228">Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="d1be9-228">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> </dl>

 

 




