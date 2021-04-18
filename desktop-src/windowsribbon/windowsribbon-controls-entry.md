---
title: Libreria di controlli Windows Ribbon Framework
description: Negli argomenti contenuti in questa sezione viene descritto il set di controlli inclusi nel framework della barra multifunzione di Windows. I controlli elencati di seguito sono gli oggetti dell'interfaccia utente in una barra multifunzione che espone la funzionalità del comando.
ms.assetid: bda13e51-7e5f-4600-a6bd-9388bffd6ce2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 840b07bafe0c43cb7ab148a4413657b9722c409b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300236"
---
# <a name="windows-ribbon-framework-control-library"></a>Libreria di controlli Windows Ribbon Framework

Negli argomenti contenuti in questa sezione viene descritto il set di controlli inclusi nel framework della barra multifunzione di Windows. I controlli elencati di seguito sono gli oggetti dell'interfaccia utente in una barra multifunzione che espone la funzionalità del comando.

-   [Introduzione](#introduction)
-   [Controlli](#windows-ribbon-framework-control-library)
    -   [Controlli di base](#basic-controls)
    -   [Controlli contenitore](#container-controls)
    -   [Controlli specializzati](#specialized-controls)
-   [Argomenti correlati](#related-topics)

## <a name="introduction"></a>Introduzione

Il Framework della barra multifunzione è costituito da componenti come [schede](windowsribbon-controls-tab.md) e dalla [barra di accesso rapido](windowsribbon-controls-quickaccesstoolbar.md), che interagiscono per offrire un'interfaccia utente avanzata. Singolarmente, questi componenti espongono tipi diversi di comandi per offrire ai clienti un'esperienza organizzata e prevedibile per tutte le applicazioni della barra multifunzione. Ogni scheda, ad esempio, espone i comandi correlati alla creazione e all'esecuzione di parti specifiche del contenuto all'interno dell'area di lavoro dell'applicazione, mentre il [menu applicazione](windowsribbon-controls-applicationmenu.md) espone funzionalità correlate a un progetto completo, ad esempio un intero documento, immagine o film.

In questo argomento viene fornito un elenco completo dei controlli della barra multifunzione e viene inclusa una breve descrizione di ogni controllo, con collegamenti a una documentazione più dettagliata, se disponibile.

## <a name="the-controls"></a>Controlli

Il Framework della barra multifunzione è costituito da due [visualizzazioni](windowsribbon-reference-elements-view.md): la visualizzazione della [**barra multifunzione**](windowsribbon-element-ribbon.md) e la visualizzazione [**ContextPopup**](windowsribbon-element-contextpopup.md) . Ogni vista può ospitare diversi componenti che fungono da contenitori di presentazione per tutti i controlli sottoposti a rendering e gestiti dal Framework.

La visualizzazione della [**barra multifunzione**](windowsribbon-element-ribbon.md) ospita l'elemento [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) , l'elemento [**QuickAccessToolBar**](windowsribbon-element-quickaccesstoolbar.md) e la barra dei comandi della barra multifunzione mentre la vista [**ContextPopup**](windowsribbon-element-contextpopup.md) ospita un elemento [**ContextMenu**](windowsribbon-element-contextmenu.md) , un elemento [**MiniToolbar**](windowsribbon-element-minitoolbar.md) o entrambi.

Ogni controllo Framework è distinto dalla funzionalità associata al relativo [**tipo di comando**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype).

### <a name="basic-controls"></a>Controlli di base

I controlli di base sono costituiti da uno o più pulsanti che possono essere richiamati con un solo clic del mouse per eseguire un'azione semplice.

> [!Note]  
> La [**casella**](windowsribbon-element-spinner.md) di selezione è un'eccezione perché contiene un controllo di modifica.

 

Nella tabella seguente sono elencati i controlli di base del Framework della barra multifunzione.



| Control                                                  | Elemento markup                                             |
|----------------------------------------------------------|------------------------------------------------------------|
| [Button](windowsribbon-controls-button.md)              | [**Pulsante**](windowsribbon-element-button.md)             |
| [Casella di controllo](windowsribbon-controls-checkbox.md)         | [**Casella**](windowsribbon-element-checkbox.md)         |
| [Pulsante della Guida](windowsribbon-controls-helpbutton.md)     | [**HelpButton**](windowsribbon-element-helpbutton.md)     |
| [Spinner](windowsribbon-controls-spinner.md)            | [**Spinner**](windowsribbon-element-spinner.md)           |
| [Interruttore](windowsribbon-controls-togglebutton.md) | [**ToggleButton**](windowsribbon-element-togglebutton.md) |



 

### <a name="container-controls"></a>Controlli contenitore

I controlli contenitore sono costituiti da gruppi di controlli, menu, elenchi o raccolte di elementi e comandi.

Il Framework distingue tra due tipi di contenitori, statici e dinamici.

### <a name="static-containers"></a>Contenitori statici

I contenitori statici vengono dichiarati e popolati, insieme a tutte le risorse associate, nel file di markup della barra multifunzione. Questi controlli non possono essere modificati in fase di esecuzione.

I vantaggi dei controlli statici includono i seguenti:

-   Prototipazione rapida. I controlli statici consentono di creare rapidamente una barra multifunzione che simula la creazione di una struttura della barra multifunzione finale che non richiede codice complesso.
-   Modifiche semplici. La maggior parte degli elementi, degli attributi, delle risorse e dei layout dei controlli statici può essere modificata nel markup.
-   Interfaccia utente coerente. Le applicazioni ben progettate forniscono un'interfaccia utente coerente e stabile che evita modifiche a menu ed elenchi in fase di esecuzione.

La tabella seguente descrive i controlli contenitore statici nel framework della barra multifunzione.



| Control                                                        | Elemento markup                                                   |
|----------------------------------------------------------------|------------------------------------------------------------------|
| [Menu applicazione](windowsribbon-controls-applicationmenu.md) | [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) |
| [Popup contesto](windowsribbon-controls-contextpopup.md)       | [**ContextPopup**](windowsribbon-element-contextpopup.md)       |
| [Pulsante a discesa](windowsribbon-controls-dropdownbutton.md)  | [**DropDownButton**](windowsribbon-element-dropdownbutton.md)   |
| [Gruppo](windowsribbon-controls-group.md)                      | [**Group**](windowsribbon-element-group.md)                     |
| [Gruppo di menu](windowsribbon-controls-menugroup.md)             | [**MenuGroup**](windowsribbon-element-menugroup.md)             |
| [Pulsante di divisione](windowsribbon-controls-splitbutton.md)         | [**SplitButton**](windowsribbon-element-splitbutton.md)         |
| [TAB](windowsribbon-controls-tab.md)                          | [**Scheda**](windowsribbon-element-tab.md)                         |
| [Gruppo di schede](windowsribbon-controls-tabgroup.md)               | [**TabGroup**](windowsribbon-element-tabgroup.md)               |



 

### <a name="dynamic-containers"></a>Contenitori dinamici

I contenitori dinamici sono dichiarati nel file di markup della barra multifunzione. Presentano un gruppo di elementi o comandi creati o modificati in fase di esecuzione.

Una sottoclasse di contenitori dinamici, detti raccolte, si distingue dalla relativa implementazione dell'interfaccia [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) . Questa interfaccia consente a un controllo di esporre l'elenco di elementi o comandi come una raccolta e di supportare gli aggiornamenti in base all'interazione dell'utente e alle condizioni di run-time. Per ulteriori informazioni, vedere [utilizzo delle raccolte](ribbon-controls-galleries.md).

Nella tabella seguente sono elencati i controlli contenitore dinamici nel framework della barra multifunzione.



| Control                                                               | Elemento markup                                                         |
|-----------------------------------------------------------------------|------------------------------------------------------------------------|
| [ComboBox](windowsribbon-controls-combobox.md)                      | [**ComboBox**](windowsribbon-element-combobox.md)                     |
| [Raccolta a discesa](windowsribbon-controls-dropdowngallery.md)       | [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)       |
| [Raccolta della barra multifunzione](windowsribbon-controls-inribbongallery.md)       | [**Inribbongallery**](windowsribbon-element-inribbongallery.md)       |
| [Barra di accesso rapido](windowsribbon-controls-quickaccesstoolbar.md) | [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md) |
| [Elementi recenti](windowsribbon-controls-recentitems.md)                | [**RecentItems**](windowsribbon-element-recentitems.md)               |
| [Raccolta di pulsanti di suddivisione](windowsribbon-controls-splitbuttongallery.md) | [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) |



 

### <a name="specialized-controls"></a>Controlli specializzati

Il Framework della barra multifunzione contiene una serie di controlli specializzati per funzionalità specifiche dell'interfaccia utente.

Nella tabella seguente sono elencati i controlli specializzati del Framework della barra multifunzione.



| Control                                                                  | Elemento markup                                                           |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Selezione colori a discesa](windowsribbon-controls-dropdowncolorpicker.md) | [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) |
| [Controllo carattere](windowsribbon-controls-fontcontrol.md)                   | [**FontControl**](windowsribbon-element-fontcontrol.md)                 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sui comandi e sui controlli](windowsribbon-commandscontrols.md)
</dt> </dl>

 

 