---
title: Cenni preliminari sulle tecniche di Rilevamento modifiche
description: Esistono diversi modi in cui i meccanismi di rilevamento delle modifiche possono avere un ambito diverso per tenere traccia delle modifiche che un'applicazione può tenere traccia delle modifiche apportate a un singolo attributo di un singolo oggetto, a tutti gli oggetti in un dominio e così via.
ms.assetid: 7359e851-61b7-420d-beb0-f7f33f79b007
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91fce20dc5e9fe8fe98937bb13885be577185e04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044102"
---
# <a name="overview-of-change-tracking-techniques"></a>Cenni preliminari sulle tecniche di Rilevamento modifiche

Esistono diversi modi in cui i meccanismi di rilevamento delle modifiche possono variare:

-   Ambito per il rilevamento delle modifiche: un'applicazione può tenere traccia delle modifiche apportate a un singolo attributo di un singolo oggetto, a tutti gli oggetti in un dominio e così via. Se il meccanismo soddisfa i requisiti dell'applicazione, l'applicazione riceve un minimo di dati irrilevanti e pertanto migliora le prestazioni.
-   Tempestività: un'applicazione riceve una notifica di ogni modifica quando si verifica oppure può ricevere una notifica dell'effetto netto delle modifiche in un periodo di minuti o ore.

    L'elaborazione di dati meno tempestivi può risultare più efficiente, perché diverse modifiche possono essere compresse in una sola. Se, ad esempio, un attributo viene modificato tre volte in un intervallo di un'ora, un'applicazione a cui viene inviata una notifica per le modifiche accumulate in un'ora verrà notificata solo una modifica dell'attributo, non tre.

    Quando si pensa alle tempistiche, si consideri l'effetto della latenza di replica. Un aggiornamento che ha origine in un controller di dominio non viene replicato immediatamente in un altro controller di dominio. La necessità di una tempestività del rilevamento delle modifiche molto migliore rispetto alla latenza di replica prevista spesso non offre alcun vantaggio reale per l'applicazione.

-   Polling o notifica: con il polling, un'applicazione esegue periodicamente una richiesta a un controller di dominio per ricevere i dati di rilevamento delle modifiche. Con la notifica, il controller di dominio invia le modifiche all'applicazione solo quando si verificano modifiche.

    Il sovraccarico del polling è evidente: l'applicazione può richiedere dati di rilevamento delle modifiche quando non si è verificata alcuna cosa significativa. Il sovraccarico della notifica è più sottile. Il server deve gestire i dati sulle richieste di notifica e deve consultare questi dati per decidere se inviare o meno una notifica. In questo modo è possibile aggiungere sovraccarico alle normali richieste di aggiornamento.

-   Esprimere le informazioni dell'applicazione: persistenza e temporanea: ogni meccanismo di rilevamento delle modifiche deve includere un metodo per il server che tiene traccia dei dati per comprendere lo stato di conoscenza dell'applicazione, in modo che l'idea di "modifica" sia ben definita. Lo stato dell'applicazione, ad esempio, potrebbe essere espresso come "aggiornato con tutte le modifiche che si sono verificate nel controller di dominio d prima dell'ora t". Un meccanismo basato su questo modo per esprimere lo stato di conoscenza di un'applicazione fornirebbe un modo efficiente per consentire all'applicazione di ottenere le modifiche apportate in seguito a un periodo di tempo specificato.

    Se l'espressione delle informazioni dell'applicazione può essere salvata in modo permanente, ovvero archiviata in modo riconoscibile, come in un file o un database, il riavvio dell'applicazione è meno intensivo delle risorse rispetto a se non lo è. Nell'esempio precedente, l'espressione delle informazioni dell'applicazione può essere salvata in modo permanente registrando il controller di dominio d e l'ora t. Alcuni meccanismi di notifica delle modifiche non consentono che questi dati siano salvati in modo permanente. Quando l'applicazione viene avviata, il server e l'applicazione devono essere sincronizzati con un altro meccanismo. Si tratta di un utilizzo intensivo delle risorse se sono coinvolti più oggetti e può implicare una programmazione complessa.

Usare le tecniche seguenti per tenere traccia delle modifiche apportate Active Directory Domain Services:

-   Usare il controllo di notifica delle modifiche per avviare una ricerca asincrona persistente delle modifiche che corrispondono a un filtro specificato. Per ulteriori informazioni, vedere la pagina relativa alle [notifiche delle modifiche in Active Directory Domain Services](change-notifications-in-active-directory-domain-services.md).
-   Utilizzare una ricerca di sincronizzazione della directory (DirSync) per recuperare le modifiche apportate dopo la ricerca DirSync precedente. Per ulteriori informazioni, vedere [polling delle modifiche tramite il controllo DirSync](polling-for-changes-using-the-dirsync-control.md).
-   Usare l'attributo USNChanged per cercare gli oggetti che sono stati modificati dopo la ricerca precedente. Per altre informazioni, vedere [polling delle modifiche con uSNChanged](polling-for-changes-using-usnchanged.md).

Il controllo delle notifiche delle modifiche è progettato per le applicazioni o i servizi che richiedono una notifica ragionevolmente tempestiva delle modifiche non frequenti. Un esempio è un servizio o un programma che archivia i dati di configurazione nel server Active Directory e deve ricevere una notifica tempestiva quando si verifica una modifica. Tenere presente che esistono limitazioni del controllo di notifica.

-   La richiesta di notifiche dipende dalla latenza di replica e dal punto in cui si è verificata la modifica. È possibile ricevere una notifica tempestiva quando una modifica viene replicata nella replica che si sta monitorando, ma la modifica potrebbe essere stata originata molto prima in un'altra replica.
-   Il controllo è limitato al monitoraggio di un singolo oggetto o degli elementi figlio immediati di un contenitore. Le applicazioni che devono monitorare più contenitori o oggetti non correlati possono registrare fino a cinque richieste di notifica.
-   Se un numero eccessivo di client è in attesa di modifiche che si verificano di frequente, le prestazioni del server potrebbero avere un effetto negativo. In generale, le applicazioni devono limitare l'utilizzo di questo controllo per motivi di prestazioni nel server. Se non è necessario conoscere immediatamente le modifiche, è consigliabile eseguire periodicamente il polling delle modifiche anziché utilizzare la notifica delle modifiche.

Le tecniche di ricerca DirSync e USNChanged sono progettate per le applicazioni che mantengono la coerenza tra i dati nel server Active Directory e i dati corrispondenti in un'altra risorsa di archiviazione. Queste tecniche vengono usate dalle applicazioni che eseguono periodicamente il polling delle modifiche. La tecnica DirSync si basa su un controllo server LDAP che è possibile utilizzare tramite le API ADSI o LDAP. Gli svantaggi del controllo DirSync sono che possono essere utilizzati solo da un account con privilegi elevati, ad esempio un amministratore di dominio. Di seguito è riportato un elenco delle limitazioni del controllo DirSync:

-   Il controllo DirSync può essere utilizzato solo da un account con privilegi elevati, ad esempio un amministratore di dominio.
-   Il controllo DirSync può monitorare solo un intero contesto dei nomi. Non è possibile limitare l'ambito di una ricerca DirSync per monitorare solo un sottoalbero, un contenitore o un oggetto specifico in un contesto dei nomi.

La tecnica USNChanged non presenta queste limitazioni, anche se è leggermente più complessa da usare rispetto a DirSync.

 

 




