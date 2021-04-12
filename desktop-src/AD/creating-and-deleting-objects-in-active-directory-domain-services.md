---
title: Creazione ed eliminazione di oggetti in Active Directory Domain Services
description: La procedura utilizzata per creare ed eliminare oggetti a livello di codice in Active Directory Domain Services dipende dalla tecnologia di programmazione utilizzata.
ms.assetid: 13f83aea-ad39-4737-af3c-24316a31046d
ms.tgt_platform: multiple
keywords:
- Creazione ed eliminazione di oggetti Active Directory Active Directory
- Active Directory Domain Services Active Directory, utilizzo della creazione e dell'eliminazione di oggetti
- oggetti Active Directory, creazione ed eliminazione di oggetti Active Directory Domain Services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11d3e85ef3c356978faeab059e3969bb657185bd
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472619"
---
# <a name="creating-and-deleting-objects-in-active-directory-domain-services"></a>Creazione ed eliminazione di oggetti in Active Directory Domain Services

La procedura utilizzata per creare ed eliminare oggetti a livello di codice in Active Directory Domain Services dipende dalla tecnologia di programmazione utilizzata. Per ulteriori informazioni sulla creazione e l'eliminazione di oggetti in Active Directory Domain Services con una tecnologia di programmazione specifica, vedere gli argomenti elencati nella tabella seguente.



| Tecnologia di programmazione                                                                       | Per ulteriori informazioni                                                            |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Interfacce di servizio Active Directory](/windows/desktop/ADSI/active-directory-service-interfaces-adsi)         | [Creazione ed eliminazione di oggetti](/windows/desktop/ADSI/creating-and-deleting-objects)             |
| [Lightweight Directory Access Protocol](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) | [Modifica di una voce di directory](/previous-versions/windows/desktop/ldap/modifying-a-directory-entry)                 |
| [System.DirectoryServices](/dotnet/api/system.directoryservices) | [Creazione, eliminazione, ridenominazione e spostamento di oggetti](https://msdn.microsoft.com/library/ms180850(v=VS.80).aspx) |



 

## <a name="creating-an-object"></a>Creazione di un oggetto

In generale, gli unici attributi necessari per la creazione di un oggetto sono gli attributi **CN** e **objectClass** . La semplice creazione di un oggetto non lo rende tuttavia necessariamente un oggetto funzionale. Alcuni tipi di oggetti, ad esempio utenti e gruppi, hanno attributi obbligatori aggiuntivi per renderli funzionali. Per ulteriori informazioni sulla creazione di tipi specifici di oggetti, vedere [creazione di un utente](creating-a-user.md) e [creazione di gruppi in un dominio](creating-groups-in-a-domain.md).

**Windows Server 2003:** Quando viene creato un oggetto della classe [**utente**](/windows/desktop/ADSchema/c-user), [**gruppo**](/windows/desktop/ADSchema/c-group)o [**computer**](/windows/desktop/ADSchema/c-computer) in un controller di dominio in esecuzione su WWindows Server 2003 o versione successiva, il controller di dominio imposta automaticamente l'attributo [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) per l'oggetto su una stringa univoca, se non ne viene specificata una.

## <a name="deleting-an-object"></a>Eliminazione di un oggetto

Quando viene eliminato un oggetto, il server Active Directory esegue le azioni seguenti:

-   L'attributo **Dedeleted** dell'oggetto eliminato è impostato su **true**. Gli oggetti con un valore di attributo **Andeleted** impostati su **true** vengono chiamati oggetti contrassegnati per la [*rimozione definitiva*](/previous-versions/windows/desktop/legacy/ms681941(v=vs.85)).
-   L'oggetto eliminato viene spostato nel contenitore degli oggetti eliminati per il contesto dei nomi. Se la proprietà **systemFlags** dell'oggetto contiene il flag 0x02000000, l'oggetto non viene spostato nel contenitore degli oggetti eliminati. Per ulteriori informazioni sull'associazione ed enumerazione del contenuto del contenitore degli oggetti eliminati, vedere Recupero di [oggetti eliminati](retrieving-deleted-objects.md).
-   Il contenitore degli oggetti eliminati è Flat, quindi tutti gli oggetti si trovano allo stesso livello all'interno del contenitore degli oggetti eliminati. Il nome distinto relativo dell'oggetto eliminato viene quindi modificato per garantire che il nome sia univoco all'interno del contenitore degli oggetti eliminati. Se il nome originale è più lungo di 75 caratteri, viene troncato a 75 caratteri. Il codice seguente viene quindi aggiunto al nuovo nome:
    1.  Carattere 0x0A
    2.  Stringa "DEL:"
    3.  Formato stringa di un GUID univoco, ad esempio "947e3228-70c9-4311-8b7a-e5c9b5bd4432"

    Un esempio di nome di oggetto eliminato è:
    ```C++
    Jeff Smith\0ADEL:947e3228-70c9-4311-8b7a-e5c9b5bd4432
    ```

    

-   La maggior parte dei valori di attributo per l'oggetto eliminato viene rimossa. Gli attributi seguenti vengono conservati automaticamente:

    -   **Elemento AttributeID**
    -   **attributeSyntax**
    -   **distinguishedName**
    -   **dNReferenceUpdate**
    -   **flatName**
    -   **governsID**
    -   **groupType**
    -   **instanceType**
    -   **lDAPDisplayName**
    -   **legacyExchangeDN**
    -   **mS-DS-CreatorSID**
    -   **mSMQOwnerID**
    -   **nome**
    -   **nCName**
    -   **objectClass**
    -   **objectGUID**
    -   **objectSid**
    -   **oMSyntax**
    -   **proxiedObjectName**
    -   **replPropertyMetaData**
    -   **sAMAccountName**
    -   **securityIdentifier**
    -   **subClassOf**
    -   **systemFlags**
    -   **trustAttributes**
    -   **trustDirection**
    -   **trustPartner**
    -   **trustType**
    -   **userAccountControl**
    -   **uSNChanged**
    -   **uSNCreated**
    -   **whenCreated**

    Vengono conservati anche altri attributi con un valore dell'attributo **searchFlags** che contiene 0x00000008.

    I valori di attributo seguenti vengono sempre rimossi da un oggetto eliminato:

    -   **objectCategory**
    -   **samAccountType**

-   Il descrittore di sicurezza dell'oggetto eliminato viene mantenuto e le voci di controllo di accesso ereditabili non vengono propagate. Il descrittore di sicurezza viene mantenuto così com'è al momento dell'eliminazione dell'oggetto.
-   I collegamenti a e dall'oggetto eliminato vengono cancellati. Questa operazione viene eseguita in background dopo l'eliminazione dell'oggetto. Se l'oggetto eliminato viene ripristinato prima che tutti i collegamenti vengano cancellati, verrà ricevuto un errore.
-   Se l'oggetto viene eliminato in un controller di dominio Windows Server 2003, l'attributo **lastKnownParent** dell'oggetto Deleted viene impostato sul nome distinto del contenitore in cui l'oggetto era contenuto al momento dell'eliminazione.

L'oggetto eliminato rimane nel contenitore degli oggetti eliminati per un periodo di tempo noto come *durata della rimozione definitiva*. Per impostazione predefinita, la durata di rimozione definitiva è 60 giorni, ma questo valore può essere modificato dall'amministratore di sistema. Al termine della durata dell'oggetto contrassegnato per la rimozione definitiva, l'oggetto viene rimosso definitivamente dal servizio directory. Per evitare che venga persa un'operazione di eliminazione, un'applicazione deve eseguire sincronizzazioni incrementali con maggiore frequenza rispetto alla durata di rimozione definitiva.

Windows Server 2003 aggiunge la possibilità di ripristinare gli oggetti eliminati. Per ulteriori informazioni sul ripristino degli oggetti eliminati, vedere [ripristino degli oggetti eliminati](restoring-deleted-objects.md).

Quando viene eliminato un elemento, nessuno degli attributi dell'oggetto può essere modificato. In Windows Server 2003 è possibile modificare il descrittore di sicurezza (attributo **ntSecurityDescriptor** ) su un oggetto eliminato. Ciò consente di ripristinare gli oggetti quando la persona che esegue il ripristino dell'oggetto non dispone delle autorizzazioni di scrittura per gli attributi obbligatori. Per aggiornare il descrittore di sicurezza in un oggetto eliminato, il chiamante deve disporre del controllo di accesso per la rimozione definitiva "reanimate" nel contesto dei nomi, oltre all' **\_ applicazione livello dati** normale di scrittura e all'accesso al **\_ proprietario** . Anche se il descrittore di sicurezza è restrittivo, l'amministratore può prima assumere la proprietà dell'oggetto, supponendo che l'amministratore disponga del privilegio **se \_ accetta il \_ \_ nome della proprietà** e quindi modifica il descrittore di sicurezza. A tale scopo, usare la funzione [**LDAP \_ Modify \_ ext \_ s**](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_ext_s) con il [**server LDAP Mostra il controllo \_ \_ \_ \_ OID eliminato**](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid) . L'elenco di modifiche deve contenere una sostituzione di attributo singolo per l'attributo **ntSecurityDescriptor** .

 

 