---
description: Le strutture seguenti supportano le funzioni API della tabella di routing distribuita (DRT).
ms.assetid: 3ff85b24-5ec0-4b26-b30e-1bf8030a575d
title: Strutture della tabella di routing distribuita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d454d2c28008422da897dc91ca9a3dc29db374b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312284"
---
# <a name="distributed-routing-table-structures"></a><span data-ttu-id="8887e-103">Strutture della tabella di routing distribuita</span><span class="sxs-lookup"><span data-stu-id="8887e-103">Distributed Routing Table Structures</span></span>

<span data-ttu-id="8887e-104">Le strutture seguenti supportano le funzioni API della tabella di routing distribuita (DRT).</span><span class="sxs-lookup"><span data-stu-id="8887e-104">The following structures support the Distributed Routing Table (DRT) API functions.</span></span>



| <span data-ttu-id="8887e-105">Struttura</span><span class="sxs-lookup"><span data-stu-id="8887e-105">Structure</span></span>                                                  | <span data-ttu-id="8887e-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8887e-106">Description</span></span>                                                                                                                                                                              |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8887e-107">**\_dati DRT**</span><span class="sxs-lookup"><span data-stu-id="8887e-107">**DRT\_DATA**</span></span>](/windows/desktop/api/drt/ns-drt-drt_data)                              | <span data-ttu-id="8887e-108">Contiene un BLOB di dati.</span><span class="sxs-lookup"><span data-stu-id="8887e-108">Contains a data blob.</span></span> <span data-ttu-id="8887e-109">Questa struttura viene utilizzata da diverse funzioni DRT.</span><span class="sxs-lookup"><span data-stu-id="8887e-109">This structure is used by several DRT functions.</span></span>                                                                                                                   |
| [<span data-ttu-id="8887e-110">**\_registrazione DRT**</span><span class="sxs-lookup"><span data-stu-id="8887e-110">**DRT\_REGISTRATION**</span></span>](/windows/desktop/api/drt/ns-drt-drt_registration)              | <span data-ttu-id="8887e-111">Contiene la registrazione della chiave.</span><span class="sxs-lookup"><span data-stu-id="8887e-111">Contains the key registration.</span></span> <span data-ttu-id="8887e-112">Si tratta di un membro della struttura dei [**\_ \_ risultati di ricerca DRT**](/windows/desktop/api/drt/ns-drt-drt_search_result) e è un argomento passato a [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey).</span><span class="sxs-lookup"><span data-stu-id="8887e-112">This is a member of the [**DRT\_SEARCH\_RESULT**](/windows/desktop/api/drt/ns-drt-drt_search_result) structure and is an argument passed to [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey).</span></span> |
| [<span data-ttu-id="8887e-113">**\_Indirizzo DRT**</span><span class="sxs-lookup"><span data-stu-id="8887e-113">**DRT\_ADDRESS**</span></span>](/windows/desktop/api/drt/ns-drt-drt_address)                        | <span data-ttu-id="8887e-114">Contiene informazioni sull'endpoint di un nodo DRT che ha partecipato a una ricerca.</span><span class="sxs-lookup"><span data-stu-id="8887e-114">Contains endpoint information about a DRT node that participated in a search.</span></span> <span data-ttu-id="8887e-115">Queste informazioni sono destinate all'uso nel debug di problemi di connettività.</span><span class="sxs-lookup"><span data-stu-id="8887e-115">This information is intended for use in debugging connectivity problems.</span></span>                                   |
| [<span data-ttu-id="8887e-116">**\_elenco indirizzi \_ DRT**</span><span class="sxs-lookup"><span data-stu-id="8887e-116">**DRT\_ADDRESS\_LIST**</span></span>](/windows/desktop/api/drt/ns-drt-drt_address_list)             | <span data-ttu-id="8887e-117">Contiene un set di strutture di [**\_ indirizzi DRT**](/windows/desktop/api/drt/ns-drt-drt_address) che rappresentano i nodi contattati durante la ricerca di una chiave.</span><span class="sxs-lookup"><span data-stu-id="8887e-117">Contains a set of [**DRT\_ADDRESS**](/windows/desktop/api/drt/ns-drt-drt_address) structures representing the nodes contacted during a search for a key.</span></span>                                                             |
| [<span data-ttu-id="8887e-118">**\_provider di sicurezza DRT \_**</span><span class="sxs-lookup"><span data-stu-id="8887e-118">**DRT\_SECURITY\_PROVIDER**</span></span>](/windows/desktop/api/Drt/ns-drt-drt_security_provider)   | <span data-ttu-id="8887e-119">Definisce l'interfaccia che deve essere implementata da un provider di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="8887e-119">Defines the interface that must be implemented by a security provider.</span></span>                                                                                                                   |
| [<span data-ttu-id="8887e-120">**\_provider bootstrap \_ DRT**</span><span class="sxs-lookup"><span data-stu-id="8887e-120">**DRT\_BOOTSTRAP\_PROVIDER**</span></span>](/windows/desktop/api/drt/ns-drt-drt_bootstrap_provider) | <span data-ttu-id="8887e-121">Definisce l'interfaccia che deve essere implementata da un provider bootstrap.</span><span class="sxs-lookup"><span data-stu-id="8887e-121">Defines the interface that must be implemented by a bootstrap provider.</span></span>                                                                                                                  |
| [<span data-ttu-id="8887e-122">**\_Impostazioni DRT**</span><span class="sxs-lookup"><span data-stu-id="8887e-122">**DRT\_SETTINGS**</span></span>](/windows/desktop/api/drt/ns-drt-drt_settings)                      | <span data-ttu-id="8887e-123">Definisce le impostazioni di DRT durante l'inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="8887e-123">Defines DRT settings at initialization.</span></span> <span data-ttu-id="8887e-124">Questa struttura viene passata come argomento a [**DrtOpen**](/windows/desktop/api/drt/nf-drt-drtopen).</span><span class="sxs-lookup"><span data-stu-id="8887e-124">This structure is passed as an argument to [**DrtOpen**](/windows/desktop/api/drt/nf-drt-drtopen).</span></span>                                                                           |
| [<span data-ttu-id="8887e-125">**\_informazioni di ricerca DRT \_**</span><span class="sxs-lookup"><span data-stu-id="8887e-125">**DRT\_SEARCH\_INFO**</span></span>](/windows/desktop/api/drt/ns-drt-drt_search_info)               | <span data-ttu-id="8887e-126">Definisce una query di ricerca.</span><span class="sxs-lookup"><span data-stu-id="8887e-126">Defines a search query.</span></span> <span data-ttu-id="8887e-127">Questa struttura viene passata come argomento a [**DrtStartSearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch).</span><span class="sxs-lookup"><span data-stu-id="8887e-127">This structure is passed as an argument to [**DrtStartSearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch).</span></span>                                                                             |
| [<span data-ttu-id="8887e-128">**\_risultato della ricerca DRT \_**</span><span class="sxs-lookup"><span data-stu-id="8887e-128">**DRT\_SEARCH\_RESULT**</span></span>](/windows/desktop/api/drt/ns-drt-drt_search_result)           | <span data-ttu-id="8887e-129">Contiene un risultato della ricerca.</span><span class="sxs-lookup"><span data-stu-id="8887e-129">Contains a search result.</span></span> <span data-ttu-id="8887e-130">Questa struttura viene restituita da [**DrtGetSearchResult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult).</span><span class="sxs-lookup"><span data-stu-id="8887e-130">This structure is returned by [**DrtGetSearchResult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult).</span></span>                                                                                |
| [<span data-ttu-id="8887e-131">**\_dati evento \_ DRT**</span><span class="sxs-lookup"><span data-stu-id="8887e-131">**DRT\_EVENT\_DATA**</span></span>](/windows/desktop/api/drt/ns-drt-drt_event_data)                 | <span data-ttu-id="8887e-132">Contiene i dati dell'evento restituiti chiamando [**DrtGetEventData**](/windows/desktop/api/drt/nf-drt-drtgeteventdata) dopo che un'applicazione ha ricevuto un segnale di evento.</span><span class="sxs-lookup"><span data-stu-id="8887e-132">Contains the event data returned by calling [**DrtGetEventData**](/windows/desktop/api/drt/nf-drt-drtgeteventdata) after an application receives an event signal.</span></span>                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="8887e-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8887e-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8887e-134">Enumerazioni tabella di routing distribuita</span><span class="sxs-lookup"><span data-stu-id="8887e-134">Distributed Routing Table Enumerations</span></span>](distributed-routing-table-enumerations.md)
</dt> <dt>

[<span data-ttu-id="8887e-135">Funzioni della tabella di routing distribuita</span><span class="sxs-lookup"><span data-stu-id="8887e-135">Distributed Routing Table Functions</span></span>](distributed-routing-table-functions.md)
</dt> <dt>

[<span data-ttu-id="8887e-136">Riferimento API Tabella routing distribuito</span><span class="sxs-lookup"><span data-stu-id="8887e-136">Distributed Routing Table API Reference</span></span>](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



