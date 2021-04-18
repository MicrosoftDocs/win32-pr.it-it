---
title: Recupero di proprietà da elementi di automazione interfaccia utente
description: Le proprietà degli oggetti IUIAutomationElement contengono informazioni sugli elementi dell'interfaccia utente, in genere i controlli.
ms.assetid: e358fd67-22d0-4e43-a138-8afcc45f130e
keywords:
- client, acquisizione di elementi di automazione interfaccia utente
- client, elementi di automazione interfaccia utente
- client, proprietà
- client, recupero di proprietà
- client, proprietà di automazione interfaccia utente
- Automazione interfaccia utente, recupero di elementi
- Automazione interfaccia utente, elementi
- Automazione interfaccia utente, proprietà
- Automazione interfaccia utente, recupero di proprietà
- recupero di proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e199522dbefaa2f722a67b0ede57fe910b8ed63b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300267"
---
# <a name="retrieving-properties-from-ui-automation-elements"></a>Recupero di proprietà da elementi di automazione interfaccia utente

Le proprietà degli oggetti [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) contengono informazioni sugli elementi dell'interfaccia utente, in genere i controlli. Le proprietà di un elemento sono generiche. ovvero non è specifico di un tipo di controllo. Le proprietà specifiche del controllo di un elemento sono esposte dalle relative interfacce del pattern di controllo.

Le proprietà di automazione interfaccia utente Microsoft sono di sola lettura. Per impostare le proprietà di un controllo, è necessario usare i metodi del pattern di controllo appropriato. Usare, ad esempio, [**IUIAutomationScrollPattern:: scroll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationscrollpattern-scroll) per modificare i valori di posizione di una finestra di scorrimento.

Per migliorare le prestazioni, è possibile memorizzare nella cache i valori delle proprietà dei controlli e dei pattern di controllo quando vengono recuperati gli elementi. Per altre informazioni, vedere [memorizzazione nella cache delle proprietà e dei pattern di controllo di automazione interfaccia utente](uiauto-cachingforclients.md).

In questo argomento sono contenute le sezioni seguenti.

-   [ID di proprietà](#property-ids)
-   [Condizioni della proprietà](#property-conditions)
-   [Recupero di proprietà](#retrieving-properties)
-   [Valori di proprietà predefiniti](#default-property-values)
-   [Argomenti correlati](#related-topics)

## <a name="property-ids"></a>ID di proprietà

Gli identificatori di proprietà sono definiti in UIAutomationClient. h. Vengono usati per specificare le proprietà quando si sottoscrivono eventi di modifica di proprietà, si recuperano i valori delle proprietà e si creano condizioni di proprietà. Gli identificatori di proprietà identificano anche la proprietà che è stata modificata quando viene chiamato [**IUIAutomationPropertyChangedEventHandler:: HandlePropertyChangedEvent**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationpropertychangedeventhandler-handlepropertychangedevent) .

Per un elenco degli identificatori di proprietà di automazione interfaccia utente, vedere [identificatori di proprietà](uiauto-entry-propids.md).

## <a name="property-conditions"></a>Condizioni della proprietà

Gli ID di proprietà vengono usati nella costruzione di oggetti [**IUIAutomationPropertyCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertycondition) usati per trovare gli elementi di automazione interfaccia utente. Ad esempio, è possibile trovare un elemento con un determinato nome o tutti i controlli abilitati. Ogni condizione di proprietà specifica un identificatore di proprietà e il valore a cui deve corrispondere la proprietà.

Per altre informazioni, vedere gli argomenti di riferimento riportati di seguito:

-   [**IUIAutomation::CreatePropertyCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertycondition)
-   [**IUIAutomation::CreatePropertyConditionEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertyconditionex)
-   [**IUIAutomationElement:: FindFirst**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst)
-   [**IUIAutomationElement:: FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall)

## <a name="retrieving-properties"></a>Recupero di proprietà

Alcune proprietà generiche e tutte le proprietà del pattern di controllo sono disponibili come proprietà nell'interfaccia [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) o pattern di controllo e possono essere recuperate tramite una funzione di accesso, ad esempio [**IUIAutomationElement:: currentname**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) o [**CachedDockPosition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationdockpattern-get_cacheddockposition).

Inoltre, è possibile recuperare qualsiasi proprietà corrente o memorizzata nella cache (ad eccezione delle proprietà del pattern di controllo) utilizzando uno dei metodi seguenti:

-   [**GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue)
-   [**GetCurrentPropertyValueEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex)
-   [**GetCachedPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue)
-   [**GetCachedPropertyValueEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalueex)

Questi metodi offrono prestazioni leggermente migliori e l'accesso alla gamma completa di proprietà. Tuttavia, i valori vengono restituiti nelle strutture [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) , mentre le singole funzioni di accesso alle proprietà eseguono il cast del valore al tipo appropriato.

## <a name="default-property-values"></a>Valori di proprietà predefiniti

Se un provider di automazione interfaccia utente non implementa una proprietà, l'automazione interfaccia utente può fornire un valore predefinito. Ad esempio, se il provider per un controllo non supporta la proprietà identificata da [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md), l'automazione interfaccia utente restituisce una stringa vuota. Analogamente, se il provider non supporta la proprietà identificata da [**UIA \_ IsDockPatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md), automazione interfaccia utente restituisce **false**.

La differenza tra [**IUIAutomationElement:: GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) e [**GetCurrentPropertyValueEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex) (e tra coppie simili di metodi) consiste nel fatto che il metodo "ex" può specificare che non deve essere restituito alcun valore predefinito. In questo caso, il valore restituito è una costante univoca speciale, che indica che la proprietà non è supportata. Quando riceve questo valore, l'applicazione può fornire il proprio valore o semplicemente ignorare la proprietà.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sulle proprietà di automazione interfaccia utente](uiauto-propertiesoverview.md)
</dt> <dt>

[Identificatori di proprietà](uiauto-entry-propids.md)
</dt> </dl>

 

 