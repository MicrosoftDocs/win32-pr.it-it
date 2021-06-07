---
title: Altri ruoli oggetto e metodi supportati (riferimento agli elementi dell'interfaccia utente MSAA)
description: Questo argomento fornisce informazioni sui ruoli oggetto non inclusi negli argomenti precedenti per gli elementi dell'interfaccia utente.
ms.assetid: 0c3a3ccf-f02a-4aca-9380-a13774598a19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f17e8573142a57e0acf08980895fdae3ea6d1841
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444002"
---
# <a name="other-object-roles-and-supported-methods-msaa-ui-element-reference"></a><span data-ttu-id="91871-103">Altri ruoli oggetto e metodi supportati (riferimento agli elementi dell'interfaccia utente MSAA)</span><span class="sxs-lookup"><span data-stu-id="91871-103">Other Object Roles and Supported Methods (MSAA UI Element Reference)</span></span>

<span data-ttu-id="91871-104">Questo argomento fornisce informazioni sui ruoli oggetto non inclusi negli argomenti precedenti per gli elementi dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="91871-104">This topic provides information about object roles that are not included in the previous topics for UI elements.</span></span> <span data-ttu-id="91871-105">Ogni ruolo oggetto include un elenco dei metodi e delle proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) supportati per il ruolo oggetto.</span><span class="sxs-lookup"><span data-stu-id="91871-105">Each object role includes a list of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods and properties that are supported for the object role.</span></span> <span data-ttu-id="91871-106">Mentre altri argomenti documentano i metodi e le proprietà **IAccessible** supportati per gli elementi dell'interfaccia utente, questo argomento elenca i metodi e le proprietà che è possibile aspettarsi di essere supportati per un ruolo oggetto specifico.</span><span class="sxs-lookup"><span data-stu-id="91871-106">While other topics document supported **IAccessible** methods and properties for UI elements, this topic lists the methods and properties you can expect to be supported for a particular object role.</span></span> <span data-ttu-id="91871-107">Molti degli elementi dell'interfaccia utente che potrebbero avere uno dei ruoli elencati di seguito sono in genere visibili nei browser.</span><span class="sxs-lookup"><span data-stu-id="91871-107">Many of the UI elements which might have one of the roles listed here are typically seen in browsers.</span></span>

> [!Note]  
> <span data-ttu-id="91871-108">Usare questo argomento come linea guida.</span><span class="sxs-lookup"><span data-stu-id="91871-108">Use this topic as a guideline.</span></span> <span data-ttu-id="91871-109">È consigliabile usare gli strumenti Microsoft Active Accessibility per verificare il comportamento previsto per un singolo ruolo oggetto.</span><span class="sxs-lookup"><span data-stu-id="91871-109">We strongly suggest that you use Microsoft Active Accessibility tools to verify expected behavior for an individual object role.</span></span>

 

<span data-ttu-id="91871-110">Nella tabella seguente sono elencati altri ruoli oggetto supportati Oleacc.dll.</span><span class="sxs-lookup"><span data-stu-id="91871-110">The following table lists additional object roles which Oleacc.dll supports.</span></span>



| &nbsp; |  &nbsp; |
|-------------------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="91871-111">**AVVISO \_ DI SISTEMA DEL \_ RUOLO**</span><span class="sxs-lookup"><span data-stu-id="91871-111">**ROLE\_SYSTEM\_ALERT**</span></span>](/windows)                           | [<span data-ttu-id="91871-112">**ELENCO \_ A DISCESA DEL SISTEMA DEI \_ RUOLI**</span><span class="sxs-lookup"><span data-stu-id="91871-112">**ROLE\_SYSTEM\_DROPLIST**</span></span>](/windows)       |
| [<span data-ttu-id="91871-113">**APPLICAZIONE \_ DI SISTEMA DEL \_ RUOLO**</span><span class="sxs-lookup"><span data-stu-id="91871-113">**ROLE\_SYSTEM\_APPLICATION**</span></span>](/windows)               | [<span data-ttu-id="91871-114">**EQUAZIONE \_ DEL SISTEMA \_ DEI RUOLI**</span><span class="sxs-lookup"><span data-stu-id="91871-114">**ROLE\_SYSTEM\_EQUATION**</span></span>](/windows)       |
| [<span data-ttu-id="91871-115">**BORDO \_ DEL SISTEMA DEL \_ RUOLO**</span><span class="sxs-lookup"><span data-stu-id="91871-115">**ROLE\_SYSTEM\_BORDER**</span></span>](/windows)                         | [<span data-ttu-id="91871-116">**IMMAGINE \_ DEL SISTEMA DEI \_ RUOLI**</span><span class="sxs-lookup"><span data-stu-id="91871-116">**ROLE\_SYSTEM\_GRAPHIC**</span></span>](/windows)         |
| [<span data-ttu-id="91871-117">**PULSANTE \_ SISTEMA \_ RUOLODROPDOWN**</span><span class="sxs-lookup"><span data-stu-id="91871-117">**ROLE\_SYSTEM\_BUTTONDROPDOWN**</span></span>](/windows)         | [<span data-ttu-id="91871-118">**GUIDA \_ AL SISTEMA DEI \_ RUOLIBALLOON**</span><span class="sxs-lookup"><span data-stu-id="91871-118">**ROLE\_SYSTEM\_HELPBALLOON**</span></span>](/windows) |
| [<span data-ttu-id="91871-119">**PULSANTE \_ SISTEMA \_ RUOLODROPDOWNGRID**</span><span class="sxs-lookup"><span data-stu-id="91871-119">**ROLE\_SYSTEM\_BUTTONDROPDOWNGRID**</span></span>](/windows) | [<span data-ttu-id="91871-120">**INDIRIZZO \_ IP DEL SISTEMA DEL \_ RUOLO**</span><span class="sxs-lookup"><span data-stu-id="91871-120">**ROLE\_SYSTEM\_IPADDRESS**</span></span>](/windows)     |
| [<span data-ttu-id="91871-121">**PULSANTE \_ SISTEMA \_ RUOLOMENU**</span><span class="sxs-lookup"><span data-stu-id="91871-121">**ROLE\_SYSTEM\_BUTTONMENU**</span></span>](/windows)                 | [<span data-ttu-id="91871-122">**COLLEGAMENTO \_ AL SISTEMA DEL \_ RUOLO**</span><span class="sxs-lookup"><span data-stu-id="91871-122">**ROLE\_SYSTEM\_LINK**</span></span>](/windows)               |
| [<span data-ttu-id="91871-123">**CELLA \_ DI SISTEMA DEL \_ RUOLO**</span><span class="sxs-lookup"><span data-stu-id="91871-123">**ROLE\_SYSTEM\_CELL**</span></span>](/windows)                             | [<span data-ttu-id="91871-124">**RIQUADRO \_ SISTEMA \_ RUOLO**</span><span class="sxs-lookup"><span data-stu-id="91871-124">**ROLE\_SYSTEM\_PANE**</span></span>](/windows)               |
| [<span data-ttu-id="91871-125">**CARATTERE \_ DI SISTEMA DEL \_ RUOLO**</span><span class="sxs-lookup"><span data-stu-id="91871-125">**ROLE\_SYSTEM\_CHARACTER**</span></span>](/windows)                   | [<span data-ttu-id="91871-126">**ROLE \_ SYSTEM \_ ROW**</span><span class="sxs-lookup"><span data-stu-id="91871-126">**ROLE\_SYSTEM\_ROW**</span></span>](/windows)                 |
| [<span data-ttu-id="91871-127">**GRAFICO \_ DI SISTEMA DEI \_ RUOLI**</span><span class="sxs-lookup"><span data-stu-id="91871-127">**ROLE\_SYSTEM\_CHART**</span></span>](/windows)                           | [<span data-ttu-id="91871-128">**ROLE \_ SYSTEM \_ ROWHEADER**</span><span class="sxs-lookup"><span data-stu-id="91871-128">**ROLE\_SYSTEM\_ROWHEADER**</span></span>](/windows)     |
| [<span data-ttu-id="91871-129">**OROLOGIO \_ DEL SISTEMA DEI \_ RUOLI**</span><span class="sxs-lookup"><span data-stu-id="91871-129">**ROLE\_SYSTEM\_CLOCK**</span></span>](/windows)                           | [<span data-ttu-id="91871-130">**SEPARATORE \_ DI SISTEMA DEI \_ RUOLI**</span><span class="sxs-lookup"><span data-stu-id="91871-130">**ROLE\_SYSTEM\_SEPARATOR**</span></span>](/windows)     |
| [<span data-ttu-id="91871-131">**COLONNA \_ DI SISTEMA DEL \_ RUOLO**</span><span class="sxs-lookup"><span data-stu-id="91871-131">**ROLE\_SYSTEM\_COLUMN**</span></span>](/windows)                         | [<span data-ttu-id="91871-132">**SUONO \_ DEL SISTEMA DEL \_ RUOLO**</span><span class="sxs-lookup"><span data-stu-id="91871-132">**ROLE\_SYSTEM\_SOUND**</span></span>](/windows)             |
| [<span data-ttu-id="91871-133">**DIAGRAMMA \_ SISTEMA RUOLO \_**</span><span class="sxs-lookup"><span data-stu-id="91871-133">**ROLE\_SYSTEM\_DIAGRAM**</span></span>](/windows)                       | [<span data-ttu-id="91871-134">**PULSANTE \_ DI DIVISIONE DEL SISTEMA DEL \_ RUOLO**</span><span class="sxs-lookup"><span data-stu-id="91871-134">**ROLE\_SYSTEM\_SPLITBUTTON**</span></span>](/windows) |
| [<span data-ttu-id="91871-135">**ROLE \_ SYSTEM \_ DIAL**</span><span class="sxs-lookup"><span data-stu-id="91871-135">**ROLE\_SYSTEM\_DIAL**</span></span>](/windows)                             | [<span data-ttu-id="91871-136">**TABELLA \_ DI SISTEMA DEI \_ RUOLI**</span><span class="sxs-lookup"><span data-stu-id="91871-136">**ROLE\_SYSTEM\_TABLE**</span></span>](/windows)             |
| [<span data-ttu-id="91871-137">**DOCUMENTO \_ DI SISTEMA DEL \_ RUOLO**</span><span class="sxs-lookup"><span data-stu-id="91871-137">**ROLE\_SYSTEM\_DOCUMENT**</span></span>](/windows)                     | [<span data-ttu-id="91871-138">**SPAZIO \_ VUOTO DEL SISTEMA DEI \_ RUOLI**</span><span class="sxs-lookup"><span data-stu-id="91871-138">**ROLE\_SYSTEM\_WHITESPACE**</span></span>](/windows)   |



 

## <a name="role_system_alert"></a><span data-ttu-id="91871-139">AVVISO \_ DI SISTEMA DEL \_ RUOLO</span><span class="sxs-lookup"><span data-stu-id="91871-139">ROLE\_SYSTEM\_ALERT</span></span>

<span data-ttu-id="91871-140">Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ ALERT**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="91871-140">For more information on this role, see [**ROLE\_SYSTEM\_ALERT**](object-roles.md).</span></span>

<span data-ttu-id="91871-141">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="91871-141">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="91871-142">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="91871-142">get\_accName</span></span>
-   <span data-ttu-id="91871-143">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="91871-143">get\_accRole</span></span>
-   <span data-ttu-id="91871-144">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="91871-144">get\_accState</span></span>

## <a name="role_system_application"></a><span data-ttu-id="91871-145">APPLICAZIONE \_ DI SISTEMA DEL \_ RUOLO</span><span class="sxs-lookup"><span data-stu-id="91871-145">ROLE\_SYSTEM\_APPLICATION</span></span>

<span data-ttu-id="91871-146">Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ APPLICATION**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="91871-146">For more information on this role, see [**ROLE\_SYSTEM\_APPLICATION**](object-roles.md).</span></span>

<span data-ttu-id="91871-147">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="91871-147">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="91871-148">accHitTest</span><span class="sxs-lookup"><span data-stu-id="91871-148">accHitTest</span></span>
-   <span data-ttu-id="91871-149">accLocation</span><span class="sxs-lookup"><span data-stu-id="91871-149">accLocation</span></span>
-   <span data-ttu-id="91871-150">accNavigate</span><span class="sxs-lookup"><span data-stu-id="91871-150">accNavigate</span></span>
-   <span data-ttu-id="91871-151">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="91871-151">get\_accChild</span></span>
-   <span data-ttu-id="91871-152">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="91871-152">get\_accChildCount</span></span>
-   <span data-ttu-id="91871-153">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="91871-153">get\_accFocus</span></span>
-   <span data-ttu-id="91871-154">ottenere \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="91871-154">get\_accHelp</span></span>
-   <span data-ttu-id="91871-155">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="91871-155">get\_accHelpTopic</span></span>
-   <span data-ttu-id="91871-156">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="91871-156">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="91871-157">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="91871-157">get\_accName</span></span>
-   <span data-ttu-id="91871-158">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="91871-158">get\_accParent</span></span>
-   <span data-ttu-id="91871-159">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="91871-159">get\_accRole</span></span>
-   <span data-ttu-id="91871-160">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="91871-160">get\_accState</span></span>

## <a name="role_system_border"></a><span data-ttu-id="91871-161">BORDO \_ DEL SISTEMA DEL \_ RUOLO</span><span class="sxs-lookup"><span data-stu-id="91871-161">ROLE\_SYSTEM\_BORDER</span></span>

<span data-ttu-id="91871-162">Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ BORDER**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="91871-162">For more information on this role, see [**ROLE\_SYSTEM\_BORDER**](object-roles.md).</span></span>

<span data-ttu-id="91871-163">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="91871-163">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="91871-164">accHitTest</span><span class="sxs-lookup"><span data-stu-id="91871-164">accHitTest</span></span>
-   <span data-ttu-id="91871-165">accLocation</span><span class="sxs-lookup"><span data-stu-id="91871-165">accLocation</span></span>
-   <span data-ttu-id="91871-166">accNavigate</span><span class="sxs-lookup"><span data-stu-id="91871-166">accNavigate</span></span>
-   <span data-ttu-id="91871-167">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="91871-167">get\_accRole</span></span>
-   <span data-ttu-id="91871-168">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="91871-168">get\_accState</span></span>

## <a name="role_system_buttondropdown"></a><span data-ttu-id="91871-169">PULSANTE \_ SISTEMA \_ RUOLODROPDOWN</span><span class="sxs-lookup"><span data-stu-id="91871-169">ROLE\_SYSTEM\_BUTTONDROPDOWN</span></span>

<span data-ttu-id="91871-170">Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ BUTTONDROPDOWN**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="91871-170">For more information on this role, see [**ROLE\_SYSTEM\_BUTTONDROPDOWN**](object-roles.md).</span></span>

<span data-ttu-id="91871-171">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="91871-171">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="91871-172">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="91871-172">accDoDefaultAction</span></span>
-   <span data-ttu-id="91871-173">accHitTest</span><span class="sxs-lookup"><span data-stu-id="91871-173">accHitTest</span></span>
-   <span data-ttu-id="91871-174">accLocation</span><span class="sxs-lookup"><span data-stu-id="91871-174">accLocation</span></span>
-   <span data-ttu-id="91871-175">accNavigate</span><span class="sxs-lookup"><span data-stu-id="91871-175">accNavigate</span></span>
-   <span data-ttu-id="91871-176">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="91871-176">get\_accChild</span></span>
-   <span data-ttu-id="91871-177">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="91871-177">get\_accChildCount</span></span>
-   <span data-ttu-id="91871-178">get \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="91871-178">get\_accDefaultAction</span></span>
-   <span data-ttu-id="91871-179">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="91871-179">get\_accFocus</span></span>
-   <span data-ttu-id="91871-180">ottenere \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="91871-180">get\_accHelp</span></span>
-   <span data-ttu-id="91871-181">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="91871-181">get\_accHelpTopic</span></span>
-   <span data-ttu-id="91871-182">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="91871-182">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="91871-183">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="91871-183">get\_accName</span></span>
-   <span data-ttu-id="91871-184">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="91871-184">get\_accParent</span></span>
-   <span data-ttu-id="91871-185">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="91871-185">get\_accRole</span></span>
-   <span data-ttu-id="91871-186">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="91871-186">get\_accState</span></span>

## <a name="role_system_buttondropdowngrid"></a><span data-ttu-id="91871-187">PULSANTE \_ SISTEMA \_ RUOLODROPDOWNGRID</span><span class="sxs-lookup"><span data-stu-id="91871-187">ROLE\_SYSTEM\_BUTTONDROPDOWNGRID</span></span>

<span data-ttu-id="91871-188">Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ BUTTONDROPDOWNGRID**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="91871-188">For more information on this role, see [**ROLE\_SYSTEM\_BUTTONDROPDOWNGRID**](object-roles.md).</span></span>

<span data-ttu-id="91871-189">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="91871-189">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="91871-190">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="91871-190">accDoDefaultAction</span></span>
-   <span data-ttu-id="91871-191">accHitTest</span><span class="sxs-lookup"><span data-stu-id="91871-191">accHitTest</span></span>
-   <span data-ttu-id="91871-192">accLocation</span><span class="sxs-lookup"><span data-stu-id="91871-192">accLocation</span></span>
-   <span data-ttu-id="91871-193">accNavigate</span><span class="sxs-lookup"><span data-stu-id="91871-193">accNavigate</span></span>
-   <span data-ttu-id="91871-194">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="91871-194">get\_accChild</span></span>
-   <span data-ttu-id="91871-195">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="91871-195">get\_accChildCount</span></span>
-   <span data-ttu-id="91871-196">get \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="91871-196">get\_accDefaultAction</span></span>
-   <span data-ttu-id="91871-197">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="91871-197">get\_accFocus</span></span>
-   <span data-ttu-id="91871-198">ottenere \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="91871-198">get\_accHelp</span></span>
-   <span data-ttu-id="91871-199">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="91871-199">get\_accHelpTopic</span></span>
-   <span data-ttu-id="91871-200">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="91871-200">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="91871-201">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="91871-201">get\_accName</span></span>
-   <span data-ttu-id="91871-202">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="91871-202">get\_accParent</span></span>
-   <span data-ttu-id="91871-203">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="91871-203">get\_accRole</span></span>
-   <span data-ttu-id="91871-204">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="91871-204">get\_accState</span></span>

## <a name="role_system_buttonmenu"></a><span data-ttu-id="91871-205">ROLE \_ SYSTEM \_ BUTTONMENU</span><span class="sxs-lookup"><span data-stu-id="91871-205">ROLE\_SYSTEM\_BUTTONMENU</span></span>

<span data-ttu-id="91871-206">Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ BUTTONMENU**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="91871-206">For more information on this role, see [**ROLE\_SYSTEM\_BUTTONMENU**](object-roles.md).</span></span>

<span data-ttu-id="91871-207">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="91871-207">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="91871-208">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="91871-208">accDoDefaultAction</span></span>
-   <span data-ttu-id="91871-209">accHitTest</span><span class="sxs-lookup"><span data-stu-id="91871-209">accHitTest</span></span>
-   <span data-ttu-id="91871-210">accLocation</span><span class="sxs-lookup"><span data-stu-id="91871-210">accLocation</span></span>
-   <span data-ttu-id="91871-211">accNavigate</span><span class="sxs-lookup"><span data-stu-id="91871-211">accNavigate</span></span>
-   <span data-ttu-id="91871-212">get \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="91871-212">get\_accDefaultAction</span></span>
-   <span data-ttu-id="91871-213">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="91871-213">get\_accFocus</span></span>
-   <span data-ttu-id="91871-214">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="91871-214">get\_accHelp</span></span>
-   <span data-ttu-id="91871-215">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="91871-215">get\_accHelpTopic</span></span>
-   <span data-ttu-id="91871-216">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="91871-216">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="91871-217">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="91871-217">get\_accName</span></span>
-   <span data-ttu-id="91871-218">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="91871-218">get\_accParent</span></span>
-   <span data-ttu-id="91871-219">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="91871-219">get\_accRole</span></span>
-   <span data-ttu-id="91871-220">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="91871-220">get\_accState</span></span>

## <a name="role_system_cell"></a><span data-ttu-id="91871-221">CELLA \_ DEL SISTEMA \_ RUOLO</span><span class="sxs-lookup"><span data-stu-id="91871-221">ROLE\_SYSTEM\_CELL</span></span>

<span data-ttu-id="91871-222">Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ CELL**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="91871-222">For more information on this role, see [**ROLE\_SYSTEM\_CELL**](object-roles.md).</span></span>

<span data-ttu-id="91871-223">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="91871-223">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="91871-224">accHitTest</span><span class="sxs-lookup"><span data-stu-id="91871-224">accHitTest</span></span>
-   <span data-ttu-id="91871-225">accLocation</span><span class="sxs-lookup"><span data-stu-id="91871-225">accLocation</span></span>
-   <span data-ttu-id="91871-226">accNavigate</span><span class="sxs-lookup"><span data-stu-id="91871-226">accNavigate</span></span>
-   <span data-ttu-id="91871-227">accSelect</span><span class="sxs-lookup"><span data-stu-id="91871-227">accSelect</span></span>
-   <span data-ttu-id="91871-228">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="91871-228">get\_accChild</span></span>
-   <span data-ttu-id="91871-229">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="91871-229">get\_accChildCount</span></span>
-   <span data-ttu-id="91871-230">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="91871-230">get\_accFocus</span></span>
-   <span data-ttu-id="91871-231">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="91871-231">get\_accHelp</span></span>
-   <span data-ttu-id="91871-232">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="91871-232">get\_accHelpTopic</span></span>
-   <span data-ttu-id="91871-233">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="91871-233">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="91871-234">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="91871-234">get\_accName</span></span>
-   <span data-ttu-id="91871-235">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="91871-235">get\_accParent</span></span>
-   <span data-ttu-id="91871-236">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="91871-236">get\_accRole</span></span>
-   <span data-ttu-id="91871-237">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="91871-237">get\_accState</span></span>
-   <span data-ttu-id="91871-238">get \_ accValue</span><span class="sxs-lookup"><span data-stu-id="91871-238">get\_accValue</span></span>

## <a name="role_system_character"></a><span data-ttu-id="91871-239">ROLE \_ SYSTEM \_ CHARACTER</span><span class="sxs-lookup"><span data-stu-id="91871-239">ROLE\_SYSTEM\_CHARACTER</span></span>

<span data-ttu-id="91871-240">Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ CHARACTER**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="91871-240">For more information on this role, see [**ROLE\_SYSTEM\_CHARACTER**](object-roles.md).</span></span>

<span data-ttu-id="91871-241">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="91871-241">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="91871-242">accHitTest</span><span class="sxs-lookup"><span data-stu-id="91871-242">accHitTest</span></span>
-   <span data-ttu-id="91871-243">accLocation</span><span class="sxs-lookup"><span data-stu-id="91871-243">accLocation</span></span>
-   <span data-ttu-id="91871-244">accNavigate</span><span class="sxs-lookup"><span data-stu-id="91871-244">accNavigate</span></span>
-   <span data-ttu-id="91871-245">get \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="91871-245">get\_accDescription</span></span>
-   <span data-ttu-id="91871-246">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="91871-246">get\_accFocus</span></span>
-   <span data-ttu-id="91871-247">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="91871-247">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="91871-248">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="91871-248">get\_accName</span></span>
-   <span data-ttu-id="91871-249">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="91871-249">get\_accParent</span></span>
-   <span data-ttu-id="91871-250">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="91871-250">get\_accRole</span></span>
-   <span data-ttu-id="91871-251">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="91871-251">get\_accState</span></span>
-   <span data-ttu-id="91871-252">get \_ accValue</span><span class="sxs-lookup"><span data-stu-id="91871-252">get\_accValue</span></span>

## <a name="role_system_chart"></a><span data-ttu-id="91871-253">ROLE \_ SYSTEM \_ CHART</span><span class="sxs-lookup"><span data-stu-id="91871-253">ROLE\_SYSTEM\_CHART</span></span>

<span data-ttu-id="91871-254">Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ CHART.**](object-roles.md)</span><span class="sxs-lookup"><span data-stu-id="91871-254">For more information on this role, see [**ROLE\_SYSTEM\_CHART**](object-roles.md).</span></span>

<span data-ttu-id="91871-255">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="91871-255">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="91871-256">accHitTest</span><span class="sxs-lookup"><span data-stu-id="91871-256">accHitTest</span></span>
-   <span data-ttu-id="91871-257">accLocation</span><span class="sxs-lookup"><span data-stu-id="91871-257">accLocation</span></span>
-   <span data-ttu-id="91871-258">accNavigate</span><span class="sxs-lookup"><span data-stu-id="91871-258">accNavigate</span></span>
-   <span data-ttu-id="91871-259">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="91871-259">get\_accChild</span></span>
-   <span data-ttu-id="91871-260">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="91871-260">get\_accChildCount</span></span>
-   <span data-ttu-id="91871-261">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="91871-261">get\_accFocus</span></span>
-   <span data-ttu-id="91871-262">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="91871-262">get\_accHelp</span></span>
-   <span data-ttu-id="91871-263">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="91871-263">get\_accHelpTopic</span></span>
-   <span data-ttu-id="91871-264">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="91871-264">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="91871-265">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="91871-265">get\_accName</span></span>
-   <span data-ttu-id="91871-266">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="91871-266">get\_accParent</span></span>
-   <span data-ttu-id="91871-267">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="91871-267">get\_accRole</span></span>
-   <span data-ttu-id="91871-268">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="91871-268">get\_accState</span></span>

## <a name="role_system_clock"></a><span data-ttu-id="91871-269">OROLOGIO \_ DEL SISTEMA DEL \_ RUOLO</span><span class="sxs-lookup"><span data-stu-id="91871-269">ROLE\_SYSTEM\_CLOCK</span></span>

<span data-ttu-id="91871-270">Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ CLOCK**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="91871-270">For more information on this role, see [**ROLE\_SYSTEM\_CLOCK**](object-roles.md).</span></span>

<span data-ttu-id="91871-271">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="91871-271">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="91871-272">accHitTest</span><span class="sxs-lookup"><span data-stu-id="91871-272">accHitTest</span></span>
-   <span data-ttu-id="91871-273">accLocation</span><span class="sxs-lookup"><span data-stu-id="91871-273">accLocation</span></span>
-   <span data-ttu-id="91871-274">accNavigate</span><span class="sxs-lookup"><span data-stu-id="91871-274">accNavigate</span></span>
-   <span data-ttu-id="91871-275">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="91871-275">get\_accFocus</span></span>
-   <span data-ttu-id="91871-276">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="91871-276">get\_accHelp</span></span>
-   <span data-ttu-id="91871-277">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="91871-277">get\_accHelpTopic</span></span>
-   <span data-ttu-id="91871-278">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="91871-278">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="91871-279">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="91871-279">get\_accName</span></span>
-   <span data-ttu-id="91871-280">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="91871-280">get\_accParent</span></span>
-   <span data-ttu-id="91871-281">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="91871-281">get\_accRole</span></span>
-   <span data-ttu-id="91871-282">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="91871-282">get\_accState</span></span>
-   <span data-ttu-id="91871-283">get \_ accValue</span><span class="sxs-lookup"><span data-stu-id="91871-283">get\_accValue</span></span>

## <a name="role_system_column"></a><span data-ttu-id="91871-284">ROLE \_ SYSTEM \_ COLUMN</span><span class="sxs-lookup"><span data-stu-id="91871-284">ROLE\_SYSTEM\_COLUMN</span></span>

<span data-ttu-id="91871-285">Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ COLUMN.**](object-roles.md)</span><span class="sxs-lookup"><span data-stu-id="91871-285">For more information on this role, see [**ROLE\_SYSTEM\_COLUMN**](object-roles.md).</span></span>

<span data-ttu-id="91871-286">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="91871-286">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="91871-287">accHitTest</span><span class="sxs-lookup"><span data-stu-id="91871-287">accHitTest</span></span>
-   <span data-ttu-id="91871-288">accLocation</span><span class="sxs-lookup"><span data-stu-id="91871-288">accLocation</span></span>
-   <span data-ttu-id="91871-289">accNavigate</span><span class="sxs-lookup"><span data-stu-id="91871-289">accNavigate</span></span>
-   <span data-ttu-id="91871-290">accSelect</span><span class="sxs-lookup"><span data-stu-id="91871-290">accSelect</span></span>
-   <span data-ttu-id="91871-291">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="91871-291">get\_accChild</span></span>
-   <span data-ttu-id="91871-292">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="91871-292">get\_accChildCount</span></span>
-   <span data-ttu-id="91871-293">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="91871-293">get\_accFocus</span></span>
-   <span data-ttu-id="91871-294">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="91871-294">get\_accName</span></span>
-   <span data-ttu-id="91871-295">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="91871-295">get\_accParent</span></span>
-   <span data-ttu-id="91871-296">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="91871-296">get\_accRole</span></span>
-   <span data-ttu-id="91871-297">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="91871-297">get\_accState</span></span>
-   <span data-ttu-id="91871-298">get \_ accValue</span><span class="sxs-lookup"><span data-stu-id="91871-298">get\_accValue</span></span>

## <a name="role_system_diagram"></a><span data-ttu-id="91871-299">DIAGRAMMA DEL \_ SISTEMA DI \_ RUOLI</span><span class="sxs-lookup"><span data-stu-id="91871-299">ROLE\_SYSTEM\_DIAGRAM</span></span>

<span data-ttu-id="91871-300">Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ DIAGRAM**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="91871-300">For more information on this role, see [**ROLE\_SYSTEM\_DIAGRAM**](object-roles.md).</span></span>

<span data-ttu-id="91871-301">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="91871-301">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="91871-302">accHitTest</span><span class="sxs-lookup"><span data-stu-id="91871-302">accHitTest</span></span>
-   <span data-ttu-id="91871-303">accLocation</span><span class="sxs-lookup"><span data-stu-id="91871-303">accLocation</span></span>
-   <span data-ttu-id="91871-304">accNavigate</span><span class="sxs-lookup"><span data-stu-id="91871-304">accNavigate</span></span>
-   <span data-ttu-id="91871-305">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="91871-305">get\_accChild</span></span>
-   <span data-ttu-id="91871-306">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="91871-306">get\_accChildCount</span></span>
-   <span data-ttu-id="91871-307">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="91871-307">get\_accFocus</span></span>
-   <span data-ttu-id="91871-308">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="91871-308">get\_accHelp</span></span>
-   <span data-ttu-id="91871-309">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="91871-309">get\_accHelpTopic</span></span>
-   <span data-ttu-id="91871-310">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="91871-310">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="91871-311">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="91871-311">get\_accName</span></span>
-   <span data-ttu-id="91871-312">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="91871-312">get\_accParent</span></span>
-   <span data-ttu-id="91871-313">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="91871-313">get\_accRole</span></span>
-   <span data-ttu-id="91871-314">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="91871-314">get\_accState</span></span>

## <a name="role_system_dial"></a><span data-ttu-id="91871-315">ROLE \_ SYSTEM \_ DIAL</span><span class="sxs-lookup"><span data-stu-id="91871-315">ROLE\_SYSTEM\_DIAL</span></span>

<span data-ttu-id="91871-316">Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ DIAL.**](object-roles.md)</span><span class="sxs-lookup"><span data-stu-id="91871-316">For more information on this role, see [**ROLE\_SYSTEM\_DIAL**](object-roles.md).</span></span>

<span data-ttu-id="91871-317">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="91871-317">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="91871-318">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="91871-318">accDoDefaultAction</span></span>
-   <span data-ttu-id="91871-319">accHitTest</span><span class="sxs-lookup"><span data-stu-id="91871-319">accHitTest</span></span>
-   <span data-ttu-id="91871-320">accLocation</span><span class="sxs-lookup"><span data-stu-id="91871-320">accLocation</span></span>
-   <span data-ttu-id="91871-321">accNavigate</span><span class="sxs-lookup"><span data-stu-id="91871-321">accNavigate</span></span>
-   <span data-ttu-id="91871-322">get \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="91871-322">get\_accDefaultAction</span></span>
-   <span data-ttu-id="91871-323">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="91871-323">get\_accFocus</span></span>
-   <span data-ttu-id="91871-324">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="91871-324">get\_accHelp</span></span>
-   <span data-ttu-id="91871-325">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="91871-325">get\_accHelpTopic</span></span>
-   <span data-ttu-id="91871-326">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="91871-326">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="91871-327">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="91871-327">get\_accName</span></span>
-   <span data-ttu-id="91871-328">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="91871-328">get\_accParent</span></span>
-   <span data-ttu-id="91871-329">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="91871-329">get\_accRole</span></span>
-   <span data-ttu-id="91871-330">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="91871-330">get\_accState</span></span>
-   <span data-ttu-id="91871-331">get \_ accValue</span><span class="sxs-lookup"><span data-stu-id="91871-331">get\_accValue</span></span>

## <a name="role_system_document"></a><span data-ttu-id="91871-332">DOCUMENTO \_ DI SISTEMA DEL \_ RUOLO</span><span class="sxs-lookup"><span data-stu-id="91871-332">ROLE\_SYSTEM\_DOCUMENT</span></span>

<span data-ttu-id="91871-333">Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ DOCUMENT**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="91871-333">For more information on this role, see [**ROLE\_SYSTEM\_DOCUMENT**](object-roles.md).</span></span>

<span data-ttu-id="91871-334">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="91871-334">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="91871-335">accHitTest</span><span class="sxs-lookup"><span data-stu-id="91871-335">accHitTest</span></span>
-   <span data-ttu-id="91871-336">accLocation</span><span class="sxs-lookup"><span data-stu-id="91871-336">accLocation</span></span>
-   <span data-ttu-id="91871-337">accNavigate</span><span class="sxs-lookup"><span data-stu-id="91871-337">accNavigate</span></span>
-   <span data-ttu-id="91871-338">accSelect</span><span class="sxs-lookup"><span data-stu-id="91871-338">accSelect</span></span>
-   <span data-ttu-id="91871-339">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="91871-339">get\_accChild</span></span>
-   <span data-ttu-id="91871-340">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="91871-340">get\_accChildCount</span></span>
-   <span data-ttu-id="91871-341">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="91871-341">get\_accFocus</span></span>
-   <span data-ttu-id="91871-342">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="91871-342">get\_accName</span></span>
-   <span data-ttu-id="91871-343">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="91871-343">get\_accParent</span></span>
-   <span data-ttu-id="91871-344">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="91871-344">get\_accRole</span></span>
-   <span data-ttu-id="91871-345">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="91871-345">get\_accState</span></span>

## <a name="role_system_droplist"></a><span data-ttu-id="91871-346">ROLE \_ SYSTEM \_ DROPLIST</span><span class="sxs-lookup"><span data-stu-id="91871-346">ROLE\_SYSTEM\_DROPLIST</span></span>

<span data-ttu-id="91871-347">Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ DROPLIST**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="91871-347">For more information on this role, see [**ROLE\_SYSTEM\_DROPLIST**](object-roles.md).</span></span>

<span data-ttu-id="91871-348">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="91871-348">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="91871-349">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="91871-349">accDoDefaultAction</span></span>
-   <span data-ttu-id="91871-350">accHitTest</span><span class="sxs-lookup"><span data-stu-id="91871-350">accHitTest</span></span>
-   <span data-ttu-id="91871-351">accLocation</span><span class="sxs-lookup"><span data-stu-id="91871-351">accLocation</span></span>
-   <span data-ttu-id="91871-352">accNavigate</span><span class="sxs-lookup"><span data-stu-id="91871-352">accNavigate</span></span>
-   <span data-ttu-id="91871-353">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="91871-353">get\_accChild</span></span>
-   <span data-ttu-id="91871-354">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="91871-354">get\_accChildCount</span></span>
-   <span data-ttu-id="91871-355">get \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="91871-355">get\_accDefaultAction</span></span>
-   <span data-ttu-id="91871-356">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="91871-356">get\_accFocus</span></span>
-   <span data-ttu-id="91871-357">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="91871-357">get\_accHelp</span></span>
-   <span data-ttu-id="91871-358">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="91871-358">get\_accHelpTopic</span></span>
-   <span data-ttu-id="91871-359">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="91871-359">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="91871-360">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="91871-360">get\_accName</span></span>
-   <span data-ttu-id="91871-361">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="91871-361">get\_accParent</span></span>
-   <span data-ttu-id="91871-362">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="91871-362">get\_accRole</span></span>
-   <span data-ttu-id="91871-363">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="91871-363">get\_accState</span></span>

## <a name="role_system_equation"></a><span data-ttu-id="91871-364">EQUAZIONE \_ DEL SISTEMA \_ DI RUOLI</span><span class="sxs-lookup"><span data-stu-id="91871-364">ROLE\_SYSTEM\_EQUATION</span></span>

<span data-ttu-id="91871-365">Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ EQUATION**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="91871-365">For more information on this role, see [**ROLE\_SYSTEM\_EQUATION**](object-roles.md).</span></span>

<span data-ttu-id="91871-366">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="91871-366">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="91871-367">accHitTest</span><span class="sxs-lookup"><span data-stu-id="91871-367">accHitTest</span></span>
-   <span data-ttu-id="91871-368">accLocation</span><span class="sxs-lookup"><span data-stu-id="91871-368">accLocation</span></span>
-   <span data-ttu-id="91871-369">accNavigate</span><span class="sxs-lookup"><span data-stu-id="91871-369">accNavigate</span></span>
-   <span data-ttu-id="91871-370">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="91871-370">get\_accFocus</span></span>
-   <span data-ttu-id="91871-371">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="91871-371">get\_accName</span></span>
-   <span data-ttu-id="91871-372">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="91871-372">get\_accParent</span></span>
-   <span data-ttu-id="91871-373">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="91871-373">get\_accRole</span></span>
-   <span data-ttu-id="91871-374">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="91871-374">get\_accState</span></span>
-   <span data-ttu-id="91871-375">get \_ accValue</span><span class="sxs-lookup"><span data-stu-id="91871-375">get\_accValue</span></span>

## <a name="role_system_graphic"></a><span data-ttu-id="91871-376">IMMAGINE DEL \_ SISTEMA \_ RUOLO</span><span class="sxs-lookup"><span data-stu-id="91871-376">ROLE\_SYSTEM\_GRAPHIC</span></span>

<span data-ttu-id="91871-377">Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ GRAPHIC.**](object-roles.md)</span><span class="sxs-lookup"><span data-stu-id="91871-377">For more information on this role, see [**ROLE\_SYSTEM\_GRAPHIC**](object-roles.md).</span></span>

<span data-ttu-id="91871-378">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="91871-378">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="91871-379">accHitTest</span><span class="sxs-lookup"><span data-stu-id="91871-379">accHitTest</span></span>
-   <span data-ttu-id="91871-380">accLocation</span><span class="sxs-lookup"><span data-stu-id="91871-380">accLocation</span></span>
-   <span data-ttu-id="91871-381">accNavigate</span><span class="sxs-lookup"><span data-stu-id="91871-381">accNavigate</span></span>
-   <span data-ttu-id="91871-382">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="91871-382">get\_accFocus</span></span>
-   <span data-ttu-id="91871-383">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="91871-383">get\_accHelp</span></span>
-   <span data-ttu-id="91871-384">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="91871-384">get\_accHelpTopic</span></span>
-   <span data-ttu-id="91871-385">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="91871-385">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="91871-386">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="91871-386">get\_accName</span></span>
-   <span data-ttu-id="91871-387">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="91871-387">get\_accParent</span></span>
-   <span data-ttu-id="91871-388">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="91871-388">get\_accRole</span></span>
-   <span data-ttu-id="91871-389">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="91871-389">get\_accState</span></span>

## <a name="role_system_helpballoon"></a><span data-ttu-id="91871-390">GUIDA \_ DEL SISTEMA DEI \_ RUOLIBALLOON</span><span class="sxs-lookup"><span data-stu-id="91871-390">ROLE\_SYSTEM\_HELPBALLOON</span></span>

<span data-ttu-id="91871-391">Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ HELPBALLOON**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="91871-391">For more information on this role, see [**ROLE\_SYSTEM\_HELPBALLOON**](object-roles.md).</span></span>

<span data-ttu-id="91871-392">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="91871-392">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="91871-393">accHitTest</span><span class="sxs-lookup"><span data-stu-id="91871-393">accHitTest</span></span>
-   <span data-ttu-id="91871-394">accLocation</span><span class="sxs-lookup"><span data-stu-id="91871-394">accLocation</span></span>
-   <span data-ttu-id="91871-395">accNavigate</span><span class="sxs-lookup"><span data-stu-id="91871-395">accNavigate</span></span>
-   <span data-ttu-id="91871-396">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="91871-396">get\_accChild</span></span>
-   <span data-ttu-id="91871-397">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="91871-397">get\_accChildCount</span></span>
-   <span data-ttu-id="91871-398">get \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="91871-398">get\_accDefaultAction</span></span>
-   <span data-ttu-id="91871-399">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="91871-399">get\_accName</span></span>
-   <span data-ttu-id="91871-400">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="91871-400">get\_accParent</span></span>
-   <span data-ttu-id="91871-401">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="91871-401">get\_accRole</span></span>
-   <span data-ttu-id="91871-402">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="91871-402">get\_accState</span></span>
-   <span data-ttu-id="91871-403">get \_ accValue</span><span class="sxs-lookup"><span data-stu-id="91871-403">get\_accValue</span></span>

## <a name="role_system_ipaddress"></a><span data-ttu-id="91871-404">ROLE \_ SYSTEM \_ IPADDRESS</span><span class="sxs-lookup"><span data-stu-id="91871-404">ROLE\_SYSTEM\_IPADDRESS</span></span>

<span data-ttu-id="91871-405">Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ IPADDRESS**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="91871-405">For more information on this role, see [**ROLE\_SYSTEM\_IPADDRESS**](object-roles.md).</span></span>

<span data-ttu-id="91871-406">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="91871-406">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="91871-407">accHitTest</span><span class="sxs-lookup"><span data-stu-id="91871-407">accHitTest</span></span>
-   <span data-ttu-id="91871-408">accLocation</span><span class="sxs-lookup"><span data-stu-id="91871-408">accLocation</span></span>
-   <span data-ttu-id="91871-409">accNavigate</span><span class="sxs-lookup"><span data-stu-id="91871-409">accNavigate</span></span>
-   <span data-ttu-id="91871-410">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="91871-410">get\_accChild</span></span>
-   <span data-ttu-id="91871-411">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="91871-411">get\_accChildCount</span></span>
-   <span data-ttu-id="91871-412">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="91871-412">get\_accFocus</span></span>
-   <span data-ttu-id="91871-413">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="91871-413">get\_accHelp</span></span>
-   <span data-ttu-id="91871-414">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="91871-414">get\_accHelpTopic</span></span>
-   <span data-ttu-id="91871-415">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="91871-415">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="91871-416">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="91871-416">get\_accName</span></span>
-   <span data-ttu-id="91871-417">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="91871-417">get\_accParent</span></span>
-   <span data-ttu-id="91871-418">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="91871-418">get\_accRole</span></span>
-   <span data-ttu-id="91871-419">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="91871-419">get\_accState</span></span>
-   <span data-ttu-id="91871-420">get \_ accValue</span><span class="sxs-lookup"><span data-stu-id="91871-420">get\_accValue</span></span>

## <a name="role_system_link"></a><span data-ttu-id="91871-421">COLLEGAMENTO SISTEMA \_ \_ RUOLO</span><span class="sxs-lookup"><span data-stu-id="91871-421">ROLE\_SYSTEM\_LINK</span></span>

<span data-ttu-id="91871-422">Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ LINK.**](object-roles.md)</span><span class="sxs-lookup"><span data-stu-id="91871-422">For more information on this role, see [**ROLE\_SYSTEM\_LINK**](object-roles.md).</span></span>

<span data-ttu-id="91871-423">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="91871-423">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="91871-424">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="91871-424">accDoDefaultAction</span></span>
-   <span data-ttu-id="91871-425">accHitTest</span><span class="sxs-lookup"><span data-stu-id="91871-425">accHitTest</span></span>
-   <span data-ttu-id="91871-426">accLocation</span><span class="sxs-lookup"><span data-stu-id="91871-426">accLocation</span></span>
-   <span data-ttu-id="91871-427">accNavigate</span><span class="sxs-lookup"><span data-stu-id="91871-427">accNavigate</span></span>
-   <span data-ttu-id="91871-428">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="91871-428">get\_accChild</span></span>
-   <span data-ttu-id="91871-429">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="91871-429">get\_accChildCount</span></span>
-   <span data-ttu-id="91871-430">get \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="91871-430">get\_accDefaultAction</span></span>
-   <span data-ttu-id="91871-431">get \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="91871-431">get\_accDescription</span></span>
-   <span data-ttu-id="91871-432">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="91871-432">get\_accFocus</span></span>
-   <span data-ttu-id="91871-433">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="91871-433">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="91871-434">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="91871-434">get\_accName</span></span>
-   <span data-ttu-id="91871-435">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="91871-435">get\_accParent</span></span>
-   <span data-ttu-id="91871-436">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="91871-436">get\_accRole</span></span>
-   <span data-ttu-id="91871-437">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="91871-437">get\_accState</span></span>
-   <span data-ttu-id="91871-438">get \_ accValue</span><span class="sxs-lookup"><span data-stu-id="91871-438">get\_accValue</span></span>

## <a name="role_system_pane"></a><span data-ttu-id="91871-439">RIQUADRO \_ SISTEMA \_ RUOLO</span><span class="sxs-lookup"><span data-stu-id="91871-439">ROLE\_SYSTEM\_PANE</span></span>

<span data-ttu-id="91871-440">Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ PANE**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="91871-440">For more information on this role, see [**ROLE\_SYSTEM\_PANE**](object-roles.md).</span></span>

<span data-ttu-id="91871-441">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="91871-441">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="91871-442">accHitTest</span><span class="sxs-lookup"><span data-stu-id="91871-442">accHitTest</span></span>
-   <span data-ttu-id="91871-443">accLocation</span><span class="sxs-lookup"><span data-stu-id="91871-443">accLocation</span></span>
-   <span data-ttu-id="91871-444">accNavigate</span><span class="sxs-lookup"><span data-stu-id="91871-444">accNavigate</span></span>
-   <span data-ttu-id="91871-445">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="91871-445">get\_accChild</span></span>
-   <span data-ttu-id="91871-446">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="91871-446">get\_accChildCount</span></span>
-   <span data-ttu-id="91871-447">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="91871-447">get\_accFocus</span></span>
-   <span data-ttu-id="91871-448">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="91871-448">get\_accHelp</span></span>
-   <span data-ttu-id="91871-449">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="91871-449">get\_accHelpTopic</span></span>
-   <span data-ttu-id="91871-450">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="91871-450">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="91871-451">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="91871-451">get\_accName</span></span>
-   <span data-ttu-id="91871-452">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="91871-452">get\_accParent</span></span>
-   <span data-ttu-id="91871-453">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="91871-453">get\_accRole</span></span>
-   <span data-ttu-id="91871-454">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="91871-454">get\_accState</span></span>

## <a name="role_system_row"></a><span data-ttu-id="91871-455">ROLE \_ SYSTEM \_ ROW</span><span class="sxs-lookup"><span data-stu-id="91871-455">ROLE\_SYSTEM\_ROW</span></span>

<span data-ttu-id="91871-456">Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ ROW.**](object-roles.md)</span><span class="sxs-lookup"><span data-stu-id="91871-456">For more information on this role, see [**ROLE\_SYSTEM\_ROW**](object-roles.md).</span></span>

<span data-ttu-id="91871-457">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="91871-457">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="91871-458">accHitTest</span><span class="sxs-lookup"><span data-stu-id="91871-458">accHitTest</span></span>
-   <span data-ttu-id="91871-459">accLocation</span><span class="sxs-lookup"><span data-stu-id="91871-459">accLocation</span></span>
-   <span data-ttu-id="91871-460">accNavigate</span><span class="sxs-lookup"><span data-stu-id="91871-460">accNavigate</span></span>
-   <span data-ttu-id="91871-461">accSelect</span><span class="sxs-lookup"><span data-stu-id="91871-461">accSelect</span></span>
-   <span data-ttu-id="91871-462">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="91871-462">get\_accChild</span></span>
-   <span data-ttu-id="91871-463">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="91871-463">get\_accChildCount</span></span>
-   <span data-ttu-id="91871-464">get \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="91871-464">get\_accDescription</span></span>
-   <span data-ttu-id="91871-465">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="91871-465">get\_accFocus</span></span>
-   <span data-ttu-id="91871-466">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="91871-466">get\_accName</span></span>
-   <span data-ttu-id="91871-467">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="91871-467">get\_accParent</span></span>
-   <span data-ttu-id="91871-468">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="91871-468">get\_accRole</span></span>
-   <span data-ttu-id="91871-469">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="91871-469">get\_accState</span></span>
-   <span data-ttu-id="91871-470">get \_ accValue</span><span class="sxs-lookup"><span data-stu-id="91871-470">get\_accValue</span></span>

## <a name="role_system_rowheader"></a><span data-ttu-id="91871-471">ROLE \_ SYSTEM \_ ROWHEADER</span><span class="sxs-lookup"><span data-stu-id="91871-471">ROLE\_SYSTEM\_ROWHEADER</span></span>

<span data-ttu-id="91871-472">Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ ROWHEADER**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="91871-472">For more information on this role, see [**ROLE\_SYSTEM\_ROWHEADER**](object-roles.md).</span></span>

<span data-ttu-id="91871-473">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="91871-473">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="91871-474">accHitTest</span><span class="sxs-lookup"><span data-stu-id="91871-474">accHitTest</span></span>
-   <span data-ttu-id="91871-475">accLocation</span><span class="sxs-lookup"><span data-stu-id="91871-475">accLocation</span></span>
-   <span data-ttu-id="91871-476">accNavigate</span><span class="sxs-lookup"><span data-stu-id="91871-476">accNavigate</span></span>
-   <span data-ttu-id="91871-477">accSelect</span><span class="sxs-lookup"><span data-stu-id="91871-477">accSelect</span></span>
-   <span data-ttu-id="91871-478">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="91871-478">get\_accChild</span></span>
-   <span data-ttu-id="91871-479">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="91871-479">get\_accChildCount</span></span>
-   <span data-ttu-id="91871-480">get \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="91871-480">get\_accDefaultAction</span></span>
-   <span data-ttu-id="91871-481">get \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="91871-481">get\_accDescription</span></span>
-   <span data-ttu-id="91871-482">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="91871-482">get\_accFocus</span></span>
-   <span data-ttu-id="91871-483">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="91871-483">get\_accName</span></span>
-   <span data-ttu-id="91871-484">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="91871-484">get\_accParent</span></span>
-   <span data-ttu-id="91871-485">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="91871-485">get\_accRole</span></span>
-   <span data-ttu-id="91871-486">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="91871-486">get\_accState</span></span>
-   <span data-ttu-id="91871-487">get \_ accValue</span><span class="sxs-lookup"><span data-stu-id="91871-487">get\_accValue</span></span>

## <a name="role_system_separator"></a><span data-ttu-id="91871-488">ROLE \_ SYSTEM \_ SEPARATOR</span><span class="sxs-lookup"><span data-stu-id="91871-488">ROLE\_SYSTEM\_SEPARATOR</span></span>

<span data-ttu-id="91871-489">Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ SEPARATOR**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="91871-489">For more information on this role, see [**ROLE\_SYSTEM\_SEPARATOR**](object-roles.md).</span></span>

<span data-ttu-id="91871-490">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="91871-490">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="91871-491">accHitTest</span><span class="sxs-lookup"><span data-stu-id="91871-491">accHitTest</span></span>
-   <span data-ttu-id="91871-492">accLocation</span><span class="sxs-lookup"><span data-stu-id="91871-492">accLocation</span></span>
-   <span data-ttu-id="91871-493">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="91871-493">get\_accChild</span></span>
-   <span data-ttu-id="91871-494">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="91871-494">get\_accChildCount</span></span>
-   <span data-ttu-id="91871-495">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="91871-495">get\_accParent</span></span>
-   <span data-ttu-id="91871-496">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="91871-496">get\_accRole</span></span>
-   <span data-ttu-id="91871-497">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="91871-497">get\_accState</span></span>

## <a name="role_system_sound"></a><span data-ttu-id="91871-498">SUONO \_ DEL SISTEMA DEL \_ RUOLO</span><span class="sxs-lookup"><span data-stu-id="91871-498">ROLE\_SYSTEM\_SOUND</span></span>

<span data-ttu-id="91871-499">Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ SOUND**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="91871-499">For more information on this role, see [**ROLE\_SYSTEM\_SOUND**](object-roles.md).</span></span>

<span data-ttu-id="91871-500">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="91871-500">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="91871-501">get \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="91871-501">get\_accDescription</span></span>
-   <span data-ttu-id="91871-502">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="91871-502">get\_accName</span></span>
-   <span data-ttu-id="91871-503">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="91871-503">get\_accRole</span></span>
-   <span data-ttu-id="91871-504">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="91871-504">get\_accState</span></span>

## <a name="role_system_splitbutton"></a><span data-ttu-id="91871-505">RUOLO \_ SISTEMA \_ SPLITBUTTON</span><span class="sxs-lookup"><span data-stu-id="91871-505">ROLE\_SYSTEM\_SPLITBUTTON</span></span>

<span data-ttu-id="91871-506">Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ SPLITBUTTON**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="91871-506">For more information on this role, see [**ROLE\_SYSTEM\_SPLITBUTTON**](object-roles.md).</span></span>

<span data-ttu-id="91871-507">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="91871-507">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="91871-508">accDoDefaultAction</span><span class="sxs-lookup"><span data-stu-id="91871-508">accDoDefaultAction</span></span>
-   <span data-ttu-id="91871-509">accHitTest</span><span class="sxs-lookup"><span data-stu-id="91871-509">accHitTest</span></span>
-   <span data-ttu-id="91871-510">accLocation</span><span class="sxs-lookup"><span data-stu-id="91871-510">accLocation</span></span>
-   <span data-ttu-id="91871-511">accNavigate</span><span class="sxs-lookup"><span data-stu-id="91871-511">accNavigate</span></span>
-   <span data-ttu-id="91871-512">get \_ accDefaultAction</span><span class="sxs-lookup"><span data-stu-id="91871-512">get\_accDefaultAction</span></span>
-   <span data-ttu-id="91871-513">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="91871-513">get\_accHelp</span></span>
-   <span data-ttu-id="91871-514">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="91871-514">get\_accHelpTopic</span></span>
-   <span data-ttu-id="91871-515">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="91871-515">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="91871-516">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="91871-516">get\_accName</span></span>
-   <span data-ttu-id="91871-517">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="91871-517">get\_accParent</span></span>
-   <span data-ttu-id="91871-518">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="91871-518">get\_accRole</span></span>
-   <span data-ttu-id="91871-519">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="91871-519">get\_accState</span></span>

## <a name="role_system_table"></a><span data-ttu-id="91871-520">TABELLA \_ DI SISTEMA DEI \_ RUOLI</span><span class="sxs-lookup"><span data-stu-id="91871-520">ROLE\_SYSTEM\_TABLE</span></span>

<span data-ttu-id="91871-521">Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ TABLE.**](object-roles.md)</span><span class="sxs-lookup"><span data-stu-id="91871-521">For more information on this role, see [**ROLE\_SYSTEM\_TABLE**](object-roles.md).</span></span>

<span data-ttu-id="91871-522">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="91871-522">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="91871-523">accHitTest</span><span class="sxs-lookup"><span data-stu-id="91871-523">accHitTest</span></span>
-   <span data-ttu-id="91871-524">accLocation</span><span class="sxs-lookup"><span data-stu-id="91871-524">accLocation</span></span>
-   <span data-ttu-id="91871-525">accNavigate</span><span class="sxs-lookup"><span data-stu-id="91871-525">accNavigate</span></span>
-   <span data-ttu-id="91871-526">accSelect</span><span class="sxs-lookup"><span data-stu-id="91871-526">accSelect</span></span>
-   <span data-ttu-id="91871-527">get \_ accChild</span><span class="sxs-lookup"><span data-stu-id="91871-527">get\_accChild</span></span>
-   <span data-ttu-id="91871-528">get \_ accChildCount</span><span class="sxs-lookup"><span data-stu-id="91871-528">get\_accChildCount</span></span>
-   <span data-ttu-id="91871-529">get \_ accDescription</span><span class="sxs-lookup"><span data-stu-id="91871-529">get\_accDescription</span></span>
-   <span data-ttu-id="91871-530">get \_ accFocus</span><span class="sxs-lookup"><span data-stu-id="91871-530">get\_accFocus</span></span>
-   <span data-ttu-id="91871-531">get \_ accHelp</span><span class="sxs-lookup"><span data-stu-id="91871-531">get\_accHelp</span></span>
-   <span data-ttu-id="91871-532">get \_ accHelpTopic</span><span class="sxs-lookup"><span data-stu-id="91871-532">get\_accHelpTopic</span></span>
-   <span data-ttu-id="91871-533">get \_ accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="91871-533">get\_accKeyboardShortcut</span></span>
-   <span data-ttu-id="91871-534">get \_ accName</span><span class="sxs-lookup"><span data-stu-id="91871-534">get\_accName</span></span>
-   <span data-ttu-id="91871-535">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="91871-535">get\_accParent</span></span>
-   <span data-ttu-id="91871-536">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="91871-536">get\_accRole</span></span>
-   <span data-ttu-id="91871-537">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="91871-537">get\_accState</span></span>

## <a name="role_system_whitespace"></a><span data-ttu-id="91871-538">SPAZIO \_ VUOTO DEL SISTEMA DI \_ RUOLI</span><span class="sxs-lookup"><span data-stu-id="91871-538">ROLE\_SYSTEM\_WHITESPACE</span></span>

<span data-ttu-id="91871-539">Per altre informazioni su questo ruolo, vedere [**ROLE \_ SYSTEM \_ WHITESPACE**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="91871-539">For more information on this role, see [**ROLE\_SYSTEM\_WHITESPACE**](object-roles.md).</span></span>

<span data-ttu-id="91871-540">**Proprietà e metodi supportati**</span><span class="sxs-lookup"><span data-stu-id="91871-540">**Supported Properties and Methods**</span></span>

-   <span data-ttu-id="91871-541">accLocation</span><span class="sxs-lookup"><span data-stu-id="91871-541">accLocation</span></span>
-   <span data-ttu-id="91871-542">accSelect</span><span class="sxs-lookup"><span data-stu-id="91871-542">accSelect</span></span>
-   <span data-ttu-id="91871-543">get \_ accParent</span><span class="sxs-lookup"><span data-stu-id="91871-543">get\_accParent</span></span>
-   <span data-ttu-id="91871-544">get \_ accRole</span><span class="sxs-lookup"><span data-stu-id="91871-544">get\_accRole</span></span>
-   <span data-ttu-id="91871-545">get \_ accState</span><span class="sxs-lookup"><span data-stu-id="91871-545">get\_accState</span></span>

 

 