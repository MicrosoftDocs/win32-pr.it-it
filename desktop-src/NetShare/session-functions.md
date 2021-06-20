---
description: Informazioni su funzioni di sessione nella gestione della condivisione di rete. Queste funzioni controllano le sessioni di rete stabilite tra workstation e server.
ms.assetid: 931455e3-1301-4a68-93c3-2674b3d4c491
title: Funzioni di sessione (Gestione condivisione di rete)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cdde451eb2942171569b24c36aae5d5742208e5
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409724"
---
# <a name="session-functions-network-share-management"></a>Funzioni di sessione (Gestione condivisione di rete)

Le funzioni della sessione di gestione di rete controllano le sessioni di rete stabilite tra workstation e server. Le funzioni richiedono l'avvio del servizio server nel server.

Le funzioni di sessione sono elencate di seguito.



| Funzione                                       | Descrizione                                                                                       |
|------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**NetSessionDel**](/windows/desktop/api/Lmshare/nf-lmshare-netsessiondel)         | Elimina le connessioni correnti tra una workstation e un server. termina la sessione di rete. |
| [**Enumerazione NetSessionEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netsessionenum)       | Restituisce informazioni su tutte le sessioni correnti stabilite per un server.                          |
| [**NetSessionGetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netsessiongetinfo) | Restituisce informazioni su una sessione specifica.                                                   |



 

Una *sessione* è un collegamento tra una workstation e un server. Una sessione viene stabilita la prima volta che una workstation effettua una connessione a una risorsa condivisa nel server. Fino al termine della sessione, tutte le altre connessioni tra la workstation e il server fanno parte della stessa sessione. Per terminare una sessione, un'applicazione sul server finale di una connessione chiama la [**funzione NetSessionDel.**](/windows/desktop/api/Lmshare/nf-lmshare-netsessiondel)

Le funzioni della sessione di gestione di rete gestiscono le informazioni in base all'utente con il *parametro username.* Poiché possono essere presenti più utenti per sessione, questo parametro è necessario per accedere alle informazioni specifiche dell'utente per la sessione.

Le funzioni di sessione sono disponibili a cinque livelli di informazioni:

<dl>

[**INFORMAZIONI \_ SESSIONE \_ 0**](/windows/desktop/api/Lmshare/ns-lmshare-session_info_0)  
[**INFORMAZIONI \_ SESSIONE \_ 1**](/windows/desktop/api/Lmshare/ns-lmshare-session_info_1)  
[**INFORMAZIONI \_ SESSIONE \_ 2**](/windows/desktop/api/Lmshare/ns-lmshare-session_info_2)  
[**INFORMAZIONI \_ SESSIONE \_ 10**](/windows/desktop/api/Lmshare/ns-lmshare-session_info_10)  
[**INFORMAZIONI \_ SESSIONE \_ 502**](/windows/desktop/api/Lmshare/ns-lmshare-session_info_502)  
</dl>

Se si programma per Active Directory, è possibile chiamare determinati metodi ADSI (Active Directory Service Interface) per ottenere le stesse funzionalità che è possibile ottenere chiamando le funzioni della sessione di gestione di rete. Per altre informazioni, vedere [**IADsSession**](/windows/desktop/api/iads/nn-iads-iadssession) e [**IADsFileServiceOperations.**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations)

 

 
