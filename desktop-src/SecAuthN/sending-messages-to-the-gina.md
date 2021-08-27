---
description: Winlogon invia messaggi all'applicazione GINA mentre vengono visualizzate le finestre di dialogo. Questi messaggi sono tutti incapsulati nel messaggio di firma di accesso condiviso WM WLX \_ \_ come indicato di seguito.
ms.assetid: 3da1c3d2-5116-47c3-98e4-f29b33693c69
title: Invio di messaggi all'applicazione GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb52da6a2a66d901207485ed97592a97286902ba51c54ec4924240ab9403a885
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918320"
---
# <a name="sending-messages-to-the-gina"></a>Invio di messaggi all'applicazione GINA

[*Winlogon invia*](../secgloss/w-gly.md) messaggi all'applicazione [*GINA*](../secgloss/g-gly.md) mentre vengono visualizzate le finestre di dialogo. Questi messaggi sono tutti incapsulati nel messaggio di firma di accesso condiviso WM WLX \_ \_ come indicato di seguito.



| Tipo di sequenza di attenzione sicura nel parametro wParam | Descrizione                                                                                                                                   |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| WLX \_ SAS \_ TYPE CTRL \_ \_ \_ ALT+CANC                     | Indica che è stata ricevuta una sequenza di tasti CTRL+ALT+CANC.                                                                                      |
| WLX \_ SAS \_ TYPE \_ SC \_ INSERT                         | Indica che un [*smart card*](../secgloss/s-gly.md) è stato inserito in un dispositivo compatibile. |
| WLX \_ SAS \_ TYPE \_ SC \_ REMOVE                         | Indica che un smart card è stato rimosso da un dispositivo compatibile.                                                                        |
| DISCONNESSIONE \_ UTENTE TIPO SAS WLX \_ \_ \_                       | Indica che un utente ha richiesto la disconnessione.                                                                                                       |
| TIMEOUT \_ \_ \_ SCRNSVR DI TIPO WLX SAS \_                   | Indica che il screen saver deve essere eseguito a causa della mancanza di input dell'utente.                                                                      |
| TIMEOUT DEL TIPO \_ DI FIRMA DI ACCESSO \_ CONDIVISO WLX \_                            | Indica che non è stato ricevuto alcun input dell'utente entro il periodo di timeout specificato.                                                               |



 

Per timeout e disconnessioni, Winlogon chiuderà la finestra di dialogo dopo l'invio del messaggio. Questo messaggio viene inviato in modo che l'operazione della finestra di dialogo possa rispondere in modo utile, ad esempio chiudendo se si è verificata una disconnessione.

Per i timeout di input, la finestra di dialogo viene chiusa con il codice WLX \_ DLG \_ INPUT \_ TIMEOUT.

Per screen saver timeout, la finestra di dialogo viene chiusa con il codice WLX \_ DLG \_ SCREEN \_ SAVER \_ TIMEOUT.

Per le disconnessioni, l'operazione della finestra di dialogo viene chiusa con il codice WLX \_ DLG \_ USER \_ LOGOFF.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Inizializzazione di Winlogon](initializing-winlogon.md)
</dt> <dt>

[Stati di Winlogon](winlogon-states.md)
</dt> <dt>

[Operazioni di timeout del servizio Della finestra di dialogo supportate](supported-dialog-box-service-time-out-operations.md)
</dt> <dt>

[Funzioni di supporto di Winlogon](authentication-functions.md)
</dt> </dl>

 

 
