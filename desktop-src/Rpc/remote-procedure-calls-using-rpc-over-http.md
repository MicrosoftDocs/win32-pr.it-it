---
title: Chiamate di procedure remote con RPC tramite HTTP
description: I programmi del browser Internet utilizzano comunemente il protocollo HTTP (Hypertext Transport Protocol) come mezzo principale per esplorare il World Wide Web.
ms.assetid: f87262f6-fd82-4e8c-bf83-8f93791deec0
keywords:
- RPC (Remote Procedure Call), attività, utilizzo di RPC/http
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c84551500af712b1126d8f9a65cb3d02eba8c9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955065"
---
# <a name="remote-procedure-calls-using-rpc-over-http"></a><span data-ttu-id="9e454-104">Chiamate di procedure remote con RPC tramite HTTP</span><span class="sxs-lookup"><span data-stu-id="9e454-104">Remote Procedure Calls Using RPC over HTTP</span></span>

<span data-ttu-id="9e454-105">I programmi del browser Internet utilizzano comunemente il protocollo HTTP (Hypertext Transport Protocol) come mezzo principale per esplorare il World Wide Web.</span><span class="sxs-lookup"><span data-stu-id="9e454-105">Internet browser programs commonly employ the Hypertext Transport Protocol (HTTP) as the primary means of browsing the World Wide Web.</span></span> <span data-ttu-id="9e454-106">Il protocollo HTTP, quindi, rileva un utilizzo estensivo nella maggior parte dei computer.</span><span class="sxs-lookup"><span data-stu-id="9e454-106">HTTP, therefore, sees extensive usage on most computers today.</span></span> <span data-ttu-id="9e454-107">Microsoft ha esteso le funzionalità di Internet Information Server (IIS) per fornire servizi RPC (Remote Procedure Call) tramite HTTP.</span><span class="sxs-lookup"><span data-stu-id="9e454-107">Microsoft has extended the capabilities of its Internet Information Server (IIS) to provide remote procedure call services using HTTP.</span></span>

<span data-ttu-id="9e454-108">L'implementazione di Microsoft RPC su HTTP (RPC su HTTP) consente ai client RPC di connettersi in modo sicuro ed efficiente attraverso Internet ai programmi server RPC ed eseguire chiamate a procedure remote.</span><span class="sxs-lookup"><span data-stu-id="9e454-108">The Microsoft RPC-over-HTTP implementation (RPC over HTTP) allows RPC clients to securely and efficiently connect across the Internet to RPC server programs and execute remote procedure calls.</span></span> <span data-ttu-id="9e454-109">Questa operazione viene eseguita con l'ausilio di un intermediario noto come proxy RPC-over-HTTP o semplicemente del proxy RPC.</span><span class="sxs-lookup"><span data-stu-id="9e454-109">This is accomplished with the help of an intermediary known as the RPC-over-HTTP Proxy, or simply the RPC Proxy.</span></span>

<span data-ttu-id="9e454-110">Il proxy RPC viene eseguito in un computer IIS.</span><span class="sxs-lookup"><span data-stu-id="9e454-110">The RPC Proxy runs on an IIS computer.</span></span> <span data-ttu-id="9e454-111">Accetta le richieste RPC provenienti da Internet, esegue l'autenticazione, la convalida e i controlli di accesso su tali richieste. se la richiesta supera tutti i test, il proxy RPC inoltra la richiesta al server RPC che esegue l'elaborazione effettiva.</span><span class="sxs-lookup"><span data-stu-id="9e454-111">It accepts RPC requests coming from the Internet, performs authentication, validation, and access checks on those requests, and if the request passes all tests, RPC Proxy forwards the request to the RPC server that performs the actual processing.</span></span> <span data-ttu-id="9e454-112">Con RPC su HTTP, il client e il server RPC non comunicano direttamente; usano invece il proxy RPC come intermediario.</span><span class="sxs-lookup"><span data-stu-id="9e454-112">With RPC over HTTP the RPC client and server do not communicate directly; rather, they use the RPC Proxy as intermediary.</span></span> <span data-ttu-id="9e454-113">Questo modello è stato scelto per diversi motivi.</span><span class="sxs-lookup"><span data-stu-id="9e454-113">This model was chosen for many reasons.</span></span> <span data-ttu-id="9e454-114">Per ulteriori informazioni, vedere la pagina relativa alla [sicurezza RPC su http](rpc-over-http-security.md).</span><span class="sxs-lookup"><span data-stu-id="9e454-114">For more information, see [RPC over HTTP Security](rpc-over-http-security.md).</span></span>

<span data-ttu-id="9e454-115">In questa sezione viene fornita una panoramica di RPC su HTTP negli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="9e454-115">This section provides an overview of RPC over HTTP in the following topics:</span></span>

-   [<span data-ttu-id="9e454-116">Utilizzo di HTTP come trasporto RPC</span><span class="sxs-lookup"><span data-stu-id="9e454-116">Using HTTP as an RPC Transport</span></span>](using-http-as-an-rpc-transport.md)
-   [<span data-ttu-id="9e454-117">Sicurezza RPC su HTTP</span><span class="sxs-lookup"><span data-stu-id="9e454-117">RPC over HTTP Security</span></span>](rpc-over-http-security.md)
-   [<span data-ttu-id="9e454-118">Requisiti di sistema e interoperabilità per RPC su HTTP</span><span class="sxs-lookup"><span data-stu-id="9e454-118">System Requirements and Interoperability for RPC over HTTP</span></span>](system-requirements-and-interoperability-for-rpc-over-http.md)
-   [<span data-ttu-id="9e454-119">Configurazione dei computer per RPC su HTTP</span><span class="sxs-lookup"><span data-stu-id="9e454-119">Configuring Computers for RPC over HTTP</span></span>](configuring-computers-for-rpc-over-http.md)
-   [<span data-ttu-id="9e454-120">Raccomandazioni sulla distribuzione RPC su HTTP</span><span class="sxs-lookup"><span data-stu-id="9e454-120">RPC over HTTP Deployment Recommendations</span></span>](rpc-over-http-deployment-recommendations.md)

<span data-ttu-id="9e454-121">Per informazioni sugli scenari RPC con volume elevato su HTTP, vedere [Microsoft RPC Load Balancing](rpc-load-balancing.md).</span><span class="sxs-lookup"><span data-stu-id="9e454-121">For information regarding high volume RPC over HTTP scenarios, please see [Microsoft RPC Load Balancing](rpc-load-balancing.md).</span></span>

 

 




