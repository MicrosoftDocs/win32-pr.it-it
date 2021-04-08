---
title: Modificare le notifiche in Active Directory Domain Services
description: Active Directory Domain Services fornire un meccanismo per la registrazione di un'applicazione client con un controller di dominio per la ricezione delle notifiche di modifica.
ms.assetid: 27f6c7c1-b32e-457a-9be5-47836d097ab1
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee564727cfbcb2bfdb367f822fdc137bca7c4e37
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046554"
---
# <a name="change-notifications-in-active-directory-domain-services"></a>Modificare le notifiche in Active Directory Domain Services

Active Directory Domain Services fornire un meccanismo per la registrazione di un'applicazione client con un controller di dominio per la ricezione delle notifiche di modifica. A tale scopo, il client specifica il controllo di notifica delle modifiche LDAP in un'operazione di ricerca LDAP asincrona. Il client specifica anche i parametri di ricerca seguenti.



| Parametro             | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ambito<br/>      | Specificare una **\_ \_ base di ambito LDAP** per monitorare solo l'oggetto o **l' \_ ambito LDAP \_ unlivello** per monitorare gli elementi figlio immediati dell'oggetto, escluso l'oggetto stesso. Non specificare un **\_ \_ sottoalbero con ambito LDAP**. Sebbene l'ambito del sottoalbero sia supportato se l'oggetto di base è la radice di un contesto dei nomi, il suo utilizzo può influire gravemente sulle prestazioni del server, perché genera un messaggio di risultato della ricerca LDAP ogni volta che viene modificato un oggetto nel contesto dei nomi. Non è possibile specificare un **\_ \_ sottoalbero con ambito LDAP** per un sottoalbero arbitrario.<br/> |
| Filtra<br/>     | Specificare un filtro di ricerca "(objectClass = \* )", che significa che vengono ricevute le notifiche per le modifiche apportate a qualsiasi oggetto nell'ambito specificato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                |
| Attributi<br/> | Consente di specificare un elenco di attributi da restituire quando si verifica una modifica. Tenere presente che si ricevono notifiche quando viene modificato un attributo, non solo gli attributi specificati.<br/>                                                                                                                                                                                                                                                                                                                                                                               |



 

È possibile registrare fino a cinque richieste di notifica su una singola connessione LDAP. È necessario disporre di un thread dedicato che attenda le notifiche e li elabori rapidamente. Quando si chiama la \_ \_ funzione Ext di ricerca LDAP per registrare una richiesta di notifica, la funzione restituisce un identificatore di messaggio che identifica la richiesta. Si usa quindi la [**funzione \_ risultato LDAP**](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result) per attendere le notifiche di modifica. Quando si verifica una modifica, il server invia un messaggio LDAP contenente l'identificatore del messaggio per la richiesta di notifica che ha generato la notifica. Questa operazione determina la restituzione della funzione di **\_ risultato LDAP** con i risultati della ricerca che identificano l'oggetto modificato.

L'applicazione client deve determinare lo stato iniziale dell'oggetto monitorato. A tale scopo, è necessario prima registrare la richiesta di notifica e quindi leggere lo stato corrente.

Anche l'applicazione client deve determinare la ragione della modifica. Per una ricerca a livello di base, una notifica si verifica quando viene modificato qualsiasi attributo o quando l'oggetto viene eliminato o spostato. Per una ricerca a un livello, si verifica una notifica quando un oggetto figlio viene creato, eliminato, spostato o modificato. Tenere presente che la modifica o la ridenominazione di un oggetto nella gerarchia precedente a un oggetto di destinazione non genera una notifica anche se il nome distinto della destinazione è stato modificato di conseguenza. Se, ad esempio, si esegue il monitoraggio delle modifiche apportate agli oggetti figlio in un contenitore, le notifiche non vengono ricevute se il contenitore stesso è stato spostato o rinominato.

Quando il client elabora i risultati della ricerca, può utilizzare la \_ funzione LDAP Get \_ DN per ottenere il nome distinto dell'oggetto modificato. Non basarsi sui nomi distinti per identificare gli oggetti monitorati, perché i nomi distinti possono cambiare. In alternativa, includere l'attributo **objectGUID** nell'elenco di attributi da recuperare. Il **objectGUID** di ogni oggetto rimane invariato indipendentemente dalla posizione in cui l'oggetto viene spostato all'interno della foresta aziendale.

Se un oggetto all'interno dell'ambito di ricerca viene eliminato, il client riceve una notifica di modifica e l'attributo **Indeleted** dell'oggetto viene impostato su **true**. In questo caso, i risultati della ricerca segnalano il nuovo nome distinto dell'oggetto nel contenitore degli oggetti eliminati della relativa partizione. Non è necessario specificare il controllo contrassegnato per la rimozione definitiva (server LDAP, ovvero l'[ \_ \_ \_ \_ OID eliminato](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid)) per ricevere le notifiche delle eliminazioni di oggetti. Per ulteriori informazioni, vedere [recupero di oggetti eliminati](retrieving-deleted-objects.md).

Quando un client ha registrato una richiesta di notifica, il client continua a ricevere notifiche fino a quando la connessione non viene interrotta o il client abbandona la ricerca chiamando la \_ funzione di abbandono LDAP. Se il client o il server si disconnette, ad esempio in caso di errore del server, la richiesta di notifica viene terminata. Quando il client si riconnette, deve registrarsi di nuovo per le notifiche e quindi leggere lo stato corrente degli oggetti di interesse nel caso in cui siano state apportate modifiche mentre il client è stato disconnesso.

Il client può usare il valore dell'attributo **uSNChanged** di un oggetto per determinare se lo stato corrente dell'oggetto nel server riflette le ultime modifiche ricevute dal client. Il sistema aumenta l'attributo **uSNChanged** di un oggetto quando l'oggetto viene spostato o modificato. Se, ad esempio, il server ha esito negativo e la partizione di directory viene ripristinata da un backup, la replica del server di un oggetto potrebbe non riflettere le modifiche precedentemente segnalate al client, nel qual caso il valore **uSNChanged** sul server sarà inferiore al valore archiviato dal client.

Per ulteriori informazioni e un esempio di codice in cui viene utilizzato il controllo di notifica delle modifiche LDAP in un'operazione di ricerca LDAP asincrona, vedere il [codice di esempio per la ricezione delle notifiche delle modifiche](example-code-for-receiving-change-notifications.md).

Per ulteriori informazioni sull'utilizzo del controllo delle notifiche delle modifiche LDAP, vedere [Cenni preliminari sulle tecniche di rilevamento modifiche](overview-of-change-tracking-techniques.md).

 

