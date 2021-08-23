---
title: Sottoscrizione a Automazione interfaccia utente eventi
description: Microsoft Automazione interfaccia utente consente ai client di sottoscrivere gli eventi di interesse. Questa funzionalità migliora le prestazioni eliminando la necessità di eseguire continuamente il polling degli elementi dell'interfaccia utente nel sistema per verificare se sono state modificate informazioni, struttura o stato.
ms.assetid: 7019ecb8-6123-4e00-926c-6725d7e71385
keywords:
- client, Automazione interfaccia utente eventi
- client, eventi per Automazione interfaccia utente
- Automazione interfaccia utente,eventi per i client
- Automazione interfaccia utente, eventi client
- Automazione interfaccia utente,sottoscrizione a eventi
- Automazione interfaccia utente, metodi di sottoscrizione
- Automazione interfaccia utente,esempi di codice
- Automazione interfaccia utente,esempi
- Automazione interfaccia utente,esempi
- sottoscrizione a eventi di automazione interfaccia utente
- eventi, Automazione interfaccia utente sottoscrizione
- Esempi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a0e8dd4cb2d810ad8423c1fa4f75020a9489ceb72acbe1483cb439e943b5676
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119505301"
---
# <a name="subscribing-to-ui-automation-events"></a>Sottoscrizione a Automazione interfaccia utente eventi

Microsoft Automazione interfaccia utente consente ai client di sottoscrivere gli eventi di interesse. Questa funzionalità migliora le prestazioni eliminando la necessità di eseguire continuamente il polling degli elementi dell'interfaccia utente nel sistema per verificare se sono state modificate informazioni, struttura o stato.

Una maggiore efficienza è ottenuta anche grazie alla possibilità di restare in ascolto di eventi solo in un ambito definito. Ad esempio, un client può restare in ascolto delle modifiche di selezione in un elemento di un elenco, nell'elenco stesso o in un'intera finestra di dialogo.

> [!Note]  
> Non presupporre che tutti gli eventi possibili siano generati da un provider Automazione interfaccia utente. Ad esempio, non tutte le modifiche alle proprietà causano la generare eventi dai provider proxy standard per i controlli Windows Form e Microsoft Win32.

 

Per una visualizzazione più ampia degli Automazione interfaccia utente, vedere Panoramica [Automazione interfaccia utente eventi](uiauto-eventsoverview.md).

> [!Note]  
> Prima di implementare un gestore eventi, è necessario avere familiarità con i problemi di threading descritti in [Informazioni sui problemi di threading.](uiauto-threading.md)

 

In questo argomento sono contenute le sezioni seguenti.

-   [Registrazione di gestori eventi](#registering-event-handlers)
-   [esempi](#examples)
-   [Argomenti correlati](#related-topics)

## <a name="registering-event-handlers"></a>Registrazione di gestori eventi

Le applicazioni client sottoscriveno eventi di un particolare tipo registrando un gestore eventi, usando uno dei metodi [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) seguenti.



| Metodo subscription                                                                                                                                                                                                | Tipo evento       | Interfaccia di callback                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------------------------------------------------------------------------------------------------|
| [**AddFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addfocuschangedeventhandler)                                                                                                                            | Modifica dello stato attivo     | [**IUIAutomationFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler)         |
| [**AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler), [ **AddPropertyChangedEventHandlerNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray) | Modifica proprietà  | [**IUIAutomationPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler)   |
| [**AddStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addstructurechangedeventhandler)                                                                                                                    | Modifica struttura | [**IUIAutomationStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationstructurechangedeventhandler) |
| [**AddNotificationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation5-addnotificationeventhandler)                                                                                                                           | Notifica     | [**IUIAutomationNotificationEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationnotificationeventhandler)         |
| [**AddAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addautomationeventhandler)                                                                                                                                | Altri eventi     | [**IUIAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationeventhandler)                                 |



 

Quando un client aggiunge un gestore eventi per tutti i discendenti [**(TreeScope \_ Descendants),**](/windows/desktop/api/UIAutomationClient/ne-uiautomationclient-treescope)Automazione interfaccia utente aggiunge un solo gestore per la radice del sottoalto e il gestore è in ascolto su tutti i discendenti. Automazione interfaccia utente non aggiunge gestori eventi in modo ricorsivo.

Quando un client chiama il [**metodo IUIAutomation::RemoveAllEventHandlers,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removealleventhandlers) Automazione interfaccia utente rimuove tutti i gestori eventi dal processo client.

Per ricevere e gestire gli eventi, implementare un oggetto di gestione degli eventi che espone un'interfaccia di callback ed è necessario registrare l'oggetto chiamando un metodo di registrazione degli eventi, ad esempio [**IUIAutomation::AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler). L'interfaccia di callback ha un solo metodo. Automazione interfaccia utente chiama questo metodo quando viene elaborato l'evento .

All'arresto o quando Automazione interfaccia utente eventi non sono più di interesse per l'applicazione, i client Automazione interfaccia utente devono chiamare uno o più dei metodi [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) seguenti.

> [!Note]  
> Un Automazione interfaccia utente client non deve usare più thread per aggiungere o rimuovere gestori eventi. Un comportamento imprevisto può verificarsi se un gestore eventi viene aggiunto o rimosso mentre un altro viene aggiunto o rimosso nello stesso processo client.

 



| Metodo                                                                                                | Descrizione                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RemoveAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removeautomationeventhandler)             | Annulla la registrazione di un gestore eventi registrato tramite [**AddAutomationEventHandler.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addautomationeventhandler)                                                                                                                                  |
| [**RemoveFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removefocuschangedeventhandler)         | Annulla la registrazione di un gestore eventi registrato tramite [**AddFocusChangedEventHandler.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addfocuschangedeventhandler)                                                                                                                              |
| [**RemovePropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removepropertychangedeventhandler)   | Annulla la registrazione di un gestore eventi registrato usando [**AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler) o [**AddPropertyChangedEventHandlerNativeArray.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray) |
| [**RemoveStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removestructurechangedeventhandler) | Annulla la registrazione di un gestore eventi registrato tramite [**AddStructureChangedEventHandler.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addstructurechangedeventhandler)                                                                                                                      |
| [**RemoveNotificationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation5-removenotificationeventhandler)        | Annulla la registrazione di un gestore eventi registrato con [**AddNotificationEventHandler.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation5-addnotificationeventhandler)                                                                                                                            |
| [**RemoveAllEventHandlers**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removealleventhandlers)                         | Annulla la registrazione di tutti i gestori eventi registrati.                                                                                                                                                                                                                                      |



 

È possibile che un evento sia recapitato a un gestore eventi dopo che il gestore è stato annullato, se l'evento viene ricevuto contemporaneamente alla richiesta di annullamento della sottoscrizione dell'evento. La procedura consigliata consiste nel seguire lo standard Component Object Model (COM) ed evitare di eliminare l'oggetto gestore eventi fino a quando il conteggio dei riferimenti non ha raggiunto lo zero. L'eliminazione di un gestore eventi immediatamente dopo l'annullamento della sottoscrizione degli eventi può comportare una violazione di accesso se un evento viene recapitato in ritardo.

## <a name="examples"></a>Esempio

Per esempi di codice che illustrano come gestire Automazione interfaccia utente eventi, vedere [Come implementare gestori eventi.](uiauto-howto-implement-event-handlers.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sugli eventi di automazione interfaccia utente](uiauto-eventsoverview.md)
</dt> <dt>

[Informazioni sui problemi di threading](uiauto-threading.md)
</dt> </dl>

 

 




