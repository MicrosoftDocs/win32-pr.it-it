---
title: Panoramica delle Rilevamento modifiche tecniche
description: Esistono diversi modi in cui i meccanismi di rilevamento delle modifiche possono differire ambito per il rilevamento delle modifiche Un'applicazione può tenere traccia delle modifiche apportate a un singolo attributo di un singolo oggetto, a tutti gli oggetti in un dominio e così via.
ms.assetid: 7359e851-61b7-420d-beb0-f7f33f79b007
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 036a16362a7f27da47fc086d8758b28619f34d1475c7bb911050deb20c86f08d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025509"
---
# <a name="overview-of-change-tracking-techniques"></a>Panoramica delle Rilevamento modifiche tecniche

Esistono diversi modi in cui i meccanismi di rilevamento delle modifiche possono differire:

-   Ambito per il rilevamento delle modifiche: un'applicazione può tenere traccia delle modifiche apportate a un singolo attributo di un singolo oggetto, a tutti gli oggetti in un dominio e così via. Se il meccanismo soddisfa i requisiti dell'applicazione, l'applicazione riceve un minimo di dati irrilevanti e quindi migliora le prestazioni.
-   Tempestività: un'applicazione viene notificata di ogni modifica nel momento in cui si verifica o può ricevere una notifica dell'effetto netto delle modifiche in un periodo di minuti o ore.

    L'elaborazione di dati meno temporati può essere più efficiente, perché diverse modifiche possono essere compresse in una sola. Ad esempio, se un attributo viene modificato tre volte in un intervallo di un'ora, un'applicazione che ha notificato le modifiche accumulate in un'ora riceverà una notifica di una sola modifica dell'attributo, non tre.

    Quando si pensa alla tempestività, considerare l'effetto della latenza di replica. Un aggiornamento che ha origine in un controller di dominio non viene replicato immediatamente in un altro controller di dominio. La necessità di una tempestività del rilevamento delle modifiche molto migliore rispetto alla latenza di replica prevista spesso non offre vantaggi reali per l'applicazione.

-   Polling o notifica: con il polling, un'applicazione invia periodicamente una richiesta a un controller di dominio per ricevere i dati di rilevamento delle modifiche. Con la notifica, il controller di dominio invia le modifiche all'applicazione solo quando si verificano modifiche.

    L'overhead del polling è ovvio: l'applicazione può richiedere i dati di rilevamento delle modifiche quando non si è verificato nulla di significativo. L'overhead della notifica è più sottile. Il server deve mantenere i dati sulle richieste di notifica e deve consultare questi dati per decidere se inviare o meno una notifica. Ciò può aggiungere sovraccarico alle normali richieste di aggiornamento.

-   Esprimere le conoscenze dell'applicazione: persistente e temporaneo: ogni meccanismo di rilevamento delle modifiche deve includere un metodo per il server che contiene i dati monitorati per comprendere lo stato di conoscenza dell'applicazione, in modo che l'idea di "modifica" sia ben definita. Ad esempio, lo stato di conoscenza dell'applicazione può essere espresso come "Aggiornato con tutte le modifiche che si sono verificate nel controller di dominio d prima dell'ora t". Un meccanismo basato su questo modo di esprimere lo stato di conoscenza di un'applicazione offrirebbe all'applicazione un modo efficiente per ottenere le modifiche che si sono verificate successivamente a un tempo specificato.

    Se l'espressione delle informazioni dell'applicazione può essere mantenuta, cio' archiviata in modo recuperabile, come in un file o in un database, il riavvio dell'applicazione richiede meno risorse rispetto a se non è possibile. Nell'esempio precedente, l'espressione delle informazioni dell'applicazione può essere mantenuta registrando il controller di dominio d e l'ora t. Alcuni meccanismi di notifica delle modifiche non consentono la persistenza di questi dati. Il server e l'applicazione devono essere sincronizzati con un altro meccanismo all'avvio dell'applicazione. Si tratta di un utilizzo intensivo delle risorse se sono coinvolti più oggetti e possono comportare una programmazione complessa.

Usare le tecniche seguenti per tenere traccia delle modifiche Active Directory Domain Services:

-   Usare il controllo di notifica delle modifiche per avviare una ricerca asincrona permanente delle modifiche che corrispondono a un filtro specificato. Per altre informazioni, vedere [Notifiche di modifica in Active Directory Domain Services](change-notifications-in-active-directory-domain-services.md).
-   Usare una ricerca di sincronizzazione directory (DirSync) per recuperare le modifiche che si sono verificate dopo la ricerca DirSync precedente. Per altre informazioni, vedere [Polling delle modifiche tramite il controllo DirSync](polling-for-changes-using-the-dirsync-control.md).
-   Usare l'attributo USNChanged per cercare gli oggetti modificati dopo la ricerca precedente. Per altre informazioni, vedere [Polling delle modifiche tramite USNChanged.](polling-for-changes-using-usnchanged.md)

Il controllo delle notifiche di modifica è progettato per applicazioni o servizi che richiedono una notifica ragionevolmente tempestiva di modifiche poco frequenti. Un esempio è un servizio o un programma che archivia i dati di configurazione nel server Active Directory e deve ricevere una notifica tempestiva quando si verifica una modifica. Tenere presente che esistono limitazioni del controllo di notifica.

-   La tempestività delle notifiche dipende dalla latenza di replica e dalla posizione in cui si è verificata la modifica. È possibile ricevere una notifica tempestiva quando una modifica viene replicata nella replica che si sta monitorando, ma la modifica potrebbe essere stata originata molto prima in un'altra replica.
-   Il controllo è limitato al monitoraggio di un singolo oggetto o degli elementi figlio immediati di un contenitore. Le applicazioni che devono monitorare più contenitori o oggetti non correlati possono registrare fino a cinque richieste di notifica.
-   Se troppi client sono in ascolto delle modifiche che si verificano di frequente, influiscono sulle prestazioni del server. In generale, le applicazioni devono limitare l'uso di questo controllo per motivi di prestazioni nel server. Se non è necessario conoscere immediatamente le modifiche, potrebbe essere meglio eseguire periodicamente il polling delle modifiche anziché usare la notifica delle modifiche.

Le tecniche di ricerca DirSync e USNChanged sono progettate per le applicazioni che mantengono la coerenza tra i dati nel server Active Directory e i dati corrispondenti in un'altra archiviazione. Queste tecniche vengono usate dalle applicazioni che esere periodicamente il polling delle modifiche. La tecnica DirSync si basa su un controllo server LDAP che è possibile usare tramite LE API ADSI o LDAP. Gli svantaggi del controllo DirSync sono che può essere usato solo da un account con privilegi elevati, ad esempio un amministratore di dominio. Di seguito è riportato un elenco di limitazioni del controllo DirSync:

-   Il controllo DirSync può essere usato solo da un account con privilegi elevati, ad esempio un amministratore di dominio.
-   Il controllo DirSync può monitorare solo un intero contesto dei nomi. Non è possibile limitare l'ambito di una ricerca DirSync per monitorare solo un sottoalbero, un contenitore o un oggetto specifico in un contesto dei nomi.

La tecnica USNChanged non presenta queste limitazioni, anche se è un po' più complicato da usare rispetto a DirSync.

 

 




