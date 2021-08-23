---
description: Le funzioni di reindirizzamento dei dispositivi reindirizzano i dispositivi MS-DOS standard, le lettere di unità e le porte LPT. In questo modo le applicazioni in esecuzione nel sistema possono usare i dispositivi e accedere alla rete in modo completamente trasparente.
ms.assetid: a61ab1e6-dad9-4dc0-a908-f8440619f610
title: Device-Redirecting funzioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af4929052ed2691d6264791cac431e59faaacdb92f7f96bb610d99fdd4ded471
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008449"
---
# <a name="device-redirecting-functions"></a>Device-Redirecting funzioni

Le funzioni di reindirizzamento dei dispositivi reindirizzano i dispositivi MS-DOS standard, le lettere di unità e le porte LPT. In questo modo le applicazioni in esecuzione nel sistema possono usare i dispositivi e accedere alla rete in modo completamente trasparente.



| Funzione                                                         | Descrizione                                                                                                                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NPAddConnection**](/windows/desktop/api/Npapi/nf-npapi-npaddconnection)                       | Reindirizza o connette un dispositivo locale a una risorsa di rete.<br/>                                                                                                                              |
| [**NPAddConnection3**](/windows/desktop/api/Npapi/nf-npapi-npaddconnection3)                     | Esegue la stessa azione di [**NPAddConnection**](/windows/desktop/api/Npapi/nf-npapi-npaddconnection), ma consente all'utente di specificare quale finestra deve essere proprietaria di qualsiasi finestra di dialogo e come deve essere stabilita la connessione.<br/> |
| [**NPCancelConnection**](/windows/desktop/api/Npapi/nf-npapi-npcancelconnection)                 | Interrompe una connessione di rete. Le modifiche vengono memorizzate se un dispositivo viene disconnesso a meno che la connessione non sia una connessione senza dispositivo.<br/>                                                    |
| [**NPGetConnection**](/windows/desktop/api/Npapi/nf-npapi-npgetconnection)                       | Restituisce informazioni su una connessione.<br/>                                                                                                                                                  |
| [**NPGetConnection3**](/windows/desktop/api/Npapi/nf-npapi-npgetconnection3)                     | Restituisce informazioni su una connessione, anche se la connessione è attualmente disconnessa.<br/>                                                                                                |
| [**NPGetConnectionPerformance**](/windows/desktop/api/Npapi/nf-npapi-npgetconnectionperformance) | Restituisce informazioni sulle prestazioni relative a una connessione.<br/>                                                                                                                                      |
| [**NPGetUniversalName**](/windows/desktop/api/Npapi/nf-npapi-npgetuniversalname)                 | Restituisce il nome universale remoto o locale, nel formato specificato durante la chiamata di funzione.<br/>                                                                                            |



 

 

 




