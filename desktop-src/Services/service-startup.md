---
description: Per avviare un servizio o un servizio driver, il programma di controllo del servizio usa la funzione StartService.
ms.assetid: 7d2ee779-1554-436a-a65c-f0322745f46a
title: Avvio del servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17901987581b6a2680e0a70cfe2e0ed80472d293cbe32932f768e9133b6a058d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888700"
---
# <a name="service-startup"></a>Avvio del servizio

Per avviare un servizio o un servizio driver, il programma di controllo del servizio usa la [**funzione StartService.**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) La **funzione StartService** ha esito negativo se il database è bloccato. In questo caso, il programma di controllo del servizio deve attendere alcuni secondi e chiamare **di nuovo StartService.** Può controllare lo stato di blocco corrente del database chiamando la [**funzione QueryServiceLockStatus.**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa)

Se il programma di controllo del servizio avvia un servizio, può usare la funzione [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) per specificare una matrice di argomenti da passare alla funzione [**ServiceMain del**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) servizio. La **funzione StartService** restituisce dopo la creazione di un nuovo thread per eseguire la **funzione ServiceMain.** Il programma di controllo del servizio può recuperare lo stato del servizio appena avviato in una struttura [**SERVICE \_ STATUS**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) chiamando la [**funzione QueryServiceStatus.**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatus) Durante l'inizializzazione, il membro **dwCurrentState** deve essere SERVICE \_ START \_ PENDING. Il **membro dwWaitHint** è un intervallo di tempo, in millisecondi, che indica per quanto tempo il programma di controllo del servizio deve attendere prima di chiamare **nuovamente QueryServiceStatus.** Al termine dell'inizializzazione, il servizio cambia **dwCurrentState in** SERVICE \_ RUNNING.

Gestione controllo servizi non supporta il passaggio di variabili di ambiente personalizzate a un servizio all'avvio. Inoltre, Gestione controllo servizi non rileva e passa le modifiche alle variabili di ambiente durante l'esecuzione del servizio. Anziché rendere un servizio dipendente da una variabile di ambiente, usare i valori del Registro di sistema o [**gli argomenti ServiceMain.**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona)

Di seguito è riportata una panoramica semplificata di ciò che accade quando un servizio tipico viene avviato da Gestione controllo servizi:

-   Gestione controllo servizi legge il percorso del servizio dal Registro di sistema e si prepara ad avviare il servizio. Ciò include l'acquisizione del blocco del servizio. Qualsiasi tentativo di avviare un altro servizio mentre viene mantenuto il blocco del servizio si blocchi fino al rilascio del blocco del servizio.
-   Gestione controllo servizi avvia il processo e attende fino alla chiusura del processo figlio (che indica un errore) o fino a quando non viene indicato lo stato SERVICE \_ RUNNING.
-   L'applicazione esegue l'inizializzazione molto semplice e chiama la [**funzione StartServiceCtrlDispatcher.**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera)
-   [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) si connette a Gestione controllo servizi e avvia un secondo thread che chiama la [**funzione ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) per il servizio. **ServiceMain deve** segnalare SERVICE \_ RUNNING appena possibile.
-   Quando il gestore di controllo del servizio viene informato che il servizio è in esecuzione, rilascia il blocco del servizio.

Se il servizio non aggiorna lo stato entro 80 secondi, oltre all'ultimo hint di attesa, il gestore di controllo del servizio determina che il servizio ha smesso di rispondere. Gestione controllo servizi registra un evento e arresta il servizio.

Se il programma avvia un servizio driver, [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) restituisce dopo che il driver di dispositivo ha completato l'inizializzazione.

Per altre informazioni, vedere [Avvio di un servizio](starting-a-service.md).

 

 
