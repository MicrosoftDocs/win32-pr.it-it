---
title: Cenni preliminari sulle proprietà di automazione interfaccia utente
description: I provider Automazione interfaccia utente Microsoft espongono proprietà Automazione interfaccia utente elementi. Le proprietà consentono alle applicazioni client di recuperare informazioni sui controlli.
ms.assetid: 35f017cb-f50a-4680-9f01-5079aa59da73
keywords:
- Automazione interfaccia utente,panoramica delle proprietà
- Automazione interfaccia utente,proprietà e eventi
- Automazione interfaccia utente,eventi e proprietà
- proprietà,informazioni su
- proprietà,identificatori
- proprietà,valori
- proprietà,eventi
- eventi, proprietà
- proprietà, dinamica
- proprietà dinamiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58267fae50fe71c320b334c35b8da7831657e00bdd1b222db596addd40f3afef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117745031"
---
# <a name="ui-automation-properties-overview"></a>Cenni preliminari sulle proprietà di automazione interfaccia utente

I provider Automazione interfaccia utente Microsoft espongono proprietà Automazione interfaccia utente elementi. Le proprietà consentono alle applicazioni client di recuperare informazioni sui controlli.

Automazione interfaccia utente due tipi diversi di proprietà: le proprietà degli elementi *di automazione* e *il pattern di controllo appropriato.* Le proprietà degli elementi di automazione sono costituite da un set comune di proprietà, ad esempio Name, AcceleratorKey e ClassName, esposte da tutti gli elementi Automazione interfaccia utente, indipendentemente dal tipo di controllo. La maggior parte delle proprietà degli elementi di automazione sono valori statici.

Le proprietà del pattern di controllo sono quelle esposte da un controllo che supporta un pattern di controllo specifico. Ogni pattern di controllo ha un set corrispondente di proprietà del pattern di controllo che il controllo deve esporre. Ad esempio, un controllo che supporta il pattern di controllo [Grid](uiauto-implementinggrid.md) espone le proprietà ColumnCount e RowCount. La maggior parte delle proprietà del pattern di controllo sono valori dinamici.

In questo argomento sono contenute le sezioni seguenti.

-   [Identificatori di proprietà](#property-identifiers)
-   [Valori delle proprietà](#property-values)
-   [Proprietà ed eventi](#properties-and-events)
-   [Argomenti correlati](#related-topics)

## <a name="property-identifiers"></a>Identificatori di proprietà

Ogni proprietà è identificata da un valore numerico **PROPERTYID** denominato *identificatore* di proprietà (ID). I provider e i client usano gli ID numerici nelle chiamate al metodo, ad esempio [**IRawElementProviderAdviseEvents::AdviseEventAdded**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovideradviseevents-adviseeventadded) e [**IUIAutomationElement::GetCachedPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue) per identificare le richieste di proprietà. Per una descrizione dettagliata di ogni Automazione interfaccia utente proprietà, inclusi il tipo di dati e il valore predefinito di ogni proprietà, vedere [Identificatori di proprietà](uiauto-entry-propids.md).

## <a name="property-values"></a>Valori della proprietà

Tutte le proprietà sono di sola lettura, anche se alcune possono essere modificate usando metodi che agiscono sul controllo, ad esempio [**IDockProvider::SetDockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-setdockposition) (provider) o [**IUIAutomationDockPattern::SetDockPosition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationdockpattern-setdockposition) (client).

Per informazioni sul recupero di valori di proprietà, vedere Recupero di proprietà [da Automazione interfaccia utente elementi](uiauto-propertiesforclients.md).

## <a name="properties-and-events"></a>Proprietà ed eventi

Strettamente associato alle proprietà in Automazione interfaccia utente è il concetto di *eventi di proprietà modificate.* Per le proprietà dinamiche, un'applicazione client deve essere in grado di sapere che il valore di una proprietà è stato modificato, in modo da poter aggiornare la cache delle informazioni o reagire alle nuove informazioni in un altro modo. I client possono registrarsi per restare in ascolto degli eventi di proprietà modificati in qualsiasi proprietà.

I provider generano eventi quando un elemento nell'interfaccia utente cambia. Ad esempio, se una casella di controllo è selezionata o deselezionata, viene generato un evento di modifica della proprietà dall'implementazione del provider del pattern di controllo [Toggle.](uiauto-implementingtoggle.md) I provider possono generare gli eventi in modo selettivo, a seconda che i client siano in ascolto di eventi oppure di eventi specifici.

Non tutte le modifiche di proprietà generano eventi. Questo dipende totalmente dall'implementazione del provider di automazione interfaccia utente per l'elemento. Ad esempio, i provider proxy standard per le caselle di riepilogo non generano un evento di modifica della proprietà quando la proprietà Selection cambia. In questo caso, l'applicazione deve restare in ascolto dell'evento generato quando cambia la selezione ([**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)).

I client sono in ascolto degli eventi sottoscrivendoli, come descritto in Sottoscrizione di Automazione interfaccia utente [eventi](uiauto-eventsforclients.md). Per gli eventi di modifica delle proprietà in particolare, i client devono implementare [**IUIAutomationPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) e passare l'interfaccia a [**IUIAutomation::AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler) o [**IUIAutomation::AddPropertyChangedEventHandlerNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[**Getcurrentpropertyvalue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue)
</dt> <dt>

[**GetCurrentPropertyValueEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex)
</dt> <dt>

[**Getcachedpropertyvalue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue)
</dt> <dt>

[**GetCachedPropertyValueEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalueex)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari sugli eventi di automazione interfaccia utente](uiauto-eventsoverview.md)
</dt> </dl>

 

 




