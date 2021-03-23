---
title: Tabelle descrittore
description: Una tabella descrittore è logicamente una matrice di descrittori.
ms.assetid: 5faf294f-acd5-4b39-92f4-1d6b2abe3040
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10414f8458006029f3279203e949b43410911fd5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "74105160"
---
# <a name="descriptor-tables"></a><span data-ttu-id="46276-103">Tabelle descrittore</span><span class="sxs-lookup"><span data-stu-id="46276-103">Descriptor Tables</span></span>

<span data-ttu-id="46276-104">Una tabella descrittore è logicamente una matrice di descrittori.</span><span class="sxs-lookup"><span data-stu-id="46276-104">A descriptor table is logically an array of descriptors.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="46276-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="46276-105">In this section</span></span>



| <span data-ttu-id="46276-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="46276-106">Topic</span></span>                                                                                 | <span data-ttu-id="46276-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="46276-107">Description</span></span>                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="46276-108">Cenni preliminari sulle tabelle descrittori</span><span class="sxs-lookup"><span data-stu-id="46276-108">Descriptor Tables Overview</span></span>](descriptor-tables-overview.md)<br/>               | <span data-ttu-id="46276-109">Ogni tabella dei descrittori archivia i descrittori di uno o più tipi, ovvero SRVs, UAVe, CBVs e Samplers.</span><span class="sxs-lookup"><span data-stu-id="46276-109">Each descriptor table stores descriptors of one or more types - SRVs, UAVe, CBVs, and Samplers.</span></span> <span data-ttu-id="46276-110">Una tabella descrittore non è un'allocazione di memoria; è semplicemente un offset e una lunghezza in un heap del descrittore.</span><span class="sxs-lookup"><span data-stu-id="46276-110">A descriptor table is not an allocation of memory; it is simply an offset and length into a descriptor heap.</span></span><br/> |
| [<span data-ttu-id="46276-111">Utilizzo di tabelle descrittore</span><span class="sxs-lookup"><span data-stu-id="46276-111">Using Descriptor Tables</span></span>](using-descriptor-tables.md)<br/>                     | <span data-ttu-id="46276-112">Le tabelle dei descrittori, ciascuna delle quali identifica un intervallo in un heap descrittore, vengono associate agli slot definiti dalla firma radice corrente in un elenco di comandi.</span><span class="sxs-lookup"><span data-stu-id="46276-112">Descriptor tables, each identifying a range in a descriptor heap, are bound at slots defined by the current root signature on a command list.</span></span> <br/>                                                               |
| [<span data-ttu-id="46276-113">Uso avanzato di tabelle di descrittori</span><span class="sxs-lookup"><span data-stu-id="46276-113">Advanced Use of Descriptor Tables</span></span>](advanced-use-of-descriptor-tables.md)<br/> | <span data-ttu-id="46276-114">Nelle sezioni seguenti vengono fornite informazioni sull'utilizzo avanzato delle tabelle dei descrittori.</span><span class="sxs-lookup"><span data-stu-id="46276-114">The following sections provide information about the advanced use of descriptor tables.</span></span><br/>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="46276-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="46276-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46276-116">Heap descrittore</span><span class="sxs-lookup"><span data-stu-id="46276-116">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> <dt>

[<span data-ttu-id="46276-117">Associazione di risorse</span><span class="sxs-lookup"><span data-stu-id="46276-117">Resource Binding</span></span>](resource-binding.md)
</dt> <dt>

[<span data-ttu-id="46276-118">Firme radice</span><span class="sxs-lookup"><span data-stu-id="46276-118">Root Signatures</span></span>](root-signatures.md)
</dt> </dl>

 

 





