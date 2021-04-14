---
title: Problemi multithread
description: Problemi multithread
ms.assetid: 17e74d2a-af4f-4188-89fa-b4f50abc424f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0910e1602d00d3429bb9e4c7a1667bf8113cd659
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104397007"
---
# <a name="multi-threaded-issues"></a><span data-ttu-id="33ffb-103">Problemi multithread</span><span class="sxs-lookup"><span data-stu-id="33ffb-103">Multi-Threaded Issues</span></span>

<span data-ttu-id="33ffb-104">OLE fornisce supporto per le applicazioni multithreading, consentendo alle applicazioni di effettuare chiamate OLE da più thread.</span><span class="sxs-lookup"><span data-stu-id="33ffb-104">OLE provides support for multithreaded applications, allowing applications to make OLE calls from multiple threads.</span></span> <span data-ttu-id="33ffb-105">Questo supporto multithreading è denominato modello di Apartment, è importante che tutti i componenti OLE che usano più thread seguano questo modello.</span><span class="sxs-lookup"><span data-stu-id="33ffb-105">This multithreaded support is called the apartment model, it is important that all OLE components using multiple threads follow this model.</span></span> <span data-ttu-id="33ffb-106">Il modello di Apartment richiede che i puntatori di interfaccia vengano sottoposti a marshalling (tramite [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface)e [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface)) quando vengono passati tra thread.</span><span class="sxs-lookup"><span data-stu-id="33ffb-106">The apartment model requires that interface pointers are marshaled (using [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface), and [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface)) when passed between threads.</span></span>

## <a name="related-topics"></a><span data-ttu-id="33ffb-107">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="33ffb-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33ffb-108">Processi, thread e Apartment</span><span class="sxs-lookup"><span data-stu-id="33ffb-108">Processes, Threads, and Apartments</span></span>](processes--threads--and-apartments.md)
</dt> </dl>

 

 




