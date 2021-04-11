---
description: I diritti dell'account determinano il tipo di accesso che può essere eseguito da un account utente. Un amministratore assegna i diritti di account agli account utente e di gruppo. I diritti degli account di ogni utente includono quelli concessi all'utente e ai gruppi a cui appartiene l'utente.
ms.assetid: 42139d33-2d56-4d29-998f-5512bb795d44
title: Costanti dei diritti dell'account (Ntsecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d5b16b75af89773df969ec78b771986b0a73dfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227187"
---
# <a name="account-rights-constants"></a>Costanti dei diritti dell'account

I diritti dell'account determinano il tipo di accesso che può essere eseguito da un account utente. Un amministratore assegna i diritti di account agli account utente e di gruppo. I diritti dell'account di ogni utente includono quelli concessi all'utente e ai gruppi a cui appartiene l'utente.

Un amministratore di sistema può utilizzare le funzioni dell' [*autorità di sicurezza locale*](/windows/desktop/SecGloss/l-gly) (LSA) per lavorare con i diritti dell'account. Le funzioni [**LsaAddAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaaddaccountrights) e [**LsaRemoveAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaremoveaccountrights) aggiungono o rimuovono i diritti dell'account da un account. La funzione [**LsaEnumerateAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaenumerateaccountrights) enumera i diritti dell'account contenuti in un account specificato. La funzione [**LsaEnumerateAccountsWithUserRight**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaenumerateaccountswithuserright) enumera gli account che contengono il diritto di un account specificato.

Per controllare la capacità di accesso di un account, vengono utilizzate le costanti di questo account seguenti. Le funzioni [**LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera) o [**LsaLogonUser**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalogonuser) hanno esito negativo se l'account a cui si è connessi non dispone dei diritti di account necessari per il tipo di accesso eseguito.



| Costante/valore                                                                                                                                                                                                                                                                                                                           | Descrizione                                                                                            |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| <span id="SE_BATCH_LOGON_NAME"></span><span id="se_batch_logon_name"></span><dl> <dt>**Se \_ Testo \_ \_ nome accesso batch**</dt> <dt>("SeBatchLogonRight")</dt> </dl>                                                                         | Obbligatorio per l'accesso di un account tramite il tipo di accesso batch.<br/>                               |
| <span id="SE_DENY_BATCH_LOGON_NAME"></span><span id="se_deny_batch_logon_name"></span><dl> <dt>**Se \_ Nega \_ testo \_ \_ nome accesso batch**</dt> <dt>("SeDenyBatchLogonRight")</dt> </dl>                                                     | Nega in modo esplicito a un account il diritto di accedere usando il tipo di accesso batch.<br/>                |
| <span id="SE_DENY_INTERACTIVE_LOGON_NAME"></span><span id="se_deny_interactive_logon_name"></span><dl> <dt>**Se \_ Nega \_ testo \_ \_ nome accesso interattivo**</dt> <dt>("SeDenyInteractiveLogonRight")</dt> </dl>                             | Nega in modo esplicito a un account il diritto di accedere usando il tipo di accesso interattivo.<br/>          |
| <span id="SE_DENY_NETWORK_LOGON_NAME"></span><span id="se_deny_network_logon_name"></span><dl> <dt>**Se \_ Nega \_ testo \_ \_ nome accesso alla rete**</dt> <dt>("SeDenyNetworkLogonRight")</dt> </dl>                                             | Nega in modo esplicito a un account il diritto di accedere usando il tipo di accesso alla rete.<br/>              |
| <span id="SE_DENY_REMOTE_INTERACTIVE_LOGON_NAME"></span><span id="se_deny_remote_interactive_logon_name"></span><dl> <dt>**Se \_ NEGA il testo del \_ \_ \_ \_ nome di accesso interattivo remoto**</dt> <dt>("SeDenyRemoteInteractiveLogonRight")</dt> </dl> | Nega in modo esplicito a un account il diritto di accedere in remoto usando il tipo di accesso interattivo.<br/> |
| <span id="SE_DENY_SERVICE_LOGON_NAME"></span><span id="se_deny_service_logon_name"></span><dl> <dt>**Se \_ NEGA il testo del \_ \_ \_ nome di accesso del servizio**</dt> <dt>("SeDenyServiceLogonRight")</dt> </dl>                                             | Nega in modo esplicito a un account il diritto di accedere usando il tipo di accesso al servizio.<br/>              |
| <span id="SE_INTERACTIVE_LOGON_NAME"></span><span id="se_interactive_logon_name"></span><dl> <dt>**Se \_ Testo \_ \_ nome accesso interattivo**</dt> <dt>("SeInteractiveLogonRight")</dt> </dl>                                                 | Obbligatorio per l'accesso di un account tramite il tipo di accesso interattivo.<br/>                         |
| <span id="SE_NETWORK_LOGON_NAME"></span><span id="se_network_logon_name"></span><dl> <dt>**Se \_ Testo \_ \_ nome accesso alla rete**</dt> <dt>("SeNetworkLogonRight")</dt> </dl>                                                                 | Obbligatorio per l'accesso di un account tramite il tipo di accesso alla rete.<br/>                             |
| <span id="SE_REMOTE_INTERACTIVE_LOGON_NAME"></span><span id="se_remote_interactive_logon_name"></span><dl> <dt>**Se \_ Testo \_ \_ \_ nome accesso interattivo remoto**</dt> <dt>("SeRemoteInteractiveLogonRight")</dt> </dl>                     | Obbligatorio per l'accesso remoto da parte di un account tramite il tipo di accesso interattivo.<br/>                |
| <span id="SE_SERVICE_LOGON_NAME"></span><span id="se_service_logon_name"></span><dl> <dt>**Se \_ Testo \_ del \_ nome di accesso del servizio**</dt> <dt>("SeServiceLogonRight")</dt> </dl>                                                                 | Obbligatorio per l'accesso di un account tramite il tipo di accesso al servizio.<br/>                             |



## <a name="remarks"></a>Commenti

I \_ diritti nega se sostituiscono i diritti dell'account corrispondente. Un amministratore può assegnare un \_ diritto Deny se a un account per eseguire l'override di eventuali diritti di accesso che un account potrebbe avere come risultato di un'appartenenza a un gruppo. Ad esempio, è possibile assegnare il \_ \_ \_ nome di accesso di rete se a tutti, ma assegnare \_ il \_ diritto di accesso negato alla rete per gli \_ \_ amministratori per impedire l'amministrazione remota dei computer.

Tutte le funzioni LSA indicate nell'introduzione precedente supportano i diritti e i [privilegi](privilege-constants.md)dell'account. Diversamente dai privilegi, tuttavia, i diritti dell'account non sono supportati dalle funzioni [**LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) e [**LookupPrivilegeName**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegenamea) . La funzione [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) otterrà informazioni sui diritti dell'account se tokenGroups e non TokenPrivileges viene specificato come valore del parametro *TokenInformationClass* .

Le costanti a destra dell'account precedente sono definite come stringhe in Ntsecapi. h. Ad esempio, la \_ costante del nome di accesso interattivo Se \_ \_ è definita come "SeInteractiveLogonRight".

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Ntsecapi. h</dt> </dl> |



 

