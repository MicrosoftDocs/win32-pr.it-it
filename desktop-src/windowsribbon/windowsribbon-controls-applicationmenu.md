---
title: Menu applicazione
description: Il menu dell'applicazione è il menu principale di un'applicazione che implementa il Framework della barra multifunzione di Windows.
ms.assetid: 5be93a5b-277b-44c1-be24-a0598a140bfc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e99f57045daa35149e5fa074cb59e2f538c589b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872537"
---
# <a name="application-menu"></a><span data-ttu-id="d907b-103">Menu applicazione</span><span class="sxs-lookup"><span data-stu-id="d907b-103">Application Menu</span></span>

<span data-ttu-id="d907b-104">Il menu dell'applicazione è il menu principale di un'applicazione che implementa il Framework della barra multifunzione di Windows.</span><span class="sxs-lookup"><span data-stu-id="d907b-104">The Application Menu is the main menu for an application that implements the Windows Ribbon framework.</span></span>

-   [<span data-ttu-id="d907b-105">Introduzione</span><span class="sxs-lookup"><span data-stu-id="d907b-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="d907b-106">Componenti del menu dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="d907b-106">Components of the Application Menu</span></span>](#components-of-the-application-menu)
    -   [<span data-ttu-id="d907b-107">Menu dell'applicazione MenuGroup</span><span class="sxs-lookup"><span data-stu-id="d907b-107">Application Menu MenuGroup</span></span>](#application-menu-menugroup)
-   [<span data-ttu-id="d907b-108">Ridimensionamento del menu dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="d907b-108">Sizing the Application Menu</span></span>](#sizing-the-application-menu)
-   [<span data-ttu-id="d907b-109">Proprietà del menu applicazione</span><span class="sxs-lookup"><span data-stu-id="d907b-109">Application Menu Properties</span></span>](#application-menu-properties)
-   [<span data-ttu-id="d907b-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d907b-110">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="d907b-111">Introduzione</span><span class="sxs-lookup"><span data-stu-id="d907b-111">Introduction</span></span>

<span data-ttu-id="d907b-112">Il menu applicazione è costituito da un controllo pulsante a discesa che consente di visualizzare un menu che contiene i comandi che espongono le funzionalità correlate a un progetto completo, ad esempio un intero documento, un'immagine o un film.</span><span class="sxs-lookup"><span data-stu-id="d907b-112">The Application Menu is composed of a drop-down button control that displays a menu containing Commands that expose functionality related to a complete project, such as an entire document, picture, or movie.</span></span> <span data-ttu-id="d907b-113">Gli esempi includono i comandi **nuovi**, **Apri**, **Salva** ed **Esci** .</span><span class="sxs-lookup"><span data-stu-id="d907b-113">Examples include the **New**, **Open**, **Save**, and **Exit** Commands.</span></span>

<span data-ttu-id="d907b-114">Lo screenshot seguente illustra il menu dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d907b-114">The following screen shot illustrates the Application Menu.</span></span>

![screenshot del menu dell'applicazione e dell'elenco di elementi recenti della barra multifunzione di Paint per Windows 7.](images/controls/recentitems.png)

## <a name="components-of-the-application-menu"></a><span data-ttu-id="d907b-116">Componenti del menu dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="d907b-116">Components of the Application Menu</span></span>

<span data-ttu-id="d907b-117">Il menu dell'applicazione è un elemento obbligatorio in qualsiasi applicazione della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="d907b-117">The Application Menu is a mandatory element in any Ribbon application.</span></span> <span data-ttu-id="d907b-118">Il punto di ingresso nel menu dell'applicazione è un pulsante distinto visualizzato come primo elemento nella riga di [tabulazione](windowsribbon-controls-tab.md) , come illustrato nella schermata seguente.</span><span class="sxs-lookup"><span data-stu-id="d907b-118">The entry point into the Application Menu is a distinctive button that appears as the first item in the [Tab](windowsribbon-controls-tab.md) row, as shown in the following screen shot.</span></span>

> [!Note]  
> <span data-ttu-id="d907b-119">Windows 8 e versioni successive: l'immagine del pulsante di menu dell'applicazione è cambiata in etichetta: **file**.</span><span class="sxs-lookup"><span data-stu-id="d907b-119">Windows 8 and newer: Application Menu button image changed to label: **File**.</span></span> <span data-ttu-id="d907b-120">Si consiglia di non usare file come etichetta per le schede.</span><span class="sxs-lookup"><span data-stu-id="d907b-120">We recommend that you do not use File as the label for any of your own tabs.</span></span>

 

![screenshot del pulsante di menu dell'applicazione di WordPad per Windows 7.](images/overviews/applicationmenu-button.png)

<span data-ttu-id="d907b-122">Quando si fa clic su questo pulsante, viene visualizzato il menu completo visualizzato nello screenshot seguente (il menu dell'applicazione da WordPad per Windows 7).</span><span class="sxs-lookup"><span data-stu-id="d907b-122">When clicked, this button displays the rich menu that is shown in the following screen shot (the Application Menu from WordPad for Windows 7).</span></span>

![screenshot del menu di menu dell'applicazione di WordPad per Windows 7.](images/overviews/applicationmenu-menu.png)

> [!Note]  
> <span data-ttu-id="d907b-124">Non vi è alcun effetto sul set di schede quando si fa clic sul pulsante di menu dell'applicazione; lo stato attivo entra invece nel menu.</span><span class="sxs-lookup"><span data-stu-id="d907b-124">There is no impact on the tab set when the Application Menu button is clicked; instead, the focus enters the menu.</span></span>

 

<span data-ttu-id="d907b-125">Il menu dell'applicazione contiene due riquadri: un elenco di comandi rappresentati da uno o più elementi [**MenuGroup**](windowsribbon-element-menugroup.md) e un elenco di [elementi recenti](windowsribbon-controls-recentitems.md) rappresentato da un elemento [**ApplicationMenu. RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) .</span><span class="sxs-lookup"><span data-stu-id="d907b-125">The Application Menu contains two panes: a list of Commands represented by one or more [**MenuGroup**](windowsribbon-element-menugroup.md) elements, and a [Recent Items](windowsribbon-controls-recentitems.md) list represented by an [**ApplicationMenu.RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) element.</span></span>

### <a name="application-menu-menugroup"></a><span data-ttu-id="d907b-126">Menu dell'applicazione MenuGroup</span><span class="sxs-lookup"><span data-stu-id="d907b-126">Application Menu MenuGroup</span></span>

<span data-ttu-id="d907b-127">L'elemento [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) deve contenere almeno un elemento figlio [**MenuGroup**](windowsribbon-element-menugroup.md) che espone un elenco di comandi a livello di applicazione.</span><span class="sxs-lookup"><span data-stu-id="d907b-127">The [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) element must contain at least one [**MenuGroup**](windowsribbon-element-menugroup.md) child element that exposes a list of application-level commands.</span></span> <span data-ttu-id="d907b-128">Se vengono dichiarati più elementi **MenuGroup** , viene disegnata una linea di divisione tra i gruppi, come illustrato nella schermata seguente.</span><span class="sxs-lookup"><span data-stu-id="d907b-128">If multiple **MenuGroup** elements are declared, a divider line is drawn between the groups, as shown in the following screen shot.</span></span>

![screenshot del menu di un'applicazione MenuGroup.](images/overviews/applicationmenu-menugroup.png)

<span data-ttu-id="d907b-130">Di seguito è riportato un elenco di vincoli per un elemento [**MenuGroup**](windowsribbon-element-menugroup.md) di un menu dell'applicazione:</span><span class="sxs-lookup"><span data-stu-id="d907b-130">The following is a list of constraints for a [**MenuGroup**](windowsribbon-element-menugroup.md) element of an Application Menu:</span></span>

-   <span data-ttu-id="d907b-131">Tutti gli elementi [**MenuGroup**](windowsribbon-element-menugroup.md) devono essere dichiarati con un valore dell'attributo della *classe* `MajorItems` .</span><span class="sxs-lookup"><span data-stu-id="d907b-131">All [**MenuGroup**](windowsribbon-element-menugroup.md) items must be declared with a *Class* attribute value of `MajorItems`.</span></span>
-   <span data-ttu-id="d907b-132">Un menu applicazione  [**MenuGroup**](windowsribbon-element-menugroup.md) supporta solo i controlli [pulsante](windowsribbon-controls-button.md), [interruttore](windowsribbon-controls-togglebutton.md), pulsante a [discesa](windowsribbon-controls-dropdownbutton.md), pulsante di menu [combinato](windowsribbon-controls-splitbutton.md), [raccolta a discesa](windowsribbon-controls-dropdowngallery.md)e [raccolta pulsanti](windowsribbon-controls-splitbuttongallery.md) di menu combinato.</span><span class="sxs-lookup"><span data-stu-id="d907b-132">An Application Menu  [**MenuGroup**](windowsribbon-element-menugroup.md) supports only the [Button](windowsribbon-controls-button.md), [Toggle Button](windowsribbon-controls-togglebutton.md), [Drop-Down Button](windowsribbon-controls-dropdownbutton.md), [Split Button](windowsribbon-controls-splitbutton.md), [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md), and [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) controls.</span></span>
    > <span data-ttu-id="d907b-133">\[! Importante\]</span><span class="sxs-lookup"><span data-stu-id="d907b-133">\[!Important\]</span></span>  
    > <span data-ttu-id="d907b-134">Le raccolte di comandi sono l'unico tipo di raccolta supportato nel menu dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d907b-134">Command galleries are the only type of gallery that are supported in the Application Menu.</span></span> <span data-ttu-id="d907b-135">Per altre informazioni sui controlli della raccolta, vedere [uso delle raccolte](./ribbon-controls-galleries.md).</span><span class="sxs-lookup"><span data-stu-id="d907b-135">See [Working with Galleries](./ribbon-controls-galleries.md), for more information on gallery controls.</span></span>

     

<span data-ttu-id="d907b-136">Quando si usa un [pulsante](windowsribbon-controls-button.md) o un [interruttore](windowsribbon-controls-togglebutton.md) in un [**MenuGroup**](windowsribbon-element-menugroup.md), il valore di [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) viene visualizzato nel menu e i valori di [**Command. TooltipTitle**](windowsribbon-element-command-tooltiptitle.md) e [**Command. TooltipDescription**](windowsribbon-element-command-tooltipdescription.md) vengono visualizzati come descrizione comando, come illustrato nella schermata seguente.</span><span class="sxs-lookup"><span data-stu-id="d907b-136">When a [Button](windowsribbon-controls-button.md) or [Toggle Button](windowsribbon-controls-togglebutton.md) is used in a [**MenuGroup**](windowsribbon-element-menugroup.md), the value of [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) is displayed in the menu and the values of [**Command.TooltipTitle**](windowsribbon-element-command-tooltiptitle.md) and [**Command.TooltipDescription**](windowsribbon-element-command-tooltipdescription.md) are displayed as the tooltip, as shown in the following screen shot.</span></span>

![Screenshot di un controllo Button nel menu di un'applicazione.](images/overviews/applicationmenu-menubutton.png)

<span data-ttu-id="d907b-138">Quando si usa un [pulsante a discesa](windowsribbon-controls-dropdownbutton.md), un pulsante di menu [combinato](windowsribbon-controls-splitbutton.md), una raccolta a [discesa](windowsribbon-controls-dropdowngallery.md)o una raccolta di pulsanti di menu [combinato](windowsribbon-controls-splitbuttongallery.md) , la parte di menu viene visualizzata come un riquadro a comparsa che copre e nasconde il riquadro **elementi recenti** .</span><span class="sxs-lookup"><span data-stu-id="d907b-138">When a [Drop-Down Button](windowsribbon-controls-dropdownbutton.md), [Split Button](windowsribbon-controls-splitbutton.md), [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md), or [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) is used in the Application Menu, the menu portion is displayed as a flyout that covers and conceals the **Recent items** pane.</span></span>

<span data-ttu-id="d907b-139">Per i controlli pulsante di menu [combinato](windowsribbon-controls-splitbutton.md) e [pulsante a discesa](windowsribbon-controls-dropdownbutton.md) , il valore di [**Command. LabelDescription**](windowsribbon-element-command-labeldescription.md) viene visualizzato inline nel menu a comparsa per aiutare gli utenti a individuare la funzionalità del comando.</span><span class="sxs-lookup"><span data-stu-id="d907b-139">For [Split Button](windowsribbon-controls-splitbutton.md) and [Drop-Down Button](windowsribbon-controls-dropdownbutton.md) controls, the value of [**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md) is shown inline in the flyout menu to visually assist users with discovering the Command functionality.</span></span> <span data-ttu-id="d907b-140">Il valore visualizzato di **Command. LabelDescription** viene suddiviso a livello di codice su un intervallo a due righe e viene effettuato un tentativo di adattare il valore esattamente sul riquadro **elementi recenti** sotto.</span><span class="sxs-lookup"><span data-stu-id="d907b-140">The displayed value of **Command.LabelDescription** is programmatically broken over a two-line span, and an attempt is made to fit the value exactly over the **Recent items** pane beneath.</span></span> <span data-ttu-id="d907b-141">Se il valore **Command. LabelDescription** non è adatto, il riquadro a comparsa si espanderà in modo da includere il valore più lungo del [**comando. Comment**](windowsribbon-element-command-comment.md) in [**MenuGroup**](windowsribbon-element-menugroup.md).</span><span class="sxs-lookup"><span data-stu-id="d907b-141">If the **Command.LabelDescription** value does not fit, the flyout will expand to accommodate the longest [**Command.Comment**](windowsribbon-element-command-comment.md) value in the [**MenuGroup**](windowsribbon-element-menugroup.md).</span></span>

<span data-ttu-id="d907b-142">Lo screenshot seguente illustra questi comportamenti in un riquadro a comparsa di un [pulsante di menu combinato](windowsribbon-controls-splitbutton.md) .</span><span class="sxs-lookup"><span data-stu-id="d907b-142">The following screen shot illustrates these behaviors in a [Split Button](windowsribbon-controls-splitbutton.md) flyout.</span></span>

![Screenshot di un riquadro a comparsa di un controllo elenco nel menu di un'applicazione.](images/overviews/applicationmenu-menuflyout.png)

<span data-ttu-id="d907b-144">Con una raccolta a [discesa](windowsribbon-controls-dropdowngallery.md) e una [raccolta di pulsanti di suddivisione](windowsribbon-controls-splitbuttongallery.md), vengono visualizzate solo un'etichetta e un'immagine.</span><span class="sxs-lookup"><span data-stu-id="d907b-144">With a [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md) and a [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md), only a label and an image are shown.</span></span>

## <a name="sizing-the-application-menu"></a><span data-ttu-id="d907b-145">Ridimensionamento del menu dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="d907b-145">Sizing the Application Menu</span></span>

<span data-ttu-id="d907b-146">Il dimensionamento del menu applicazione è gestito dal framework della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="d907b-146">Sizing of the Application Menu is handled by the Ribbon framework.</span></span> <span data-ttu-id="d907b-147">Se vengono fornite stringhe molto lunghe per il valore di [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) o [**Command. LabelDescription**](windowsribbon-element-command-labeldescription.md)oppure viene utilizzato un lungo elenco di comandi, il menu ne modificherà le dimensioni per adattarlo al contenuto.</span><span class="sxs-lookup"><span data-stu-id="d907b-147">If very long strings are supplied for the value of [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) or [**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md), or a long list of Commands is used, the menu will adjust its size to accommodate the contents.</span></span> <span data-ttu-id="d907b-148">Alcune forme di regolazione includono l'espansione delle dimensioni dei riquadri riquadri a comparsa o menu e l'aggiunta di visualizzatori di Pan quando è necessario lo scorrimento.</span><span class="sxs-lookup"><span data-stu-id="d907b-148">Some forms of adjustment include expanding the size of flyouts or menu panes, and adding pan viewers when scrolling is required.</span></span>

## <a name="application-menu-properties"></a><span data-ttu-id="d907b-149">Proprietà del menu applicazione</span><span class="sxs-lookup"><span data-stu-id="d907b-149">Application Menu Properties</span></span>

<span data-ttu-id="d907b-150">Il Framework della barra multifunzione definisce una raccolta di [chiavi di proprietà](windowsribbon-reference-properties.md) per il controllo menu applicazione.</span><span class="sxs-lookup"><span data-stu-id="d907b-150">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Application Menu control.</span></span>

<span data-ttu-id="d907b-151">In genere, una proprietà del menu applicazione viene aggiornata nell'interfaccia utente della barra multifunzione invalidando il comando associato al controllo tramite una chiamata al metodo [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="d907b-151">Typically, an Application Menu property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="d907b-152">L'evento di invalidamento viene gestito e gli aggiornamenti delle proprietà vengono definiti dal metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="d907b-152">The invalidation event is handled and the property updates are defined by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="d907b-153">Il metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) non viene eseguito e per l'applicazione non viene eseguita una query per ottenere un valore di proprietà aggiornato fino a quando la proprietà non è richiesta dal Framework.</span><span class="sxs-lookup"><span data-stu-id="d907b-153">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed and the application is not queried for an updated property value until the property is required by the framework.</span></span> <span data-ttu-id="d907b-154">Il Framework, ad esempio, richiede la proprietà quando viene attivata una scheda e viene visualizzato un controllo nell'interfaccia utente della barra multifunzione o quando viene visualizzata una descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="d907b-154">For example, the framework requires the property when a tab is activated and a control is revealed in the ribbon UI, or when a tooltip is displayed.</span></span>



| <span data-ttu-id="d907b-155">Chiave della proprietà</span><span class="sxs-lookup"><span data-stu-id="d907b-155">Property key</span></span>                                                                                     | <span data-ttu-id="d907b-156">Note</span><span class="sxs-lookup"><span data-stu-id="d907b-156">Notes</span></span>                                     |
|--------------------------------------------------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="d907b-157">Interfaccia utente \_ pkey \_ TooltipDescription</span><span class="sxs-lookup"><span data-stu-id="d907b-157">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | <span data-ttu-id="d907b-158">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="d907b-158">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="d907b-159">Interfaccia utente \_ pkey \_ TooltipTitle</span><span class="sxs-lookup"><span data-stu-id="d907b-159">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | <span data-ttu-id="d907b-160">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="d907b-160">Can only be updated through invalidation.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d907b-161">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d907b-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d907b-162">Libreria di controlli Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="d907b-162">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="d907b-163">**Elemento di markup ApplicationMenu**</span><span class="sxs-lookup"><span data-stu-id="d907b-163">**ApplicationMenu markup element**</span></span>](windowsribbon-element-applicationmenu.md)
</dt> </dl>

 

 