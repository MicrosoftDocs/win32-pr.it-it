---
description: Questo argomento descrive considerazioni specifiche sulla programmazione quando si usa l'infrastruttura peer.
ms.assetid: 525b0625-ec13-4aba-a741-dbacff3587f9
title: Considerazioni sulla programmazione (peer-to-peer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89956cbdbbc8d2ed89226a490bbae505862ab18f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312226"
---
# <a name="programming-considerations-peer-to-peer"></a><span data-ttu-id="e7728-103">Considerazioni sulla programmazione (peer-to-peer)</span><span class="sxs-lookup"><span data-stu-id="e7728-103">Programming Considerations (Peer-to-Peer)</span></span>

<span data-ttu-id="e7728-104">Questo argomento descrive considerazioni specifiche sulla programmazione quando si usa l'infrastruttura peer.</span><span class="sxs-lookup"><span data-stu-id="e7728-104">This topic discusses specific programming considerations when using the Peer Infrastructure.</span></span>

<span data-ttu-id="e7728-105">Quando si usa l'infrastruttura peer per sviluppare applicazioni peer, è necessario tenere conto delle considerazioni di programmazione seguenti:</span><span class="sxs-lookup"><span data-stu-id="e7728-105">When using the Peer Infrastructure to develop peer applications, you must take the following programming considerations into account:</span></span>

-   <span data-ttu-id="e7728-106">IPv6</span><span class="sxs-lookup"><span data-stu-id="e7728-106">IPv6</span></span>

    <span data-ttu-id="e7728-107">Per l'infrastruttura peer è necessario che IPv6 sia installato e avviato per consentire il funzionamento delle applicazioni di rete peer.</span><span class="sxs-lookup"><span data-stu-id="e7728-107">The Peer Infrastructure requires that IPv6 be installed and started to enable peer networking applications to function.</span></span>

-   <span data-ttu-id="e7728-108">Porte del firewall</span><span class="sxs-lookup"><span data-stu-id="e7728-108">Firewall Ports</span></span>

    <span data-ttu-id="e7728-109">Quando si utilizza un firewall in una rete, ad esempio il firewall della connessione Internet IPv6, è necessario aprire porte specifiche per consentire il funzionamento dell'infrastruttura peer.</span><span class="sxs-lookup"><span data-stu-id="e7728-109">When a firewall is being used on a network (such as the IPv6 Internet Connection firewall), specific ports must be opened to allow the Peer Infrastructure to function.</span></span> <span data-ttu-id="e7728-110">È necessario aprire le seguenti porte:</span><span class="sxs-lookup"><span data-stu-id="e7728-110">The following ports must be open:</span></span>

    <span data-ttu-id="e7728-111">Porta TCP 3587 per l'infrastruttura di raggruppamento peer.</span><span class="sxs-lookup"><span data-stu-id="e7728-111">TCP port 3587 for the Peer Grouping Infrastructure.</span></span>

    <span data-ttu-id="e7728-112">Porta UDP 3540 per l'infrastruttura di Peer Graphing.</span><span class="sxs-lookup"><span data-stu-id="e7728-112">UDP port 3540 for the Peer Graphing Infrastructure.</span></span>

    > [!Note]  
    > <span data-ttu-id="e7728-113">Le applicazioni che utilizzano l'infrastruttura peer Graphing su TCP scelgono la propria porta TCP quando chiamano [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten).</span><span class="sxs-lookup"><span data-stu-id="e7728-113">Applications that use the Peer Graphing Infrastructure over TCP choose their own TCP port when calling [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten).</span></span>

     

-   <span data-ttu-id="e7728-114">Opzione socket</span><span class="sxs-lookup"><span data-stu-id="e7728-114">Socket Option</span></span>

    <span data-ttu-id="e7728-115">Quando si tenta di connettersi direttamente ad altri nodi peer IPv6 (senza usare l'infrastruttura peer), assicurarsi che il livello di protezione IPV6 dell'opzione socket \_ \_ sia impostato sul **livello di protezione \_ \_ senza restrizioni**.</span><span class="sxs-lookup"><span data-stu-id="e7728-115">When attempting to connect to other IPv6 peer nodes directly (without using the Peer Infrastructure), ensure that the socket option IPV6\_PROTECTION\_LEVEL is set to **PROTECTION\_LEVEL\_UNRESTRICTED**.</span></span>

-   <span data-ttu-id="e7728-116">Larghezza di banda</span><span class="sxs-lookup"><span data-stu-id="e7728-116">Bandwidth</span></span>

    <span data-ttu-id="e7728-117">Quando si usa PNRP, un'applicazione può pubblicare uno o più [nomi di peer](peer-names.md) che possono essere risolti.</span><span class="sxs-lookup"><span data-stu-id="e7728-117">When using PNRP, an application can publish one or more [peer names](peer-names.md) that can be resolved.</span></span> <span data-ttu-id="e7728-118">Per ogni nome peer registrato con PNRP, si verifica un aumento della larghezza di banda di rete usato da PNRP per pubblicare il nome peer e lo si mantiene disponibile per la risoluzione da parte di altri nodi.</span><span class="sxs-lookup"><span data-stu-id="e7728-118">For each peer name registered with PNRP, there is an increase in the network bandwidth that PNRP uses to publish the peer name, and keep it available to be resolved by other nodes.</span></span>

    <span data-ttu-id="e7728-119">Per evitare di utilizzare troppa larghezza di banda, le applicazioni devono evitare di registrare un numero elevato di nomi di peer in un computer.</span><span class="sxs-lookup"><span data-stu-id="e7728-119">To prevent using too much bandwidth, applications should avoid registering large numbers of peer names on a computer.</span></span> <span data-ttu-id="e7728-120">Ad esempio, un'applicazione che pubblica immagini non deve creare un nome peer per ogni immagine, ma deve creare un nome peer per il servizio che pubblica le immagini e usare un protocollo diverso per consentire ai client di eseguire query sul servizio per immagini specifiche.</span><span class="sxs-lookup"><span data-stu-id="e7728-120">For example, an application that publishes pictures should not create a peer name for each picture, but should create one peer name for the service that publishes pictures, and use a different protocol for clients to query the service for specific pictures.</span></span>

-   <span data-ttu-id="e7728-121">Registrazione del nome peer</span><span class="sxs-lookup"><span data-stu-id="e7728-121">Peer Name Registration</span></span>

    <span data-ttu-id="e7728-122">È possibile che alcune applicazioni debbano registrare lo stesso [nome peer](peer-names.md) in più di un computer.</span><span class="sxs-lookup"><span data-stu-id="e7728-122">Some applications may be required to register the same [peer name](peer-names.md) on more than one computer.</span></span> <span data-ttu-id="e7728-123">In genere, ciò si verifica se un nome peer è associato a una persona che utilizza più di un computer.</span><span class="sxs-lookup"><span data-stu-id="e7728-123">Typically, this happens if a peer name is associated with a person who uses more than one computer.</span></span> <span data-ttu-id="e7728-124">Un metodo che è possibile utilizzare per registrare lo stesso nome peer in più computer consiste nel creare un gruppo peer per la persona e connettersi a tale gruppo da tutti i computer.</span><span class="sxs-lookup"><span data-stu-id="e7728-124">One method that you can use to register the same peer name on multiple computers is to create a peer group for the person, and connect to that group from all computers.</span></span> <span data-ttu-id="e7728-125">Un altro metodo consiste nel creare un'identità peer e un nome peer in un computer, esportare l'identità peer dal computer e importarla in altri computer.</span><span class="sxs-lookup"><span data-stu-id="e7728-125">Another method is to create a peer identity and peer name on one computer, export the peer identity from that computer, and import it on other computers.</span></span> <span data-ttu-id="e7728-126">In questo modo è possibile creare lo stesso nome peer sicuro in tutti i computer che hanno importato l'identità peer.</span><span class="sxs-lookup"><span data-stu-id="e7728-126">This allows the same secure peer name to be created on all the computers that have imported the peer identity.</span></span>

 

 



