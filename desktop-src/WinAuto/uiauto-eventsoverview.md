---
title: Cenni preliminari sugli eventi di automazione interfaccia utente
description: La notifica degli eventi di automazione interfaccia utente Microsoft è una funzionalità chiave per le tecnologie per l'accesso facilitato, quali utilità per la lettura dello schermo e ingrandimenti
ms.assetid: 0ded64ba-188e-427e-897f-4381237ace75
keywords:
- Automazione interfaccia utente, panoramica degli eventi
- Automazione interfaccia utente, categorie di eventi
- Automazione interfaccia utente, notifiche degli eventi
- notifiche di eventi
- eventi, categorie
- eventi, notifiche degli eventi
- Eventi di modifica delle proprietà
- Eventi azione elemento
- Eventi di modifica della struttura
- Eventi di modifica del desktop globale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9ddd61ed72ae0e92a13f6b59b493427fd7be421
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337662"
---
# <a name="ui-automation-events-overview"></a>Cenni preliminari sugli eventi di automazione interfaccia utente

La notifica degli eventi di automazione interfaccia utente Microsoft è una funzionalità chiave per le tecnologie per l'accesso facilitato, quali utilità per la lettura dello schermo e ingrandimenti Questi client di automazione interfaccia utente tengono traccia degli eventi generati dai provider di automazione interfaccia utente quando si verifica un evento nell'interfaccia utente e usano le informazioni per inviare notifiche agli utenti finali.

Una maggiore efficienza è ottenuta consentendo alle applicazioni provider di generare eventi in modo selettivo, se per tali eventi esistono sottoscrizioni di client, o di non generarne affatto, se nessun client è in attesa di eventi.

Gli eventi di automazione interfaccia utente ricadono nelle categorie seguenti.



| Categoria di eventi        | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Modifica proprietà       | Generato quando una proprietà dell'elemento o del pattern di controllo di automazione interfaccia utente viene modificata. Ad esempio, se un client deve monitorare una casella di controllo di un'applicazione, può registrarsi per restare in attesa di un evento di modifica della proprietà nella proprietà [**IUIAutomationTogglePattern:: CurrentToggleState**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtogglepattern-get_currenttogglestate) . Quando il controllo casella di controllo viene selezionato o deselezionato, il provider genera l'evento e il client può agire secondo necessità. |
| Azione elemento        | Generato quando viene apportata una modifica nei risultati dell'interfaccia utente dall'utente finale o dall'attività a livello di codice, ad esempio quando si fa clic su un pulsante o viene richiamato tramite [**IUIAutomationInvokePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern).                                                                                                                                                                                                                                                     |
| Modifica struttura      | Generato quando viene modificata la struttura dell'albero di automazione interfaccia utente. La struttura viene modificata quando nuovi elementi dell'interfaccia utente diventano visibili oppure vengono nascosti o rimossi dal desktop.                                                                                                                                                                                                                                                                                                              |
| Modifica globale desktop | Generato quando si verificano azioni di interesse globale per il client, ad esempio quando lo stato attivo passa da un elemento a un altro o quando si chiude una finestra.                                                                                                                                                                                                                                                                                                                      |
| Notifica          | Generato quando un'app chiama la funzione [**UiaRaiseNotificationEvent**](https://www.bing.com/search?q=**UiaRaiseNotificationEvent**) . [**NotificationKind**](/windows/win32/api/uiautomationcore/ne-uiautomationcore-notificationkind) indica il tipo di notifica.                                                                                                                                                                                                                                                 |



 

Alcuni eventi non indicano necessariamente che lo stato dell'interfaccia utente è cambiato. Se, ad esempio, l'utente esegue la tabulazione in un campo di immissione di testo e quindi fa clic su un pulsante per aggiornare il campo, viene generato un evento [**\_ \_ TextChangedEventId di testo UIA**](uiauto-event-ids.md) , anche se l'utente non ha modificato effettivamente il testo. Durante l'elaborazione di un evento, prima di eseguire un'azione può essere necessario per un'applicazione client verificare se sia effettivamente avvenuta una modifica.

I seguenti eventi possono essere generati anche se lo stato dell'interfaccia utente non è cambiato.

-   [**UIA \_ AutomationPropertyChangedEventId**](uiauto-event-ids.md) (a seconda della proprietà che è stata modificata)
-   [**\_ElementSelectedEventId SelectionItem di UIA \_**](uiauto-event-ids.md)
-   [**\_InvalidatedEventId selezione \_ UIA**](uiauto-event-ids.md)
-   [**\_TextChangedEventId testo \_ UIA**](uiauto-event-ids.md)

Per una descrizione di tutti gli eventi di automazione interfaccia utente, vedere [identificatori di evento](uiauto-event-ids.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sottoscrizione degli eventi di automazione interfaccia utente](uiauto-eventsforclients.md)
</dt> </dl>

 

 