---
title: Tipo di controllo AppBar
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo AppBar.
ms.assetid: B56F4E7A-934F-8516-9B1B-B23B80D54273
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo AppBar
- Automazione interfaccia utente, tipo di controllo AppBar
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo AppBar
- pattern di controllo, tipo di controllo AppBar
- supporto per il tipo di controllo AppBar
- Tipo di controllo AppBar
- tipi di controllo, AppBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 151aecc0f5f97878e10b59b091c4c59ec98cb26d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473859"
---
# <a name="appbar-control-type"></a>Tipo di controllo AppBar

In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **AppBar** .

Una barra dell'app è un elemento dell'interfaccia utente che presenta la navigazione, i comandi e gli strumenti per l'utente. Per le app di Windows Store, è possibile visualizzare le barre dell'app per le app premendo il tasto Windows + Z.

Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **AppBar** .

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Eventi obbligatori](#required-events)
-   [Eventi rilevanti](#relevant-events)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

La tabella seguente illustra una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente che riguarda i controlli **AppBar** e descrive il possibile contenuto di ogni visualizzazione. Il **pulsante** è l'elemento più comune all'interno di un **AppBar** , ma sono possibili anche altri controlli che richiamano azioni per un'app. Un **AppBar** può anche avere 0 o più separatori (tipo di controllo **separator** ), che vengono visualizzati nella visualizzazione controlli come posizionati tra gli altri controlli. Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Visualizzazione controlli</th>
<th>Visualizzazione contenuto</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li>AppBar
<ul>
<li>Button (0 o più)</li>
<li>Altri controlli (0 o molti)</li>
</ul></li>
</ul></td>
<td><ul>
<li>Non applicabile
<ul>
<li>Button (0 o più)</li>
<li>Altri controlli (0 o molti)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per i controlli che implementano il tipo di controllo **AppBar** . Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | Valore      | Note                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONIDPROPERTYID UIA**](uiauto-automation-element-propids.md)                 | Vedere le note. | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.                                                                                                                |
| [**\_BOUNDINGRECTANGLEPROPERTYID UIA**](uiauto-automation-element-propids.md)       | Vedere le note. | Il valore esposto da questa proprietà deve includere tutti i controlli contenuti.                                                                                                                                    |
| [**\_CONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md)                   | **AppBar** |                                                                                                                                                                                                                             |
| [**\_ISCONTENTELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | FALSE      | Un controllo barra dell'app non è incluso nella visualizzazione contenuto dell'albero di automazione interfaccia utente.                                                                                                                                           |
| [**\_ISCONTROLELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | true       | Un controllo barra dell'app viene sempre incluso nella visualizzazione controlli dell'albero di automazione interfaccia utente.                                                                                                                                        |
| [**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**](uiauto-automation-element-propids.md)   | Vedere le note  | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà. I controlli all'interno della barra dell'app possono in genere assumere lo stato attivo.                                                                                    |
| [**\_ISOFFSCREENPROPERTYID UIA**](uiauto-automation-element-propids.md)                   | Vedere le note. | Il valore di questa proprietà dipende dal fatto che il controllo sia visualizzabile o meno sullo schermo.                                                                                                                                        |
| [**\_LABELEDBYPROPERTYID UIA**](uiauto-automation-element-propids.md)                       | Null       | I controlli barra dell'app in genere non hanno un'etichetta.                                                                                                                                                                               |
| [**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md) | Vedere le note. | Stringa localizzata corrispondente al tipo di controllo **AppBar** . Il valore predefinito è "barra app" per en-US o inglese (Stati Uniti).                                                                                         |
| [**\_NAMEPROPERTYID UIA**](uiauto-automation-element-propids.md)                                 | Vedere le note. | Il controllo barra dell'app non necessita di un nome a meno che un'applicazione non disponga di più di una barra dell'app. Se in un'applicazione sono presenti più barre dell'app, usare questa proprietà per esporre i nomi distinti, ad esempio "Top" o "bottom". |



 

## <a name="required-events"></a>Eventi obbligatori

La tabella seguente elenca gli eventi di automazione interfaccia utente che devono essere supportati dai controlli barra dell'app. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento di automazione interfaccia utente                                                                                                                   | Note                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.                 | Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.             | Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento. |
| [**\_STRUCTURECHANGEDEVENTID UIA**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="relevant-events"></a>Eventi rilevanti

La tabella seguente elenca gli eventi di automazione interfaccia utente che sono particolarmente rilevanti per i controlli che implementano il tipo di controllo **AppBar** , ma non sono strettamente necessari.



| Evento di automazione interfaccia utente                                                                                 | Note                                                                              |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**\_MENUCLOSEDEVENTID UIA**](uiauto-event-ids.md)                            | Le implementazioni della piattaforma possono generare questo evento quando il controllo barra dell'app è chiuso. |
| [**\_MENUOPENEDEVENTID UIA**](uiauto-event-ids.md)                            | Le implementazioni della piattaforma possono generare questo evento quando viene aperto il controllo barra dell'app. |
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

[**AppBar (controllo XAML)**](/uwp/api/Windows.UI.Xaml.Controls.AppBar)
</dt> <dt>

[**Oggetto WinJS. UI. AppBar**](/previous-versions/windows/apps/br229670(v=win.10))
</dt> </dl>

 

 