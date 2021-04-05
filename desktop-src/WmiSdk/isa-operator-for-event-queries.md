---
description: L'operatore ISA è un operatore specifico di WQL che può essere usato nelle query di eventi. Quando ISA è incluso nella clausola WHERE di una query di eventi, richiede la notifica degli eventi per tutte le classi all'interno di una gerarchia di classi, anziché una specifica classe di evento.
ms.assetid: 68b7a903-a206-4491-95c4-4a412537f6f5
ms.tgt_platform: multiple
title: Operatore ISA per le query di eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0acdd262492bfd876867bdfa7e13fd50e5380270
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057953"
---
# <a name="isa-operator-for-event-queries"></a><span data-ttu-id="3f4f9-104">Operatore ISA per le query di eventi</span><span class="sxs-lookup"><span data-stu-id="3f4f9-104">ISA Operator for Event Queries</span></span>

<span data-ttu-id="3f4f9-105">L'operatore ISA è un operatore specifico di WQL che può essere usato nelle query di eventi.</span><span class="sxs-lookup"><span data-stu-id="3f4f9-105">The ISA operator is a WQL-specific operator that can be used in event queries.</span></span> <span data-ttu-id="3f4f9-106">Quando ISA è incluso nella [clausola WHERE](where-clause.md) di una query di eventi, richiede la notifica degli eventi per tutte le classi all'interno di una gerarchia di classi, anziché una specifica classe di evento.</span><span class="sxs-lookup"><span data-stu-id="3f4f9-106">When ISA is included in the [WHERE clause](where-clause.md) of an event query, it requests notification of events for all classes within a class hierarchy, rather than a specific event class.</span></span>

<span data-ttu-id="3f4f9-107">Nell'esempio seguente viene richiesta la notifica ogni 10 minuti di eventi di modifica dell'istanza per tutte le istanze che sono membri di qualsiasi classe derivata dalla classe [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="3f4f9-107">The following example requests notification every 10 minutes of instance modification events for all instances that are members of any class derived from the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span>


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 600
WHERE TargetInstance ISA "Win32_LogicalDisk"
```



<span data-ttu-id="3f4f9-108">Per altre informazioni sull'uso di ISA con una query di eventi, vedere [creazione di un evento timer con Win32 \_ LocalTime o Win32 \_ UTCTime](./creating-a-timer-event-with-win32-localtime-or-win32-utctime.md).</span><span class="sxs-lookup"><span data-stu-id="3f4f9-108">For more information on using ISA with an event query, see [Creating a Timer Event with Win32\_LocalTime or Win32\_UTCTime](./creating-a-timer-event-with-win32-localtime-or-win32-utctime.md).</span></span>

 

 
