---
description: Poiché ogni voce del servizio viene letta dal database dei servizi installati, SCM Crea un record del servizio per il servizio.
ms.assetid: c0ee43e2-af9b-4578-9017-46a5ed50b938
title: Elenco di record di servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1143625de977c7e5c488c5cc56620adc3a5454db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307213"
---
# <a name="service-record-list"></a>Elenco di record di servizio

Poiché ogni voce del servizio viene letta dal database dei servizi installati, SCM Crea un record del servizio per il servizio. Un record di servizio include:

-   Nome del servizio
-   Tipo di avvio (avvio automatico o richiesta-avvio)
-   Stato del servizio (vedere la struttura [**\_ dello stato del servizio**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) ) <dl> Tipo  
    Stato corrente  
    Codici di controllo accettabili  
    Codice di uscita  
    Hint Wait  
    </dl>
-   Pointer to dependency list

Il nome utente e la password di un account vengono specificati al momento dell'installazione del servizio. Il servizio SCM archivia il nome utente nel registro di sistema e la password in una parte sicura dell'autorità di protezione locale (LSA). L'amministratore di sistema può creare account con password senza scadenza. In alternativa, l'amministratore di sistema può creare account con password che scadono e gestiscono gli account cambiando periodicamente le password.

Il controllo SCM conserva due copie della password di un account utente, una password corrente e una password di backup. La password specificata la prima volta che il servizio viene installato viene archiviato come password corrente e la password di backup non viene inizializzata. Quando il servizio SCM tenta di eseguire il servizio nel contesto di sicurezza dell'account utente, usa la password corrente. Se la password corrente viene utilizzata correttamente, viene salvata anche come password di backup. Se la password viene modificata con la funzione [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) o l'utilità del pannello di controllo dei servizi, la nuova password viene archiviata come password corrente e la password precedente viene archiviata come password di backup. Se il controllo SCM tenta di avviare il servizio e la password corrente ha esito negativo, viene utilizzata la password di backup. Se la password di backup viene utilizzata correttamente, viene salvata come password corrente.

SCM aggiorna lo stato del servizio quando un servizio invia notifiche di stato tramite la funzione [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) . Gestione controllo servizi gestisce lo stato di un servizio driver eseguendo una query sul sistema di I/O, anziché ricevere notifiche di stato, come avviene da un servizio.

Un servizio può registrare informazioni sul tipo aggiuntive chiamando la funzione [**SetServiceBits**](/windows/desktop/api/Lmserver/nf-lmserver-setservicebits) . Le funzioni [**NetServerGetInfo**](/windows/desktop/api/lmserver/nf-lmserver-netservergetinfo) e [**NetServerEnum**](/windows/desktop/api/lmserver/nf-lmserver-netserverenum) ottengono i tipi di servizio supportati.

 

 
