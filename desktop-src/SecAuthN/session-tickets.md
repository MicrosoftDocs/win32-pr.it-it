---
description: Anziché inviare le chiavi della sessione crittografata a entrambe le entità, il KDC invia al client sia le copie del client che del server della chiave della sessione.
ms.assetid: 6b20ab30-2cd9-4f2e-a26b-316980c4bc78
title: Ticket di sessione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 762223311dd71f8bded5e021372d3a281f711eda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311598"
---
# <a name="session-tickets"></a>Ticket di sessione

Anziché inviare le chiavi della sessione crittografata a entrambe le entità, il [KDC](key-distribution-center.md) invia al client sia le copie del client che del server della [*chiave della sessione*](../secgloss/s-gly.md) . La copia del client della chiave di sessione viene crittografata con la [*chiave master*](../secgloss/m-gly.md) del client e pertanto non può essere decrittografata da nessun'altra entità. La copia del server della chiave della sessione è incorporata, insieme ai dati di autorizzazione relativi al client, in una struttura di dati denominata ticket. Il ticket è interamente crittografato con la chiave master del server e pertanto non può essere letto o modificato dal client o da qualsiasi altra entità che non dispone dell'accesso alla chiave master del server. È responsabilità del client archiviare il ticket in modo sicuro fino al contatto con il server.

> [!Note]  
> Il KDC fornisce solo un servizio di concessione ticket. Il client e il server sono responsabili delle rispettive chiavi master protette.

 

Quando il client riceve la risposta del KDC, estrae il ticket e la relativa copia della chiave della sessione, mettendolo a parte in una cache sicura. Per stabilire una sessione protetta con il server, viene inviato al server un messaggio costituito dal ticket, ancora crittografato con la chiave master del server e un [messaggio di autenticazione](authenticator-messages.md) crittografato con la chiave della sessione. Insieme, il messaggio ticket e Authenticator sono le [*credenziali*](../secgloss/c-gly.md) del client per il server.

Quando il server riceve le credenziali da un client, decrittografa il ticket con la relativa [*chiave master*](../secgloss/m-gly.md), estrae la [*chiave della sessione*](../secgloss/s-gly.md)e usa la chiave della sessione per decrittografare il messaggio di autenticazione del client. Se tutto viene verificato, il server sa che le credenziali del client sono state rilasciate dal KDC, un'autorità attendibile. Per l'autenticazione reciproca, il server risponde crittografando il timestamp dal messaggio di autenticazione del client usando la chiave della sessione. Questo messaggio crittografato viene inviato al client. Il client decrittografa quindi il messaggio. Se il messaggio restituito è uguale al timestamp del messaggio di autenticazione originale, il server viene autenticato.

Come ulteriore vantaggio, il server non deve archiviare le chiavi di sessione che usa con i relativi client. Ogni cliente ha la responsabilità di gestire il ticket per il server nella propria cache dei ticket e di presentare il ticket ogni volta che accede al server. Ogni volta che il server riceve un ticket da un client, usa la chiave master per decrittografare il ticket ed estrarre la chiave della sessione. Quando il server non necessita più della chiave della sessione, la chiave viene eliminata.

Il client non deve accedere al KDC ogni volta che desidera accedere a questo particolare server. I ticket possono essere riutilizzati. Come precauzione contro la possibilità di furto di ticket, i ticket hanno una data di scadenza, specificata dal KDC nella struttura del ticket. Il periodo di validità di un ticket dipende dal criterio Kerberos per l'area di autenticazione. In genere, i ticket sono validi per non più di otto ore, per la durata di una normale [*sessione di accesso*](../secgloss/l-gly.md). Quando l'utente a una workstation client si disconnette, la cache dei ticket client viene scaricata e tutti i ticket e le chiavi della sessione client vengono eliminati definitivamente.

 

 
