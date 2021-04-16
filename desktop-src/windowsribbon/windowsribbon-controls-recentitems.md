---
title: Elementi recenti
description: L'elenco degli elementi recenti è un riquadro del menu dell'applicazione in cui vengono visualizzati gli elementi utilizzati più di recente per un'applicazione.
ms.assetid: fdead358-d303-46de-9f8e-6fc2832d8e94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f78c01fc4d6cc830eba644f7dcf22b6fb03e82
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104555949"
---
# <a name="recent-items"></a><span data-ttu-id="ec29e-103">Elementi recenti</span><span class="sxs-lookup"><span data-stu-id="ec29e-103">Recent Items</span></span>

<span data-ttu-id="ec29e-104">L'elenco degli elementi recenti è un riquadro del [menu dell'applicazione](windowsribbon-controls-applicationmenu.md) in cui vengono visualizzati gli elementi utilizzati più di recente per un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ec29e-104">The Recent Items list is a pane in the [Application Menu](windowsribbon-controls-applicationmenu.md) that displays the most recently used (MRU) items for an application.</span></span>

-   [<span data-ttu-id="ec29e-105">Dettagli</span><span class="sxs-lookup"><span data-stu-id="ec29e-105">Details</span></span>](#details)
-   [<span data-ttu-id="ec29e-106">Proprietà degli elementi recenti</span><span class="sxs-lookup"><span data-stu-id="ec29e-106">Recent Items Properties</span></span>](#recent-items-properties)
-   [<span data-ttu-id="ec29e-107">Osservazioni:</span><span class="sxs-lookup"><span data-stu-id="ec29e-107">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="ec29e-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ec29e-108">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="ec29e-109">Dettagli</span><span class="sxs-lookup"><span data-stu-id="ec29e-109">Details</span></span>

<span data-ttu-id="ec29e-110">Lo screenshot seguente illustra un elenco di elementi recenti da WordPad per Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ec29e-110">The following screen shot illustrates a Recent Items list from WordPad for Windows 7).</span></span>

![screenshot dell'elenco di elementi recenti nella barra multifunzione di Microsoft Paint.](images/controls/recentitems.png)

<span data-ttu-id="ec29e-112">Il [menu dell'applicazione](windowsribbon-controls-applicationmenu.md) può contenere al massimo un elenco [**ApplicationMenu. RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) , rappresentato da un elemento **ApplicationMenu. RecentItems** , per la visualizzazione di documenti recenti, immagini, filmati e altri progetti su cui un utente sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="ec29e-112">The [Application Menu](windowsribbon-controls-applicationmenu.md) can have at most one [**ApplicationMenu.RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) list, represented by an **ApplicationMenu.RecentItems** element, for displaying recent documents, pictures, movies, and other projects a user has been working on.</span></span> <span data-ttu-id="ec29e-113">Il numero di elementi elencati è compreso tra 0 e il numero massimo specificato nel markup e il valore predefinito è dieci.</span><span class="sxs-lookup"><span data-stu-id="ec29e-113">The number of listed items ranges from zero to the maximum number specified in markup, with a default value of ten.</span></span> <span data-ttu-id="ec29e-114">Gli elementi recenti vengono visualizzati come un elenco numerato di stringhe che indicano i nomi di file.</span><span class="sxs-lookup"><span data-stu-id="ec29e-114">The recent items are displayed as a numbered list of strings indicating file names.</span></span> <span data-ttu-id="ec29e-115">È consigliabile usare la proprietà [**Command. LabelDescription**](windowsribbon-element-command-labeldescription.md) per fornire il percorso completo per il percorso del file, come illustrato nella schermata seguente.</span><span class="sxs-lookup"><span data-stu-id="ec29e-115">It is recommended that the [**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md) property be used to give the full path for the file location, as shown in the following screen shot .</span></span>

![Screenshot di un elenco di elementi recenti nel menu di un'applicazione.](images/overviews/applicationmenu-menurecentitems.png)

<span data-ttu-id="ec29e-117">L'elemento [**RecentItems**](windowsribbon-element-recentitems.md) ha un attributo *EnablePinning* che, se impostato su `true` , Visualizza un'icona a forma di puntina a destra di ogni elemento nell'elenco, come illustrato nella schermata seguente.</span><span class="sxs-lookup"><span data-stu-id="ec29e-117">The [**RecentItems**](windowsribbon-element-recentitems.md) element has an *EnablePinning* attribute that, if set to `true`, displays a pin icon to the right of each item in the list, as shown in the following screen shot.</span></span>

> [!Note]  
> <span data-ttu-id="ec29e-118">Il blocco è abilitato per impostazione predefinita se l'attributo *EnablePinning* non è specificato.</span><span class="sxs-lookup"><span data-stu-id="ec29e-118">Pinning is enabled by default if the *EnablePinning* attribute is not specified.</span></span>

 

![screenshot dell'aggiunta di elementi recenti nel menu di un'applicazione.](images/overviews/applicationmenu-menurecentitemspinned.png)

<span data-ttu-id="ec29e-120">L'algoritmo di blocco ha lo scopo di evitare che gli elementi cadano nell'elenco **degli elementi recenti** .</span><span class="sxs-lookup"><span data-stu-id="ec29e-120">The pinning algorithm is intended to keep items from falling off the **Recent items** list.</span></span> <span data-ttu-id="ec29e-121">L'algoritmo produce il comportamento seguente:</span><span class="sxs-lookup"><span data-stu-id="ec29e-121">The algorithm produces the following behavior:</span></span>

-   <span data-ttu-id="ec29e-122">Un nuovo elemento viene sempre aggiunto all'inizio dell'elenco di **elementi recenti** .</span><span class="sxs-lookup"><span data-stu-id="ec29e-122">A new item is always added at the top of the **Recent items** list.</span></span>
-   <span data-ttu-id="ec29e-123">Gli elementi vengono spostati nell'elenco nel tempo.</span><span class="sxs-lookup"><span data-stu-id="ec29e-123">Items will move down in the list over time.</span></span> <span data-ttu-id="ec29e-124">Quando l'elenco è pieno (raggiunge il numero massimo di elementi specificato nel markup), gli elementi meno recenti rientrano nella parte inferiore dell'elenco man volta che vengono aggiunti nuovi elementi all'inizio dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="ec29e-124">Once the list is full (reaches the maximum number of items specified in markup), older items fall off the bottom of the list as new items are added to the top of the list.</span></span>
-   <span data-ttu-id="ec29e-125">Se un elemento è già presente nell'elenco, ma viene nuovamente eseguito l'accesso, viene spostato di nuovo nella parte superiore dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="ec29e-125">If an item already appears somewhere in the list but is accessed again, it moves back to the top of the list.</span></span>
-   <span data-ttu-id="ec29e-126">Se un elemento è bloccato, verrà comunque spostata verso il basso nell'elenco, ma non verrà escluso.</span><span class="sxs-lookup"><span data-stu-id="ec29e-126">If an item is pinned, it will still travel down the list, but it will not fall off the bottom.</span></span> <span data-ttu-id="ec29e-127">Al contrario, una volta completato l'elenco, il primo elemento rimosso sopra l'elemento bloccato verrà disattivato quando viene aggiunto un nuovo elemento all'elenco.</span><span class="sxs-lookup"><span data-stu-id="ec29e-127">Instead, once the list is full, the first unpinned item above the pinned item will fall off when a new item is added to the list.</span></span>
-   <span data-ttu-id="ec29e-128">Se il numero di elementi bloccati raggiunge il numero massimo di elementi, nessun nuovo elemento verrà aggiunto all'elenco fino a quando non viene sbloccato un elemento.</span><span class="sxs-lookup"><span data-stu-id="ec29e-128">If the number of pinned items ever reaches the maximum number of items, then no new items will get added to the list until an item is unpinned.</span></span>

## <a name="recent-items-properties"></a><span data-ttu-id="ec29e-129">Proprietà degli elementi recenti</span><span class="sxs-lookup"><span data-stu-id="ec29e-129">Recent Items Properties</span></span>

<span data-ttu-id="ec29e-130">Il Framework della barra multifunzione definisce una raccolta di [chiavi di proprietà](windowsribbon-reference-properties.md) per il controllo degli elementi recenti.</span><span class="sxs-lookup"><span data-stu-id="ec29e-130">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Recent Items control.</span></span>

<span data-ttu-id="ec29e-131">In genere, una proprietà degli elementi recenti viene aggiornata nell'interfaccia utente della barra multifunzione invalidando il comando associato al controllo tramite una chiamata al metodo [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="ec29e-131">Typically, a Recent Items property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="ec29e-132">L'evento di invalidamento viene gestito e gli aggiornamenti delle proprietà definiti dal metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="ec29e-132">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="ec29e-133">Il metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) non viene eseguito e l'applicazione ha sottoposto a query un valore aggiornato della proprietà, fino a quando la proprietà non è richiesta dal Framework.</span><span class="sxs-lookup"><span data-stu-id="ec29e-133">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="ec29e-134">Ad esempio, quando viene attivata una scheda e viene visualizzato un controllo nell'interfaccia utente della barra multifunzione o quando viene visualizzata una descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="ec29e-134">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="ec29e-135">In alcuni casi, una proprietà può essere recuperata tramite il metodo [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e impostata con il metodo [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="ec29e-135">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="ec29e-136">Nella tabella seguente sono elencate le chiavi di proprietà associate al controllo elementi recenti.</span><span class="sxs-lookup"><span data-stu-id="ec29e-136">The following table lists the property keys that are associated with the Recent Items control.</span></span>



| <span data-ttu-id="ec29e-137">Chiave della proprietà</span><span class="sxs-lookup"><span data-stu-id="ec29e-137">Property Key</span></span>                                                                       | <span data-ttu-id="ec29e-138">Note</span><span class="sxs-lookup"><span data-stu-id="ec29e-138">Notes</span></span>                                     |
|------------------------------------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="ec29e-139">Suggerimento tasto di interfaccia utente \_ pkey \_</span><span class="sxs-lookup"><span data-stu-id="ec29e-139">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)           | <span data-ttu-id="ec29e-140">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="ec29e-140">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="ec29e-141">Interfaccia utente \_ pkey \_ RecentItems</span><span class="sxs-lookup"><span data-stu-id="ec29e-141">UI\_PKEY\_RecentItems</span></span>](windowsribbon-reference-properties-uipkey-recentitems.md) | <span data-ttu-id="ec29e-142">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="ec29e-142">Can only be updated through invalidation.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ec29e-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="ec29e-143">Remarks</span></span>

<span data-ttu-id="ec29e-144">Il metodo [IApplicationDocumentLists:: GetList](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationdocumentlists-getlist) può essere usato per recuperare l'elenco di Windows Shell MRU per l'applicazione Ribbon.</span><span class="sxs-lookup"><span data-stu-id="ec29e-144">The [IApplicationDocumentLists::GetList](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationdocumentlists-getlist) method can be used to retrieve the Windows Shell MRU list for the Ribbon application.</span></span> <span data-ttu-id="ec29e-145">L'oggetto recuperato da questo metodo può quindi essere utilizzato dall'applicazione per creare i dati richiesti dal framework della barra multifunzione per popolare l'elenco di **elementi recenti** del [menu dell'applicazione](windowsribbon-controls-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="ec29e-145">The object retrieved by this method can then be used by the application to create the data required by the Ribbon framework to populate the **Recent items** list of the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>

> [!Note]  
> <span data-ttu-id="ec29e-146">Quando si usa questo metodo, *ListType* deve avere il valore `ADLT_RECENT` .</span><span class="sxs-lookup"><span data-stu-id="ec29e-146">When using this method, *listtype* should have the value `ADLT_RECENT`.</span></span>

 

<span data-ttu-id="ec29e-147">Per un esempio di come implementare un elenco di elementi MRU in un'applicazione di Framework della barra multifunzione, vedere l' [esempio HTMLEditRibbon](windowsribbon-htmleditribbonsample.md).</span><span class="sxs-lookup"><span data-stu-id="ec29e-147">For an example of how to implement an MRU items list in a Ribbon framework application, see the [HTMLEditRibbon Sample](windowsribbon-htmleditribbonsample.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ec29e-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ec29e-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec29e-149">Libreria di controlli Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="ec29e-149">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="ec29e-150">**Elemento di markup elementi recenti**</span><span class="sxs-lookup"><span data-stu-id="ec29e-150">**Recent items markup element**</span></span>](windowsribbon-element-recentitems.md)
</dt> </dl>

 

 