---
title: Sottoscrizione degli eventi di automazione interfaccia utente
description: Automazione interfaccia utente Microsoft consente ai client di sottoscrivere gli eventi di interesse. Questa funzionalità consente di migliorare le prestazioni eliminando la necessità di eseguire continuamente il polling degli elementi dell'interfaccia utente nel sistema per verificare se sono state apportate modifiche alle informazioni, alla struttura o allo stato.
ms.assetid: 7019ecb8-6123-4e00-926c-6725d7e71385
keywords:
- client, eventi di automazione interfaccia utente
- client, eventi per l'automazione interfaccia utente
- Automazione interfaccia utente, eventi per i client
- Automazione interfaccia utente, eventi client
- Automazione interfaccia utente, sottoscrizione di eventi
- Automazione interfaccia utente, metodi di sottoscrizione
- Automazione interfaccia utente, esempi di codice
- Automazione interfaccia utente, esempi
- Automazione interfaccia utente, esempi
- sottoscrizione a eventi di automazione interfaccia utente
- eventi, sottoscrizione di automazione interfaccia utente
- Esempi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d9a89df1b9d2afc401e07b6cd77d1307d912f11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330359"
---
# <a name="subscribing-to-ui-automation-events"></a>Sottoscrizione degli eventi di automazione interfaccia utente

Automazione interfaccia utente Microsoft consente ai client di sottoscrivere gli eventi di interesse. Questa funzionalità consente di migliorare le prestazioni eliminando la necessità di eseguire continuamente il polling degli elementi dell'interfaccia utente nel sistema per verificare se sono state apportate modifiche alle informazioni, alla struttura o allo stato.

Una maggiore efficienza è ottenuta anche grazie alla possibilità di restare in ascolto di eventi solo in un ambito definito. Un client può ad esempio restare in ascolto delle modifiche di selezione di un elemento di un elenco, nell'elenco stesso o in un'intera finestra di dialogo.

> [!Note]  
> Non presupporre che tutti gli eventi possibili vengano generati da un provider di automazione interfaccia utente. Non tutte le modifiche alle proprietà, ad esempio, determinano la generazione di eventi da parte dei provider proxy standard per i controlli Windows Form e Microsoft Win32.

 

Per una visualizzazione più ampia degli eventi di automazione interfaccia utente, vedere [Cenni preliminari sugli eventi di automazione interfaccia utente](uiauto-eventsoverview.md).

> [!Note]  
> Prima di implementare un gestore eventi, è necessario conoscere i problemi di threading descritti in [informazioni sui problemi di threading](uiauto-threading.md).

 

In questo argomento sono contenute le sezioni seguenti.

-   [Registrazione di gestori eventi](#registering-event-handlers)
-   [esempi](#examples)
-   [Argomenti correlati](#related-topics)

## <a name="registering-event-handlers"></a>Registrazione di gestori eventi

Le applicazioni client sottoscrivono eventi di un particolare tipo registrando un gestore eventi, usando uno dei metodi [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) seguenti.



| Metodo di sottoscrizione                                                                                                                                                                                                | Tipo evento       | Interfaccia di callback                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------------------------------------------------------------------------------------------------|
| [**AddFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addfocuschangedeventhandler)                                                                                                                            | Modifica dello stato attivo     | [**IUIAutomationFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler)         |
| [**AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler), [ **AddPropertyChangedEventHandlerNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray) | Modifica proprietà  | [**IUIAutomationPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler)   |
| [**AddStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addstructurechangedeventhandler)                                                                                                                    | Modifica struttura | [**IUIAutomationStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationstructurechangedeventhandler) |
| [**AddNotificationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation5-addnotificationeventhandler)                                                                                                                           | Notifica     | [**IUIAutomationNotificationEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationnotificationeventhandler)         |
| [**AddAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addautomationeventhandler)                                                                                                                                | Altri eventi     | [**IUIAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationeventhandler)                                 |



 

Quando un client aggiunge un gestore eventi per tutti i discendenti [**( \_ discendenti TreeScope**](/windows/desktop/api/UIAutomationClient/ne-uiautomationclient-treescope)), l'automazione interfaccia utente aggiunge un solo gestore per la radice del sottoalbero e il gestore resta in attesa su tutti i discendenti. L'automazione interfaccia utente non aggiunge i gestori eventi in modo ricorsivo.

Quando un client chiama il metodo [**IUIAutomation:: RemoveAllEventHandlers**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removealleventhandlers) , l'automazione interfaccia utente rimuove tutti i gestori eventi dal processo client.

Per ricevere e gestire gli eventi, si implementa un oggetto di gestione degli eventi che espone un'interfaccia di callback ed è necessario registrare l'oggetto chiamando un metodo di registrazione eventi, ad esempio [**IUIAutomation:: AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler). L'interfaccia di callback ha un solo metodo; Automazione interfaccia utente chiama questo metodo quando l'evento viene elaborato.

Al momento dell'arresto o quando gli eventi di automazione interfaccia utente non sono più di interesse per l'applicazione, i client di automazione interfaccia utente devono chiamare uno o più dei seguenti metodi [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) .

> [!Note]  
> Un client di automazione interfaccia utente non deve usare più thread per aggiungere o rimuovere i gestori eventi. Un comportamento imprevisto può verificarsi se un gestore eventi viene aggiunto o rimosso mentre un altro viene aggiunto o rimosso nello stesso processo client.

 



| Metodo                                                                                                | Descrizione                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RemoveAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removeautomationeventhandler)             | Annulla la registrazione di un gestore eventi registrato utilizzando [**AddAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addautomationeventhandler).                                                                                                                                  |
| [**RemoveFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removefocuschangedeventhandler)         | Annulla la registrazione di un gestore eventi registrato utilizzando [**AddFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addfocuschangedeventhandler).                                                                                                                              |
| [**RemovePropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removepropertychangedeventhandler)   | Annulla la registrazione di un gestore eventi registrato tramite [**AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler) o [**AddPropertyChangedEventHandlerNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray). |
| [**RemoveStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removestructurechangedeventhandler) | Annulla la registrazione di un gestore eventi registrato utilizzando [**AddStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addstructurechangedeventhandler).                                                                                                                      |
| [**RemoveNotificationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation5-removenotificationeventhandler)        | Annulla la registrazione di un gestore eventi registrato da Weas usando [**AddNotificationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation5-addnotificationeventhandler).                                                                                                                            |
| [**RemoveAllEventHandlers**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removealleventhandlers)                         | Annulla la registrazione di tutti i gestori eventi registrati.                                                                                                                                                                                                                                      |



 

È possibile recapitare un evento a un gestore eventi dopo che è stata annullata la sottoscrizione del gestore, se l'evento viene ricevuto simultaneamente con la richiesta di annullare la sottoscrizione dell'evento. La procedura consigliata consiste nel seguire lo standard Component Object Model (COM) ed evitare di eliminare definitivamente l'oggetto gestore eventi fino a quando il conteggio dei riferimenti non raggiunge zero. L'eliminazione definitiva di un gestore eventi dopo l'annullamento della sottoscrizione per gli eventi potrebbe causare una violazione di accesso se un evento viene recapitato in ritardo.

## <a name="examples"></a>Esempio

Per esempi di codice che illustrano come gestire gli eventi di automazione interfaccia utente, vedere [come implementare i gestori eventi](uiauto-howto-implement-event-handlers.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sugli eventi di automazione interfaccia utente](uiauto-eventsoverview.md)
</dt> <dt>

[Informazioni sui problemi di threading](uiauto-threading.md)
</dt> </dl>

 

 




