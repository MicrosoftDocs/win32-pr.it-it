---
description: Vengono descritti gli operatori WQL utilizzati nella clausola WHERE o nell'istruzione SELECT.
ms.assetid: a62de66d-d5ba-49a1-8262-bfa10ac2db75
ms.tgt_platform: multiple
title: Operatori WQL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f5cc37d03884a3609abf3f76d2c78ba22b3c9f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313156"
---
# <a name="wql-operators"></a>Operatori WQL

Il linguaggio WQL (Strumentazione gestione Windows Query Language) supporta un set di operatori standard utilizzati nella [clausola WHERE](where-clause.md) di un'istruzione SELECT, come indicato di seguito.



| Operatore       | Descrizione              |
|----------------|--------------------------|
| =              | Uguale a                 |
| <           | Minore di                |
| >           | Maggiore di             |
| <=          | Minore o uguale a    |
| >=          | Maggiore o uguale a |
| ! = o <> | Diverso da             |



 

Sono disponibili alcuni operatori aggiuntivi specifici di WQL: è, non è, ISA e LIKE. Gli operatori IS e IS NOT sono validi nella clausola WHERE solo se la costante è **null**. Ad esempio, le query seguenti sono valide:


```sql
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NULL
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NOT NULL
```



Le query seguenti mostrano usi non validi di IS e NOT:


```sql
SELECT * FROM Win32_LogicalDisk WHERE DriveType IS 5
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NOT "NTFS"
```



L'operatore ISA viene utilizzato nella clausola WHERE di query di dati e di eventi per testare oggetti incorporati per una gerarchia di classi. L'operatore ISA Elimina la necessità di tenere traccia delle nuove classi derivate quando si richiede una gerarchia di classi. Quando si utilizza ISA, le sottoclassi appena create e quelle esistenti della classe richiesta vengono incluse automaticamente nel set di risultati.

Per ulteriori informazioni sulla sintassi e sull'utilizzo di questo operatore, vedere gli argomenti seguenti:

-   [Operatore ISA per query di dati](isa-operator-for-data-queries.md)
-   [Operatore ISA per le query di eventi](isa-operator-for-event-queries.md)
-   [Operatore ISA per query dello schema](isa-operator-for-schema-queries.md)

L'operatore LIKE è valido nella clausola WHERE e viene usato per determinare se una determinata stringa di caratteri corrisponde a un modello specificato. Ad esempio, la query seguente restituisce tutte le istanze delle \_ classi Win32.


```sql
SELECT * FROM Meta_Class WHERE __Class LIKE "%Win32%"
```



Per ulteriori informazioni sulla sintassi e sull'utilizzo di questo operatore, vedere [operatore like](like-operator.md).

 

 



