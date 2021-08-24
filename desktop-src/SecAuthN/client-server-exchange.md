---
description: Client/Server Exchange
ms.assetid: 2449c4b3-720d-4b84-b3cf-fcc4abd05d33
title: Client/Server Exchange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb2401d3cf2bb59586e608bc7566c13009869d2874a1532b659f70c6c4e09e4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141174"
---
# <a name="clientserver-exchange"></a>Client/Server Exchange

Dopo che un utente ha un ticket per un server, il client della workstation può stabilire una sessione di comunicazione protetta con tale server.

**Per stabilire una sessione di comunicazione protetta con un server**

1.  Il client invia al server un messaggio di tipo KRB \_ AP \_ REQ (Richiesta applicazione Kerberos). Questo messaggio contiene un messaggio di autenticazione crittografato con la chiave inviata dal [*Centro distribuzione chiavi*](/windows/desktop/SecGloss/k-gly) (KDC) per la sessione con il server, il ticket per le sessioni con il server e un flag che indica se il client richiede l'autenticazione reciproca. L'impostazione del flag che richiede l'autenticazione reciproca è una delle opzioni disponibili nella configurazione di [*Kerberos.*](/windows/desktop/SecGloss/k-gly) All'utente non viene mai chiesto se usare l'autenticazione reciproca.
2.  Il server riceve l'AP REQ KRB, decrittografa il ticket ed estrae i dati di autorizzazione \_ \_ dell'utente e la [*chiave di sessione*](/windows/desktop/SecGloss/s-gly).
3.  Il server usa la chiave di sessione del ticket per decrittografare il messaggio dell'autenticatore dell'utente e valuta il timestamp all'interno.
4.  Se il messaggio dell'autenticatore è valido, il server controlla il flag di autenticazione reciproca nella richiesta del client.
5.  Se il flag di autenticazione reciproca è impostato, il server usa la chiave di sessione per crittografare l'ora dal messaggio dell'autenticatore dell'utente e restituisce il risultato in un messaggio di tipo KRB \_ AP \_ REP (Kerberos Application Reply).
6.  Quando il client riceve il punto di accesso KRB, decrittografa il messaggio dell'autenticatore del server con la chiave di sessione che condivide con il server e confronta l'ora inviata dal servizio con l'ora nel messaggio originale \_ \_ dell'autenticatore. Se corrispondono, il client ha la certezza che il servizio è originale e la connessione continua.

 

 
