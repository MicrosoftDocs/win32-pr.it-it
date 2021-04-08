---
title: Funzioni di gruppo locale
description: Un gruppo locale può contenere account utente o account di gruppo globali da uno o più domini. I gruppi globali possono contenere utenti di un solo dominio. Un gruppo locale condivide i privilegi e i diritti comuni solo all'interno del proprio dominio.
ms.assetid: ed4c59d6-6532-4190-9807-95678053fc72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd13a23b322a860d6896a213b27fb6263586412
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727815"
---
# <a name="local-group-functions"></a>Funzioni di gruppo locale

Un *gruppo locale* può contenere account utente o account di gruppo globali da uno o più domini. I gruppi globali possono contenere utenti di un solo dominio. Un gruppo locale condivide i privilegi e i diritti comuni solo all'interno del proprio dominio.

Le funzioni gruppo locale gestione rete controllano i membri dei gruppi locali in modo che le funzioni possano essere chiamate solo localmente nel sistema in cui è definito il gruppo locale. In una workstation o in un server che non è un controller di dominio, è possibile utilizzare solo un gruppo locale definito nel sistema.

In Active Directory, i domini in modalità nativa, i gruppi locali sono denominati *gruppi locali di dominio*. I gruppi locali di dominio sono disponibili in tutti i controller di dominio, i server membri e le workstation aggiunti al dominio. Active Directory domini in modalità mista vengono definiti sul controller di dominio primario e replicati in tutti gli altri controller del dominio. Pertanto, un gruppo locale è disponibile su tutti i controller di dominio all'interno del dominio in cui è stato creato.

Le funzioni del gruppo locale creano o eliminano gruppi locali e ricontrollano o modificano le appartenenze dei gruppi locali. Queste funzioni sono elencate di seguito.



| Funzione                                                   | Descrizione                                                             |
|------------------------------------------------------------|-------------------------------------------------------------------------|
| [**NetLocalGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupadd)               | Crea un gruppo locale.                                                  |
| [**NetLocalGroupAddMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupaddmembers) | Aggiunge uno o più utenti o gruppi globali a un gruppo locale esistente.     |
| [**NetLocalGroupDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdel)               | Elimina un gruppo locale, rimuovendo tutti i membri esistenti dal gruppo.    |
| [**NetLocalGroupDelMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdelmembers) | Rimuove uno o più membri da un gruppo locale esistente.               |
| [**NetLocalGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupenum)             | Restituisce informazioni su ogni account di gruppo locale in un server.         |
| [**NetLocalGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetinfo)       | Restituisce informazioni su un determinato account di gruppo locale in un server. |
| [**NetLocalGroupGetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetmembers) | Elenca tutti i membri di un gruppo locale specificato.                           |
| [**NetLocalGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetinfo)       | Imposta le informazioni generali su un gruppo locale.                           |
| [**NetLocalGroupSetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetmembers) | Assegna membri a un gruppo locale.                                       |



 

È possibile aggiungere un membro a un gruppo locale specificando l'ID di sicurezza (SID) del membro. Per convertire un nome di account membro in un SID, chiamare la funzione [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) .

Quando si crea un gruppo locale chiamando la funzione [**NetLocalGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupadd) , è necessario specificare un nome di gruppo locale. Inizialmente, il gruppo locale non dispone di membri.

Le informazioni sull'account di gruppo locale sono disponibili ai livelli seguenti:

-   [**LOCALGROUP \_ info \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_info_0)
-   [**LOCALGROUP \_ info \_ 1**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_info_1)
-   [**LOCALGROUP \_ INFO \_ 1002**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_info_1002)

Le informazioni sull'appartenenza ai gruppi locali sono disponibili ai livelli di informazioni seguenti:

-   [**Informazioni sui membri di LOCALGROUP \_ \_ \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_members_info_0)
-   [**Informazioni sui membri di LOCALGROUP \_ \_ \_ 1**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_members_info_1)
-   [**Informazioni sui membri di LOCALGROUP \_ \_ \_ 2**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_members_info_2)
-   [**Informazioni sui membri di LOCALGROUP \_ \_ \_ 3**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_members_info_3)

È possibile recuperare i nomi dei gruppi locali a cui un utente appartiene chiamando la funzione [**funzione NetUserGetLocalGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups) , specificando il livello di Informazioni seguente:

[**Informazioni sugli utenti di LOCALGROUP \_ \_ \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-localgroup_users_info_0)

Per ulteriori informazioni, vedere le funzioni del [gruppo](group-functions.md)di gestione di rete.

Se si sta programmando per Active Directory, è possibile chiamare determinati metodi di Active Directory Service Interface (ADSI) per ottenere la stessa funzionalità che è possibile ottenere chiamando le funzioni del gruppo locale di gestione della rete. Per ulteriori informazioni, vedere [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup).

 

 