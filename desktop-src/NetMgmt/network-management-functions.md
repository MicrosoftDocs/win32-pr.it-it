---
title: Funzioni di gestione della rete
description: Le funzioni di gestione della rete possono essere raggruppate nel modo seguente.
ms.assetid: dd159e2e-f37e-46b2-b980-008b73d40b39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9e9aba93607e3609f0d20f7208184f169fb871ee67f5f2917445683f70e4f04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796962"
---
# <a name="network-management-functions"></a>Funzioni di gestione della rete

Le funzioni di gestione della rete possono essere raggruppate nel modo seguente.

## <a name="alert-functions"></a>Funzioni di avviso



| Funzione                                   | Descrizione                                                                                                                                                                                            |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetAlertRaise**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraise)     | Notifica a tutti i client registrati che si è verificato un evento specifico.                                                                                                                                  |
| [**NetAlertRaiseEx**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraiseex) | Semplifica la notifica ai client registrati che si è verificato un evento specifico, perché, a differenza di **NetAlertRaise,** **NetAlertRaiseEx** non richiede una [**struttura STD \_ ALERT.**](/windows/desktop/api/Lmalert/ns-lmalert-std_alert) |



 

## <a name="api-buffer-functions"></a>Funzioni buffer API



| Funzione                                                 | Descrizione                                                                                                               |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**NetApiBufferAllocate**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferallocate)     | Alloca memoria dall'heap. Chiamare questa funzione quando è necessaria la compatibilità con **la funzione NetApiBufferFree.** |
| [**NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree)             | Libera la memoria allocata dalla **funzione NetApiBufferAllocate** e da altre funzioni di gestione di rete.                   |
| [**NetApiBufferReallocate**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferreallocate) | Modifica le dimensioni di un buffer allocato da una chiamata alla **funzione NetApiBufferAllocate.**                                |
| [**NetApiBufferSize**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibuffersize)             | Restituisce le dimensioni, in byte, di un buffer allocato da una chiamata alla **funzione NetApiBufferAllocate.**                     |



 

## <a name="azure-active-directory-join-information-functions"></a>Azure Active Directory Funzioni di informazioni di join



| Funzione                                                       | Descrizione                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetFreeAadJoinInformation**](/windows/desktop/api/lmjoin/nf-lmjoin-netfreeaadjoininformation) | Libera la memoria allocata per la struttura [**DSREG \_ JOIN \_ INFO**](/windows/desktop/api/lmjoin/ns-lmjoin-dsreg_join_info) specificata, che contiene le informazioni di join per un tenant e recuperate chiamando la [**funzione NetGetAadJoinInformation.**](/windows/desktop/api/lmjoin/nf-lmjoin-netgetaadjoininformation) |
| [**NetGetAadJoinInformation**](/windows/desktop/api/lmjoin/nf-lmjoin-netgetaadjoininformation)   | Recupera le informazioni di join per il tenant specificato. Questa funzione esamina le informazioni di join per Microsoft Azure Active Directory e l'account aziendale aggiunto dall'utente corrente.                                                                     |



 

## <a name="directory-service-and-domain-join-functions"></a>Funzioni di aggiunta al dominio e al servizio directory



| Funzione                                                                             | Descrizione                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetAddAlternateComputerName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netaddalternatecomputername)                   | Aggiunge un nome alternativo per il computer specificato.                                                                                                                                                                                                                      |
| [**NetCreateProvisioningPackage**](/windows/desktop/api/Lmjoin/nf-lmjoin-netprovisioncomputeraccount)                  | Effettua il provisioning di un account computer per un uso successivo in un'operazione di aggiunta a un dominio offline.                                                                                                                                                                                        |
| [**NetEnumerateComputerNames**](/windows/desktop/api/Lmjoin/nf-lmjoin-netenumeratecomputernames)                       | Enumera i nomi per il computer specificato.                                                                                                                                                                                                                            |
| [**NetGetJoinableOUs**](/windows/desktop/api/Lmjoin/nf-lmjoin-netgetjoinableous)                                       | Recupera un elenco di unità organizzative in cui è possibile creare un account computer.                                                                                                                                                                              |
| [**NetGetJoinInformation**](/windows/desktop/api/Lmjoin/nf-lmjoin-netgetjoininformation)                               | Recupera le informazioni sullo stato del join per il computer specificato.                                                                                                                                                                                                           |
| [**NetJoinDomain**](/windows/desktop/api/Lmjoin/nf-lmjoin-netjoindomain)                                               | Aggiunge un computer a un gruppo di lavoro o a un dominio.                                                                                                                                                                                                                              |
| [**NetProvisionComputerAccount**](/windows/desktop/api/Lmjoin/nf-lmjoin-netprovisioncomputeraccount)                   | Esegue il provisioning di un account computer per un uso successivo in un'operazione di aggiunta a un dominio offline.                                                                                                                                                                                       |
| [**NetRemoveAlternateComputerName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netremovealternatecomputername)             | Rimuove un nome alternativo per il computer specificato.                                                                                                                                                                                                                   |
| [**NetRenameMachineInDomain**](/windows/desktop/api/Lmjoin/nf-lmjoin-netrenamemachineindomain)                         | Modifica il nome di un computer in un dominio.                                                                                                                                                                                                                             |
| [**NetRequestOfflineDomainJoin**](/windows/desktop/api/Lmjoin/nf-lmjoin-netrequestofflinedomainjoin)                   | Viene eseguito in locale in un computer per modificare Windows'immagine del sistema operativo montata in un volume. Il Registro di sistema viene caricato per l'immagine e i dati BLOB di provisioning vengono scritti in cui possono essere recuperati durante la fase di completamento di un'operazione di aggiunta a un dominio offline.     |
| [**NetRequestProvisioningPackageInstall**](/windows/desktop/api/Lmjoin/nf-lmjoin-netrequestprovisioningpackageinstall) | Viene eseguito in locale in un computer per modificare Windows'immagine del sistema operativo montata in un volume. Il Registro di sistema viene caricato dall'immagine e i dati del pacchetto di provisioning vengono scritti in cui possono essere recuperati durante la fase di completamento di un'operazione di aggiunta a un dominio offline. |
| [**NetSetPrimaryComputerName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netsetprimarycomputername)                       | Imposta il nome del computer primario per il computer specificato.                                                                                                                                                                                                              |
| [**NetUnjoinDomain**](/windows/desktop/api/Lmjoin/nf-lmjoin-netunjoindomain)                                           | Scollega un computer da un gruppo di lavoro o da un dominio.                                                                                                                                                                                                                        |
| [**NetValidateName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netvalidatename)                                           | Verifica la validità di un nome computer, un nome di gruppo di lavoro o un nome di dominio.                                                                                                                                                                                               |



 

## <a name="get-functions"></a>Funzioni Get



| Funzione                                                               | Descrizione                                                                                                                              |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetGetAnyDCName**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetanydcname)                             | Restituisce il nome di qualsiasi controller di dominio per un dominio considerato direttamente attendibile da un server specificato.                                   |
| [**NetGetDCName**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdcname)                                   | Restituisce il nome del controller di dominio primario (PDC) per il dominio specificato.                                                        |
| [**NetGetDisplayInformationIndex**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdisplayinformationindex) | Restituisce l'indice della prima voce di informazioni di visualizzazione il cui nome inizia con una stringa specificata o segue alfabeticamente la stringa. |
| [**NetQueryDisplayInformation**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation)       | Restituisce informazioni sull'account utente, computer o gruppo globale.                                                                             |



 

## <a name="group-functions"></a>Funzioni di gruppo



| Funzione                                     | Descrizione                                                                       |
|----------------------------------------------|-----------------------------------------------------------------------------------|
| [**NetGroupAggiungi**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd)           | Crea un gruppo globale.                                                           |
| [**NetGroupAddUser**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadduser)   | Aggiunge un utente a un gruppo globale esistente.                                        |
| [**NetGroupDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdel)           | Rimuove un gruppo globale indipendentemente dal fatto che il gruppo abbia o meno membri.                  |
| [**NetGroupDelUser**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdeluser)   | Rimuove un nome utente da un gruppo globale.                                        |
| [**NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum)         | Elenca tutti i gruppi globali in un server.                                              |
| [**NetGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo)   | Restituisce informazioni su un gruppo globale specifico.                              |
| [**NetGroupGetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers) | Elenca tutti i membri di un gruppo globale specifico.                                   |
| [**NetGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo)   | Imposta informazioni generali su un gruppo globale.                                    |
| [**NetGroupSetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetusers) | Assegna membri a un nuovo gruppo globale. sostituisce i membri di un gruppo esistente. |



 

## <a name="local-group-functions"></a>Funzioni del gruppo locale



| Funzione                                                   | Descrizione                                                             |
|------------------------------------------------------------|-------------------------------------------------------------------------|
| [**NetLocalGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupadd)               | Crea un gruppo locale.                                                  |
| [**NetLocalGroupAddMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupaddmembers) | Aggiunge uno o più utenti o gruppi globali a un gruppo locale esistente.     |
| [**NetLocalGroupDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdel)               | Elimina un gruppo locale, rimuovendo tutti i membri esistenti dal gruppo.    |
| [**NetLocalGroupDelMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdelmembers) | Rimuove uno o più membri da un gruppo locale esistente.               |
| [**NetLocalGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupenum)             | Restituisce informazioni su ogni account del gruppo locale in un server.         |
| [**NetLocalGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetinfo)       | Restituisce informazioni su un determinato account del gruppo locale in un server. |
| [**NetLocalGroupGetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetmembers) | Elenca tutti i membri di un gruppo locale specificato.                           |
| [**NetLocalGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetinfo)       | Imposta informazioni generali su un gruppo locale.                           |
| [**NetLocalGroupSetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetmembers) | Assegna membri a un gruppo locale.                                       |



 

## <a name="message-functions"></a>Funzioni di messaggio



| Funzione                                               | Descrizione                                                                     |
|--------------------------------------------------------|---------------------------------------------------------------------------------|
| [**NetMessageBufferSend**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagebuffersend)   | Invia un messaggio a un alias di messaggio registrato.                                  |
| [**NetMessageNameAdd**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameadd)         | Registra un alias del messaggio nella tabella del nome del messaggio.                            |
| [**NetMessageNameDel**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenamedel)         | Elimina un alias del messaggio dalla tabella del nome del messaggio.                            |
| [**NetMessageNameEnum**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameenum)       | Elenca tutti gli alias dei messaggi archiviati nella tabella dei nomi dei messaggi.                 |
| [**NetMessageNameGetInfo**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenamegetinfo) | Restituisce informazioni su un alias di messaggio specifico nella tabella del nome del messaggio. |



 

## <a name="netfile-functions"></a>Funzioni NetFile



| Funzione                                | Descrizione                                                          |
|-----------------------------------------|----------------------------------------------------------------------|
| [**NetFileClose**](/windows/desktop/api/lmshare/nf-lmshare-netfileclose)     | Forza la chiusura di una risorsa.                                          |
| [**NetFileEnum**](/windows/desktop/api/lmshare/nf-lmshare-netfileenum)       | Restituisce informazioni sui file aperti in un server.                    |
| [**NetFileGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo) | Restituisce informazioni su una particolare apertura di una risorsa server. |



 

## <a name="remote-utility-functions"></a>Funzioni di utilità remota



| Funzione                                                       | Descrizione                                                                             |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**NetRemoteComputerSupports**](/windows/desktop/api/Lmremutl/nf-lmremutl-netremotecomputersupports) | Esegue una query sul redirector per recuperare le funzionalità facoltative supportate da un sistema remoto. |
| [**NetRemoteTOD**](/windows/desktop/api/Lmremutl/nf-lmremutl-netremotetod)                           | Consente alle applicazioni di accedere alle informazioni relative all'ora del giorno in un server remoto.          |



 

## <a name="schedule-functions"></a>Funzioni di pianificazione



| Funzione                                                                     | Descrizione                                                      |
|------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**NetScheduleJobAdd**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobadd)                               | Invia un processo da eseguire in una data e un'ora future specificate.        |
| [**NetScheduleJobDel**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobdel)                               | Annulla un intervallo di processi accodati per l'esecuzione in un computer.             |
| [**NetScheduleJobEnum**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobenum)                             | Elenca i processi accodati in un computer specificato.                   |
| [**NetScheduleJobGetInfo**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobgetinfo)                       | Restituisce informazioni su un processo specifico accodato in un computer. |
| [**GetNetScheduleAccountInformation**](/windows/desktop/api/AtAcct/nf-atacct-getnetscheduleaccountinformation) | Recupera il nome dell'account del servizio AT.                           |
| [**SetNetScheduleAccountInformation**](/windows/desktop/api/AtAcct/nf-atacct-setnetscheduleaccountinformation) | Imposta il nome e la password dell'account del servizio AT.                   |



 

## <a name="server-functions"></a>Funzioni server



| Funzione                                       | Descrizione                                                                        |
|------------------------------------------------|------------------------------------------------------------------------------------|
| [**NetServerDiskEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverdiskenum) | Restituisce un elenco di unità disco locali in un server.                                   |
| [**NetServerEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverenum)         | Elenca tutti i server visibili di un determinato tipo (o tipi) nel dominio specificato. |
| [**NetServerGetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netservergetinfo)   | Restituisce informazioni di configurazione su un server specificato.                        |
| [**NetServerSetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netserversetinfo)   | Imposta i parametri operativi per un server.                                        |



 

## <a name="server-and-workstation-transport-functions"></a>Funzioni di trasporto server e workstation



| Funzione                                                     | Descrizione                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetServerComputerNameAdd**](/windows/desktop/api/Lmserver/nf-lmserver-netservercomputernameadd) | Associa un nome di server emulato a ognuno dei protocolli di trasporto in cui è attivo un server. Combina la funzionalità della funzione [**NetServerTransportEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportenum) e della [**funzione NetServerTransportAddEx.**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportaddex)                                            |
| [**NetServerComputerNameDel**](/windows/desktop/api/Lmserver/nf-lmserver-netservercomputernamedel) | Disconnette ogni protocollo di trasporto di rete da un nome di server emulato impostato da una chiamata precedente alla **funzione NetServerComputerNameAdd.**                                                                                                                                                                               |
| [**NetServerTransportAdd**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportadd)       | Associa il server specificato al protocollo di trasporto. Questa funzione supporta solo il livello di [**informazioni SERVER TRANSPORT INFO \_ \_ \_ 0.**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_0)                                                                                                                                                |
| [**NetServerTransportAddEx**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportaddex)   | Associa il server specificato al protocollo di trasporto. Questa funzione estesa supporta i livelli di informazioni [**SERVER \_ TRANSPORT INFO \_ \_ 1**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_1), [**SERVER TRANSPORT INFO \_ \_ \_ 2**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_2)e [**SERVER TRANSPORT INFO \_ \_ \_ 3.**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_3) |
| [**NetServerTransportDel**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportdel)       | Disconnette il protocollo di trasporto dal server.                                                                                                                                                                                                                                                                         |
| [**NetServerTransportEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportenum)     | Enumera i protocolli di trasporto gestiti dal server.                                                                                                                                                                                                                                                                   |
| [**NetWkstaTransportEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstatransportenum)       | Elenca i protocolli di trasporto gestiti dal redirector.                                                                                                                                                                                                                                                           |



 

## <a name="use-functions"></a>Usare le funzioni



| Funzione                               | Descrizione                                                                               |
|----------------------------------------|-------------------------------------------------------------------------------------------|
| [**NetUseAdd**](/windows/desktop/api/Lmuse/nf-lmuse-netuseadd)         | Crea una connessione tra un computer locale e un server.                               |
| [**NetUseDel**](/windows/desktop/api/Lmuse/nf-lmuse-netusedel)         | Termina una connessione a una risorsa condivisa.                                                   |
| [**NetUseEnum**](/windows/desktop/api/Lmuse/nf-lmuse-netuseenum)       | Elenca tutte le connessioni correnti tra il computer locale e le risorse nei server remoti. |
| [**NetUseGetInfo**](/windows/desktop/api/Lmuse/nf-lmuse-netusegetinfo) | Restituisce informazioni su una connessione a una risorsa condivisa.                              |



 

## <a name="user-functions"></a>Funzioni utente



| Funzione                                               | Descrizione                                                         |
|--------------------------------------------------------|---------------------------------------------------------------------|
| [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd)                       | Aggiunge un account utente e assegna una password e un livello di privilegio.     |
| [**NetUserChangePassword**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserchangepassword) | Modifica la password di un utente per un dominio o un server di rete specificato. |
| [**NetUserDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel)                       | Elimina un account utente dal server.                             |
| [**NetUserEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum)                     | Elenca tutti gli account utente in un server.                                |
| [**NetUserGetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups)           | Restituisce un elenco di nomi di gruppi globali a cui appartiene un utente.       |
| [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo)               | Restituisce informazioni su un determinato account utente in un server.    |
| [**NetUserGetLocalGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups) | Restituisce un elenco di nomi di gruppi locali a cui appartiene un utente.        |
| [**NetUserSetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetgroups)           | Imposta le appartenenze a gruppi globali per un account utente specificato.         |
| [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo)               | Imposta la password e altri elementi di un account utente.             |



 

## <a name="user-modals-functions"></a>Funzioni modali utente



| Funzione                                     | Descrizione                                                                                                                                                                                             |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetUserModalsGet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget) | Restituisce informazioni globali per tutti gli utenti e i gruppi globali nel database di sicurezza, ovvero il database di gestione degli account di sicurezza (SAM) o, nel caso dei controller di dominio, Active Directory. |
| [**NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset) | Imposta le informazioni globali per tutti gli utenti e i gruppi globali nel database di sicurezza.                                                                                                                       |



 

## <a name="validation-functions"></a>Funzioni di convalida



| Funzione                                                               | Descrizione                                                                                                                                                                                                                     |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetValidatePasswordPolicyFree**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicyfree) | Libera la memoria allocata dalla [**funzione NetValidatePasswordPolicy**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicy) per il *parametro OutputArg,*                                                                                      |
| [**NetValidatePasswordPolicy**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicy)         | Consente a un'applicazione di verificare la conformità delle password rispetto a un database di account fornito dall'applicazione e verificare che le password soddisfino i requisiti di complessità, aging, lunghezza minima e riutilizzo della cronologia di un criterio password. |



 

## <a name="workstation-and-workstation-user-functions"></a>Funzioni utente per workstation e workstation



| Funzione                                           | Descrizione                                                                         |
|----------------------------------------------------|-------------------------------------------------------------------------------------|
| [**NetWkstaGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo)         | Restituisce informazioni sugli elementi di configurazione per una workstation.             |
| [**NetWkstaSetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstasetinfo)         | Configura una workstation.                                                           |
| [**NetWkstaUserEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)       | Elenca le informazioni su tutti gli utenti attualmente connessi alla workstation.           |
| [**NetWkstaUserGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstausergetinfo) | Restituisce informazioni su un utente attualmente connesso.                             |
| [**NetWkstaUserSetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstausersetinfo) | Imposta le informazioni specifiche dell'utente per gli elementi di configurazione di una workstation. |



 

## <a name="obsolete-functions"></a>Funzioni obsolete

-   [**NetAccessAggiungi**](/windows/desktop/api/lmaccess/nf-lmaccess-netaccessadd)
-   [**NetAccessCheck**](/previous-versions/windows/desktop/legacy/aa370291(v=vs.85))
-   [**NetAccessDel**](/windows/desktop/api/lmaccess/nf-lmaccess-netaccessdel)
-   [**NetAccessEnum**](/windows/desktop/api/lmaccess/nf-lmaccess-netaccessenum)
-   [**NetAccessGetInfo**](/windows/desktop/api/lmaccess/nf-lmaccess-netaccessgetinfo)
-   [**NetAccessGetUserPerms**](/windows/desktop/api/lmaccess/nf-lmaccess-netaccessgetuserperms)
-   [**NetAccessSetInfo**](/windows/desktop/api/lmaccess/nf-lmaccess-netaccesssetinfo)
-   [**NetAuditClear**](netauditclear.md)
-   [**NetAuditRead**](netauditread.md)
-   [**NetAuditWrite**](netauditwrite.md)
-   [**NetConfigGet**](netconfigget.md)
-   [**NetConfigGetAll**](netconfiggetall.md)
-   [**NetConfigSet**](netconfigset.md)
-   [**NetErrorLogClear**](neterrorlogclear.md)
-   [**NetErrorLogRead**](neterrorlogread.md)
-   [**NetErrorLogWrite**](neterrorlogwrite.md)
-   [**NetLocalGroupAddMember**](/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupaddmember)
-   [**NetLocalGroupDelMember**](/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupdelmember)
-   [**NetServiceControl**](netservicecontrol.md)
-   [**NetServiceEnum**](netserviceenum.md)
-   [**NetServiceGetInfo**](netservicegetinfo.md)
-   [**NetServiceInstall**](netserviceinstall.md)
-   [**NetWkstaTransportAdd**](/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportadd)
-   [**NetWkstaTransportDel**](/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportdel)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Funzioni di rete](/windows/desktop/WNet/windows-networking-functions)
</dt> </dl>

 

 