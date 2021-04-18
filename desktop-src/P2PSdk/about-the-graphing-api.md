---
description: L'API per la rappresentazione grafica dei peer consente alle applicazioni di passare i dati tra i peer in modo efficiente e affidabile. I concetti di base della tecnologia di peer Graph sono i nodi di un grafo peer e le notifiche degli eventi.
ms.assetid: c3530134-bde3-4a9a-b433-4f198430a607
title: Informazioni sull'API Graphing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1b08e320f1c8d176d0bd34cc7a9a9422c6cfadc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312304"
---
# <a name="about-the-graphing-api"></a><span data-ttu-id="d252e-104">Informazioni sull'API Graphing</span><span class="sxs-lookup"><span data-stu-id="d252e-104">About the Graphing API</span></span>

<span data-ttu-id="d252e-105">L'API per la rappresentazione grafica dei peer consente alle applicazioni di passare i dati tra i peer in modo efficiente e affidabile.</span><span class="sxs-lookup"><span data-stu-id="d252e-105">The Peer Graphing API allows applications to pass data between peers efficiently and reliably.</span></span> <span data-ttu-id="d252e-106">I concetti di base della tecnologia di peer Graph sono i **nodi** di un grafo peer e le notifiche degli eventi.</span><span class="sxs-lookup"><span data-stu-id="d252e-106">The core concepts of peer graph technology are the **nodes** of a peer graph, and event notices.</span></span>

## <a name="nodes"></a><span data-ttu-id="d252e-107">Nodi</span><span class="sxs-lookup"><span data-stu-id="d252e-107">Nodes</span></span>

<span data-ttu-id="d252e-108">Un nodo rappresenta un'istanza specifica di un peer in una rete.</span><span class="sxs-lookup"><span data-stu-id="d252e-108">A node represents a specific instance of a peer on a network.</span></span> <span data-ttu-id="d252e-109">L'infrastruttura dell'API per la rappresentazione di peering garantisce che ogni nodo disponga di una visualizzazione coerente dei dati in un grafico.</span><span class="sxs-lookup"><span data-stu-id="d252e-109">The Peer Graphing API infrastructure ensures that each node has a consistent view of the data in a graph.</span></span> <span data-ttu-id="d252e-110">Un nodo presenta le funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="d252e-110">A node has the following features:</span></span>

-   <span data-ttu-id="d252e-111">Può connettersi a un nodo diverso e formare una rete interconnessa denominata grafico a più peer.</span><span class="sxs-lookup"><span data-stu-id="d252e-111">Can connect to a different node, and form an interrelated network called a peer graph.</span></span>
-   <span data-ttu-id="d252e-112">Può condividere dati con altri nodi in un grafico sotto forma di [record](records.md).</span><span class="sxs-lookup"><span data-stu-id="d252e-112">Can share data with other nodes in a graph in the form of a [record](records.md).</span></span>
-   <span data-ttu-id="d252e-113">Consente di creare connessioni dirette separate dai grafici peer stabiliti tramite l'API di [raggruppamento](about-the-grouping-api.md)peer.</span><span class="sxs-lookup"><span data-stu-id="d252e-113">Can create direct connections separate from the peer graphs established by using the Peer [Grouping API](about-the-grouping-api.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="d252e-114">Le connessioni dirette consentono ai nodi di inviare i dati privati tra loro.</span><span class="sxs-lookup"><span data-stu-id="d252e-114">Direct connections allow nodes to send private data to each other.</span></span>

     

## <a name="event-notices"></a><span data-ttu-id="d252e-115">Notifiche degli eventi</span><span class="sxs-lookup"><span data-stu-id="d252e-115">Event Notices</span></span>

<span data-ttu-id="d252e-116">L'API per la grafica di peering dispone di un'infrastruttura di eventi che consente a un'applicazione di registrare e ricevere l'avviso di un evento peer nell'infrastruttura dell'API per la rappresentazione di Peer Graphing.</span><span class="sxs-lookup"><span data-stu-id="d252e-116">The Peer Graphing API has an event infrastructure that allows an application to register and receive notice of a peer event within the Peer Graphing API infrastructure.</span></span> <span data-ttu-id="d252e-117">Quando viene modificato un elemento in un grafico peer, un'applicazione invia una notifica di evento per identificare che si è verificata una modifica.</span><span class="sxs-lookup"><span data-stu-id="d252e-117">When something changes within a peer graph, an application sends an event notice to identify that a change has occurred.</span></span>

 

 



