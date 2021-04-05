---
title: Considerazioni sull'implementazione di IPropertySetStorage
description: Molti problemi si verificano quando si considera come fornire un'implementazione dell'interfaccia IPropertySetStorage che legge e scrive il formato del set di proprietà COM. Le sezioni seguenti descrivono queste considerazioni.
ms.assetid: 055da516-ed42-49ec-b20c-a5e98718bea8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f7532211668fa1ecf290484a707b19e1c263b9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712739"
---
# <a name="ipropertysetstorage-implementation-considerations"></a><span data-ttu-id="49ae2-104">Considerazioni sull'implementazione di IPropertySetStorage</span><span class="sxs-lookup"><span data-stu-id="49ae2-104">IPropertySetStorage Implementation Considerations</span></span>

<span data-ttu-id="49ae2-105">Molti problemi si verificano quando si considera come fornire un'implementazione dell'interfaccia [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) che legge e scrive il formato del set di proprietà com.</span><span class="sxs-lookup"><span data-stu-id="49ae2-105">Several issues arise when considering how to provide an implementation of the [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) interface that reads and writes the COM property set format.</span></span> <span data-ttu-id="49ae2-106">Le sezioni seguenti descrivono queste considerazioni.</span><span class="sxs-lookup"><span data-stu-id="49ae2-106">The following sections describe these considerations.</span></span>

-   [<span data-ttu-id="49ae2-107">Nomi in IStorage</span><span class="sxs-lookup"><span data-stu-id="49ae2-107">Names in IStorage</span></span>](names-in-istorage.md)
-   [<span data-ttu-id="49ae2-108">Oggetti di archiviazione e di flusso per un set di proprietà</span><span class="sxs-lookup"><span data-stu-id="49ae2-108">Storage and Stream Objects for a Property Set</span></span>](storage-vs--stream-for-a-property-set.md)
-   [<span data-ttu-id="49ae2-109">Impostazione dell'identificatore di classe del set di proprietà</span><span class="sxs-lookup"><span data-stu-id="49ae2-109">Setting the Property Set Class Identifier</span></span>](setting-the-property-set-class-identifier.md)
-   [<span data-ttu-id="49ae2-110">Punti di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="49ae2-110">Synchronization Points</span></span>](synchronization-points.md)
-   [<span data-ttu-id="49ae2-111">Tabelle codici e stringhe Unicode</span><span class="sxs-lookup"><span data-stu-id="49ae2-111">Code Pages and Unicode Strings</span></span>](code-pages-and-unicode-strings.md)
-   [<span data-ttu-id="49ae2-112">Dizionario</span><span class="sxs-lookup"><span data-stu-id="49ae2-112">Dictionary</span></span>](dictionary.md)
-   [<span data-ttu-id="49ae2-113">Estensioni</span><span class="sxs-lookup"><span data-stu-id="49ae2-113">Extensions</span></span>](extensions.md)
-   [<span data-ttu-id="49ae2-114">Serializzazione del set di proprietà</span><span class="sxs-lookup"><span data-stu-id="49ae2-114">Property Set Serialization</span></span>](version-0-vs--version-1-property-set-serialization.md)

<span data-ttu-id="49ae2-115">Per ulteriori informazioni, vedere [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) nella sezione di riferimento in Interfaces.</span><span class="sxs-lookup"><span data-stu-id="49ae2-115">For more information, see [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) in the Reference section under Interfaces.</span></span>

 

 




