---
description: Un inserimento/espulsione è un pseudofile che risiede in memoria e si usano funzioni file standard per accedervi.
ms.assetid: 9a68905d-c235-4c72-bc71-1cccdf5cdadc
title: Informazioni su mailslot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bd83fc0d952577efdb149d4c7f25fffbab9784f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319617"
---
# <a name="about-mailslots"></a><span data-ttu-id="26df1-103">Informazioni su mailslot</span><span class="sxs-lookup"><span data-stu-id="26df1-103">About Mailslots</span></span>

<span data-ttu-id="26df1-104">Un inserimento/espulsione è un pseudofile che risiede in memoria e si usano funzioni file standard per accedervi.</span><span class="sxs-lookup"><span data-stu-id="26df1-104">A mailslot is a pseudofile that resides in memory, and you use standard file functions to access it.</span></span> <span data-ttu-id="26df1-105">I dati in un messaggio inserimento/espulsione possono essere in qualsiasi formato, ma non possono essere più grandi di 424 byte se inviati tra computer.</span><span class="sxs-lookup"><span data-stu-id="26df1-105">The data in a mailslot message can be in any form, but cannot be larger than 424 bytes when sent between computers.</span></span> <span data-ttu-id="26df1-106">A differenza dei file su disco, mailslot sono temporanei.</span><span class="sxs-lookup"><span data-stu-id="26df1-106">Unlike disk files, mailslots are temporary.</span></span> <span data-ttu-id="26df1-107">Quando tutti gli handle di un inserimento/espulsione vengono chiusi, il inserimento/espulsione e tutti i dati in esso contenuti vengono eliminati.</span><span class="sxs-lookup"><span data-stu-id="26df1-107">When all handles to a mailslot are closed, the mailslot and all the data it contains are deleted.</span></span>

<span data-ttu-id="26df1-108">Un *Server inserimento/espulsione* è un processo che crea e possiede un inserimento/espulsione.</span><span class="sxs-lookup"><span data-stu-id="26df1-108">A *mailslot server* is a process that creates and owns a mailslot.</span></span> <span data-ttu-id="26df1-109">Quando il server crea un inserimento/espulsione, riceve un handle inserimento/espulsione.</span><span class="sxs-lookup"><span data-stu-id="26df1-109">When the server creates a mailslot, it receives a mailslot handle.</span></span> <span data-ttu-id="26df1-110">Questo handle deve essere usato quando un processo legge i messaggi dal inserimento/espulsione.</span><span class="sxs-lookup"><span data-stu-id="26df1-110">This handle must be used when a process reads messages from the mailslot.</span></span> <span data-ttu-id="26df1-111">Solo il processo che crea un inserimento/espulsione o ha ottenuto l'handle da un altro meccanismo, ad esempio l'ereditarietà, può leggere da inserimento/espulsione.</span><span class="sxs-lookup"><span data-stu-id="26df1-111">Only the process that creates a mailslot or has obtained the handle by some other mechanism (such as inheritance) can read from the mailslot.</span></span> <span data-ttu-id="26df1-112">Tutte le mailslot sono locali per il processo che le crea.</span><span class="sxs-lookup"><span data-stu-id="26df1-112">All mailslots are local to the process that creates them.</span></span> <span data-ttu-id="26df1-113">Un processo non è in grado di creare un inserimento/espulsione remoto.</span><span class="sxs-lookup"><span data-stu-id="26df1-113">A process cannot create a remote mailslot.</span></span>

<span data-ttu-id="26df1-114">Un *client inserimento/espulsione* è un processo che scrive un messaggio in un inserimento/espulsione.</span><span class="sxs-lookup"><span data-stu-id="26df1-114">A *mailslot client* is a process that writes a message to a mailslot.</span></span> <span data-ttu-id="26df1-115">Tutti i processi che hanno il nome di un inserimento/espulsione possono inserire un messaggio.</span><span class="sxs-lookup"><span data-stu-id="26df1-115">Any process that has the name of a mailslot can put a message there.</span></span> <span data-ttu-id="26df1-116">I nuovi messaggi seguono tutti i messaggi esistenti in inserimento/espulsione.</span><span class="sxs-lookup"><span data-stu-id="26df1-116">New messages follow any existing messages in the mailslot.</span></span>

<span data-ttu-id="26df1-117">Mailslot è in grado di trasmettere messaggi all'interno di un dominio.</span><span class="sxs-lookup"><span data-stu-id="26df1-117">Mailslots can broadcast messages within a domain.</span></span> <span data-ttu-id="26df1-118">Se più processi in un dominio creano un inserimento/espulsione con lo stesso nome, ogni messaggio indirizzato a tale inserimento/espulsione e inviato al dominio viene ricevuto dai processi partecipanti.</span><span class="sxs-lookup"><span data-stu-id="26df1-118">If several processes in a domain each create a mailslot using the same name, every message that is addressed to that mailslot and sent to the domain is received by the participating processes.</span></span> <span data-ttu-id="26df1-119">Poiché un processo può controllare sia un handle inserimento/espulsione server che l'handle client recuperato quando viene aperto il inserimento/espulsione per un'operazione di scrittura, le applicazioni possono implementare facilmente una semplice funzione di passaggio dei messaggi all'interno di un dominio.</span><span class="sxs-lookup"><span data-stu-id="26df1-119">Because one process can control both a server mailslot handle and the client handle retrieved when the mailslot is opened for a write operation, applications can easily implement a simple message-passing facility within a domain.</span></span>

<span data-ttu-id="26df1-120">Per inviare messaggi di dimensioni superiori a 424 byte tra computer, utilizzare [Named Pipes](named-pipes.md) o [Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2) .</span><span class="sxs-lookup"><span data-stu-id="26df1-120">To send messages that are larger than 424 bytes between computers, use [named pipes](named-pipes.md) or [Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2) instead.</span></span>

## <a name="related-topics"></a><span data-ttu-id="26df1-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="26df1-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26df1-122">Nomi inserimento/espulsione</span><span class="sxs-lookup"><span data-stu-id="26df1-122">Mailslot Names</span></span>](mailslot-names.md)
</dt> <dt>

[<span data-ttu-id="26df1-123">Operazioni inserimento/espulsione</span><span class="sxs-lookup"><span data-stu-id="26df1-123">Mailslot Operations</span></span>](mailslot-operations.md)
</dt> </dl>

 

 
