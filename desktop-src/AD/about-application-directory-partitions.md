---
title: Informazioni sulle partizioni di directory applicative
description: Gli sviluppatori che usano ADSI o LDAP per archiviare e accedere a dati relativamente statici e globali in Active Directory Domain Services possono anche preferire, per semplicità e uniformità, continuare a usare l'accesso ADSI o LDAP per i requisiti di dati dinamici. I dati dinamici cambiano più frequentemente rispetto a quanto consigliato per l'archiviazione in Active Directory Domain Services. I dati dinamici cambiano in genere più frequentemente rispetto alla latenza di replica coinvolta nella propagazione della modifica a tutte le repliche dei dati.
ms.assetid: bf856c3a-9061-474a-a536-c87ca50d5f83
ms.tgt_platform: multiple
keywords:
- Informazioni sulle partizioni di directory applicative
- partizioni di directory applicative, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9063a05bdb6f04681f012f1e6317b3343833c79c8f6a5af39a1a7865eccbab63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117841031"
---
# <a name="about-application-directory-partitions"></a>Informazioni sulle partizioni di directory applicative

Gli sviluppatori che usano ADSI o LDAP per archiviare e accedere a dati relativamente statici e globali in Active Directory Domain Services possono anche preferire, per semplicità e uniformità, continuare a usare l'accesso ADSI o LDAP per i requisiti di dati dinamici. I dati dinamici cambiano più frequentemente rispetto a quanto consigliato per l'archiviazione in Active Directory Domain Services. I dati dinamici cambiano in genere più frequentemente rispetto alla latenza di replica coinvolta nella propagazione della modifica a tutte le repliche dei dati.

In Windows 2000 il supporto per i dati dinamici è limitato. L'archiviazione dei dati dinamici in una partizione di dominio può essere complessa. I dati vengono replicati in tutti i controller di dominio nel dominio, che spesso non sono necessari e possono causare dati incoerenti a causa della latenza di replica. Ciò può influire negativamente sulle prestazioni di rete. Inoltre, le partizioni di dominio non sono efficaci per le applicazioni che devono replicare i dati oltre i limiti del dominio. Un'altra opzione Windows 2000 è archiviare i dati dinamici in attributi contrassegnati come non replicati. Tuttavia, questa disposizione è limitata in quanto ha un singolo punto di errore, ci esempio, il singolo controller di dominio che ospita l'unica copia degli attributi non replicati dell'oggetto.

Le partizioni di directory applicative consentono di controllare l'ambito della replica e di consentire il posizionamento delle repliche in modo più appropriato per i dati dinamici. Di conseguenza, la partizione di directory applicativa offre la possibilità di ospitare dati dinamici nel server Active Directory, consentendo così l'accesso ADSI/LDAP ad esso, senza influire in modo significativo sulle prestazioni di rete.

Il Windows DNS 2000 è un esempio di servizio che può sfruttare le partizioni di directory applicative. In Windows 2000, se il servizio DNS è configurato facoltativamente per l'uso di Active Directory Domain Services, i dati della zona DNS vengono archiviati nel server Active Directory in una partizione di dominio. In altri parole, i dati vengono replicati in tutti i controller di dominio nel dominio, indipendentemente dal fatto che un server DNS sia configurato per l'esecuzione nel controller di dominio. Si tratta di un'istanza in cui la replica completa a livello di dominio non è necessaria. Archiviando i dati della zona DNS in una partizione di directory applicativa, il servizio può ridefinire l'ambito della replica solo per il subset di controller di dominio nel dominio che esegue effettivamente il server DNS.

Si considerino gli scenari seguenti per l'hosting di una replica di una partizione di directory applicativa:

-   È possibile creare una replica di una partizione di directory applicativa in qualsiasi sistema operativo Windows Server 2003 e in un controller di dominio successivo in una Active Directory Domain Services foresta.
-   È possibile specificare il set di controller di dominio che ospitano repliche di una partizione di directory applicativa. A differenza di una partizione di dominio, non è necessaria una partizione di directory applicativa per la replica in tutti i controller di dominio in un dominio e può essere replicata nei controller di dominio in domini diversi della foresta.
-   Un controller di dominio con una replica di partizione di directory applicativa può coesistere e funzionare in un ambiente in modalità mista con altri computer che eseguono Windows 2000 o Windows NT 4.0.

I tipi di dati che possono essere archiviati in una partizione di directory applicativa includono:

-   Una partizione di directory applicativa può contenere istanze di qualsiasi tipo di oggetto, ad eccezione delle entità di sicurezza, ad esempio utenti, computer o gruppi.
-   Gli oggetti in una partizione di directory applicativa possono mantenere riferimenti DN-value ad altri oggetti nella stessa partizione di directory applicativa, agli oggetti nelle partizioni di configurazione e schema e a qualsiasi head del contesto di denominazione (che è l'oggetto principale di una partizione di directory, ad esempio l'oggetto **domainDNS** nella parte superiore di una partizione di directory applicativa).
-   Per altre informazioni e un esempio del tipo di dati dinamici che possono essere archiviati in una partizione di directory [applicativa,](dynamic-objects.md)vedere Oggetti dinamici . Gli oggetti dinamici sono supportati a partire Windows Server 2003. Gli oggetti dinamici dispongono di una proprietà che determina la data e l'ora di inizio, dopo la quale l'oggetto viene eliminato dal server Active Directory.

Alcune limitazioni delle partizioni di directory applicative includono:

-   Gli oggetti in una partizione di directory applicativa non possono mantenere riferimenti di valore *DN* a oggetti in altre partizioni di directory applicative o partizioni di dominio. I riferimenti ai valori DN sono riferimenti persistenti a un valore di nome distinto, ad esempio "CN=someuser,DC=corp,DC=Fabrikam,DC=com". Analogamente, gli oggetti nelle partizioni di dominio, configurazione e schema non possono mantenere riferimenti di valore DN agli oggetti in una partizione di directory applicativa. Un riferimento DN-value può essere mantenuto nell'head del contesto dei nomi. () )
-   Gli oggetti in una partizione di directory applicativa non vengono replicati nel catalogo globale. Come per qualsiasi controller di dominio, anche un server di catalogo globale può essere configurato per contenere una replica completa di una partizione di directory applicativa, ma i dati della partizione di directory applicativa sono completamente separati dai dati del catalogo globale.
-   Quando viene creata una replica di partizione di directory applicativa, il ruolo FSMO Domain-Naming deve essere in uno dei controller di dominio del sistema operativo Windows Server 2003 e versioni successive. Dopo aver creato la replica della partizione di directory applicativa, il ruolo FSMO di denominazione del dominio può essere assegnato nuovamente a un controller di dominio Windows 2000.
-   Gli oggetti partizione di directory applicativa non possono essere spostati in altre partizioni di Active Directory all'esterno della partizione in cui sono stati creati.

Altre funzionalità della partizione di directory applicativa includono:

-   Il modello di sicurezza e controllo di accesso per la partizione di directory applicativa è lo stesso di quello per altre partizioni in Active Directory Domain Services.
-   Gli intervalli di tempo che controllano la latenza di avvio di una notifica di modifica di origine ai partner di replica all'interno di un sito possono essere configurati separatamente per ogni partizione di directory applicativa.
-   Le partizioni di directory applicative possono essere denominate come domini normali, collegate in qualsiasi punto dello spazio dei nomi di Active Directory in cui può essere presente un dominio e individuate usando DNS anche da sistemi Windows 2000.
-   È possibile creare una partizione di directory applicativa, definire l'ambito di replica e le relative impostazioni configurabili a livello di codice usando le API LDAP e ADSI standard. Per altre informazioni sulla modifica delle partizioni di directory applicative a livello di codice, vedere [Partizioni di directory applicative](application-directory-partitions.md).

 

 




