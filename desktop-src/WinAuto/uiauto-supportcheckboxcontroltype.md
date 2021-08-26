---
title: Tipo di controllo CheckBox
description: Questo argomento fornisce informazioni sul supporto di Microsoft Automazione interfaccia utente per il tipo di controllo CheckBox.
ms.assetid: 5a9061bc-2eac-4839-8f2c-32b9d58fe712
keywords:
- Automazione interfaccia utente,supporto per il tipo di controllo CheckBox
- Automazione interfaccia utente,Tipo di controllo CheckBox
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo CheckBox
- Automazione interfaccia utente,proprietà per il tipo di controllo CheckBox
- Automazione interfaccia utente,pattern di controllo per il tipo di controllo CheckBox
- Automazione interfaccia utente,events per il tipo di controllo CheckBox
- strutture ad albero, tipo di controllo CheckBox
- proprietà,tipo di controllo CheckBox
- pattern di controllo, tipo di controllo CheckBox
- eventi, tipo di controllo CheckBox
- supporto per il tipo di controllo CheckBox
- CheckBox (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo CheckBox
- tipi di controllo, pattern di controllo per il tipo di controllo CheckBox
- tipi di controllo, supporto per CheckBox
- tipi di controllo,CheckBox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec20bc259095c41bd1bdc4c3d4e5953be2e883d2
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467808"
---
# <a name="checkbox-control-type"></a>Tipo di controllo CheckBox

Questo argomento fornisce informazioni sul supporto microsoft Automazione interfaccia utente per il **tipo di controllo CheckBox.**

Una casella di controllo è un oggetto usato per indicare uno stato con cui gli utenti possono interagire per scorrere tale stato. Le caselle di controllo presentano all'utente un'opzione binaria (Yes/No), (On/Off) o terziaria (On, Off, Indeterminate).

Le sezioni seguenti definiscono la struttura ad Automazione interfaccia utente, le proprietà, i pattern di controllo e gli eventi necessari per il **tipo di controllo CheckBox.** I Automazione interfaccia utente si applicano a tutti i controlli casella di controllo in cui il framework o la piattaforma dell'interfaccia utente Automazione interfaccia utente supporto per i tipi di controllo e i pattern di controllo.

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Defaultaction](#defaultaction)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

La tabella seguente illustra un controllo tipico e una visualizzazione contenuto dell'albero Automazione interfaccia utente che riguarda i controlli casella di controllo e descrive cosa può essere contenuto in ogni visualizzazione. Per altre informazioni sull'albero Automazione interfaccia utente, vedere panoramica Automazione interfaccia utente [albero](uiauto-treeoverview.md).




| Visualizzazione controlli | Visualizzazione contenuto | 
|--------------|--------------|
| <ul><li>CheckBox</li></ul> | <ul><li>CheckBox</li></ul> | 




 

## <a name="relevant-properties"></a>Proprietà rilevanti

Nella tabella seguente sono elencate le Automazione interfaccia utente il cui valore o definizione è particolarmente rilevante per il **tipo di controllo CheckBox.** Per altre informazioni sulle Automazione interfaccia utente, vedere Recupero di proprietà [da Automazione interfaccia utente elementi](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | valore        | Note                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vedere le note.   | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata dell'Automazione interfaccia utente albero.                                                                                                                                                                       |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vedere le note.   | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                                                                                                           |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vedere le note.   | Supportata se è presente un rettangolo di delimitazione. Se non tutti i punti all'interno del rettangolo di delimitazione sono selezionabili e l'elemento esegue hit testing specializzati, esegue l'override e fornisce un punto selezionabile.                                                                               |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **CheckBox** |                                                                                                                                                                                                                                                                                    |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | true         | Il valore di questa proprietà deve sempre essere **TRUE.** Ciò significa che il controllo casella di controllo deve sempre essere incluso nella visualizzazione contenuto dell'Automazione interfaccia utente albero.                                                                                                                   |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true         | Il valore di questa proprietà deve sempre essere **TRUE.** Ciò significa che il controllo casella di controllo deve sempre essere incluso nella visualizzazione controlli dell'Automazione interfaccia utente albero.                                                                                                                   |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vedere le note.   | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                                                                                                                                                          |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Null         | I controlli casella di controllo sono auto-etichettatura.                                                                                                                                                                                                                                              |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vedere le note.   | Stringa localizzata corrispondente al **tipo di controllo CheckBox.** Il valore predefinito è "check box" per en-US o english (Stati Uniti).                                                                                                                                            |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vedere le note.   | Il valore della proprietà [**IUIAutomationElement::CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) (o [**CachedName)**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedname)del controllo casella di controllo è il testo visualizzato accanto alla casella che mantiene lo stato di attivazione/disattivazione. |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

Nella tabella seguente sono elencati i Automazione interfaccia utente di controllo necessari per essere supportati da tutti i controlli casella di controllo. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo/proprietà del pattern                  | Supporto/valore | Note                                                                                                                                                             |
|---------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) | Obbligatoria      | Le caselle di controllo [supportano il](uiauto-implementingtoggle.md) pattern di controllo Toggle per consentire il ciclo a livello di codice della casella di controllo nei relativi stati interni. |



 

## <a name="required-events"></a>Eventi obbligatori

Nella tabella seguente sono elencati Automazione interfaccia utente eventi che i controlli casella di controllo devono supportare. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automazione interfaccia utente evento                                                                                                                   | Note                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md) |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)             | Se il controllo supporta la [**proprietà IsOffscreen,**](uiauto-automation-element-propids.md) deve supportare questo evento. |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                 | Se il controllo supporta la [**proprietà IsEnabled,**](uiauto-automation-element-propids.md) deve supportare questo evento.   |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà ToggleToggleStatePropertyId.**](uiauto-control-pattern-propids.md)    |                                                                                                                            |



 

## <a name="defaultaction"></a>Defaultaction

L'azione predefinita della casella di controllo è fare sì che un pulsante di opzione assuma lo stato attivo e attivarne/disattivarne lo stato corrente. Come accennato in precedenza, le caselle di controllo presentano una decisione binaria (Sì/No o On/Off) all'utente o una decisione terziaria (On, Off, Indeterminate). Se la casella di controllo è binaria, l'azione predefinita fa sì che lo stato "on" diventi "off" o che lo stato "off" diventi "on". In una casella di controllo terziaria l'azione predefinita scorre gli stati della casella di controllo nello stesso ordine in cui l'utente ha inviato clic successivi del mouse al controllo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




