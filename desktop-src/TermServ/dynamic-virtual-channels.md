---
title: Canali virtuali dinamici
description: Le API del canale virtuale dinamico (DVC) estendono le API del canale virtuale esistente per Servizi Desktop remoto, note come API del canale virtuale statico (SVC).
ms.assetid: bddf0048-482d-40f3-a973-9d7bc15be8fa
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3181c0960b50289846018c3ace773a8351cb20
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395894"
---
# <a name="dynamic-virtual-channels"></a><span data-ttu-id="c702d-103">Canali virtuali dinamici</span><span class="sxs-lookup"><span data-stu-id="c702d-103">Dynamic Virtual Channels</span></span>

<span data-ttu-id="c702d-104">Le API del canale virtuale dinamico (DVC) estendono le API del canale virtuale esistente per Servizi Desktop remoto, note come API del canale virtuale statico (SVC).</span><span class="sxs-lookup"><span data-stu-id="c702d-104">Dynamic virtual channel (DVC) APIs extend the existing virtual channel APIs for Remote Desktop Services, known as static virtual channel (SVC) APIs.</span></span> <span data-ttu-id="c702d-105">Le API DVC affrontano diverse limitazioni esistenti nelle API SVC tra il client e il server, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="c702d-105">DVC APIs address several limitations that existed in SVC APIs between the client and server, such as:</span></span>

-   <span data-ttu-id="c702d-106">Un numero limitato di canali</span><span class="sxs-lookup"><span data-stu-id="c702d-106">A limited number of channels</span></span>
-   <span data-ttu-id="c702d-107">Ricostruzione di pacchetti</span><span class="sxs-lookup"><span data-stu-id="c702d-107">Packet reconstruction</span></span>

<span data-ttu-id="c702d-108">Le API DVC consentiranno di implementare moduli sul lato server e client di una connessione Servizi Desktop remoto che comunicano tra loro.</span><span class="sxs-lookup"><span data-stu-id="c702d-108">DVC APIs will help you to implement modules on the server and client side of a Remote Desktop Services connection that communicate with each other.</span></span>

<span data-ttu-id="c702d-109">Analogamente a molte altre architetture client/server, viene stabilita una connessione basata su una porzione di dati comunemente concordata, definita endpoint.</span><span class="sxs-lookup"><span data-stu-id="c702d-109">Like many other client/server architectures, a connection is established based on a commonly agreed upon piece of data, referred to as an endpoint.</span></span> <span data-ttu-id="c702d-110">Un esempio simile è TCP/IP, in cui un endpoint viene stabilito tramite una combinazione di indirizzo IP del server e nome della porta.</span><span class="sxs-lookup"><span data-stu-id="c702d-110">A similar example is TCP/IP, where an endpoint is established through a combination of server IP address and the port name.</span></span> <span data-ttu-id="c702d-111">Un altro esempio è Named Pipes, in cui un endpoint è una combinazione del nome del server e del nome della pipe.</span><span class="sxs-lookup"><span data-stu-id="c702d-111">Another example is named pipes, where an endpoint is a combination of the server name and the pipe name.</span></span> <span data-ttu-id="c702d-112">In una connessione Servizi Desktop remoto sono presenti solo due parti.</span><span class="sxs-lookup"><span data-stu-id="c702d-112">In a Remote Desktop Services connection there are only two sides involved.</span></span> <span data-ttu-id="c702d-113">Pertanto, l'endpoint è costituito da una semplice stringa arbitraria che identifica in modo univoco la connessione.</span><span class="sxs-lookup"><span data-stu-id="c702d-113">Therefore, the endpoint consists of a simple arbitrary string that uniquely identifies the connection.</span></span> <span data-ttu-id="c702d-114">Analogamente a TCP/IP e named pipe, è possibile avviare più connessioni dallo stesso nome di endpoint.</span><span class="sxs-lookup"><span data-stu-id="c702d-114">Much like TCP/IP and named pipes, multiple connections can initiate from the same endpoint name.</span></span> <span data-ttu-id="c702d-115">In questo senso, le connessioni non hanno nomi; solo un listener che attende le richieste in ingresso sull'endpoint.</span><span class="sxs-lookup"><span data-stu-id="c702d-115">In that sense, connections do not have names; just a listener that waits for incoming requests on the endpoint.</span></span>

<span data-ttu-id="c702d-116">Le API DVC sono costituite dai seguenti elementi:</span><span class="sxs-lookup"><span data-stu-id="c702d-116">The DVC APIs consist of the following:</span></span>

-   <span data-ttu-id="c702d-117">API client</span><span class="sxs-lookup"><span data-stu-id="c702d-117">Client APIs</span></span>

    <span data-ttu-id="c702d-118">Queste API sono disponibili nel client di Connessione Desktop remoto (RDC) come plug-in.</span><span class="sxs-lookup"><span data-stu-id="c702d-118">These APIs are available in the Remote Desktop Connection (RDC) client as a plug-in.</span></span> <span data-ttu-id="c702d-119">Il lato client è in modalità passiva, in cui è in ascolto delle connessioni in ingresso ma non stabilisce attivamente una connessione.</span><span class="sxs-lookup"><span data-stu-id="c702d-119">The client side is in passive mode, where it listens for incoming connections but does not actively establish a connection.</span></span>

-   <span data-ttu-id="c702d-120">API server</span><span class="sxs-lookup"><span data-stu-id="c702d-120">Server APIs</span></span>

    <span data-ttu-id="c702d-121">Queste API avviano attivamente la connessione.</span><span class="sxs-lookup"><span data-stu-id="c702d-121">These APIs actively initiate the connection.</span></span>

<span data-ttu-id="c702d-122">Per informazioni su come scrivere un modulo canale virtuale dinamico (DVC), vedere [Dettagli di implementazione di DVC](dvc-implementation-details.md).</span><span class="sxs-lookup"><span data-stu-id="c702d-122">For information about how to write a dynamic virtual channel (DVC) module, see [DVC Implementation Details](dvc-implementation-details.md).</span></span>

 

 




