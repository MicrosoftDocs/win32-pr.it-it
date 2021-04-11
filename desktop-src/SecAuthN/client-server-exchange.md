---
description: Exchange client/server
ms.assetid: 2449c4b3-720d-4b84-b3cf-fcc4abd05d33
title: Exchange client/server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6274705ef6719c846f0551f90fca8790ba89f2e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131059"
---
# <a name="clientserver-exchange"></a>Exchange client/server

Dopo che un utente ha effettuato un ticket per un server, il client workstation può stabilire una sessione di comunicazione protetta con tale server.

**Per stabilire una sessione di comunicazione protetta con un server**

1.  Il client invia al server un messaggio di tipo KRB \_ AP \_ req (richiesta dell'applicazione Kerberos). Questo messaggio contiene un messaggio di autenticazione crittografato con la chiave inviata dal [*centro distribuzione chiavi*](/windows/desktop/SecGloss/k-gly) (KDC) per la sessione con il server, il ticket per le sessioni con il server e un flag che indica se il client richiede l'autenticazione reciproca. L'impostazione del flag che richiede l'autenticazione reciproca è una delle opzioni disponibili nella pagina relativa alla configurazione di [*Kerberos*](/windows/desktop/SecGloss/k-gly). All'utente non viene mai chiesto se usare l'autenticazione reciproca.
2.  Il server riceve KRB \_ AP \_ req, decrittografa il ticket ed estrae i dati di autorizzazione dell'utente e la [*chiave della sessione*](/windows/desktop/SecGloss/s-gly).
3.  Il server usa la chiave della sessione dal ticket per decrittografare il messaggio di autenticazione dell'utente e valuta il timestamp all'interno.
4.  Se il messaggio di autenticazione è valido, il server verifica il flag di autenticazione reciproca nella richiesta del client.
5.  Se viene impostato il flag di autenticazione reciproca, il server utilizza la chiave di sessione per crittografare l'ora dal messaggio di autenticazione dell'utente e restituisce il risultato in un messaggio di tipo KRB \_ AP \_ Rep (risposta dell'applicazione Kerberos).
6.  Quando il client riceve KRB \_ AP \_ Rep, decrittografa il messaggio di autenticazione del server con la chiave di sessione che condivide con il server e confronta il tempo inviato dal servizio con il tempo nel messaggio originale dell'autenticatore. Se corrispondono, il client ha la certezza che il servizio sia autentico e che la connessione proceda.

 

 
