---
title: Dichiarazione di comandi e controlli con markup della barra multifunzione
description: Il framework Windows della barra multifunzione usa un linguaggio di markup basato su Extensible Application Markup Language (XAML) per implementare in modo dichiarativo l'aspetto di un'applicazione barra multifunzione.
ms.assetid: 76bacfb3-ecaf-47b3-be97-afa5e7e52330
keywords:
- Windows Barra multifunzione, struttura di markup
- Barra multifunzione, struttura di markup
- Windows Barra multifunzione, separazione della presentazione dalla logica dei comandi
- Barra multifunzione, separazione della presentazione dalla logica dei comandi
- Windows Barra multifunzione, componenti
- Barra multifunzione, componenti
- Sistema di comandi per la Windows multifunzione
- controlli per Windows barra multifunzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20ae6c8d62012fac240c6d044c688295d89d8d5899e3673a3b914d8d142111d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118201323"
---
# <a name="declaring-commands-and-controls-with-ribbon-markup"></a>Dichiarazione di comandi e controlli con markup della barra multifunzione

Il framework Windows della barra multifunzione usa un linguaggio di markup basato su Extensible Application Markup Language (XAML) per implementare in modo dichiarativo l'aspetto di un'applicazione barra multifunzione.

-   [Separazione della presentazione dalla logica dei comandi](#separating-presentation-from-command-logic)
-   [Struttura del markup](#markup-structure)
-   [Componenti della barra multifunzione](#ribbon-components)
-   [Argomenti correlati](#related-topics)

## <a name="separating-presentation-from-command-logic"></a>Separazione della presentazione dalla logica dei comandi

La separazione degli attributi di presentazione e di visualizzazione dalla logica di comando nel framework della barra multifunzione viene eseguita tramite due piattaforme di sviluppo distinte, ma dipendenti. Layout di controllo, comportamenti di ridimensionamento, dichiarazioni command e specifiche delle risorse sono il dominio in fase di progettazione di una sintassi di markup dichiarativa basata [sulla specifica Extensible Application Markup Language (XAML).](/dotnet/framework/wpf/advanced/xaml-in-wpf) Funzionalità di basso livello, hook dell'applicazione e gestori di comandi sono definiti nelle implementazioni dell'interfaccia basata su Component Object Model (COM).

Questa separazione tra presentazione e logica offre i vantaggi seguenti:

-   Ciclo di sviluppo di applicazioni più efficiente che consente agli sviluppatori e alle finestre di progettazione dell'interfaccia utente di implementare l'interfaccia utente grafica dell'applicazione barra multifunzione indipendentemente dalle funzionalità principali dell'applicazione. Questa funzionalità di base può essere lasciata agli sviluppatori di software dedicati.
-   Manutenzione meno dis costosa perché le modifiche all'interfaccia utente grafica sono possibili senza modifiche alle funzionalità di base (e viceversa).
-   Specifica semplice delle risorse stringa e immagine tramite markup.
-   Facilità di prototipazione.

## <a name="markup-structure"></a>Struttura del markup

Nella struttura del markup del framework della barra multifunzione sono presenti due rami distinti.

Il primo ramo contiene un manifesto di dichiarazioni di comando e di risorse (stringhe e immagini). Ogni voce Command viene usata dal framework per associare un controllo Barra multifunzione, tramite un ID comando, a un gestore di comandi definito nel codice dell'applicazione.

Il secondo ramo contiene le dichiarazioni di controllo effettive. Ogni controllo è associato a un oggetto Command tramite un *attributo CommandName* che esegue il mapping a un *attributo Name* specificato in ogni dichiarazione Command.

## <a name="ribbon-components"></a>Componenti della barra multifunzione

La funzionalità dell'interfaccia utente del framework della barra multifunzione viene esposta [tramite Visualizzazioni](windowsribbon-reference-elements-view.md). Una visualizzazione è essenzialmente un contenitore, ad esempio la barra multifunzione e [**ContextPopup**](windowsribbon-element-contextpopup.md), usato per presentare i controlli del framework e i comandi a cui sono associati. [](windowsribbon-element-ribbon.md)

La [](windowsribbon-element-ribbon.md) visualizzazione barra multifunzione è costituita da diversi componenti che includono un [menu](windowsribbon-controls-applicationmenu.md)dell'applicazione , la barra [](windowsribbon-controls-tab.md) di accesso [](windowsribbon-controls-group.md) rapido [(QAT)](windowsribbon-controls-quickaccesstoolbar.md) per visualizzare i comandi di uso comune dall'interfaccia utente della barra multifunzione, le schede principali e contestuali che contengono gruppi di controlli e il sistema di menu di scelta rapida completo di [**ContextPopup**](windowsribbon-element-contextpopup.md).

Tutti i componenti della barra multifunzione vengono dichiarati in un file di markup autonomo che:

-   Specifica le proprietà di base per ogni elemento.
-   Mostra chiaramente le relazioni gerarchiche.
-   Fornisce preferenze di layout e hint di ridimensionamento. Per altre informazioni sui modelli di layout del framework della barra multifunzione, vedere Personalizzazione di una barra multifunzione tramite [definizioni delle dimensioni e criteri di ridimensionamento](windowsribbon-templates.md).
-   Consente di definire risorse quali immagini ed etichette. Per altre informazioni sulle risorse immagine, vedere Specifica delle risorse immagine [della barra multifunzione](windowsribbon-imageformats.md).

I due esempi di markup della barra multifunzione seguenti illustrano come un set di voci del menu dell'applicazione della barra multifunzione sia associato a un nome di comando e a un ID.

1.  Questa sezione illustra le dichiarazioni command necessarie per un menu dell'applicazione con comandi di base, ad esempio New, Open e Save.
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

    

2.  In questa sezione vengono illustrate le dichiarazioni Control associate.
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

    

Quando il markup viene compilato con lo strumento UICC (Ui Command Compiler), i nomi e gli ID dei comandi vengono inseriti in un file di intestazione usato dall'applicazione host della barra multifunzione.

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

 

 