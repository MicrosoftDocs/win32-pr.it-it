---
description: Winlogon invia messaggi a GINA mentre vengono visualizzate le finestre di dialogo. Questi messaggi sono tutti incapsulati nel messaggio di firma di accesso condiviso di WLX \_ WM \_ come indicato di seguito.
ms.assetid: 3da1c3d2-5116-47c3-98e4-f29b33693c69
title: Invio di messaggi a GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d2f7b5b0d8fbecafad0bcc36c84cf395813f767
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311602"
---
# <a name="sending-messages-to-the-gina"></a>Invio di messaggi a GINA

[*Winlogon*](../secgloss/w-gly.md) invia messaggi a [*Gina*](../secgloss/g-gly.md) mentre vengono visualizzate le finestre di dialogo. Questi messaggi sono tutti incapsulati nel messaggio di firma di accesso condiviso di WLX \_ WM \_ come indicato di seguito.



| Tipo di sequenza di attenzione sicura nel parametro wParam | Descrizione                                                                                                                                   |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| tipo di firma di accesso condiviso di WLX \_ \_ \_ CTRL \_ ALT \_ Canc                     | Indica che è stata ricevuta una sequenza di tasti CTRL + ALT + CANC.                                                                                      |
| tipo di firma di accesso condiviso di WLX \_ SAS \_ \_ \_                         | Indica che una [*Smart Card*](../secgloss/s-gly.md) è stata inserita in un dispositivo compatibile. |
| tipo di firma di accesso condiviso di WLX \_ \_ \_ SC \_ Remove                         | Indica che una smart card è stata rimossa da un dispositivo compatibile.                                                                        |
| \_disconnessione \_ utente tipo di SAS \_ wlx \_                       | Indica che un utente ha richiesto la disconnessione.                                                                                                       |
| \_ \_ \_ timeout SCRNSVR tipo SAS \_ di wlx                   | Indica che la screen saver deve essere eseguita a causa della mancanza di input dell'utente.                                                                      |
| \_ \_ timeout tipo di SAS di WLX \_                            | Indica che non è stato ricevuto alcun input da parte dell'utente entro il periodo di timeout specificato.                                                               |



 

Per i timeout e le disconnessioni, Winlogon chiude la finestra di dialogo dopo che il messaggio è stato inviato. Questo messaggio viene inviato in modo che l'operazione della finestra di dialogo possa rispondere in modo utile, ad esempio chiudendosi se si è verificata una disconnessione.

Per i timeout di input, la finestra di dialogo viene chiusa con il timeout di input del codice WLX \_ DLG \_ \_ .

Per screen saver i timeout, la finestra di dialogo viene chiusa con il timeout del codice WLX \_ DLG \_ Screen \_ saver \_ .

Per le disconnessioni, l'operazione della finestra di dialogo viene chiusa con \_ la \_ disconnessione utente del codice wlx DLG \_ .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Inizializzazione di Winlogon](initializing-winlogon.md)
</dt> <dt>

[Stati di Winlogon](winlogon-states.md)
</dt> <dt>

[Operazioni di Tempo di servizio della finestra di dialogo supportate](supported-dialog-box-service-time-out-operations.md)
</dt> <dt>

[Funzioni di supporto di Winlogon](authentication-functions.md)
</dt> </dl>

 

 
