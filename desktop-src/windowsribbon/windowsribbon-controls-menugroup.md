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
# <a name="menu-group"></a>Gruppo di menu

Il gruppo di menu Organizza i comandi e i controlli correlati all'interno di un menu o di una barra degli strumenti.

-   [Introduzione](#introduction)
-   [Proprietà del gruppo di menu](#menu-group-properties)
-   [Argomenti correlati](#related-topics)

## <a name="introduction"></a>Introduzione

Il controllo gruppo di menu, esposto tramite l'elemento di markup [**MenuGroup**](windowsribbon-element-menugroup.md) , è un contenitore logico per gruppi di elementi o comandi nei controlli basati su menu, inclusa la mini-barra degli strumenti [popup del contesto](windowsribbon-controls-contextpopup.md) .

È possibile specificare un'etichetta per un gruppo di menu tramite l'attributo *LabelTitle* o la proprietà [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) di una dichiarazione di comando associata. Il valore assegnato a *LabelTitle* viene sottoposto a rendering come intestazione di categoria.

Nell'esempio seguente viene illustrato il markup del comando per un controllo pulsante di menu [combinato](windowsribbon-controls-splitbutton.md) che include due dichiarazioni di comando del gruppo di menu.


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



Nell'esempio seguente viene illustrato il markup necessario per un elemento [**SplitButton**](windowsribbon-element-splitbutton.md) con tre dichiarazioni di elemento [**MenuGroup**](windowsribbon-element-menugroup.md) , due delle quali sono associate ai comandi del gruppo di menu dell'esempio precedente. L'attributo *Class* dell'elemento **MenuGroup** viene utilizzato per specificare la dimensione delle voci di menu.


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



Lo screenshot seguente illustra il menu (con tre controlli gruppo di menu) generato dal markup degli esempi precedenti.

![Screenshot di un menu con tre controlli gruppo di menu.](images/controls/menugroup.png)

## <a name="menu-group-properties"></a>Proprietà del gruppo di menu

Il Framework della barra multifunzione definisce una raccolta di [chiavi di proprietà](windowsribbon-reference-properties.md) per il controllo gruppo di menu.

In genere, una proprietà del gruppo di menu viene aggiornata nell'interfaccia utente della barra multifunzione invalidando il comando associato al controllo tramite una chiamata al metodo [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . L'evento di invalidamento viene gestito e gli aggiornamenti delle proprietà definiti dal metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

Il metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) non viene eseguito e l'applicazione ha sottoposto a query un valore aggiornato della proprietà, fino a quando la proprietà non è richiesta dal Framework. Ad esempio, quando viene attivata una scheda e viene visualizzato un controllo nell'interfaccia utente della barra multifunzione o quando viene visualizzata una descrizione comando.

> [!Note]  
> In alcuni casi, una proprietà può essere recuperata tramite il metodo [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e impostata con il metodo [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

Nella tabella seguente sono elencate le chiavi di proprietà associate al controllo gruppo di menu.



| Chiave della proprietà                                                                                     | Note                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Interfaccia utente \_ pkey \_ abilitata](windowsribbon-reference-properties-uipkey-enabled.md)                       | Supporta [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty). |
| [Suggerimento tasto di interfaccia utente \_ pkey \_](windowsribbon-reference-properties-uipkey-keytip.md)                         | Può essere aggiornato solo tramite l'invalidamento.                                                                                                                                                                                     |
| [\_Etichetta pkey dell'interfaccia utente \_](windowsribbon-reference-properties-uipkey-label.md)                           | Può essere aggiornato solo tramite l'invalidamento.                                                                                                                                                                                     |
| [Interfaccia utente \_ pkey \_ TooltipDescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | Può essere aggiornato solo tramite l'invalidamento.                                                                                                                                                                                     |
| [Interfaccia utente \_ pkey \_ TooltipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | Può essere aggiornato solo tramite l'invalidamento.                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Libreria di controlli Windows Ribbon Framework](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento di markup MenuGroup**](windowsribbon-element-menugroup.md)
</dt> </dl>

 

 