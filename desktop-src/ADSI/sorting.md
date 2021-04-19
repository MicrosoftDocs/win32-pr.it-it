---
title: Ordinamento (ADSI)
description: Un client può richiedere un server per ordinare il set di risultati.
ms.assetid: 795d27f0-0bfa-417e-aa1f-f2471f92dc45
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e4ee790a646367366afe33639abd8f5aa57ed4f
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/11/2019
ms.locfileid: "106299323"
---
# <a name="sorting-adsi"></a><span data-ttu-id="19e8f-103">Ordinamento (ADSI)</span><span class="sxs-lookup"><span data-stu-id="19e8f-103">Sorting (ADSI)</span></span>

<span data-ttu-id="19e8f-104">Un client può richiedere un server per ordinare il set di risultati.</span><span class="sxs-lookup"><span data-stu-id="19e8f-104">A client can request a server to sort the result set.</span></span> <span data-ttu-id="19e8f-105">È possibile specificare:</span><span class="sxs-lookup"><span data-stu-id="19e8f-105">You can specify:</span></span>

-   <span data-ttu-id="19e8f-106">Tipo di ordinamento: è possibile specificare l'ordinamento crescente o decrescente.</span><span class="sxs-lookup"><span data-stu-id="19e8f-106">Sort order: Either ascending or descending sort order can be specified.</span></span>
-   <span data-ttu-id="19e8f-107">Attributi di ordinamento: è possibile specificare più attributi in una stringa di ordinamento.</span><span class="sxs-lookup"><span data-stu-id="19e8f-107">Sort attributes: Multiple attributes can be specified in a sort string.</span></span> <span data-ttu-id="19e8f-108">Ad esempio, Ordina in base al cognome e quindi al nome.</span><span class="sxs-lookup"><span data-stu-id="19e8f-108">For example, sort by Last Name, then First Name.</span></span>

<span data-ttu-id="19e8f-109">Quando si specifica l'ordinamento, provare a usare uno degli attributi indicizzati.</span><span class="sxs-lookup"><span data-stu-id="19e8f-109">When you specify sort order, you should try to use one of the indexed attributes.</span></span> <span data-ttu-id="19e8f-110">In caso contrario, è necessario che il server calcoli un set di risultati completo prima di inviarlo al client.</span><span class="sxs-lookup"><span data-stu-id="19e8f-110">Otherwise, the server must calculate a complete result set before sending it to the client.</span></span> <span data-ttu-id="19e8f-111">Questo vale anche se è stata richiesta una ricerca di paging e sono state specificate le dimensioni della pagina.</span><span class="sxs-lookup"><span data-stu-id="19e8f-111">This is true even if you have requested a paged search and specified a page size.</span></span>

> [!Note]  
> <span data-ttu-id="19e8f-112">Non tutti i server di directory supportano più tipi di attributi o ordinamento.</span><span class="sxs-lookup"><span data-stu-id="19e8f-112">Not all directory servers support multiple attribute sorts or sort order.</span></span>

 

 

 




