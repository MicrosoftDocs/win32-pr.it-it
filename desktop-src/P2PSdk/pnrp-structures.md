---
description: "L'API del provider dello spazio dei nomi PNRP usa le strutture seguenti:"
ms.assetid: 697fb99a-259f-429c-8818-0d725255bc86
title: Strutture PNRP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a78e2ee85f3673395ade31417c79c010354f16b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312227"
---
# <a name="pnrp-structures"></a><span data-ttu-id="ff2fd-103">Strutture PNRP</span><span class="sxs-lookup"><span data-stu-id="ff2fd-103">PNRP Structures</span></span>

<span data-ttu-id="ff2fd-104">L'API del provider dello spazio dei nomi PNRP usa le strutture seguenti:</span><span class="sxs-lookup"><span data-stu-id="ff2fd-104">The PNRP Namespace Provider API uses the following structures:</span></span>



| <span data-ttu-id="ff2fd-105">Struttura</span><span class="sxs-lookup"><span data-stu-id="ff2fd-105">Structure</span></span>                                                             | <span data-ttu-id="ff2fd-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ff2fd-106">Description</span></span>                                                                                                                                                         |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ff2fd-107">**\_ \_ informazioni endpoint PNRP \_ peer**</span><span class="sxs-lookup"><span data-stu-id="ff2fd-107">**PEER\_PNRP\_ENDPOINT\_INFO**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_pnrp_endpoint_info)         | <span data-ttu-id="ff2fd-108">Contiene gli indirizzi IP e i dati associati a un endpoint peer.</span><span class="sxs-lookup"><span data-stu-id="ff2fd-108">Contains the IP addresses and data associated with a peer endpoint.</span></span>                                                                                                 |
| [<span data-ttu-id="ff2fd-109">**\_informazioni sul \_ cloud \_ PNRP peer**</span><span class="sxs-lookup"><span data-stu-id="ff2fd-109">**PEER\_PNRP\_CLOUD\_INFO**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_pnrp_cloud_info)               | <span data-ttu-id="ff2fd-110">Contiene informazioni su un Cloud PNRP (Peer Name Resolution Protocol).</span><span class="sxs-lookup"><span data-stu-id="ff2fd-110">Contains information about a Peer Name Resolution Protocol (PNRP) cloud.</span></span>                                                                                            |
| [<span data-ttu-id="ff2fd-111">**\_informazioni di \_ registrazione \_ PNRP peer**</span><span class="sxs-lookup"><span data-stu-id="ff2fd-111">**PEER\_PNRP\_REGISTRATION\_INFO**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_pnrp_registration_info) | <span data-ttu-id="ff2fd-112">Contiene le informazioni fornite da un'identità peer quando viene registrato con un Cloud PNRP.</span><span class="sxs-lookup"><span data-stu-id="ff2fd-112">Contains the information provided by a peer identity when it registers with a PNRP cloud.</span></span>                                                                           |
| [<span data-ttu-id="ff2fd-113">PNRP e BLOB</span><span class="sxs-lookup"><span data-stu-id="ff2fd-113">PNRP and BLOB</span></span>](pnrp-and-blob.md)                                    | <span data-ttu-id="ff2fd-114">Passa i dati alla struttura [**WSAQUERYSET**](winsock-nsp-reference-links.md) durante le chiamate a diverse funzioni.</span><span class="sxs-lookup"><span data-stu-id="ff2fd-114">Passes data to the [**WSAQUERYSET**](winsock-nsp-reference-links.md) structure during calls to several functions.</span></span>                                                  |
| [<span data-ttu-id="ff2fd-115">PNRP e WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="ff2fd-115">PNRP and WSAQUERYSET</span></span>](pnrp-and-wsaqueryset.md)                      | <span data-ttu-id="ff2fd-116">Semplifica la risoluzione dei nomi e l'enumerazione di nomi e cloud.</span><span class="sxs-lookup"><span data-stu-id="ff2fd-116">Facilitates the resolving of names and the enumeration of names and clouds.</span></span>                                                                                         |
| [<span data-ttu-id="ff2fd-117">**\_ID Cloud \_ PNRP**</span><span class="sxs-lookup"><span data-stu-id="ff2fd-117">**PNRP\_CLOUD\_ID**</span></span>](/windows/desktop/api/Pnrpdef/ns-pnrpdef-pnrp_cloud_id)                              | <span data-ttu-id="ff2fd-118">Contiene i valori che definiscono un cloud di rete.</span><span class="sxs-lookup"><span data-stu-id="ff2fd-118">Contains the values that define a network cloud.</span></span>                                                                                                                    |
| [<span data-ttu-id="ff2fd-119">**PNRPCLOUDINFO**</span><span class="sxs-lookup"><span data-stu-id="ff2fd-119">**PNRPCLOUDINFO**</span></span>](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo)                                | <span data-ttu-id="ff2fd-120">A cui fa riferimento il membro **lpBlob** della struttura [**WSAQUERYSET**](winsock-nsp-reference-links.md) .</span><span class="sxs-lookup"><span data-stu-id="ff2fd-120">Pointed to by the **lpBlob** member of the [**WSAQUERYSET**](winsock-nsp-reference-links.md) structure.</span></span>                                                            |
| [<span data-ttu-id="ff2fd-121">**PNRPINFO \_ V1**</span><span class="sxs-lookup"><span data-stu-id="ff2fd-121">**PNRPINFO\_V1**</span></span>](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)                                      | <span data-ttu-id="ff2fd-122">A cui fa riferimento il membro **lpBlob** della struttura [**WSAQUERYSET**](winsock-nsp-reference-links.md)</span><span class="sxs-lookup"><span data-stu-id="ff2fd-122">Pointed to by the **lpBlob** member of the [**WSAQUERYSET**](winsock-nsp-reference-links.md) structure</span></span>                                                             |
| <span data-ttu-id="ff2fd-123">[**PNRPINFO \_ v2**](/previous-versions/windows/desktop/legacy/aa371671(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ff2fd-123">[**PNRPINFO\_V2**](/previous-versions/windows/desktop/legacy/aa371671(v=vs.85))</span></span>                                   | <span data-ttu-id="ff2fd-124">A cui fa riferimento il membro **lpBlob** della struttura [**WSAQUERYSET**](winsock-nsp-reference-links.md) e fornisce il supporto per i dati opachi specifici dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ff2fd-124">Pointed to by the **lpBlob** member of the [**WSAQUERYSET**](winsock-nsp-reference-links.md) structure, and provides support for application-specific opaque data.</span></span> |



 

 

 
