---
description: I diritti dell'account determinano il tipo di accesso che un account utente può eseguire. Un amministratore assegna i diritti di account agli account utente e di gruppo. I diritti dell'account di ogni utente includono quelli concessi all'utente e ai gruppi a cui appartiene l'utente.
ms.assetid: 42139d33-2d56-4d29-998f-5512bb795d44
title: Costanti dei diritti dell'account (Ntsecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4285561761908308f67585544bef6c87d2f0ebbaa25de9989f53fcab051b79b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785370"
---
# <a name="account-rights-constants"></a>Costanti per i diritti dell'account

I diritti dell'account determinano il tipo di accesso che un account utente può eseguire. Un amministratore assegna i diritti di account agli account utente e di gruppo. I diritti dell'account di ogni utente includono quelli concessi all'utente e ai gruppi a cui appartiene l'utente.

Un amministratore di sistema può usare le [*funzioni dell'autorità*](/windows/desktop/SecGloss/l-gly) di sicurezza locale (LSA) per usare i diritti dell'account. Le [**funzioni LsaAddAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaaddaccountrights) e [**LsaRemoveAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaremoveaccountrights) aggiungono o rimuovono i diritti dell'account da un account. La [**funzione LsaEnumerateAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaenumerateaccountrights) enumera i diritti dell'account di un account specificato. La [**funzione LsaEnumerateAccountsWithUserRight**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaenumerateaccountswithuserright) enumera gli account che hanno un diritto di account specificato.

Per controllare la capacità di accesso di un account, vengono usate le costanti seguenti per i diritti di account. Le [**funzioni LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera) o [**LsaLogonUser**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalogonuser) hanno esito negativo se l'account connesso non dispone dei diritti di account necessari per il tipo di accesso eseguito.



| Costante/valore                                                                                                                                                                                                                                                                                                                           | Descrizione                                                                                            |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| <span id="SE_BATCH_LOGON_NAME"></span><span id="se_batch_logon_name"></span><dl> <dt>**edizione Standard \_ BATCH \_ LOGON \_ NAME**</dt> <dt>TEXT("SeBatchLogonRight")</dt> </dl>                                                                         | Obbligatorio per l'accesso di un account usando il tipo di accesso batch.<br/>                               |
| <span id="SE_DENY_BATCH_LOGON_NAME"></span><span id="se_deny_batch_logon_name"></span><dl> <dt>**edizione Standard \_ DENY \_ BATCH \_ LOGON \_ NAME**</dt> <dt>TEXT("SeDenyBatchLogonRight")</dt> </dl>                                                     | Nega in modo esplicito a un account il diritto di accedere usando il tipo di accesso batch.<br/>                |
| <span id="SE_DENY_INTERACTIVE_LOGON_NAME"></span><span id="se_deny_interactive_logon_name"></span><dl> <dt>**edizione Standard \_ DENY \_ INTERACTIVE \_ LOGON \_ NAME**</dt> <dt>TEXT("SeDenyInteractiveLogonRight")</dt> </dl>                             | Nega in modo esplicito a un account il diritto di accedere usando il tipo di accesso interattivo.<br/>          |
| <span id="SE_DENY_NETWORK_LOGON_NAME"></span><span id="se_deny_network_logon_name"></span><dl> <dt>**edizione Standard \_ DENY \_ NETWORK \_ LOGON \_ NAME**</dt> <dt>TEXT("SeDenyNetworkLogonRight")</dt> </dl>                                             | Nega in modo esplicito a un account il diritto di accedere usando il tipo di accesso di rete.<br/>              |
| <span id="SE_DENY_REMOTE_INTERACTIVE_LOGON_NAME"></span><span id="se_deny_remote_interactive_logon_name"></span><dl> <dt>**edizione Standard \_ DENY \_ REMOTE INTERACTIVE LOGON \_ \_ \_ NAME**</dt> <dt>TEXT("SeDenyRemoteInteractiveLogonRight")</dt> </dl> | Nega in modo esplicito a un account il diritto di accedere in remoto usando il tipo di accesso interattivo.<br/> |
| <span id="SE_DENY_SERVICE_LOGON_NAME"></span><span id="se_deny_service_logon_name"></span><dl> <dt>**edizione Standard \_ DENY \_ SERVICE \_ LOGON \_ NAME**</dt> <dt>TEXT("SeDenyServiceLogonRight")</dt> </dl>                                             | Nega in modo esplicito a un account il diritto di accedere usando il tipo di accesso del servizio.<br/>              |
| <span id="SE_INTERACTIVE_LOGON_NAME"></span><span id="se_interactive_logon_name"></span><dl> <dt>**edizione Standard \_ INTERACTIVE \_ LOGON \_ NAME**</dt> <dt>TEXT("SeInteractiveLogonRight")</dt> </dl>                                                 | Obbligatorio per l'accesso di un account usando il tipo di accesso interattivo.<br/>                         |
| <span id="SE_NETWORK_LOGON_NAME"></span><span id="se_network_logon_name"></span><dl> <dt>**edizione Standard \_ NETWORK \_ LOGON \_ NAME**</dt> <dt>TEXT("SeNetworkLogonRight")</dt> </dl>                                                                 | Obbligatorio per l'accesso di un account usando il tipo di accesso di rete.<br/>                             |
| <span id="SE_REMOTE_INTERACTIVE_LOGON_NAME"></span><span id="se_remote_interactive_logon_name"></span><dl> <dt>**edizione Standard \_ REMOTE \_ INTERACTIVE \_ LOGON \_ NAME**</dt> <dt>TEXT("SeRemoteInteractiveLogonRight")</dt> </dl>                     | Obbligatorio per l'accesso remoto di un account usando il tipo di accesso interattivo.<br/>                |
| <span id="SE_SERVICE_LOGON_NAME"></span><span id="se_service_logon_name"></span><dl> <dt>**edizione Standard \_ SERVICE \_ LOGON \_ NAME**</dt> <dt>TEXT("SeServiceLogonRight")</dt> </dl>                                                                 | Obbligatorio per l'accesso di un account usando il tipo di accesso del servizio.<br/>                             |



## <a name="remarks"></a>Commenti

I edizione Standard \_ DENY eseguono l'override dei diritti dell'account corrispondenti. Un amministratore può assegnare un edizione Standard deny a un account per eseguire l'override di tutti i diritti di accesso che un account potrebbe avere come risultato \_ dell'appartenenza a un gruppo. Ad esempio, è possibile assegnare il diritto edizione Standard NETWORK LOGON NAME a Everyone, ma assegnare il diritto edizione Standard DENY NETWORK LOGON NAME agli amministratori per impedire l'amministrazione \_ \_ remota dei \_ \_ \_ \_ \_ computer.

Tutte le funzioni LSA indicate nell'introduzione precedente supportano sia i diritti dell'account che [i privilegi](privilege-constants.md). A differenza dei privilegi, tuttavia, i diritti dell'account non sono supportati dalle [**funzioni LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) e [**LookupPrivilegeName.**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegenamea) La [**funzione GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) otterrà informazioni sui diritti dell'account se TokenGroups e non TokenPrivileges vengono specificati come valore del *parametro TokenInformationClass.*

Le costanti di destra dell'account precedenti sono definite come stringhe in Ntsecapi.h. Ad esempio, la edizione Standard \_ INTERACTIVE LOGON NAME è definita come \_ \_ "SeInteractiveLogonRight".

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Ntsecapi.h</dt> </dl> |



 

