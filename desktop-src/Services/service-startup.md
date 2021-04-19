---
description: Per avviare un servizio o un servizio driver, il programma di controllo del servizio utilizza la funzione StartService.
ms.assetid: 7d2ee779-1554-436a-a65c-f0322745f46a
title: Avvio del servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f5fcd9ee820357e75bf07649da8e6c5445d3f42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317677"
---
# <a name="service-startup"></a>Avvio del servizio

Per avviare un servizio o un servizio driver, il programma di controllo del servizio utilizza la funzione [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) . La funzione **StartService** ha esito negativo se il database è bloccato. In tal caso, il programma di controllo del servizio deve attendere alcuni secondi e chiamare nuovamente **StartService** . Può verificare lo stato di blocco corrente del database chiamando la funzione [**QueryServiceLockStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) .

Se il programma di controllo del servizio avvia un servizio, può usare la funzione [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) per specificare una matrice di argomenti da passare alla funzione [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) del servizio. La funzione **StartService** viene restituita dopo la creazione di un nuovo thread per l'esecuzione della funzione **ServiceMain** . Il programma di controllo del servizio può recuperare lo stato del servizio appena avviato in una struttura di [**\_ stato del servizio**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) chiamando la funzione [**QueryServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatus) . Durante l'inizializzazione, il membro **dwCurrentState** deve essere l'avvio del servizio \_ \_ in sospeso. Il membro **dwWaitHint** è un intervallo di tempo, in millisecondi, che indica per quanto tempo il programma di controllo del servizio deve attendere prima di chiamare di nuovo **QueryServiceStatus** . Al termine dell'inizializzazione, il servizio modifica **dwCurrentState** nel servizio \_ in esecuzione.

Gestione controllo servizi non supporta il passaggio di variabili di ambiente personalizzate a un servizio all'avvio. Inoltre, gestione controllo servizi non rileva e passa le modifiche alle variabili di ambiente durante l'esecuzione del servizio. Anziché rendere un servizio dipendente da una variabile di ambiente, utilizzare i valori del registro di sistema o gli argomenti [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) .

Di seguito è riportata una panoramica semplificata di ciò che accade quando un servizio tipico viene avviato da Gestione controllo servizi:

-   SCM legge il percorso del servizio dal registro di sistema e prepara l'avvio del servizio. Ciò include l'acquisizione del blocco del servizio. Qualsiasi tentativo di avviare un altro servizio mentre viene mantenuto il blocco del servizio si bloccherà fino a quando non viene rilasciato il blocco del servizio.
-   Il gestore SCM avvia il processo e attende fino a quando non viene chiuso il processo figlio (indicante un errore) o segnala lo stato di esecuzione del servizio \_ .
-   L'applicazione esegue l'inizializzazione molto semplice e chiama la funzione [**Impossibile eseguire StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) .
-   [**Impossibile eseguire StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) si connette a gestione controllo servizi e avvia un secondo thread che chiama la funzione [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) per il servizio. **ServiceMain** deve segnalare \_ il servizio in esecuzione il prima possibile.
-   Quando Gestione controllo servizi riceve una notifica che indica che il servizio è in esecuzione, rilascia il blocco del servizio.

Se il servizio non aggiorna lo stato entro 80 secondi, più l'ultimo hint di attesa, gestione controllo servizi determina che il servizio non risponde. Gestione controllo servizi registrerà un evento e arresterà il servizio.

Se il programma avvia un servizio driver, [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) viene restituito dopo che il driver di dispositivo ha completato l'inizializzazione.

Per ulteriori informazioni, vedere [avvio di un servizio](starting-a-service.md).

 

 
