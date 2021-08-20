---
title: Cenni preliminari sugli eventi di automazione interfaccia utente
description: La notifica Automazione interfaccia utente eventi di Microsoft è una funzionalità chiave per le tecnologie di assistive, ad esempio utilità per la lettura dello schermo e le lente di ingrandimento dello schermo.
ms.assetid: 0ded64ba-188e-427e-897f-4381237ace75
keywords:
- Automazione interfaccia utente,panoramica degli eventi
- Automazione interfaccia utente,categorie di eventi
- Automazione interfaccia utente,notifiche degli eventi
- notifiche di eventi
- eventi,categorie
- eventi, notifiche di eventi
- Eventi di modifica delle proprietà
- Eventi di azione degli elementi
- Eventi di modifica della struttura
- Eventi di modifica del desktop globale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ec99a479d390c72232f28521394b2d178f1ad76c913d72ec80aa0a4c93e0d57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859571"
---
# <a name="ui-automation-events-overview"></a>Cenni preliminari sugli eventi di automazione interfaccia utente

La notifica Automazione interfaccia utente eventi di Microsoft è una funzionalità chiave per le tecnologie di assistive, ad esempio utilità per la lettura dello schermo e le lente di ingrandimento dello schermo. Questi Automazione interfaccia utente client rilevano gli eventi generati dai provider Automazione interfaccia utente quando si verifica un evento nell'interfaccia utente e usano le informazioni per notificare agli utenti finali.

Una maggiore efficienza è ottenuta consentendo alle applicazioni provider di generare eventi in modo selettivo, se per tali eventi esistono sottoscrizioni di client, o di non generarne affatto, se nessun client è in attesa di eventi.

Gli eventi di automazione interfaccia utente ricadono nelle categorie seguenti.



| Categoria di eventi        | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Modifica proprietà       | Generato quando viene modificata una proprietà Automazione interfaccia utente elemento o pattern di controllo. Ad esempio, se un client deve monitorare un controllo casella di controllo dell'applicazione, può registrarsi per restare in ascolto di un evento di modifica della proprietà nella proprietà [**IUIAutomationTogglePattern::CurrentToggleState.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtogglepattern-get_currenttogglestate) Quando il controllo casella di controllo viene selezionato o deselezionato, il provider genera l'evento e il client può agire secondo necessità. |
| Azione elemento        | Generato quando una modifica nell'interfaccia utente risulta dall'utente finale o da un'attività a livello di codice, ad esempio quando un pulsante viene selezionato o richiamato tramite [**IUIAutomationInvokePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern).                                                                                                                                                                                                                                                     |
| Modifica struttura      | Generato quando cambia la struttura dell'Automazione interfaccia utente albero. La struttura viene modificata quando nuovi elementi dell'interfaccia utente diventano visibili oppure vengono nascosti o rimossi dal desktop.                                                                                                                                                                                                                                                                                                              |
| Modifica globale desktop | Generato quando si verificano azioni di interesse globale per il client, ad esempio quando lo stato attivo passa da un elemento a un altro o quando si chiude una finestra.                                                                                                                                                                                                                                                                                                                      |
| Notifica          | Generato quando un'app chiama la [**funzione UiaRaiseNotificationEvent.**](https://www.bing.com/search?q=**UiaRaiseNotificationEvent**) [**NotificationKind**](/windows/win32/api/uiautomationcore/ne-uiautomationcore-notificationkind) indica il tipo di notifica.                                                                                                                                                                                                                                                 |



 

Alcuni eventi non indicano necessariamente che lo stato dell'interfaccia utente è cambiato. Ad esempio, se l'utente fa clic su un campo di immissione di testo e quindi fa clic su un pulsante per aggiornare il campo, viene generato un evento [**\_ \_ TextChangedEventId**](uiauto-event-ids.md) dell'interfaccia utente, anche se l'utente non ha effettivamente modificato il testo. Durante l'elaborazione di un evento, prima di eseguire un'azione può essere necessario per un'applicazione client verificare se sia effettivamente avvenuta una modifica.

I seguenti eventi possono essere generati anche se lo stato dell'interfaccia utente non è cambiato.

-   [**Interfaccia \_ utente AutomationPropertyChangedEventId**](uiauto-event-ids.md) (a seconda della proprietà modificata)
-   [**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)
-   [**UIA \_ Selection \_ InvalidatedEventId**](uiauto-event-ids.md)
-   [**\_TextChangedEventId dell'interfaccia utenteA \_**](uiauto-event-ids.md)

Per una descrizione di tutti Automazione interfaccia utente eventi, vedere [Identificatori di evento](uiauto-event-ids.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sottoscrizione a eventi Automazione interfaccia utente eventi](uiauto-eventsforclients.md)
</dt> </dl>

 

 