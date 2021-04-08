---
title: Dove creare un punto di connessione del servizio
description: Quando viene installata un'istanza di Active Directory Domain Services, il programma di installazione del servizio crea gli oggetti del punto di connessione del servizio (SCP) nel Active Directory Domain Services.
ms.assetid: a90566d9-dd68-43e2-be9e-300d57a7fbf4
ms.tgt_platform: multiple
keywords:
- dove creare un punto di connessione del servizio AD
- Active Directory, dove creare un punto di connessione del servizio
- dove creare un punto di connessione del servizio AD
- creazione di un punto di connessione del servizio AD
- AD del punto di connessione del servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf122ebabcfd8085ebad46314ffd1c09f827e783
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044085"
---
# <a name="where-to-create-a-service-connection-point"></a>Dove creare un punto di connessione del servizio

Quando viene installata un'istanza di Active Directory Domain Services, il programma di installazione del servizio crea gli oggetti del punto di connessione del servizio (SCP) nel Active Directory Domain Services. L'obiettivo principale consiste nel ridurre al minimo il traffico di replica e abilitare l'amministrazione e la manutenzione efficienti degli oggetti.

Tenere presente che le applicazioni client trovano convergenza eseguendo una ricerca nella directory delle parole chiave in SCP. L'attributo **Keywords** di SCP è incluso nel catalogo globale; i client possono eseguire ricerche nel catalogo globale per trovare convergenza nella foresta. Per questo motivo, il client non influisce sulla posizione di pubblicazione di convergenza.

## <a name="minimize-replication-traffic"></a>Ridurre al minimo il traffico di replica

Per ridurre al minimo il traffico di replica, creare convergenza nella partizione del dominio del computer host del servizio. Ad esempio, è possibile creare convergenza come oggetti figlio dell'oggetto computer in cui è installato il servizio. Una partizione di dominio di Active Directory Domain Services, talvolta denominata contesto dei nomi di dominio, contiene oggetti specifici del dominio, ad esempio gli oggetti per gli utenti e i computer del dominio. Una replica completa di tutti gli oggetti nella partizione di dominio viene replicata in ogni controller di dominio del dominio, ma non viene replicata nei controller di dominio di altri domini.

Non creare convergenza nella partizione di configurazione, nota anche come contesto dei nomi di configurazione, perché le modifiche apportate alla partizione di configurazione vengono replicate in ogni controller di dominio della foresta. Come indicato in precedenza, i client in tutta la foresta possono eseguire query nel catalogo globale per trovare convergenza in qualsiasi punto della foresta, quindi la creazione di convergenza nella partizione di configurazione non li rende più visibili ai client. genera solo più traffico di replica.

## <a name="ease-of-administration"></a>Facilità di amministrazione

Prendere in considerazione le linee guida seguenti per l'amministrazione degli oggetti:

-   Inserire oggetti specifici del servizio, in cui gli amministratori possono controllare l'accesso a tali oggetti usando i criteri e le autorizzazioni di accesso ereditate.
-   Inserire gli oggetti in dove un amministratore può trovarli facilmente.

Un percorso predefinito valido che soddisfi entrambi gli obiettivi consiste nel creare SCP e altri oggetti specifici del servizio nell'oggetto computer del computer host di ogni istanza del servizio. Per ulteriori informazioni, vedere [pubblicazione in un oggetto computer](publishing-under-a-computer-object.md).

Una valida alternativa per i servizi non collegati a un singolo host consiste nel creare un contenitore per gli oggetti servizio nel contenitore di sistema in una partizione di dominio. Per ulteriori informazioni, vedere [pubblicazione in un contenitore di sistema del dominio](publishing-in-a-domain-system-container.md).

Il diagramma seguente mostra parte della gerarchia di contenitori predefinita per una partizione di dominio.

![gerarchia del contenitore della partizione di dominio predefinita](images/domain-container-heirarchy.png)

Il diagramma mostra la gerarchia di dominio predefinita inclusa con Active Directory Domain Services. Tuttavia, molte aziende creano una gerarchia di contenitori di unità organizzativa (OU) per raggruppare le classi di oggetti, ad esempio utenti e computer, insieme ai fini dell'amministrazione. Gli amministratori possono quindi applicare i criteri e le voci di controllo di accesso ereditabili (ACE) a un'unità organizzativa per delegare l'autorità amministrativa per gli oggetti nell'unità organizzativa. Ciò consente agli amministratori di gestire in modo efficiente un'azienda, ma presenta alcune conseguenze per i programmatori di servizi:

-   L'oggetto computer per un host del servizio potrebbe non trovarsi nel contenitore computer, come illustrato nel diagramma. Per ulteriori informazioni su come trovare l'oggetto computer per il computer locale, vedere [pubblicazione in un oggetto computer](publishing-under-a-computer-object.md).
-   Gli amministratori possono spostare gli oggetti in base alle esigenze dell'organizzazione. Ciò significa che non è possibile dipendere dagli oggetti rimanenti in un percorso fisso; ovvero, il servizio non può dipendere da un nome distinto dell'oggetto che rimane lo stesso. Usare invece l'attributo **objectGUID** di un oggetto, che non cambia se l'oggetto viene spostato o rinominato. Per ulteriori informazioni e un esempio di codice in cui viene creato un punto di connessione del servizio, archivia il relativo **objectGUID** e in seguito recupera il **objectGUID** per l'associazione al SCP, vedere [creazione e gestione di un punto di connessione del servizio](creating-and-maintaining-a-service-connection-point.md).
-   Tutte le classi di oggetti standard correlate ai servizi, nonché le sottoclassi di queste classi, sono elementi figlio validi delle classi **computer** e **OrganizationalUnit** . Se si estende lo schema per definire una classe specifica del servizio, assicurarsi che le classi **computer** e **OrganizationalUnit** siano incluse nei possibili superiori.
-   Il programma di installazione del servizio determina il percorso predefinito per la creazione di convergenza. Potrebbe essere necessario consentire all'amministratore di installare il servizio per specificare un percorso di installazione alternativo.

Gli oggetti specifici del servizio non devono essere creati nelle aree seguenti:

-   I servizi non devono pubblicare oggetti direttamente nei contenitori utenti o computer di una partizione di dominio, né devono creare nuovi contenitori in questi contenitori. Tuttavia, i servizi possono pubblicare oggetti come oggetti figlio di un oggetto computer, indipendentemente dal fatto che l'oggetto computer sia archiviato nel contenitore computer.
-   I servizi che usano le API di registrazione e risoluzione di Windows Sockets (RnR) o RpcNs (RPC Name Service) per annunciarsi, creare gli oggetti appropriati nei contenitori WinsockServices e RpcServices nel contenitore di sistema di una partizione di dominio. Non creare in modo esplicito oggetti in questi contenitori. In questo modo non viene causato alcun danno diretto, ma è possibile che si verifichino confusione per gli amministratori.

 

 




