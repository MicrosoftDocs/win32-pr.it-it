---
description: Le funzioni di reindirizzamento dispositivi rimandano i dispositivi MS-DOS standard, le lettere di unità e le porte LPT. Questo consente alle applicazioni in esecuzione nel sistema di usare i dispositivi e accedere alla rete in modo completamente trasparente.
ms.assetid: a61ab1e6-dad9-4dc0-a908-f8440619f610
title: Funzioni Device-Redirecting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 577f8d108b6bfdeb01f786478cd736e6c84cc83d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225904"
---
# <a name="device-redirecting-functions"></a>Funzioni Device-Redirecting

Le funzioni di reindirizzamento dispositivi rimandano i dispositivi MS-DOS standard, le lettere di unità e le porte LPT. Questo consente alle applicazioni in esecuzione nel sistema di usare i dispositivi e accedere alla rete in modo completamente trasparente.



| Funzione                                                         | Descrizione                                                                                                                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NPAddConnection**](/windows/desktop/api/Npapi/nf-npapi-npaddconnection)                       | Reindirizza o connette un dispositivo locale a una risorsa di rete.<br/>                                                                                                                              |
| [**NPAddConnection3**](/windows/desktop/api/Npapi/nf-npapi-npaddconnection3)                     | Esegue la stessa azione di [**NPAddConnection**](/windows/desktop/api/Npapi/nf-npapi-npaddconnection), ma consente all'utente di specificare quale finestra deve essere proprietaria di tutte le finestre di dialogo e il modo in cui deve essere stabilita la connessione.<br/> |
| [**NPCancelConnection**](/windows/desktop/api/Npapi/nf-npapi-npcancelconnection)                 | Interrompe una connessione di rete. Le modifiche vengono memorizzate se un dispositivo viene disconnesso a meno che non si tratti di una connessione senza dispositivo.<br/>                                                    |
| [**NPGetConnection**](/windows/desktop/api/Npapi/nf-npapi-npgetconnection)                       | Restituisce informazioni su una connessione.<br/>                                                                                                                                                  |
| [**NPGetConnection3**](/windows/desktop/api/Npapi/nf-npapi-npgetconnection3)                     | Restituisce informazioni su una connessione, anche se la connessione è attualmente disconnessa.<br/>                                                                                                |
| [**NPGetConnectionPerformance**](/windows/desktop/api/Npapi/nf-npapi-npgetconnectionperformance) | Restituisce informazioni sulle prestazioni relative a una connessione.<br/>                                                                                                                                      |
| [**NPGetUniversalName**](/windows/desktop/api/Npapi/nf-npapi-npgetuniversalname)                 | Restituisce il nome universale remoto o locale, nel formato specificato durante la chiamata di funzione.<br/>                                                                                            |



 

 

 




