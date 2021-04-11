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
# <a name="clientserver-exchange"></a><span data-ttu-id="f3c6f-103">Exchange client/server</span><span class="sxs-lookup"><span data-stu-id="f3c6f-103">Client/Server Exchange</span></span>

<span data-ttu-id="f3c6f-104">Dopo che un utente ha effettuato un ticket per un server, il client workstation può stabilire una sessione di comunicazione protetta con tale server.</span><span class="sxs-lookup"><span data-stu-id="f3c6f-104">After a user has a ticket to a server, the workstation client can establish a secure communications session with that server.</span></span>

<span data-ttu-id="f3c6f-105">**Per stabilire una sessione di comunicazione protetta con un server**</span><span class="sxs-lookup"><span data-stu-id="f3c6f-105">**To establish a secure communications session with a server**</span></span>

1.  <span data-ttu-id="f3c6f-106">Il client invia al server un messaggio di tipo KRB \_ AP \_ req (richiesta dell'applicazione Kerberos).</span><span class="sxs-lookup"><span data-stu-id="f3c6f-106">The client sends the server a message of type KRB\_AP\_REQ (Kerberos Application Request).</span></span> <span data-ttu-id="f3c6f-107">Questo messaggio contiene un messaggio di autenticazione crittografato con la chiave inviata dal [*centro distribuzione chiavi*](/windows/desktop/SecGloss/k-gly) (KDC) per la sessione con il server, il ticket per le sessioni con il server e un flag che indica se il client richiede l'autenticazione reciproca.</span><span class="sxs-lookup"><span data-stu-id="f3c6f-107">This message contains an authenticator message that is encrypted with the key sent by the [*Key Distribution Center*](/windows/desktop/SecGloss/k-gly) (KDC) for the session with the server, the ticket for sessions with the server, and a flag that indicates whether the client requests mutual authentication.</span></span> <span data-ttu-id="f3c6f-108">L'impostazione del flag che richiede l'autenticazione reciproca è una delle opzioni disponibili nella pagina relativa alla configurazione di [*Kerberos*](/windows/desktop/SecGloss/k-gly).</span><span class="sxs-lookup"><span data-stu-id="f3c6f-108">Setting the flag that requests mutual authentication is one of the options in configuring [*Kerberos*](/windows/desktop/SecGloss/k-gly).</span></span> <span data-ttu-id="f3c6f-109">All'utente non viene mai chiesto se usare l'autenticazione reciproca.</span><span class="sxs-lookup"><span data-stu-id="f3c6f-109">The user is never asked whether mutual authentication should be used.</span></span>
2.  <span data-ttu-id="f3c6f-110">Il server riceve KRB \_ AP \_ req, decrittografa il ticket ed estrae i dati di autorizzazione dell'utente e la [*chiave della sessione*](/windows/desktop/SecGloss/s-gly).</span><span class="sxs-lookup"><span data-stu-id="f3c6f-110">The server receives KRB\_AP\_REQ, decrypts the ticket, and extracts the user's authorization data and the [*session key*](/windows/desktop/SecGloss/s-gly).</span></span>
3.  <span data-ttu-id="f3c6f-111">Il server usa la chiave della sessione dal ticket per decrittografare il messaggio di autenticazione dell'utente e valuta il timestamp all'interno.</span><span class="sxs-lookup"><span data-stu-id="f3c6f-111">The server uses the session key from the ticket to decrypt the user's authenticator message and evaluates the time stamp inside.</span></span>
4.  <span data-ttu-id="f3c6f-112">Se il messaggio di autenticazione è valido, il server verifica il flag di autenticazione reciproca nella richiesta del client.</span><span class="sxs-lookup"><span data-stu-id="f3c6f-112">If the authenticator message is valid, the server checks the mutual authentication flag in the client's request.</span></span>
5.  <span data-ttu-id="f3c6f-113">Se viene impostato il flag di autenticazione reciproca, il server utilizza la chiave di sessione per crittografare l'ora dal messaggio di autenticazione dell'utente e restituisce il risultato in un messaggio di tipo KRB \_ AP \_ Rep (risposta dell'applicazione Kerberos).</span><span class="sxs-lookup"><span data-stu-id="f3c6f-113">If the mutual authentication flag is set, the server uses the session key to encrypt the time from the user's authenticator message and returns the result in a message of type KRB\_AP\_REP (Kerberos Application Reply).</span></span>
6.  <span data-ttu-id="f3c6f-114">Quando il client riceve KRB \_ AP \_ Rep, decrittografa il messaggio di autenticazione del server con la chiave di sessione che condivide con il server e confronta il tempo inviato dal servizio con il tempo nel messaggio originale dell'autenticatore.</span><span class="sxs-lookup"><span data-stu-id="f3c6f-114">When the client receives KRB\_AP\_REP, it decrypts the server's authenticator message with the session key it shares with the server and compares the time sent back by the service with the time in its original authenticator message.</span></span> <span data-ttu-id="f3c6f-115">Se corrispondono, il client ha la certezza che il servizio sia autentico e che la connessione proceda.</span><span class="sxs-lookup"><span data-stu-id="f3c6f-115">If they match, the client is assured that the service is genuine, and the connection proceeds.</span></span>

 

 
