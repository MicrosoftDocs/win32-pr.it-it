---
description: Risoluzione dei problemi relativi a COM+ CRM
ms.assetid: 4d2d9372-b540-4e08-9b57-8687802610b6
title: Risoluzione dei problemi relativi a COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b04e37d183dbf3df8d017e780917f955e14a033
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523865"
---
# <a name="troubleshooting-the-com-crm"></a>Risoluzione dei problemi relativi a COM+ CRM

Di seguito sono riportati i problemi più comuni riscontrati durante lo sviluppo e l'utilizzo di COM+ CRM:

-   **Messaggi del registro eventi.** Se l'applicazione del server CRM rileva un errore interno grave, FailFast (termina il processo dell'applicazione server CRM) e scrive un messaggio nel registro eventi di Windows. Se vengono rilevati problemi, fare riferimento al registro eventi.

-   **Eccezioni dal compensatore CRM.** L'infrastruttura CRM crea il compensatore CRM e lo passa alle notifiche relative ai risultati delle transazioni e ai record di log scritti dal ruolo di lavoro CRM. Se il compensatore CRM restituisce un errore o genera un'eccezione, viene rilevata dall'infrastruttura CRM e genera un FailFast. Un messaggio nel registro eventi indica che è stata ricevuta un'eccezione dal compensatore CRM. È possibile forzare l'ignoranza di queste eccezioni. (Vedere [le impostazioni del registro di sistema com+ CRM](com--crm-registry-settings.md)). Le eccezioni del compensatore CRM più probabile indicano un problema nel componente di compensazione CRM specifico e non nell'infrastruttura di CRM.

-   **Traccia di ripristino.** La traccia di ripristino può essere molto utile per determinare i problemi durante il ripristino. Per informazioni sull'abilitazione della traccia di ripristino, vedere [impostazioni del registro di sistema com+ CRM](com--crm-registry-settings.md).

-   **Il tentativo di eseguire con CRM non è abilitato.** Non è sufficiente inserire i componenti di lavoro CRM e Compensator CRM nell'applicazione server COM+. Il supporto per dispongono deve essere abilitato in modo specifico per l'applicazione server COM+ specifica utilizzando l'opzione **Abilita gestioni risorse di compensazione** nella scheda **Avanzate** delle pagine delle proprietà dell'applicazione com+. Per ulteriori informazioni, vedere [Configuring com+ CRM Components](configuring-com--crm-components.md) . Se viene effettuato un tentativo di usare un CRM in un'applicazione server in cui non è abilitato il CRM, viene restituito un codice di errore al ruolo di lavoro CRM.

-   **Tentativo di eseguire dispongono nei processi client.** Dispongono non vengono eseguiti nei processi client; devono essere eseguiti in un processo dell'applicazione server COM+. I componenti CRM possono essere inseriti in un pacchetto di libreria per l'uso da più applicazioni server COM+, ma non sono disponibili per l'uso nei processi client. Il tentativo di usare le interfacce CRM all'interno di un processo client restituisce un codice di errore al ruolo di lavoro CRM.

-   **Ripristino in corso.** Il ripristino viene avviato all'avvio di un'applicazione server CRM. Tuttavia, il ripristino viene eseguito in background durante la normale elaborazione dell'applicazione server CRM. Il ruolo di lavoro CRM può essere creato prima del completamento del ripristino. Non è possibile usare dispongono in un processo dell'applicazione server CRM finché il ripristino non è stato completato correttamente. In questo caso, il ruolo di lavoro CRM riceve un codice di errore "ripristino in corso" durante il tentativo di registrare il compensatore CRM. Il ruolo di lavoro CRM deve eseguire il polling o ritardare l'operazione fino al completamento del ripristino. Il tempo di recupero è specifico di un determinato tipo di CRM e deve essere preso in considerazione quando si progetta il CRM. I recuperi a lunga durata non sono desiderati.

-   **Sicurezza sul file di log CRM.** Se l'accesso al file di log CRM viene negato, vedere [considerazioni sulla sicurezza di com+ CRM](com--crm-security-considerations.md) per una descrizione della modalità di impostazione della sicurezza nel file di log CRM.

-   **Transazioni in dubbio.** In rari casi, una transazione DTC potrebbe entrare nello stato in dubbio. ovvero, il DTC non è in grado di determinare il risultato della transazione. In questi casi, durante il ripristino, il CRM mantiene i record del log per la transazione nel file di log CRM. Quando la transazione in dubbio è stata risolta da DTC, l'esecuzione di un altro ripristino CRM completa la transazione.

-   **Creazione e rilascio del compensatore CRM.** La prima volta che un compensatore CRM viene registrato da un ruolo di lavoro CRM, viene creato dall'infrastruttura CRM e viene eseguita una query per determinare quale delle interfacce del compensatore CRM supporta. Viene quindi rilasciata immediatamente. I compensatori CRM devono supportare la possibilità di essere creati e rilasciati senza alcuna chiamata al metodo corrispondente. Se non è possibile creare correttamente il compensatore CRM, probabilmente a causa di una registrazione COM non corretta o se non supporta almeno una delle interfacce di compensazione CRM corrette, al ruolo di lavoro CRM viene restituito un codice di errore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti Gestione risorse di compensazione COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



