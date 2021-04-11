---
description: Le query di associazione dello schema utilizzano le stesse istruzioni utilizzate nelle query di associazione dati, ovvero gli ASSOCIATOri di e i riferimenti di.
ms.assetid: b5fc2d86-702a-42cd-82e6-f15c905ba6aa
ms.tgt_platform: multiple
title: Associazioni schema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2f0c3b753bf4657c66a635319bab7dbe435a3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233459"
---
# <a name="schema-associations"></a>Associazioni schema

Le query di associazione dello schema utilizzano le stesse istruzioni utilizzate nelle query di associazione dati, ovvero gli ASSOCIATOri di e i riferimenti di. Tuttavia, con le query di associazione dati, vengono restituite le istanze della classe e con le query di associazione dello schema, vengono restituiti i nomi delle classi che possono partecipare alle relazioni di associazione. Utilizzare, ad esempio, una query di schema per individuare tutte le classi di associazione definite nello schema che fanno riferimento a una classe di origine.

La sintassi per gli ASSOCIATOri di e i riferimenti di istruzioni è la stessa per le query di associazione dello schema, così come per le query di associazione dati, con le eccezioni seguenti:

-   L'oggetto di origine è una classe anziché un'istanza di.
-   Esiste una parola chiave aggiuntiva, **SchemaOnly**, che identifica la query come applicabile a uno schema anziché ai dati.
-   La parola chiave **ClassDefsOnly** non è valida.

Nell'esempio seguente viene illustrata la sintassi completa degli ASSOCIATOri di statement per una query di schema. Per informazioni dettagliate sulla sintassi, vedere [associrs of Statement](associators-of-statement.md).


```sql
ASSOCIATORS OF {SourceClass} WHERE 
    AssocClass = AssocClassName
    RequiredAssocQualifier = QualifierName
    RequiredQualifier = QualifierName
    ResultClass = ClassName
    ResultRole = PropertyName
    Role = PropertyName
    SchemaOnly
```



Nell'esempio seguente viene illustrata una query che restituisce le classi del **protocollo** e del **driver** , le due classi che fanno riferimento alla classe di origine.


```sql
ASSOCIATORS OF {Adapter} WHERE SchemaOnly
```



La query seguente restituisce solo la classe **driver** a causa della restrizione inserita dalla parola chiave **AssocClass** .


```sql
ASSOCIATORS OF {Adapter} WHERE AssocClass = AdapterDriver SchemaOnly
```



Di seguito è riportata la sintassi completa dei riferimenti dell'istruzione per una query di schema. Per la sintassi dettagliata, vedere [References of Statement](references-of-statement.md).


```sql
REFERENCES OF {SourceClass} WHERE
    ResultClass = ClassName
    Role = PropertyName
    RequiredQualifier = QualifierName
    SchemaOnly
```



> [!Note]  
> Le query di associazione dello schema possono restituire oggetti duplicati.

 

Ad esempio, la query seguente restituirà la classe [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) più volte durante l'enumerazione delle classi nello spazio dei nomi **\\ CIMV2 radice** .


```sql
ASSOCIATORS OF {Win32_ComputerSystem} WHERE SchemaOnly
```



 

 
