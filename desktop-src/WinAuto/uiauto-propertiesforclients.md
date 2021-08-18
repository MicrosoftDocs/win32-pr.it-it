---
title: Recupero di proprietà da Automazione interfaccia utente elementi
description: Le proprietà degli oggetti IUIAutomationElement contengono informazioni sugli elementi dell'interfaccia utente, in genere i controlli.
ms.assetid: e358fd67-22d0-4e43-a138-8afcc45f130e
keywords:
- client, recupero Automazione interfaccia utente elementi
- client, Automazione interfaccia utente elementi
- client, proprietà
- client, recupero di proprietà
- client, Automazione interfaccia utente proprietà
- Automazione interfaccia utente,recupero di elementi
- Automazione interfaccia utente,elements
- Automazione interfaccia utente,properties
- Automazione interfaccia utente, recupero di proprietà
- recupero di proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbbe524e6f82f8c7dba018b24895ade54ced3e6a4632e1caefed410753b56fab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118564372"
---
# <a name="retrieving-properties-from-ui-automation-elements"></a>Recupero di proprietà da Automazione interfaccia utente elementi

Le proprietà degli [**oggetti IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) contengono informazioni sugli elementi dell'interfaccia utente, in genere i controlli. Le proprietà di un elemento sono generiche. ciò significa che non è specifico di un tipo di controllo. Le proprietà specifiche del controllo di un elemento vengono esposte dalle relative interfacce del pattern di controllo.

Le Automazione interfaccia utente microsoft sono di sola lettura. Per impostare le proprietà di un controllo, è necessario usare i metodi del pattern di controllo appropriato. Ad esempio, usare [**IUIAutomationScrollPattern::Scroll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationscrollpattern-scroll) per modificare i valori di posizione di una finestra di scorrimento.

Per migliorare le prestazioni, i valori delle proprietà dei controlli e dei pattern di controllo possono essere memorizzati nella cache quando vengono recuperati gli elementi. Per altre informazioni, vedere [Proprietà Caching Automazione interfaccia utente e Pattern di controllo.](uiauto-cachingforclients.md)

In questo argomento sono contenute le sezioni seguenti.

-   [ID di proprietà](#property-ids)
-   [Condizioni della proprietà](#property-conditions)
-   [Recupero di proprietà](#retrieving-properties)
-   [Valori di proprietà predefiniti](#default-property-values)
-   [Argomenti correlati](#related-topics)

## <a name="property-ids"></a>ID di proprietà

Gli identificatori di proprietà sono definiti in Uiautomationclient.h. Vengono usate per specificare le proprietà quando si sottoscriveno eventi di modifica delle proprietà, si recuperano i valori delle proprietà e si creano condizioni di proprietà. Gli identificatori di proprietà identificano anche la proprietà modificata quando viene chiamato [**IUIAutomationPropertyChangedEventHandler::HandlePropertyChangedEvent.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationpropertychangedeventhandler-handlepropertychangedevent)

Per un elenco di identificatori Automazione interfaccia utente proprietà, vedere [Identificatori di proprietà.](uiauto-entry-propids.md)

## <a name="property-conditions"></a>Condizioni della proprietà

Gli ID proprietà vengono usati nella costruzione di oggetti [**IUIAutomationPropertyCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertycondition) usati per trovare Automazione interfaccia utente elementi. Ad esempio, potrebbe essere necessario trovare un elemento con un determinato nome o tutti i controlli abilitati. Ogni condizione di proprietà specifica un identificatore di proprietà e il valore che la proprietà deve corrispondere.

Per altre informazioni, vedere gli argomenti di riferimento riportati di seguito:

-   [**IUIAutomation::CreatePropertyCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertycondition)
-   [**IUIAutomation::CreatePropertyConditionEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertyconditionex)
-   [**IUIAutomationElement::FindFirst**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst)
-   [**IUIAutomationElement::FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall)

## <a name="retrieving-properties"></a>Recupero di proprietà

Alcune proprietà generiche e tutte le proprietà del pattern di controllo sono disponibili come proprietà [**nell'interfaccia IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) o del pattern di controllo e possono essere recuperate usando una funzione di accesso, ad esempio [**IUIAutomationElement::CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) o [**CachedDockPosition.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationdockpattern-get_cacheddockposition)

Inoltre, qualsiasi proprietà corrente o memorizzata nella cache (diversa dalle proprietà del pattern di controllo) può essere recuperata usando uno dei metodi seguenti:

-   [**Getcurrentpropertyvalue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue)
-   [**GetCurrentPropertyValueEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex)
-   [**Getcachedpropertyvalue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue)
-   [**GetCachedPropertyValueEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalueex)

Questi metodi offrono prestazioni leggermente migliori e l'accesso alla gamma completa di proprietà. Tuttavia, i valori vengono restituiti nelle [**strutture VARIANT,**](/windows/win32/api/oaidl/ns-oaidl-variant) mentre le singole funzioni di accesso alle proprietà ese ciascuna esegue il cast del valore al tipo appropriato.

## <a name="default-property-values"></a>Valori di proprietà predefiniti

Se un provider Automazione interfaccia utente non implementa una proprietà, Automazione interfaccia utente può fornire un valore predefinito. Ad esempio, se il provider per un controllo non supporta la proprietà identificata da [**\_ UIA HelpTextPropertyId,**](uiauto-automation-element-propids.md)Automazione interfaccia utente restituisce una stringa vuota. Analogamente, se il provider non supporta la proprietà identificata da [**\_ UIA IsDockPatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md), Automazione interfaccia utente restituisce **FALSE.**

La differenza tra [**IUIAutomationElement::GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) e [**GetCurrentPropertyValueEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex) (e tra coppie simili di metodi) è che il metodo "Ex" può specificare che non deve essere restituito alcun valore predefinito. In questo caso, il valore restituito è una costante univoca speciale, che indica che la proprietà non è supportata. Quando riceve questo valore, l'applicazione può fornire il proprio valore o semplicemente ignorare la proprietà .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sulle proprietà di automazione interfaccia utente](uiauto-propertiesoverview.md)
</dt> <dt>

[Identificatori di proprietà](uiauto-entry-propids.md)
</dt> </dl>

 

 