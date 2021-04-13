---
description: Descrive il processo di un'operazione di I/O di rete in Windows.
ms.assetid: 72dc0c57-28ae-4289-bb0d-b399d294c126
title: Descrizione di un'operazione di I/O di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371b72389554f1c3fa2ec43180b1a6e4c76dc012
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345801"
---
# <a name="description-of-a-network-io-operation"></a><span data-ttu-id="58b14-103">Descrizione di un'operazione di I/O di rete</span><span class="sxs-lookup"><span data-stu-id="58b14-103">Description of a Network I/O Operation</span></span>

<span data-ttu-id="58b14-104">Nella figura seguente viene illustrato il processo di un'operazione di I/O di rete in Windows.</span><span class="sxs-lookup"><span data-stu-id="58b14-104">The following figure illustrates the process of a network I/O operation under Windows.</span></span>

![operazione di i/o di rete in Windows](images/fig4.png)

<span data-ttu-id="58b14-106">Quando un'applicazione chiama una funzione di I/O di file per accedere a un file in un computer remoto, si verificano gli eventi seguenti:</span><span class="sxs-lookup"><span data-stu-id="58b14-106">When an application calls a file I/O function to access a file on a remote computer, the following events occur:</span></span>

-   <span data-ttu-id="58b14-107">La richiesta di I/O viene intercettata da un [redirector di rete](network-redirectors.md), detto anche semplicemente redirector, nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="58b14-107">The I/O request is intercepted by a [network redirector](network-redirectors.md), also referred to simply as a redirector, on the local computer.</span></span> <span data-ttu-id="58b14-108">Questa operazione viene illustrata nella figura precedente mediante la freccia a tinta unita tra l'applicazione e il redirector client.</span><span class="sxs-lookup"><span data-stu-id="58b14-108">This is depicted in the preceding figure by the solid arrow between the application and the client redirector.</span></span>
-   <span data-ttu-id="58b14-109">Il redirector costruisce un pacchetto di dati contenente tutte le informazioni sulla richiesta e lo invia al server in cui si trova il file.</span><span class="sxs-lookup"><span data-stu-id="58b14-109">The redirector constructs a data packet containing all of the information about the request, and sends it to the server where the file is located.</span></span> <span data-ttu-id="58b14-110">Questa operazione viene illustrata nella figura precedente mediante la freccia a tinta unita tra il redirector client e il redirector del server.</span><span class="sxs-lookup"><span data-stu-id="58b14-110">This is depicted in the preceding figure by the solid arrow between the client redirector and the server redirector.</span></span>
-   <span data-ttu-id="58b14-111">Il redirector sul server riceve il pacchetto dal client, autentica l'accesso al file richiesto dalla richiesta di I/O e, se autenticato, esegue la richiesta per conto del client.</span><span class="sxs-lookup"><span data-stu-id="58b14-111">The redirector on the server receives the packet from the client, authenticates the access to the file required by the I/O request, and, if authenticated, executes the request on behalf of the client.</span></span> <span data-ttu-id="58b14-112">In caso contrario, restituisce un codice di errore al redirector sul client.</span><span class="sxs-lookup"><span data-stu-id="58b14-112">If not, it returns an error code to the redirector on the client.</span></span> <span data-ttu-id="58b14-113">Questa operazione viene illustrata nella figura precedente mediante la freccia a tinta unita curva tra il redirector del server e il file.</span><span class="sxs-lookup"><span data-stu-id="58b14-113">This is depicted in the preceding figure by the curved solid arrow between the server redirector and the file.</span></span>
-   <span data-ttu-id="58b14-114">Quando la richiesta è stata eseguita, il redirector sul server invia tutti i dati risultanti dalla richiesta di I/O al redirector sul client insieme a una notifica di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="58b14-114">When the request has been executed, the redirector on the server sends any data resulting from the I/O request to the redirector on the client along with a success notification.</span></span> <span data-ttu-id="58b14-115">Questa operazione viene illustrata nella figura precedente dalla freccia tratteggiata tra il server e il redirector client.</span><span class="sxs-lookup"><span data-stu-id="58b14-115">This is depicted in the preceding figure by the dotted arrow between the server and the client redirector.</span></span>
-   <span data-ttu-id="58b14-116">Il redirector sul client riceve il pacchetto dal server e passa i dati nel pacchetto all'applicazione insieme a una notifica di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="58b14-116">The redirector on the client receives the packet from the server and passes the data in the packet to the application along with a success notification.</span></span> <span data-ttu-id="58b14-117">Questa operazione viene illustrata nella figura precedente dalla freccia tratteggiata tra il redirector client e l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="58b14-117">This is depicted in the preceding figure by the dotted arrow between the client redirector and the application.</span></span>

<span data-ttu-id="58b14-118">Windows può utilizzare un'ampia gamma di protocolli di rete per eseguire un'operazione di I/O di rete, tra cui il protocollo [Microsoft SMB e la panoramica del protocollo CIFS](microsoft-smb-protocol-and-cifs-protocol-overview.md) e NFS.</span><span class="sxs-lookup"><span data-stu-id="58b14-118">Windows can use a variety of networking protocols to perform a network I/O operation, including [Microsoft SMB Protocol and CIFS Protocol Overview](microsoft-smb-protocol-and-cifs-protocol-overview.md) and NFS.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="58b14-119">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="58b14-119">In this section</span></span>



| <span data-ttu-id="58b14-120">Argomento</span><span class="sxs-lookup"><span data-stu-id="58b14-120">Topic</span></span>                                                                                       | <span data-ttu-id="58b14-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="58b14-121">Description</span></span>                                                          |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="58b14-122">Differenze nell'I/O locale e di rete</span><span class="sxs-lookup"><span data-stu-id="58b14-122">Differences in Local and Network I/O</span></span>](differences-in-local-and-network-i-o.md)<br/> | <span data-ttu-id="58b14-123">Differenze tra l'i/o locale e l'I/O di rete in Windows.</span><span class="sxs-lookup"><span data-stu-id="58b14-123">Differences between local I/O and network I/O on Windows.</span></span><br/> |
| [<span data-ttu-id="58b14-124">Redirector di rete</span><span class="sxs-lookup"><span data-stu-id="58b14-124">Network Redirectors</span></span>](network-redirectors.md)<br/>                                   | <span data-ttu-id="58b14-125">Descrive la funzionalità di un redirector di rete.</span><span class="sxs-lookup"><span data-stu-id="58b14-125">Describes the functionality of a network redirector.</span></span><br/>      |



 

 

 




