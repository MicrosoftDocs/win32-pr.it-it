---
title: Dichiarazione di comandi e controlli con markup della barra multifunzione
description: Il Framework della barra multifunzione di Windows usa un linguaggio di markup basato su Extensible Application Markup Language (XAML) per implementare in modo dichiarativo l'aspetto di un'applicazione Ribbon.
ms.assetid: 76bacfb3-ecaf-47b3-be97-afa5e7e52330
keywords:
- Barra multifunzione di Windows, struttura markup
- Barra multifunzione, struttura markup
- Barra multifunzione di Windows, separazione della presentazione dalla logica dei comandi
- Barra multifunzione, separazione della presentazione dalla logica del comando
- Barra multifunzione di Windows, componenti
- Barra multifunzione, componenti
- sistema di comando per la barra multifunzione di Windows
- controlli per la barra multifunzione di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c97c5c193332ce217709c825a58f0ae546c03c9c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399447"
---
# <a name="declaring-commands-and-controls-with-ribbon-markup"></a>Dichiarazione di comandi e controlli con markup della barra multifunzione

Il Framework della barra multifunzione di Windows usa un linguaggio di markup basato su Extensible Application Markup Language (XAML) per implementare in modo dichiarativo l'aspetto di un'applicazione Ribbon.

-   [Separazione della presentazione dalla logica del comando](#separating-presentation-from-command-logic)
-   [Struttura di markup](#markup-structure)
-   [Componenti della barra multifunzione](#ribbon-components)
-   [Argomenti correlati](#related-topics)

## <a name="separating-presentation-from-command-logic"></a>Separazione della presentazione dalla logica del comando

La separazione degli attributi di presentazione e visualizzazione dalla logica dei comandi nel framework della barra multifunzione viene eseguita tramite due piattaforme di sviluppo distinte, ma dipendenti. I layout di controllo, i comportamenti di ridimensionamento, le dichiarazioni di comando e le specifiche delle risorse sono il dominio della fase di progettazione di una sintassi di markup dichiarativa basata sulla specifica [Extensible Application Markup Language (XAML)](/dotnet/framework/wpf/advanced/xaml-in-wpf) . Funzionalità di basso livello, hook dell'applicazione e gestori di comandi sono definiti nelle implementazioni di interfaccia basate su Component Object Model (COM).

Questa separazione di presentazione e logica offre i vantaggi seguenti:

-   Un ciclo di sviluppo di applicazioni più efficiente che consente agli sviluppatori e ai progettisti dell'interfaccia utente di implementare l'interfaccia utente grafica dell'applicazione Ribbon indipendentemente dalla funzionalità di base dell'applicazione. Questa funzionalità di base può essere lasciata agli sviluppatori di software dedicati.
-   Manutenzione meno costosa poiché le modifiche all'interfaccia utente grafica sono possibili senza modifiche alle funzionalità principali (e viceversa).
-   Specifica semplice delle risorse stringa e immagine tramite markup.
-   Semplicità di prototipo.

## <a name="markup-structure"></a>Struttura di markup

All'interno della struttura del markup del Framework Ribbon sono presenti due rami distinti.

Il primo ramo contiene un manifesto di dichiarazioni di comando e di risorse (stringhe e immagini). Ogni voce di comando viene utilizzata dal Framework per associare un controllo Ribbon, tramite un ID di comando, a un gestore di comandi definito nel codice dell'applicazione.

Il secondo ramo contiene le dichiarazioni di controllo effettive. Ogni controllo è associato a un comando tramite un attributo *CommandName* che esegue il mapping a un attributo *Name* specificato in ogni dichiarazione di comando.

## <a name="ribbon-components"></a>Componenti della barra multifunzione

La funzionalità dell'interfaccia utente del Framework Ribbon è esposta tramite [viste](windowsribbon-reference-elements-view.md). Una vista è essenzialmente un contenitore, ad esempio la [**barra multifunzione**](windowsribbon-element-ribbon.md) e [**ContextPopup**](windowsribbon-element-contextpopup.md), usato per presentare i controlli del Framework e i comandi a cui sono associati.

La visualizzazione della [**barra multifunzione**](windowsribbon-element-ribbon.md) è costituita da diversi componenti che includono un [menu applicazione](windowsribbon-controls-applicationmenu.md), la [barra di accesso rapido (QAT)](windowsribbon-controls-quickaccesstoolbar.md) per la visualizzazione dei comandi di uso comune dall'interfaccia utente della barra multifunzione, le [schede](windowsribbon-controls-tab.md) core e contestuali che contengono [gruppi](windowsribbon-controls-group.md) di controlli e il sistema di menu di scelta rapida completo del [**ContextPopup**](windowsribbon-element-contextpopup.md).

Tutti i componenti della barra multifunzione sono dichiarati in un file di markup autonomo:

-   Specifica le proprietà di base per ogni elemento.
-   Mostra chiaramente le relazioni gerarchiche.
-   Fornisce le preferenze di layout e gli hint di scalabilità. Per ulteriori informazioni sui modelli di layout del Framework della barra multifunzione, vedere [personalizzazione di una barra multifunzione tramite definizioni di dimensioni e criteri di scalabilità](windowsribbon-templates.md).
-   Fornisce un modo per definire risorse quali immagini ed etichette. Per altre informazioni sulle risorse di immagine, vedere [specifica delle risorse dell'immagine della barra multifunzione](windowsribbon-imageformats.md).

I due esempi di markup della barra multifunzione seguenti illustrano come un set di voci di menu dell'applicazione Ribbon è associato a un nome di comando e a un ID.

1.  In questa sezione vengono illustrate le dichiarazioni di comando necessarie per un menu dell'applicazione con comandi di base, ad esempio nuovo, Apri e Salva.
    ```XML
    <!-- Command declarations for the Application Menu. -->
    <Command Name="cmdFileMenu"
             Symbol="ID_FILE_MENU"
             Id="25000" />
    <!-- Command declaration for most recently used items. -->
    <Command Name="cmdMRUItems"
             Symbol="ID_FILE_MRUITEMS"
             Id="25050"/>
    <!-- Command declarations for Application Menu items. -->
    <Command Name="cmdNew"
             Symbol="ID_FILE_NEW"
             Comment="New"
             Id="25001"
             LabelTitle="&amp;New"/>
    <Command Name="cmdOpen"
             Symbol="ID_FILE_OPEN"
             Comment="Open"
             Id="25002"
             LabelTitle="&amp;&amp;Open"/>
    <Command>
      <Command.Name>cmdSave</Command.Name>
      <Command.Symbol>ID_FILE_SAVE</Command.Symbol>
      <Command.Comment>Save</Command.Comment>
      <Command.Id>25003</Command.Id>
      <Command.LabelTitle>
        <String>
          <String.Content>Label for Save</String.Content>
          <String.Id>59999</String.Id>
          <String.Symbol>strSave</String.Symbol>
        </String>
      </Command.LabelTitle>
      <Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
      <Command.TooltipDescription>Tooltip description for Save Command.</Command.TooltipDescription>
      <Command.Keytip>s1</Command.Keytip>
    </Command>
    <Command Name="cmdPrint"
             Symbol="ID_FILE_PRINT"
             Comment="Save"
             Id="25004"
             LabelTitle="Print" />
    <Command Name="cmdExit"
             Symbol="ID_FILE_EXIT"
             Comment="Exit"
             Id="25005"
             LabelTitle="Exit" />
    ```

    

2.  In questa sezione vengono illustrate le dichiarazioni di controllo associate.
    ```XML
    <!-- Control declarations for Application Menu items. -->
    <Ribbon.ApplicationMenu>
      <ApplicationMenu CommandName="cmdFileMenu">
        <!-- Most recently used items collection. -->
        <ApplicationMenu.RecentItems>
          <RecentItems CommandName="cmdMRUItems"/>
        </ApplicationMenu.RecentItems>
        <!-- Menu items collection. -->
        <MenuGroup>
          <Button CommandName="cmdNew" />
          <Button CommandName="cmdOpen" />
          <Button CommandName="cmdSave" />
        </MenuGroup>
        <MenuGroup>
          <Button CommandName="cmdPrint" />
          <Button CommandName="cmdExit" />
        </MenuGroup>
      </ApplicationMenu>
    </Ribbon.ApplicationMenu>
    ```

    

Quando il markup viene compilato con lo strumento del compilatore di comandi dell'interfaccia utente (UICC), i nomi e gli ID del comando vengono inseriti in un file di intestazione utilizzato dall'applicazione host della barra multifunzione.

Di seguito è riportato un esempio di un file di intestazione generato da UICC.


```
// *****************************************************************************
// * This is an automatically generated header file for UI Element definition  *
// * resource symbols and values. Please do not modify manually.               *
// *****************************************************************************

#pragma once

#define cmdFileMenu 25000 
#define cmdNew 22001  /* New */ 
#define cmdNew_LabelTitle_RESID 60005
#define cmdOpen 22002  /* Open */ 
#define cmdOpen_LabelTitle_RESID 60006
#define cmdSave 22003  /* Save */ 
#define cmdSave_LabelTitle_RESID 60007
#define cmdSave_TooltipTitle_RESID 60008
#define cmdSave_TooltipDescription_RESID 60009
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Extensible Application Markup Language (XAML)](/dotnet/framework/wpf/advanced/xaml-in-wpf)
</dt> <dt>

[Compilazione del markup della barra multifunzione](windowsribbon-intentcl.md)
</dt> </dl>

 

 