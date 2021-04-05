---
title: Uso di sottoclassi di tema
description: Le classi di tema che rappresentano controlli quali ComboBox, Edit, ExplorerBar, Rebar, TAB e Toolbar possono essere sottoclassi per fornire variazioni del tema per quel particolare controllo.
ms.assetid: 4f5e26c1-72ae-48de-a407-9ac3c0d5f502
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5c5448bb5fea90193beed854e833cd34e7691b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710048"
---
# <a name="using-theme-subclasses"></a><span data-ttu-id="17401-103">Uso di sottoclassi di tema</span><span class="sxs-lookup"><span data-stu-id="17401-103">Using Theme Subclasses</span></span>

<span data-ttu-id="17401-104">Le classi di tema che rappresentano controlli quali ComboBox, Edit, ExplorerBar, Rebar, TAB e Toolbar possono essere sottoclassi per fornire variazioni del tema per quel particolare controllo.</span><span class="sxs-lookup"><span data-stu-id="17401-104">Theme classes that represent controls such as ComboBox, Edit, ExplorerBar, Rebar, Tab, and Toolbar can be subclassed in order to provide theme variations for that particular control.</span></span> <span data-ttu-id="17401-105">La classe **Button** , ad esempio, è sottoclassata come per `Start::Button` fornire il controllo sul tema applicato al pulsante **Avvia** .</span><span class="sxs-lookup"><span data-stu-id="17401-105">For example, the **Button** class is subclassed as `Start::Button` in order to provide control over the theme applied to the **Start** button.</span></span>

> [!Note]  
> <span data-ttu-id="17401-106">Prestare attenzione quando si creano sottoclassi come quelle descritte in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="17401-106">Use caution when you create subclasses like those that are discussed in this topic.</span></span> <span data-ttu-id="17401-107">Poiché le sottoclassi potrebbero essere modificate o non disponibili nelle versioni successive di Windows, non è consigliabile utilizzarle.</span><span class="sxs-lookup"><span data-stu-id="17401-107">Because subclasses might be altered or unavailable in subsequent versions of Windows, you are discouraged from using them.</span></span>

 

## <a name="two-ways-to-use-a-theme-subclass"></a><span data-ttu-id="17401-108">Due modi per usare una sottoclasse di tema</span><span class="sxs-lookup"><span data-stu-id="17401-108">Two Ways to Use a Theme Subclass</span></span>

<span data-ttu-id="17401-109">Un'applicazione può usare un tema sottoclassato in uno dei due modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="17401-109">An application can use a subclassed theme in one of these two ways:</span></span>

-   <span data-ttu-id="17401-110">Può usare la funzione [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) con una stringa del form `subclass::class` nel parametro *pszClassList* .</span><span class="sxs-lookup"><span data-stu-id="17401-110">It can use the [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) function with a string of the form `subclass::class` in the *pszClassList* parameter.</span></span>
-   <span data-ttu-id="17401-111">Può chiamare [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) con il nome della sottoclasse del tema nel parametro *pszSubAppName* .</span><span class="sxs-lookup"><span data-stu-id="17401-111">It can call [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) with the theme subclass name in the *pszSubAppName* parameter.</span></span>

## <a name="using-theme-messages-that-set-visual-style"></a><span data-ttu-id="17401-112">Uso di messaggi di tema che impostano lo stile di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="17401-112">Using Theme Messages That Set Visual Style</span></span>

<span data-ttu-id="17401-113">Alcuni controlli, ad esempio Rebar e Toolbar, forniscono messaggi specifici che è possibile inviare per indicare al controllo di usare una sottoclasse di tema.</span><span class="sxs-lookup"><span data-stu-id="17401-113">Certain controls, such as Rebar and Toolbar, provide specific messages that you can send to instruct the control to use a theme subclass.</span></span> <span data-ttu-id="17401-114">Per questi controlli, fornire un puntatore a un buffer contenente il nome della sottoclasse del tema nel parametro *lParam* del messaggio.</span><span class="sxs-lookup"><span data-stu-id="17401-114">For those controls, provide a pointer to a buffer that contains the theme subclass name in the *lParam* parameter of the message.</span></span> <span data-ttu-id="17401-115">Usare il messaggio [**\_ SETWINDOWTHEME CCM**](ccm-setwindowtheme.md) generico oppure usare una variante specifica come quelle mostrate nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="17401-115">Use the generic [**CCM\_SETWINDOWTHEME**](ccm-setwindowtheme.md) message, or use a specific variant like those shown in the following table.</span></span>



| <span data-ttu-id="17401-116">Control</span><span class="sxs-lookup"><span data-stu-id="17401-116">Control</span></span>    | <span data-ttu-id="17401-117">Message</span><span class="sxs-lookup"><span data-stu-id="17401-117">Message</span></span>                                             |
|------------|-----------------------------------------------------|
| <span data-ttu-id="17401-118">Descrizione comando</span><span class="sxs-lookup"><span data-stu-id="17401-118">Tooltip</span></span>    | [<span data-ttu-id="17401-119">**\_SETWINDOWTHEME TTM**</span><span class="sxs-lookup"><span data-stu-id="17401-119">**TTM\_SETWINDOWTHEME**</span></span>](ttm-setwindowtheme.md)   |
| <span data-ttu-id="17401-120">Barra degli strumenti</span><span class="sxs-lookup"><span data-stu-id="17401-120">Toolbar</span></span>    | [<span data-ttu-id="17401-121">**TB \_ SETWINDOWTHEME**</span><span class="sxs-lookup"><span data-stu-id="17401-121">**TB\_SETWINDOWTHEME**</span></span>](tb-setwindowtheme.md)     |
| <span data-ttu-id="17401-122">Rebar</span><span class="sxs-lookup"><span data-stu-id="17401-122">Rebar</span></span>      | [<span data-ttu-id="17401-123">**RB \_ SETWINDOWTHEME**</span><span class="sxs-lookup"><span data-stu-id="17401-123">**RB\_SETWINDOWTHEME**</span></span>](rb-setwindowtheme.md)     |
| <span data-ttu-id="17401-124">ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="17401-124">ComboBoxEx</span></span> | [<span data-ttu-id="17401-125">**\_SETWINDOWTHEME CBEM**</span><span class="sxs-lookup"><span data-stu-id="17401-125">**CBEM\_SETWINDOWTHEME**</span></span>](cbem-setwindowtheme.md) |



 

<span data-ttu-id="17401-126">Nella tabella seguente sono elencate alcune delle sottoclassi definite da Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="17401-126">The following table lists some of the subclasses that Windows Vista defines.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="17401-127">Classe</span><span class="sxs-lookup"><span data-stu-id="17401-127">Class</span></span></th>
<th><span data-ttu-id="17401-128">Sottoclassi</span><span class="sxs-lookup"><span data-stu-id="17401-128">Subclasses</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="17401-129">ComboBox</span><span class="sxs-lookup"><span data-stu-id="17401-129">ComboBox</span></span></td>
<td><ul>
<li><span data-ttu-id="17401-130">Indirizzo</span><span class="sxs-lookup"><span data-stu-id="17401-130">Address</span></span></li>
<li><span data-ttu-id="17401-131">AddressComposited</span><span class="sxs-lookup"><span data-stu-id="17401-131">AddressComposited</span></span></li>
<li><span data-ttu-id="17401-132">InactiveAddress</span><span class="sxs-lookup"><span data-stu-id="17401-132">InactiveAddress</span></span></li>
<li><span data-ttu-id="17401-133">InactiveAddressComposited</span><span class="sxs-lookup"><span data-stu-id="17401-133">InactiveAddressComposited</span></span></li>
<li><span data-ttu-id="17401-134">MaxAddress</span><span class="sxs-lookup"><span data-stu-id="17401-134">MaxAddress</span></span></li>
<li><span data-ttu-id="17401-135">MaxAddressComposited</span><span class="sxs-lookup"><span data-stu-id="17401-135">MaxAddressComposited</span></span></li>
<li><span data-ttu-id="17401-136">MaxInactiveAddress</span><span class="sxs-lookup"><span data-stu-id="17401-136">MaxInactiveAddress</span></span></li>
<li><span data-ttu-id="17401-137">MaxInactiveAddressComposited</span><span class="sxs-lookup"><span data-stu-id="17401-137">MaxInactiveAddressComposited</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17401-138">Modifica</span><span class="sxs-lookup"><span data-stu-id="17401-138">Edit</span></span></td>
<td><ul>
<li><span data-ttu-id="17401-139">Indirizzo</span><span class="sxs-lookup"><span data-stu-id="17401-139">Address</span></span></li>
<li><span data-ttu-id="17401-140">AddressComposited</span><span class="sxs-lookup"><span data-stu-id="17401-140">AddressComposited</span></span></li>
<li><span data-ttu-id="17401-141">InactiveAddress</span><span class="sxs-lookup"><span data-stu-id="17401-141">InactiveAddress</span></span></li>
<li><span data-ttu-id="17401-142">InactiveAddressComposited</span><span class="sxs-lookup"><span data-stu-id="17401-142">InactiveAddressComposited</span></span></li>
<li><span data-ttu-id="17401-143">InactiveSearchBoxEdit</span><span class="sxs-lookup"><span data-stu-id="17401-143">InactiveSearchBoxEdit</span></span></li>
<li><span data-ttu-id="17401-144">InactiveSearchBoxEditComposited</span><span class="sxs-lookup"><span data-stu-id="17401-144">InactiveSearchBoxEditComposited</span></span></li>
<li><span data-ttu-id="17401-145">MaxAddress</span><span class="sxs-lookup"><span data-stu-id="17401-145">MaxAddress</span></span></li>
<li><span data-ttu-id="17401-146">MaxAddressComposited</span><span class="sxs-lookup"><span data-stu-id="17401-146">MaxAddressComposited</span></span></li>
<li><span data-ttu-id="17401-147">MaxInactiveAddress</span><span class="sxs-lookup"><span data-stu-id="17401-147">MaxInactiveAddress</span></span></li>
<li><span data-ttu-id="17401-148">MaxInactiveAddressComposited</span><span class="sxs-lookup"><span data-stu-id="17401-148">MaxInactiveAddressComposited</span></span></li>
<li><span data-ttu-id="17401-149">MaxInactiveSearchBoxEdit</span><span class="sxs-lookup"><span data-stu-id="17401-149">MaxInactiveSearchBoxEdit</span></span></li>
<li><span data-ttu-id="17401-150">MaxInactiveSearchBoxEditComposited</span><span class="sxs-lookup"><span data-stu-id="17401-150">MaxInactiveSearchBoxEditComposited</span></span></li>
<li><span data-ttu-id="17401-151">MaxSearchBoxEdit</span><span class="sxs-lookup"><span data-stu-id="17401-151">MaxSearchBoxEdit</span></span></li>
<li><span data-ttu-id="17401-152">MaxSearchBoxEditComposited</span><span class="sxs-lookup"><span data-stu-id="17401-152">MaxSearchBoxEditComposited</span></span></li>
<li><span data-ttu-id="17401-153">SearchBoxEdit</span><span class="sxs-lookup"><span data-stu-id="17401-153">SearchBoxEdit</span></span></li>
<li><span data-ttu-id="17401-154">SearchBoxEditComposited</span><span class="sxs-lookup"><span data-stu-id="17401-154">SearchBoxEditComposited</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="17401-155">Rebar</span><span class="sxs-lookup"><span data-stu-id="17401-155">Rebar</span></span></td>
<td><ul>
<li><span data-ttu-id="17401-156">BrowserTabBar</span><span class="sxs-lookup"><span data-stu-id="17401-156">BrowserTabBar</span></span></li>
<li><span data-ttu-id="17401-157">InactiveNavbar</span><span class="sxs-lookup"><span data-stu-id="17401-157">InactiveNavbar</span></span></li>
<li><span data-ttu-id="17401-158">InactiveNavbarComposited</span><span class="sxs-lookup"><span data-stu-id="17401-158">InactiveNavbarComposited</span></span></li>
<li><span data-ttu-id="17401-159">MaxInactiveNavbar</span><span class="sxs-lookup"><span data-stu-id="17401-159">MaxInactiveNavbar</span></span></li>
<li><span data-ttu-id="17401-160">MaxInactiveNavbarComposited</span><span class="sxs-lookup"><span data-stu-id="17401-160">MaxInactiveNavbarComposited</span></span></li>
<li><span data-ttu-id="17401-161">MaxNavbar</span><span class="sxs-lookup"><span data-stu-id="17401-161">MaxNavbar</span></span></li>
<li><span data-ttu-id="17401-162">MaxNavbarComposited</span><span class="sxs-lookup"><span data-stu-id="17401-162">MaxNavbarComposited</span></span></li>
<li><span data-ttu-id="17401-163">Barra di navigazione</span><span class="sxs-lookup"><span data-stu-id="17401-163">Navbar</span></span></li>
<li><span data-ttu-id="17401-164">NavbarComposited</span><span class="sxs-lookup"><span data-stu-id="17401-164">NavbarComposited</span></span></li>
<li><span data-ttu-id="17401-165">NavbarNonTopmost</span><span class="sxs-lookup"><span data-stu-id="17401-165">NavbarNonTopmost</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17401-166">Scheda</span><span class="sxs-lookup"><span data-stu-id="17401-166">Tab</span></span></td>
<td><ul>
<li><span data-ttu-id="17401-167">BrowserTab</span><span class="sxs-lookup"><span data-stu-id="17401-167">BrowserTab</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="17401-168">Barra degli strumenti</span><span class="sxs-lookup"><span data-stu-id="17401-168">Toolbar</span></span></td>
<td><ul>
<li><span data-ttu-id="17401-169">Go</span><span class="sxs-lookup"><span data-stu-id="17401-169">Go</span></span></li>
<li><span data-ttu-id="17401-170">GoComposited</span><span class="sxs-lookup"><span data-stu-id="17401-170">GoComposited</span></span></li>
<li><span data-ttu-id="17401-171">InactiveGo</span><span class="sxs-lookup"><span data-stu-id="17401-171">InactiveGo</span></span></li>
<li><span data-ttu-id="17401-172">InactiveGoComposited</span><span class="sxs-lookup"><span data-stu-id="17401-172">InactiveGoComposited</span></span></li>
<li><span data-ttu-id="17401-173">MaxGo</span><span class="sxs-lookup"><span data-stu-id="17401-173">MaxGo</span></span></li>
<li><span data-ttu-id="17401-174">MaxGoComposited</span><span class="sxs-lookup"><span data-stu-id="17401-174">MaxGoComposited</span></span></li>
<li><span data-ttu-id="17401-175">MaxInactiveGo</span><span class="sxs-lookup"><span data-stu-id="17401-175">MaxInactiveGo</span></span></li>
<li><span data-ttu-id="17401-176">MaxInactiveGoComposited</span><span class="sxs-lookup"><span data-stu-id="17401-176">MaxInactiveGoComposited</span></span></li>
<li><span data-ttu-id="17401-177">SearchButton</span><span class="sxs-lookup"><span data-stu-id="17401-177">SearchButton</span></span></li>
<li><span data-ttu-id="17401-178">SearchButtonComposited</span><span class="sxs-lookup"><span data-stu-id="17401-178">SearchButtonComposited</span></span></li>
<li><span data-ttu-id="17401-179">Viaggi</span><span class="sxs-lookup"><span data-stu-id="17401-179">Travel</span></span></li>
<li><span data-ttu-id="17401-180">TravelComposited</span><span class="sxs-lookup"><span data-stu-id="17401-180">TravelComposited</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="internet-explorer-subclasses"></a><span data-ttu-id="17401-181">Sottoclassi di Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="17401-181">Internet Explorer Subclasses</span></span>

<span data-ttu-id="17401-182">In Windows Vista, le sottoclassi di determinate classi interne a Windows Internet Explorer ed Esplora risorse sono disponibili anche se le classi stesse non lo sono.</span><span class="sxs-lookup"><span data-stu-id="17401-182">In Windows Vista, the subclasses of certain classes internal to Windows Internet Explorer and Windows Explorer are available even though the classes themselves are not.</span></span> <span data-ttu-id="17401-183">Nella tabella seguente sono elencate le sottoclassi disponibili.</span><span class="sxs-lookup"><span data-stu-id="17401-183">The following table lists the available subclasses.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="17401-184">AddressBand</span><span class="sxs-lookup"><span data-stu-id="17401-184">AddressBand</span></span></td>
<td><ul>
<li><span data-ttu-id="17401-185">AB</span><span class="sxs-lookup"><span data-stu-id="17401-185">AB</span></span></li>
<li><span data-ttu-id="17401-186">ABGreen</span><span class="sxs-lookup"><span data-stu-id="17401-186">ABGreen</span></span></li>
<li><span data-ttu-id="17401-187">ABGreenComposited</span><span class="sxs-lookup"><span data-stu-id="17401-187">ABGreenComposited</span></span></li>
<li><span data-ttu-id="17401-188">ABRed</span><span class="sxs-lookup"><span data-stu-id="17401-188">ABRed</span></span></li>
<li><span data-ttu-id="17401-189">ABRedComposited</span><span class="sxs-lookup"><span data-stu-id="17401-189">ABRedComposited</span></span></li>
<li><span data-ttu-id="17401-190">ABYellow</span><span class="sxs-lookup"><span data-stu-id="17401-190">ABYellow</span></span></li>
<li><span data-ttu-id="17401-191">ABYellowComposited</span><span class="sxs-lookup"><span data-stu-id="17401-191">ABYellowComposited</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="17401-192">SearchBox</span><span class="sxs-lookup"><span data-stu-id="17401-192">SearchBox</span></span></td>
<td><ul>
<li><span data-ttu-id="17401-193">InactiveSearchBox</span><span class="sxs-lookup"><span data-stu-id="17401-193">InactiveSearchBox</span></span></li>
<li><span data-ttu-id="17401-194">InactiveSearchBoxComposited</span><span class="sxs-lookup"><span data-stu-id="17401-194">InactiveSearchBoxComposited</span></span></li>
<li><span data-ttu-id="17401-195">MaxInactiveSearchBox</span><span class="sxs-lookup"><span data-stu-id="17401-195">MaxInactiveSearchBox</span></span></li>
<li><span data-ttu-id="17401-196">MaxInactiveSearchBoxComposited</span><span class="sxs-lookup"><span data-stu-id="17401-196">MaxInactiveSearchBoxComposited</span></span></li>
<li><span data-ttu-id="17401-197">MaxSearchBox</span><span class="sxs-lookup"><span data-stu-id="17401-197">MaxSearchBox</span></span></li>
<li><span data-ttu-id="17401-198">MaxSearchBoxComposited</span><span class="sxs-lookup"><span data-stu-id="17401-198">MaxSearchBoxComposited</span></span></li>
<li><span data-ttu-id="17401-199">SearchBoxComposited</span><span class="sxs-lookup"><span data-stu-id="17401-199">SearchBoxComposited</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="17401-200">Nella tabella seguente vengono illustrate le specifiche di queste classi.</span><span class="sxs-lookup"><span data-stu-id="17401-200">The following table shows the specifics of these classes.</span></span>



| <span data-ttu-id="17401-201">Control</span><span class="sxs-lookup"><span data-stu-id="17401-201">Control</span></span>     | <span data-ttu-id="17401-202">Parte</span><span class="sxs-lookup"><span data-stu-id="17401-202">Part</span></span>         | <span data-ttu-id="17401-203">Stati</span><span class="sxs-lookup"><span data-stu-id="17401-203">States</span></span>                                                 |
|-------------|--------------|--------------------------------------------------------|
| <span data-ttu-id="17401-204">ADDRESSBAND</span><span class="sxs-lookup"><span data-stu-id="17401-204">ADDRESSBAND</span></span> | <span data-ttu-id="17401-205">ABBACKGROUND</span><span class="sxs-lookup"><span data-stu-id="17401-205">ABBACKGROUND</span></span> | <span data-ttu-id="17401-206">NORMAL (0x1), HOT (0x2), DISABLEd (0x3), FOCUSED (0x4)</span><span class="sxs-lookup"><span data-stu-id="17401-206">NORMAL (0x1), HOT (0x2), DISABLED (0x3), FOCUSED (0x4)</span></span> |
| <span data-ttu-id="17401-207">SEARCHBOX</span><span class="sxs-lookup"><span data-stu-id="17401-207">SEARCHBOX</span></span>   | <span data-ttu-id="17401-208">SBBACKGROUND</span><span class="sxs-lookup"><span data-stu-id="17401-208">SBBACKGROUND</span></span> | <span data-ttu-id="17401-209">NORMAL (0x1), HOT (0x2), DISABLEd (0x3), FOCUSED (0x4)</span><span class="sxs-lookup"><span data-stu-id="17401-209">NORMAL (0x1), HOT (0x2), DISABLED (0x3), FOCUSED (0x4)</span></span> |



 

 

 




