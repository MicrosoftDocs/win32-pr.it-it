---
description: Gli identificatori di sicurezza (SID) noti identificano i gruppi e gli utenti generici.
ms.assetid: eb2f95c4-9465-409b-b76c-9ccae1d05eda
title: SID noti
ms.topic: article
ms.date: 03/04/2020
ms.custom: 19H1
ms.openlocfilehash: 1fdde933b3e4f844e63785ff130aaf89204fe0af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315425"
---
# <a name="well-known-sids"></a>SID noti

Gli [*identificatori di sicurezza*](/windows/desktop/SecGloss/s-gly) (SID) noti identificano i gruppi e gli utenti generici. Ad esempio, sono disponibili SID ben noti per identificare i gruppi e gli utenti seguenti:

-   Everyone o World, ovvero un gruppo che include tutti gli utenti.
-   \_Proprietario dell'autore, usato come segnaposto in una voce ACE ereditabile. Quando la voce ACE viene ereditata, il sistema sostituisce il SID del proprietario dell'autore \_ con il SID del creatore dell'oggetto.
-   Il gruppo Administrators per il dominio predefinito nel computer locale.

Ci sono [*SID noti universali*](/windows/desktop/SecGloss/u-gly), che sono significativi in tutti i sistemi protetti che usano questo modello di sicurezza, inclusi i sistemi operativi diversi da Windows. Sono inoltre disponibili SID ben noti che sono significativi solo nei sistemi Windows.

L'API Windows definisce un set di costanti per i valori dell'autorità di certificazione e del RID (identificatore [*relativo*](/windows/desktop/SecGloss/r-gly) ) noti. È possibile utilizzare queste costanti per creare SID noti. L'esempio seguente combina l' \_ autorità SID del mondo di sicurezza e le \_ \_ costanti RID del mondo della sicurezza \_ \_ per visualizzare il SID noto universale per il gruppo speciale che rappresenta tutti gli utenti (Everyone o World):

S-1-1-0

In questo esempio viene utilizzata la notazione stringa per SID in cui S identifica la stringa come SID, il primo è il livello di revisione del SID e le due cifre rimanenti sono l' \_ autorità SID del mondo di sicurezza \_ e le \_ \_ costanti RID del mondo di sicurezza \_ .

È possibile utilizzare la funzione [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) per compilare un SID combinando un valore dell'autorità di identificazione con un massimo di otto valori di sottoautorizzazione. Per determinare, ad esempio, se l'utente connesso è un membro di un particolare gruppo noto, chiamare **AllocateAndInitializeSid** per compilare un SID per il gruppo noto e usare la funzione [**EqualSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-equalsid) per confrontare tale SID con i SID del gruppo nel [*token di accesso*](/windows/desktop/SecGloss/a-gly)dell'utente. Per un esempio, vedere [ricerca di un SID in un token di accesso in C++](searching-for-a-sid-in-an-access-token-in-c--.md). Per liberare un SID allocato da **AllocateAndInitializeSid**, è necessario chiamare la funzione [**FreeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-freesid) .

Nella parte restante di questa sezione sono contenute le tabelle di SID noti e le tabelle delle costanti dell'autorità di identificazione e della sottoautorizzazione che è possibile utilizzare per compilare SID noti.

Di seguito sono riportati alcuni [*SID noti universali*](/windows/desktop/SecGloss/u-gly).



| SID noto universale    | Valore stringa       | Identifica                                                                                                                                               |
|-----------------------------|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| SID NULL<br/>         | S-1-0-0<br/> | Gruppo privo di membri. Questa operazione viene spesso utilizzata quando un valore SID non è noto.<br/>                                                                    |
| World<br/>            | S-1-1-0<br/> | Gruppo che include tutti gli utenti.<br/>                                                                                                              |
| Locale<br/>            | S-1-2-0<br/> | Utenti che accedono ai [*terminali*](/windows/desktop/SecGloss/t-gly) in locale (fisicamente) connessi al sistema.<br/> |
| ID proprietario autore<br/> | S-1-3-0<br/> | Identificatore di sicurezza da sostituire con l'ID di sicurezza dell'utente che ha creato un nuovo oggetto. Questo SID viene usato in ACE ereditabili.<br/>   |
| ID gruppo creatore<br/> | S-1-3-1<br/> | Identificatore di sicurezza che deve essere sostituito dal SID di gruppo primario dell'utente che ha creato un nuovo oggetto. Utilizzare questo SID in ACE ereditabili.<br/>         |



 

Nella tabella seguente sono elencate le costanti di autorità di identificazione predefinite. I primi quattro valori vengono utilizzati con i SID universali noti; l'ultimo valore viene utilizzato con i SID noti di Windows.



| Autorità di identificazione                         | Valore        | Valore stringa |
|----------------------------------------------|--------------|-------------------|
| \_ \_ autorità SID di sicurezza null \_<br/>    | 0<br/> | S-1-0<br/>  |
| \_ \_ autorità SID del mondo della sicurezza \_<br/>   | 1<br/> | S-1-1<br/>  |
| \_ \_ autorità SID locale di sicurezza \_<br/>   | 2<br/> | S-1-2<br/>  |
| autorità di certificazione SID dell'autore della sicurezza \_ \_ \_<br/> | 3<br/> | S-1-3<br/>  |
| \_autorità NT per la sicurezza \_<br/>           | 5<br/> | S-1-5<br/>  |



 

I valori [*RID*](/windows/desktop/SecGloss/r-gly) seguenti vengono utilizzati con i [*SID noti universali*](/windows/desktop/SecGloss/u-gly). Nella colonna autorità identificatore viene visualizzato il prefisso dell'autorità di identificazione con la quale è possibile combinare il RID per creare un SID noto universalmente.



| Autorità identificatore relativo            | Valore        | Valore stringa |
|------------------------------------------|--------------|----------------------|
| \_RID null di sicurezza \_<br/>           | 0<br/> | S-1-0<br/>     |
| \_RID del mondo della sicurezza \_<br/>          | 0<br/> | S-1-1<br/>     |
| \_RID locale \_ sicurezza<br/>          | 0<br/> | S-1-2<br/>     |
| \_ \_ RID accesso locale \_ sicurezza<br/>   | 1<br/> | S-1-2<br/>     |
| \_RID del \_ proprietario del creatore della sicurezza \_<br/> | 0<br/> | S-1-3<br/>     |
| \_ \_ RID gruppo creatore \_ sicurezza<br/> | 1<br/> | S-1-3<br/>     |



 

L' \_ autorità di identificazione predefinita della protezione NT \_ Authority (S-1-5) produce SID che non sono universali ma sono significativi solo nelle installazioni di Windows. \_Per creare SID noti, è possibile utilizzare i seguenti valori RID con l' \_ autorità NT di sicurezza.



| Costante                                          | Valore stringa               | Identifica                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RID sicurezza in \_ remoto \_<br/>                  | S-1-5-1<br/>         | Utenti che accedono ai [*terminali*](/windows/desktop/SecGloss/t-gly) usando un modem remoto. Si tratta di un identificatore di gruppo.<br/>                                                                                                                                                                                                                                                                                                                                                                  |
| \_RID rete di sicurezza \_<br/>                 | S-1-5-2<br/>         | Utenti che accedono in una rete. Si tratta di un identificatore di gruppo aggiunto al token di un processo quando era connesso attraverso una rete. Il tipo di accesso corrispondente è LOGON32 \_ login \_ Network.<br/>                                                                                                                                                                                                                                                                                                                      |
| \_RID batch di sicurezza \_<br/>                   | S-1-5-3<br/>         | Utenti che accedono utilizzando una funzionalità di Accodamento batch. Si tratta di un identificatore di gruppo aggiunto al token di un processo quando è stato registrato come processo batch. Il tipo di accesso corrispondente è LOGON32 \_ login \_ batch.<br/>                                                                                                                                                                                                                                                                                                                 |
| \_RID Interactive sicurezza \_<br/>             | S-1-5-4<br/>         | Utenti che accedono a un'operazione interattiva. Identificatore di gruppo aggiunto al token di un processo quando è stato eseguito l'accesso in modo interattivo. Il tipo di accesso corrispondente è LOGON32 \_ Logon \_ Interactive.<br/>                                                                                                                                                                                                                                                                                                            |
| \_ \_ RID ID accesso di sicurezza \_<br/>              | S-1-5-5-*X* - *Y*<br/> | Una sessione di accesso. Viene usato per garantire che solo [*i processi*](/windows/desktop/SecGloss/p-gly) in una determinata sessione di accesso possano ottenere l'accesso agli oggetti della stazione di Windows per la sessione. I valori *X* e *Y* per questi SID sono diversi per ogni sessione di accesso. Il \_ conteggio degli ID di accesso alla sicurezza del valore \_ \_ \_ è il numero di RID in questo identificatore (5-*X* - *Y*).<br/>                                                                                                                   |
| \_RID servizio di sicurezza \_<br/>                 | S-1-5-6<br/>         | Account autorizzati ad accedere come servizio. Si tratta di un identificatore di gruppo aggiunto al token di un processo quando è stato registrato come servizio. Il tipo di accesso corrispondente è LOGON32 \_ Logon \_ Service.<br/>                                                                                                                                                                                                                                                                                                                    |
| \_ \_ RID accesso anonimo \_ sicurezza<br/>        | S-1-5-7<br/>         | Accesso anonimo o accesso alla sessione null.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| \_RID del proxy di sicurezza \_<br/>                   | S-1-5-8<br/>         | Proxy.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| SICUREZZA \_ di \_ controller aziendali \_ RID<br/> | S-1-5-9<br/>         | Controller aziendali.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| autorid entità di sicurezza \_ \_ \_<br/>         | S-1-5-10<br/>        | L' \_ identificatore di sicurezza automatica principale può essere utilizzato nell'elenco ACL di un oggetto utente o gruppo. Durante un controllo di accesso, il sistema sostituisce il SID con il SID dell'oggetto. Il \_ SID Self-Service principale è utile per specificare una voce ACE ereditabile che si applica all'oggetto utente o gruppo che eredita la voce ACE. È l'unico modo per rappresentare il SID di un oggetto creato nel [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) predefinito dello schema.<br/> |
| \_RID utente autenticato per la sicurezza \_ \_<br/>     | S-1-5-11<br/>        | Utenti autenticati.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| \_RID del \_ codice con restrizioni di sicurezza \_<br/>        | S-1-5-12<br/>        | Codice con restrizioni.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| \_RID del \_ server \_ Terminal di sicurezza<br/>        | S-1-5-13<br/>        | Servizi terminal. Aggiunto automaticamente al token di sicurezza di un utente che accede a un server terminal.<br/>                                                                                                                                                                                                                                                                                                                                                                                                            |
| \_ \_ RID sistema locale \_ sicurezza<br/>           | S-1-5-18<br/>        | Un account speciale usato dal sistema operativo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| SICUREZZA \_ NT \_ non \_ univoca<br/>              | S-1-5-21<br/>        | I SID non sono univoci.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| \_ \_ RID dominio incorporato sicurezza \_<br/>         | S-1-5-32<br/>        | Dominio di sistema predefinito.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| \_RID del \_ \_ codice con \_ restrizioni di scrittura della sicurezza<br/> | S-1-5-33<br/>        | Scrivere codice con restrizioni.<br/> |


 

I seguenti RID sono relativi a ogni dominio.



| RID                                                                | Valore       | Identifica                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ALIAS di dominio \_ \_ RID \_ CERTSVC \_ \_ gruppo di accesso DCOM \_<br/>              | 0x0000023E | Gruppo di utenti che possono connettersi alle autorità di certificazione utilizzando Distributed Component Object Model (DCOM).<br/>                                                                                                                          |
| \_ \_ amministratore RID utenti di dominio \_<br/>                                      | 0x000001F4 | Account utente amministratore in un dominio.<br/>                                                                                                                                                                                              |
| \_ \_ Guest RID utente di dominio \_<br/>                                      | 0x000001F5 | Account utente guest in un dominio. Gli utenti che non dispongono di un account possono accedere automaticamente a questo account.<br/>                                                                                                                            |
| \_ \_ amministratori RID del gruppo di dominio \_<br/>                                    | 0x00000200 | Gruppo Domain Administrators. Questo account esiste solo nei sistemi che eseguono sistemi operativi server.<br/>                                                                                                                                   |
| \_ \_ utenti RID del gruppo di dominio \_<br/>                                     | 0x00000201 | Gruppo che contiene tutti gli account utente in un dominio. Tutti gli utenti vengono aggiunti automaticamente a questo gruppo.<br/>                                                                                                                                     |
| \_ \_ Guest RID del gruppo di dominio \_<br/>                                    | 0x00000202 | Account di gruppo Guest in un dominio.<br/>                                                                                                                                                                                                      |
| \_ \_ computer RID del gruppo di dominio \_<br/>                                 | 0x00000203 | Gruppo computer del dominio. Tutti i computer nel dominio sono membri di questo gruppo.<br/>                                                                                                                                                       |
| \_ \_ controller RID del gruppo di dominio \_<br/>                               | 0x00000204 | Il gruppo controller di dominio. Tutti i controller di dominio nel dominio sono membri di questo gruppo.<br/>                                                                                                                                                           |
| \_amministratori del \_ \_ certificato RID del gruppo \_ di dominio<br/>                              | 0x00000205 | Gruppo di autori di certificati. I computer che eseguono Servizi certificati sono membri di questo gruppo.<br/>                                                                                                                                      |
| controller di dominio del gruppo di dominio \_ \_ RID \_ Enterprise \_ ReadOnly \_ \_<br/> | 0x000001F2 | Gruppo di controller di dominio di sola lettura aziendali.<br/>                                                                                                                                                                                     |
| \_ \_ \_ amministratori dello schema RID del gruppo di dominio \_<br/>                            | 0x00000206 | Gruppo degli amministratori dello schema. I membri di questo gruppo possono modificare lo schema di Active Directory.<br/>                                                                                                                                           |
| gruppo di dominio \_ \_ RID \_ Enterprise \_ Admins<br/>                        | 0x00000207 | Gruppo Enterprise Administrators. I membri di questo gruppo dispongono di accesso completo a tutti i domini nella foresta Active Directory. Gli amministratori dell'organizzazione sono responsabili delle operazioni a livello di foresta, ad esempio l'aggiunta o la rimozione di nuovi domini.<br/> |
| \_amministratori dei \_ \_ criteri RID del gruppo \_ di dominio<br/>                            | 0x00000208 | Gruppo di amministratori dei criteri.<br/>                                                                                                                                                                                                         |
| controller di dominio di sola \_ \_ lettura RID del gruppo di \_ dominio \_<br/>                     | 0x00000209 | Gruppo di controller di dominio di sola lettura.<br/>                                                                                                                                                                                                |                                             
| \_ \_ \_ controller clonabili del gruppo di dominio RID \_<br />                   | 0x0000020A | Gruppo di controller di dominio clonabili.<br/>                                                                                                                                                                                                |
| RID del gruppo di dominio- \_ \_ \_ \_ riservato CDC<br />                            | 0x0000020C | Gruppo CDC riservato.<br/>                                                                                                                                                                                                                   |
| \_ \_ \_ utenti protetti RID del gruppo di dominio \_<br />                         | 0x0000020D | Gruppo utenti protetti.</br>                                                                                                                                                                                                                |
| \_amministratori della \_ \_ chiave RID del gruppo \_ di dominio<br />                              | 0x0000020E | Il gruppo Key Admins.<br/>                                                                                                                                                                                                                     |
| \_amministratori della \_ \_ chiave Enterprise \_ RID \_ del gruppo di dominio<br />                  | 0x0000020F | Gruppo Enterprise Key Admins</br>                                                                                                                                                                                                           |



 

Per specificare il livello di integrità obbligatorio vengono usati i RID seguenti.



| RID                                                     | Valore                                               | Identifica                        |
|---------------------------------------------------------|-----------------------------------------------------|-----------------------------------|
| \_RID non \_ attendibile obbligatorio per la sicurezza \_<br/>          | 0x00000000<br/>                               | Untrusted.<br/>             |
| SICUREZZA \_ obbligatoria \_ basso \_ RID<br/>                | 0x00001000<br/>                               | Integrità bassa.<br/>         |
| PROTEZIONE \_ obbligatoria \_ media \_ RID<br/>             | 0x00002000<br/>                               | Integrità media.<br/>      |
| SICUREZZA \_ obbligatoria \_ media \_ Plus \_ RID<br/>       | PROTEZIONE \_ obbligatoria \_ media \_ RID + 0x100<br/> | Integrità media elevata.<br/> |
| SICUREZZA \_ \_ elevata obbligatoria \_ RID<br/>               | 0X00003000<br/>                               | Integrità elevata.<br/>        |
| \_RID di \_ sistema \_ obbligatorio per la sicurezza<br/>             | 0x00004000<br/>                               | Integrità del sistema.<br/>      |
| \_ \_ \_ RID processo protetto obbligatorio \_ per la sicurezza<br/> | 0x00005000<br/>                               | Processo protetto.<br/>     |



 

La tabella seguente include esempi di RID relativi al dominio che è possibile usare per formare i SID noti per i gruppi locali (alias). Per ulteriori informazioni sui gruppi locali e globali, vedere [funzioni di gruppo](/windows/desktop/NetMgmt/local-group-functions) e [funzioni di gruppo](/windows/desktop/NetMgmt/group-functions)locali.



| RID                                                              | Valore                 |Valore stringa  | Identifica                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------|-----------------|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ amministratori RID alias di dominio \_<br/>                            | 0x00000220<br/> | S-1-5-32-544<br/> | Gruppo locale utilizzato per l'amministrazione del dominio.<br/>                                                                                                                                                                                                                            |
| \_ \_ utenti RID alias di dominio \_<br/>                             | 0x00000221<br/> | S-1-5-32-545<br/> | Gruppo locale che rappresenta tutti gli utenti nel dominio.<br/>                                                                                                                                                                                                                          |
| utenti \_ \_ Guest RID \_ alias di dominio<br/>                            | 0x00000222<br/> | S-1-5-32-546<br/> | Gruppo locale che rappresenta i Guest del dominio.<br/>                                                                                                                                                                                                                             |
| \_ \_ \_ utenti avanzati RID alias \_ di dominio<br/>                      | 0x00000223<br/> | S-1-5-32-547<br/> | Gruppo locale utilizzato per rappresentare un utente o un set di utenti che si aspettano di trattare un sistema come se fosse il personal computer anziché come una workstation per più utenti.<br/>                                                                                                      |
| \_account RID alias di dominio \_ \_ \_ Ops<br/>                      | 0x00000224<br/> | S-1-5-32-548<br/> | Gruppo locale esistente solo nei sistemi che eseguono sistemi operativi server. Questo gruppo locale consente di controllare gli account non amministratore.<br/>                                                                                                                                    |
| \_operazioni di \_ \_ sistema RID alias di \_ dominio<br/>                       | 0x00000225<br/> | S-1-5-32-549<br/> | Gruppo locale esistente solo nei sistemi che eseguono sistemi operativi server. Questo gruppo locale esegue funzioni amministrative di sistema, escluse le funzioni di sicurezza. Stabilisce le condivisioni di rete, controlla le stampanti, Sblocca le workstation ed esegue altre operazioni.<br/> |
| \_Ops di \_ \_ stampa RID alias di \_ dominio<br/>                        | 0x00000226<br/> | S-1-5-32-550<br/> | Gruppo locale esistente solo nei sistemi che eseguono sistemi operativi server. Questo gruppo locale controlla le stampanti e le code di stampa.<br/>                                                                                                                                                |
| \_operazioni di \_ \_ backup RID alias di \_ dominio<br/>                       | 0x00000227<br/> | S-1-5-32-551<br/> | Gruppo locale utilizzato per controllare l'assegnazione dei privilegi di backup e ripristino di file.<br/>                                                                                                                                                                                            |
| \_ \_ replicatore RID alias di dominio \_<br/>                        | 0x00000228<br/> | S-1-5-32-552<br/> | Gruppo locale responsabile della copia dei database di sicurezza dal controller di dominio primario ai controller di dominio di backup. Questi account vengono usati solo dal sistema.<br/>                                                                                                       |
| \_ \_ \_ server RAS RID alias \_ di dominio<br/>                      | 0x00000229<br/> | S-1-5-32-553<br/> | Gruppo locale che rappresenta i server RAS e IAS. Questo gruppo consente l'accesso a vari attributi degli oggetti utente.<br/>                                                                                                                                                             |
| \_ \_ PREW2KCOMPACCESS RID alias di dominio \_<br/>                  | 0x0000022A<br/> | S-1-5-32-554<br/> | Un gruppo locale disponibile solo nei sistemi che eseguono Windows Server 2000. Per ulteriori informazioni, vedere [consentire l'accesso anonimo](allowing-anonymous-access.md).<br/>                                                                                                                    |
| ALIAS di dominio \_ \_ RID \_ Remote \_ Desktop \_ Users<br/>            | 0x0000022B<br/> | S-1-5-32-555<br/> | Gruppo locale che rappresenta tutti gli utenti di desktop remoto.<br/>                                                                                                                                                                                                                         |
| operazione \_ di \_ \_ configurazione di rete RID \_ alias di dominio \_<br/>       | 0x0000022C<br/> | S-1-5-32-556<br/> | Gruppo locale che rappresenta la configurazione di rete. <br/>                                                                                                                                                                                                                       |
| ALIAS di dominio \_ \_ RID del \_ trust tra foreste in ingresso \_ \_ \_<br/> | 0x0000022D<br/> | S-1-5-32-557<br/> | Gruppo locale che rappresenta gli utenti di trust tra foreste.<br/>                                                                                                                                                                                                                           |
| \_utenti di \_ \_ monitoraggio RID alias di \_ dominio<br/>                 | 0x0000022E<br/> | S-1-5-32-558<br/> | Gruppo locale che rappresenta tutti gli utenti monitorati.<br/>                                                                                                                                                                                                                        |
| \_utenti di \_ \_ registrazione RID alias di \_ dominio<br/>                    | 0x0000022F<br/> | S-1-5-32-559<br/> | Gruppo locale responsabile della registrazione degli utenti.<br/>                                                                                                                                                                                                                                    |
| \_ \_ AUTHORIZATIONACCESS RID alias di dominio \_<br/>               | 0x00000230<br/> | S-1-5-32-560<br/> | Gruppo locale che rappresenta tutti gli accessi autorizzati.<br/>                                                                                                                                                                                                                            |
| \_alias di \_ dominio \_ \_ server licenze Servizi terminal RID \_<br/>              | 0x00000231<br/> | S-1-5-32-561<br/> | Gruppo locale presente solo nei sistemi che eseguono sistemi operativi server che consentono Servizi terminal e accesso remoto.<br/>                                                                                                                                                  |
| \_ \_ \_ utenti DCOM RID alias \_ di dominio<br/>                       | 0x00000232<br/> | S-1-5-32-562<br/> | Gruppo locale che rappresenta gli utenti che possono utilizzare Distributed Component Object Model (DCOM).<br/>                                                                                                                                                                                      |
| \_ \_ IUSERS RID alias di dominio \_<br/>                            | 0X00000238<br/> | S-1-5-32-568<br/> | Gruppo locale che rappresenta gli utenti Internet.<br/>                                                                                                                                                                                                                                   |
| \_operatori di \_ \_ crittografia RID alias di \_ dominio<br/>                 | 0x00000239<br/> | S-1-5-32-569<br/> | Gruppo locale che rappresenta l'accesso agli operatori di crittografia.<br/>                                                                                                                                                                                                                 |
| gruppo di entità a cui è stato memorizzato un alias di dominio \_ \_ \_ \_ \_<br/>      | 0x0000023B<br/> | S-1-5-32-571<br/> | Gruppo locale che rappresenta le entità che possono essere memorizzate nella cache.<br/>                                                                                                                                                                                                                    |
| \_gruppo di \_ \_ entità non \_ memorizzabile nella cache \_ \_ del dominio alias RID<br/> | 0x0000023C<br/> | S-1-5-32-572<br/> | Gruppo locale che rappresenta entità che non possono essere memorizzate nella cache.<br/>                                                                                                                                                                                                                 |
| \_ \_ \_ \_ \_ gruppo lettori registro eventi RID \_ alias del dominio<br/>        | 0x0000023D<br/> | S-1-5-32-573<br/> | Gruppo locale che rappresenta i lettori del registro eventi.<br/>                                                                                                                                                                                                                                |
| ALIAS di dominio \_ \_ RID \_ CERTSVC \_ \_ gruppo di accesso DCOM \_<br/>      | 0x0000023E<br/> | S-1-5-32-574<br/> | Il gruppo locale di utenti che possono connettersi alle autorità di certificazione utilizzando Distributed Component Object Model (DCOM).<br/>                                                                                                                                                          |
| \_server di \_ \_ \_ accesso remoto RDS \_ RID alias di dominio \_<br />     | 0x0000023F<br/> | S-1-5-32-575<br/> | Gruppo locale che rappresenta i server di accesso remoto RDS.<br/> |
| \_ \_ \_ \_ \_ server endpoint Servizi Desktop remoto RID alias di dominio                 | 0x00000240<br/> | S-1-5-32-576<br/> | Gruppo locale che rappresenta i server endpoint.<br/> |
| \_server di \_ \_ gestione RDS \_ RID \_ alias di dominio               | 0x00000241<br/> | S-1-5-32-577<br/> | Gruppo locale che rappresenta i server di gestione. <br/>|
| ALIAS di dominio \_ \_ RID di \_ Hyper \_ V \_ Admins                       | 0x00000242<br/> | S-1-5-32-578<br/> | Un gruppo locale che rappresenta gli amministratori di Hyper-v <br/>|
| \_controllo di \_ accesso RID alias di dominio \_ \_ \_ \_ Ops       | 0x00000243<br/> | S-1-5-32-579<br/> | Gruppo locale che rappresenta le operazioni di assistenza per il controllo di accesso.<br/> |
| \_utenti di \_ \_ gestione remota \_ RID \_ alias di dominio              | 0x00000244<br/> | S-1-5-32-580<br/> | Gruppo locale che rappresenta gli utenti di gestione remota. <br/>|
| \_ \_ \_ account predefinito RID alias \_ dominio                       | 0x00000245<br/> | S-1-5-32-581<br/> | Gruppo locale che rappresenta l'account predefinito. <br/>|
| ALIAS di dominio \_ \_ RID di \_ \_ replica archiviazione \_ amministratori               | 0x00000246<br/> | S-1-5-32-582<br/> | Gruppo locale che rappresenta gli amministratori della replica di archiviazione. <br/>|
| \_proprietari del \_ \_ dispositivo RID alias di \_ dominio                            | 0x00000247<br/> | S-1-5-32-583<br/> | Un gruppo locale che rappresenta può effettuare impostazioni previste per i proprietari del dispositivo.<br/>|


 

L'enumerazione di [**\_ \_ \_ tipi SID ben nota**](/windows/desktop/api/Winnt/ne-winnt-well_known_sid_type) definisce l'elenco dei SID usati comunemente. Inoltre, il [linguaggio SDDL (Security Descriptor Definition Language](security-descriptor-definition-language.md) ) utilizza [stringhe SID](sid-strings.md) per fare riferimento a SID noti in un formato stringa.

 

