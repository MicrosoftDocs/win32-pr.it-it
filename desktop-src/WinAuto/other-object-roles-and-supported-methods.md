---
title: Altri ruoli oggetto e metodi supportati (riferimento all'elemento dell'interfaccia utente MSAA)
description: In questo argomento vengono fornite informazioni sui ruoli degli oggetti che non sono inclusi negli argomenti precedenti per gli elementi dell'interfaccia utente.
ms.assetid: 0c3a3ccf-f02a-4aca-9380-a13774598a19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f3d7fbdbb6dfbf83729f3e1c1d4caa3027f8d51
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729026"
---
# <a name="other-object-roles-and-supported-methods-msaa-ui-element-reference"></a><span data-ttu-id="cd6f6-103">Altri ruoli oggetto e metodi supportati (riferimento all'elemento dell'interfaccia utente MSAA)</span><span class="sxs-lookup"><span data-stu-id="cd6f6-103">Other Object Roles and Supported Methods (MSAA UI Element Reference)</span></span>

<span data-ttu-id="cd6f6-104">In questo argomento vengono fornite informazioni sui ruoli degli oggetti che non sono inclusi negli argomenti precedenti per gli elementi dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="cd6f6-104">This topic provides information about object roles that are not included in the previous topics for UI elements.</span></span> <span data-ttu-id="cd6f6-105">Ogni ruolo di oggetto include un elenco dei metodi e delle proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) supportati per il ruolo dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cd6f6-105">Each object role includes a list of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods and properties that are supported for the object role.</span></span> <span data-ttu-id="cd6f6-106">Mentre altri argomenti documentano i metodi e le proprietà **IAccessible** supportati per gli elementi dell'interfaccia utente, in questo argomento vengono elencati i metodi e le proprietà che possono essere supportati per un particolare ruolo dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cd6f6-106">While other topics document supported **IAccessible** methods and properties for UI elements, this topic lists the methods and properties you can expect to be supported for a particular object role.</span></span> <span data-ttu-id="cd6f6-107">Molti degli elementi dell'interfaccia utente che possono avere uno dei ruoli elencati di seguito vengono in genere visualizzati nei browser.</span><span class="sxs-lookup"><span data-stu-id="cd6f6-107">Many of the UI elements which might have one of the roles listed here are typically seen in browsers.</span></span>

> [!Note]  
> <span data-ttu-id="cd6f6-108">Usare questo argomento come linee guida.</span><span class="sxs-lookup"><span data-stu-id="cd6f6-108">Use this topic as a guideline.</span></span> <span data-ttu-id="cd6f6-109">Si consiglia vivamente di utilizzare gli strumenti di Microsoft Active Accessibility per verificare il comportamento previsto per un singolo ruolo di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="cd6f6-109">We strongly suggest that you use Microsoft Active Accessibility tools to verify expected behavior for an individual object role.</span></span>

 

<span data-ttu-id="cd6f6-110">Nella tabella seguente sono elencati i ruoli oggetto aggiuntivi Oleacc.dll supportati da.</span><span class="sxs-lookup"><span data-stu-id="cd6f6-110">The following table lists additional object roles which Oleacc.dll supports.</span></span>



|                                                                         |                                                           |
|-------------------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="cd6f6-111">**\_avviso di sistema del ruolo \_**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-111">**ROLE\_SYSTEM\_ALERT**</span></span>](/windows)                           | [<span data-ttu-id="cd6f6-112">**\_elenco a \_ selezione sistema ruolo**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-112">**ROLE\_SYSTEM\_DROPLIST**</span></span>](/windows)       |
| [<span data-ttu-id="cd6f6-113">**\_applicazione di sistema ruolo \_**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-113">**ROLE\_SYSTEM\_APPLICATION**</span></span>](/windows)               | [<span data-ttu-id="cd6f6-114">**\_equazione del sistema di ruolo \_**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-114">**ROLE\_SYSTEM\_EQUATION**</span></span>](/windows)       |
| [<span data-ttu-id="cd6f6-115">**\_bordo sistema \_ ruolo**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-115">**ROLE\_SYSTEM\_BORDER**</span></span>](/windows)                         | [<span data-ttu-id="cd6f6-116">**\_rappresentazione grafica del sistema di ruoli \_**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-116">**ROLE\_SYSTEM\_GRAPHIC**</span></span>](/windows)         |
| [<span data-ttu-id="cd6f6-117">**\_BUTTONDROPDOWN di sistema ruolo \_**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-117">**ROLE\_SYSTEM\_BUTTONDROPDOWN**</span></span>](/windows)         | [<span data-ttu-id="cd6f6-118">**\_HELPBALLOON di sistema ruolo \_**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-118">**ROLE\_SYSTEM\_HELPBALLOON**</span></span>](/windows) |
| [<span data-ttu-id="cd6f6-119">**\_BUTTONDROPDOWNGRID di sistema ruolo \_**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-119">**ROLE\_SYSTEM\_BUTTONDROPDOWNGRID**</span></span>](/windows) | [<span data-ttu-id="cd6f6-120">**\_IPAddress sistema \_ ruolo**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-120">**ROLE\_SYSTEM\_IPADDRESS**</span></span>](/windows)     |
| [<span data-ttu-id="cd6f6-121">**\_BUTTONMENU di sistema ruolo \_**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-121">**ROLE\_SYSTEM\_BUTTONMENU**</span></span>](/windows)                 | [<span data-ttu-id="cd6f6-122">**\_collegamento del sistema ruolo \_**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-122">**ROLE\_SYSTEM\_LINK**</span></span>](/windows)               |
| [<span data-ttu-id="cd6f6-123">**\_cella del sistema del ruolo \_**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-123">**ROLE\_SYSTEM\_CELL**</span></span>](/windows)                             | [<span data-ttu-id="cd6f6-124">**\_riquadro sistema \_ ruoli**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-124">**ROLE\_SYSTEM\_PANE**</span></span>](/windows)               |
| [<span data-ttu-id="cd6f6-125">**\_carattere di sistema ruolo \_**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-125">**ROLE\_SYSTEM\_CHARACTER**</span></span>](/windows)                   | [<span data-ttu-id="cd6f6-126">**\_riga sistema \_ ruolo**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-126">**ROLE\_SYSTEM\_ROW**</span></span>](/windows)                 |
| [<span data-ttu-id="cd6f6-127">**\_grafico del sistema di ruoli \_**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-127">**ROLE\_SYSTEM\_CHART**</span></span>](/windows)                           | [<span data-ttu-id="cd6f6-128">**\_ROWHEADER di sistema ruolo \_**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-128">**ROLE\_SYSTEM\_ROWHEADER**</span></span>](/windows)     |
| [<span data-ttu-id="cd6f6-129">**\_clock di sistema del ruolo \_**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-129">**ROLE\_SYSTEM\_CLOCK**</span></span>](/windows)                           | [<span data-ttu-id="cd6f6-130">**\_separatore di sistema ruolo \_**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-130">**ROLE\_SYSTEM\_SEPARATOR**</span></span>](/windows)     |
| [<span data-ttu-id="cd6f6-131">**\_colonna di sistema del ruolo \_**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-131">**ROLE\_SYSTEM\_COLUMN**</span></span>](/windows)                         | [<span data-ttu-id="cd6f6-132">**\_suono del sistema di ruolo \_**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-132">**ROLE\_SYSTEM\_SOUND**</span></span>](/windows)             |
| [<span data-ttu-id="cd6f6-133">**\_diagramma del sistema di ruoli \_**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-133">**ROLE\_SYSTEM\_DIAGRAM**</span></span>](/windows)                       | [<span data-ttu-id="cd6f6-134">**\_SPLITBUTTON di sistema ruolo \_**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-134">**ROLE\_SYSTEM\_SPLITBUTTON**</span></span>](/windows) |
| [<span data-ttu-id="cd6f6-135">**\_Composizione sistema \_ ruolo**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-135">**ROLE\_SYSTEM\_DIAL**</span></span>](/windows)                             | [<span data-ttu-id="cd6f6-136">**\_tabella di sistema del ruolo \_**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-136">**ROLE\_SYSTEM\_TABLE**</span></span>](/windows)             |
| [<span data-ttu-id="cd6f6-137">**\_documento di sistema del ruolo \_**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-137">**ROLE\_SYSTEM\_DOCUMENT**</span></span>](/windows)                     | [<span data-ttu-id="cd6f6-138">**\_spazio del sistema ruolo \_**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-138">**ROLE\_SYSTEM\_WHITESPACE**</span></span>](/windows)   |



 

## <a name="role_system_alert"></a><span data-ttu-id="cd6f6-139">\_avviso di sistema del ruolo \_</span><span class="sxs-lookup"><span data-stu-id="cd6f6-139">ROLE\_SYSTEM\_ALERT</span></span>

<span data-ttu-id="cd6f6-140">Per ulteriori informazioni su questo ruolo, vedere [**\_ \_ avviso di sistema dei ruoli**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="cd6f6-140">For more information on this role, see [**ROLE\_SYSTEM\_ALERT**](object-roles.md).</span></span>

<span data-ttu-id="cd6f6-141">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-141">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="cd6f6-142">ottenere \_ accName</span><span class="sxs-lookup"><span data-stu-id="cd6f6-142">get\_accName</span></span>
-   <span data-ttu-id="cd6f6-143">ottenere \_ accRole</span><span class="sxs-lookup"><span data-stu-id="cd6f6-143">get\_accRole</span></span>
-   <span data-ttu-id="cd6f6-144">ottenere \_ accState</span><span class="sxs-lookup"><span data-stu-id="cd6f6-144">get\_accState</span></span>

## <a name="role_system_application"></a><span data-ttu-id="cd6f6-145">\_applicazione di sistema ruolo \_</span><span class="sxs-lookup"><span data-stu-id="cd6f6-145">ROLE\_SYSTEM\_APPLICATION</span></span>

<span data-ttu-id="cd6f6-146">Per altre informazioni su questo ruolo, vedere [**\_ \_ applicazione di sistema dei ruoli**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="cd6f6-146">For more information on this role, see [**ROLE\_SYSTEM\_APPLICATION**](object-roles.md).</span></span>

<span data-ttu-id="cd6f6-147">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-147">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="cd6f6-148">accHitTest</span><span class="sxs-lookup"><span data-stu-id="cd6f6-148">accHitTest</span></span>
-   <span data-ttu-id="cd6f6-149">accLocation</span><span class="sxs-lookup"><span data-stu-id="cd6f6-149">accLocation</span></span>
-   <span data-ttu-id="cd6f6-150">accNavigate</span><span class="sxs-lookup"><span data-stu-id="cd6f6-150">accNavigate</span></span>
-   <span data-ttu-id="cd6f6-151">ottenere \_ accChild</span><span class="sxs-lookup"><span data-stu-id="cd6f6-151">get\_accChild</span></span>
-   <span data-ttu-id="cd6f6-152">ottenere \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="cd6f6-152">get\_accChildCount</span></span>
-   <span data-ttu-id="cd6f6-153">ottenere \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="cd6f6-153">get\_accFocus</span></span>
-   <span data-ttu-id="cd6f6-154">ottenere \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="cd6f6-154">get\_accHelp</span></span>
-   <span data-ttu-id="cd6f6-155">ottenere \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="cd6f6-155">get\_accHelpTopic</span></span>
-   <span data-ttu-id="cd6f6-156">ottenere \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="cd6f6-156">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="cd6f6-157">ottenere \_ accName</span><span class="sxs-lookup"><span data-stu-id="cd6f6-157">get\_accName</span></span>
-   <span data-ttu-id="cd6f6-158">ottenere \_ accParent</span><span class="sxs-lookup"><span data-stu-id="cd6f6-158">get\_accParent</span></span>
-   <span data-ttu-id="cd6f6-159">ottenere \_ accRole</span><span class="sxs-lookup"><span data-stu-id="cd6f6-159">get\_accRole</span></span>
-   <span data-ttu-id="cd6f6-160">ottenere \_ accState</span><span class="sxs-lookup"><span data-stu-id="cd6f6-160">get\_accState</span></span>

## <a name="role_system_border"></a><span data-ttu-id="cd6f6-161">\_bordo sistema \_ ruolo</span><span class="sxs-lookup"><span data-stu-id="cd6f6-161">ROLE\_SYSTEM\_BORDER</span></span>

<span data-ttu-id="cd6f6-162">Per ulteriori informazioni su questo ruolo, vedere [**\_ \_ bordo del sistema dei ruoli**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="cd6f6-162">For more information on this role, see [**ROLE\_SYSTEM\_BORDER**](object-roles.md).</span></span>

<span data-ttu-id="cd6f6-163">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-163">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="cd6f6-164">accHitTest</span><span class="sxs-lookup"><span data-stu-id="cd6f6-164">accHitTest</span></span>
-   <span data-ttu-id="cd6f6-165">accLocation</span><span class="sxs-lookup"><span data-stu-id="cd6f6-165">accLocation</span></span>
-   <span data-ttu-id="cd6f6-166">accNavigate</span><span class="sxs-lookup"><span data-stu-id="cd6f6-166">accNavigate</span></span>
-   <span data-ttu-id="cd6f6-167">ottenere \_ accRole</span><span class="sxs-lookup"><span data-stu-id="cd6f6-167">get\_accRole</span></span>
-   <span data-ttu-id="cd6f6-168">ottenere \_ accState</span><span class="sxs-lookup"><span data-stu-id="cd6f6-168">get\_accState</span></span>

## <a name="role_system_buttondropdown"></a><span data-ttu-id="cd6f6-169">\_BUTTONDROPDOWN di sistema ruolo \_</span><span class="sxs-lookup"><span data-stu-id="cd6f6-169">ROLE\_SYSTEM\_BUTTONDROPDOWN</span></span>

<span data-ttu-id="cd6f6-170">Per ulteriori informazioni su questo ruolo, vedere [**ruolo del \_ sistema \_ BUTTONDROPDOWN**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="cd6f6-170">For more information on this role, see [**ROLE\_SYSTEM\_BUTTONDROPDOWN**](object-roles.md).</span></span>

<span data-ttu-id="cd6f6-171">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-171">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="cd6f6-172">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="cd6f6-172">accDoDefaultAction</span></span>
-   <span data-ttu-id="cd6f6-173">accHitTest</span><span class="sxs-lookup"><span data-stu-id="cd6f6-173">accHitTest</span></span>
-   <span data-ttu-id="cd6f6-174">accLocation</span><span class="sxs-lookup"><span data-stu-id="cd6f6-174">accLocation</span></span>
-   <span data-ttu-id="cd6f6-175">accNavigate</span><span class="sxs-lookup"><span data-stu-id="cd6f6-175">accNavigate</span></span>
-   <span data-ttu-id="cd6f6-176">ottenere \_ accChild</span><span class="sxs-lookup"><span data-stu-id="cd6f6-176">get\_accChild</span></span>
-   <span data-ttu-id="cd6f6-177">ottenere \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="cd6f6-177">get\_accChildCount</span></span>
-   <span data-ttu-id="cd6f6-178">ottenere \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="cd6f6-178">get\_accDefaultAction</span></span>
-   <span data-ttu-id="cd6f6-179">ottenere \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="cd6f6-179">get\_accFocus</span></span>
-   <span data-ttu-id="cd6f6-180">ottenere \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="cd6f6-180">get\_accHelp</span></span>
-   <span data-ttu-id="cd6f6-181">ottenere \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="cd6f6-181">get\_accHelpTopic</span></span>
-   <span data-ttu-id="cd6f6-182">ottenere \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="cd6f6-182">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="cd6f6-183">ottenere \_ accName</span><span class="sxs-lookup"><span data-stu-id="cd6f6-183">get\_accName</span></span>
-   <span data-ttu-id="cd6f6-184">ottenere \_ accParent</span><span class="sxs-lookup"><span data-stu-id="cd6f6-184">get\_accParent</span></span>
-   <span data-ttu-id="cd6f6-185">ottenere \_ accRole</span><span class="sxs-lookup"><span data-stu-id="cd6f6-185">get\_accRole</span></span>
-   <span data-ttu-id="cd6f6-186">ottenere \_ accState</span><span class="sxs-lookup"><span data-stu-id="cd6f6-186">get\_accState</span></span>

## <a name="role_system_buttondropdowngrid"></a><span data-ttu-id="cd6f6-187">\_BUTTONDROPDOWNGRID di sistema ruolo \_</span><span class="sxs-lookup"><span data-stu-id="cd6f6-187">ROLE\_SYSTEM\_BUTTONDROPDOWNGRID</span></span>

<span data-ttu-id="cd6f6-188">Per ulteriori informazioni su questo ruolo, vedere [**ruolo del \_ sistema \_ BUTTONDROPDOWNGRID**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="cd6f6-188">For more information on this role, see [**ROLE\_SYSTEM\_BUTTONDROPDOWNGRID**](object-roles.md).</span></span>

<span data-ttu-id="cd6f6-189">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-189">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="cd6f6-190">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="cd6f6-190">accDoDefaultAction</span></span>
-   <span data-ttu-id="cd6f6-191">accHitTest</span><span class="sxs-lookup"><span data-stu-id="cd6f6-191">accHitTest</span></span>
-   <span data-ttu-id="cd6f6-192">accLocation</span><span class="sxs-lookup"><span data-stu-id="cd6f6-192">accLocation</span></span>
-   <span data-ttu-id="cd6f6-193">accNavigate</span><span class="sxs-lookup"><span data-stu-id="cd6f6-193">accNavigate</span></span>
-   <span data-ttu-id="cd6f6-194">ottenere \_ accChild</span><span class="sxs-lookup"><span data-stu-id="cd6f6-194">get\_accChild</span></span>
-   <span data-ttu-id="cd6f6-195">ottenere \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="cd6f6-195">get\_accChildCount</span></span>
-   <span data-ttu-id="cd6f6-196">ottenere \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="cd6f6-196">get\_accDefaultAction</span></span>
-   <span data-ttu-id="cd6f6-197">ottenere \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="cd6f6-197">get\_accFocus</span></span>
-   <span data-ttu-id="cd6f6-198">ottenere \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="cd6f6-198">get\_accHelp</span></span>
-   <span data-ttu-id="cd6f6-199">ottenere \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="cd6f6-199">get\_accHelpTopic</span></span>
-   <span data-ttu-id="cd6f6-200">ottenere \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="cd6f6-200">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="cd6f6-201">ottenere \_ accName</span><span class="sxs-lookup"><span data-stu-id="cd6f6-201">get\_accName</span></span>
-   <span data-ttu-id="cd6f6-202">ottenere \_ accParent</span><span class="sxs-lookup"><span data-stu-id="cd6f6-202">get\_accParent</span></span>
-   <span data-ttu-id="cd6f6-203">ottenere \_ accRole</span><span class="sxs-lookup"><span data-stu-id="cd6f6-203">get\_accRole</span></span>
-   <span data-ttu-id="cd6f6-204">ottenere \_ accState</span><span class="sxs-lookup"><span data-stu-id="cd6f6-204">get\_accState</span></span>

## <a name="role_system_buttonmenu"></a><span data-ttu-id="cd6f6-205">\_BUTTONMENU di sistema ruolo \_</span><span class="sxs-lookup"><span data-stu-id="cd6f6-205">ROLE\_SYSTEM\_BUTTONMENU</span></span>

<span data-ttu-id="cd6f6-206">Per ulteriori informazioni su questo ruolo, vedere [**ruolo del \_ sistema \_ BUTTONMENU**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="cd6f6-206">For more information on this role, see [**ROLE\_SYSTEM\_BUTTONMENU**](object-roles.md).</span></span>

<span data-ttu-id="cd6f6-207">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-207">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="cd6f6-208">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="cd6f6-208">accDoDefaultAction</span></span>
-   <span data-ttu-id="cd6f6-209">accHitTest</span><span class="sxs-lookup"><span data-stu-id="cd6f6-209">accHitTest</span></span>
-   <span data-ttu-id="cd6f6-210">accLocation</span><span class="sxs-lookup"><span data-stu-id="cd6f6-210">accLocation</span></span>
-   <span data-ttu-id="cd6f6-211">accNavigate</span><span class="sxs-lookup"><span data-stu-id="cd6f6-211">accNavigate</span></span>
-   <span data-ttu-id="cd6f6-212">ottenere \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="cd6f6-212">get\_accDefaultAction</span></span>
-   <span data-ttu-id="cd6f6-213">ottenere \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="cd6f6-213">get\_accFocus</span></span>
-   <span data-ttu-id="cd6f6-214">ottenere \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="cd6f6-214">get\_accHelp</span></span>
-   <span data-ttu-id="cd6f6-215">ottenere \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="cd6f6-215">get\_accHelpTopic</span></span>
-   <span data-ttu-id="cd6f6-216">ottenere \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="cd6f6-216">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="cd6f6-217">ottenere \_ accName</span><span class="sxs-lookup"><span data-stu-id="cd6f6-217">get\_accName</span></span>
-   <span data-ttu-id="cd6f6-218">ottenere \_ accParent</span><span class="sxs-lookup"><span data-stu-id="cd6f6-218">get\_accParent</span></span>
-   <span data-ttu-id="cd6f6-219">ottenere \_ accRole</span><span class="sxs-lookup"><span data-stu-id="cd6f6-219">get\_accRole</span></span>
-   <span data-ttu-id="cd6f6-220">ottenere \_ accState</span><span class="sxs-lookup"><span data-stu-id="cd6f6-220">get\_accState</span></span>

## <a name="role_system_cell"></a><span data-ttu-id="cd6f6-221">\_cella del sistema del ruolo \_</span><span class="sxs-lookup"><span data-stu-id="cd6f6-221">ROLE\_SYSTEM\_CELL</span></span>

<span data-ttu-id="cd6f6-222">Per ulteriori informazioni su questo ruolo, vedere [**\_ \_ cella del sistema del ruolo**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="cd6f6-222">For more information on this role, see [**ROLE\_SYSTEM\_CELL**](object-roles.md).</span></span>

<span data-ttu-id="cd6f6-223">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-223">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="cd6f6-224">accHitTest</span><span class="sxs-lookup"><span data-stu-id="cd6f6-224">accHitTest</span></span>
-   <span data-ttu-id="cd6f6-225">accLocation</span><span class="sxs-lookup"><span data-stu-id="cd6f6-225">accLocation</span></span>
-   <span data-ttu-id="cd6f6-226">accNavigate</span><span class="sxs-lookup"><span data-stu-id="cd6f6-226">accNavigate</span></span>
-   <span data-ttu-id="cd6f6-227">accSelect</span><span class="sxs-lookup"><span data-stu-id="cd6f6-227">accSelect</span></span>
-   <span data-ttu-id="cd6f6-228">ottenere \_ accChild</span><span class="sxs-lookup"><span data-stu-id="cd6f6-228">get\_accChild</span></span>
-   <span data-ttu-id="cd6f6-229">ottenere \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="cd6f6-229">get\_accChildCount</span></span>
-   <span data-ttu-id="cd6f6-230">ottenere \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="cd6f6-230">get\_accFocus</span></span>
-   <span data-ttu-id="cd6f6-231">ottenere \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="cd6f6-231">get\_accHelp</span></span>
-   <span data-ttu-id="cd6f6-232">ottenere \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="cd6f6-232">get\_accHelpTopic</span></span>
-   <span data-ttu-id="cd6f6-233">ottenere \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="cd6f6-233">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="cd6f6-234">ottenere \_ accName</span><span class="sxs-lookup"><span data-stu-id="cd6f6-234">get\_accName</span></span>
-   <span data-ttu-id="cd6f6-235">ottenere \_ accParent</span><span class="sxs-lookup"><span data-stu-id="cd6f6-235">get\_accParent</span></span>
-   <span data-ttu-id="cd6f6-236">ottenere \_ accRole</span><span class="sxs-lookup"><span data-stu-id="cd6f6-236">get\_accRole</span></span>
-   <span data-ttu-id="cd6f6-237">ottenere \_ accState</span><span class="sxs-lookup"><span data-stu-id="cd6f6-237">get\_accState</span></span>
-   <span data-ttu-id="cd6f6-238">ottenere \_ accValue</span><span class="sxs-lookup"><span data-stu-id="cd6f6-238">get\_accValue</span></span>

## <a name="role_system_character"></a><span data-ttu-id="cd6f6-239">\_carattere di sistema ruolo \_</span><span class="sxs-lookup"><span data-stu-id="cd6f6-239">ROLE\_SYSTEM\_CHARACTER</span></span>

<span data-ttu-id="cd6f6-240">Per ulteriori informazioni su questo ruolo, vedere [**Role \_ System \_ character**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="cd6f6-240">For more information on this role, see [**ROLE\_SYSTEM\_CHARACTER**](object-roles.md).</span></span>

<span data-ttu-id="cd6f6-241">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-241">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="cd6f6-242">accHitTest</span><span class="sxs-lookup"><span data-stu-id="cd6f6-242">accHitTest</span></span>
-   <span data-ttu-id="cd6f6-243">accLocation</span><span class="sxs-lookup"><span data-stu-id="cd6f6-243">accLocation</span></span>
-   <span data-ttu-id="cd6f6-244">accNavigate</span><span class="sxs-lookup"><span data-stu-id="cd6f6-244">accNavigate</span></span>
-   <span data-ttu-id="cd6f6-245">ottenere \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="cd6f6-245">get\_accDescription</span></span>
-   <span data-ttu-id="cd6f6-246">ottenere \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="cd6f6-246">get\_accFocus</span></span>
-   <span data-ttu-id="cd6f6-247">ottenere \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="cd6f6-247">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="cd6f6-248">ottenere \_ accName</span><span class="sxs-lookup"><span data-stu-id="cd6f6-248">get\_accName</span></span>
-   <span data-ttu-id="cd6f6-249">ottenere \_ accParent</span><span class="sxs-lookup"><span data-stu-id="cd6f6-249">get\_accParent</span></span>
-   <span data-ttu-id="cd6f6-250">ottenere \_ accRole</span><span class="sxs-lookup"><span data-stu-id="cd6f6-250">get\_accRole</span></span>
-   <span data-ttu-id="cd6f6-251">ottenere \_ accState</span><span class="sxs-lookup"><span data-stu-id="cd6f6-251">get\_accState</span></span>
-   <span data-ttu-id="cd6f6-252">ottenere \_ accValue</span><span class="sxs-lookup"><span data-stu-id="cd6f6-252">get\_accValue</span></span>

## <a name="role_system_chart"></a><span data-ttu-id="cd6f6-253">\_grafico del sistema di ruoli \_</span><span class="sxs-lookup"><span data-stu-id="cd6f6-253">ROLE\_SYSTEM\_CHART</span></span>

<span data-ttu-id="cd6f6-254">Per ulteriori informazioni su questo ruolo, vedere [**il \_ \_ grafico del sistema dei ruoli**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="cd6f6-254">For more information on this role, see [**ROLE\_SYSTEM\_CHART**](object-roles.md).</span></span>

<span data-ttu-id="cd6f6-255">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-255">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="cd6f6-256">accHitTest</span><span class="sxs-lookup"><span data-stu-id="cd6f6-256">accHitTest</span></span>
-   <span data-ttu-id="cd6f6-257">accLocation</span><span class="sxs-lookup"><span data-stu-id="cd6f6-257">accLocation</span></span>
-   <span data-ttu-id="cd6f6-258">accNavigate</span><span class="sxs-lookup"><span data-stu-id="cd6f6-258">accNavigate</span></span>
-   <span data-ttu-id="cd6f6-259">ottenere \_ accChild</span><span class="sxs-lookup"><span data-stu-id="cd6f6-259">get\_accChild</span></span>
-   <span data-ttu-id="cd6f6-260">ottenere \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="cd6f6-260">get\_accChildCount</span></span>
-   <span data-ttu-id="cd6f6-261">ottenere \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="cd6f6-261">get\_accFocus</span></span>
-   <span data-ttu-id="cd6f6-262">ottenere \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="cd6f6-262">get\_accHelp</span></span>
-   <span data-ttu-id="cd6f6-263">ottenere \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="cd6f6-263">get\_accHelpTopic</span></span>
-   <span data-ttu-id="cd6f6-264">ottenere \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="cd6f6-264">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="cd6f6-265">ottenere \_ accName</span><span class="sxs-lookup"><span data-stu-id="cd6f6-265">get\_accName</span></span>
-   <span data-ttu-id="cd6f6-266">ottenere \_ accParent</span><span class="sxs-lookup"><span data-stu-id="cd6f6-266">get\_accParent</span></span>
-   <span data-ttu-id="cd6f6-267">ottenere \_ accRole</span><span class="sxs-lookup"><span data-stu-id="cd6f6-267">get\_accRole</span></span>
-   <span data-ttu-id="cd6f6-268">ottenere \_ accState</span><span class="sxs-lookup"><span data-stu-id="cd6f6-268">get\_accState</span></span>

## <a name="role_system_clock"></a><span data-ttu-id="cd6f6-269">\_clock di sistema del ruolo \_</span><span class="sxs-lookup"><span data-stu-id="cd6f6-269">ROLE\_SYSTEM\_CLOCK</span></span>

<span data-ttu-id="cd6f6-270">Per altre informazioni su questo ruolo, vedere [**\_ \_ clock di sistema del ruolo**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="cd6f6-270">For more information on this role, see [**ROLE\_SYSTEM\_CLOCK**](object-roles.md).</span></span>

<span data-ttu-id="cd6f6-271">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-271">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="cd6f6-272">accHitTest</span><span class="sxs-lookup"><span data-stu-id="cd6f6-272">accHitTest</span></span>
-   <span data-ttu-id="cd6f6-273">accLocation</span><span class="sxs-lookup"><span data-stu-id="cd6f6-273">accLocation</span></span>
-   <span data-ttu-id="cd6f6-274">accNavigate</span><span class="sxs-lookup"><span data-stu-id="cd6f6-274">accNavigate</span></span>
-   <span data-ttu-id="cd6f6-275">ottenere \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="cd6f6-275">get\_accFocus</span></span>
-   <span data-ttu-id="cd6f6-276">ottenere \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="cd6f6-276">get\_accHelp</span></span>
-   <span data-ttu-id="cd6f6-277">ottenere \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="cd6f6-277">get\_accHelpTopic</span></span>
-   <span data-ttu-id="cd6f6-278">ottenere \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="cd6f6-278">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="cd6f6-279">ottenere \_ accName</span><span class="sxs-lookup"><span data-stu-id="cd6f6-279">get\_accName</span></span>
-   <span data-ttu-id="cd6f6-280">ottenere \_ accParent</span><span class="sxs-lookup"><span data-stu-id="cd6f6-280">get\_accParent</span></span>
-   <span data-ttu-id="cd6f6-281">ottenere \_ accRole</span><span class="sxs-lookup"><span data-stu-id="cd6f6-281">get\_accRole</span></span>
-   <span data-ttu-id="cd6f6-282">ottenere \_ accState</span><span class="sxs-lookup"><span data-stu-id="cd6f6-282">get\_accState</span></span>
-   <span data-ttu-id="cd6f6-283">ottenere \_ accValue</span><span class="sxs-lookup"><span data-stu-id="cd6f6-283">get\_accValue</span></span>

## <a name="role_system_column"></a><span data-ttu-id="cd6f6-284">\_colonna di sistema del ruolo \_</span><span class="sxs-lookup"><span data-stu-id="cd6f6-284">ROLE\_SYSTEM\_COLUMN</span></span>

<span data-ttu-id="cd6f6-285">Per ulteriori informazioni su questo ruolo, vedere [**\_ \_ colonna di sistema del ruolo**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="cd6f6-285">For more information on this role, see [**ROLE\_SYSTEM\_COLUMN**](object-roles.md).</span></span>

<span data-ttu-id="cd6f6-286">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-286">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="cd6f6-287">accHitTest</span><span class="sxs-lookup"><span data-stu-id="cd6f6-287">accHitTest</span></span>
-   <span data-ttu-id="cd6f6-288">accLocation</span><span class="sxs-lookup"><span data-stu-id="cd6f6-288">accLocation</span></span>
-   <span data-ttu-id="cd6f6-289">accNavigate</span><span class="sxs-lookup"><span data-stu-id="cd6f6-289">accNavigate</span></span>
-   <span data-ttu-id="cd6f6-290">accSelect</span><span class="sxs-lookup"><span data-stu-id="cd6f6-290">accSelect</span></span>
-   <span data-ttu-id="cd6f6-291">ottenere \_ accChild</span><span class="sxs-lookup"><span data-stu-id="cd6f6-291">get\_accChild</span></span>
-   <span data-ttu-id="cd6f6-292">ottenere \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="cd6f6-292">get\_accChildCount</span></span>
-   <span data-ttu-id="cd6f6-293">ottenere \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="cd6f6-293">get\_accFocus</span></span>
-   <span data-ttu-id="cd6f6-294">ottenere \_ accName</span><span class="sxs-lookup"><span data-stu-id="cd6f6-294">get\_accName</span></span>
-   <span data-ttu-id="cd6f6-295">ottenere \_ accParent</span><span class="sxs-lookup"><span data-stu-id="cd6f6-295">get\_accParent</span></span>
-   <span data-ttu-id="cd6f6-296">ottenere \_ accRole</span><span class="sxs-lookup"><span data-stu-id="cd6f6-296">get\_accRole</span></span>
-   <span data-ttu-id="cd6f6-297">ottenere \_ accState</span><span class="sxs-lookup"><span data-stu-id="cd6f6-297">get\_accState</span></span>
-   <span data-ttu-id="cd6f6-298">ottenere \_ accValue</span><span class="sxs-lookup"><span data-stu-id="cd6f6-298">get\_accValue</span></span>

## <a name="role_system_diagram"></a><span data-ttu-id="cd6f6-299">\_diagramma del sistema di ruoli \_</span><span class="sxs-lookup"><span data-stu-id="cd6f6-299">ROLE\_SYSTEM\_DIAGRAM</span></span>

<span data-ttu-id="cd6f6-300">Per altre informazioni su questo ruolo, vedere [**\_ \_ diagramma di sistema dei ruoli**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="cd6f6-300">For more information on this role, see [**ROLE\_SYSTEM\_DIAGRAM**](object-roles.md).</span></span>

<span data-ttu-id="cd6f6-301">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-301">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="cd6f6-302">accHitTest</span><span class="sxs-lookup"><span data-stu-id="cd6f6-302">accHitTest</span></span>
-   <span data-ttu-id="cd6f6-303">accLocation</span><span class="sxs-lookup"><span data-stu-id="cd6f6-303">accLocation</span></span>
-   <span data-ttu-id="cd6f6-304">accNavigate</span><span class="sxs-lookup"><span data-stu-id="cd6f6-304">accNavigate</span></span>
-   <span data-ttu-id="cd6f6-305">ottenere \_ accChild</span><span class="sxs-lookup"><span data-stu-id="cd6f6-305">get\_accChild</span></span>
-   <span data-ttu-id="cd6f6-306">ottenere \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="cd6f6-306">get\_accChildCount</span></span>
-   <span data-ttu-id="cd6f6-307">ottenere \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="cd6f6-307">get\_accFocus</span></span>
-   <span data-ttu-id="cd6f6-308">ottenere \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="cd6f6-308">get\_accHelp</span></span>
-   <span data-ttu-id="cd6f6-309">ottenere \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="cd6f6-309">get\_accHelpTopic</span></span>
-   <span data-ttu-id="cd6f6-310">ottenere \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="cd6f6-310">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="cd6f6-311">ottenere \_ accName</span><span class="sxs-lookup"><span data-stu-id="cd6f6-311">get\_accName</span></span>
-   <span data-ttu-id="cd6f6-312">ottenere \_ accParent</span><span class="sxs-lookup"><span data-stu-id="cd6f6-312">get\_accParent</span></span>
-   <span data-ttu-id="cd6f6-313">ottenere \_ accRole</span><span class="sxs-lookup"><span data-stu-id="cd6f6-313">get\_accRole</span></span>
-   <span data-ttu-id="cd6f6-314">ottenere \_ accState</span><span class="sxs-lookup"><span data-stu-id="cd6f6-314">get\_accState</span></span>

## <a name="role_system_dial"></a><span data-ttu-id="cd6f6-315">\_Composizione sistema \_ ruolo</span><span class="sxs-lookup"><span data-stu-id="cd6f6-315">ROLE\_SYSTEM\_DIAL</span></span>

<span data-ttu-id="cd6f6-316">Per ulteriori informazioni su questo ruolo, vedere la pagina relativa alla [**\_ \_ composizione del sistema di ruoli**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="cd6f6-316">For more information on this role, see [**ROLE\_SYSTEM\_DIAL**](object-roles.md).</span></span>

<span data-ttu-id="cd6f6-317">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-317">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="cd6f6-318">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="cd6f6-318">accDoDefaultAction</span></span>
-   <span data-ttu-id="cd6f6-319">accHitTest</span><span class="sxs-lookup"><span data-stu-id="cd6f6-319">accHitTest</span></span>
-   <span data-ttu-id="cd6f6-320">accLocation</span><span class="sxs-lookup"><span data-stu-id="cd6f6-320">accLocation</span></span>
-   <span data-ttu-id="cd6f6-321">accNavigate</span><span class="sxs-lookup"><span data-stu-id="cd6f6-321">accNavigate</span></span>
-   <span data-ttu-id="cd6f6-322">ottenere \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="cd6f6-322">get\_accDefaultAction</span></span>
-   <span data-ttu-id="cd6f6-323">ottenere \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="cd6f6-323">get\_accFocus</span></span>
-   <span data-ttu-id="cd6f6-324">ottenere \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="cd6f6-324">get\_accHelp</span></span>
-   <span data-ttu-id="cd6f6-325">ottenere \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="cd6f6-325">get\_accHelpTopic</span></span>
-   <span data-ttu-id="cd6f6-326">ottenere \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="cd6f6-326">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="cd6f6-327">ottenere \_ accName</span><span class="sxs-lookup"><span data-stu-id="cd6f6-327">get\_accName</span></span>
-   <span data-ttu-id="cd6f6-328">ottenere \_ accParent</span><span class="sxs-lookup"><span data-stu-id="cd6f6-328">get\_accParent</span></span>
-   <span data-ttu-id="cd6f6-329">ottenere \_ accRole</span><span class="sxs-lookup"><span data-stu-id="cd6f6-329">get\_accRole</span></span>
-   <span data-ttu-id="cd6f6-330">ottenere \_ accState</span><span class="sxs-lookup"><span data-stu-id="cd6f6-330">get\_accState</span></span>
-   <span data-ttu-id="cd6f6-331">ottenere \_ accValue</span><span class="sxs-lookup"><span data-stu-id="cd6f6-331">get\_accValue</span></span>

## <a name="role_system_document"></a><span data-ttu-id="cd6f6-332">\_documento di sistema del ruolo \_</span><span class="sxs-lookup"><span data-stu-id="cd6f6-332">ROLE\_SYSTEM\_DOCUMENT</span></span>

<span data-ttu-id="cd6f6-333">Per ulteriori informazioni su questo ruolo, vedere [**il \_ \_ documento di sistema dei ruoli**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="cd6f6-333">For more information on this role, see [**ROLE\_SYSTEM\_DOCUMENT**](object-roles.md).</span></span>

<span data-ttu-id="cd6f6-334">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-334">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="cd6f6-335">accHitTest</span><span class="sxs-lookup"><span data-stu-id="cd6f6-335">accHitTest</span></span>
-   <span data-ttu-id="cd6f6-336">accLocation</span><span class="sxs-lookup"><span data-stu-id="cd6f6-336">accLocation</span></span>
-   <span data-ttu-id="cd6f6-337">accNavigate</span><span class="sxs-lookup"><span data-stu-id="cd6f6-337">accNavigate</span></span>
-   <span data-ttu-id="cd6f6-338">accSelect</span><span class="sxs-lookup"><span data-stu-id="cd6f6-338">accSelect</span></span>
-   <span data-ttu-id="cd6f6-339">ottenere \_ accChild</span><span class="sxs-lookup"><span data-stu-id="cd6f6-339">get\_accChild</span></span>
-   <span data-ttu-id="cd6f6-340">ottenere \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="cd6f6-340">get\_accChildCount</span></span>
-   <span data-ttu-id="cd6f6-341">ottenere \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="cd6f6-341">get\_accFocus</span></span>
-   <span data-ttu-id="cd6f6-342">ottenere \_ accName</span><span class="sxs-lookup"><span data-stu-id="cd6f6-342">get\_accName</span></span>
-   <span data-ttu-id="cd6f6-343">ottenere \_ accParent</span><span class="sxs-lookup"><span data-stu-id="cd6f6-343">get\_accParent</span></span>
-   <span data-ttu-id="cd6f6-344">ottenere \_ accRole</span><span class="sxs-lookup"><span data-stu-id="cd6f6-344">get\_accRole</span></span>
-   <span data-ttu-id="cd6f6-345">ottenere \_ accState</span><span class="sxs-lookup"><span data-stu-id="cd6f6-345">get\_accState</span></span>

## <a name="role_system_droplist"></a><span data-ttu-id="cd6f6-346">\_elenco a \_ selezione sistema ruolo</span><span class="sxs-lookup"><span data-stu-id="cd6f6-346">ROLE\_SYSTEM\_DROPLIST</span></span>

<span data-ttu-id="cd6f6-347">Per ulteriori informazioni su questo ruolo, vedere la pagina relativa all' [**\_ \_ elenco**](object-roles.md)a discapito di sistema dei ruoli.</span><span class="sxs-lookup"><span data-stu-id="cd6f6-347">For more information on this role, see [**ROLE\_SYSTEM\_DROPLIST**](object-roles.md).</span></span>

<span data-ttu-id="cd6f6-348">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-348">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="cd6f6-349">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="cd6f6-349">accDoDefaultAction</span></span>
-   <span data-ttu-id="cd6f6-350">accHitTest</span><span class="sxs-lookup"><span data-stu-id="cd6f6-350">accHitTest</span></span>
-   <span data-ttu-id="cd6f6-351">accLocation</span><span class="sxs-lookup"><span data-stu-id="cd6f6-351">accLocation</span></span>
-   <span data-ttu-id="cd6f6-352">accNavigate</span><span class="sxs-lookup"><span data-stu-id="cd6f6-352">accNavigate</span></span>
-   <span data-ttu-id="cd6f6-353">ottenere \_ accChild</span><span class="sxs-lookup"><span data-stu-id="cd6f6-353">get\_accChild</span></span>
-   <span data-ttu-id="cd6f6-354">ottenere \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="cd6f6-354">get\_accChildCount</span></span>
-   <span data-ttu-id="cd6f6-355">ottenere \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="cd6f6-355">get\_accDefaultAction</span></span>
-   <span data-ttu-id="cd6f6-356">ottenere \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="cd6f6-356">get\_accFocus</span></span>
-   <span data-ttu-id="cd6f6-357">ottenere \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="cd6f6-357">get\_accHelp</span></span>
-   <span data-ttu-id="cd6f6-358">ottenere \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="cd6f6-358">get\_accHelpTopic</span></span>
-   <span data-ttu-id="cd6f6-359">ottenere \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="cd6f6-359">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="cd6f6-360">ottenere \_ accName</span><span class="sxs-lookup"><span data-stu-id="cd6f6-360">get\_accName</span></span>
-   <span data-ttu-id="cd6f6-361">ottenere \_ accParent</span><span class="sxs-lookup"><span data-stu-id="cd6f6-361">get\_accParent</span></span>
-   <span data-ttu-id="cd6f6-362">ottenere \_ accRole</span><span class="sxs-lookup"><span data-stu-id="cd6f6-362">get\_accRole</span></span>
-   <span data-ttu-id="cd6f6-363">ottenere \_ accState</span><span class="sxs-lookup"><span data-stu-id="cd6f6-363">get\_accState</span></span>

## <a name="role_system_equation"></a><span data-ttu-id="cd6f6-364">\_equazione del sistema di ruolo \_</span><span class="sxs-lookup"><span data-stu-id="cd6f6-364">ROLE\_SYSTEM\_EQUATION</span></span>

<span data-ttu-id="cd6f6-365">Per altre informazioni su questo ruolo, vedere [**\_ \_ equazione del sistema di ruolo**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="cd6f6-365">For more information on this role, see [**ROLE\_SYSTEM\_EQUATION**](object-roles.md).</span></span>

<span data-ttu-id="cd6f6-366">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-366">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="cd6f6-367">accHitTest</span><span class="sxs-lookup"><span data-stu-id="cd6f6-367">accHitTest</span></span>
-   <span data-ttu-id="cd6f6-368">accLocation</span><span class="sxs-lookup"><span data-stu-id="cd6f6-368">accLocation</span></span>
-   <span data-ttu-id="cd6f6-369">accNavigate</span><span class="sxs-lookup"><span data-stu-id="cd6f6-369">accNavigate</span></span>
-   <span data-ttu-id="cd6f6-370">ottenere \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="cd6f6-370">get\_accFocus</span></span>
-   <span data-ttu-id="cd6f6-371">ottenere \_ accName</span><span class="sxs-lookup"><span data-stu-id="cd6f6-371">get\_accName</span></span>
-   <span data-ttu-id="cd6f6-372">ottenere \_ accParent</span><span class="sxs-lookup"><span data-stu-id="cd6f6-372">get\_accParent</span></span>
-   <span data-ttu-id="cd6f6-373">ottenere \_ accRole</span><span class="sxs-lookup"><span data-stu-id="cd6f6-373">get\_accRole</span></span>
-   <span data-ttu-id="cd6f6-374">ottenere \_ accState</span><span class="sxs-lookup"><span data-stu-id="cd6f6-374">get\_accState</span></span>
-   <span data-ttu-id="cd6f6-375">ottenere \_ accValue</span><span class="sxs-lookup"><span data-stu-id="cd6f6-375">get\_accValue</span></span>

## <a name="role_system_graphic"></a><span data-ttu-id="cd6f6-376">\_rappresentazione grafica del sistema di ruoli \_</span><span class="sxs-lookup"><span data-stu-id="cd6f6-376">ROLE\_SYSTEM\_GRAPHIC</span></span>

<span data-ttu-id="cd6f6-377">Per altre informazioni su questo ruolo, vedere [**\_ \_ Graphic System Role**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="cd6f6-377">For more information on this role, see [**ROLE\_SYSTEM\_GRAPHIC**](object-roles.md).</span></span>

<span data-ttu-id="cd6f6-378">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-378">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="cd6f6-379">accHitTest</span><span class="sxs-lookup"><span data-stu-id="cd6f6-379">accHitTest</span></span>
-   <span data-ttu-id="cd6f6-380">accLocation</span><span class="sxs-lookup"><span data-stu-id="cd6f6-380">accLocation</span></span>
-   <span data-ttu-id="cd6f6-381">accNavigate</span><span class="sxs-lookup"><span data-stu-id="cd6f6-381">accNavigate</span></span>
-   <span data-ttu-id="cd6f6-382">ottenere \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="cd6f6-382">get\_accFocus</span></span>
-   <span data-ttu-id="cd6f6-383">ottenere \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="cd6f6-383">get\_accHelp</span></span>
-   <span data-ttu-id="cd6f6-384">ottenere \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="cd6f6-384">get\_accHelpTopic</span></span>
-   <span data-ttu-id="cd6f6-385">ottenere \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="cd6f6-385">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="cd6f6-386">ottenere \_ accName</span><span class="sxs-lookup"><span data-stu-id="cd6f6-386">get\_accName</span></span>
-   <span data-ttu-id="cd6f6-387">ottenere \_ accParent</span><span class="sxs-lookup"><span data-stu-id="cd6f6-387">get\_accParent</span></span>
-   <span data-ttu-id="cd6f6-388">ottenere \_ accRole</span><span class="sxs-lookup"><span data-stu-id="cd6f6-388">get\_accRole</span></span>
-   <span data-ttu-id="cd6f6-389">ottenere \_ accState</span><span class="sxs-lookup"><span data-stu-id="cd6f6-389">get\_accState</span></span>

## <a name="role_system_helpballoon"></a><span data-ttu-id="cd6f6-390">\_HELPBALLOON di sistema ruolo \_</span><span class="sxs-lookup"><span data-stu-id="cd6f6-390">ROLE\_SYSTEM\_HELPBALLOON</span></span>

<span data-ttu-id="cd6f6-391">Per ulteriori informazioni su questo ruolo, vedere [**ruolo del \_ sistema \_ HELPBALLOON**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="cd6f6-391">For more information on this role, see [**ROLE\_SYSTEM\_HELPBALLOON**](object-roles.md).</span></span>

<span data-ttu-id="cd6f6-392">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-392">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="cd6f6-393">accHitTest</span><span class="sxs-lookup"><span data-stu-id="cd6f6-393">accHitTest</span></span>
-   <span data-ttu-id="cd6f6-394">accLocation</span><span class="sxs-lookup"><span data-stu-id="cd6f6-394">accLocation</span></span>
-   <span data-ttu-id="cd6f6-395">accNavigate</span><span class="sxs-lookup"><span data-stu-id="cd6f6-395">accNavigate</span></span>
-   <span data-ttu-id="cd6f6-396">ottenere \_ accChild</span><span class="sxs-lookup"><span data-stu-id="cd6f6-396">get\_accChild</span></span>
-   <span data-ttu-id="cd6f6-397">ottenere \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="cd6f6-397">get\_accChildCount</span></span>
-   <span data-ttu-id="cd6f6-398">ottenere \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="cd6f6-398">get\_accDefaultAction</span></span>
-   <span data-ttu-id="cd6f6-399">ottenere \_ accName</span><span class="sxs-lookup"><span data-stu-id="cd6f6-399">get\_accName</span></span>
-   <span data-ttu-id="cd6f6-400">ottenere \_ accParent</span><span class="sxs-lookup"><span data-stu-id="cd6f6-400">get\_accParent</span></span>
-   <span data-ttu-id="cd6f6-401">ottenere \_ accRole</span><span class="sxs-lookup"><span data-stu-id="cd6f6-401">get\_accRole</span></span>
-   <span data-ttu-id="cd6f6-402">ottenere \_ accState</span><span class="sxs-lookup"><span data-stu-id="cd6f6-402">get\_accState</span></span>
-   <span data-ttu-id="cd6f6-403">ottenere \_ accValue</span><span class="sxs-lookup"><span data-stu-id="cd6f6-403">get\_accValue</span></span>

## <a name="role_system_ipaddress"></a><span data-ttu-id="cd6f6-404">\_IPAddress sistema \_ ruolo</span><span class="sxs-lookup"><span data-stu-id="cd6f6-404">ROLE\_SYSTEM\_IPADDRESS</span></span>

<span data-ttu-id="cd6f6-405">Per ulteriori informazioni su questo ruolo, vedere [**Role \_ System \_ IPAddress**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="cd6f6-405">For more information on this role, see [**ROLE\_SYSTEM\_IPADDRESS**](object-roles.md).</span></span>

<span data-ttu-id="cd6f6-406">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-406">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="cd6f6-407">accHitTest</span><span class="sxs-lookup"><span data-stu-id="cd6f6-407">accHitTest</span></span>
-   <span data-ttu-id="cd6f6-408">accLocation</span><span class="sxs-lookup"><span data-stu-id="cd6f6-408">accLocation</span></span>
-   <span data-ttu-id="cd6f6-409">accNavigate</span><span class="sxs-lookup"><span data-stu-id="cd6f6-409">accNavigate</span></span>
-   <span data-ttu-id="cd6f6-410">ottenere \_ accChild</span><span class="sxs-lookup"><span data-stu-id="cd6f6-410">get\_accChild</span></span>
-   <span data-ttu-id="cd6f6-411">ottenere \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="cd6f6-411">get\_accChildCount</span></span>
-   <span data-ttu-id="cd6f6-412">ottenere \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="cd6f6-412">get\_accFocus</span></span>
-   <span data-ttu-id="cd6f6-413">ottenere \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="cd6f6-413">get\_accHelp</span></span>
-   <span data-ttu-id="cd6f6-414">ottenere \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="cd6f6-414">get\_accHelpTopic</span></span>
-   <span data-ttu-id="cd6f6-415">ottenere \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="cd6f6-415">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="cd6f6-416">ottenere \_ accName</span><span class="sxs-lookup"><span data-stu-id="cd6f6-416">get\_accName</span></span>
-   <span data-ttu-id="cd6f6-417">ottenere \_ accParent</span><span class="sxs-lookup"><span data-stu-id="cd6f6-417">get\_accParent</span></span>
-   <span data-ttu-id="cd6f6-418">ottenere \_ accRole</span><span class="sxs-lookup"><span data-stu-id="cd6f6-418">get\_accRole</span></span>
-   <span data-ttu-id="cd6f6-419">ottenere \_ accState</span><span class="sxs-lookup"><span data-stu-id="cd6f6-419">get\_accState</span></span>
-   <span data-ttu-id="cd6f6-420">ottenere \_ accValue</span><span class="sxs-lookup"><span data-stu-id="cd6f6-420">get\_accValue</span></span>

## <a name="role_system_link"></a><span data-ttu-id="cd6f6-421">\_collegamento del sistema ruolo \_</span><span class="sxs-lookup"><span data-stu-id="cd6f6-421">ROLE\_SYSTEM\_LINK</span></span>

<span data-ttu-id="cd6f6-422">Per ulteriori informazioni su questo ruolo, vedere [**\_ \_ collegamento del sistema di ruolo**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="cd6f6-422">For more information on this role, see [**ROLE\_SYSTEM\_LINK**](object-roles.md).</span></span>

<span data-ttu-id="cd6f6-423">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-423">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="cd6f6-424">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="cd6f6-424">accDoDefaultAction</span></span>
-   <span data-ttu-id="cd6f6-425">accHitTest</span><span class="sxs-lookup"><span data-stu-id="cd6f6-425">accHitTest</span></span>
-   <span data-ttu-id="cd6f6-426">accLocation</span><span class="sxs-lookup"><span data-stu-id="cd6f6-426">accLocation</span></span>
-   <span data-ttu-id="cd6f6-427">accNavigate</span><span class="sxs-lookup"><span data-stu-id="cd6f6-427">accNavigate</span></span>
-   <span data-ttu-id="cd6f6-428">ottenere \_ accChild</span><span class="sxs-lookup"><span data-stu-id="cd6f6-428">get\_accChild</span></span>
-   <span data-ttu-id="cd6f6-429">ottenere \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="cd6f6-429">get\_accChildCount</span></span>
-   <span data-ttu-id="cd6f6-430">ottenere \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="cd6f6-430">get\_accDefaultAction</span></span>
-   <span data-ttu-id="cd6f6-431">ottenere \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="cd6f6-431">get\_accDescription</span></span>
-   <span data-ttu-id="cd6f6-432">ottenere \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="cd6f6-432">get\_accFocus</span></span>
-   <span data-ttu-id="cd6f6-433">ottenere \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="cd6f6-433">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="cd6f6-434">ottenere \_ accName</span><span class="sxs-lookup"><span data-stu-id="cd6f6-434">get\_accName</span></span>
-   <span data-ttu-id="cd6f6-435">ottenere \_ accParent</span><span class="sxs-lookup"><span data-stu-id="cd6f6-435">get\_accParent</span></span>
-   <span data-ttu-id="cd6f6-436">ottenere \_ accRole</span><span class="sxs-lookup"><span data-stu-id="cd6f6-436">get\_accRole</span></span>
-   <span data-ttu-id="cd6f6-437">ottenere \_ accState</span><span class="sxs-lookup"><span data-stu-id="cd6f6-437">get\_accState</span></span>
-   <span data-ttu-id="cd6f6-438">ottenere \_ accValue</span><span class="sxs-lookup"><span data-stu-id="cd6f6-438">get\_accValue</span></span>

## <a name="role_system_pane"></a><span data-ttu-id="cd6f6-439">\_riquadro sistema \_ ruoli</span><span class="sxs-lookup"><span data-stu-id="cd6f6-439">ROLE\_SYSTEM\_PANE</span></span>

<span data-ttu-id="cd6f6-440">Per ulteriori informazioni su questo ruolo, vedere [**\_ \_ riquadro sistema ruoli**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="cd6f6-440">For more information on this role, see [**ROLE\_SYSTEM\_PANE**](object-roles.md).</span></span>

<span data-ttu-id="cd6f6-441">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-441">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="cd6f6-442">accHitTest</span><span class="sxs-lookup"><span data-stu-id="cd6f6-442">accHitTest</span></span>
-   <span data-ttu-id="cd6f6-443">accLocation</span><span class="sxs-lookup"><span data-stu-id="cd6f6-443">accLocation</span></span>
-   <span data-ttu-id="cd6f6-444">accNavigate</span><span class="sxs-lookup"><span data-stu-id="cd6f6-444">accNavigate</span></span>
-   <span data-ttu-id="cd6f6-445">ottenere \_ accChild</span><span class="sxs-lookup"><span data-stu-id="cd6f6-445">get\_accChild</span></span>
-   <span data-ttu-id="cd6f6-446">ottenere \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="cd6f6-446">get\_accChildCount</span></span>
-   <span data-ttu-id="cd6f6-447">ottenere \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="cd6f6-447">get\_accFocus</span></span>
-   <span data-ttu-id="cd6f6-448">ottenere \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="cd6f6-448">get\_accHelp</span></span>
-   <span data-ttu-id="cd6f6-449">ottenere \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="cd6f6-449">get\_accHelpTopic</span></span>
-   <span data-ttu-id="cd6f6-450">ottenere \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="cd6f6-450">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="cd6f6-451">ottenere \_ accName</span><span class="sxs-lookup"><span data-stu-id="cd6f6-451">get\_accName</span></span>
-   <span data-ttu-id="cd6f6-452">ottenere \_ accParent</span><span class="sxs-lookup"><span data-stu-id="cd6f6-452">get\_accParent</span></span>
-   <span data-ttu-id="cd6f6-453">ottenere \_ accRole</span><span class="sxs-lookup"><span data-stu-id="cd6f6-453">get\_accRole</span></span>
-   <span data-ttu-id="cd6f6-454">ottenere \_ accState</span><span class="sxs-lookup"><span data-stu-id="cd6f6-454">get\_accState</span></span>

## <a name="role_system_row"></a><span data-ttu-id="cd6f6-455">\_riga sistema \_ ruolo</span><span class="sxs-lookup"><span data-stu-id="cd6f6-455">ROLE\_SYSTEM\_ROW</span></span>

<span data-ttu-id="cd6f6-456">Per ulteriori informazioni su questo ruolo, vedere [**\_ \_ riga di sistema del ruolo**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="cd6f6-456">For more information on this role, see [**ROLE\_SYSTEM\_ROW**](object-roles.md).</span></span>

<span data-ttu-id="cd6f6-457">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-457">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="cd6f6-458">accHitTest</span><span class="sxs-lookup"><span data-stu-id="cd6f6-458">accHitTest</span></span>
-   <span data-ttu-id="cd6f6-459">accLocation</span><span class="sxs-lookup"><span data-stu-id="cd6f6-459">accLocation</span></span>
-   <span data-ttu-id="cd6f6-460">accNavigate</span><span class="sxs-lookup"><span data-stu-id="cd6f6-460">accNavigate</span></span>
-   <span data-ttu-id="cd6f6-461">accSelect</span><span class="sxs-lookup"><span data-stu-id="cd6f6-461">accSelect</span></span>
-   <span data-ttu-id="cd6f6-462">ottenere \_ accChild</span><span class="sxs-lookup"><span data-stu-id="cd6f6-462">get\_accChild</span></span>
-   <span data-ttu-id="cd6f6-463">ottenere \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="cd6f6-463">get\_accChildCount</span></span>
-   <span data-ttu-id="cd6f6-464">ottenere \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="cd6f6-464">get\_accDescription</span></span>
-   <span data-ttu-id="cd6f6-465">ottenere \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="cd6f6-465">get\_accFocus</span></span>
-   <span data-ttu-id="cd6f6-466">ottenere \_ accName</span><span class="sxs-lookup"><span data-stu-id="cd6f6-466">get\_accName</span></span>
-   <span data-ttu-id="cd6f6-467">ottenere \_ accParent</span><span class="sxs-lookup"><span data-stu-id="cd6f6-467">get\_accParent</span></span>
-   <span data-ttu-id="cd6f6-468">ottenere \_ accRole</span><span class="sxs-lookup"><span data-stu-id="cd6f6-468">get\_accRole</span></span>
-   <span data-ttu-id="cd6f6-469">ottenere \_ accState</span><span class="sxs-lookup"><span data-stu-id="cd6f6-469">get\_accState</span></span>
-   <span data-ttu-id="cd6f6-470">ottenere \_ accValue</span><span class="sxs-lookup"><span data-stu-id="cd6f6-470">get\_accValue</span></span>

## <a name="role_system_rowheader"></a><span data-ttu-id="cd6f6-471">\_ROWHEADER di sistema ruolo \_</span><span class="sxs-lookup"><span data-stu-id="cd6f6-471">ROLE\_SYSTEM\_ROWHEADER</span></span>

<span data-ttu-id="cd6f6-472">Per ulteriori informazioni su questo ruolo, vedere [**ruolo del \_ sistema \_ ROWHEADER**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="cd6f6-472">For more information on this role, see [**ROLE\_SYSTEM\_ROWHEADER**](object-roles.md).</span></span>

<span data-ttu-id="cd6f6-473">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-473">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="cd6f6-474">accHitTest</span><span class="sxs-lookup"><span data-stu-id="cd6f6-474">accHitTest</span></span>
-   <span data-ttu-id="cd6f6-475">accLocation</span><span class="sxs-lookup"><span data-stu-id="cd6f6-475">accLocation</span></span>
-   <span data-ttu-id="cd6f6-476">accNavigate</span><span class="sxs-lookup"><span data-stu-id="cd6f6-476">accNavigate</span></span>
-   <span data-ttu-id="cd6f6-477">accSelect</span><span class="sxs-lookup"><span data-stu-id="cd6f6-477">accSelect</span></span>
-   <span data-ttu-id="cd6f6-478">ottenere \_ accChild</span><span class="sxs-lookup"><span data-stu-id="cd6f6-478">get\_accChild</span></span>
-   <span data-ttu-id="cd6f6-479">ottenere \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="cd6f6-479">get\_accChildCount</span></span>
-   <span data-ttu-id="cd6f6-480">ottenere \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="cd6f6-480">get\_accDefaultAction</span></span>
-   <span data-ttu-id="cd6f6-481">ottenere \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="cd6f6-481">get\_accDescription</span></span>
-   <span data-ttu-id="cd6f6-482">ottenere \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="cd6f6-482">get\_accFocus</span></span>
-   <span data-ttu-id="cd6f6-483">ottenere \_ accName</span><span class="sxs-lookup"><span data-stu-id="cd6f6-483">get\_accName</span></span>
-   <span data-ttu-id="cd6f6-484">ottenere \_ accParent</span><span class="sxs-lookup"><span data-stu-id="cd6f6-484">get\_accParent</span></span>
-   <span data-ttu-id="cd6f6-485">ottenere \_ accRole</span><span class="sxs-lookup"><span data-stu-id="cd6f6-485">get\_accRole</span></span>
-   <span data-ttu-id="cd6f6-486">ottenere \_ accState</span><span class="sxs-lookup"><span data-stu-id="cd6f6-486">get\_accState</span></span>
-   <span data-ttu-id="cd6f6-487">ottenere \_ accValue</span><span class="sxs-lookup"><span data-stu-id="cd6f6-487">get\_accValue</span></span>

## <a name="role_system_separator"></a><span data-ttu-id="cd6f6-488">\_separatore di sistema ruolo \_</span><span class="sxs-lookup"><span data-stu-id="cd6f6-488">ROLE\_SYSTEM\_SEPARATOR</span></span>

<span data-ttu-id="cd6f6-489">Per ulteriori informazioni su questo ruolo, vedere [**\_ \_ separatore di sistema dei ruoli**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="cd6f6-489">For more information on this role, see [**ROLE\_SYSTEM\_SEPARATOR**](object-roles.md).</span></span>

<span data-ttu-id="cd6f6-490">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-490">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="cd6f6-491">accHitTest</span><span class="sxs-lookup"><span data-stu-id="cd6f6-491">accHitTest</span></span>
-   <span data-ttu-id="cd6f6-492">accLocation</span><span class="sxs-lookup"><span data-stu-id="cd6f6-492">accLocation</span></span>
-   <span data-ttu-id="cd6f6-493">ottenere \_ accChild</span><span class="sxs-lookup"><span data-stu-id="cd6f6-493">get\_accChild</span></span>
-   <span data-ttu-id="cd6f6-494">ottenere \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="cd6f6-494">get\_accChildCount</span></span>
-   <span data-ttu-id="cd6f6-495">ottenere \_ accParent</span><span class="sxs-lookup"><span data-stu-id="cd6f6-495">get\_accParent</span></span>
-   <span data-ttu-id="cd6f6-496">ottenere \_ accRole</span><span class="sxs-lookup"><span data-stu-id="cd6f6-496">get\_accRole</span></span>
-   <span data-ttu-id="cd6f6-497">ottenere \_ accState</span><span class="sxs-lookup"><span data-stu-id="cd6f6-497">get\_accState</span></span>

## <a name="role_system_sound"></a><span data-ttu-id="cd6f6-498">\_suono del sistema di ruolo \_</span><span class="sxs-lookup"><span data-stu-id="cd6f6-498">ROLE\_SYSTEM\_SOUND</span></span>

<span data-ttu-id="cd6f6-499">Per altre informazioni su questo ruolo, vedere [**\_ \_ suono del sistema di ruolo**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="cd6f6-499">For more information on this role, see [**ROLE\_SYSTEM\_SOUND**](object-roles.md).</span></span>

<span data-ttu-id="cd6f6-500">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-500">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="cd6f6-501">ottenere \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="cd6f6-501">get\_accDescription</span></span>
-   <span data-ttu-id="cd6f6-502">ottenere \_ accName</span><span class="sxs-lookup"><span data-stu-id="cd6f6-502">get\_accName</span></span>
-   <span data-ttu-id="cd6f6-503">ottenere \_ accRole</span><span class="sxs-lookup"><span data-stu-id="cd6f6-503">get\_accRole</span></span>
-   <span data-ttu-id="cd6f6-504">ottenere \_ accState</span><span class="sxs-lookup"><span data-stu-id="cd6f6-504">get\_accState</span></span>

## <a name="role_system_splitbutton"></a><span data-ttu-id="cd6f6-505">\_SPLITBUTTON di sistema ruolo \_</span><span class="sxs-lookup"><span data-stu-id="cd6f6-505">ROLE\_SYSTEM\_SPLITBUTTON</span></span>

<span data-ttu-id="cd6f6-506">Per ulteriori informazioni su questo ruolo, vedere [**ruolo del \_ sistema \_ SPLITBUTTON**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="cd6f6-506">For more information on this role, see [**ROLE\_SYSTEM\_SPLITBUTTON**](object-roles.md).</span></span>

<span data-ttu-id="cd6f6-507">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-507">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="cd6f6-508">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="cd6f6-508">accDoDefaultAction</span></span>
-   <span data-ttu-id="cd6f6-509">accHitTest</span><span class="sxs-lookup"><span data-stu-id="cd6f6-509">accHitTest</span></span>
-   <span data-ttu-id="cd6f6-510">accLocation</span><span class="sxs-lookup"><span data-stu-id="cd6f6-510">accLocation</span></span>
-   <span data-ttu-id="cd6f6-511">accNavigate</span><span class="sxs-lookup"><span data-stu-id="cd6f6-511">accNavigate</span></span>
-   <span data-ttu-id="cd6f6-512">ottenere \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="cd6f6-512">get\_accDefaultAction</span></span>
-   <span data-ttu-id="cd6f6-513">ottenere \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="cd6f6-513">get\_accHelp</span></span>
-   <span data-ttu-id="cd6f6-514">ottenere \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="cd6f6-514">get\_accHelpTopic</span></span>
-   <span data-ttu-id="cd6f6-515">ottenere \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="cd6f6-515">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="cd6f6-516">ottenere \_ accName</span><span class="sxs-lookup"><span data-stu-id="cd6f6-516">get\_accName</span></span>
-   <span data-ttu-id="cd6f6-517">ottenere \_ accParent</span><span class="sxs-lookup"><span data-stu-id="cd6f6-517">get\_accParent</span></span>
-   <span data-ttu-id="cd6f6-518">ottenere \_ accRole</span><span class="sxs-lookup"><span data-stu-id="cd6f6-518">get\_accRole</span></span>
-   <span data-ttu-id="cd6f6-519">ottenere \_ accState</span><span class="sxs-lookup"><span data-stu-id="cd6f6-519">get\_accState</span></span>

## <a name="role_system_table"></a><span data-ttu-id="cd6f6-520">\_tabella di sistema del ruolo \_</span><span class="sxs-lookup"><span data-stu-id="cd6f6-520">ROLE\_SYSTEM\_TABLE</span></span>

<span data-ttu-id="cd6f6-521">Per altre informazioni su questo ruolo, vedere [**\_ \_ tabella di sistema dei ruoli**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="cd6f6-521">For more information on this role, see [**ROLE\_SYSTEM\_TABLE**](object-roles.md).</span></span>

<span data-ttu-id="cd6f6-522">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-522">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="cd6f6-523">accHitTest</span><span class="sxs-lookup"><span data-stu-id="cd6f6-523">accHitTest</span></span>
-   <span data-ttu-id="cd6f6-524">accLocation</span><span class="sxs-lookup"><span data-stu-id="cd6f6-524">accLocation</span></span>
-   <span data-ttu-id="cd6f6-525">accNavigate</span><span class="sxs-lookup"><span data-stu-id="cd6f6-525">accNavigate</span></span>
-   <span data-ttu-id="cd6f6-526">accSelect</span><span class="sxs-lookup"><span data-stu-id="cd6f6-526">accSelect</span></span>
-   <span data-ttu-id="cd6f6-527">ottenere \_ accChild</span><span class="sxs-lookup"><span data-stu-id="cd6f6-527">get\_accChild</span></span>
-   <span data-ttu-id="cd6f6-528">ottenere \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="cd6f6-528">get\_accChildCount</span></span>
-   <span data-ttu-id="cd6f6-529">ottenere \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="cd6f6-529">get\_accDescription</span></span>
-   <span data-ttu-id="cd6f6-530">ottenere \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="cd6f6-530">get\_accFocus</span></span>
-   <span data-ttu-id="cd6f6-531">ottenere \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="cd6f6-531">get\_accHelp</span></span>
-   <span data-ttu-id="cd6f6-532">ottenere \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="cd6f6-532">get\_accHelpTopic</span></span>
-   <span data-ttu-id="cd6f6-533">ottenere \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="cd6f6-533">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="cd6f6-534">ottenere \_ accName</span><span class="sxs-lookup"><span data-stu-id="cd6f6-534">get\_accName</span></span>
-   <span data-ttu-id="cd6f6-535">ottenere \_ accParent</span><span class="sxs-lookup"><span data-stu-id="cd6f6-535">get\_accParent</span></span>
-   <span data-ttu-id="cd6f6-536">ottenere \_ accRole</span><span class="sxs-lookup"><span data-stu-id="cd6f6-536">get\_accRole</span></span>
-   <span data-ttu-id="cd6f6-537">ottenere \_ accState</span><span class="sxs-lookup"><span data-stu-id="cd6f6-537">get\_accState</span></span>

## <a name="role_system_whitespace"></a><span data-ttu-id="cd6f6-538">\_spazio del sistema ruolo \_</span><span class="sxs-lookup"><span data-stu-id="cd6f6-538">ROLE\_SYSTEM\_WHITESPACE</span></span>

<span data-ttu-id="cd6f6-539">Per altre informazioni su questo ruolo, vedere [**\_ \_ spazio del sistema dei ruoli**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="cd6f6-539">For more information on this role, see [**ROLE\_SYSTEM\_WHITESPACE**](object-roles.md).</span></span>

<span data-ttu-id="cd6f6-540">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="cd6f6-540">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="cd6f6-541">accLocation</span><span class="sxs-lookup"><span data-stu-id="cd6f6-541">accLocation</span></span>
-   <span data-ttu-id="cd6f6-542">accSelect</span><span class="sxs-lookup"><span data-stu-id="cd6f6-542">accSelect</span></span>
-   <span data-ttu-id="cd6f6-543">ottenere \_ accParent</span><span class="sxs-lookup"><span data-stu-id="cd6f6-543">get\_accParent</span></span>
-   <span data-ttu-id="cd6f6-544">ottenere \_ accRole</span><span class="sxs-lookup"><span data-stu-id="cd6f6-544">get\_accRole</span></span>
-   <span data-ttu-id="cd6f6-545">ottenere \_ accState</span><span class="sxs-lookup"><span data-stu-id="cd6f6-545">get\_accState</span></span>

 

 