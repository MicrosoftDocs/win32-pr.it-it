---
title: Funzioni utente
description: Le funzioni utente di gestione della rete controllano l'account di un utente nel database di sicurezza, ovvero il database sam (Security Accounts Manager) o, nel caso dei controller di dominio, Active Directory. Le funzioni utente sono elencate di seguito.
ms.assetid: cf0e5102-3924-46c0-8124-0aa04e95f48d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34c8d7b59ff121c0225f166888b42ef1a731336ed80799cd0593ba38b4fb04ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796817"
---
# <a name="user-functions"></a>Funzioni utente

Le funzioni utente di gestione della rete controllano l'account di un utente nel database di sicurezza, ovvero il database sam (Security Accounts Manager) o, nel caso dei controller di dominio, Active Directory. Le funzioni utente sono elencate di seguito.



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



 

Ogni utente o applicazione che accede alle risorse di rete deve avere un account nel database di sicurezza. I servizi directory usano questo account per verificare che l'utente o l'applicazione abbia l'autorizzazione per connettersi a una risorsa. Quando un utente o un'applicazione richiede l'accesso a una risorsa, il sistema di sicurezza Windows verifica la presenza di un account utente o un account di gruppo appropriato per consentire l'accesso.

Dopo aver rimosso un account utente chiamando la [**funzione NetUserDel,**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel) l'utente non può più accedere al server se non usando l'account guest.

Poiché la password di un utente è riservata, non viene restituita dalla [**funzione NetUserEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum) o [**NetUserGetInfo.**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo) La password viene assegnata inizialmente quando si chiama [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd).

Le informazioni sull'account utente sono disponibili ai livelli seguenti:

-   [**INFORMAZIONI \_ UTENTE \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_0)
-   [**INFORMAZIONI \_ UTENTE \_ 1**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1)
-   [**INFORMAZIONI \_ UTENTE \_ 2**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_2)
-   [**INFORMAZIONI \_ UTENTE \_ 3**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_3)
-   [**INFORMAZIONI \_ UTENTE \_ 4**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_4)
-   [**INFORMAZIONI \_ UTENTE \_ 10**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_10)
-   [**INFORMAZIONI \_ UTENTE \_ 11**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_11)
-   [**INFORMAZIONI \_ UTENTE \_ 20**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_20)
-   [**INFORMAZIONI \_ UTENTE \_ 21**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_21)
-   [**INFORMAZIONI \_ UTENTE \_ 22**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_22)
-   [**INFORMAZIONI \_ UTENTE \_ 23**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_23)

Inoltre, i livelli di informazioni seguenti sono validi quando si chiama la [**funzione NetUserSetInfo:**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo)

-   [**INFORMAZIONI \_ UTENTE \_ 1003**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1003)
-   [**INFORMAZIONI \_ UTENTE \_ 1005**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1005)
-   [**INFORMAZIONI \_ UTENTE \_ 1006**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1006)
-   [**INFORMAZIONI \_ UTENTE \_ 1007**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1007)
-   [**INFORMAZIONI \_ UTENTE \_ 1008**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1008)
-   [**INFORMAZIONI \_ UTENTE \_ 1009**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1009)
-   [**INFORMAZIONI \_ UTENTE \_ 1010**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1010)
-   [**INFORMAZIONI \_ UTENTE \_ 1011**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1011)
-   [**INFORMAZIONI \_ UTENTE \_ 1012**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1012)
-   [**INFORMAZIONI \_ UTENTE \_ 1014**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1014)
-   [**INFORMAZIONI \_ UTENTE \_ 1017**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1017)
-   [**INFORMAZIONI \_ UTENTE \_ 1020**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1020)
-   [**INFORMAZIONI \_ UTENTE \_ 1024**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1024)
-   [**INFORMAZIONI \_ UTENTE \_ 1051**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1051)
-   [**INFORMAZIONI \_ UTENTE \_ 1052**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1052)
-   [**INFORMAZIONI \_ UTENTE \_ 1053**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1053)

Le funzioni seguenti consentono alle applicazioni di controllare la conformità delle password.



| Funzione                                                               | Descrizione                                                                                                |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**NetValidatePasswordPolicyFree**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicyfree) | Libera la memoria allocata dalla [**funzione NetValidatePasswordPolicy.**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicy) |
| [**NetValidatePasswordPolicy**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicy)         | Verifica che le password soddisfino i requisiti di complessità, aging, lunghezza minima e riutilizzo della cronologia.            |



 

Se si sta programmando per Active Directory, è possibile chiamare determinati metodi ADSI (Active Directory Service Interface) per ottenere le stesse funzionalità che è possibile ottenere chiamando le funzioni utente di gestione della rete. Per altre informazioni, vedere [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) e [**IADsComputer.**](/windows/desktop/api/iads/nn-iads-iadscomputer)

 

 