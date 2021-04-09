---
description: Un privilegio è il diritto di un account, ad esempio un account utente o di gruppo, per eseguire varie operazioni relative al sistema sul computer locale, ad esempio l'arresto del sistema, il caricamento dei driver di dispositivo o la modifica dell'ora di sistema.
ms.assetid: fe6aae0f-93eb-4aba-a6ac-45e71c251c51
title: Privilegi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cccedffdf5786da07dd2cfd77c3de428ee15ba94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966819"
---
# <a name="privileges"></a>Privilegi

Un [*privilegio*](/windows/desktop/SecGloss/p-gly) è il diritto di un account, ad esempio un account utente o di gruppo, per eseguire varie operazioni relative al sistema sul computer locale, ad esempio l'arresto del sistema, il caricamento dei driver di dispositivo o la modifica dell'ora di sistema. I privilegi differiscono dai diritti di accesso in due modi:

-   I privilegi controllano l'accesso alle risorse di sistema e alle attività relative al sistema, mentre i diritti di accesso controllano l'accesso agli [oggetti a protezione diretta](securable-objects.md).
-   Un amministratore di sistema assegna privilegi agli account utente e di gruppo, mentre il sistema concede o nega l'accesso a un oggetto a protezione diretta in base ai diritti di accesso concessi nelle voci ACE nell'elenco DACL dell'oggetto.

Ogni sistema dispone di un database di account che archivia i privilegi utilizzati dagli account utente e di gruppo. Quando un utente esegue l'accesso, il sistema produce un [token di accesso](access-tokens.md) che contiene un elenco dei privilegi dell'utente, inclusi quelli concessi all'utente o ai gruppi a cui appartiene l'utente. Si noti che i privilegi sono validi solo per il computer locale. un account di dominio può avere privilegi diversi in computer diversi.

Quando l'utente tenta di eseguire un'operazione con privilegi, il sistema controlla il token di accesso dell'utente per determinare se l'utente possiede i privilegi necessari e, in tal caso, verifica se i privilegi sono abilitati. Se l'utente non riesce a eseguire questi test, il sistema non esegue l'operazione.

Per determinare i privilegi contenuti in un token di accesso, chiamare la funzione [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) , che indica anche quali privilegi sono abilitati. La maggior parte dei privilegi è disabilitata per impostazione predefinita.

L'API Windows definisce un set di costanti di stringa, ad esempio SE \_ ASSIGNPRIMARYTOKEN \_ , per identificare i vari privilegi. Queste costanti sono le stesse in tutti i sistemi e sono definite in Winnt. h. Per una tabella dei privilegi definiti da Windows, vedere [costanti Privilege](authorization-constants.md). Tuttavia, le funzioni che ottengono e regolano i privilegi in un token di accesso usano il tipo [**LUID**](/windows/desktop/api/Winnt/ns-winnt-luid) per identificare i privilegi. I valori **LUID** per un privilegio possono differire da un computer a un altro e da un avvio all'altro nello stesso computer. Per ottenere il **LUID** corrente che corrisponde a una delle costanti di stringa, usare la funzione [**LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) . Usare la funzione [**LookupPrivilegeName**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegenamea) per convertire un **LUID** nella costante di stringa corrispondente.

Il sistema fornisce un set di nomi visualizzati che descrivono ognuno dei privilegi. Queste informazioni sono utili quando è necessario visualizzare una descrizione di un privilegio per l'utente. Usare la funzione [**LookupPrivilegeDisplayName**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegedisplaynamea) per recuperare una stringa di descrizione che corrisponde alla costante di stringa per un privilegio. Ad esempio, nei sistemi che utilizzano la lingua inglese (Stati Uniti), il nome visualizzato per il privilegio del nome di SE \_ SYSTEMTIME \_ è "modifica l'ora di sistema".

È possibile usare la funzione [**PrivilegeCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-privilegecheck) per determinare se un token di accesso include un set di privilegi specificato. Questa operazione è utile principalmente per le applicazioni server che rappresentano un client.

Un amministratore di sistema può utilizzare strumenti di amministrazione, ad esempio gestione utenti, per aggiungere o rimuovere privilegi per gli account utente e di gruppo. Gli amministratori possono utilizzare a livello di codice le funzioni dell' [*autorità di sicurezza locale*](/windows/desktop/SecGloss/l-gly) (LSA) per lavorare con i privilegi. Le funzioni [**LsaAddAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaaddaccountrights) e [**LsaRemoveAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaremoveaccountrights) aggiungono o rimuovono i privilegi da un account. La funzione [**LsaEnumerateAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaenumerateaccountrights) enumera i privilegi contenuti in un account specificato. La funzione [**LsaEnumerateAccountsWithUserRight**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaenumerateaccountswithuserright) enumera gli account che contengono un privilegio specificato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti di autorizzazione](authorization-constants.md)
</dt> <dt>

[Abilitazione e disabilitazione dei privilegi in C++](enabling-and-disabling-privileges-in-c--.md)
</dt> </dl>

 

 
