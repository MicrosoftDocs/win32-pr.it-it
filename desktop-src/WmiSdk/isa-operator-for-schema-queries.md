---
description: L'operatore ISA è un operatore specifico di WQL che può essere utilizzato nelle query di dati, eventi e schemi.
ms.assetid: 0520470c-ebfc-4c45-8a1f-47fd66bf8414
ms.tgt_platform: multiple
title: Operatore ISA per query sullo schema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bde4c48e2b80d84d4af1a8d52556752e5b77f682ee273fa5ab6320fd71038a2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118819271"
---
# <a name="isa-operator-for-schema-queries"></a>Operatore ISA per query sullo schema

L'operatore ISA è un operatore specifico di WQL che può essere utilizzato nelle query di dati, eventi e schemi.

Quando ISA è incluso nella clausola [WHERE](where-clause.md) di una query di schema, richiede che la query sia applicata a tutte le sottoclassi della classe specificata.

Ad esempio, l'istruzione seguente richiede una notifica ogni 10 minuti di eventi di modifica dell'istanza per tutte le istanze che sono membri di qualsiasi classe che deriva dalla [**classe \_ LogicalDisk Win32.**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 600
WHERE TargetInstance ISA "Win32_LogicalDisk"
```



La query seguente restituisce la definizione per la classe [**del processore CIM \_**](/windows/desktop/CIMWin32Prov/cim-processor) e le definizioni per tutte le relative sottoclassi.


```sql
SELECT * FROM meta_class WHERE __this ISA "CIM_Processor"
```



La **metaclasse \_** della classe lo identifica come query dello schema, la proprietà denominata **\_ \_ this** identifica la classe di destinazione della query e l'operatore ISA richiede le definizioni per le sottoclassi della classe di destinazione.

 

 
