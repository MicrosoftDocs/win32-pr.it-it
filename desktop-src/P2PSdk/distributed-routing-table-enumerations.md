---
description: Le enumerazioni seguenti supportano l'API DRT (Distributed routing table).
ms.assetid: 38ce95a0-1603-42c2-8a5e-4370f52c8fc9
title: Enumerazioni tabella di routing distribuita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c432b156a9299a9f70026a394a6fd97f06528a25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312287"
---
# <a name="distributed-routing-table-enumerations"></a><span data-ttu-id="d0c86-103">Enumerazioni tabella di routing distribuita</span><span class="sxs-lookup"><span data-stu-id="d0c86-103">Distributed Routing Table Enumerations</span></span>

<span data-ttu-id="d0c86-104">Le enumerazioni seguenti supportano l'API DRT (Distributed routing table).</span><span class="sxs-lookup"><span data-stu-id="d0c86-104">The following enumerations support the Distributed Routing Table (DRT) API.</span></span>



| <span data-ttu-id="d0c86-105">Enumerazione</span><span class="sxs-lookup"><span data-stu-id="d0c86-105">Enumeration</span></span>                                                            | <span data-ttu-id="d0c86-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d0c86-106">Description</span></span>                                                                                                                                                           |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d0c86-107">**\_ambito DRT**</span><span class="sxs-lookup"><span data-stu-id="d0c86-107">**DRT\_SCOPE**</span></span>](/windows/desktop/api/drt/ne-drt-drt_scope)                                        | <span data-ttu-id="d0c86-108">Definisce il set di ambiti IPv6 in cui DRT funzionerà quando si utilizza il trasporto UDP IPv6 creato da [**DrtCreateIpv6UdpTransport**](/windows/desktop/api/drt/nf-drt-drtcreateipv6udptransport).</span><span class="sxs-lookup"><span data-stu-id="d0c86-108">Defines the set of IPv6 scopes in which DRT will operate when using the IPv6 UDP transport created by [**DrtCreateIpv6UdpTransport**](/windows/desktop/api/drt/nf-drt-drtcreateipv6udptransport).</span></span> |
| [<span data-ttu-id="d0c86-109">**\_flag indirizzi \_ DRT**</span><span class="sxs-lookup"><span data-stu-id="d0c86-109">**DRT\_ADDRESS\_FLAGS**</span></span>](/windows/desktop/api/drt/ne-drt-drt_address_flags)                       | <span data-ttu-id="d0c86-110">Definisce il set di risposte che possono essere restituite da un nodo intermedio durante l'esecuzione di una ricerca di una chiave.</span><span class="sxs-lookup"><span data-stu-id="d0c86-110">Defines the set of responses that may be returned by an intermediate node when performing a search for a key.</span></span>                                                         |
| [<span data-ttu-id="d0c86-111">**\_stato DRT**</span><span class="sxs-lookup"><span data-stu-id="d0c86-111">**DRT\_STATUS**</span></span>](/windows/desktop/api/drt/ne-drt-drt_status)                                      | <span data-ttu-id="d0c86-112">Definisce i possibili stati di connettività e di errore di un nodo locale.</span><span class="sxs-lookup"><span data-stu-id="d0c86-112">Defines the possible connectivity and error states of a local node.</span></span>                                                                                                   |
| [<span data-ttu-id="d0c86-113">**\_tipo di corrispondenza DRT \_**</span><span class="sxs-lookup"><span data-stu-id="d0c86-113">**DRT\_MATCH\_TYPE**</span></span>](/windows/desktop/api/drt/ne-drt-drt_match_type)                             | <span data-ttu-id="d0c86-114">Definisce l'esattezza dei risultati restituiti quando viene eseguita una ricerca.</span><span class="sxs-lookup"><span data-stu-id="d0c86-114">Defines the exactness of results returned when a search is performed.</span></span>                                                                                                 |
| [<span data-ttu-id="d0c86-115">**\_tipo di \_ modifica della chiave LEAFSET \_ di DRT \_**</span><span class="sxs-lookup"><span data-stu-id="d0c86-115">**DRT\_LEAFSET\_KEY\_CHANGE\_TYPE**</span></span>](/windows/desktop/api/drt/ne-drt-drt_leafset_key_change_type) | <span data-ttu-id="d0c86-116">Definisce il set di tipi di modifiche che possono essere eseguiti su un nodo set foglia locale nella cache DRT locale.</span><span class="sxs-lookup"><span data-stu-id="d0c86-116">Defines the set of change types that can be performed on a local leaf set node in the local DRT cache.</span></span>                                                                |
| [<span data-ttu-id="d0c86-117">**\_tipo di evento DRT \_**</span><span class="sxs-lookup"><span data-stu-id="d0c86-117">**DRT\_EVENT\_TYPE**</span></span>](/windows/desktop/api/drt/ne-drt-drt_event_type)                             | <span data-ttu-id="d0c86-118">Definisce il set di eventi che possono essere generati da DRT.</span><span class="sxs-lookup"><span data-stu-id="d0c86-118">Defines the set of events that can be raised by the DRT.</span></span>                                                                                                              |
| [<span data-ttu-id="d0c86-119">**\_modalità di sicurezza DRT \_**</span><span class="sxs-lookup"><span data-stu-id="d0c86-119">**DRT\_SECURITY\_MODE**</span></span>](/windows/desktop/api/drt/ne-drt-drt_security_mode)                       | <span data-ttu-id="d0c86-120">Definisce le modalità di sicurezza possibili di DRT.</span><span class="sxs-lookup"><span data-stu-id="d0c86-120">Defines the possible security modes of the DRT.</span></span> <span data-ttu-id="d0c86-121">Questa enumerazione è un campo della struttura [**delle \_ Impostazioni DRT**](/windows/desktop/api/drt/ns-drt-drt_settings) .</span><span class="sxs-lookup"><span data-stu-id="d0c86-121">This enumeration is a field of the [**DRT\_SETTINGS**](/windows/desktop/api/drt/ns-drt-drt_settings) structure.</span></span>                                   |
| [<span data-ttu-id="d0c86-122">**\_stato di registrazione DRT \_**</span><span class="sxs-lookup"><span data-stu-id="d0c86-122">**DRT\_REGISTRATION\_STATE**</span></span>](/windows/desktop/api/drt/ne-drt-drt_registration_state)             | <span data-ttu-id="d0c86-123">Definisce lo stato di una chiave registrata.</span><span class="sxs-lookup"><span data-stu-id="d0c86-123">Defines the state of a registered key.</span></span>                                                                                                                                |



 

## <a name="related-topics"></a><span data-ttu-id="d0c86-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d0c86-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0c86-125">Strutture della tabella di routing distribuita</span><span class="sxs-lookup"><span data-stu-id="d0c86-125">Distributed Routing Table Structures</span></span>](distributed-routing-table-structures.md)
</dt> <dt>

[<span data-ttu-id="d0c86-126">Funzioni della tabella di routing distribuita</span><span class="sxs-lookup"><span data-stu-id="d0c86-126">Distributed Routing Table Functions</span></span>](distributed-routing-table-functions.md)
</dt> <dt>

[<span data-ttu-id="d0c86-127">Riferimento API Tabella routing distribuito</span><span class="sxs-lookup"><span data-stu-id="d0c86-127">Distributed Routing Table API Reference</span></span>](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



