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
# <a name="isa-operator-for-event-queries"></a>Operatore ISA per le query di eventi

L'operatore ISA è un operatore specifico di WQL che può essere usato nelle query di eventi. Quando ISA è incluso nella [clausola WHERE](where-clause.md) di una query di eventi, richiede la notifica degli eventi per tutte le classi all'interno di una gerarchia di classi, anziché una specifica classe di evento.

Nell'esempio seguente viene richiesta la notifica ogni 10 minuti di eventi di modifica dell'istanza per tutte le istanze che sono membri di qualsiasi classe derivata dalla classe [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 600
WHERE TargetInstance ISA "Win32_LogicalDisk"
```



Per altre informazioni sull'uso di ISA con una query di eventi, vedere [creazione di un evento timer con Win32 \_ LocalTime o Win32 \_ UTCTime](./creating-a-timer-event-with-win32-localtime-or-win32-utctime.md).

 

 
