---
description: Il parametro del protocollo in socket e WSASocket è un identificatore che stabilisce un tipo di rete e un metodo per identificare i vari protocolli di trasporto eseguiti sulla rete.
ms.assetid: cb4d99d5-3ae0-4bfc-b521-122dd9d4f1c2
title: Famiglia di identificatori di protocollo IPX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7fc808a04f1cf10bb099cd7d923bf471e9bd8d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129166"
---
# <a name="ipx-family-of-protocol-identifiers"></a><span data-ttu-id="86b43-103">Famiglia di identificatori di protocollo IPX</span><span class="sxs-lookup"><span data-stu-id="86b43-103">IPX Family of Protocol Identifiers</span></span>

<span data-ttu-id="86b43-104">Il parametro del *protocollo* in [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) e [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) è un identificatore che stabilisce un tipo di rete e un metodo per identificare i vari protocolli di trasporto eseguiti sulla rete.</span><span class="sxs-lookup"><span data-stu-id="86b43-104">The *protocol* parameter in [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) and [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) is an identifier that establishes a network type and a method for identifying the various transport protocols that run on the network.</span></span> <span data-ttu-id="86b43-105">A differenza di IP, IPX non usa un singolo valore di protocollo per la selezione di uno stack di trasporto.</span><span class="sxs-lookup"><span data-stu-id="86b43-105">Unlike IP, IPX does not use a single protocol value for selecting a transport stack.</span></span> <span data-ttu-id="86b43-106">Poiché non esiste alcun requisito di rete per usare un valore specifico per ogni protocollo di trasporto, è possibile assegnarli in modo appropriato per le applicazioni Winsock.</span><span class="sxs-lookup"><span data-stu-id="86b43-106">Since there is no network requirement to use a specific value for each transport protocol, we are free to assign them in a manner convenient for Winsock applications.</span></span> <span data-ttu-id="86b43-107">Si evitano i valori da 0 a 255 per evitare conflitti con i valori del \_ protocollo di PF inet corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="86b43-107">We avoid values 0–255 in order to avoid collisions with the corresponding PF\_INET protocol values.</span></span>



| <span data-ttu-id="86b43-108">Nome</span><span class="sxs-lookup"><span data-stu-id="86b43-108">Name</span></span>         | <span data-ttu-id="86b43-109">Valore</span><span class="sxs-lookup"><span data-stu-id="86b43-109">Value</span></span>       | <span data-ttu-id="86b43-110">Tipi di socket</span><span class="sxs-lookup"><span data-stu-id="86b43-110">Socket types</span></span>              | <span data-ttu-id="86b43-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86b43-111">Description</span></span>                                         |
|--------------|-------------|---------------------------|-----------------------------------------------------|
| <span data-ttu-id="86b43-112">Riservato</span><span class="sxs-lookup"><span data-stu-id="86b43-112">Reserved</span></span>     | <span data-ttu-id="86b43-113">0-255</span><span class="sxs-lookup"><span data-stu-id="86b43-113">0-255</span></span>       |                           | <span data-ttu-id="86b43-114">Riservato per \_ i valori del protocollo di PF inet.</span><span class="sxs-lookup"><span data-stu-id="86b43-114">Reserved for PF\_INET protocol values.</span></span>              |
| <span data-ttu-id="86b43-115">NSPROTO \_ IPX</span><span class="sxs-lookup"><span data-stu-id="86b43-115">NSPROTO\_IPX</span></span> | <span data-ttu-id="86b43-116">1000-1255</span><span class="sxs-lookup"><span data-stu-id="86b43-116">1000 - 1255</span></span> | <span data-ttu-id="86b43-117">SOCK \_ DGRAM Sock \_ RAW</span><span class="sxs-lookup"><span data-stu-id="86b43-117">SOCK\_DGRAM SOCK\_RAW</span></span>     | <span data-ttu-id="86b43-118">Servizio datagramma per IPX.</span><span class="sxs-lookup"><span data-stu-id="86b43-118">Datagram service for IPX.</span></span>                           |
| <span data-ttu-id="86b43-119">\_SPX NSPROTO</span><span class="sxs-lookup"><span data-stu-id="86b43-119">NSPROTO\_SPX</span></span> | <span data-ttu-id="86b43-120">1256</span><span class="sxs-lookup"><span data-stu-id="86b43-120">1256</span></span>        | <span data-ttu-id="86b43-121">Sock \_ Stream Sock \_ SEQPKT</span><span class="sxs-lookup"><span data-stu-id="86b43-121">SOCK\_STREAM SOCK\_SEQPKT</span></span> | <span data-ttu-id="86b43-122">Scambio di pacchetti affidabili con pacchetti a dimensione fissa.</span><span class="sxs-lookup"><span data-stu-id="86b43-122">Reliable packet exchange using fixed-sized packets.</span></span> |



 

> [!Note]  
> <span data-ttu-id="86b43-123">Quando \_ si specifica NSPROTO SPX, il protocollo SPX II viene usato automaticamente se entrambi gli endpoint sono in grado di eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="86b43-123">When NSPROTO\_SPX is specified, the SPX II protocol is automatically utilized if both endpoints are capable of doing so.</span></span>

 

 

 



