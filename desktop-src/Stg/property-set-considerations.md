---
title: Considerazioni sui set di proprietà
description: È consigliabile mantenere piccoli i set di proprietà perché il flusso del set di proprietà viene letto in memoria prima che una singola proprietà possa essere letta o scritta.
ms.assetid: 520db05e-81cd-40ef-af89-471d7194c634
keywords:
- Considerazioni sui set di proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ddfd89140092b13d113122ffe1c1a2b576e654c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714560"
---
# <a name="property-set-considerations"></a><span data-ttu-id="deca5-104">Considerazioni sui set di proprietà</span><span class="sxs-lookup"><span data-stu-id="deca5-104">Property Set Considerations</span></span>

<span data-ttu-id="deca5-105">È consigliabile mantenere piccoli i set di proprietà perché il flusso del set di proprietà viene letto in memoria prima che una singola proprietà possa essere letta o scritta.</span><span class="sxs-lookup"><span data-stu-id="deca5-105">It is strongly recommended that property sets be kept small because the property set stream is read into memory before a single property can be read or written.</span></span> <span data-ttu-id="deca5-106">"Small" significa meno di 32 kilobyte di dati.</span><span class="sxs-lookup"><span data-stu-id="deca5-106">"small" means less than 32 kilobytes of data.</span></span> <span data-ttu-id="deca5-107">Questo raramente presenta un problema perché, in genere, le proprietà "inline" saranno elementi piccoli, ad esempio stringhe descrittive, parole chiave, timestamp, conteggi, nomi di autore, identificatori univoci globali (GUID), identificatori di classe (CLSID) e così via.</span><span class="sxs-lookup"><span data-stu-id="deca5-107">This rarely presents a problem because typically, "in-line" properties will be small items such as descriptive strings, keywords, time stamps, counts, author names, globally unique identifiers (GUIDs), class identifiers (CLSIDs), and so forth.</span></span>

<span data-ttu-id="deca5-108">Per archiviare blocchi di dati di dimensioni maggiori o nei casi in cui la dimensione totale di un set di proprietà correlate supera la quantità consigliata, è consigliabile utilizzare tipi non semplici come **il \_ flusso di VT** e l' **\_ archiviazione VT** .</span><span class="sxs-lookup"><span data-stu-id="deca5-108">To store larger chunks of data, or in cases where the total size of a set of related properties far exceeds the recommended amount, the use of nonsimple types such as **VT\_STREAM** and **VT\_STORAGE** are strongly recommended.</span></span> <span data-ttu-id="deca5-109">Questi elementi non vengono archiviati all'interno del flusso del set di proprietà, pertanto non influiscono significativamente sul sovraccarico iniziale del primo accesso e della scrittura di una proprietà.</span><span class="sxs-lookup"><span data-stu-id="deca5-109">These are not stored within the property set stream, so they do not significantly affect the initial overhead of the first accessing and writing of a property.</span></span> <span data-ttu-id="deca5-110">Il flusso del set di proprietà contiene un overhead minimo perché contiene il nome del flusso di pari livello o della proprietà con valori di archiviazione e questa operazione richiede una quantità di tempo minore per l'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="deca5-110">There is a minimal overhead as the property set stream contains the name of the sibling stream- or storage-valued property and this takes an additional small amount of time to process.</span></span>

<span data-ttu-id="deca5-111">Per altre informazioni, vedere:</span><span class="sxs-lookup"><span data-stu-id="deca5-111">For more information, see:</span></span>

-   [<span data-ttu-id="deca5-112">Considerazioni sull'implementazione di IPropertySetStorage</span><span class="sxs-lookup"><span data-stu-id="deca5-112">IPropertySetStorage Implementation Considerations</span></span>](ipropertysetstorage-implementation-considerations.md)
-   [<span data-ttu-id="deca5-113">Archiviazione di set di proprietà</span><span class="sxs-lookup"><span data-stu-id="deca5-113">Storing Property Sets</span></span>](storing-property-sets.md)
-   [<span data-ttu-id="deca5-114">Caratteristiche di prestazioni</span><span class="sxs-lookup"><span data-stu-id="deca5-114">Performance Characteristics</span></span>](performance-characteristics.md)
-   [<span data-ttu-id="deca5-115">Implementazione del set di proprietà informazioni di riepilogo</span><span class="sxs-lookup"><span data-stu-id="deca5-115">Implementing the Summary Information Property Set</span></span>](implementing-the-summary-information-property-set.md)

 

 




