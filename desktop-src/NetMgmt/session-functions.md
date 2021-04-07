---
title: Funzioni di sessione (gestione della rete)
description: Le funzioni di sessione di gestione di rete controllano le sessioni di rete stabilite tra workstation e server. Per le funzioni è necessario che il servizio Server sia avviato nel server.
ms.assetid: ef912cd9-be5c-4202-89aa-e60f275e8938
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06b1e0236881b50f0363a6c872394cfe42f44748
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103873221"
---
# <a name="session-functions-network-management"></a>Funzioni di sessione (gestione della rete)

Le funzioni di sessione di gestione di rete controllano le sessioni di rete stabilite tra workstation e server. Per le funzioni è necessario che il servizio Server sia avviato nel server.

Le funzioni di sessione sono elencate di seguito.



| Funzione                                      | Descrizione                                                                                       |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**NetSessionDel**](/windows/desktop/api/lmshare/nf-lmshare-netsessiondel)         | Elimina le connessioni correnti tra una workstation e un server. termina la sessione di rete. |
| [**NetSessionEnum**](/windows/desktop/api/lmshare/nf-lmshare-netsessionenum)       | Restituisce informazioni su tutte le sessioni correnti stabilite per un server.                          |
| [**NetSessionGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsessiongetinfo) | Restituisce informazioni su una determinata sessione.                                                   |



 

Una *sessione* è un collegamento tra una workstation e un server. Viene stabilita una sessione la prima volta che una workstation stabilisce una connessione a una risorsa condivisa nel server. Fino al termine della sessione, tutte le altre connessioni tra la workstation e il server fanno parte della stessa sessione. Per terminare una sessione, un'applicazione sul lato server di una connessione chiama la funzione [**NetSessionDel**](/windows/desktop/api/lmshare/nf-lmshare-netsessiondel) .

Le funzioni della sessione di gestione di rete gestiscono le informazioni in base ai singoli utenti con il parametro *username* . Poiché possono essere presenti più utenti per sessione, questo parametro è necessario per accedere alle informazioni specifiche dell'utente per la sessione.

Le funzioni di sessione sono disponibili ai livelli di informazioni seguenti:

-   [**Informazioni sulla sessione \_ \_ 0**](/windows/desktop/api/lmshare/ns-lmshare-session_info_0)
-   [**\_Informazioni sessione \_ 1**](/windows/desktop/api/lmshare/ns-lmshare-session_info_1)
-   [**\_Informazioni sessione \_ 2**](/windows/desktop/api/lmshare/ns-lmshare-session_info_2)
-   [**Informazioni sulla sessione \_ \_ 10**](/windows/desktop/api/lmshare/ns-lmshare-session_info_10)
-   [**Informazioni sulla sessione \_ \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-session_info_502)

Se si sta programmando per Active Directory, è possibile chiamare determinati metodi di Active Directory Service Interface (ADSI) per ottenere la stessa funzionalità che è possibile ottenere chiamando le funzioni della sessione di gestione della rete. Per ulteriori informazioni, vedere [**IADsSession**](/windows/desktop/api/iads/nn-iads-iadssession) e [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).

 

 
