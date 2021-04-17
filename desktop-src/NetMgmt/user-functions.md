---
title: Funzioni utente
description: Le funzioni utente di gestione di rete controllano l'account di un utente nel database di sicurezza, ovvero il database di gestione degli account di sicurezza (SAM) o, nel caso di controller di dominio, il Active Directory. Le funzioni utente sono elencate di seguito.
ms.assetid: cf0e5102-3924-46c0-8124-0aa04e95f48d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6a3349673d09e42fbfe7a5dc949d1bcff53b828
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300283"
---
# <a name="user-functions"></a>Funzioni utente

Le funzioni utente di gestione di rete controllano l'account di un utente nel database di sicurezza, ovvero il database di gestione degli account di sicurezza (SAM) o, nel caso di controller di dominio, il Active Directory. Le funzioni utente sono elencate di seguito.



| Funzione                                               | Descrizione                                                         |
|--------------------------------------------------------|---------------------------------------------------------------------|
| [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd)                       | Aggiunge un account utente e assegna una password e un livello di privilegio.     |
| [**NetUserChangePassword**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserchangepassword) | Modifica la password di un utente per un server o un dominio di rete specificato. |
| [**NetUserDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel)                       | Elimina un account utente dal server.                             |
| [**NetUserEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum)                     | Elenca tutti gli account utente in un server.                                |
| [**NetUserGetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups)           | Restituisce un elenco di nomi di gruppi globali a cui appartiene un utente.       |
| [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo)               | Restituisce informazioni su un determinato account utente in un server.    |
| [**Funzione NetUserGetLocalGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups) | Restituisce un elenco di nomi di gruppi locali a cui appartiene un utente.        |
| [**NetUserSetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetgroups)           | Imposta le appartenenze ai gruppi globali per un account utente specificato.         |
| [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo)               | Imposta la password e altri elementi di un account utente.             |



 

Ogni utente o applicazione che accede alle risorse di rete deve disporre di un account nel database di sicurezza. I servizi directory usano questo account per verificare che l'utente o l'applicazione disponga delle autorizzazioni per connettersi a una risorsa. Quando un utente o un'applicazione richiede l'accesso a una risorsa, il sistema di sicurezza di Windows verifica la presenza di un account utente o di un account di gruppo appropriato per consentire l'accesso.

Una volta rimosso un account utente chiamando la funzione [**NetUserDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel) , l'utente non potrà più accedere al server, tranne tramite l'account Guest.

Poiché la password di un utente è riservata, non viene restituita dalla funzione [**NetUserEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum) o dalla funzione [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo) . La password viene inizialmente assegnata quando si chiama [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd).

Le informazioni sull'account utente sono disponibili ai livelli seguenti:

-   [**\_Informazioni utente \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_0)
-   [**\_Informazioni utente \_ 1**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1)
-   [**\_Informazioni utente \_ 2**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_2)
-   [**\_Informazioni utente \_ 3**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_3)
-   [**\_Informazioni utente \_ 4**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_4)
-   [**\_Informazioni utente \_ 10**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_10)
-   [**\_Informazioni utente \_ 11**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_11)
-   [**\_Informazioni utente \_ 20**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_20)
-   [**\_Informazioni utente \_ 21**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_21)
-   [**\_Informazioni utente \_ 22**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_22)
-   [**\_Informazioni utente \_ 23**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_23)

Inoltre, i livelli di informazioni seguenti sono validi quando si chiama la funzione [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) :

-   [**\_Informazioni utente \_ 1003**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1003)
-   [**\_Informazioni utente \_ 1005**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1005)
-   [**\_Informazioni utente \_ 1006**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1006)
-   [**\_Informazioni utente \_ 1007**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1007)
-   [**\_Informazioni utente \_ 1008**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1008)
-   [**\_Informazioni utente \_ 1009**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1009)
-   [**\_Informazioni utente \_ 1010**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1010)
-   [**\_Informazioni utente \_ 1011**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1011)
-   [**\_Informazioni utente \_ 1012**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1012)
-   [**\_Informazioni utente \_ 1014**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1014)
-   [**\_Informazioni utente \_ 1017**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1017)
-   [**\_Informazioni utente \_ 1020**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1020)
-   [**\_Informazioni utente \_ 1024**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1024)
-   [**\_Informazioni utente \_ 1051**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1051)
-   [**\_Informazioni utente \_ 1052**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1052)
-   [**\_Informazioni utente \_ 1053**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1053)

Le funzioni seguenti consentono alle applicazioni di controllare la conformità delle password.



| Funzione                                                               | Descrizione                                                                                                |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**NetValidatePasswordPolicyFree**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicyfree) | Libera la memoria allocata dalla funzione [**NetValidatePasswordPolicy**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicy) . |
| [**NetValidatePasswordPolicy**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicy)         | Verifica che le password soddisfino i requisiti di complessità, durata, lunghezza minima e riutilizzo della cronologia.            |



 

Se si sta programmando per Active Directory, è possibile chiamare determinati metodi di Active Directory Service Interface (ADSI) per ottenere la stessa funzionalità che è possibile ottenere chiamando le funzioni utente di gestione di rete. Per ulteriori informazioni, vedere [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) e [**IADsComputer**](/windows/desktop/api/iads/nn-iads-iadscomputer).

 

 