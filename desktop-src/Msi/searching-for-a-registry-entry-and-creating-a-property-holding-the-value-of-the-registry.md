---
description: Durante un'installazione di Windows Installer, il programma di installazione può cercare una voce del registro di sistema e creare una proprietà contenente il valore del registro di sistema.
ms.assetid: 3a663fc7-cdcf-4ac3-8251-836ba0d3cc11
title: Ricerca di una voce del registro di sistema e creazione di una proprietà contenente il valore del registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82bd7572c0176f4870eed199800715190d9bbbf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878682"
---
# <a name="searching-for-a-registry-entry-and-creating-a-property-holding-the-value-of-the-registry"></a><span data-ttu-id="469ee-103">Ricerca di una voce del registro di sistema e creazione di una proprietà contenente il valore del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="469ee-103">Searching for a Registry Entry and Creating a Property Holding the Value of the Registry</span></span>

<span data-ttu-id="469ee-104">**Per cercare una voce del registro di sistema e creare una proprietà contenente il valore di tale file**</span><span class="sxs-lookup"><span data-stu-id="469ee-104">**To search for a registry entry and create a property holding the value of that file**</span></span>

1.  <span data-ttu-id="469ee-105">Non aggiungere la firma alla tabella della [firma](signature-table.md) o alla [tabella CompLocator](complocator-table.md).</span><span class="sxs-lookup"><span data-stu-id="469ee-105">Do not add the signature to the [Signature Table](signature-table.md) or the [CompLocator Table](complocator-table.md).</span></span> <span data-ttu-id="469ee-106">Se la firma di un file è elencata nella [tabella AppSearch](appsearch-table.md) e non è elencata nelle tabelle Signature o CompLocator, il programma di installazione cerca nella [tabella RegLocator](reglocator-table.md).</span><span class="sxs-lookup"><span data-stu-id="469ee-106">If a file signature is listed in the [AppSearch Table](appsearch-table.md) and is not listed in the Signature or CompLocator tables, the Installer looks in the [RegLocator Table](reglocator-table.md).</span></span>

2.  <span data-ttu-id="469ee-107">Consente di specificare la voce del registro di sistema da cercare nella [tabella RegLocator](reglocator-table.md).</span><span class="sxs-lookup"><span data-stu-id="469ee-107">Specify the registry entry to be searched for in the [RegLocator Table](reglocator-table.md).</span></span> <span data-ttu-id="469ee-108">Se la firma è assente dalla [tabella di firma](signature-table.md) e il valore della colonna del tipo è **msidbLocatorTypeRawValue**, si presuppone che la ricerca sia per il nome della chiave del registro di sistema a cui punta la tabella RegLocator.</span><span class="sxs-lookup"><span data-stu-id="469ee-108">If the signature is absent from the [Signature Table](signature-table.md) and the value of the Type column is **msidbLocatorTypeRawValue**, then the search is assumed to be for the specific registry key name pointed to by the RegLocator Table.</span></span>

    <span data-ttu-id="469ee-109">[Tabella RegLocator](reglocator-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="469ee-109">[RegLocator Table](reglocator-table.md) (partial)</span></span>

    

    | <span data-ttu-id="469ee-110">Firma\_</span><span class="sxs-lookup"><span data-stu-id="469ee-110">Signature\_</span></span>         | <span data-ttu-id="469ee-111">Radice</span><span class="sxs-lookup"><span data-stu-id="469ee-111">Root</span></span>         | <span data-ttu-id="469ee-112">Codice</span><span class="sxs-lookup"><span data-stu-id="469ee-112">Key</span></span>                                                           | <span data-ttu-id="469ee-113">Nome</span><span class="sxs-lookup"><span data-stu-id="469ee-113">Name</span></span>                  | <span data-ttu-id="469ee-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="469ee-114">Type</span></span>                                    |
    |---------------------|--------------|---------------------------------------------------------------|-----------------------|-----------------------------------------|
    | <span data-ttu-id="469ee-115">AppValue</span><span class="sxs-lookup"><span data-stu-id="469ee-115">AppValue</span></span><br/> | <span data-ttu-id="469ee-116">2</span><span class="sxs-lookup"><span data-stu-id="469ee-116">2</span></span><br/> | <span data-ttu-id="469ee-117">**Software** \\ di **Microsoft** \\ **MyApp**</span><span class="sxs-lookup"><span data-stu-id="469ee-117">**SOFTWARE**\\**Microsoft**\\**MyApp**</span></span><br/> <br/> | <span data-ttu-id="469ee-118">**Myname**</span><span class="sxs-lookup"><span data-stu-id="469ee-118">**Myname**</span></span><br/> | <span data-ttu-id="469ee-119">**msidbLocatorTypeRawValue**</span><span class="sxs-lookup"><span data-stu-id="469ee-119">**msidbLocatorTypeRawValue**</span></span><br/> |

    

     

3.  <span data-ttu-id="469ee-120">Infine, popolare la [tabella AppSearch](appsearch-table.md) in modo che l' [azione AppSearch](appsearch-action.md) restituisce il valore di AppValue.</span><span class="sxs-lookup"><span data-stu-id="469ee-120">Finally, populate the [AppSearch Table](appsearch-table.md) so that the [AppSearch Action](appsearch-action.md) returns the value of AppValue.</span></span> <span data-ttu-id="469ee-121">Dopo che il programma di installazione ha eseguito l'azione AppSearch, il valore di MYREGVAL corrisponde al valore di AppValue.</span><span class="sxs-lookup"><span data-stu-id="469ee-121">After the Installer executes the AppSearch Action, the value of MYREGVAL is the value of AppValue.</span></span>

    <span data-ttu-id="469ee-122">[Tabella AppSearch](appsearch-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="469ee-122">[AppSearch Table](appsearch-table.md) (partial)</span></span>

    

    | <span data-ttu-id="469ee-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="469ee-123">Property</span></span>            | <span data-ttu-id="469ee-124">Firma</span><span class="sxs-lookup"><span data-stu-id="469ee-124">Signature</span></span>           |
    |---------------------|---------------------|
    | <span data-ttu-id="469ee-125">MYREGVAL</span><span class="sxs-lookup"><span data-stu-id="469ee-125">MYREGVAL</span></span><br/> | <span data-ttu-id="469ee-126">AppValue</span><span class="sxs-lookup"><span data-stu-id="469ee-126">AppValue</span></span><br/> |

    

     

 

 




