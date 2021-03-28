---
description: A partire da Windows XP, il pannello di controllo supporta la categorizzazione degli elementi del pannello di controllo. Gli elementi sono registrati per essere visualizzati in una o più categorie. Non è possibile creare nuove categorie.
title: Assegnazione delle categorie del pannello di controllo
ms.topic: article
ms.date: 05/31/2018
ms.assetid: e189b57d-c066-4f28-b1d5-3e05d6c6eeb2
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: bade62cda23c2d2f66ffdfd70f3f555a243f3efc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977407"
---
# <a name="assigning-control-panel-categories"></a><span data-ttu-id="d2e54-105">Assegnazione delle categorie del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="d2e54-105">Assigning Control Panel Categories</span></span>

<span data-ttu-id="d2e54-106">A partire da Windows XP, il pannello di controllo supporta la categorizzazione degli elementi del pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="d2e54-106">As of Windows XP, Control Panel supports categorization of Control Panel items.</span></span> <span data-ttu-id="d2e54-107">Gli elementi sono registrati per essere visualizzati in una o più categorie.</span><span class="sxs-lookup"><span data-stu-id="d2e54-107">Items are registered to appear in one or more category.</span></span> <span data-ttu-id="d2e54-108">Non è possibile creare nuove categorie.</span><span class="sxs-lookup"><span data-stu-id="d2e54-108">New categories cannot be created.</span></span>

<span data-ttu-id="d2e54-109">Per registrare un elemento del pannello di controllo in una o più categorie, aggiungere i valori come illustrato nella sezione registrazione elemento del pannello di controllo [eseguibile](registering-control-panel-items.md) o [registrazione elemento](registering-control-panel-items.md) del pannello di controllo di registrazione degli [elementi del pannello di controllo](registering-control-panel-items.md), a seconda dei casi.</span><span class="sxs-lookup"><span data-stu-id="d2e54-109">To register a Control Panel item in one or more categories, add values as explained in the [Executable Control Panel Item Registration](registering-control-panel-items.md) or [DLL Control Panel Item Registration](registering-control-panel-items.md) section of [Registering Control Panel Items](registering-control-panel-items.md), as appropriate.</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d2e54-110">ID della categoria</span><span class="sxs-lookup"><span data-stu-id="d2e54-110">Category ID</span></span></th>
<th><span data-ttu-id="d2e54-111">Nome categoria (Windows 7)</span><span class="sxs-lookup"><span data-stu-id="d2e54-111">Category Name (Windows 7)</span></span></th>
<th><span data-ttu-id="d2e54-112">Nome categoria (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="d2e54-112">Category Name (Windows Vista)</span></span></th>
<th><span data-ttu-id="d2e54-113">Nome categoria (Windows XP)</span><span class="sxs-lookup"><span data-stu-id="d2e54-113">Category Name (Windows XP)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d2e54-114">0</span><span class="sxs-lookup"><span data-stu-id="d2e54-114">0</span></span></td>
<td><span data-ttu-id="d2e54-115">&quot;Tutti gli elementi del pannello di controllo&quot;</span><span class="sxs-lookup"><span data-stu-id="d2e54-115">&quot;All Control Panel Items&quot;</span></span></td>
<td><span data-ttu-id="d2e54-116">&quot;Opzioni aggiuntive&quot;</span><span class="sxs-lookup"><span data-stu-id="d2e54-116">&quot;Additional Options&quot;</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="d2e54-117">In questa categoria vengono visualizzati tutti gli elementi del pannello di controllo che non specificano un ID categoria.</span><span class="sxs-lookup"><span data-stu-id="d2e54-117">Any Control Panel item that does not specify a category ID appears in this category.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="d2e54-118">&quot;Altre opzioni del pannello di controllo&quot;</span><span class="sxs-lookup"><span data-stu-id="d2e54-118">&quot;Other Control Panel Options&quot;</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="d2e54-119">In questa categoria vengono visualizzati tutti gli elementi del pannello di controllo che non specificano un ID categoria.</span><span class="sxs-lookup"><span data-stu-id="d2e54-119">Any Control Panel item that does not specify a category ID appears in this category.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2e54-120">1</span><span class="sxs-lookup"><span data-stu-id="d2e54-120">1</span></span></td>
<td><span data-ttu-id="d2e54-121">&quot;Aspetto e personalizzazione&quot;</span><span class="sxs-lookup"><span data-stu-id="d2e54-121">&quot;Appearance and Personalization&quot;</span></span></td>
<td><span data-ttu-id="d2e54-122">&quot;Aspetto e personalizzazione&quot;</span><span class="sxs-lookup"><span data-stu-id="d2e54-122">&quot;Appearance and Personalization&quot;</span></span></td>
<td><span data-ttu-id="d2e54-123">&quot;Aspetto e temi&quot;</span><span class="sxs-lookup"><span data-stu-id="d2e54-123">&quot;Appearance and Themes&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2e54-124">2</span><span class="sxs-lookup"><span data-stu-id="d2e54-124">2</span></span></td>
<td><span data-ttu-id="d2e54-125">&quot;Hardware e audio&quot;</span><span class="sxs-lookup"><span data-stu-id="d2e54-125">&quot;Hardware and Sound&quot;</span></span></td>
<td><span data-ttu-id="d2e54-126">&quot;Hardware e audio&quot;</span><span class="sxs-lookup"><span data-stu-id="d2e54-126">&quot;Hardware and Sound&quot;</span></span></td>
<td><span data-ttu-id="d2e54-127">&quot;Stampanti e altro hardware&quot;</span><span class="sxs-lookup"><span data-stu-id="d2e54-127">&quot;Printers and Other Hardware&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2e54-128">3</span><span class="sxs-lookup"><span data-stu-id="d2e54-128">3</span></span></td>
<td><span data-ttu-id="d2e54-129">&quot;Rete e Internet&quot;</span><span class="sxs-lookup"><span data-stu-id="d2e54-129">&quot;Network and Internet&quot;</span></span></td>
<td><span data-ttu-id="d2e54-130">&quot;Rete e Internet&quot;</span><span class="sxs-lookup"><span data-stu-id="d2e54-130">&quot;Network and Internet&quot;</span></span></td>
<td><span data-ttu-id="d2e54-131">&quot;Connessioni di rete e Internet&quot;</span><span class="sxs-lookup"><span data-stu-id="d2e54-131">&quot;Network and Internet Connections&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2e54-132">4</span><span class="sxs-lookup"><span data-stu-id="d2e54-132">4</span></span></td>
<td><span data-ttu-id="d2e54-133">Non più utilizzata.</span><span class="sxs-lookup"><span data-stu-id="d2e54-133">No longer used.</span></span> <span data-ttu-id="d2e54-134">Tutti gli elementi che si aggiungono solo alla categoria 4 vengono visualizzati nella categoria 2 (hardware e suono).</span><span class="sxs-lookup"><span data-stu-id="d2e54-134">Any item that adds itself only to category 4 appears in category 2 (Hardware and Sound).</span></span></td>
<td><span data-ttu-id="d2e54-135">Non più utilizzata.</span><span class="sxs-lookup"><span data-stu-id="d2e54-135">No longer used.</span></span> <span data-ttu-id="d2e54-136">Tutti gli elementi che si aggiungono solo alla categoria 4 vengono visualizzati nella categoria 2 (hardware e suono).</span><span class="sxs-lookup"><span data-stu-id="d2e54-136">Any item that adds itself only to category 4 appears in category 2 (Hardware and Sound).</span></span></td>
<td><span data-ttu-id="d2e54-137">&quot;Suoni, sintesi vocale e dispositivi audio&quot;</span><span class="sxs-lookup"><span data-stu-id="d2e54-137">&quot;Sounds, Speech, and Audio Devices&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2e54-138">5</span><span class="sxs-lookup"><span data-stu-id="d2e54-138">5</span></span></td>
<td><span data-ttu-id="d2e54-139">&quot;Sistema e sicurezza&quot;</span><span class="sxs-lookup"><span data-stu-id="d2e54-139">&quot;System and Security&quot;</span></span></td>
<td><span data-ttu-id="d2e54-140">&quot;Sistema e manutenzione&quot;</span><span class="sxs-lookup"><span data-stu-id="d2e54-140">&quot;System and Maintenance&quot;</span></span></td>
<td><span data-ttu-id="d2e54-141">&quot;Prestazioni e manutenzione&quot;</span><span class="sxs-lookup"><span data-stu-id="d2e54-141">&quot;Performance and Maintenance&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2e54-142">6</span><span class="sxs-lookup"><span data-stu-id="d2e54-142">6</span></span></td>
<td><span data-ttu-id="d2e54-143">&quot;Clock, lingua e area&quot;</span><span class="sxs-lookup"><span data-stu-id="d2e54-143">&quot;Clock, Language, and Region&quot;</span></span></td>
<td><span data-ttu-id="d2e54-144">&quot;Clock, lingua e area&quot;</span><span class="sxs-lookup"><span data-stu-id="d2e54-144">&quot;Clock, Language, and Region&quot;</span></span></td>
<td><span data-ttu-id="d2e54-145">&quot;Data, ora, lingua e opzioni internazionali&quot;</span><span class="sxs-lookup"><span data-stu-id="d2e54-145">&quot;Date, Time, Language, and Regional Options&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2e54-146">7</span><span class="sxs-lookup"><span data-stu-id="d2e54-146">7</span></span></td>
<td><span data-ttu-id="d2e54-147">&quot;Ease of Access&quot;</span><span class="sxs-lookup"><span data-stu-id="d2e54-147">&quot;Ease of Access&quot;</span></span></td>
<td><span data-ttu-id="d2e54-148">&quot;Ease of Access&quot;</span><span class="sxs-lookup"><span data-stu-id="d2e54-148">&quot;Ease of Access&quot;</span></span></td>
<td><span data-ttu-id="d2e54-149">&quot;Opzioni di accessibilità&quot;</span><span class="sxs-lookup"><span data-stu-id="d2e54-149">&quot;Accessibility Options&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2e54-150">8</span><span class="sxs-lookup"><span data-stu-id="d2e54-150">8</span></span></td>
<td><span data-ttu-id="d2e54-151">&quot;Programs&quot;</span><span class="sxs-lookup"><span data-stu-id="d2e54-151">&quot;Programs&quot;</span></span></td>
<td><span data-ttu-id="d2e54-152">&quot;Programs&quot;</span><span class="sxs-lookup"><span data-stu-id="d2e54-152">&quot;Programs&quot;</span></span></td>
<td><span data-ttu-id="d2e54-153">&quot;Installazione applicazioni&quot;</span><span class="sxs-lookup"><span data-stu-id="d2e54-153">&quot;Add or Remove Programs&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2e54-154">9</span><span class="sxs-lookup"><span data-stu-id="d2e54-154">9</span></span></td>
<td><span data-ttu-id="d2e54-155">&quot;Account utente&quot;</span><span class="sxs-lookup"><span data-stu-id="d2e54-155">&quot;User Accounts&quot;</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="d2e54-156">Quando non si è connessi a un dominio, questo è denominato &quot; account utente e sicurezza della famiglia &quot; .</span><span class="sxs-lookup"><span data-stu-id="d2e54-156">When not connected to a domain, this is called &quot;User Accounts and Family Safety&quot;.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="d2e54-157">&quot;Account utente&quot;</span><span class="sxs-lookup"><span data-stu-id="d2e54-157">&quot;User Accounts&quot;</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="d2e54-158">Quando non si è connessi a un dominio, questo è denominato &quot; account utente e sicurezza della famiglia &quot; .</span><span class="sxs-lookup"><span data-stu-id="d2e54-158">When not connected to a domain, this is called &quot;User Accounts and Family Safety&quot;.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="d2e54-159">&quot;Account utente&quot;</span><span class="sxs-lookup"><span data-stu-id="d2e54-159">&quot;User Accounts&quot;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2e54-160">10</span><span class="sxs-lookup"><span data-stu-id="d2e54-160">10</span></span></td>
<td><span data-ttu-id="d2e54-161">Non più utilizzata.</span><span class="sxs-lookup"><span data-stu-id="d2e54-161">No longer used.</span></span> <span data-ttu-id="d2e54-162">Gli elementi registrati in questa categoria vengono visualizzati nella categoria 5 (sistema e sicurezza).</span><span class="sxs-lookup"><span data-stu-id="d2e54-162">Items registered in this category appear in category 5 (System and Security).</span></span></td>
<td><span data-ttu-id="d2e54-163">&quot;Sicurezza&quot;</span><span class="sxs-lookup"><span data-stu-id="d2e54-163">&quot;Security&quot;</span></span></td>
<td><span data-ttu-id="d2e54-164">&quot;Centro sicurezza&quot;</span><span class="sxs-lookup"><span data-stu-id="d2e54-164">&quot;Security Center&quot;</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="d2e54-165">Disponibile solo in Windows XP Service Pack 2 (SP2) o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="d2e54-165">Available only in Windows XP Service Pack 2 (SP2) or later.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2e54-166">11</span><span class="sxs-lookup"><span data-stu-id="d2e54-166">11</span></span></td>
<td><span data-ttu-id="d2e54-167">Non più utilizzata.</span><span class="sxs-lookup"><span data-stu-id="d2e54-167">No longer used.</span></span> <span data-ttu-id="d2e54-168">Gli elementi registrati in questa categoria vengono visualizzati nella categoria 0 (tutti gli elementi del pannello di controllo).</span><span class="sxs-lookup"><span data-stu-id="d2e54-168">Items registered in this category appear in category 0 (All Control Panel Items).</span></span></td>
<td><span data-ttu-id="d2e54-169">&quot;PC portatile&quot;</span><span class="sxs-lookup"><span data-stu-id="d2e54-169">&quot;Mobile PC&quot;</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="d2e54-170">Questa categoria è visibile solo nei PC portatili.</span><span class="sxs-lookup"><span data-stu-id="d2e54-170">This category is only visible on mobile PCs.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="d2e54-171">Non usato.</span><span class="sxs-lookup"><span data-stu-id="d2e54-171">Not used.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d2e54-172">In Windows XP le categorie **aggiungere o rimuovere programmi** e **account utente** funzionano in modo diverso rispetto ad altre categorie nel pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="d2e54-172">In Windows XP, the categories **Add or Remove Programs** and **User Accounts** work somewhat differently from other categories in Control Panel.</span></span> <span data-ttu-id="d2e54-173">Quando uno o più elementi vengono aggiunti a una di queste due categorie, il collegamento associato nel pannello di controllo apre una pagina di categoria.</span><span class="sxs-lookup"><span data-stu-id="d2e54-173">When one or more items are added to one of these two categories, the associated link in Control Panel opens a category page.</span></span> <span data-ttu-id="d2e54-174">Gli elementi registrati vengono visualizzati nella parte inferiore della pagina sotto l'intestazione "oppure selezionare un'icona del pannello di controllo".</span><span class="sxs-lookup"><span data-stu-id="d2e54-174">The registered items appear in the lower portion of the page under the heading "or Pick a Control Panel icon".</span></span> <span data-ttu-id="d2e54-175">Quando non viene registrato alcun elemento per una di queste categorie, il collegamento associato nel pannello di controllo richiama direttamente l'elemento Windows standard per quella categoria.</span><span class="sxs-lookup"><span data-stu-id="d2e54-175">When no items are registered for one of these categories, the associated link in Control Panel directly invokes the standard Windows item for that category.</span></span> <span data-ttu-id="d2e54-176">In Windows Vista e versioni successive, la categoria **programmi** e la categoria **account utente** non dispongono di questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="d2e54-176">In Windows Vista and later, the **Programs** category and the **User Accounts** category do not have this property.</span></span>

<span data-ttu-id="d2e54-177">La categoria **Centro sicurezza** , disponibile solo in Windows XP SP2, è anche in qualche modo non standard.</span><span class="sxs-lookup"><span data-stu-id="d2e54-177">The **Security Center** category, available only in Windows XP SP2, is also somewhat non-standard.</span></span> <span data-ttu-id="d2e54-178">Se si fa clic su questa categoria, viene visualizzata la pagina **Centro sicurezza** in una nuova finestra.</span><span class="sxs-lookup"><span data-stu-id="d2e54-178">Clicking this category opens the **Security Center** page in a new window.</span></span> <span data-ttu-id="d2e54-179">Gli elementi registrati per il **Centro sicurezza** vengono visualizzati nella parte inferiore della pagina sotto l'intestazione **Gestisci impostazioni di sicurezza per:**.</span><span class="sxs-lookup"><span data-stu-id="d2e54-179">Items registered for **Security Center** appear in the lower portion of that page under the heading **Manage security settings for:**.</span></span> <span data-ttu-id="d2e54-180">Fare clic su un'icona per aprire l'elemento del pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="d2e54-180">Clicking an icon opens the Control Panel item.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d2e54-181">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d2e54-181">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2e54-182">Elementi del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="d2e54-182">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="d2e54-183">Linee guida sull'esperienza utente</span><span class="sxs-lookup"><span data-stu-id="d2e54-183">User Experience Guidelines</span></span>](user-experience-guidelines.md)
</dt> <dt>

[<span data-ttu-id="d2e54-184">Registrazione degli elementi del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="d2e54-184">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="d2e54-185">Uso di CPLApplet</span><span class="sxs-lookup"><span data-stu-id="d2e54-185">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="d2e54-186">Elaborazione del messaggio del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="d2e54-186">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="d2e54-187">Esecuzione degli elementi del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="d2e54-187">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="d2e54-188">Estensione degli elementi del pannello di controllo di sistema</span><span class="sxs-lookup"><span data-stu-id="d2e54-188">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="d2e54-189">Creazione di collegamenti alle attività ricercabili per un elemento del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="d2e54-189">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
</dt> <dt>

[<span data-ttu-id="d2e54-190">Accesso al pannello di controllo in modalità provvisoria in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d2e54-190">Accessing the Control Panel in Safe Mode under Windows Vista</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 




