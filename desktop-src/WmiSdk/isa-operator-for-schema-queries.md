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
# <a name="isa-operator-for-schema-queries"></a><span data-ttu-id="f5785-103">Operatore ISA per query dello schema</span><span class="sxs-lookup"><span data-stu-id="f5785-103">ISA Operator for Schema Queries</span></span>

<span data-ttu-id="f5785-104">L'operatore ISA è un operatore specifico di WQL che può essere utilizzato in query di dati, eventi e schemi.</span><span class="sxs-lookup"><span data-stu-id="f5785-104">The ISA operator is a WQL-specific operator that can be used in data, event, and schema queries.</span></span>

<span data-ttu-id="f5785-105">Quando ISA è incluso nella [clausola WHERE](where-clause.md) di una query di schema, richiede che la query venga applicata a tutte le sottoclassi della classe specificata.</span><span class="sxs-lookup"><span data-stu-id="f5785-105">When ISA is included in the [WHERE clause](where-clause.md) of an schema query, it requests that the query be applied to all subclasses of the class you specify.</span></span>

<span data-ttu-id="f5785-106">L'istruzione seguente, ad esempio, richiede la notifica ogni 10 minuti di eventi di modifica dell'istanza per tutte le istanze che sono membri di qualsiasi classe derivante dalla classe [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="f5785-106">For example, the following statement requests notification every 10 minutes of instance modification events for all instances that are members of any class deriving from the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span>


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 600
WHERE TargetInstance ISA "Win32_LogicalDisk"
```



<span data-ttu-id="f5785-107">La query seguente restituisce la definizione per la classe del [**\_ processore CIM**](/windows/desktop/CIMWin32Prov/cim-processor) e le definizioni per tutte le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="f5785-107">The following query returns the definition for the [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor) class and definitions for all of its subclasses.</span></span>


```sql
SELECT * FROM meta_class WHERE __this ISA "CIM_Processor"
```



<span data-ttu-id="f5785-108">La **\_ metaclasse** della classe identifica questo come una query dello schema, la **\_ \_ proprietà denominata che** identifica la classe di destinazione della query e l'operatore ISA richiede le definizioni per le sottoclassi della classe di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f5785-108">The class **meta\_class** identifies this as a schema query, the property called **\_\_this** identifies the target class of the query, and the ISA operator requests definitions for the subclasses of the target class.</span></span>

 

 
