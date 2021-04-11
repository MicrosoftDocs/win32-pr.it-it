---
description: La famiglia di indirizzi IPX definisce la struttura di indirizzamento per i protocolli che utilizzano l'indirizzamento dei socket IPX standard. Per questi trasporti, un indirizzo endpoint è costituito da un numero di rete, un indirizzo del nodo e un numero di socket.
ms.assetid: cf749ae7-ab17-4c60-b00c-b34e092c6431
title: Famiglia di indirizzi AF_IPX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21508b23541b489c11fbdc38a2ff8dcf4ad53e48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129227"
---
# <a name="af_ipx-address-family"></a><span data-ttu-id="71aef-104">\_Famiglia di indirizzi IPX AF</span><span class="sxs-lookup"><span data-stu-id="71aef-104">AF\_IPX Address Family</span></span>

<span data-ttu-id="71aef-105">La famiglia di indirizzi IPX definisce la struttura di indirizzamento per i protocolli che utilizzano l'indirizzamento dei socket IPX standard.</span><span class="sxs-lookup"><span data-stu-id="71aef-105">The IPX address family defines the addressing structure for protocols that use standard IPX socket addressing.</span></span> <span data-ttu-id="71aef-106">Per questi trasporti, un indirizzo endpoint è costituito da un numero di rete, un indirizzo del nodo e un numero di socket.</span><span class="sxs-lookup"><span data-stu-id="71aef-106">For these transports, an endpoint address consists of a network number, node address, and socket number.</span></span>

<span data-ttu-id="71aef-107">Il numero di rete è un dominio amministrativo e in genere denomina un singolo segmento di anello Ethernet o token.</span><span class="sxs-lookup"><span data-stu-id="71aef-107">The network number is an administrative domain and typically names a single Ethernet or token ring segment.</span></span> <span data-ttu-id="71aef-108">Il numero del nodo è un indirizzo fisico della stazione.</span><span class="sxs-lookup"><span data-stu-id="71aef-108">The node number is a station's physical address.</span></span> <span data-ttu-id="71aef-109">La combinazione di rete e nodo costituisce un indirizzo di stazione univoco che si presume sia univoco nel mondo.</span><span class="sxs-lookup"><span data-stu-id="71aef-109">The combination of net and node form a unique station address that is presumed to be unique in the world.</span></span> <span data-ttu-id="71aef-110">I numeri di nodo e NET sono rappresentati nel testo ASCII in un blocco o in una notazione tratteggiata come:' 0101a040, 00001b498765' o ' 01-01-a0-40, 00-00-1B-49-87-65'.</span><span class="sxs-lookup"><span data-stu-id="71aef-110">Net and node numbers are represented in ASCII text in either block or dashed notation as: '0101a040,00001b498765' or '01-01-a0-40,00-00-1b-49-87-65'.</span></span> <span data-ttu-id="71aef-111">Gli zeri iniziali non devono essere presenti.</span><span class="sxs-lookup"><span data-stu-id="71aef-111">Leading zeros need not be present.</span></span>

<span data-ttu-id="71aef-112">Il numero di socket IPX è un numero di servizio di rete/trasporto molto simile a un numero di porta TCP e non deve essere confuso con il descrittore di socket Winsock.</span><span class="sxs-lookup"><span data-stu-id="71aef-112">The IPX socket number is a network/transport service number much like a TCP port number and is not to be confused with the Winsock socket descriptor.</span></span> <span data-ttu-id="71aef-113">I numeri di socket IPX sono globali per la stazione finale e non possono essere associati a indirizzi net/node specifici.</span><span class="sxs-lookup"><span data-stu-id="71aef-113">IPX socket numbers are global to the end station and cannot be bound to specific net/node addresses.</span></span> <span data-ttu-id="71aef-114">Ad esempio, se la stazione finale ha due schede di interfaccia di rete, un socket associato può inviare e ricevere su entrambe le schede.</span><span class="sxs-lookup"><span data-stu-id="71aef-114">For instance, if the end station has two network interface cards, a bound socket can send and receive on both cards.</span></span> <span data-ttu-id="71aef-115">In particolare, i socket di datagramma riceveranno datagrammi broadcast su entrambe le schede.</span><span class="sxs-lookup"><span data-stu-id="71aef-115">In particular, datagram sockets would receive broadcast datagrams on both cards.</span></span>

> [!Caution]  
> <span data-ttu-id="71aef-116">SOCKADDR \_ IPX ha una lunghezza di 14 byte ed è più breve della struttura di [**riferimento sockaddr**](sockaddr-2.md) a 16 byte.</span><span class="sxs-lookup"><span data-stu-id="71aef-116">SOCKADDR\_IPX is 14 bytes long and is shorter than the 16-byte [**sockaddr**](sockaddr-2.md) reference structure.</span></span> <span data-ttu-id="71aef-117">Le implementazioni IPX/SPX possono accettare la lunghezza di 16 byte e la lunghezza vera.</span><span class="sxs-lookup"><span data-stu-id="71aef-117">IPX/SPX implementations may accept the 16-byte length as well as the true length.</span></span> <span data-ttu-id="71aef-118">Se si usa SOCKADDR \_ IPX e una lunghezza hardcoded di 16 byte, l'implementazione può presumere che abbia accesso ai 2 byte che seguono la struttura.</span><span class="sxs-lookup"><span data-stu-id="71aef-118">If you use SOCKADDR\_IPX and a hard-coded length of 16 bytes, the implementation may assume that it has access to the 2 bytes following your structure.</span></span>

 



| <span data-ttu-id="71aef-119">Campo</span><span class="sxs-lookup"><span data-stu-id="71aef-119">Field</span></span>           | <span data-ttu-id="71aef-120">Valore</span><span class="sxs-lookup"><span data-stu-id="71aef-120">Value</span></span>                                    |
|-----------------|------------------------------------------|
| <span data-ttu-id="71aef-121">**\_famiglia sa**</span><span class="sxs-lookup"><span data-stu-id="71aef-121">**sa\_family**</span></span>  | <span data-ttu-id="71aef-122">Famiglia di indirizzi AF \_ IPX nell'ordine host.</span><span class="sxs-lookup"><span data-stu-id="71aef-122">Address family AF\_IPX in host order.</span></span>    |
| <span data-ttu-id="71aef-123">**\_Netnum SA**</span><span class="sxs-lookup"><span data-stu-id="71aef-123">**Sa\_netnum**</span></span>  | <span data-ttu-id="71aef-124">Identificatore di rete IPX in ordine di rete.</span><span class="sxs-lookup"><span data-stu-id="71aef-124">IPX network identifier in network order.</span></span> |
| <span data-ttu-id="71aef-125">**\_Nodenum SA**</span><span class="sxs-lookup"><span data-stu-id="71aef-125">**Sa\_nodenum**</span></span> | <span data-ttu-id="71aef-126">Indirizzo del nodo della stazione, svuotato a destra.</span><span class="sxs-lookup"><span data-stu-id="71aef-126">Station node address, flushed right.</span></span>     |
| <span data-ttu-id="71aef-127">**\_Socket SA**</span><span class="sxs-lookup"><span data-stu-id="71aef-127">**Sa\_socket**</span></span>  | <span data-ttu-id="71aef-128">Numero di socket IPX nell'ordine di rete.</span><span class="sxs-lookup"><span data-stu-id="71aef-128">IPX socket number in network order.</span></span>      |



 

 

 



