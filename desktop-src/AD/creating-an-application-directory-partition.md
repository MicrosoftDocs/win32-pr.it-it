---
title: Creazione di una partizione di directory applicativa
description: Una partizione di directory applicativa è rappresentata da un oggetto domainDNS con un valore di attributo instanceType di DS \_ instanceType \_ è la \_ \_ testa NC combinata con DS \_ instanceType \_ NC \_ è \_ scrivibile.
ms.assetid: 5e90f316-9d67-484d-98b8-0632dd3c2c43
ms.tgt_platform: multiple
keywords:
- Creazione di una partizione di directory applicativa AD
- Directory dell'applicazione-partizioni di Active Directory, creazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a17471696825179b6e49230b5168abbaf88b8e2
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472622"
---
# <a name="creating-an-application-directory-partition"></a>Creazione di una partizione di directory applicativa

Una partizione di directory applicativa è rappresentata da un oggetto [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) con un valore di attributo [**instanceType**](/windows/desktop/ADSchema/a-instancetype) di **DS \_ instanceType \_ è la \_ \_ testa NC** combinata con **DS \_ instanceType \_ NC \_ è \_ scrivibile**. Questo oggetto **domainDNS** rappresenta la radice della partizione di directory applicativa (Head NC) ed è denominato simile a una partizione di dominio normale, ad esempio, "DC = DYNAMICDATA, DC = Fabrikam, DC = com", che corrisponde a un nome DNS "DynamicData.fabrikam.com". È quindi possibile creare un'istanza di una partizione di directory applicativa ovunque sia possibile creare un'istanza di una partizione di dominio. Nessun nome NetBIOS associato a una partizione di directory applicativa.

È possibile annidare le partizioni di directory applicative, ovvero una partizione di directory applicativa può includere partizioni di directory applicative figlio. Ricerche con ambito sottoalbero con radice in una partizione di directory applicativa Head genererà riferimenti di continuazione alle partizioni di directory dell'applicazione figlio.

È possibile creare una replica della partizione di directory applicativa solo in un controller di dominio in esecuzione in Windows Server 2003 e versioni successive e solo quando il Domain-Naming ruolo FSMO è gestito da un controller di dominio Windows Server 2003 e versioni successive. In una foresta mista che dispone di controller di dominio Windows Server 2003 e controller di dominio di livello inferiore (controller di dominio Windows 2000 o controller di dominio primario di Windows NT 4,0), il tentativo di creare una replica della partizione di directory applicativa in un controller di dominio di livello inferiore avrà esito negativo.

Una partizione di directory applicativa dispone anche di un oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) corrispondente nel contenitore partizioni della partizione di configurazione. **CrossRef** può essere creato manualmente prima di creare l'oggetto [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) . Per l'oggetto **crossRef** creato in precedenza devono essere presenti i valori di attributo indicati nella tabella seguente, altrimenti la creazione della partizione avrà esito negativo. Se l'oggetto **crossRef** non esiste, il server Active Directory ne creerà uno al momento della creazione della partizione di directory applicativa.

| Attributo                          | Descrizione                                                                                                                               |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot) | Contiene il percorso DNS del controller di dominio in cui verrà creata la partizione di directory applicativa.                               |
| [**Abilitato**](/windows/desktop/ADSchema/a-enabled) | Contiene **false**.                                                                                                                       |
| [**nCName**](/windows/desktop/ADSchema/a-ncname)   | Contiene il nome distinto della partizione. Nell'esempio precedente, questo attributo conterrebbe "DC = DynamicData, DC = dominio, DC = com". |



 

**Per creare una nuova partizione di directory applicativa con la prima replica, seguire questa procedura**

1.  Eseguire l'associazione allo spazio dei nomi per la nuova partizione, specificando il controller di dominio che ospiterà la partizione di directory applicativa in ADsPath. Ad esempio, per creare una partizione con ADsPath "DC = DynamicData, DC = dominio, DC = com", il binding ADsPath sarà "LDAP:// <domain controller> /DC = dominio, DC = com", dove " &lt; domain controller &gt; " è il nome DNS del controller di dominio che ospiterà la partizione.

    L'operazione di associazione deve specificare le opzioni Fast e Delegation. L'opzione Fast consente l'esito positivo dell'associazione anche se lo spazio dei nomi non esiste. L'opzione delega è necessaria per consentire al controller di dominio di contattare il titolare del ruolo FSMO Domain-Naming usando le stesse credenziali.

    La versione di sistema del controller di dominio deve essere sistema operativo Windows Server 2003 e versioni successive.

2.  Creare un oggetto [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) con un nome appropriato per la partizione, ad esempio "DC = DynamicData", per rappresentare l'intestazione del contesto dei nomi per la nuova partizione. L'oggetto **domainDNS** deve avere un attributo [**instanceType**](/windows/desktop/ADSchema/a-instancetype) con un valore pari a 5 (**DS \_ instanceType \_ è \_ NC \_ Head** \| **DS \_ instanceType \_ NC \_ è \_ scrivibile**). L'attributo **instanceType** può essere impostato solo in fase di creazione perché è un attributo di sistema.

Quando viene creato l'oggetto [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) , il server Active Directory eseguirà i passaggi seguenti:

1.  Cerca un oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) nel contenitore partizioni con un valore di attributo [**NCName**](/windows/desktop/ADSchema/a-ncname) corrispondente al nome distinto della partizione e, se viene trovata una corrispondenza, modifica l'oggetto **crossRef** per rappresentare la partizione di directory applicativa. Se non viene trovato un oggetto **crossRef** corrispondente, il server Active Directory crea un nuovo oggetto **crossRef** per rappresentare la partizione di directory applicativa.

    Nella tabella seguente sono elencati gli attributi importanti dell'oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) .

    | Attributo                                                              | Descrizione                                                                                                                                        |
    |------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
    | [**nCName**](/windows/desktop/ADSchema/a-ncname)                                       | Contiene il nome distinto della partizione.                                                                                                  |
    | [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot)                                     | Contiene il nome DNS della partizione.                                                                                                            |
    | [**msDS-NC-replica-posizioni**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) | All'attributo viene aggiunto il nome distinto dell'oggetto [**NTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) del controller di dominio per la prima replica. |

    

     

2.  Avviare una sincronizzazione della partizione di configurazione e attendere il completamento. Ciò consente all'applicazione client di modificare i parametri di configurazione per la partizione di directory applicativa appena creata mentre è associato allo stesso controller di dominio utilizzato per creare la partizione di directory applicativa.
3.  Creare l'oggetto [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) con **DS \_ INSTANCETYPE \_ è \_ NC \_ Head** e **DS \_ INSTANCETYPE \_ NC sono flag \_ \_ scrivibili** impostati per la proprietà [**INSTANCETYPE**](/windows/desktop/ADSchema/a-instancetype) . La proprietà **instanceType** può contenere anche altri flag privati.
4.  Popolare l'attributo [**ms-DS-has-Master-NCs**](/windows/desktop/ADSchema/a-msds-hasmasterncs) dell'oggetto [**NTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) per il controller di dominio di destinazione con il nome distinto della partizione di directory applicativa appena creata.

Quando viene creata la partizione di directory applicativa o quando una nuova replica della partizione di directory applicativa viene aggiunta e completamente sincronizzata, il server Active Directory registra correttamente la replica con NetLogon e DNS. Per ulteriori informazioni e per un elenco dei record SRV registrati, vedere [individuazione di un server host partizione di directory applicativa](locating-an-application-directory-partition-host-server.md).

Per ulteriori informazioni sulla creazione di una partizione di directory applicativa, vedere il [codice di esempio per la creazione di una partizione di directory applicativa](example-code-for-creating-an-application-directory-partition.md).

## <a name="locating-the-partitions-container"></a>Individuazione del contenitore di partizioni

Il nome distinto del contenitore partizioni può essere trovato in uno dei due modi seguenti. Il primo è più complicato da eseguire, ma fornirà sempre un risultato accurato:

1.  Eseguire l'associazione a RootDSE e ottenere l'attributo **configurationNamingContext** .
2.  Usare l'attributo **configurationNamingContext** per eseguire l'associazione al contenitore di configurazione.
3.  Eseguire una ricerca nel contenitore di configurazione per un oggetto di tipo [**crossRefContainer**](/windows/desktop/ADSchema/c-crossrefcontainer) .
4.  Ottenere il valore dell'attributo **Distinguishname** dell'oggetto [**crossRefContainer**](/windows/desktop/ADSchema/c-crossrefcontainer) . Si tratta del nome distinto del contenitore di partizioni.

Per ulteriori informazioni e un esempio di codice che illustra questo metodo per l'individuazione del contenitore di partizioni, vedere la funzione **GetPartitionsDNSearch** nel [codice di esempio per l'individuazione del contenitore di partizioni](example-code-for-locating-the-partitions-container.md).

Il secondo metodo è più semplice da implementare, ma si basa sul contenitore di partizioni con un nome distinto relativo specifico. Non è attualmente possibile modificare il nome del contenitore di partizioni, ma se questa funzionalità verrà aggiunta in futuro, la procedura seguente non funzionerà correttamente se il contenitore di partizioni è stato rinominato.

1.  Eseguire l'associazione a RootDSE e ottenere l'attributo **configurationNamingContext** .
2.  Combinare la stringa "CN = Partitions" seguita dall'attributo **configurationNamingContext** per formare il nome distinto del contenitore di partizioni. Il nome distinto avrà il formato "CN = partizioni <configuration DN> ".

Per ulteriori informazioni e un esempio di codice che illustra questo metodo per l'individuazione del contenitore di partizioni, vedere la funzione **GetPartitionsDNManual** nel [codice di esempio per l'individuazione del contenitore di partizioni](example-code-for-locating-the-partitions-container.md).

 

 