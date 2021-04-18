---
description: Vengono illustrate le stringhe utilizzate da SDDLs.
ms.assetid: a531532f-afba-46a1-8576-90d4ff881b94
title: Stringhe SID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dad653f221f884fb5d96a402109d0b415d64222
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308128"
---
# <a name="sid-strings"></a>Stringhe SID

Nel linguaggio SDDL ( [Security Descriptor Definition Language](security-descriptor-definition-language.md) ) la [stringa del descrittore di sicurezza](security-descriptor-string-format.md) utilizza stringhe SID per i componenti seguenti di un [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly):

-   Proprietario
-   Gruppo primario
-   [Trustee](trustees.md) in una voce ACE

Una stringa SID in una stringa del descrittore di sicurezza può usare la rappresentazione di stringa standard di un SID (s-*R* - *i* - *s* -  ) o una delle costanti di stringa definite in SDDL. h. Per ulteriori informazioni sulla notazione di stringa SID standard, vedere la pagina relativa ai [Componenti SID](sid-components.md).

Le costanti di stringa SID seguenti per i SID noti sono definite in SDDL. h. Per informazioni sugli [*ID relativi*](/windows/desktop/SecGloss/r-gly) corrispondenti (RID), vedere [SID noti](well-known-sids.md).



| Stringa SID SDDL | Costante in SDDL. h                               | Alias dell'account e RID corrispondente                                                                                                                                                                                                                        |
|-----------------|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| UN<br/> | SDDL \_ Anonimo<br/>                       | Accesso anonimo. Il RID corrispondente è il \_ RID di accesso anonimo alla sicurezza \_ \_ .<br/>                                                                                                                                                                      |
| Ao<br/> | \_operatori di account SDDL \_<br/>              | Operatori account. Il RID corrispondente è l' \_ alias del dominio \_ \_ Ops account RID \_ .<br/>                                                                                                                                                                   |
| Au<br/> | \_utenti autenticati \_ SDDL<br/>            | Utenti autenticati. Il RID corrispondente è il \_ RID utente autenticato della sicurezza \_ \_ .<br/>                                                                                                                                                               |
| BA<br/> | \_Amministratori predefiniti SDDL \_<br/>         | Amministratori predefiniti. Il RID corrispondente è DOMAIN \_ alias \_ RID \_ Admins.<br/>                                                                                                                                                                   |
| BG<br/> | \_Guest predefiniti SDDL \_<br/>                 | Guest predefiniti. Il RID corrispondente è un \_ alias di dominio \_ RID \_ Guest.<br/>                                                                                                                                                                           |
| Bo<br/> | \_operatori di backup SDDL \_<br/>               | Operatori di backup. Il RID corrispondente è l' \_ alias del dominio \_ operazioni di backup RID \_ \_ .<br/>                                                                                                                                                                     |
| Bu<br/> | \_utenti predefiniti SDDL \_<br/>                  | Utenti incorporati. Il RID corrispondente è un \_ alias di dominio \_ RID \_ Users.<br/>                                                                                                                                                                             |
| CA<br/> | \_ \_ amministratori serv del certificato SDDL \_<br/>      | Autori di certificati. Il RID corrispondente è il \_ gruppo di dominio \_ RID \_ CERT \_ Admins.<br/>                                                                                                                                                              |
| CD<br/> | \_ \_ accesso DCOM CERTSVC \_ SDDL<br/>           | Utenti che possono connettersi alle autorità di certificazione utilizzando Distributed Component Object Model (DCOM). Il gruppo RID corrispondente è l'alias di dominio \_ \_ RID \_ CERTSVC \_ DCOM \_ \_ .<br/>                                                                  |
| CG<br/> | \_gruppo di autori SDDL \_<br/>                  | Gruppo creatore. Il RID corrispondente è RID del gruppo di autori della sicurezza \_ \_ \_ .<br/>                                                                                                                                                                          |
| Co<br/> | \_proprietario dell'autore SDDL \_<br/>                  | Proprietario dell'autore. Il RID corrispondente è il \_ RID del proprietario del creatore della sicurezza \_ \_ .<br/>                                                                                                                                                                          |
| DA<br/> | \_amministratori di dominio SDDL \_<br/>          | Amministratori di dominio. Il RID corrispondente è \_ amministratore RID del gruppo di dominio \_ \_ .<br/>                                                                                                                                                                     |
| DC<br/> | \_computer del dominio SDDL \_<br/>               | Computer del dominio. Il RID corrispondente è \_ computer RID del gruppo di dominio \_ \_ .<br/>                                                                                                                                                                       |
| GG<br/> | \_controller di \_ dominio \_ SDDL<br/>     | Controller di dominio. Il RID corrispondente è il \_ gruppo di dominio \_ \_ controller RID.<br/>                                                                                                                                                                   |
| DG<br/> | \_Guest di dominio SDDL \_<br/>                  | Guest di dominio. Il RID corrispondente è il \_ gruppo di dominio \_ \_ Guest RID.<br/>                                                                                                                                                                             |
| DU<br/> | \_utenti del dominio SDDL \_<br/>                   | Utenti di dominio. Il RID corrispondente è il \_ gruppo di dominio \_ \_ utenti RID.<br/>                                                                                                                                                                               |
| EA<br/> | SDDL \_ Enterprise \_ Admins<br/>              | Amministratori dell'organizzazione. Il RID corrispondente è il \_ gruppo di dominio \_ RID \_ Enterprise \_ Admins.<br/>                                                                                                                                                     |
| ED<br/> | \_controller di \_ dominio SDDL Enterprise \_<br/> | Controller di dominio aziendali. Il RID corrispondente è il \_ RID di accesso al server di sicurezza \_ \_ .<br/>                                                                                                                                                           |
| Ciao<br/> | SDDL \_ ml \_ alto<br/>                        | Livello di integrità elevato. Il RID corrispondente è il \_ RID massimo obbligatorio per la sicurezza \_ \_ .<br/>                                                                                                                                                                  |
| IU<br/> | SDDL \_ interattivo<br/>                     | Utente connesso in modo interattivo. Identificatore di gruppo aggiunto al token di un processo quando è stato eseguito l'accesso in modo interattivo. Il tipo di accesso corrispondente è LOGON32 \_ Logon \_ Interactive. Il RID corrispondente è il \_ RID interattivo per la sicurezza \_ .<br/> |
| TIMA<br/> | \_amministratore locale \_ SDDL<br/>                    | Amministratore locale. Il RID corrispondente è \_ amministratore RID utente del dominio \_ \_ .<br/>                                                                                                                                                                         |
| LG<br/> | \_Guest locale \_ SDDL<br/>                    | Guest locale. Il RID corrispondente è \_ \_ Guest RID utente \_ del dominio.<br/>                                                                                                                                                                                 |
| LS<br/> | \_servizio locale \_ SDDL<br/>                  | Account del servizio locale. Il RID corrispondente è il \_ RID del servizio locale di sicurezza \_ \_ .<br/>                                                                                                                                                                  |
| LW<br/> | SDDL \_ ml- \_ basso<br/>                         | Livello di integrità basso. Il RID corrispondente è obbligatorio per la sicurezza con \_ \_ \_ RID basso.<br/>                                                                                                                                                                    |
| MI<br/> | \_MLMEDIUM SDDL<br/>                        | Livello di integrità medio. Il RID corrispondente è il \_ RID di sicurezza \_ medio obbligatorio \_ .<br/>                                                                                                                                                              |
| "MU"<br/> | \_utenti di PerfMon PerfMon \_<br/>                  | Utenti di performance monitor.<br/>                                                                                                                                                                                                                      |
| NON<br/> | \_operazioni di \_ configurazione di rete SDDL \_<br/>     | Operatori di configurazione di rete. Il RID corrispondente è la \_ configurazione di rete RID alias di dominio \_ \_ \_ \_ Ops.<br/>                                                                                                                                      |
| NS<br/> | \_servizio di rete SDDL \_<br/>                | Account del servizio di rete. Il RID corrispondente è \_ RID servizio di rete sicurezza \_ \_ .<br/>                                                                                                                                                              |
| Nu<br/> | \_rete SDDL<br/>                         | Utente di accesso alla rete. Si tratta di un identificatore di gruppo aggiunto al token di un processo quando era connesso attraverso una rete. Il tipo di accesso corrispondente è LOGON32 \_ login \_ Network. Il RID corrispondente è RID della rete di sicurezza \_ \_ .<br/>                |
| PA<br/> | \_amministratori di \_ criteri di gruppo SDDL \_<br/>           | Criteri di gruppo gli amministratori. Il gruppo RID corrispondente è \_ \_ amministratori dei criteri RID del gruppo di dominio \_ \_ .<br/>                                                                                                                                                       |
| PO<br/> | \_operatori stampanti \_ SDDL<br/>              | Operatori stampanti. Il RID corrispondente è il \_ RID alias di dominio \_ \_ Ops di stampa \_ .<br/>                                                                                                                                                                     |
| PS<br/> | \_auto personale \_ SDDL<br/>                  | Entità autonoma. Il RID corrispondente è \_ autorid dell'entità di sicurezza \_ \_ .<br/>                                                                                                                                                                        |
| PU<br/> | \_utenti avanzati \_ SDDL<br/>                    | Power Users. Il RID corrispondente è un \_ alias di dominio \_ RID \_ Power \_ Users.<br/>                                                                                                                                                                         |
| RC<br/> | \_ \_ codice con restrizioni SDDL<br/>                | Codice con restrizioni. Si tratta di un token con restrizioni creato mediante la funzione [**CreateRestrictedToken**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) . Il RID corrispondente è un \_ codice con restrizioni per la sicurezza \_ \_ .<br/>                                                        |
| Rd<br/> | \_Desktop remoto \_ SDDL<br/>                 | Utenti di Terminal Server. Il RID corrispondente è il \_ RID alias del dominio \_ \_ \_ utenti desktop remoto \_ .<br/>                                                                                                                                                     |
| Re<br/> | \_replicatore SDDL<br/>                      | Replicatore. Il RID corrispondente è il \_ \_ replicatore RID alias di dominio \_ .<br/>                                                                                                                                                                            |
| RO<br/> | \_Controller di dominio per Enterprise \_ ro SDDL \_<br/>             | Controller di dominio di sola lettura aziendali. Il RID corrispondente è controller di dominio del gruppo di dominio \_ \_ RID \_ Enterprise \_ ReadOnly \_ \_ .<br/>                                                                                                                |
| RS<br/> | \_server RAS \_ SDDL<br/>                    | Gruppo server RAS. Il RID corrispondente è il \_ \_ server RAS RID alias del dominio \_ \_ .<br/>                                                                                                                                                                   |
| RU<br/> | \_Alias SDDL \_ PREW2KCOMPACC<br/>            | Alias per concedere le autorizzazioni agli account che usano le applicazioni compatibili con i sistemi operativi precedenti a Windows 2000. Il RID corrispondente è il \_ RID alias del dominio \_ \_ PREW2KCOMPACCESS.<br/>                                                         |
| SA<br/> | \_amministratori dello schema SDDL \_<br/>          | Amministratori dello schema. Il RID corrispondente è DOMAIN \_ Group \_ RID \_ schema \_ Admins.<br/>                                                                                                                                                             |
| SI<br/> | \_sistema SDDL ml \_<br/>                      | Livello di integrità del sistema. Il RID corrispondente è il \_ RID di sistema obbligatorio per la sicurezza \_ \_ .<br/>                                                                                                                                                              |
| IN modo<br/> | \_operatori del server SDDL \_<br/>               | Operatori server. Il RID corrispondente è un \_ alias del dominio \_ operazioni di sistema RID \_ \_ .<br/>                                                                                                                                                                     |
| SU<br/> | \_servizio SDDL<br/>                         | Utente di accesso al servizio. Si tratta di un identificatore di gruppo aggiunto al token di un processo quando è stato registrato come servizio. Il tipo di accesso corrispondente è LOGON32 \_ Logon \_ Service. Il RID corrispondente è il \_ RID del servizio di sicurezza \_ .<br/>                       |
| SY<br/> | \_sistema locale \_ SDDL<br/>                   | Sistema locale. Il RID corrispondente è il \_ RID del sistema locale di sicurezza \_ \_ .<br/>                                                                                                                                                                            |
| WD<br/> | SDDL \_ Everyone<br/>                        | Tutti. Il RID corrispondente è il \_ RID del mondo della sicurezza \_ .<br/>                                                                                                                                                                                        |



 

Le funzioni [**ConvertSidToStringSid**](/windows/desktop/api/Sddl/nf-sddl-convertsidtostringsida) e [**ConvertStringSidToSid**](/windows/desktop/api/Sddl/nf-sddl-convertstringsidtosida) utilizzano sempre la notazione di stringa SID standard e non supportano le costanti di stringa SID SDDL.

Per ulteriori informazioni sui SID ben noti, vedere [SID noti](well-known-sids.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[\[MS-DTYP \] : Security Descriptor Description Language](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)
</dt> </dl>

