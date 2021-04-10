---
title: Funzioni modali utente
description: Le funzioni modali utente Gestione rete ottengono e impostano parametri a livello di sistema correlati al comportamento del sistema di sicurezza.
ms.assetid: e655b9f6-2808-4bd4-998c-c8a2e980920b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c65595f78a412196b9fd54030ec1ac1f1fb8ae59
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963390"
---
# <a name="user-modal-functions"></a>Funzioni modali utente

Le funzioni modali utente Gestione rete ottengono e impostano parametri a livello di sistema correlati al comportamento del sistema di sicurezza.

Le funzioni modali utente sono elencate di seguito.



| Funzione                                     | Descrizione                                                                                                                                                                                             |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetUserModalsGet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget) | Restituisce informazioni globali per tutti gli utenti e i gruppi globali nel database di sicurezza, ovvero il database di gestione degli account di sicurezza (SAM) o, nel caso di controller di dominio, il Active Directory. |
| [**NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset) | Imposta le informazioni globali per tutti gli utenti e i gruppi globali nel database di sicurezza.                                                                                                                       |



 

Le funzioni **NetUserModalsGet** e **NetUserModalsSet** esaminano e modificano le impostazioni modali, che sono parametri globali che interessano ogni account nel database di sicurezza, ad esempio la lunghezza minima consentita per la password. Tutte le impostazioni modali possono essere modificate chiamando **NetUserModalsSet**. La maggior parte dei modale può essere modificata anche usando il comando **net accounts** . Per le funzioni modali utente di gestione di rete non è necessario che il server disponga di sicurezza a livello di utente.

Le informazioni modali dell'utente sono disponibili ai livelli seguenti:

-   [**\_Informazioni sulle modalità \_ utente \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_0)
-   [**\_Informazioni sulle modalità \_ utente \_ 1**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1)
-   [**\_Informazioni sulle modalità \_ utente \_ 2**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_2)
-   [**\_Informazioni sulle modalità \_ utente \_ 3**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_3)

I livelli di informazioni seguenti sono validi solo per [**NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset) e sostituiscono il modo precedente di passare un *Parmnum* per impostare un campo specifico:

-   [**\_Informazioni sulle modalità \_ utente \_ 1001**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1001)
-   [**\_Informazioni sulle modalità \_ utente \_ 1002**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1002)
-   [**\_Informazioni sulle modalità \_ utente \_ 1003**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1003)
-   [**\_Informazioni sulle modalità \_ utente \_ 1004**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1004)
-   [**\_Informazioni sulle modalità \_ utente \_ 1005**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1005)
-   [**\_Informazioni sulle modalità \_ utente \_ 1006**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1006)
-   [**\_Informazioni sulle modalità \_ utente \_ 1007**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1007)

Se si sta programmando per Active Directory, è possibile chiamare determinati metodi di Active Directory Service Interface (ADSI) per ottenere la stessa funzionalità che è possibile ottenere chiamando le funzioni modali dell'utente di gestione della rete. Per ulteriori informazioni, vedere [**IADsDomain**](/windows/desktop/api/iads/nn-iads-iadsdomain).

 

 