---
title: Funzioni di gruppo
description: Un gruppo globale contiene gli account utente di un dominio raggruppati in un nome di account di gruppo.
ms.assetid: 2199258d-bde9-4fdb-b9c1-147616420fbe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7696755cd5f5cbe75de11d386cb238fa3bd5d35d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399547"
---
# <a name="group-functions"></a>Funzioni di gruppo

Un *gruppo globale* contiene gli account utente di un dominio raggruppati in un nome di account di gruppo. Un gruppo globale può contenere solo membri (utenti) del dominio in cui viene creato il gruppo globale; non può contenere gruppi locali. Un gruppo globale è disponibile all'interno del proprio dominio e all'interno di qualsiasi dominio trusting.

Le funzioni del gruppo di gestione di rete controllano i gruppi globali. Le funzioni di gruppo sono elencate di seguito.



| Funzione                                     | Descrizione                                                                       |
|----------------------------------------------|-----------------------------------------------------------------------------------|
| [**NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd)           | Crea un gruppo globale.                                                           |
| [**NetGroupAddUser**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadduser)   | Aggiunge un utente a un gruppo globale esistente.                                        |
| [**NetGroupDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdel)           | Rimuove un gruppo globale indipendentemente dal fatto che il gruppo disponga di membri.                  |
| [**NetGroupDelUser**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdeluser)   | Rimuove un nome utente da un gruppo globale.                                        |
| [**NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum)         | Elenca tutti i gruppi globali in un server.                                              |
| [**NetGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo)   | Restituisce informazioni su un particolare gruppo globale.                              |
| [**NetGroupGetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers) | Elenca tutti i membri di un determinato gruppo globale.                                   |
| [**NetGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo)   | Imposta le informazioni generali su un gruppo globale.                                    |
| [**NetGroupSetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetusers) | Assegna membri a un nuovo gruppo globale; sostituisce i membri di un gruppo esistente. |



 

Quando si chiama la funzione [**NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd) per creare un gruppo globale, è necessario specificare un nome di gruppo. Inizialmente, un nuovo gruppo non dispone di membri.

Gli account utente appartengono automaticamente agli specifici utenti del dominio del gruppo globale. L'appartenenza a questo gruppo è indirettamente controllata dalle funzioni [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd), [**NetUserDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel)e [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .

Le informazioni sull'account di gruppo globale sono disponibili ai livelli seguenti:

-   [**Informazioni sul gruppo \_ \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_0)
-   [**Informazioni sul gruppo \_ \_ 1**](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_1)
-   [**Informazioni sul gruppo \_ \_ 2**](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_2)
-   [**Informazioni sul gruppo \_ \_ 3**](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_3)
-   [**Informazioni sul gruppo \_ \_ 1002**](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_1002)
-   [**Informazioni sul gruppo \_ \_ 1005**](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_1005)

I livelli 1002 e 1005 sono validi solo per la funzione [**NetGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo) .

Le informazioni sui membri del gruppo globale sono disponibili al livello di Informazioni seguente:

-   [**Informazioni sugli utenti del gruppo \_ \_ \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-group_users_info_0)

Per ulteriori informazioni, vedere la pagina relativa alle [funzioni del gruppo locale](local-group-functions.md)di gestione della rete.

Se si sta programmando per Active Directory, è possibile chiamare determinati metodi di Active Directory Service Interface (ADSI) per ottenere la stessa funzionalità che è possibile ottenere chiamando le funzioni del gruppo di gestione di rete. Per ulteriori informazioni, vedere [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup).

 

 