---
title: Creazione ed eliminazione di oggetti in Active Directory Domain Services
description: La procedura utilizzata per creare ed eliminare oggetti in un Active Directory Domain Services a livello di codice dipende dalla tecnologia di programmazione utilizzata.
ms.assetid: 13f83aea-ad39-4737-af3c-24316a31046d
ms.tgt_platform: multiple
keywords:
- Creazione ed eliminazione di oggetti Active Directory In Active Directory
- Active Directory Domain Services Active Directory tramite la creazione e l'eliminazione di oggetti
- oggetti Active Directory , creazione ed eliminazione Active Directory Domain Services oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b681f7e4d193a248a8846ad8f02d1b3c222d735194bfe57940bd7e787710035d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118020432"
---
# <a name="creating-and-deleting-objects-in-active-directory-domain-services"></a>Creazione ed eliminazione di oggetti in Active Directory Domain Services

La procedura utilizzata per creare ed eliminare oggetti in un Active Directory Domain Services a livello di codice dipende dalla tecnologia di programmazione utilizzata. Per altre informazioni sulla creazione e l'eliminazione di oggetti in Active Directory Domain Services con una tecnologia di programmazione specifica, vedere gli argomenti elencati nella tabella seguente.



| Tecnologia di programmazione                                                                       | Per ulteriori informazioni                                                            |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Interfacce di servizio Active Directory](/windows/desktop/ADSI/active-directory-service-interfaces-adsi)         | [Creazione ed eliminazione di oggetti](/windows/desktop/ADSI/creating-and-deleting-objects)             |
| [Lightweight Directory Access Protocol](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) | [Modifica di una voce di directory](/previous-versions/windows/desktop/ldap/modifying-a-directory-entry)                 |
| [System.DirectoryServices](/dotnet/api/system.directoryservices) | [Creare, eliminare, rinominare e spostare oggetti](https://msdn.microsoft.com/library/ms180850(v=VS.80).aspx) |



 

## <a name="creating-an-object"></a>Creazione di un oggetto

In generale, gli unici attributi necessari per la creazione di un oggetto sono gli attributi **cn** **e objectClass.** La semplice creazione di un oggetto, tuttavia, non lo rende necessariamente un oggetto funzionale. Alcuni tipi di oggetti, ad esempio utenti e gruppi, hanno attributi obbligatori aggiuntivi per renderli funzionali. Per altre informazioni sulla creazione di tipi specifici di oggetti, vedere [Creazione di](creating-a-user.md) un utente e Creazione di gruppi in [un dominio.](creating-groups-in-a-domain.md)

**Windows Server 2003:** Quando viene creato un [](/windows/desktop/ADSchema/c-group)oggetto della classe utente [**,**](/windows/desktop/ADSchema/c-user)gruppo o [**computer**](/windows/desktop/ADSchema/c-computer) in un controller di dominio in esecuzione in WWindows Server 2003 o versioni successive, il controller di dominio imposta automaticamente l'attributo [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) per l'oggetto su una stringa univoca, se non è specificato.

## <a name="deleting-an-object"></a>Eliminazione di un oggetto

Il server Active Directory esegue le azioni seguenti quando viene eliminato un oggetto:

-   **L'attributo isDeleted** dell'oggetto eliminato è impostato su **TRUE.** Gli oggetti con **un valore di attributo isDeleted** impostato su **TRUE** sono denominati [*oggetti contrassegnati per la rimozione definitiva.*](/previous-versions/windows/desktop/legacy/ms681941(v=vs.85))
-   L'oggetto eliminato viene spostato nel contenitore Oggetti eliminati per il relativo contesto dei nomi. Se la proprietà **systemFlags dell'oggetto** contiene il flag 0x02000000, l'oggetto non viene spostato nel contenitore Oggetti eliminati. Per altre informazioni sull'associazione e sull'enumerazione del contenuto del contenitore Oggetti eliminati, vedere [Recupero di oggetti eliminati.](retrieving-deleted-objects.md)
-   Il contenitore Oggetti eliminati è flat, quindi tutti gli oggetti risiedono allo stesso livello all'interno del contenitore Oggetti eliminati. Di conseguenza, il nome distinto relativo dell'oggetto eliminato viene modificato per garantire che il nome sia univoco all'interno del contenitore Degli oggetti eliminati. Se il nome originale è più lungo di 75 caratteri, viene troncato a 75 caratteri. Al nuovo nome vengono quindi aggiunti gli elementi seguenti:
    1.  Carattere 0x0A
    2.  Stringa "DEL:"
    3.  Formato stringa di un GUID univoco, ad esempio "947e3228-70c9-4311-8b7a-e5c9b5bd4432"

    Un esempio di nome di oggetto eliminato è:
    ```C++
    Jeff Smith\0ADEL:947e3228-70c9-4311-8b7a-e5c9b5bd4432
    ```

    

-   La maggior parte dei valori di attributo per l'oggetto eliminato viene rimossa. Gli attributi seguenti vengono mantenuti automaticamente:

    -   **Attributeid**
    -   **attributeSyntax**
    -   **Distinguishedname**
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
    -   **Ncname**
    -   **Objectclass**
    -   **objectGUID**
    -   **objectSid**
    -   **oMSyntax**
    -   **proxiedObjectName**
    -   **replPropertyMetaData**
    -   **sAMAccountName**
    -   **securityIdentifier**
    -   **subClassOf**
    -   **systemFlags**
    -   **attributi trustAttributes**
    -   **Trustdirection**
    -   **trustPartner**
    -   **trustType**
    -   **userAccountControl**
    -   **Usnchanged**
    -   **uSNCreated**
    -   **whenCreated**

    Vengono mantenuti anche altri attributi con un valore di attributo **searchFlags** che 0x00000008 attributi.

    I valori di attributo seguenti vengono sempre rimossi da un oggetto eliminato:

    -   **objectCategory**
    -   **samAccountType**

-   Il descrittore di sicurezza dell'oggetto eliminato viene mantenuto e le voci di controllo di accesso ereditabili non vengono propagate. Il descrittore di sicurezza viene mantenuto così come è al momento dell'eliminazione dell'oggetto.
-   I collegamenti da e verso l'oggetto eliminato vengono cancellati. Questa operazione viene eseguita in background dopo l'eliminazione dell'oggetto. Se l'oggetto eliminato viene ripristinato prima che tutti i collegamenti siano cancellati, verrà visualizzato un errore.
-   Se l'oggetto viene eliminato in un controller di dominio di Windows Server 2003, l'attributo **lastKnownParent dell'oggetto** eliminato viene impostato sul nome distinto del contenitore in cui l'oggetto era contenuto al momento dell'eliminazione.

L'oggetto eliminato rimane nel contenitore Degli oggetti eliminati per un periodo di tempo noto come durata *di rimozione definitiva.* Per impostazione predefinita, la durata di rimozione definitiva è di 60 giorni, ma questo valore può essere modificato dall'amministratore di sistema. Dopo la scadenza della durata di rimozione definitiva, l'oggetto viene rimosso definitivamente dal servizio directory. Per evitare la mancanza di un'operazione di eliminazione, un'applicazione deve eseguire sincronizzazioni incrementali con maggiore frequenza rispetto alla durata di rimozione definitiva.

Windows Server 2003 aggiunge la possibilità di ripristinare gli oggetti eliminati. Per altre informazioni sul ripristino degli oggetti eliminati, vedere [Ripristino di oggetti eliminati.](restoring-deleted-objects.md)

Quando un elemento viene eliminato, nessuno degli attributi dell'oggetto può essere modificato. In Windows Server 2003 è possibile modificare il descrittore di sicurezza (attributo **ntSecurityDescriptor)** in un oggetto eliminato. Ciò consente il ripristino degli oggetti quando l'utente che esegue il ripristino dell'oggetto non dispone delle autorizzazioni di scrittura per gli attributi obbligatori. Per aggiornare il descrittore di sicurezza su un oggetto eliminato, il chiamante deve disporre del diritto di accesso di controllo "Rianimate Tombstone" nel contesto dei nomi, oltre ai normali accessi **WRITE \_ DAC** e **WRITE \_ OWNER.** Anche se il descrittore di sicurezza è restrittivo, l'amministratore può prima di tutto assumere la proprietà dell'oggetto, supponendo che abbia il privilegio **edizione Standard \_ TAKE OWNERSHIP \_ \_ NAME** e quindi modificare il descrittore di sicurezza. A tale scopo, usare la [**funzione ldap \_ modify \_ ext \_ s**](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_ext_s) con il [**controllo LDAP SERVER SHOW DELETED \_ \_ \_ \_ OID.**](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid) L'elenco di modifiche deve contenere una singola sostituzione di attributo per **l'attributo ntSecurityDescriptor.**

 

 