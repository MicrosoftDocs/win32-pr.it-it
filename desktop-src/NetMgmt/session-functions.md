---
title: Funzioni di sessione (Gestione rete)
description: Esaminare le funzioni di sessione, che sono un gruppo di funzioni di gestione di rete. Queste funzioni controllano le sessioni di rete stabilite tra workstation e server.
ms.assetid: ef912cd9-be5c-4202-89aa-e60f275e8938
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbaa2362db5d6583c44cff73fb2831f9dbd7b6f164d5a8df1dce07827d6144d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911441"
---
# <a name="session-functions-network-management"></a>Funzioni di sessione (Gestione rete)

Le funzioni di sessione di gestione di rete controllano le sessioni di rete stabilite tra workstation e server. Le funzioni richiedono l'avvio del servizio server nel server.

Le funzioni di sessione sono elencate di seguito.



| Funzione                                      | Descrizione                                                                                       |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**NetSessionDel**](/windows/desktop/api/lmshare/nf-lmshare-netsessiondel)         | Elimina le connessioni correnti tra una workstation e un server. termina la sessione di rete. |
| [**NetSessionEnum**](/windows/desktop/api/lmshare/nf-lmshare-netsessionenum)       | Restituisce informazioni su tutte le sessioni correnti stabilite per un server.                          |
| [**NetSessionGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsessiongetinfo) | Restituisce informazioni su una sessione specifica.                                                   |



 

Una *sessione* è un collegamento tra una workstation e un server. Una sessione viene stabilita la prima volta che una workstation esegue una connessione a una risorsa condivisa nel server. Fino al termine della sessione, tutte le altre connessioni tra la workstation e il server fanno parte della stessa sessione. Per terminare una sessione, un'applicazione sul server finale di una connessione chiama la [**funzione NetSessionDel.**](/windows/desktop/api/lmshare/nf-lmshare-netsessiondel)

Le funzioni della sessione di gestione di rete gestiscono le informazioni in base all'utente con il *parametro username.* Poiché possono essere presenti più utenti per sessione, questo parametro è necessario per accedere alle informazioni specifiche dell'utente per la sessione.

Le funzioni di sessione sono disponibili ai livelli di informazioni seguenti:

-   [**INFORMAZIONI \_ SESSIONE \_ 0**](/windows/desktop/api/lmshare/ns-lmshare-session_info_0)
-   [**INFORMAZIONI \_ SULLA \_ SESSIONE 1**](/windows/desktop/api/lmshare/ns-lmshare-session_info_1)
-   [**INFORMAZIONI \_ SULLA \_ SESSIONE 2**](/windows/desktop/api/lmshare/ns-lmshare-session_info_2)
-   [**INFORMAZIONI \_ SULLA \_ SESSIONE 10**](/windows/desktop/api/lmshare/ns-lmshare-session_info_10)
-   [**INFORMAZIONI \_ SULLA \_ SESSIONE 502**](/windows/desktop/api/lmshare/ns-lmshare-session_info_502)

Se si sta programmando per Active Directory, è possibile chiamare determinati metodi ADSI (Active Directory Service Interface) per ottenere le stesse funzionalità che è possibile ottenere chiamando le funzioni della sessione di gestione di rete. Per altre informazioni, vedere [**IADsSession**](/windows/desktop/api/iads/nn-iads-iadssession) e [**IADsFileServiceOperations.**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations)

 

 
