---
title: Pacchetti di richiesta BITS
description: Pacchetti di richiesta BITS
ms.assetid: 4d8fd5f3-7621-438f-926f-38ece7a52f52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6738f77477342f1329818ae7c2ffb5c010b074c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955219"
---
# <a name="bits-request-packets"></a><span data-ttu-id="b93c7-103">Pacchetti di richiesta BITS</span><span class="sxs-lookup"><span data-stu-id="b93c7-103">BITS Request Packets</span></span>

<span data-ttu-id="b93c7-104">I pacchetti di richiesta descrivono le richieste client.</span><span class="sxs-lookup"><span data-stu-id="b93c7-104">Request packets describe client requests.</span></span> <span data-ttu-id="b93c7-105">In un determinato momento può essere presente una sola richiesta in attesa; prima di inviare un'altra richiesta, è necessario ricevere un [ACK](bits-response-packets.md) per la richiesta corrente dal server.</span><span class="sxs-lookup"><span data-stu-id="b93c7-105">There can be only one outstanding request at any given time; you must receive an [Ack](bits-response-packets.md) for the current request from the server before sending another request.</span></span>

<span data-ttu-id="b93c7-106">La tabella seguente elenca i pacchetti di richiesta inviati al server BITS per i processi di caricamento e caricamento-risposta.</span><span class="sxs-lookup"><span data-stu-id="b93c7-106">The following table lists the request packets sent to the BITS server for upload and upload-reply jobs.</span></span> <span data-ttu-id="b93c7-107">La tabella elenca i pacchetti nella sequenza tipica che vengono inviati al server.</span><span class="sxs-lookup"><span data-stu-id="b93c7-107">The table lists the packets in the typical sequence they are sent to the server.</span></span>



| <span data-ttu-id="b93c7-108">Richiedi pacchetto</span><span class="sxs-lookup"><span data-stu-id="b93c7-108">Request packet</span></span>                       | <span data-ttu-id="b93c7-109">Scopo</span><span class="sxs-lookup"><span data-stu-id="b93c7-109">Purpose</span></span>                                                                                                                                                        |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b93c7-110">Ping</span><span class="sxs-lookup"><span data-stu-id="b93c7-110">Ping</span></span>](ping.md)                     | <span data-ttu-id="b93c7-111">Stabilisce una connessione e negozia la sicurezza con il server.</span><span class="sxs-lookup"><span data-stu-id="b93c7-111">Establishes a connection and negotiates security with the server.</span></span>                                                                                              |
| [<span data-ttu-id="b93c7-112">Creazione sessione</span><span class="sxs-lookup"><span data-stu-id="b93c7-112">Create-Session</span></span>](create-session.md) | <span data-ttu-id="b93c7-113">Richiede una sessione di caricamento con il server BITS.</span><span class="sxs-lookup"><span data-stu-id="b93c7-113">Requests an upload session with the BITS server.</span></span>                                                                                                               |
| [<span data-ttu-id="b93c7-114">Frammento</span><span class="sxs-lookup"><span data-stu-id="b93c7-114">Fragment</span></span>](fragment.md)             | <span data-ttu-id="b93c7-115">Invia un frammento del file al server BITS.</span><span class="sxs-lookup"><span data-stu-id="b93c7-115">Sends a fragment of the file to the BITS server.</span></span> <span data-ttu-id="b93c7-116">Il numero di richieste di frammenti inviate dipende dalle dimensioni del frammento scelte e dalle dimensioni del file di caricamento.</span><span class="sxs-lookup"><span data-stu-id="b93c7-116">The number of fragment requests sent depends on the fragment size you choose and the size of the upload file.</span></span> |
| [<span data-ttu-id="b93c7-117">Chiudi sessione</span><span class="sxs-lookup"><span data-stu-id="b93c7-117">Close-Session</span></span>](close-session.md)   | <span data-ttu-id="b93c7-118">Termina la sessione di caricamento dei file con il server BITS.</span><span class="sxs-lookup"><span data-stu-id="b93c7-118">Ends the file upload session with the BITS server.</span></span>                                                                                                             |
| [<span data-ttu-id="b93c7-119">Annulla-sessione</span><span class="sxs-lookup"><span data-stu-id="b93c7-119">Cancel-Session</span></span>](cancel-session.md) | <span data-ttu-id="b93c7-120">Termina la sessione di caricamento dei file con il server BITS.</span><span class="sxs-lookup"><span data-stu-id="b93c7-120">Ends the file upload session with the BITS server.</span></span> <span data-ttu-id="b93c7-121">In genere, si invia il pacchetto di Cancel-Session se l'utente ha annullato il processo.</span><span class="sxs-lookup"><span data-stu-id="b93c7-121">Typically, you send the Cancel-Session packet if the user canceled the job.</span></span>                                 |



 

<span data-ttu-id="b93c7-122">Il pacchetto ping è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b93c7-122">The Ping packet is optional.</span></span> <span data-ttu-id="b93c7-123">Anziché inviare un pacchetto ping, è possibile utilizzare il pacchetto Create-Session per stabilire una connessione e negoziare la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="b93c7-123">Instead of sending a Ping packet, you can use the Create-Session packet to establish a connection and negotiate security.</span></span> <span data-ttu-id="b93c7-124">Tuttavia, è più efficiente usare il pacchetto ping a questo scopo.</span><span class="sxs-lookup"><span data-stu-id="b93c7-124">However, it is more efficient to use the Ping packet for this purpose.</span></span>

 

 




