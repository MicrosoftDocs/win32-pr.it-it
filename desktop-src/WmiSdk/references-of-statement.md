---
description: I riferimenti dell'istruzione recuperano tutte le istanze di associazione che fanno riferimento a una particolare istanza di origine.
ms.assetid: 674be546-e7fd-4150-9d7c-2888d24bf1b3
ms.tgt_platform: multiple
title: RIFERIMENTI dell'istruzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1c7cc624a1e91220fc6bfc89ef0a75878a9cfb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309918"
---
# <a name="references-of-statement"></a>RIFERIMENTI dell'istruzione

I riferimenti dell'istruzione recuperano tutte le istanze di associazione che fanno riferimento a una particolare istanza di origine. La sintassi dei riferimenti all'istruzione è simile a quella dell'oggetto ASSOCIATOrs OF Statement. Tuttavia, anziché recuperare le istanze dell'endpoint, vengono recuperate le istanze di associazione coinvolte.

I riferimenti della clausola WHERE possono includere una o più delle seguenti parole chiave predefinite e i relativi valori:


```sql
REFERENCES OF {SourceObject} WHERE 
    ClassDefsOnly
    RequiredQualifier = QualifierName
    ResultClass = ClassName
    Role = PropertyName
```



Per specificare un oggetto di origine, usare qualsiasi percorso di oggetto valido per SourceObject. Come per l'istruzione SELECT, la clausola WHERE è facoltativa e viene utilizzata per definire ulteriormente la query. In altre parole, l'istruzione seguente è perfettamente valida:


```sql
REFERENCES OF {Adapter="AHA-294X"}
```



La parola chiave **ClassDefsOnly** indica che l'istruzione restituisce un set di risultati di oggetti definizione di classe anziché le istanze effettive delle classi di associazione. Questi oggetti contengono le definizioni delle classi a cui appartengono le istanze che fanno riferimento all'oggetto di origine. Ad esempio, l'istruzione seguente restituisce le definizioni per le classi **AdapterDriver** e **AdapterProtocol** :


```sql
REFERENCES OF {Adapter="AHA-294X"} WHERE ClassDefsOnly
```



La parola chiave **RequiredQualifier** indica che gli oggetti Association restituiti devono includere il qualificatore specificato. La parola chiave **RequiredQualifier** può essere utilizzata per includere specifiche istanze di associazioni nel set di risultati. Ad esempio, l'istruzione seguente restituisce le istanze di associazione che includono un qualificatore denominato **AdapterTag**:


```sql
REFERENCES OF {Adapter="AHA-294X"}  WHERE RequiredQualifier = AdapterTag
```



La parola chiave **ResultClass** indica che gli oggetti Association restituiti devono appartenere o essere derivati dalla classe specificata. Ad esempio, l'istruzione seguente restituisce le associazioni della classe **AdapterDriver** o delle sottoclassi di **AdapterDriver**:


```sql
REFERENCES OF {Adapter="AHA-294X"} WHERE ResultClass = AdapterDriver
```



Le parole chiave **ClassDefsOnly** e **ResultClass** si escludono a vicenda. Il loro utilizzo combinato causa un errore di query non valido.

La parola chiave **Role** indica che le associazioni restituite sono solo quelle in cui l'oggetto di origine svolge un particolare ruolo. Il ruolo viene definito dalla proprietà specificata, una proprietà Reference di tipo [ref](references.md). La parola chiave **Role** è utile nelle associazioni in cui un determinato oggetto può riprodurre un ruolo in alcuni casi e un altro ruolo in altri, ad esempio in associazioni gerarchiche. È possibile utilizzare la parola chiave **Role** per recuperare tutte le associazioni in cui l'oggetto di origine svolge il ruolo di padre, ad esempio. Nell'istruzione seguente viene illustrata la sintassi per recuperare le associazioni con una proprietà **padre** che fa riferimento all'oggetto di origine come elemento padre:


```sql
REFERENCES OF {Adapter="AHA-294X"} WHERE Role = parent
```



> [!Note]  
> Le query complesse non possono usare "and" o "or" per separare le parole chiave per gli ASSOCIATOri di e i riferimenti delle istruzioni. Inoltre, il segno di uguale è l'unico operatore valido che può essere utilizzato con le parole chiave in queste query. Viene ad esempio considerata valida la query seguente:

 


```sql
"REFERENCES OF {Win32_NetworkAdapter.DeviceID="0"} " +
    "WHERE resultclass = Win32_NetworkAdapterSetting " +
    "requiredQualifier = Dynamic"
```



> [!Note]  
> Gli esempi successivi non sono validi. Il primo esempio non usa il segno di uguale e il secondo esempio tenta erroneamente di usare la parola chiave **and** :

 


```sql
"REFERENCES OF {Win32_NetworkAdapter.DeviceID="0"} " +
    "WHERE resultclass = Win32_NetworkAdapterSetting " +
    "requiredQualifier <> Dynamic"

"REFERENCES OF {Win32_NetworkAdapter.DeviceID="0"} " +
"WHERE resultclass = Win32_NetworkAdapterSetting " +
"AND requiredQualifier = Dynamic"
```



 

 



