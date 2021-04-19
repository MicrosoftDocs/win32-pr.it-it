---
description: Il modello di sicurezza di Windows consente di controllare l'accesso agli oggetti servizio e gestione controllo servizi.
ms.assetid: 23d1c382-6ba4-49e2-8039-c2a91471076c
title: Sicurezza del servizio e diritti di accesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7677b8a9f7a5e1fadf8231999d266a9474fb731
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317679"
---
# <a name="service-security-and-access-rights"></a>Sicurezza del servizio e diritti di accesso

Il modello di sicurezza di Windows consente di controllare l'accesso agli oggetti servizio e gestione controllo servizi. Le sezioni seguenti forniscono informazioni dettagliate:

-   [Diritti di accesso per Gestione controllo servizi](#access-rights-for-the-service-control-manager)
-   [Diritti di accesso per un servizio](#access-rights-for-a-service)

## <a name="access-rights-for-the-service-control-manager"></a>Diritti di accesso per Gestione controllo servizi

Di seguito sono riportati i diritti di accesso specifici per SCM.



| Diritto di accesso                                   | Descrizione                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SC \_ GESTIONE \_ tutti gli \_ accessi** (0xF003F)         | Include **\_ i diritti standard \_ necessari**, oltre a tutti i diritti di accesso in questa tabella.                                                                                                                                                                                                                                                                                 |
| **SC \_ GESTIONE \_ creazione \_ servizio** (0x0002)      | Obbligatorio per chiamare la funzione [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) per creare un oggetto servizio e aggiungerlo al database.                                                                                                                                                                                                                                              |
| **SC \_ GESTIONE \_ connessione** (0x0001)              | Obbligatorio per connettersi a gestione controllo servizi.                                                                                                                                                                                                                                                                                                                      |
| **SC \_ GESTIONE \_ enumerazione \_ servizio** (0x0004)   | Obbligatorio per chiamare la funzione [**EnumServicesStatus**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusa) o [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) per elencare i servizi presenti nel database.<br/> Obbligatorio per chiamare la funzione [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea) per ricevere una notifica quando viene creato o eliminato un servizio.<br/> |
| **SC \_ \_Blocco gestione** (0x0008)                 | Obbligatorio per chiamare la funzione [**LockServiceDatabase**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase) per acquisire un blocco sul database.                                                                                                                                                                                                                                                      |
| **SC \_ GESTIONE \_ modifica \_ \_ configurazione di avvio** (0x0020) | Obbligatorio per chiamare la funzione [**NotifyBootConfigStatus**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus) .                                                                                                                                                                                                                                                                                  |
| **SC \_ \_Stato di \_ blocco \_ della query di gestione** (0x0010)  | Obbligatorio per chiamare la funzione [**QueryServiceLockStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) per recuperare le informazioni sullo stato del blocco per il database.                                                                                                                                                                                                                         |



 

Di seguito sono riportati i [diritti di accesso generici](/windows/desktop/SecAuthZ/generic-access-rights) per SCM.



<table>
<thead>
<tr class="header">
<th>Diritto di accesso</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>GENERIC_READ</strong></td>
<td><dl> <strong>STANDARD_RIGHTS_READ</strong><br />
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong><br />
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong><br />
</dl></td>
</tr>
<tr class="even">
<td><strong>GENERIC_WRITE</strong></td>
<td><dl> <strong>STANDARD_RIGHTS_WRITE</strong><br />
<strong>SC_MANAGER_CREATE_SERVICE</strong><br />
<strong>SC_MANAGER_MODIFY_BOOT_CONFIG</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td><strong>GENERIC_EXECUTE</strong></td>
<td><dl> <strong>STANDARD_RIGHTS_EXECUTE</strong><br />
<strong>SC_MANAGER_CONNECT</strong><br />
<strong>SC_MANAGER_LOCK</strong><br />
</dl></td>
</tr>
<tr class="even">
<td><strong>GENERIC_ALL</strong></td>
<td><dl> <strong>SC_MANAGER_ALL_ACCESS</strong><br />
</dl></td>
</tr>
</tbody>
</table>



 

Un processo con i diritti di accesso corretti può aprire un handle per SCM che può essere utilizzato nelle funzioni [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea), [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa)e [**QueryServiceLockStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) . Solo i processi con privilegi di amministratore sono in grado di aprire gli handle per SCM che possono essere usati dalle funzioni [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) e [**LockServiceDatabase**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase) .

Il sistema crea il descrittore di sicurezza per SCM. Per ottenere o impostare il descrittore di sicurezza per SCM, utilizzare le funzioni [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) e [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) con un handle per l'oggetto SCManager.

**Windows Server 2003 e Windows XP:** A differenza della maggior parte degli altri oggetti a protezione diretta, il descrittore di sicurezza per SCM non può essere modificato. Questo comportamento è stato modificato a partire da Windows Server 2003 con Service Pack 1 (SP1).

Vengono concessi i seguenti diritti di accesso.



<table>
<thead>
<tr class="header">
<th>Account</th>
<th>Diritti di accesso</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Utenti con autenticazione remota</td>
<td><dl> <strong>SC_MANAGER_CONNECT</strong><br />
</dl></td>
</tr>
<tr class="even">
<td>Utenti autenticati locali (inclusi LocalService e NetworkService)</td>
<td><dl> <strong>SC_MANAGER_CONNECT</strong><br />
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong><br />
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong><br />
<strong>STANDARD_RIGHTS_READ</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td>LocalSystem</td>
<td><dl> <strong>SC_MANAGER_CONNECT</strong><br />
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong><br />
<strong>SC_MANAGER_MODIFY_BOOT_CONFIG</strong><br />
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong><br />
<strong>STANDARD_RIGHTS_READ</strong><br />
</dl></td>
</tr>
<tr class="even">
<td>Administrators</td>
<td><dl> <strong>SC_MANAGER_ALL_ACCESS</strong><br />
</dl></td>
</tr>
</tbody>
</table>



 

Si noti che gli utenti remoti autenticati in rete ma non connessi in modo interattivo possono connettersi a SCM senza eseguire operazioni che richiedono altri diritti di accesso. Per eseguire queste operazioni, è necessario che l'utente sia connesso in modo interattivo o che il servizio utilizzi uno degli account del servizio.

**Windows Server 2003 e Windows XP:** Agli utenti con autenticazione remota viene concesso il servizio **SC \_ Manager \_ Connect**, **SC \_ Manager \_ enumerate \_ Service**, **SC \_ Manager \_ query \_ lock \_ status** e Rights **\_ \_ Read** Rights Access Rights. Questi diritti di accesso sono limitati come descritto nella tabella precedente a partire da Windows Server 2003 con SP1

Quando un processo usa la funzione [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) per aprire un handle per un database di servizi installati, può richiedere i diritti di accesso. Il sistema esegue un controllo di sicurezza rispetto al descrittore di sicurezza per SCM prima di concedere i diritti di accesso richiesti.

## <a name="access-rights-for-a-service"></a>Diritti di accesso per un servizio

Di seguito sono riportati i diritti di accesso specifici per un servizio.



| Diritto di accesso                                | Descrizione                                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Servizio \_ di Tutti gli \_ accessi** (0xF01FF)          | Include **\_ i diritti standard \_ necessari** , oltre a tutti i diritti di accesso in questa tabella.                                                                                                                                                                                                                                                                                              |
| **Servizio \_ di MODIFICA \_ configurazione** (0x0002)        | Obbligatorio per chiamare la funzione [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) o [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) per modificare la configurazione del servizio. Poiché in questo modo il chiamante concede il diritto di modificare il file eseguibile eseguito dal sistema, deve essere concesso solo agli amministratori.                                                              |
| **Servizio \_ di ENUMERA \_ dipendenti** (0x0008) | Obbligatorio per chiamare la funzione [**EnumDependentServices**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa) per enumerare tutti i servizi che dipendono dal servizio.                                                                                                                                                                                                                                         |
| **Servizio \_ di INTERROGA** (0x0080)           | Obbligatorio per chiamare la funzione [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) per chiedere al servizio di segnalare immediatamente lo stato.                                                                                                                                                                                                                                                          |
| **Servizio \_ di SOSPENDi \_ continua** (0x0040)       | Obbligatorio per chiamare la funzione [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) per sospendere o continuare il servizio.                                                                                                                                                                                                                                                                             |
| **Servizio \_ di \_Configurazione query** (0x0001)         | Obbligatorio per chiamare le funzioni [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) e [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) per eseguire una query sulla configurazione del servizio.                                                                                                                                                                                                           |
| **Servizio \_ di \_Stato query** (0x0004)         | Obbligatorio per chiamare la funzione [**QueryServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatus) o [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) per chiedere al gestore di controllo del servizio lo stato del servizio.<br/> Obbligatorio per chiamare la funzione [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea) per ricevere una notifica quando viene modificato lo stato di un servizio.<br/> |
| **Servizio \_ di AVVIO** (0x0010)                 | Obbligatorio per chiamare la funzione [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) per avviare il servizio.                                                                                                                                                                                                                                                                                             |
| **Servizio \_ di ARRESTA** (0x0020)                  | Obbligatorio per chiamare la funzione [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) per arrestare il servizio.                                                                                                                                                                                                                                                                                          |
| **Servizio \_ di \_ \_ Controllo definito dall'utente**(0x0100) | Obbligatorio per chiamare la funzione [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) per specificare un codice di controllo definito dall'utente.                                                                                                                                                                                                                                                                       |



 

Di seguito sono riportati i [diritti di accesso standard](/windows/desktop/SecAuthZ/standard-access-rights) per un servizio.



| Diritto di accesso                 | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ACCESSO \_ alla \_ sicurezza del sistema** | Obbligatorio per chiamare la funzione [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) o [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) per accedere all'elenco SACL. Il modo corretto per ottenere questo accesso consiste nell'abilitare il [**privilegio**](/windows/desktop/SecAuthZ/privileges) di **\_ sicurezza del \_ nome se** nel token di accesso corrente del chiamante, aprire l'handle per accedere alla **\_ \_ sicurezza del sistema** e quindi disabilitare il privilegio. |
| **Elimina**   (0x10000)       | Obbligatorio per chiamare la funzione [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) per eliminare il servizio.                                                                                                                                                                                                                                                                                                                                                  |
| **Leggi \_ CONTROLLO**  (0x20000)    | Obbligatorio per chiamare la funzione [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) per eseguire una query sul descrittore di sicurezza dell'oggetto servizio.                                                                                                                                                                                                                                                                                  |
| **Scrivi \_ Applicazione livello dati**  (0x40000)    | Obbligatorio per chiamare la funzione [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) per modificare il membro **DACL** del descrittore di sicurezza dell'oggetto servizio.                                                                                                                                                                                                                                                                   |
| **Scrivi \_ PROPRIETARIO** (0x80000)   | Obbligatorio per chiamare la funzione [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) per modificare i membri del **proprietario** e del **gruppo** del descrittore di sicurezza dell'oggetto servizio.                                                                                                                                                                                                                                                   |



 

Di seguito sono riportati i [diritti di accesso generici](/windows/desktop/SecAuthZ/generic-access-rights) per un servizio.



<table>
<thead>
<tr class="header">
<th>Diritto di accesso</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>GENERIC_READ</strong></td>
<td><dl> <strong>STANDARD_RIGHTS_READ</strong><br />
<strong>SERVICE_QUERY_CONFIG</strong><br />
<strong>SERVICE_QUERY_STATUS</strong><br />
<strong>SERVICE_INTERROGATE</strong><br />
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong><br />
</dl></td>
</tr>
<tr class="even">
<td><strong>GENERIC_WRITE</strong></td>
<td><dl> <strong>STANDARD_RIGHTS_WRITE</strong><br />
<strong>SERVICE_CHANGE_CONFIG</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td><strong>GENERIC_EXECUTE</strong></td>
<td><dl> <strong>STANDARD_RIGHTS_EXECUTE</strong><br />
<strong>SERVICE_START</strong><br />
<strong>SERVICE_STOP</strong><br />
<strong>SERVICE_PAUSE_CONTINUE</strong><br />
<strong>SERVICE_USER_DEFINED_CONTROL</strong><br />
</dl></td>
</tr>
</tbody>
</table>



 

Il gestore SCM Crea il descrittore di sicurezza di un oggetto servizio quando il servizio viene installato tramite la funzione [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) . Il descrittore di sicurezza predefinito di un oggetto servizio concede il seguente accesso.



<table>
<thead>
<tr class="header">
<th>Account</th>
<th>Diritti di accesso</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Utenti con autenticazione remota</td>
<td>Non concessa per impostazione predefinita. <strong>Windows Server 2003 con SP1: SERVICE_USER_DEFINED_CONTROL</strong><br/> <strong>Windows Server 2003 e Windows XP:</strong> I diritti di accesso per gli utenti con autenticazione remota sono identici a quelli degli utenti autenticati locali.<br/></td>
</tr>
<tr class="even">
<td>Utenti autenticati locali (inclusi LocalService e NetworkService)</td>
<td><dl> <strong>READ_CONTROL</strong><br />
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong><br />
<strong>SERVICE_INTERROGATE</strong><br />
<strong>SERVICE_QUERY_CONFIG</strong><br />
<strong>SERVICE_QUERY_STATUS</strong><br />
<strong>SERVICE_USER_DEFINED_CONTROL</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td>LocalSystem</td>
<td><dl> <strong>READ_CONTROL</strong><br />
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong><br />
<strong>SERVICE_INTERROGATE</strong><br />
<strong>SERVICE_PAUSE_CONTINUE</strong><br />
<strong>SERVICE_QUERY_CONFIG</strong><br />
<strong>SERVICE_QUERY_STATUS</strong><br />
<strong>SERVICE_START</strong><br />
<strong>SERVICE_STOP</strong><br />
<strong>SERVICE_USER_DEFINED_CONTROL</strong><br />
</dl></td>
</tr>
<tr class="even">
<td>Administrators</td>
<td><dl> <strong>DELETE</strong><br />
<strong>READ_CONTROL</strong><br />
<strong>SERVICE_ALL_ACCESS</strong><br />
<strong>WRITE_DAC</strong><br />
<strong>WRITE_OWNER</strong><br />
</dl></td>
</tr>
</tbody>
</table>



 

Per eseguire qualsiasi operazione, è necessario che l'utente sia connesso in modo interattivo o che il servizio utilizzi uno degli account del servizio.

Per ottenere o impostare il descrittore di sicurezza per un oggetto servizio, usare le funzioni [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) e [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) . Per ulteriori informazioni, vedere [modifica dell'elenco DACL per un servizio](modifying-the-dacl-for-a-service.md).

Quando un processo utilizza la funzione [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) , il sistema controlla i diritti di accesso richiesti rispetto al descrittore di sicurezza per l'oggetto servizio.

La concessione di determinati diritti di accesso a utenti non attendibili, ad esempio la **\_ \_ configurazione delle modifiche dei servizi** o l' **\_ arresto del servizio**, può consentire loro di interferire con l'esecuzione del servizio e possibilmente consentire l'esecuzione di applicazioni con l'account LocalSystem.

Quando viene chiamata la [**funzione EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) , se il chiamante non dispone del diritto di accesso **\_ \_ stato query del servizio** a un servizio, il servizio viene omesso automaticamente dall'elenco di servizi restituiti al client.

 

