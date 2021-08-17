---
description: Descrive gli operatori WQL usati nella clausola WHERE o nell'istruzione SELECT.
ms.assetid: a62de66d-d5ba-49a1-8262-bfa10ac2db75
ms.tgt_platform: multiple
title: Operatori WQL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a441afb661e4f8d92e21d944462dddd6d7390fd2dbe871512342f7c9251d6ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118553088"
---
# <a name="wql-operators"></a>Operatori WQL

Il Windows Management Instrumentation Query Language (WQL) supporta un set di operatori standard usati nella clausola [WHERE](where-clause.md) di un'istruzione SELECT, come indicato di seguito.



| Operatore       | Descrizione              |
|----------------|--------------------------|
| =              | Uguale a                 |
| <           | Minore di                |
| >           | Maggiore di             |
| <=          | Minore o uguale a    |
| >=          | Maggiore o uguale a |
| != o <> | Diverso da             |



 

Esistono alcuni operatori aggiuntivi specifici di WQL: IS, IS NOT, ISA e LIKE. Gli operatori IS e IS NOT sono validi nella clausola WHERE solo se la costante è **NULL.** Ad esempio, le query seguenti sono valide:


```sql
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NULL
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NOT NULL
```



Le query seguenti mostrano gli usi non validi di IS e IS NOT:


```sql
SELECT * FROM Win32_LogicalDisk WHERE DriveType IS 5
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NOT "NTFS"
```



L'operatore ISA viene usato nella clausola WHERE delle query di dati ed eventi per testare gli oggetti incorporati per una gerarchia di classi. L'operatore ISA elimina la necessità di tenere traccia delle nuove classi derivate quando si richiede una gerarchia di classi. Quando si usa ISA, le sottoclassi appena create ed esistenti della classe richiesta vengono incluse automaticamente nel set di risultati.

Per altre informazioni sulla sintassi e sull'uso di questo operatore, vedere gli argomenti seguenti:

-   [Operatore ISA per query di dati](isa-operator-for-data-queries.md)
-   [Operatore ISA per query di eventi](isa-operator-for-event-queries.md)
-   [Operatore ISA per query di schema](isa-operator-for-schema-queries.md)

L'operatore LIKE è valido nella clausola WHERE e viene usato per determinare se una determinata stringa di caratteri corrisponde a un criterio specificato. Ad esempio, la query seguente restituisce tutte le istanze delle classi \_ Win32.


```sql
SELECT * FROM Meta_Class WHERE __Class LIKE "%Win32%"
```



Per altre informazioni sulla sintassi e sull'uso di questo operatore, vedere [Operatore LIKE](like-operator.md).

 

 



