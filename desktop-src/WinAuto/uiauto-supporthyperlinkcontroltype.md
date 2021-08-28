---
title: Tipo di controllo Collegamento ipertestuale
description: Questo argomento fornisce informazioni sul supporto di Microsoft Automazione interfaccia utente per il tipo di controllo Collegamento ipertestuale.
ms.assetid: 6dd16ae6-eff0-4913-8916-5092aec34f1f
keywords:
- Automazione interfaccia utente,supporto per il tipo di controllo Collegamento ipertestuale
- Automazione interfaccia utente,Tipo di controllo Collegamento ipertestuale
- Automazione interfaccia utente,struttura ad albero per tipo di controllo Collegamento ipertestuale
- Automazione interfaccia utente,proprietà per il tipo di controllo Collegamento ipertestuale
- Automazione interfaccia utente,pattern di controllo per il tipo di controllo Collegamento ipertestuale
- Automazione interfaccia utente,eventi per tipo di controllo Collegamento ipertestuale
- strutture ad albero, tipo di controllo Collegamento ipertestuale
- proprietà,Tipo di controllo Collegamento ipertestuale
- pattern di controllo,tipo di controllo Collegamento ipertestuale
- eventi,tipo di controllo Collegamento ipertestuale
- supporto per il tipo di controllo Collegamento ipertestuale
- Hyperlink (tipo di controllo)
- tipi di controllo, struttura ad albero per tipo di controllo Collegamento ipertestuale
- tipi di controllo,pattern di controllo per tipo di controllo Collegamento ipertestuale
- tipi di controllo,supporto per collegamento ipertestuale
- tipi di controllo,Collegamento ipertestuale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52735983429a60061a548bf4cce71b7b128f4b6e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466958"
---
# <a name="hyperlink-control-type"></a>Tipo di controllo Collegamento ipertestuale

Questo argomento fornisce informazioni sul supporto di Microsoft Automazione interfaccia utente per il **tipo di controllo Collegamento** ipertestuale.

I controlli collegamento ipertestuale creano collegamenti che consentono agli utenti di spostarsi all'interno della stessa pagina o da una pagina a un'altra.

Le sezioni seguenti definiscono la struttura ad Automazione interfaccia utente, le proprietà, i pattern di controllo e gli eventi necessari per il **tipo di controllo Collegamento** ipertestuale. I Automazione interfaccia utente si applicano a tutti i controlli collegamento ipertestuale in cui il framework o la piattaforma dell'interfaccia utente Automazione interfaccia utente supporto per i tipi di controllo e i pattern di controllo.

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Osservazioni:](#remarks)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

La tabella seguente illustra un controllo tipico e una visualizzazione contenuto dell'albero Automazione interfaccia utente che riguarda i controlli collegamento ipertestuale e descrive cosa può essere contenuto in ogni visualizzazione. Per altre informazioni sull'albero Automazione interfaccia utente, vedere Panoramica Automazione interfaccia utente [albero](uiauto-treeoverview.md).




| Visualizzazione controlli | Visualizzazione contenuto | 
|--------------|--------------|
| <ul><li>Hyperlink</li></ul> | <ul><li>Hyperlink</li></ul> | 




 

## <a name="relevant-properties"></a>Proprietà rilevanti

Nella tabella seguente sono elencate le Automazione interfaccia utente il cui valore o definizione è particolarmente rilevante per i controlli collegamento ipertestuale. Per altre informazioni sulle Automazione interfaccia utente, vedere Recupero di proprietà [da Automazione interfaccia utente Elements](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | valore         | Note                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vedere le note.    | Il valore di questa proprietà deve essere univoco in tutti i controlli di un'applicazione.                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vedere le note.    | Il rettangolo più esterno che contiene l'intero controllo.                                                                                 |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vedere le note.    | Il punto selezionabile del controllo collegamento ipertestuale deve essere un punto che avvia il collegamento ipertestuale se si fa clic con un puntatore del mouse.                     |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Collegamento ipertestuale** |                                                                                                                                          |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | true          | Il controllo collegamento ipertestuale è sempre incluso nella visualizzazione contenuto dell'Automazione interfaccia utente struttura ad albero.                                                  |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true          | Il controllo collegamento ipertestuale è sempre incluso nella visualizzazione controlli dell'Automazione interfaccia utente albero.                                                  |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vedere le note.    | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vedere le note.    | Se è presente un'etichetta di testo statica, questa proprietà deve esporre un riferimento a tale controllo.                                                  |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vedere le note.    | Stringa localizzata corrispondente al **tipo di controllo Collegamento** ipertestuale. Il valore predefinito è "hyperlink" per en-US o english (Stati Uniti). |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vedere le note.    | Il nome del controllo collegamento ipertestuale è il testo visualizzato sullo schermo sotto forma di sottolineatura.                                                  |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

Nella tabella seguente sono elencati i Automazione interfaccia utente di controllo che i controlli collegamento ipertestuale devono supportare. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo/proprietà del pattern                  | Supporto/valore                | Note                                                                                                                                                                                                                                                  |
|---------------------------------------------------|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) | Obbligatoria                     | Tutti i controlli collegamento ipertestuale devono supportare il [pattern di](uiauto-implementinginvoke.md) controllo Invoke.                                                                                                                                                       |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)   | Dipende da                      | I controlli collegamento ipertestuale devono [supportare il](uiauto-implementingvalue.md) pattern di controllo Valore quando il collegamento contiene informazioni utilizzabili e significative per l'utente.                                                                              |
| [**valore**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)      | Ad esempio, "https://www..". | Un URL per un indirizzo Internet o Intranet è un esempio di collegamento ipertestuale che contiene informazioni significative per l'utente. Un collegamento a livello di codice, tuttavia, è significativo solo per un'applicazione e non è consigliabile per la **proprietà** Value. |



 

## <a name="required-events"></a>Eventi obbligatori

Nella tabella seguente sono elencati Automazione interfaccia utente eventi che i controlli collegamento ipertestuale devono supportare. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automazione interfaccia utente evento                                                                                                                   | Note                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md) |                                                                                                                            |
| [**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md)                                                     |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                 | Se il controllo supporta la [**proprietà IsEnabled,**](uiauto-automation-element-propids.md) deve supportare questo evento.   |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)             | Se il controllo supporta la [**proprietà IsOffscreen,**](uiauto-automation-element-propids.md) deve supportare questo evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="remarks"></a>Commenti

Il tipo di controllo Collegamento ipertestuale deve essere applicato solo a un oggetto che, quando si fa clic, determina la navigazione. non deve essere applicato al contenitore del collegamento ipertestuale. Ad esempio, solo gli "hot spot" selezionabili all'interno di una mappa immagine devono avere il **tipo di** controllo Collegamento ipertestuale. Lo stesso vale per i collegamenti ipertestuali in un campo di testo o in un contenitore di documenti. In questo caso, solo il testo o l'immagine del collegamento ipertestuale deve avere il **tipo di controllo Collegamento** ipertestuale, non il contenitore.

Il [pattern di](uiauto-implementingtextandtextrange.md) controllo Text è ideale per supportare collegamenti ipertestuali incorporati in elementi di testo o documento.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




