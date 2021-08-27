---
title: Tipo di controllo AppBar
description: Questo argomento fornisce informazioni sul supporto di Microsoft Automazione interfaccia utente per il tipo di controllo AppBar.
ms.assetid: B56F4E7A-934F-8516-9B1B-B23B80D54273
keywords:
- Automazione interfaccia utente,supporto per il tipo di controllo AppBar
- Automazione interfaccia utente, tipo di controllo AppBar
- Automazione interfaccia utente,pattern di controllo per il tipo di controllo AppBar
- pattern di controllo, tipo di controllo AppBar
- supporto per il tipo di controllo AppBar
- Tipo di controllo AppBar
- tipi di controllo, AppBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fc8cf562b125267e9b35239e8490f11ed6ae830
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472887"
---
# <a name="appbar-control-type"></a>Tipo di controllo AppBar

Questo argomento fornisce informazioni sul supporto di Microsoft Automazione interfaccia utente per il **tipo di controllo AppBar.**

Una barra dell'app è un elemento dell'interfaccia utente che presenta la navigazione, i comandi e gli strumenti all'utente. Per Windows store, le barre delle app per le app possono essere visualizzate premendo Windows tasto + Z.

Le sezioni seguenti definiscono la struttura Automazione interfaccia utente struttura ad albero, le proprietà, i pattern di controllo e gli eventi per il **tipo di controllo AppBar.**

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Eventi obbligatori](#required-events)
-   [Eventi pertinenti](#relevant-events)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

La tabella seguente illustra un controllo tipico e una visualizzazione contenuto dell'albero Automazione interfaccia utente relativo ai controlli **AppBar** e descrive cosa può essere contenuto in ogni visualizzazione. **Button** è l'elemento più comune all'interno di **un controllo AppBar,** ma sono possibili anche altri controlli che richiamano azioni per un'app. Un **controllo AppBar** può anche avere 0 o più separatori (tipo di controllo **Separator),** visualizzati nella visualizzazione controlli posizionati tra gli altri controlli. Per altre informazioni sull'albero Automazione interfaccia utente, vedere panoramica [Automazione interfaccia utente albero.](uiauto-treeoverview.md)




| Visualizzazione controlli | Visualizzazione contenuto | 
|--------------|--------------|
| <ul><li>AppBar<ul><li>Button (0 o più)</li><li>Altri controlli (0 o molti)</li></ul></li></ul> | <ul><li>Non applicabile<ul><li>Button (0 o più)</li><li>Altri controlli (0 o molti)</li></ul></li></ul> | 




 

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le Automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per i controlli che implementano il tipo **di controllo AppBar.** Per altre informazioni sulle Automazione interfaccia utente, vedere [Recupero di proprietà da Automazione interfaccia utente elementi](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | valore      | Note                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vedere le note. | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata dell'Automazione interfaccia utente albero.                                                                                                                |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vedere le note. | Il valore esposto da questa proprietà deve includere tutti i controlli contenuti.                                                                                                                                    |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **AppBar** |                                                                                                                                                                                                                             |
| [**\_IsContentElementPropertyId dell'interfaccia utente**](uiauto-automation-element-propids.md)         | FALSE      | Un controllo barra dell'app non è incluso nella visualizzazione contenuto dell'Automazione interfaccia utente albero.                                                                                                                                           |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true       | Un controllo barra dell'app è sempre incluso nella visualizzazione controlli dell'Automazione interfaccia utente albero.                                                                                                                                        |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vedere le note  | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà. I controlli all'interno della barra dell'app in genere possono usare lo stato attivo della tastiera.                                                                                    |
| [**UIA \_ IsOffscreenPropertyId**](uiauto-automation-element-propids.md)                   | Vedere le note. | Il valore di questa proprietà dipende dal fatto che il controllo sia visualizzabile o meno sullo schermo.                                                                                                                                        |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Null       | I controlli barra dell'app in genere non hanno un'etichetta.                                                                                                                                                                               |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vedere le note. | Stringa localizzata corrispondente al **tipo di controllo AppBar.** Il valore predefinito è "app bar" per en-US o English (Stati Uniti).                                                                                         |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vedere le note. | Il controllo barra dell'app non richiede un nome, a meno che un'applicazione non abbia più di una barra dell'app. Se in un'applicazione sono presenti più barre dell'app, usare questa proprietà per esporre nomi distinti, ad esempio "Top" o "Bottom". |



 

## <a name="required-events"></a>Eventi obbligatori

La tabella seguente elenca gli eventi Automazione interfaccia utente che i controlli barra dell'app devono supportare. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automazione interfaccia utente eventi                                                                                                                   | Note                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md) |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                 | Se il controllo supporta la [**proprietà IsEnabled,**](uiauto-automation-element-propids.md) deve supportare questo evento.   |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)             | Se il controllo supporta la [**proprietà IsOffscreen,**](uiauto-automation-element-propids.md) deve supportare questo evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="relevant-events"></a>Eventi pertinenti

La tabella seguente elenca gli Automazione interfaccia utente che sono particolarmente rilevanti per i controlli che implementano il tipo di **controllo AppBar,** ma non strettamente necessari.



| Automazione interfaccia utente eventi                                                                                 | Note                                                                              |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**UIA \_ MenuClosedEventId**](uiauto-event-ids.md)                            | Le implementazioni della piattaforma possono creare questo evento quando il controllo barra dell'app viene chiuso. |
| [**UIA \_ MenuOpenedEventId**](uiauto-event-ids.md)                            | Le implementazioni della piattaforma possono creare questo evento all'apertura del controllo barra dell'app. |
| [**IUIAutomationPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) | Gestore dell'evento di modifica della proprietà.                                                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> <dt>

**Riferimento**
</dt> <dt>

[**Controllo XAML AppBar**](/uwp/api/Windows.UI.Xaml.Controls.AppBar)
</dt> <dt>

[**Oggetto WinJS.UI.AppBar**](/previous-versions/windows/apps/br229670(v=win.10))
</dt> </dl>

 

 
