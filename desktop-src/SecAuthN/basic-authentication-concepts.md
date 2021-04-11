---
description: In un modello di applicazione client/server, i client sono programmi che agiscono per conto di utenti che hanno bisogno di qualcosa.
ms.assetid: c3e38cd3-3749-4384-80ff-0551acfe1eec
title: Concetti di base sull'autenticazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723cf42913906435c8dbc3c41950da8db8ece0ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130430"
---
# <a name="basic-authentication-concepts"></a><span data-ttu-id="59a64-103">Concetti di base sull'autenticazione</span><span class="sxs-lookup"><span data-stu-id="59a64-103">Basic Authentication Concepts</span></span>

<span data-ttu-id="59a64-104">In un modello di applicazione client/server, i client sono programmi che agiscono per conto di utenti che hanno bisogno di qualcosa.</span><span class="sxs-lookup"><span data-stu-id="59a64-104">In a client/server application model, clients are programs acting on behalf of users who need something done.</span></span> <span data-ttu-id="59a64-105">Questo potrebbe essere l'apertura e l'utilizzo di un file, l'accesso a una cassetta postale, l'esecuzione di query su un database o la stampa di un documento.</span><span class="sxs-lookup"><span data-stu-id="59a64-105">This might be opening and using a file, accessing a mailbox, querying a database, or printing a document.</span></span> <span data-ttu-id="59a64-106">I server sono programmi che forniscono servizi ai client quali archiviazione file, gestione della posta elettronica, elaborazione di query e spooling di stampa.</span><span class="sxs-lookup"><span data-stu-id="59a64-106">Servers are programs providing services to clients such as file storage, mail handling, query processing, and print spooling.</span></span> <span data-ttu-id="59a64-107">I client avviano un'azione, i server rispondono.</span><span class="sxs-lookup"><span data-stu-id="59a64-107">Clients initiate action, servers respond.</span></span> <span data-ttu-id="59a64-108">In genere, un server è in ascolto su una porta di comunicazione in attesa che i client si connettano e chiedano il servizio.</span><span class="sxs-lookup"><span data-stu-id="59a64-108">Typically, a server listens at a communications port waiting for clients to connect and ask for service.</span></span>

<span data-ttu-id="59a64-109">Nel modello di protocollo Kerberos ogni connessione al client/server inizia con l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="59a64-109">In the Kerberos protocol model, every client/server connection begins with authentication.</span></span> <span data-ttu-id="59a64-110">Il client e il server effettuano a loro volta una sequenza di azioni progettata per indicare alla parte in ciascuna estremità della connessione che la parte nell'altra estremità è autentica.</span><span class="sxs-lookup"><span data-stu-id="59a64-110">Client and server, in turn, step through a sequence of actions designed to verify to the party on each end of the connection that the party on the other end is genuine.</span></span> <span data-ttu-id="59a64-111">Se l'autenticazione ha esito positivo, viene completata l'installazione della sessione e viene stabilita una sessione client/server sicura.</span><span class="sxs-lookup"><span data-stu-id="59a64-111">If authentication is successful, session setup completes and a secure client/server session is established.</span></span>

<span data-ttu-id="59a64-112">Il protocollo Kerberos si avvale di:</span><span class="sxs-lookup"><span data-stu-id="59a64-112">The Kerberos protocol makes use of:</span></span>

-   [<span data-ttu-id="59a64-113">Autenticazione della chiave</span><span class="sxs-lookup"><span data-stu-id="59a64-113">Key authentication</span></span>](key-authentication.md)
-   [<span data-ttu-id="59a64-114">Messaggi di autenticazione</span><span class="sxs-lookup"><span data-stu-id="59a64-114">Authenticator messages</span></span>](authenticator-messages.md)
-   [<span data-ttu-id="59a64-115">Distribuzione delle chiavi</span><span class="sxs-lookup"><span data-stu-id="59a64-115">Key distribution</span></span>](key-distribution.md)
-   [<span data-ttu-id="59a64-116">Ticket di sessione</span><span class="sxs-lookup"><span data-stu-id="59a64-116">Session tickets</span></span>](session-tickets.md)
-   [<span data-ttu-id="59a64-117">Ticket di concessione ticket</span><span class="sxs-lookup"><span data-stu-id="59a64-117">Ticket-granting tickets</span></span>](ticket-granting-tickets.md)

 

 



