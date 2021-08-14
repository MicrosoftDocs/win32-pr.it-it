---
title: Dove creare un punto di connessione del servizio
description: Quando viene installata un'istanza di Active Directory Domain Services, il programma di installazione del servizio crea oggetti punto di connessione del servizio (SCP) in Active Directory Domain Services.
ms.assetid: a90566d9-dd68-43e2-be9e-300d57a7fbf4
ms.tgt_platform: multiple
keywords:
- dove creare un punto di connessione del servizio AD
- Active Directory, dove creare un punto di connessione del servizio
- dove creare un punto di connessione del servizio AD
- creazione di un punto di connessione del servizio AD
- punto di connessione del servizio AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b585c11333b8e307a7f6771bd89ccf5ad82038fb22f10fca7eb114c1101a063a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118182085"
---
# <a name="where-to-create-a-service-connection-point"></a>Dove creare un punto di connessione del servizio

Quando viene installata un'istanza di Active Directory Domain Services, il programma di installazione del servizio crea oggetti punto di connessione del servizio (SCP) in Active Directory Domain Services. L'obiettivo principale deve essere ridurre al minimo il traffico di replica e consentire un'amministrazione e una manutenzione efficienti degli oggetti.

Tenere presente che le applicazioni client trovano i criteri di sicurezza cercando le parole chiave nella directory in SCP. **L'attributo keywords** di un SCP è incluso nel catalogo globale. I client possono eseguire ricerche nel catalogo globale per trovare i criteri di sicurezza nella foresta. Per questo motivo, il client non influenza la posizione in cui pubblicare gli scp.

## <a name="minimize-replication-traffic"></a>Ridurre al minimo il traffico di replica

Per ridurre al minimo il traffico di replica, creare scp nella partizione di dominio del dominio del computer host del servizio. Ad esempio, è possibile creare provider di servizi di configurazione come oggetti figlio dell'oggetto computer in cui è installato il servizio. Una partizione di dominio di Active Directory Domain Services, talvolta denominata contesto dei nomi di dominio, contiene oggetti specifici del dominio, ad esempio gli oggetti per gli utenti e i computer del dominio. Una replica completa di tutti gli oggetti nella partizione di dominio viene replicata in ogni controller di dominio per il dominio, ma non viene replicata nei controller di dominio di altri domini.

Non creare scp nella partizione di configurazione, nota anche come contesto dei nomi di configurazione, perché le modifiche alla partizione di configurazione vengono replicate in ogni controller di dominio nella foresta. Come indicato in precedenza, i client in tutta la foresta possono eseguire query nel catalogo globale per trovare gli scp in qualsiasi punto della foresta, quindi la creazione di scp nella partizione di configurazione non li rende più visibili ai client. genera solo più traffico di replica.

## <a name="ease-of-administration"></a>Facilità di amministrazione

Si considerino le linee guida seguenti per l'amministrazione degli oggetti:

-   Posizionare gli oggetti specifici del servizio in cui gli amministratori possono controllare l'accesso usando criteri e autorizzazioni di accesso ereditate.
-   Posizionare gli oggetti in dove un amministratore può trovarli facilmente.

Un buon percorso predefinito che soddisfa entrambi gli obiettivi è creare SCP e altri oggetti specifici del servizio nell'oggetto computer del computer host di ogni istanza del servizio. Per altre informazioni, vedere [Pubblicazione in un oggetto computer](publishing-under-a-computer-object.md).

Un'alternativa valida per i servizi non associati a un singolo host consiste nel creare un contenitore per gli oggetti servizio nel contenitore System in una partizione di dominio. Per altre informazioni, vedere [Pubblicazione in un contenitore del sistema di dominio](publishing-in-a-domain-system-container.md).

Il diagramma seguente illustra parte della gerarchia di contenitori predefinita per una partizione di dominio.

![gerarchia del contenitore della partizione di dominio predefinita](images/domain-container-heirarchy.png)

Il diagramma mostra la gerarchia di dominio predefinita inclusa in Active Directory Domain Services. Tuttavia, molte aziende creano una gerarchia di contenitori di unità organizzative (OU) per raggruppare classi di oggetti, ad esempio utenti e computer, insieme ai fini dell'amministrazione. Gli amministratori possono quindi applicare i criteri e le voci di controllo di accesso (ACE) ereditabili a un'unità organizzativa per delegare l'autorità amministrativa per gli oggetti nell'unità organizzativa. Ciò consente agli amministratori di gestire in modo efficiente un'organizzazione, ma presenta alcune conseguenze per i programmatori di servizi:

-   L'oggetto computer per un host del servizio potrebbe non essere nel contenitore Computer, come illustrato nel diagramma. Per altre informazioni su come trovare l'oggetto computer per il computer locale, vedere [Pubblicazione in un oggetto computer](publishing-under-a-computer-object.md).
-   Gli amministratori possono spostare gli oggetti in base alle esigenze dell'organizzazione. Ciò significa che non è possibile dipendere dagli oggetti che restano in una posizione fissa. in altre informazioni, il servizio non può dipendere da un nome distinto dell'oggetto che rimane lo stesso. Usare invece l'attributo **objectGUID** di un oggetto, che non cambia se l'oggetto viene spostato o rinominato. Per altre informazioni e un esempio di codice che crea un SCP, archivia il relativo **objectGUID** e successivamente recupera **objectGUID** da associare a SCP, vedere Creazione e gestione di un punto di connessione [del servizio](creating-and-maintaining-a-service-connection-point.md).
-   Tutte le classi di oggetti standard correlate al servizio, nonché tutte le sottoclassi di queste classi, sono elementi figlio validi delle classi **computer** e **organizationalUnit.** Se si estende lo schema per definire una classe specifica del servizio, assicurarsi che le classi **computer** e **organizationalUnit** siano incluse nei possibili superiori.
-   Il programma di installazione del servizio determina il percorso predefinito per la creazione di provider di servizi. È possibile consentire all'amministratore che installa il servizio di specificare un percorso di installazione alternativo.

Gli oggetti specifici del servizio non devono essere creati nelle aree seguenti:

-   I servizi non devono pubblicare oggetti direttamente nei contenitori Utenti o Computer di una partizione di dominio né devono creare nuovi contenitori in questi contenitori. Tuttavia, i servizi possono pubblicare oggetti come oggetti figlio di un oggetto computer, indipendentemente dal fatto che l'oggetto computer sia archiviato o meno nel contenitore Computer.
-   I servizi, che usano la registrazione e la risoluzione di Windows Sockets (RnR) o le API rpc name service (RpcNs) per annunciarsi, creano gli oggetti adeguati nei contenitori WinsockServices e RpcServices nel contenitore System di una partizione di dominio. Non creare oggetti in modo esplicito in questi contenitori. Questa operazione non causa danni diretti, ma può generare confusione per gli amministratori.

 

 




