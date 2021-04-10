---
title: Gruppo di menu
description: Il gruppo di menu Organizza i comandi e i controlli correlati all'interno di un menu o di una barra degli strumenti.
ms.assetid: 5454f2a3-275b-47f4-ae97-d10dd12da5ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9862e78cbedf84b92c7540bec4de58288af5c9ef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963350"
---
# <a name="menu-group"></a><span data-ttu-id="42da1-103">Gruppo di menu</span><span class="sxs-lookup"><span data-stu-id="42da1-103">Menu Group</span></span>

<span data-ttu-id="42da1-104">Il gruppo di menu Organizza i comandi e i controlli correlati all'interno di un menu o di una barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="42da1-104">The Menu Group organizes related Commands and controls within a menu or toolbar.</span></span>

-   [<span data-ttu-id="42da1-105">Introduzione</span><span class="sxs-lookup"><span data-stu-id="42da1-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="42da1-106">Proprietà del gruppo di menu</span><span class="sxs-lookup"><span data-stu-id="42da1-106">Menu Group Properties</span></span>](#menu-group-properties)
-   [<span data-ttu-id="42da1-107">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="42da1-107">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="42da1-108">Introduzione</span><span class="sxs-lookup"><span data-stu-id="42da1-108">Introduction</span></span>

<span data-ttu-id="42da1-109">Il controllo gruppo di menu, esposto tramite l'elemento di markup [**MenuGroup**](windowsribbon-element-menugroup.md) , è un contenitore logico per gruppi di elementi o comandi nei controlli basati su menu, inclusa la mini-barra degli strumenti [popup del contesto](windowsribbon-controls-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="42da1-109">The Menu Group control, exposed through the [**MenuGroup**](windowsribbon-element-menugroup.md) markup element, is a logical container for groups of items or Commands in menu-based controls, including the [Context Popup](windowsribbon-controls-contextpopup.md) Mini-Toolbar.</span></span>

<span data-ttu-id="42da1-110">È possibile specificare un'etichetta per un gruppo di menu tramite l'attributo *LabelTitle* o la proprietà [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) di una dichiarazione di comando associata.</span><span class="sxs-lookup"><span data-stu-id="42da1-110">A label can be specified for a Menu Group through the *LabelTitle* attribute or [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) property of an associated Command declaration.</span></span> <span data-ttu-id="42da1-111">Il valore assegnato a *LabelTitle* viene sottoposto a rendering come intestazione di categoria.</span><span class="sxs-lookup"><span data-stu-id="42da1-111">The value assigned to *LabelTitle* is rendered as a category header.</span></span>

<span data-ttu-id="42da1-112">Nell'esempio seguente viene illustrato il markup del comando per un controllo pulsante di menu [combinato](windowsribbon-controls-splitbutton.md) che include due dichiarazioni di comando del gruppo di menu.</span><span class="sxs-lookup"><span data-stu-id="42da1-112">The following example demonstrates the Command markup for a [Split Button](windowsribbon-controls-splitbutton.md) control that includes two Menu Group Command declarations.</span></span>


```XML
<!-- SplitButton -->
<Command Name="cmdSplitButtonGroup"
         Symbol="cmdSplitButtonGroup"
         Comment="SplitButton Group"
         LabelTitle="SplitButton"/>
<Command Name="cmdSplitButton"
         Symbol="cmdSplitButton"
         Comment="SplitButton"
         LabelTitle="SplitButton"/>
<Command Name="cmdSBButtonItem"
         Symbol="cmdSBButtonItem"
         Comment="SBButtonItem"
         LabelTitle="SB ButtonItem"/>
<Command Name="cmdSBButton1"
         Symbol="cmdSBButton1"
         Comment="SBButton1"
         LabelTitle="SB Button">
  <Command.LargeImages>
    <Image Source="res/copyL_32.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/copyS_16.bmp"/>
  </Command.SmallImages>
  <Command.LargeHighContrastImages>
    <Image Source="res/copyLHC_32.bmp"/>
  </Command.LargeHighContrastImages>
  <Command.SmallHighContrastImages>
    <Image Source="res/copySHC_16.bmp"/>
  </Command.SmallHighContrastImages>
</Command>
<Command Name="cmdSBMajorItems"
         Comment="Major Items Category"
         LabelTitle="Major Items"/>
<Command Name="cmdSBStandardItems"
         Comment="Standard Items Category"
         LabelTitle="Standard Items"/>
```



<span data-ttu-id="42da1-113">Nell'esempio seguente viene illustrato il markup necessario per un elemento [**SplitButton**](windowsribbon-element-splitbutton.md) con tre dichiarazioni di elemento [**MenuGroup**](windowsribbon-element-menugroup.md) , due delle quali sono associate ai comandi del gruppo di menu dell'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="42da1-113">The following example demonstrates the markup required for a [**SplitButton**](windowsribbon-element-splitbutton.md) element with three [**MenuGroup**](windowsribbon-element-menugroup.md) element declarations, two of which are associated with the Menu Group Commands from the previous example.</span></span> <span data-ttu-id="42da1-114">L'attributo *Class* dell'elemento **MenuGroup** viene utilizzato per specificare la dimensione delle voci di menu.</span><span class="sxs-lookup"><span data-stu-id="42da1-114">The *Class* attribute of the **MenuGroup** element is used to specify the size of the menu items.</span></span>


```XML
<Group CommandName="cmdSplitButtonGroup">
  <SplitButton CommandName="cmdSplitButton">
    <SplitButton.ButtonItem>
      <Button CommandName="cmdSBButtonItem"/>
    </SplitButton.ButtonItem>
    <SplitButton.MenuGroups>
      <MenuGroup CommandName="cmdSBMajorItems" 
                 Class="MajorItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup CommandName="cmdSBStandardItems"
                 Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
    </SplitButton.MenuGroups>
  </SplitButton>
</Group>
```



<span data-ttu-id="42da1-115">Lo screenshot seguente illustra il menu (con tre controlli gruppo di menu) generato dal markup degli esempi precedenti.</span><span class="sxs-lookup"><span data-stu-id="42da1-115">The following screen shot illustrates the menu (with three Menu Group controls) that is generated from the markup in the previous examples.</span></span>

![Screenshot di un menu con tre controlli gruppo di menu.](images/controls/menugroup.png)

## <a name="menu-group-properties"></a><span data-ttu-id="42da1-117">Proprietà del gruppo di menu</span><span class="sxs-lookup"><span data-stu-id="42da1-117">Menu Group Properties</span></span>

<span data-ttu-id="42da1-118">Il Framework della barra multifunzione definisce una raccolta di [chiavi di proprietà](windowsribbon-reference-properties.md) per il controllo gruppo di menu.</span><span class="sxs-lookup"><span data-stu-id="42da1-118">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Menu Group control.</span></span>

<span data-ttu-id="42da1-119">In genere, una proprietà del gruppo di menu viene aggiornata nell'interfaccia utente della barra multifunzione invalidando il comando associato al controllo tramite una chiamata al metodo [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="42da1-119">Typically, a Menu Group property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="42da1-120">L'evento di invalidamento viene gestito e gli aggiornamenti delle proprietà definiti dal metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="42da1-120">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="42da1-121">Il metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) non viene eseguito e l'applicazione ha sottoposto a query un valore aggiornato della proprietà, fino a quando la proprietà non è richiesta dal Framework.</span><span class="sxs-lookup"><span data-stu-id="42da1-121">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="42da1-122">Ad esempio, quando viene attivata una scheda e viene visualizzato un controllo nell'interfaccia utente della barra multifunzione o quando viene visualizzata una descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="42da1-122">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="42da1-123">In alcuni casi, una proprietà può essere recuperata tramite il metodo [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e impostata con il metodo [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="42da1-123">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="42da1-124">Nella tabella seguente sono elencate le chiavi di proprietà associate al controllo gruppo di menu.</span><span class="sxs-lookup"><span data-stu-id="42da1-124">The following table lists the property keys that are associated with the Menu Group control.</span></span>



| <span data-ttu-id="42da1-125">Chiave della proprietà</span><span class="sxs-lookup"><span data-stu-id="42da1-125">Property Key</span></span>                                                                                     | <span data-ttu-id="42da1-126">Note</span><span class="sxs-lookup"><span data-stu-id="42da1-126">Notes</span></span>                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="42da1-127">Interfaccia utente \_ pkey \_ abilitata</span><span class="sxs-lookup"><span data-stu-id="42da1-127">UI\_PKEY\_Enabled</span></span>](windowsribbon-reference-properties-uipkey-enabled.md)                       | <span data-ttu-id="42da1-128">Supporta [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span><span class="sxs-lookup"><span data-stu-id="42da1-128">Supports [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) and [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span></span> |
| [<span data-ttu-id="42da1-129">Suggerimento tasto di interfaccia utente \_ pkey \_</span><span class="sxs-lookup"><span data-stu-id="42da1-129">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)                         | <span data-ttu-id="42da1-130">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="42da1-130">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="42da1-131">\_Etichetta pkey dell'interfaccia utente \_</span><span class="sxs-lookup"><span data-stu-id="42da1-131">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)                           | <span data-ttu-id="42da1-132">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="42da1-132">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="42da1-133">Interfaccia utente \_ pkey \_ TooltipDescription</span><span class="sxs-lookup"><span data-stu-id="42da1-133">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | <span data-ttu-id="42da1-134">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="42da1-134">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="42da1-135">Interfaccia utente \_ pkey \_ TooltipTitle</span><span class="sxs-lookup"><span data-stu-id="42da1-135">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | <span data-ttu-id="42da1-136">Può essere aggiornato solo tramite l'invalidamento.</span><span class="sxs-lookup"><span data-stu-id="42da1-136">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="42da1-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="42da1-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42da1-138">Libreria di controlli Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="42da1-138">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="42da1-139">**Elemento di markup MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="42da1-139">**MenuGroup markup element**</span></span>](windowsribbon-element-menugroup.md)
</dt> </dl>

 

 