---
description: È necessario prestare particolare attenzione a mittenti o ricevitori PGM multihomed. In questa pagina vengono descritte le considerazioni e vengono fornite linee guida per procedure di programmazione ottimali.
ms.assetid: 10fb56dd-3c96-4944-9b53-aee76c269528
title: Multihoming e PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 142527c7fdf3e5d34d80c51e4002bc21ad47691c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306929"
---
# <a name="multihoming-and-pgm"></a><span data-ttu-id="5fcc9-104">Multihoming e PGM</span><span class="sxs-lookup"><span data-stu-id="5fcc9-104">Multihoming and PGM</span></span>

<span data-ttu-id="5fcc9-105">È necessario prestare particolare attenzione a mittenti o ricevitori PGM multihomed.</span><span class="sxs-lookup"><span data-stu-id="5fcc9-105">Special consideration must be given to multihomed PGM senders or receivers.</span></span> <span data-ttu-id="5fcc9-106">In questa pagina vengono descritte le considerazioni e vengono fornite linee guida per procedure di programmazione ottimali.</span><span class="sxs-lookup"><span data-stu-id="5fcc9-106">This page describes the considerations, and provides guidelines for best programming practices.</span></span>

## <a name="multihomed-pgm-sender"></a><span data-ttu-id="5fcc9-107">Mittente PGM multihomed</span><span class="sxs-lookup"><span data-stu-id="5fcc9-107">Multihomed PGM Sender</span></span>

<span data-ttu-id="5fcc9-108">Quando un'applicazione non riesce a specificare un'interfaccia quando chiama la funzione [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) , viene usata la prima interfaccia disponibile.</span><span class="sxs-lookup"><span data-stu-id="5fcc9-108">When an application fails to specify an interface upon calling the [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) function, the first available interface is used.</span></span> <span data-ttu-id="5fcc9-109">Se non è disponibile alcuna interfaccia, la **connessione** ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="5fcc9-109">If no interface is available, **connect** fails.</span></span>

<span data-ttu-id="5fcc9-110">Quando un'applicazione specifica un'interfaccia utilizzando l'opzione [RM \_ set \_ Send \_ if](socket-options.md) socket, un tentativo di [**associazione**](/windows/desktop/api/winsock/nf-winsock-bind) viene eseguito in modo implicito a tale interfaccia utilizzando TCP/IP e ha esito negativo se TCP/IP non riesce a eseguire la richiesta di binding.</span><span class="sxs-lookup"><span data-stu-id="5fcc9-110">When an application specifies an interface using the [RM\_SET\_SEND\_IF](socket-options.md) socket option, a [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) attempt is made implicitly to that interface using TCP/IP, and fails if TCP/IP fails the bind request.</span></span> <span data-ttu-id="5fcc9-111">Se l'interfaccia viene impostata con RM \_ set \_ Send \_ se più volte, è applicabile solo l'ultimo set di interfacce.</span><span class="sxs-lookup"><span data-stu-id="5fcc9-111">If the interface is set using RM\_SET\_SEND\_IF multiple times, only the last interface set successfully is applicable.</span></span>

<span data-ttu-id="5fcc9-112">Windows Sockets mantiene l'interfaccia impostata e, se tale interfaccia scompare, la sessione viene disconnessa.</span><span class="sxs-lookup"><span data-stu-id="5fcc9-112">Windows Sockets maintains which interface is set, and if that interface disappears, the session is disconnected.</span></span>

## <a name="multihomed-pgm-receiver"></a><span data-ttu-id="5fcc9-113">Ricevitore PGM multihomed</span><span class="sxs-lookup"><span data-stu-id="5fcc9-113">Multihomed PGM Receiver</span></span>

<span data-ttu-id="5fcc9-114">Quando un'applicazione non riesce a specificare un'interfaccia quando chiama la funzione [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) , viene utilizzata l'interfaccia predefinita.</span><span class="sxs-lookup"><span data-stu-id="5fcc9-114">When an application fails to specify an interface upon calling the [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) function, the default interface is used.</span></span> <span data-ttu-id="5fcc9-115">Se non è disponibile alcuna interfaccia, l' [**associazione**](/windows/desktop/api/winsock/nf-winsock-bind) non riesce.</span><span class="sxs-lookup"><span data-stu-id="5fcc9-115">If no interface is available, [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) fails.</span></span>

<span data-ttu-id="5fcc9-116">Quando un'applicazione specifica una o più interfacce su cui restare in ascolto utilizzando [RM \_ Add \_ Receive \_ if](socket-options.md), Windows Sockets tenta di eseguire l'associazione all'interfaccia o alle interfacce richieste tramite TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="5fcc9-116">When an application specifies one or more interfaces on which to listen, using [RM\_ADD\_RECEIVE\_IF](socket-options.md), Windows Sockets attempts to bind to the requested interface or interfaces using TCP/IP.</span></span> <span data-ttu-id="5fcc9-117">Qualsiasi errore di TCP/IP causa la mancata riuscita della richiesta.</span><span class="sxs-lookup"><span data-stu-id="5fcc9-117">Any error from TCP/IP causes this request to fail.</span></span> <span data-ttu-id="5fcc9-118">A differenza del caso del mittente PGM, l'aggiunta di un'interfaccia di ricezione più volte comporta la pubblicazione in attesa di tutte le interfacce aggiunte correttamente.</span><span class="sxs-lookup"><span data-stu-id="5fcc9-118">Unlike the PGM sender case, adding a receive interface multiple times result in the listens being posted on all the successfully added interfaces.</span></span> <span data-ttu-id="5fcc9-119">Usare l' \_ \_ \_ opzione di ricezione del socket If di RM per arrestare l'attesa su un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="5fcc9-119">Use the RM\_DEL\_RECEIVE\_IF socket option to stop listening on an interface.</span></span>

<span data-ttu-id="5fcc9-120">Windows Sockets non mantiene lo stato di più interfacce di ascolto specificate e si basa invece su TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="5fcc9-120">Windows Sockets does not maintain state about multiple specified listening interfaces, and instead relies on TCP/IP to do so.</span></span> <span data-ttu-id="5fcc9-121">Quando è in corso una sessione, tuttavia, Windows Sockets tiene traccia dell'interfaccia in ingresso per tale sessione. se l'interfaccia scompare, Windows Sockets disconnette la sessione.</span><span class="sxs-lookup"><span data-stu-id="5fcc9-121">Once a session is in progress, however, Windows Sockets track the incoming interface for that session, and if that interface disappears, Windows Sockets disconnects the session.</span></span>

 

 



