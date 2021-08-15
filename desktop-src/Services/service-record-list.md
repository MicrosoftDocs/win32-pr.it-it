---
description: Quando ogni voce del servizio viene letta dal database dei servizi installati, Gestione controllo servizi crea un record di servizio per il servizio.
ms.assetid: c0ee43e2-af9b-4578-9017-46a5ed50b938
title: Elenco dei record di servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ef0bdebed5e302b1dc59bea6494fd812ec506e7e6d2531634b2a6686b86bc98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888855"
---
# <a name="service-record-list"></a>Elenco dei record di servizio

Quando ogni voce del servizio viene letta dal database dei servizi installati, Gestione controllo servizi crea un record di servizio per il servizio. Un record di servizio include:

-   Nome del servizio
-   Tipo di avvio (avvio automatico o avvio su richiesta)
-   Stato del servizio (vedere la [**struttura \_ SERVICE STATUS)**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) <dl> Tipo  
    Stato corrente  
    Codici di controllo accettabili  
    Codice di uscita  
    Hint di attesa  
    </dl>
-   Pointer to dependency list

Il nome utente e la password di un account vengono specificati al momento dell'installazione del servizio. Gestione controllo servizi archivia il nome utente nel Registro di sistema e la password in una parte sicura dell'autorità di sicurezza locale (LSA). L'amministratore di sistema può creare account con password che non scadono mai. In alternativa, l'amministratore di sistema può creare account con password che scadono e gestire gli account modificando periodicamente le password.

Gestione controllo servizi conserva due copie della password di un account utente, una password corrente e una password di backup. La password specificata alla prima installazione del servizio viene archiviata come password corrente e la password di backup non viene inizializzata. Quando gestione controllo servizi tenta di eseguire il servizio nel contesto di sicurezza dell'account utente, usa la password corrente. Se la password corrente viene usata correttamente, viene salvata anche come password di backup. Se la password viene modificata con la funzione [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) o l'utilità del Pannello di controllo Servizi, la nuova password viene archiviata come password corrente e la password precedente viene archiviata come password di backup. Se Gestione controllo servizi tenta di avviare il servizio e la password corrente ha esito negativo, usa la password di backup. Se la password di backup viene usata correttamente, viene salvata come password corrente.

Gestione controllo servizi aggiorna lo stato del servizio quando un servizio invia notifiche di stato usando la [**funzione SetServiceStatus.**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) Gestione controllo servizi mantiene lo stato di un servizio driver tramite query sul sistema di I/O, anziché ricevere notifiche di stato, come da un servizio.

Un servizio può registrare informazioni aggiuntive sul tipo chiamando la [**funzione SetServiceBits.**](/windows/desktop/api/Lmserver/nf-lmserver-setservicebits) Le [**funzioni NetServerGetInfo**](/windows/desktop/api/lmserver/nf-lmserver-netservergetinfo) [**e NetServerEnum**](/windows/desktop/api/lmserver/nf-lmserver-netserverenum) ottengono i tipi di servizio supportati.

 

 
