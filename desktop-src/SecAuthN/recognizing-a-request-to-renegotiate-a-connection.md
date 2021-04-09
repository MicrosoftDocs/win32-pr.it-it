---
description: La funzione DecryptMessage (generale) intercetta le richieste di rinegoziazione provenienti dal mittente del messaggio. Invia una notifica all'applicazione decrittografando i dati del messaggio e restituendo il valore SEC i \_ \_ rinegoziare.
ms.assetid: 036a93dc-7f52-42f8-945d-7f654289ef63
title: Riconoscimento di una richiesta di rinegoziazione di una connessione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d8ae8083c59485b8b7c917fe03893fa363f5a8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049978"
---
# <a name="recognizing-a-request-to-renegotiate-a-connection"></a><span data-ttu-id="b0316-104">Riconoscimento di una richiesta di rinegoziazione di una connessione</span><span class="sxs-lookup"><span data-stu-id="b0316-104">Recognizing a Request to Renegotiate a Connection</span></span>

<span data-ttu-id="b0316-105">La funzione [**DecryptMessage (generale)**](decryptmessage--general.md) intercetta le richieste di rinegoziazione provenienti dal mittente del messaggio.</span><span class="sxs-lookup"><span data-stu-id="b0316-105">The [**DecryptMessage (General)**](decryptmessage--general.md) function traps requests for renegotiation coming from the message sender.</span></span> <span data-ttu-id="b0316-106">Invia una notifica all'applicazione decrittografando i dati del messaggio e restituendo il valore SEC i \_ \_ rinegoziare.</span><span class="sxs-lookup"><span data-stu-id="b0316-106">It notifies your application by decrypting the message data and returning the SEC\_I\_RENEGOTIATE value.</span></span>

<span data-ttu-id="b0316-107">L'applicazione deve gestire tali richieste chiamando [**AcceptSecurityContext (General)**](acceptsecuritycontext--general.md) (Server) o [**InitializeSecurityContext (generale)**](initializesecuritycontext--general.md) (client) e passando il contenuto di SECBUFFER_EXTRA restituito da DecryptMessage nel SECBUFFER_TOKEN.</span><span class="sxs-lookup"><span data-stu-id="b0316-107">Your application must handle such requests by calling [**AcceptSecurityContext (General)**](acceptsecuritycontext--general.md) (servers) or [**InitializeSecurityContext (General)**](initializesecuritycontext--general.md) (clients) and passing the contents of SECBUFFER_EXTRA returned from DecryptMessage in the SECBUFFER_TOKEN.</span></span> <span data-ttu-id="b0316-108">Dopo che la chiamata iniziale restituisce un valore, procedere come se l'applicazione creasse una nuova connessione.</span><span class="sxs-lookup"><span data-stu-id="b0316-108">After this initial call returns a value, proceed as though your application were creating a new connection.</span></span>

 

 



