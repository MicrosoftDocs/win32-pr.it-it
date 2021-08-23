---
description: Invece di inviare le chiavi di sessione crittografate a entrambe le entità, il KDC invia al client sia le copie del client che del server della chiave di sessione.
ms.assetid: 6b20ab30-2cd9-4f2e-a26b-316980c4bc78
title: Ticket di sessione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7b514abc76eabcbe70f00c1e879b9389c83ad333d7b5c10d4150478f03db6a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918070"
---
# <a name="session-tickets"></a>Ticket di sessione

Invece di inviare le chiavi di sessione crittografate a entrambe le entità, il [KDC](key-distribution-center.md) [](../secgloss/s-gly.md) invia al client sia le copie del client che del server della chiave di sessione. La copia della chiave di sessione del client viene crittografata con la chiave [*master*](../secgloss/m-gly.md) del client e pertanto non può essere decrittografata da altre entità. La copia della chiave di sessione del server è incorporata, insieme ai dati di autorizzazione relativi al client, in una struttura di dati denominata ticket. Il ticket è interamente crittografato con la chiave master del server e pertanto non può essere letto o modificato dal client o da qualsiasi altra entità che non ha accesso alla chiave master del server. È responsabilità del client archiviare il ticket in modo sicuro fino al contatto con il server.

> [!Note]  
> Il KDC fornisce solo un servizio di concessione di ticket. Il client e il server sono responsabili della protezione delle rispettive chiavi master.

 

Quando il client riceve la risposta del KDC, estrae il ticket e la propria copia della chiave di sessione, mettendoli entrambi da parte in una cache protetta. Per stabilire una sessione protetta con il server, invia al server un messaggio costituito dal ticket, [](authenticator-messages.md) ancora crittografato con la chiave master del server, e da un messaggio di autenticazione crittografato con la chiave di sessione. Insieme, il ticket e il messaggio dell'autenticatore sono le credenziali [*del*](../secgloss/c-gly.md) client per il server.

Quando il server riceve le credenziali da un client, decrittografa [](../secgloss/s-gly.md)il ticket con la chiave [*master,*](../secgloss/m-gly.md)estrae la chiave di sessione e usa la chiave di sessione per decrittografare il messaggio dell'autenticatore del client. Se tutto viene verificato, il server sa che le credenziali del client sono state rilasciate dal KDC, un'autorità attendibile. Per l'autenticazione reciproca, il server risponde crittografando il timestamp dal messaggio dell'autenticatore del client usando la chiave di sessione. Questo messaggio crittografato viene inviato al client. Il client decrittografa quindi il messaggio. Se il messaggio restituito corrisponde al timestamp nel messaggio dell'autenticatore originale, il server viene autenticato.

Come ulteriore vantaggio, il server non deve archiviare le chiavi di sessione che usa con i client. È responsabilità di ogni client gestire il ticket per il server nella cache dei ticket e presentare tale ticket ogni volta che accede al server. Ogni volta che il server riceve un ticket da un client, usa la chiave master per decrittografare il ticket ed estrarre la chiave della sessione. Quando il server non necessita più della chiave di sessione, la chiave viene eliminata.

Il client non deve accedere al KDC ogni volta che vuole accedere a questo server specifico. I ticket possono essere riutilizzati. Come precauzione contro la possibilità di furto di ticket, i ticket hanno una scadenza, specificata dal KDC nella struttura dei ticket. La durata della validità di un ticket dipende dai criteri Kerberos per l'area di autenticazione. In genere, i ticket sono buoni per non più di otto ore, circa la durata di una normale sessione [*di accesso*](../secgloss/l-gly.md). Quando l'utente di una workstation client si disconnette, la cache dei ticket client viene scaricata e tutti i ticket e le chiavi della sessione client vengono distrutti.

 

 
