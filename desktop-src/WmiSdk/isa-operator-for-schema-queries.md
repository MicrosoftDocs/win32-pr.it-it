---
description: L'operatore ISA è un operatore specifico di WQL che può essere utilizzato in query di dati, eventi e schemi.
ms.assetid: 0520470c-ebfc-4c45-8a1f-47fd66bf8414
ms.tgt_platform: multiple
title: Operatore ISA per query dello schema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fb50146e4bd1219712c84bc1acec7fc7d50146b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315206"
---
# <a name="isa-operator-for-schema-queries"></a>Operatore ISA per query dello schema

L'operatore ISA è un operatore specifico di WQL che può essere utilizzato in query di dati, eventi e schemi.

Quando ISA è incluso nella [clausola WHERE](where-clause.md) di una query di schema, richiede che la query venga applicata a tutte le sottoclassi della classe specificata.

L'istruzione seguente, ad esempio, richiede la notifica ogni 10 minuti di eventi di modifica dell'istanza per tutte le istanze che sono membri di qualsiasi classe derivante dalla classe [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 600
WHERE TargetInstance ISA "Win32_LogicalDisk"
```



La query seguente restituisce la definizione per la classe del [**\_ processore CIM**](/windows/desktop/CIMWin32Prov/cim-processor) e le definizioni per tutte le relative sottoclassi.


```sql
SELECT * FROM meta_class WHERE __this ISA "CIM_Processor"
```



La **\_ metaclasse** della classe identifica questo come una query dello schema, la **\_ \_ proprietà denominata che** identifica la classe di destinazione della query e l'operatore ISA richiede le definizioni per le sottoclassi della classe di destinazione.

 

 
