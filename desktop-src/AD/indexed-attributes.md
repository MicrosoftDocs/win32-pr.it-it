---
title: Attributi indicizzati (AD DS)
description: Gli attributi possono essere indicizzati. L'indicizzazione di un attributo può migliorare le prestazioni delle query per tale attributo.
ms.assetid: 20e10fc9-d767-4d82-9ed6-b9f384e77b12
ms.tgt_platform: multiple
keywords:
- Attributi indicizzati AD
- Attributi AD, indicizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c280d5390d666b6b0f95f49972e4c569f046865b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "106299568"
---
# <a name="indexed-attributes-ad-ds"></a><span data-ttu-id="9ef58-106">Attributi indicizzati (AD DS)</span><span class="sxs-lookup"><span data-stu-id="9ef58-106">Indexed Attributes (AD DS)</span></span>

<span data-ttu-id="9ef58-107">Gli attributi possono essere indicizzati.</span><span class="sxs-lookup"><span data-stu-id="9ef58-107">Attributes may be indexed.</span></span> <span data-ttu-id="9ef58-108">L'indicizzazione di un attributo può migliorare le prestazioni delle query per tale attributo.</span><span class="sxs-lookup"><span data-stu-id="9ef58-108">Indexing an attribute can improve the performance of queries for that attribute.</span></span>

<span data-ttu-id="9ef58-109">Gli attributi vengono indicizzati quando l'attributo [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) nella definizione dello schema dell'attributo presenta il bit meno significativo impostato su 1.</span><span class="sxs-lookup"><span data-stu-id="9ef58-109">An attributes is indexed when the [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) attribute in the attribute's schema definition has the least significant bit set to 1.</span></span> <span data-ttu-id="9ef58-110">Impostando il bit meno significativo della definizione dello schema dell'attributo **searchFlags** su 1, viene compilato dinamicamente un indice.</span><span class="sxs-lookup"><span data-stu-id="9ef58-110">Setting the least significant bit of the **searchFlags** attribute schema definition to 1 will dynamically build an index.</span></span> <span data-ttu-id="9ef58-111">Impostando il bit meno significativo della definizione dello schema dell'attributo **searchFlags** su 0, l'indice per l'attributo verrà rimosso.</span><span class="sxs-lookup"><span data-stu-id="9ef58-111">Setting the least significant bit of the **searchFlags** attribute schema definition to 0 will cause the index for the attribute to be removed.</span></span> <span data-ttu-id="9ef58-112">L'indice verrà compilato automaticamente da un thread in background sul controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="9ef58-112">The index will be built automatically by a background thread on the domain controller.</span></span>

<span data-ttu-id="9ef58-113">Idealmente, gli attributi indicizzati devono essere a valore singolo con valori univoci distribuiti uniformemente nel set di istanze.</span><span class="sxs-lookup"><span data-stu-id="9ef58-113">Ideally, indexed attributes should be single valued with highly unique values evenly distributed across the set of instances.</span></span> <span data-ttu-id="9ef58-114">Meno univoci i valori di un attributo sono, minore sarà l'efficacia dell'indice.</span><span class="sxs-lookup"><span data-stu-id="9ef58-114">The less unique the values of an attribute are, the less effective the index will be.</span></span>

<span data-ttu-id="9ef58-115">Gli attributi multivalore possono anche essere indicizzati, ma il costo per compilare l'indice per un attributo multivalore è maggiore in termini di archiviazione, aggiornamento e tempo di ricerca.</span><span class="sxs-lookup"><span data-stu-id="9ef58-115">Multi-valued attributes can also be indexed, but the cost to build the index for a multi-valued attribute is larger in terms of storage, update, and search time.</span></span> <span data-ttu-id="9ef58-116">Il requisito di univocità per una proprietà multivalore è identico a quello di una proprietà a valore singolo, più univoco è l'indice più efficiente.</span><span class="sxs-lookup"><span data-stu-id="9ef58-116">The uniqueness requirement for a multi-valued property is the same as that for a single-valued property—the more unique the values are the more effective the index.</span></span>

<span data-ttu-id="9ef58-117">Maggiore è l'attributo indicizzato di una classe, maggiore è il tempo necessario per creare nuove istanze della classe.</span><span class="sxs-lookup"><span data-stu-id="9ef58-117">The more indexed attributes a class has, the more time is required to create new instances of the class.</span></span>

<span data-ttu-id="9ef58-118">Gli indici si applicano agli attributi, non alle classi.</span><span class="sxs-lookup"><span data-stu-id="9ef58-118">Indexes apply to attributes, not to classes.</span></span> <span data-ttu-id="9ef58-119">Ovvero, quando un attributo viene contrassegnato come indicizzato, tutte le istanze dell'attributo vengono aggiunte all'indice e non solo alle istanze che sono membri di una classe specifica.</span><span class="sxs-lookup"><span data-stu-id="9ef58-119">That is, when an attribute is marked as indexed, all instances of the attribute are added to the index, not just the instances that are members of a particular class.</span></span>

<span data-ttu-id="9ef58-120">Per verificare che un server utilizzi un indice per elaborare una query, impostare il seguente valore del registro di sistema su un controller di dominio su 4.</span><span class="sxs-lookup"><span data-stu-id="9ef58-120">To verify that a server is using an index to process a query, set the following registry value on a domain controller to 4.</span></span> <span data-ttu-id="9ef58-121">Eseguire quindi una query sul controller di dominio e cercare nel registro eventi della directory i dati sugli eventuali indici usati per elaborare la query.</span><span class="sxs-lookup"><span data-stu-id="9ef58-121">Then perform a query on that domain controller and look in the directory event log for data about the indexes, if any, used to process the query.</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      Current Control Set
         Services
            NTDS
               Diagnostics
                  9 Internal Processing
```

<span data-ttu-id="9ef58-122">Per ulteriori informazioni sugli altri bit della proprietà [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) , vedere [caratteristiche degli attributi](characteristics-of-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="9ef58-122">For more information about other bits in the [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) property, see [Characteristics of Attributes](characteristics-of-attributes.md).</span></span>

 

 