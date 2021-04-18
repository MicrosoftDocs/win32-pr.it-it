---
description: Le funzioni di sessione di gestione di rete controllano le sessioni di rete stabilite tra workstation e server. Per le funzioni è necessario che il servizio Server sia avviato nel server.
ms.assetid: 931455e3-1301-4a68-93c3-2674b3d4c491
title: Funzioni di sessione (gestione delle condivisioni di rete)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c672abd7c976cb9f83fa4f387dd40d175879dee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310776"
---
# <a name="session-functions-network-share-management"></a>Funzioni di sessione (gestione delle condivisioni di rete)

Le funzioni di sessione di gestione di rete controllano le sessioni di rete stabilite tra workstation e server. Per le funzioni è necessario che il servizio Server sia avviato nel server.

Le funzioni di sessione sono elencate di seguito.



| Funzione                                       | Descrizione                                                                                       |
|------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**NetSessionDel**](/windows/desktop/api/Lmshare/nf-lmshare-netsessiondel)         | Elimina le connessioni correnti tra una workstation e un server. termina la sessione di rete. |
| [**NetSessionEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netsessionenum)       | Restituisce informazioni su tutte le sessioni correnti stabilite per un server.                          |
| [**NetSessionGetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netsessiongetinfo) | Restituisce informazioni su una determinata sessione.                                                   |



 

Una *sessione* è un collegamento tra una workstation e un server. Viene stabilita una sessione la prima volta che una workstation stabilisce una connessione a una risorsa condivisa nel server. Fino al termine della sessione, tutte le altre connessioni tra la workstation e il server fanno parte della stessa sessione. Per terminare una sessione, un'applicazione sul lato server di una connessione chiama la funzione [**NetSessionDel**](/windows/desktop/api/Lmshare/nf-lmshare-netsessiondel) .

Le funzioni della sessione di gestione di rete gestiscono le informazioni in base ai singoli utenti con il parametro *username* . Poiché possono essere presenti più utenti per sessione, questo parametro è necessario per accedere alle informazioni specifiche dell'utente per la sessione.

Le funzioni di sessione sono disponibili a cinque livelli di informazioni:

<dl>

[**Informazioni sulla sessione \_ \_ 0**](/windows/desktop/api/Lmshare/ns-lmshare-session_info_0)  
[**\_Informazioni sessione \_ 1**](/windows/desktop/api/Lmshare/ns-lmshare-session_info_1)  
[**\_Informazioni sessione \_ 2**](/windows/desktop/api/Lmshare/ns-lmshare-session_info_2)  
[**Informazioni sulla sessione \_ \_ 10**](/windows/desktop/api/Lmshare/ns-lmshare-session_info_10)  
[**Informazioni sulla sessione \_ \_ 502**](/windows/desktop/api/Lmshare/ns-lmshare-session_info_502)  
</dl>

Se si sta programmando per Active Directory, è possibile chiamare determinati metodi di Active Directory Service Interface (ADSI) per ottenere la stessa funzionalità che è possibile ottenere chiamando le funzioni della sessione di gestione della rete. Per ulteriori informazioni, vedere [**IADsSession**](/windows/desktop/api/iads/nn-iads-iadssession) e [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).

 

 
