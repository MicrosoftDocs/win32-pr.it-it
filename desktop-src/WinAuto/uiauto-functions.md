---
title: Funzioni per i provider
description: Questa sezione descrive le funzioni del provider di automazione interfaccia utente per le applicazioni Win32 Microsoft.
ms.assetid: 76012ec7-0114-4b6b-a35e-5cfde5b90230
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea0542c3d0b313e1bed8ec040924349e37a29fea
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299832"
---
# <a name="functions-for-providers"></a>Funzioni per i provider

Questa sezione descrive le funzioni del provider di automazione interfaccia utente per le applicazioni Win32 Microsoft.

## <a name="in-this-section"></a>Contenuto della sezione



| Funzione                                                                                                 | Descrizione                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UiaClientsAreListening**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaclientsarelistening)<br/>                       | Ottiene un valore che indica se un'applicazione client ha eseguito la sottoscrizione agli eventi di automazione interfaccia utente Microsoft.<br/>                                             |
| [**UiaDisconnectAllProviders**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiadisconnectallproviders)<br/>                         | Rilascia tutte le risorse di automazione interfaccia utente mantenute da tutti i provider associati al processo chiamante. <br/>                                               |
| [**UiaDisconnectProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiadisconnectprovider)<br/>                                 | Rilascia tutti i riferimenti che un determinato provider possiede agli oggetti di automazione interfaccia utente.<br/>                                                                      |
| [**UiaGetReservedMixedAttributeValue**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservedmixedattributevalue)<br/> | Recupera un valore riservato che indica che il valore di un attributo di testo di automazione interfaccia utente varia in un intervallo di testo.<br/>                                      |
| [**UiaGetReservedNotSupportedValue**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservednotsupportedvalue)<br/>     | Recupera un valore riservato che indica che non è supportata una proprietà di automazione interfaccia utente o un attributo di testo.<br/>                                               |
| [**UiaHostProviderFromHwnd**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahostproviderfromhwnd)<br/>                     | Ottiene il provider host per una finestra.<br/>                                                                                                                    |
| [**UiaIAccessibleFromProvider**](/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiaiaccessiblefromprovider)<br/>                   | Recupera un'implementazione di [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) che fornisce dati di Microsoft Active Accessibility per conto di un provider di automazione interfaccia utente.<br/> |
| [**UiaProviderForNonClient**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaproviderfornonclient)<br/>                     | Ottiene il provider per l'intera area non client di una finestra o per un controllo nell'area non client di una finestra.<br/>                                      |
| [**UiaProviderFromIAccessible**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaproviderfromiaccessible)<br/>               | Crea un provider di automazione interfaccia utente basato sull'oggetto Active Accessibility Microsoft specificato.<br/>                                                          |
| [**UiaRaiseAsyncContentLoadedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseasynccontentloadedevent)<br/>     | Chiamato da un provider per notificare al core di automazione interfaccia utente che il contenuto viene caricato in modo asincrono.<br/>                                                      |
| [**UiaRaiseAutomationEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseautomationevent)<br/>                     | Notifica ai listener di un evento.<br/>                                                                                                                         |
| [**UiaRaiseAutomationPropertyChangedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseautomationpropertychangedevent)<br/>    | Chiamato dai provider per notificare al core di automazione interfaccia utente che una proprietà dell'elemento è stata modificata.<br/>                                                              |
| [**UiaRaiseChangesEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisechangesevent)<br/>                           | Chiamato dai provider per notificare al core di automazione interfaccia utente che si è verificata una modifica.<br/>                                                                        |
| [**UiaRaiseNotificationEvent**](https://www.bing.com/search?q=**UiaRaiseNotificationEvent**)<br/>             | Chiamato dai provider per avviare un evento di notifica.<br/>                                                                                                   |
| [**UiaRaiseStructureChangedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisestructurechangedevent)<br/>         | Chiamato da un provider per notificare al nucleo di automazione interfaccia utente la modifica della struttura ad albero.<br/>                                                              |
| [**UiaRaiseTextEditTextChangedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisetextedittextchangedevent)<br/>   | Chiamato da un provider per notificare al nucleo di automazione interfaccia utente che un controllo testo ha modificato il testo a livello di codice.<br/>                                            |
| [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider)<br/>             | Ottiene un'interfaccia per il provider di automazione interfaccia utente per una finestra.<br/>                                                                                           |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Provider di automazione interfaccia utente](uiauto-entry-uiautoprovidersforwin32apps.md)
</dt> </dl>

 

