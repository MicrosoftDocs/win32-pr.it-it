---
title: Funzioni modali dell'utente
description: Le funzioni modali utente di gestione della rete ottengono e impostano parametri a livello di sistema correlati al comportamento del sistema di sicurezza.
ms.assetid: e655b9f6-2808-4bd4-998c-c8a2e980920b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: addea3c76d79cbcdb0e359424be154893d2c436c1f6d45157ecf50e748fc9417
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796797"
---
# <a name="user-modal-functions"></a>Funzioni modali dell'utente

Le funzioni modali utente di gestione della rete ottengono e impostano parametri a livello di sistema correlati al comportamento del sistema di sicurezza.

Di seguito sono elencate le funzioni modali dell'utente.



| Funzione                                     | Descrizione                                                                                                                                                                                             |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetUserModalsGet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget) | Restituisce informazioni globali per tutti gli utenti e i gruppi globali nel database di sicurezza, ovvero il database di gestione degli account di sicurezza (SAM) o, nel caso dei controller di dominio, Active Directory. |
| [**NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset) | Imposta le informazioni globali per tutti gli utenti e i gruppi globali nel database di sicurezza.                                                                                                                       |



 

Le **funzioni NetUserModalsGet** e **NetUserModalsSet** esaminano e modificano le impostazioni modali, ovvero parametri globali che influiscono su ogni account nel database di sicurezza, ad esempio la lunghezza minima consentita per la password. Tutte le impostazioni modali possono essere modificate chiamando **NetUserModalsSet.** La maggior parte dei modali può essere modificata anche usando il **comando net accounts.** Le funzioni modali utente di gestione della rete non richiedono che il server abbia la sicurezza a livello di utente.

Le informazioni modali dell'utente sono disponibili ai livelli seguenti:

-   [**USER \_ MODALS \_ INFO \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_0)
-   [**USER \_ MODALS \_ INFO \_ 1**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1)
-   [**USER \_ MODALS \_ INFO \_ 2**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_2)
-   [**INFORMAZIONI \_ MODALI \_ UTENTE \_ 3**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_3)

I livelli di informazioni seguenti sono validi solo [**per NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset) e sostituiscono il modo precedente di passare un *parmnum* per impostare un campo specifico:

-   [**USER \_ MODALS \_ INFO \_ 1001**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1001)
-   [**USER \_ MODALS \_ INFO \_ 1002**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1002)
-   [**USER \_ MODALS \_ INFO \_ 1003**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1003)
-   [**USER \_ MODALS \_ INFO \_ 1004**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1004)
-   [**USER \_ MODALS \_ INFO \_ 1005**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1005)
-   [**USER \_ MODALS \_ INFO \_ 1006**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1006)
-   [**USER \_ MODALS \_ INFO \_ 1007**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1007)

Se si programma per Active Directory, è possibile chiamare determinati metodi ADSI (Active Directory Service Interface) per ottenere le stesse funzionalità che è possibile ottenere chiamando le funzioni modali dell'utente di gestione della rete. Per altre informazioni, vedere [**IADsDomain.**](/windows/desktop/api/iads/nn-iads-iadsdomain)

 

 