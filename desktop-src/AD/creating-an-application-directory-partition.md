---
title: Creazione di una partizione di directory applicativa
description: Una partizione di directory applicativa è rappresentata da un oggetto domainDNS con un valore di attributo instanceType di DS \_ INSTANCETYPE IS NC HEAD combinato con \_ \_ \_ DS \_ INSTANCETYPE \_ NC \_ IS \_ WRITEABLE.
ms.assetid: 5e90f316-9d67-484d-98b8-0632dd3c2c43
ms.tgt_platform: multiple
keywords:
- Creazione di una partizione di directory applicativa AD
- Partizioni di directory applicative AD , creazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c340bac215be62867dcddcda97326c33fc70c458ee242965258cc1ee24cf25f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118020540"
---
# <a name="creating-an-application-directory-partition"></a>Creazione di una partizione di directory applicativa

Una partizione di directory applicativa è rappresentata da un oggetto [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) con un valore dell'attributo [**instanceType**](/windows/desktop/ADSchema/a-instancetype) di **DS \_ INSTANCETYPE \_ IS \_ NC \_ HEAD** combinato con **DS \_ INSTANCETYPE \_ NC \_ IS \_ WRITEABLE.** Questo oggetto **domainDNS** rappresenta la radice della partizione di directory applicativa (NC head) ed è denominato in modo simile a una normale partizione di dominio, ad esempio "DC=dynamicdata,DC=fabrikam,DC=com", che corrisponde a un nome DNS "dynamicdata.fabrikam.com". È pertanto possibile creare un'istanza di una partizione di directory applicativa ovunque sia possibile creare un'istanza di una partizione di dominio. Non esiste alcun nome NetBIOS associato a una partizione di directory applicativa.

È possibile annidare partizioni di directory applicative, ad esempio una partizione di directory applicativa può avere partizioni di directory applicative figlio. Le ricerche con ambito sottoalbero rooted in un head della partizione di directory applicativa genereranno riferimenti di continuazione alle partizioni di directory applicative figlio.

Una replica di partizione di directory applicativa può essere creata solo in un controller di dominio in esecuzione in Windows Server 2003 e versioni successive e solo mentre il ruolo FSMO di Domain-Naming è utilizzato da un controller di dominio di Windows Server 2003 e versioni successive. In una foresta mista con controller di dominio di Windows Server 2003 e controller di dominio di livello inferiore (controller di dominio Windows 2000 o controller di dominio primari di Windows NT 4.0), un tentativo di creare una replica di partizione di directory applicativa in un controller di dominio di livello inferiore avrà esito negativo.

Una partizione di directory applicativa ha anche un oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) corrispondente nel contenitore Partizioni della partizione di configurazione. Il **crossRef** può essere creato manualmente prima di creare [**l'oggetto domainDNS.**](/windows/desktop/ADSchema/c-domaindns) L'oggetto **crossRef creato** in precedenza deve avere i valori di attributo indicati nella tabella seguente, in caso di esito negativo della creazione della partizione. Se **l'oggetto crossRef** non esiste, il server Active Directory ne creerà uno al momento della creazione della partizione di directory applicativa.

| Attributo                          | Descrizione                                                                                                                               |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot) | Contiene il percorso DNS del controller di dominio in cui verrà creata la partizione di directory applicativa.                               |
| [**Abilitato**](/windows/desktop/ADSchema/a-enabled) | Contiene **FALSE.**                                                                                                                       |
| [**Ncname**](/windows/desktop/ADSchema/a-ncname)   | Contiene il nome distinto della partizione. Nell'esempio precedente questo attributo conterrà "DC=dynamicdata,DC=mydomain,DC=com". |



 

**Per creare una nuova partizione di directory applicativa con la prima replica, seguire questa procedura**

1.  Eseguire il binding allo spazio dei nomi per la nuova partizione, specificando il controller di dominio che ospiterà la partizione di directory applicativa in ADsPath. Ad esempio, per creare una partizione con ADsPath "DC=dynamicdata,DC=mydomain,DC=com", il binding ADsPath sarà "LDAP:// <domain controller> /DC=mydomain,DC=com", dove " controller di dominio " è il nome DNS del controller di dominio che &lt; &gt; ospiterà la partizione.

    L'operazione di associazione deve specificare le opzioni fast e delegation. L'opzione fast consente l'esito positivo dell'associazione anche se lo spazio dei nomi non esiste. L'opzione di delega è necessaria per consentire al controller di dominio di contattare il Domain-Naming del ruolo FSMO usando le stesse credenziali.

    La versione di sistema del controller di dominio deve Windows sistema operativo Server 2003 e versioni successive.

2.  Creare un [**oggetto domainDNS**](/windows/desktop/ADSchema/c-domaindns) con un nome appropriato per la partizione, ad esempio "DC=dynamicdata", per rappresentare l'head del contesto dei nomi per la nuova partizione. **L'oggetto domainDNS** deve avere un attributo [**instanceType**](/windows/desktop/ADSchema/a-instancetype) con valore 5 (**DS \_ INSTANCETYPE \_ IS \_ NC \_ HEAD** \| **DS \_ INSTANCETYPE \_ NC IS \_ \_ WRITEABLE**). **L'attributo instanceType** può essere impostato solo in fase di creazione perché è un attributo solo di sistema.

Quando viene [**creato l'oggetto domainDNS,**](/windows/desktop/ADSchema/c-domaindns) il server Active Directory eseguirà i passaggi seguenti:

1.  Cerca un oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) nel contenitore Partitions con un valore di attributo [**nCName**](/windows/desktop/ADSchema/a-ncname) corrispondente al nome distinto della partizione e, se viene trovata una corrispondenza, modifica l'oggetto **crossRef** per rappresentare la partizione di directory dell'applicazione. Se non viene trovato un oggetto **crossRef** corrispondente, il server Active Directory crea un nuovo **oggetto crossRef** per rappresentare la partizione di directory dell'applicazione.

    Nella tabella seguente sono elencati gli attributi importanti [**dell'oggetto crossRef.**](/windows/desktop/ADSchema/c-crossref)

    | Attributo                                                              | Descrizione                                                                                                                                        |
    |------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
    | [**Ncname**](/windows/desktop/ADSchema/a-ncname)                                       | Contiene il nome distinto della partizione.                                                                                                  |
    | [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot)                                     | Contiene il nome DNS della partizione.                                                                                                            |
    | [**MsDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) | Il nome distinto [**dell'oggetto nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) del controller di dominio per la prima replica viene aggiunto a questo attributo. |

    

     

2.  Avviare una sincronizzazione della partizione di configurazione e attendere il completamento. In questo modo l'applicazione client può modificare i parametri di configurazione per la partizione di directory applicativa appena creata mentre è associata allo stesso controller di dominio usato per la creazione della partizione di directory applicativa.
3.  Creare [**l'oggetto domainDNS**](/windows/desktop/ADSchema/c-domaindns) con i flag **DS \_ INSTANCETYPE \_ IS \_ NC \_ HEAD** e **DS \_ INSTANCETYPE \_ NC \_ IS \_ WRITEABLE** impostati sulla [**proprietà instanceType.**](/windows/desktop/ADSchema/a-instancetype) La **proprietà instanceType** può contenere anche altri flag privati.
4.  Popolare l'attributo [**ms-DS-Has-Master-NCs**](/windows/desktop/ADSchema/a-msds-hasmasterncs) dell'oggetto [**nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) per il controller di dominio di destinazione con il nome distinto della partizione di directory applicativa appena creata.

Quando viene creata la partizione di directory applicativa o quando viene aggiunta e sincronizzata una nuova replica della partizione di directory applicativa, il server Active Directory registra correttamente la replica con NetLogon e DNS. Per altre informazioni e un elenco dei record SRV registrati, vedere Individuazione di un server host della partizione [di directory applicativa.](locating-an-application-directory-partition-host-server.md)

Per altre informazioni sulla creazione di una partizione di directory applicativa, vedere [Codice di esempio per la creazione di una partizione di directory applicativa.](example-code-for-creating-an-application-directory-partition.md)

## <a name="locating-the-partitions-container"></a>Individuazione del contenitore Partitions

Il nome distinto del contenitore Partitions è disponibile in uno dei due modi seguenti. La prima è più complessa da eseguire, ma fornirà sempre un risultato accurato:

1.  Eseguire l'associazione a RootDSE e ottenere **l'attributo configurationNamingContext.**
2.  Usare **l'attributo configurationNamingContext** per eseguire l'associazione al contenitore di configurazione.
3.  Cercare nel contenitore di configurazione un oggetto di [**tipo crossRefContainer.**](/windows/desktop/ADSchema/c-crossrefcontainer)
4.  Ottenere il **valore dell'attributo distinguishedName** [**dell'oggetto crossRefContainer.**](/windows/desktop/ADSchema/c-crossrefcontainer) Questo sarà il nome distinto del contenitore Partizioni.

Per altre informazioni e un esempio di codice che illustra questo metodo per individuare il contenitore Partitions, vedere la **funzione GetPartitionsDNSearch** in Codice di esempio per l'individuazione del contenitore [Partitions.](example-code-for-locating-the-partitions-container.md)

Il secondo metodo è più semplice da implementare, ma si basa sul contenitore Partitions con un particolare nome distinto relativo. Attualmente non è possibile modificare il nome del contenitore Partizioni, ma se questa funzionalità verrà aggiunta in futuro, la procedura seguente non funzionerà correttamente se il contenitore Partizioni è stato rinominato.

1.  Eseguire l'associazione a RootDSE e ottenere **l'attributo configurationNamingContext.**
2.  Combinare la stringa "CN=Partitions" seguita dall'attributo **configurationNamingContext** per formare il nome distinto del contenitore Partitions. Il nome distinto sarà nel formato "CN=Partitions, <configuration DN> ".

Per altre informazioni e un esempio di codice che illustra questo metodo per individuare il contenitore Partitions, vedere la **funzione GetPartitionsDNManual** in Codice di esempio per l'individuazione del contenitore [Partitions.](example-code-for-locating-the-partitions-container.md)

 

 