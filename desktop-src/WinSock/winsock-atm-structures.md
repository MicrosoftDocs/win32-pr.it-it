---
description: Nell'elenco seguente vengono fornite descrizioni concise di ogni struttura ATM di Winsock. Per ulteriori informazioni su qualsiasi struttura, fare clic sul nome della struttura.
ms.assetid: ce80ef1f-9a76-4a6f-a7ce-f166bc46ca08
title: Strutture ATM Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaf28266de89e5346727a9ad42fdb90d9167bc9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308862"
---
# <a name="winsock-atm-structures"></a><span data-ttu-id="48551-104">Strutture ATM Winsock</span><span class="sxs-lookup"><span data-stu-id="48551-104">Winsock ATM Structures</span></span>

<span data-ttu-id="48551-105">Nell'elenco seguente vengono fornite descrizioni concise di ogni struttura ATM di Winsock.</span><span class="sxs-lookup"><span data-stu-id="48551-105">The following list provides concise descriptions of each Winsock ATM structure.</span></span> <span data-ttu-id="48551-106">Per ulteriori informazioni su qualsiasi struttura, fare clic sul nome della struttura.</span><span class="sxs-lookup"><span data-stu-id="48551-106">For additional information on any structure, click the structure name.</span></span>



| <span data-ttu-id="48551-107">Struttura ATM</span><span class="sxs-lookup"><span data-stu-id="48551-107">ATM Structure</span></span>                           | <span data-ttu-id="48551-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="48551-108">Description</span></span>                                                |
|-----------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="48551-109">**\_indirizzo ATM**</span><span class="sxs-lookup"><span data-stu-id="48551-109">**ATM\_ADDRESS**</span></span>](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_address)   | <span data-ttu-id="48551-110">Archivia i dati dell'indirizzo ATM per i socket basati su ATM.</span><span class="sxs-lookup"><span data-stu-id="48551-110">Stores ATM address data for ATM-based sockets.</span></span>             |
| [<span data-ttu-id="48551-111">**\_BHLI ATM**</span><span class="sxs-lookup"><span data-stu-id="48551-111">**ATM\_BHLI**</span></span>](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_bhli)         | <span data-ttu-id="48551-112">Identifica le informazioni B-HLI per un socket ATM associato.</span><span class="sxs-lookup"><span data-stu-id="48551-112">Identifies B-HLI information for an associated ATM socket.</span></span> |
| [<span data-ttu-id="48551-113">**\_BLLI ATM**</span><span class="sxs-lookup"><span data-stu-id="48551-113">**ATM\_BLLI**</span></span>](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_blli)         | <span data-ttu-id="48551-114">Identifica le informazioni B-LLI per un socket ATM associato.</span><span class="sxs-lookup"><span data-stu-id="48551-114">Identifies B-LLI information for an associated ATM socket.</span></span> |
| [<span data-ttu-id="48551-115">**sockaddr \_ ATM**</span><span class="sxs-lookup"><span data-stu-id="48551-115">**sockaddr\_atm**</span></span>](/windows/desktop/api/Ws2atm/ns-ws2atm-sockaddr_atm) | <span data-ttu-id="48551-116">Archivia le informazioni sull'indirizzo del socket per i socket ATM.</span><span class="sxs-lookup"><span data-stu-id="48551-116">Stores socket address information for ATM sockets.</span></span>         |



 

<span data-ttu-id="48551-117">Per i servizi ATM nativi, usare AF \_ ATM per la famiglia di indirizzi e la struttura di indirizzi del socket [**\_ ATM sockaddr**](/windows/desktop/api/Ws2atm/ns-ws2atm-sockaddr_atm) .</span><span class="sxs-lookup"><span data-stu-id="48551-117">For native ATM services, use AF\_ATM for address family and the [**sockaddr\_atm**](/windows/desktop/api/Ws2atm/ns-ws2atm-sockaddr_atm) socket address structure.</span></span> <span data-ttu-id="48551-118">Per aprire un socket ATM nativo, passare \_ rispettivamente AF ATM, Sock \_ RAW e ATMPROTO \_ AAL5 o ATMPROTO \_ AALUSER nella funzione [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) .</span><span class="sxs-lookup"><span data-stu-id="48551-118">To open a native ATM socket, pass AF\_ATM, SOCK\_RAW, and ATMPROTO\_AAL5 or ATMPROTO\_AALUSER into the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function, respectively.</span></span>

 

 



