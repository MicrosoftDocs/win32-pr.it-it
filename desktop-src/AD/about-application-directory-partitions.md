---
title: Informazioni sulle partizioni di directory applicative
description: Gli sviluppatori che usano ADSI o LDAP per archiviare e accedere a dati relativamente statici e globali in Active Directory Domain Services possono anche preferire, per semplicità e uniformità, di continuare a usare l'accesso ADSI o LDAP per i requisiti di dati dinamici. Le modifiche ai dati dinamici sono più frequenti rispetto a quelle consigliate per l'archiviazione in Active Directory Domain Services. I dati dinamici vengono in genere modificati più di frequente rispetto alla latenza di replica dovuta alla propagazione della modifica a tutte le repliche dei dati.
ms.assetid: bf856c3a-9061-474a-a536-c87ca50d5f83
ms.tgt_platform: multiple
keywords:
- Informazioni sulle partizioni di directory applicative
- Partizioni di directory applicative, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fc1970f27d18d760ab3a45fae389809a40a2a89
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044020"
---
# <a name="about-application-directory-partitions"></a>Informazioni sulle partizioni di directory applicative

Gli sviluppatori che usano ADSI o LDAP per archiviare e accedere a dati relativamente statici e globali in Active Directory Domain Services possono anche preferire, per semplicità e uniformità, di continuare a usare l'accesso ADSI o LDAP per i requisiti di dati dinamici. Le modifiche ai dati dinamici sono più frequenti rispetto a quelle consigliate per l'archiviazione in Active Directory Domain Services. I dati dinamici vengono in genere modificati più di frequente rispetto alla latenza di replica dovuta alla propagazione della modifica a tutte le repliche dei dati.

In Windows 2000 il supporto per i dati dinamici è limitato. L'archiviazione di dati dinamici in una partizione di dominio può essere complessa. I dati vengono replicati in tutti i controller di dominio del dominio spesso non necessari e possono causare dati incoerenti a causa della latenza di replica. Ciò può influire negativamente sulle prestazioni della rete. Inoltre, le partizioni di dominio non sono valide per le applicazioni che devono replicare i dati tra i limiti di dominio. Un'altra opzione in Windows 2000 consiste nell'archiviare i dati dinamici negli attributi contrassegnati come non replicati. Tuttavia, questa disposizione è limitata perché presenta un singolo punto di errore, ovvero, il singolo controller di dominio che ospita l'unica copia degli attributi non replicati dell'oggetto.

Le partizioni di directory applicative offrono la possibilità di controllare l'ambito di replica e consentono il posizionamento delle repliche in modo più appropriato per i dati dinamici. Di conseguenza, la partizione di directory applicativa offre la possibilità di ospitare i dati dinamici nel server Active Directory, consentendo in tal modo l'accesso ADSI/LDAP, senza influire significativamente sulle prestazioni della rete.

Il servizio DNS di Windows 2000 è un esempio di servizio che può sfruttare le partizioni di directory applicative. In Windows 2000, se il servizio DNS è eventualmente configurato per l'uso di Active Directory Domain Services, i dati della zona DNS vengono archiviati nel server di Active Directory in una partizione di dominio. Ovvero i dati vengono replicati in tutti i controller di dominio del dominio, indipendentemente dal fatto che un server DNS sia configurato per l'esecuzione sul controller di dominio. Si tratta di un'istanza in cui la replica completa a livello di dominio non è necessaria. Archiviando i dati della zona DNS in una partizione di directory applicativa, il servizio può ridefinire l'ambito della replica solo per quel subset di controller di dominio nel dominio che esegue effettivamente il server DNS.

Considerare gli scenari seguenti per l'hosting di una replica di una partizione di directory applicativa:

-   Una replica di una partizione di directory applicativa può essere creata in qualsiasi sistema operativo Windows Server 2003 e in un controller di dominio successivo in una foresta Active Directory Domain Services.
-   È possibile specificare il set di controller di dominio che ospitano repliche di una partizione di directory applicativa. A differenza di una partizione di dominio, non è necessario che una partizione di directory applicativa venga replicata in tutti i controller di dominio in un dominio e possa essere replicata nei controller di dominio in domini diversi della foresta.
-   Un controller di dominio con una replica della partizione di directory applicativa può coesistere e funzionare in un ambiente in modalità mista con altri computer che eseguono Windows 2000 o Windows NT 4,0.

I tipi di dati che possono essere archiviati in una partizione di directory applicativa includono:

-   Una partizione di directory applicativa può contenere istanze di qualsiasi tipo di oggetto, ad eccezione delle entità di sicurezza, ad esempio utenti, computer o gruppi.
-   Gli oggetti in una partizione di directory applicativa possono mantenere riferimenti DN-value ad altri oggetti nella stessa partizione di directory applicativa, agli oggetti nelle partizioni di configurazione e dello schema e a qualsiasi intestazione del contesto dei nomi, ovvero l'oggetto principale di una partizione di directory, ad esempio l'oggetto **domainDNS** all'inizio di una partizione di directory applicativa.
-   Per ulteriori informazioni e un esempio del tipo di dati dinamici che possono essere archiviati in una partizione di directory applicativa, vedere [oggetti dinamici](dynamic-objects.md). Gli oggetti dinamici sono supportati a partire da Windows Server 2003. Gli oggetti dinamici hanno una proprietà che determina la durata (TTL), dopo la quale l'oggetto viene eliminato dal server Active Directory.

Di seguito sono elencate alcune limitazioni delle partizioni di directory applicative:

-   Gli oggetti in una partizione di directory applicativa non possono mantenere *riferimenti a valori DN* a oggetti in altre partizioni di directory applicative o di dominio. (I riferimenti ai valori DN sono riferimenti permanenti a un valore del nome distinto, ad esempio "CN = someuser, DC = corp, DC = Fabrikam, DC = com"). Analogamente, gli oggetti in partizioni di dominio, configurazione e schema non possono mantenere i riferimenti DN-value agli oggetti in una partizione di directory applicativa. Un riferimento DN-valore può essere mantenuto nell'intestazione del contesto dei nomi. () )
-   Gli oggetti in una partizione di directory applicativa non vengono replicati nel catalogo globale. Come con qualsiasi controller di dominio, è anche possibile configurare un server di catalogo globale in modo che contenga una replica completa di una partizione di directory applicativa, ma i dati della partizione di directory applicativa sono completamente distinti dai dati del catalogo globale.
-   Quando viene creata una replica della partizione di directory applicativa, il Domain-Naming ruolo FSMO deve trovarsi in uno dei controller di dominio del sistema operativo Windows Server 2003 e versioni successive. Dopo la creazione della replica della partizione di directory applicativa, il ruolo FSMO per la denominazione dei domini può essere assegnato a un controller di dominio di Windows 2000.
-   Gli oggetti partizione di directory applicativa non possono essere spostati in altre partizioni Active Directory esterne alla partizione in cui sono state create.

Altre funzionalità della partizione di directory applicativa includono:

-   Il modello di controllo di sicurezza e di accesso per la partizione di directory applicativa è identico a quello per le altre partizioni in Active Directory Domain Services.
-   Gli intervalli di tempo che controllano la latenza di avvio di una notifica di modifica di origine ai partner di replica all'interno di un sito possono essere configurati separatamente per ogni partizione di directory applicativa.
-   Le partizioni di directory applicative possono essere denominate come domini normali, collegate ovunque nello spazio dei nomi Active Directory in cui un dominio può e individuato tramite DNS anche da sistemi Windows 2000 di livello inferiore.
-   È possibile creare una partizione di directory applicativa, l'ambito di replica definito e le impostazioni configurabili a livello di programmazione usando le API standard LDAP e ADSI. Per altre informazioni su come modificare a livello di codice le partizioni di directory applicative, vedere [partizioni di directory applicative](application-directory-partitions.md).

 

 




