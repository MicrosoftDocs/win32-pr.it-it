---
title: Cenni preliminari sulle proprietà di automazione interfaccia utente
description: I provider di automazione interfaccia utente Microsoft espongono proprietà sugli elementi di automazione interfaccia utente. Le proprietà consentono alle applicazioni client di recuperare informazioni sui controlli.
ms.assetid: 35f017cb-f50a-4680-9f01-5079aa59da73
keywords:
- Automazione interfaccia utente, panoramica delle proprietà
- Automazione interfaccia utente, proprietà e eventi
- Automazione interfaccia utente, eventi e proprietà
- Proprietà, informazioni
- Proprietà, identificatori
- Proprietà, valori
- Proprietà, eventi
- eventi, proprietà
- Proprietà, dinamiche
- proprietà dinamiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0f4e5e1b29ae516059a531b17d50d0631282f82
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104220863"
---
# <a name="ui-automation-properties-overview"></a>Cenni preliminari sulle proprietà di automazione interfaccia utente

I provider di automazione interfaccia utente Microsoft espongono proprietà sugli elementi di automazione interfaccia utente. Le proprietà consentono alle applicazioni client di recuperare informazioni sui controlli.

Automazione interfaccia utente espone due tipi diversi di proprietà: le *proprietà degli elementi di automazione* e i pattern di *controllo*. Le proprietà degli elementi di automazione sono costituite da un set comune di proprietà, ad esempio Name, AcceleratorKey e NomeClasse, che sono esposte da tutti gli elementi di automazione interfaccia utente, indipendentemente dal tipo di controllo. La maggior parte delle proprietà degli elementi di automazione sono valori statici.

Le proprietà del pattern di controllo sono quelle esposte da un controllo che supporta un particolare pattern di controllo. Ogni pattern di controllo ha un set corrispondente di proprietà del pattern di controllo che il controllo deve esporre. Ad esempio, un controllo che supporta il pattern di controllo [Grid](uiauto-implementinggrid.md) espone le proprietà ColumnCount e RowCount. La maggior parte delle proprietà dei pattern di controllo sono valori dinamici.

In questo argomento sono contenute le sezioni seguenti.

-   [Identificatori di proprietà](#property-identifiers)
-   [Valori delle proprietà](#property-values)
-   [Proprietà ed eventi](#properties-and-events)
-   [Argomenti correlati](#related-topics)

## <a name="property-identifiers"></a>Identificatori di proprietà

Ogni proprietà è identificata da un valore numerico **PROPERTYID** denominato *identificatore di proprietà* (ID). I provider e i client utilizzano gli ID numerici nelle chiamate al metodo, ad esempio [**IRawElementProviderAdviseEvents:: AdviseEventAdded**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovideradviseevents-adviseeventadded) e [**IUIAutomationElement:: GetCachedPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue) per identificare le richieste di proprietà. Per una descrizione dettagliata di ogni identificatore di proprietà di automazione interfaccia utente, inclusi il tipo di dati e il valore predefinito di ogni proprietà, vedere [identificatori di proprietà](uiauto-entry-propids.md).

## <a name="property-values"></a>Valori della proprietà

Tutte le proprietà sono di sola lettura, sebbene alcune possano essere modificate utilizzando metodi che agiscono sul controllo, ad esempio [**IDockProvider:: SetDockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-setdockposition) (provider) o [**IUIAutomationDockPattern:: SetDockPosition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationdockpattern-setdockposition) (client).

Per informazioni sul recupero dei valori delle proprietà, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).

## <a name="properties-and-events"></a>Proprietà ed eventi

Strettamente associato alle proprietà in automazione interfaccia utente è il concetto di *eventi di modifica della proprietà*. Per le proprietà dinamiche, un'applicazione client necessita di un modo per capire che un valore di proprietà è stato modificato, in modo che possa aggiornare la cache delle informazioni o rispondere in altro modo alle nuove informazioni. I client possono eseguire la registrazione per restare in ascolto degli eventi di modifica della proprietà su qualsiasi proprietà.

I provider generano eventi quando viene modificato un elemento nell'interfaccia utente. Se, ad esempio, una casella di controllo è selezionata o deselezionata, viene generato un evento di modifica della proprietà dall'implementazione del provider del pattern di controllo di [attivazione/disattivazione](uiauto-implementingtoggle.md) . I provider possono generare gli eventi in modo selettivo, a seconda che i client siano in ascolto di eventi oppure di eventi specifici.

Non tutte le modifiche di proprietà generano eventi. Questo dipende totalmente dall'implementazione del provider di automazione interfaccia utente per l'elemento. Ad esempio, i provider di proxy standard per le caselle di riepilogo non generano un evento di modifica della proprietà quando la proprietà Selection viene modificata. In questo caso, l'applicazione deve rimanere in ascolto dell'evento generato quando la selezione cambia ([**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)).

I client restano in ascolto degli eventi sottoscrivendoli, come descritto in [sottoscrizione di eventi di automazione interfaccia utente](uiauto-eventsforclients.md). Per gli eventi di modifica delle proprietà in particolare, i client devono implementare [**IUIAutomationPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) e passare l'interfaccia a [**IUIAutomation:: AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler) o [**IUIAutomation:: AddPropertyChangedEventHandlerNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[**GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue)
</dt> <dt>

[**GetCurrentPropertyValueEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex)
</dt> <dt>

[**GetCachedPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue)
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

 

 




