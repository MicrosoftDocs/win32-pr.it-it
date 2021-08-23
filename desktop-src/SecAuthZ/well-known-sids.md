---
description: Gli ID di sicurezza (SID) noti identificano i gruppi generici e gli utenti generici.
ms.assetid: eb2f95c4-9465-409b-b76c-9ccae1d05eda
title: SID noti
ms.topic: article
ms.date: 03/04/2020
ms.custom: 19H1
ms.openlocfilehash: 17fe8827100f9e3684ac0219fc83f183581017cc5738af5933b7bb7cc4ea3ff8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119623091"
---
# <a name="well-known-sids"></a>SID noti

Gli ID di [*sicurezza (SID)*](/windows/desktop/SecGloss/s-gly) noti identificano i gruppi generici e gli utenti generici. Ad esempio, sono disponibili SID noti per identificare i gruppi e gli utenti seguenti:

-   Everyone o World, ovvero un gruppo che include tutti gli utenti.
-   CREATOR \_ OWNER, usato come segnaposto in una ACE ereditabile. Quando la ACE viene ereditata, il sistema sostituisce il SID CREATOR OWNER con il \_ SID dell'autore dell'oggetto.
-   Gruppo Administrators per il dominio predefinito nel computer locale.

Sono disponibili [*SID*](/windows/desktop/SecGloss/u-gly)noti universali, significativi in tutti i sistemi sicuri che usano questo modello di sicurezza, inclusi i sistemi operativi diversi da Windows. Inoltre, esistono SID noti che sono significativi solo nei sistemi Windows sistema.

L Windows API definisce un set di costanti per [](/windows/desktop/SecGloss/r-gly) i valori noti dell'autorità dell'identificatore e dell'identificatore relativo (RID). È possibile usare queste costanti per creare SID noti. L'esempio seguente combina le costanti SECURITY WORLD SID AUTHORITY e SECURITY WORLD RID per mostrare il SID noto universale per il gruppo speciale che rappresenta tutti gli utenti \_ \_ \_ \_ \_ (Everyone o World):

S-1-1-0

In questo esempio viene utilizzata la notazione di stringa per i SID in cui S identifica la stringa come SID, il primo 1 è il livello di revisione del SID e le due cifre rimanenti sono le costanti SECURITY WORLD SID AUTHORITY e \_ SECURITY \_ WORLD \_ \_ \_ RID.

È possibile usare la [**funzione AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) per compilare un SID combinando un valore dell'autorità identificatore con un massimo di otto valori di sottoautorità. Ad esempio, per determinare se l'utente connesso è membro di un particolare gruppo noto, chiamare **AllocateAndInitializeSid** per compilare un SID per il gruppo noto e usare la funzione [**EqualSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-equalsid) per confrontare tale SID con i SID di gruppo nel token di accesso dell'utente. [](/windows/desktop/SecGloss/a-gly) Per un esempio, vedere [Ricerca di un SID in un token di accesso in C++.](searching-for-a-sid-in-an-access-token-in-c--.md) È necessario chiamare la [**funzione FreeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-freesid) per liberare un SID allocato **da AllocateAndInitializeSid**.

Nella parte restante di questa sezione sono contenute tabelle di SID noti e tabelle di costanti di autorità identificatore e sottoautorità che è possibile usare per compilare SID noti.

Di seguito sono riportati [*alcuni SID noti universali.*](/windows/desktop/SecGloss/u-gly)



| SID noto universale    | Valore stringa       | Identifica                                                                                                                                               |
|-----------------------------|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Null SID<br/>         | S-1-0-0<br/> | Gruppo senza membri. Viene spesso usato quando un valore SID non è noto.<br/>                                                                    |
| World<br/>            | S-1-1-0<br/> | Gruppo che include tutti gli utenti.<br/>                                                                                                              |
| Locale<br/>            | S-1-2-0<br/> | Utenti che a log on to [*terminals*](/windows/desktop/SecGloss/t-gly) localmente (fisicamente) connessi al sistema.<br/> |
| ID proprietario autore<br/> | S-1-3-0<br/> | Identificatore di sicurezza da sostituire con l'ID di sicurezza dell'utente che ha creato un nuovo oggetto. Questo SID viene usato nelle ACE ereditabili.<br/>   |
| ID gruppo autori<br/> | S-1-3-1<br/> | Identificatore di sicurezza da sostituire con il SID del gruppo primario dell'utente che ha creato un nuovo oggetto. Usare questo SID in ACE ereditabili.<br/>         |



 

Nella tabella seguente sono elencate le costanti di autorità dell'identificatore predefinite. I primi quattro valori vengono usati con SID noti universali. L'ultimo valore viene usato con Windows SID noti.



| Autorità identificatore                         | Valore        | Valore stringa |
|----------------------------------------------|--------------|-------------------|
| SECURITY \_ NULL \_ SID \_ AUTHORITY<br/>    | 0<br/> | S-1-0<br/>  |
| SECURITY \_ WORLD \_ SID \_ AUTHORITY<br/>   | 1<br/> | S-1-1<br/>  |
| AUTORITÀ \_ \_ SID LOCALE DI \_ SICUREZZA<br/>   | 2<br/> | S-1-2<br/>  |
| SECURITY \_ CREATOR \_ SID \_ AUTHORITY<br/> | 3<br/> | S-1-3<br/>  |
| AUTORITÀ \_ NT DI \_ SICUREZZA<br/>           | 5<br/> | S-1-5<br/>  |



 

I valori [*RID*](/windows/desktop/SecGloss/r-gly) seguenti vengono usati con [*i SID noti universali*](/windows/desktop/SecGloss/u-gly). La colonna Identificatore autorità mostra il prefisso dell'autorità di identificazione con cui è possibile combinare il RID per creare un SID noto universale.



| Autorità identificatore relativo            | Valore        | Valore stringa |
|------------------------------------------|--------------|----------------------|
| RID \_ NULL \_ DI SICUREZZA<br/>           | 0<br/> | S-1-0<br/>     |
| SECURITY \_ WORLD \_ RID<br/>          | 0<br/> | S-1-1<br/>     |
| RID \_ LOCALE DI \_ SICUREZZA<br/>          | 0<br/> | S-1-2<br/>     |
| RID \_ DI ACCESSO LOCALE DI \_ \_ SICUREZZA<br/>   | 1<br/> | S-1-2<br/>     |
| RID PROPRIETARIO \_ AUTORE \_ \_ SICUREZZA<br/> | 0<br/> | S-1-3<br/>     |
| RID DEL \_ GRUPPO DI AUTORI DI \_ \_ SICUREZZA<br/> | 1<br/> | S-1-3<br/>     |



 

L'autorità identificatore \_ predefinita SECURITY NT AUTHORITY (S-1-5) produce SID non universali, ma significativi solo Windows \_ installazioni. È possibile usare i valori RID seguenti con SECURITY \_ NT AUTHORITY per creare \_ SID noti.



| Costante                                          | Valore stringa               | Identifica                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_RID DI CONNESSIONE REMOTA DI \_ SICUREZZA<br/>                  | S-1-5-1<br/>         | Utenti che a log on to [*terminals*](/windows/desktop/SecGloss/t-gly) using a dial-up modem. Si tratta di un identificatore di gruppo.<br/>                                                                                                                                                                                                                                                                                                                                                                  |
| RID \_ DI RETE DI \_ SICUREZZA<br/>                 | S-1-5-2<br/>         | Utenti che a log on attraverso una rete. Si tratta di un identificatore di gruppo aggiunto al token di un processo quando è stato connesso in una rete. Il tipo di accesso corrispondente è LOGON32 \_ LOGON \_ NETWORK.<br/>                                                                                                                                                                                                                                                                                                                      |
| SICUREZZA \_ BATCH \_ RID<br/>                   | S-1-5-3<br/>         | Utenti che accodno usando una funzionalità di accodamento batch. Si tratta di un identificatore di gruppo aggiunto al token di un processo quando è stato registrato come processo batch. Il tipo di accesso corrispondente è LOGON32 \_ LOGON \_ BATCH.<br/>                                                                                                                                                                                                                                                                                                                 |
| RID \_ INTERATTIVO DI \_ SICUREZZA<br/>             | S-1-5-4<br/>         | Utenti che eseere connessi per operazioni interattive. Si tratta di un identificatore di gruppo aggiunto al token di un processo quando è stato connesso in modo interattivo. Il tipo di accesso corrispondente è LOGON32 \_ LOGON \_ INTERACTIVE.<br/>                                                                                                                                                                                                                                                                                                            |
| RID \_ ID DI ACCESSO DI \_ \_ SICUREZZA<br/>              | S-1-5-5-*X* - *Y*<br/> | Una sessione di accesso. Viene usato per garantire che solo i [*processi*](/windows/desktop/SecGloss/p-gly) in una determinata sessione di accesso possano accedere agli oggetti window-station per tale sessione. I *valori X* e *Y* per questi SID sono diversi per ogni sessione di accesso. Il valore SECURITY \_ LOGON IDS RID COUNT è il numero di RID in questo \_ identificatore \_ \_ (5-*X* - *Y*).<br/>                                                                                                                   |
| RID \_ DEL SERVIZIO DI \_ SICUREZZA<br/>                 | S-1-5-6<br/>         | Account autorizzati ad accedere come servizio. Si tratta di un identificatore di gruppo aggiunto al token di un processo quando è stato registrato come servizio. Il tipo di accesso corrispondente è LOGON32 \_ LOGON \_ SERVICE.<br/>                                                                                                                                                                                                                                                                                                                    |
| RID \_ DI ACCESSO ANONIMO DI \_ \_ SICUREZZA<br/>        | S-1-5-7<br/>         | Accesso anonimo o accesso di sessione Null.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| RID \_ PROXY \_ DI SICUREZZA<br/>                   | S-1-5-8<br/>         | Proxy.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| SICUREZZA \_ ENTERPRISE \_ CONTROLLERS \_ RID<br/> | S-1-5-9<br/>         | Enterprise controller.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| SELF \_ \_ RID DELL'ENTITÀ \_ DI SICUREZZA<br/>         | S-1-5-10<br/>        | L'identificatore di sicurezza PRINCIPAL \_ SELF può essere usato nell'ACL di un oggetto utente o gruppo. Durante un controllo di accesso, il sistema sostituisce il SID con il SID dell'oggetto. Il SID PRINCIPAL SELF è utile per specificare una ACE ereditabile che si applica all'oggetto utente o gruppo che \_ eredita la ACE. Rappresenta l'unico modo per rappresentare il SID di un oggetto creato nel descrittore [*di sicurezza*](/windows/desktop/SecGloss/s-gly) predefinito dello schema.<br/> |
| RID \_ UTENTE CON AUTENTICAZIONE DI \_ \_ SICUREZZA<br/>     | S-1-5-11<br/>        | Utenti autenticati.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| RID \_ CODICE CON RESTRIZIONI DI \_ \_ SICUREZZA<br/>        | S-1-5-12<br/>        | Codice con restrizioni.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| SICUREZZA \_ DI TERMINAL SERVER \_ \_ RID<br/>        | S-1-5-13<br/>        | Servizi terminal. Aggiunta automatica al token di sicurezza di un utente che accede a un server terminal.<br/>                                                                                                                                                                                                                                                                                                                                                                                                            |
| RID \_ DI SISTEMA LOCALE DI \_ \_ SICUREZZA<br/>           | S-1-5-18<br/>        | Account speciale usato dal sistema operativo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| SICUREZZA \_ NT \_ NON \_ UNIVOCA<br/>              | S-1-5-21<br/>        | I SIDS non sono univoci.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| SICUREZZA \_ BUILTIN \_ DOMAIN \_ RID<br/>         | S-1-5-32<br/>        | Dominio di sistema predefinito.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| RID \_ CODICE CON RESTRIZIONI DI SCRITTURA DI \_ \_ \_ SICUREZZA<br/> | S-1-5-33<br/>        | Scrivere codice con restrizioni.<br/> |


 

I RID seguenti sono relativi a ogni dominio.



| RID                                                                | Valore       | Identifica                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GRUPPO \_ DI ACCESSO DCOM DOMAIN ALIAS RID \_ \_ \_ CERTSVC \_ \_<br/>              | 0x0000023E | Gruppo di utenti che possono connettersi alle autorità di certificazione usando Distributed Component Object Model (DCOM).<br/>                                                                                                                          |
| AMMINISTRATORE \_ RID UTENTE DI \_ \_ DOMINIO<br/>                                      | 0x000001F4 | Account utente amministrativo in un dominio.<br/>                                                                                                                                                                                              |
| DOMAIN \_ USER \_ RID \_ GUEST<br/>                                      | 0x000001F5 | Account utente guest in un dominio. Gli utenti che non hanno un account possono accedere automaticamente a questo account.<br/>                                                                                                                            |
| AMMINISTRATORI \_ \_ RID DEL GRUPPO DI \_ DOMINIO<br/>                                    | 0x00000200 | Gruppo degli amministratori di dominio. Questo account esiste solo nei sistemi che eseguono sistemi operativi server.<br/>                                                                                                                                   |
| UTENTI \_ \_ RID DEL GRUPPO DI \_ DOMINIO<br/>                                     | 0x00000201 | Gruppo che contiene tutti gli account utente in un dominio. Tutti gli utenti vengono aggiunti automaticamente a questo gruppo.<br/>                                                                                                                                     |
| GUEST \_ \_ RID DEL GRUPPO DI \_ DOMINIO<br/>                                    | 0x00000202 | Account del gruppo guest in un dominio.<br/>                                                                                                                                                                                                      |
| COMPUTER \_ \_ RID DEL GRUPPO DI \_ DOMINIO<br/>                                 | 0x00000203 | Gruppo di computer del dominio. Tutti i computer nel dominio sono membri di questo gruppo.<br/>                                                                                                                                                       |
| CONTROLLER \_ \_ RID DEL GRUPPO DI \_ DOMINIO<br/>                               | 0x00000204 | Gruppo dei controller di dominio. Tutti i controller di dominio nel dominio sono membri di questo gruppo.<br/>                                                                                                                                                           |
| DOMAIN \_ GROUP \_ RID \_ CERT \_ ADMINS<br/>                              | 0x00000205 | Gruppo di autori di certificati. I computer che eseguono Servizi certificati sono membri di questo gruppo.<br/>                                                                                                                                      |
| CONTROLLER \_ DI DOMINIO RID ENTERPRISE DI SOLA LETTURA DEL GRUPPO DI \_ \_ \_ \_ \_ DOMINIO<br/> | 0x000001F2 | Gruppo di controller di dominio aziendali di sola lettura.<br/>                                                                                                                                                                                     |
| AMMINISTRATORI \_ DELLO SCHEMA RID DEL GRUPPO DI \_ \_ \_ DOMINIO<br/>                            | 0x00000206 | Gruppo di amministratori dello schema. I membri di questo gruppo possono modificare lo schema di Active Directory.<br/>                                                                                                                                           |
| DOMAIN \_ GROUP \_ RID \_ ENTERPRISE \_ ADMINS<br/>                        | 0x00000207 | Gruppo di amministratori dell'organizzazione. I membri di questo gruppo hanno accesso completo a tutti i domini nella foresta Active Directory. Enterprise amministratori sono responsabili delle operazioni a livello di foresta, ad esempio l'aggiunta o la rimozione di nuovi domini.<br/> |
| AMMINISTRATORI \_ DI CRITERI RID DI GRUPPO DI \_ \_ \_ DOMINIO<br/>                            | 0x00000208 | Gruppo di amministratori dei criteri.<br/>                                                                                                                                                                                                         |
| CONTROLLER DI SOLA LETTURA RID DEL GRUPPO \_ \_ DI \_ \_ DOMINIO<br/>                     | 0x00000209 | Gruppo di controller di dominio di sola lettura.<br/>                                                                                                                                                                                                |                                             
| CONTROLLER \_ \_ CLONABILI RID DEL GRUPPO \_ DI \_ DOMINIO<br />                   | 0x0000020A | Gruppo di controller di dominio clonabili.<br/>                                                                                                                                                                                                |
| GRUPPO \_ DI DOMINIO RID \_ \_ CDC \_ RISERVATO<br />                            | 0x0000020C | Gruppo CDC riservato.<br/>                                                                                                                                                                                                                   |
| UTENTI \_ PROTETTI CON RID RID DEL GRUPPO DI \_ \_ \_ DOMINIO<br />                         | 0x0000020D | Gruppo di utenti protetti.</br>                                                                                                                                                                                                                |
| AMMINISTRATORI \_ DELLE CHIAVI RID DEL GRUPPO DI \_ \_ \_ DOMINIO<br />                              | 0x0000020E | Gruppo di amministratori delle chiavi.<br/>                                                                                                                                                                                                                     |
| DOMAIN \_ GROUP \_ RID \_ ENTERPRISE \_ KEY \_ ADMINS<br />                  | 0x0000020F | Gruppo di amministratori delle chiavi aziendali</br>                                                                                                                                                                                                           |



 

I RID seguenti vengono usati per specificare il livello di integrità obbligatorio.



| RID                                                     | Valore                                               | Identifica                        |
|---------------------------------------------------------|-----------------------------------------------------|-----------------------------------|
| RID \_ \_ NON ATTENDIBILE OBBLIGATORIO PER LA \_ SICUREZZA<br/>          | 0x00000000<br/>                               | Attendibile.<br/>             |
| RID \_ MINIMO \_ OBBLIGATORIO PER LA \_ SICUREZZA<br/>                | 0x00001000<br/>                               | Bassa integrità.<br/>         |
| RID \_ MEDIO OBBLIGATORIO \_ PER LA \_ SICUREZZA<br/>             | 0x00002000<br/>                               | Integrità media.<br/>      |
| SICUREZZA \_ OBBLIGATORIA MEDIA PIÙ \_ \_ \_ RID<br/>       | SECURITY \_ MANDATORY MEDIUM RID + \_ \_ 0x100<br/> | Integrità media elevata.<br/> |
| RID \_ ELEVATO \_ OBBLIGATORIO PER LA \_ SICUREZZA<br/>               | 0X00003000<br/>                               | Integrità elevata.<br/>        |
| RID \_ DI \_ SISTEMA OBBLIGATORIO PER LA \_ SICUREZZA<br/>             | 0x00004000<br/>                               | Integrità del sistema.<br/>      |
| RID \_ DI PROCESSO PROTETTO \_ \_ OBBLIGATORIO PER LA \_ SICUREZZA<br/> | 0x00005000<br/>                               | Processo protetto.<br/>     |



 

La tabella seguente contiene esempi di ID relativi al dominio che è possibile usare per formare SID noti per gruppi locali (alias). Per altre informazioni sui gruppi locali e globali, vedere [Funzioni di gruppo locale](/windows/desktop/NetMgmt/local-group-functions) e Funzioni di [gruppo](/windows/desktop/NetMgmt/group-functions).



| RID                                                              | Valore                 |Valore stringa  | Identifica                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------|-----------------|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DOMAIN \_ ALIAS \_ RID \_ ADMINS<br/>                            | 0x00000220<br/> | S-1-5-32-544<br/> | Gruppo locale usato per l'amministrazione del dominio.<br/>                                                                                                                                                                                                                            |
| UTENTI \_ RID ALIAS DI \_ \_ DOMINIO<br/>                             | 0x00000221<br/> | S-1-5-32-545<br/> | Gruppo locale che rappresenta tutti gli utenti nel dominio.<br/>                                                                                                                                                                                                                          |
| DOMAIN \_ ALIAS \_ RID \_ GUESTS<br/>                            | 0x00000222<br/> | S-1-5-32-546<br/> | Gruppo locale che rappresenta i guest del dominio.<br/>                                                                                                                                                                                                                             |
| ALIAS \_ DI DOMINIO RID POWER \_ \_ \_ USERS<br/>                      | 0x00000223<br/> | S-1-5-32-547<br/> | Gruppo locale usato per rappresentare un utente o un set di utenti che prevedono di considerare un sistema come se fosse il proprio personal computer anziché come workstation per più utenti.<br/>                                                                                                      |
| OPERAZIONI \_ \_ DELL'ACCOUNT RID \_ ALIAS DI \_ DOMINIO<br/>                      | 0x00000224<br/> | S-1-5-32-548<br/> | Gruppo locale che esiste solo nei sistemi che eseguono sistemi operativi server. Questo gruppo locale consente il controllo su account non amministratori.<br/>                                                                                                                                    |
| DOMAIN \_ ALIAS \_ RID \_ SYSTEM \_ OPS<br/>                       | 0x00000225<br/> | S-1-5-32-549<br/> | Gruppo locale che esiste solo nei sistemi che eseguono sistemi operativi server. Questo gruppo locale esegue funzioni amministrative di sistema, senza includere le funzioni di sicurezza. Stabilisce condivisioni di rete, controlla le stampanti, sblocca le workstation ed esegue altre operazioni.<br/> |
| OPS \_ DI STAMPA RID ALIAS DI \_ \_ \_ DOMINIO<br/>                        | 0x00000226<br/> | S-1-5-32-550<br/> | Gruppo locale che esiste solo nei sistemi che eseguono sistemi operativi server. Questo gruppo locale controlla le stampanti e le code di stampa.<br/>                                                                                                                                                |
| OPERAZIONI \_ DI BACKUP RID ALIAS DI \_ \_ \_ DOMINIO<br/>                       | 0x00000227<br/> | S-1-5-32-551<br/> | Gruppo locale utilizzato per controllare l'assegnazione dei privilegi di backup e ripristino dei file.<br/>                                                                                                                                                                                            |
| REPLICATORE \_ \_ RID ALIAS DI \_ DOMINIO<br/>                        | 0x00000228<br/> | S-1-5-32-552<br/> | Gruppo locale responsabile della copia dei database di sicurezza dal controller di dominio primario ai controller di dominio di backup. Questi account vengono usati solo dal sistema.<br/>                                                                                                       |
| SERVER \_ \_ RAS RID ALIAS \_ DI \_ DOMINIO<br/>                      | 0x00000229<br/> | S-1-5-32-553<br/> | Gruppo locale che rappresenta i server RAS e IAS. Questo gruppo consente l'accesso a vari attributi degli oggetti utente.<br/>                                                                                                                                                             |
| DOMINIO \_ ALIAS \_ RID \_ PREW2KCOMPACCESS<br/>                  | 0x0000022A<br/> | S-1-5-32-554<br/> | Gruppo locale esistente solo nei sistemi che eseguono Windows 2000 Server. Per altre informazioni, vedere [Consentire l'accesso anonimo.](allowing-anonymous-access.md)<br/>                                                                                                                    |
| UTENTI \_ DI DESKTOP REMOTO RID ALIAS DI \_ \_ \_ \_ DOMINIO<br/>            | 0x0000022B<br/> | S-1-5-32-555<br/> | Gruppo locale che rappresenta tutti gli utenti desktop remoto.<br/>                                                                                                                                                                                                                         |
| OPERAZIONI \_ DI CONFIGURAZIONE DELLA RETE RID ALIAS DI \_ \_ \_ \_ DOMINIO<br/>       | 0x0000022C<br/> | S-1-5-32-556<br/> | Gruppo locale che rappresenta la configurazione di rete. <br/>                                                                                                                                                                                                                       |
| DOMAIN \_ ALIAS \_ RID \_ INCOMING \_ FOREST \_ TRUST \_ BUILDERS<br/> | 0x0000022D<br/> | S-1-5-32-557<br/> | Gruppo locale che rappresenta tutti gli utenti del trust tra foreste.<br/>                                                                                                                                                                                                                           |
| UTENTI DI \_ MONITORAGGIO RID ALIAS DI \_ \_ \_ DOMINIO<br/>                 | 0x0000022E<br/> | S-1-5-32-558<br/> | Gruppo locale che rappresenta tutti gli utenti monitorati.<br/>                                                                                                                                                                                                                        |
| UTENTI DI \_ REGISTRAZIONE RID ALIAS DI \_ \_ \_ DOMINIO<br/>                    | 0x0000022F<br/> | S-1-5-32-559<br/> | Gruppo locale responsabile della registrazione degli utenti.<br/>                                                                                                                                                                                                                                    |
| ALIAS \_ DI DOMINIO RID \_ \_ AUTHORIZATIONACCESS<br/>               | 0x00000230<br/> | S-1-5-32-560<br/> | Gruppo locale che rappresenta tutti gli accessi autorizzati.<br/>                                                                                                                                                                                                                            |
| SERVER \_ LICENZE DI DOMAIN ALIAS RID \_ \_ TS \_ \_<br/>              | 0x00000231<br/> | S-1-5-32-561<br/> | Gruppo locale che esiste solo nei sistemi che eseguono sistemi operativi server che consentono servizi terminal e accesso remoto.<br/>                                                                                                                                                  |
| UTENTI \_ \_ DCOM RID ALIAS \_ \_ DI DOMINIO<br/>                       | 0x00000232<br/> | S-1-5-32-562<br/> | Gruppo locale che rappresenta gli utenti che possono usare DCOM (Distributed Component Object Model).<br/>                                                                                                                                                                                      |
| DOMAIN \_ ALIAS \_ RID \_ IUSERS<br/>                            | 0X00000238<br/> | S-1-5-32-568<br/> | Gruppo locale che rappresenta gli utenti Internet.<br/>                                                                                                                                                                                                                                   |
| OPERATORI DI \_ CRITTOGRAFIA RID ALIAS DI \_ \_ \_ DOMINIO<br/>                 | 0x00000239<br/> | S-1-5-32-569<br/> | Gruppo locale che rappresenta l'accesso agli operatori di crittografia.<br/>                                                                                                                                                                                                                 |
| GRUPPO \_ DI \_ ENTITÀ MEMORIZZABILI NELLA CACHE DI ALIAS \_ DI \_ \_ DOMINIO<br/>      | 0x0000023B<br/> | S-1-5-32-571<br/> | Gruppo locale che rappresenta le entità che possono essere memorizzate nella cache.<br/>                                                                                                                                                                                                                    |
| GRUPPO \_ DI ENTITÀ NON \_ \_ \_ MEMORIZZABILI NELLA CACHE \_ \_ DI DOMAIN ALIAS RID<br/> | 0x0000023C<br/> | S-1-5-32-572<br/> | Gruppo locale che rappresenta le entità che non possono essere memorizzate nella cache.<br/>                                                                                                                                                                                                                 |
| GRUPPO LETTORI \_ REGISTRO EVENTI RID ALIAS DI \_ \_ \_ \_ \_ DOMINIO<br/>        | 0x0000023D<br/> | S-1-5-32-573<br/> | Gruppo locale che rappresenta i lettori del log eventi.<br/>                                                                                                                                                                                                                                |
| GRUPPO \_ DI ACCESSO DCOM DOMAIN ALIAS RID \_ \_ \_ CERTSVC \_ \_<br/>      | 0x0000023E<br/> | S-1-5-32-574<br/> | Gruppo locale di utenti che possono connettersi alle autorità di certificazione usando Distributed Component Object Model (DCOM).<br/>                                                                                                                                                          |
| SERVER DI ACCESSO REMOTO DI SERVIZI DESKTOP REMOTO DI SERVIZI DESKTOP REMOTO CON \_ RID \_ ALIAS DI \_ \_ \_ \_ DOMINIO<br />     | 0x0000023F<br/> | S-1-5-32-575<br/> | Gruppo locale che rappresenta i server di accesso remoto di Servizi Desktop remoto.<br/> |
| SERVER \_ ENDPOINT DI SERVIZI DESKTOP REMOTO RID ALIAS DI \_ \_ \_ \_ DOMINIO                 | 0x00000240<br/> | S-1-5-32-576<br/> | Gruppo locale che rappresenta i server endpoint.<br/> |
| SERVER DI \_ GESTIONE SERVIZI DESKTOP REMOTO DI RID ALIAS DI \_ \_ \_ \_ DOMINIO               | 0x00000241<br/> | S-1-5-32-577<br/> | Gruppo locale che rappresenta i server di gestione. <br/>|
| DOMAIN \_ ALIAS \_ RID \_ HYPER \_ V \_ ADMINS                       | 0x00000242<br/> | S-1-5-32-578<br/> | Gruppo locale che rappresenta gli amministratori hyper-v <br/>|
| OPS DI \_ ASSISTENZA PER IL CONTROLLO DEGLI \_ \_ \_ ACCESSI CON RID \_ ALIAS \_ DI DOMINIO       | 0x00000243<br/> | S-1-5-32-579<br/> | Gruppo locale che rappresenta l'assistenza per il controllo di accesso OPS.<br/> |
| UTENTI DI \_ GESTIONE REMOTA DI DOMAIN ALIAS \_ RID \_ \_ \_              | 0x00000244<br/> | S-1-5-32-580<br/> | Gruppo locale che rappresenta gli utenti di gestione remota. <br/>|
| \_ACCOUNT PREDEFINITO DI RID ALIAS DI \_ \_ \_ DOMINIO                       | 0x00000245<br/> | S-1-5-32-581<br/> | Gruppo locale che rappresenta l'account predefinito. <br/>|
| DOMAIN \_ ALIAS \_ RID \_ STORAGE \_ REPLICA \_ ADMINS               | 0x00000246<br/> | S-1-5-32-582<br/> | Gruppo locale che rappresenta gli amministratori della replica di archiviazione. <br/>|
| PROPRIETARI \_ DI DISPOSITIVI RID ALIAS DI \_ \_ \_ DOMINIO                            | 0x00000247<br/> | S-1-5-32-583<br/> | Un gruppo locale che rappresenta può creare impostazioni previste per i proprietari dei dispositivi.<br/>|


 

[**L'enumerazione WELL \_ KNOWN \_ SID \_ TYPE**](/windows/desktop/api/Winnt/ne-winnt-well_known_sid_type) definisce l'elenco dei SID di uso comune. Inoltre, il linguaggio SDDL [(Security Descriptor Definition Language)](security-descriptor-definition-language.md) usa stringhe [SID](sid-strings.md) per fare riferimento a SID noti in formato stringa.

 

