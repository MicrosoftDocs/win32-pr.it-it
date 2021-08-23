---
description: Un privilegio è il diritto di un account, ad esempio un account utente o di gruppo, di eseguire diverse operazioni correlate al sistema nel computer locale, ad esempio l'arresto del sistema, il caricamento dei driver di dispositivo o la modifica dell'ora di sistema.
ms.assetid: fe6aae0f-93eb-4aba-a6ac-45e71c251c51
title: Privilegi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7c0289ea66f4c1d2f94cb74112a1160dd93cc873125ae5183bd6a6fab5834b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118912137"
---
# <a name="privileges"></a>Privilegi

Un [](/windows/desktop/SecGloss/p-gly) privilegio è il diritto di un account, ad esempio un account utente o di gruppo, di eseguire diverse operazioni correlate al sistema nel computer locale, ad esempio l'arresto del sistema, il caricamento dei driver di dispositivo o la modifica dell'ora di sistema. I privilegi differiscono dai diritti di accesso in due modi:

-   I privilegi controllano l'accesso alle risorse di sistema e alle attività correlate al sistema, mentre i diritti di accesso controllano l'accesso [agli oggetti a protezione diretta.](securable-objects.md)
-   Un amministratore di sistema assegna privilegi agli account utente e di gruppo, mentre il sistema concede o nega l'accesso a un oggetto a protezione diretta in base ai diritti di accesso concessi nelle voci ACE nell'elenco DACL dell'oggetto.

Ogni sistema dispone di un database di account in cui sono archiviati i privilegi di cui dispongono gli account utente e di gruppo. Quando un utente esegue l'accesso, il sistema produce un [token](access-tokens.md) di accesso che contiene un elenco dei privilegi dell'utente, inclusi quelli concessi all'utente o ai gruppi a cui appartiene l'utente. Si noti che i privilegi si applicano solo al computer locale. Un account di dominio può avere privilegi diversi in computer diversi.

Quando l'utente tenta di eseguire un'operazione con privilegi, il sistema controlla il token di accesso dell'utente per determinare se l'utente dispone dei privilegi necessari e, in tal caso, controlla se i privilegi sono abilitati. Se l'utente non supera questi test, il sistema non esegue l'operazione.

Per determinare i privilegi mantenuti in un token di accesso, chiamare la [**funzione GetTokenInformation,**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) che indica anche quali privilegi sono abilitati. La maggior parte dei privilegi è disabilitata per impostazione predefinita.

L Windows API definisce un set di costanti stringa, ad esempio \_ edizione Standard ASSIGNPRIMARYTOKEN NAME, per identificare i \_ vari privilegi. Queste costanti sono le stesse in tutti i sistemi e sono definite in Winnt.h. Per una tabella dei privilegi definiti da Windows, vedere [Costanti dei privilegi.](authorization-constants.md) Tuttavia, le funzioni che ottengono e regolano i privilegi in un token di accesso usano il [**tipo LUID**](/windows/desktop/api/Winnt/ns-winnt-luid) per identificare i privilegi. I **valori LUID** per un privilegio possono differire da un computer a un altro e da un avvio a un altro nello stesso computer. Per ottenere il **LUID corrente** che corrisponde a una delle costanti stringa, usare la [**funzione LookupPrivilegeValue.**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) Usare la [**funzione LookupPrivilegeName**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegenamea) per convertire un **LUID** nella costante stringa corrispondente.

Il sistema fornisce un set di nomi visualizzati che descrivono ognuno dei privilegi. Sono utili quando è necessario visualizzare una descrizione di un privilegio per l'utente. Usare la [**funzione LookupPrivilegeDisplayName**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegedisplaynamea) per recuperare una stringa di descrizione che corrisponde alla costante stringa per un privilegio. Ad esempio, nei sistemi che usano l'inglese (Stati Uniti) il nome visualizzato per il privilegio \_ edizione Standard SYSTEMTIME NAME è "Change the system time" (Modifica ora \_ di sistema).

È possibile usare la [**funzione PrivilegeCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-privilegecheck) per determinare se un token di accesso contiene un set specificato di privilegi. Ciò è utile principalmente per le applicazioni server che rappresentano un client.

Un amministratore di sistema può usare strumenti di amministrazione, ad esempio User Manager, per aggiungere o rimuovere privilegi per gli account utente e di gruppo. Gli amministratori possono usare le funzioni [*dell'autorità*](/windows/desktop/SecGloss/l-gly) di sicurezza locale (LSA) a livello di codice per utilizzare i privilegi. Le [**funzioni LsaAddAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaaddaccountrights) e [**LsaRemoveAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaremoveaccountrights) aggiungono o rimuovono privilegi da un account. La [**funzione LsaEnumerateAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaenumerateaccountrights) enumera i privilegi di un account specificato. La [**funzione LsaEnumerateAccountsWithUserRight**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaenumerateaccountswithuserright) enumera gli account che contengono un privilegio specificato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti di autorizzazione](authorization-constants.md)
</dt> <dt>

[Abilitazione e disabilitazione dei privilegi in C++](enabling-and-disabling-privileges-in-c--.md)
</dt> </dl>

 

 
