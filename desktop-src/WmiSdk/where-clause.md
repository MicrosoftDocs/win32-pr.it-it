---
description: Usare la clausola WHERE per restringere l'ambito di una query di dati, eventi o schema.
ms.assetid: b275f8e0-773d-422c-be21-b427e7a1fb6b
ms.tgt_platform: multiple
title: Clausola WHERE (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a6a51657dac26a002890bde8346cd7570f6057f2ace5cdfb5350d6c90d0fee8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312182"
---
# <a name="where-clause-wmi"></a>Clausola WHERE (WMI)

Usare la clausola WHERE per restringere l'ambito di una query di dati, eventi o schema. Per altre informazioni, vedere [Esecuzione di query con WQL.](querying-with-wql.md) La clausola WHERE è costituito da una proprietà o una parola chiave, un operatore e una costante. Tutte le clausole WHERE devono specificare uno degli operatori predefiniti inclusi in Windows Management Instrumentation (WMI) Query Language (WQL). È possibile aggiungere la clausola WHERE all'istruzione SELECT usando uno dei formati seguenti:


```sql
SELECT * FROM class WHERE property operator constant
SELECT * FROM class WHERE constant operator property
```



dove è l'elemento su cui viene eseguita la query, class è la classe in cui eseguire una query e constant, operator e property sono la costante, l'operatore e la proprietà o la parola chiave \* da usare. Per altre informazioni sull'istruzione SELECT, vedere Istruzione SELECT per query [di dati,](select-statement-for-data-queries.md) [istruzione SELECT](select-statement-for-event-queries.md)per query di eventi o istruzione SELECT per query [di schema.](select-statement-for-schema-queries.md)

Il valore della costante deve essere del tipo corretto per la proprietà . Inoltre, l'operatore deve essere in elenco di operatori [WQL validi.](wql-operators.md) Il nome di una proprietà o una costante deve essere presente su entrambi i lati dell'operatore nella clausola WHERE.

È possibile usare valori letterali stringa, ad esempio "NTFS", in una clausola WHERE. Se si desidera includere i caratteri speciali seguenti nella stringa, è prima necessario eseguire l'escape del carattere anteporvi una barra rovesciata ( \\ ):

-   barra rovesciata ( \\ \\ )
-   virgolette doppie ( \\ ")
-   virgolette singole ( \\ ')

Non è possibile usare espressioni aritmetiche arbitrarie. Ad esempio, la query seguente restituisce solo le istanze della [**classe \_ LogicalDisk Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) che rappresentano le unità NTFS:


```sql
SELECT * FROM Win32_LogicalDisk WHERE FileSystem = "NTFS"
```



I nomi delle proprietà non possono essere visualizzati su entrambi i lati dell'operatore. La query seguente è un esempio di query non valida:


```sql
SELECT * FROM PhysicalDisk WHERE Partitions < (4 + 7 - 2) 
    OR   (Partitions = SectorsPerTrack / 7)
```



Per la maggior parte degli usi dei descrittori di classe in una clausola WHERE, WMI contrassegna la query come non valida e restituisce un errore. Tuttavia, usare l'operatore punto (.) per le proprietà di tipo **object** in WMI. Ad esempio, la query seguente è valida se Prop è una proprietà valida di MyClass e è di tipo **object**:

``` syntax
SELECT * FROM MyClass WHERE Prop.embedprop = 5
```

Per i test di confronto non viene sempre fatto distinzione tra maiuscole e minuscole. In altre informazioni, tutte e tre le istruzioni seguenti restituiscono **TRUE:**


```sql
SELECT * FROM MyClass WHERE Prop1 = "cat"
SELECT * FROM MyClass WHERE Prop1 = "CAT"
SELECT * FROM MyClass WHERE Prop1 = "cAt"
```



È possibile costruire una query che include tipi di dati booleani, ma gli unici tipi di operandi booleani validi sono i tipi =, != e <> booleani. Il valore **TRUE** equivale al numero 1 e il valore **FALSE** è equivalente al numero 0. Gli esempi seguenti sono query che confrontano un valore booleano con i valori **TRUE** o **FALSE.**


```sql
SELECT * FROM MyClass WHERE BoolProp = 1
SELECT * FROM MyClass WHERE BoolProp = TRUE
SELECT * FROM MyClass WHERE BoolProp <> FALSE
SELECT * FROM MyClass WHERE BoolProp = 0
SELECT * FROM MyClass WHERE BoolProp = FALSE
SELECT * FROM MyClass WHERE BoolProp != 1
SELECT * FROM MyClass WHERE BoolProp != FALSE
SELECT * FROM MyClass WHERE BoolProp <> FALSE
```



Gli esempi seguenti sono relativi a query non valide che tentano di usare operandi non validi.


```sql
SELECT * FROM MyClass WHERE BoolProp <= TRUE
SELECT * FROM MyClass WHERE BoolProp >= 0
SELECT * FROM MyClass WHERE BoolProp > FALSE
SELECT * FROM win32_computersystem WHERE infraredsupported >= null
```



È possibile combinare più gruppi di proprietà, operatori e costanti in una clausola WHERE usando operatori logici e sottoespressioni tra parentesi. Ogni gruppo deve essere unito con gli operatori AND, OR o [NOT,](wql-operators.md) come illustrato nelle query seguenti. La prima query recupera tutte le istanze della [**classe \_ LogicalDisk Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) con la **proprietà Name** impostata su C o D:


```sql
SELECT * FROM Win32_LogicalDisk WHERE Name = "C:" OR Name = "D:"
```



La seconda query recupera i dischi denominati "C:" o "D:" solo se hanno una certa quantità di spazio libero rimanente e hanno file system NTFS:


```sql
SELECT * FROM Win32_LogicalDisk WHERE (Name = "C:" OR Name = "D:") 
    AND  FreeSpace > 2000000  AND   FileSystem = "NTFS"
```



In questo esempio viene illustrata una query di schema che usa la clausola WHERE.


```sql
SELECT * FROM meta_class WHERE __this ISA "myClassName"
```



La metaclasse della classe lo identifica come query dello schema, la proprietà denominata this identifica la classe di destinazione della query e \_ \_ \_ [l'operatore ISA](isa-operator-for-schema-queries.md) richiede le definizioni per le sottoclassi della classe di destinazione. Pertanto, la query precedente restituisce la definizione per la classe myClassName e le definizioni per tutte le relative sottoclassi.

L'esempio seguente è una query di dati che usa [l'istruzione ASSOCIATORS OF](associators-of-statement.md) con WHERE:


```sql
ASSOCIATORS OF {myClass.keyVal="Value1"} WHERE ClassDefsOnly
```



Nell'esempio seguente viene illustrata una query di schema che usa ASSOCIATORS OF e WHERE:


```sql
ASSOCIATORS OF {myClass} WHERE SchemaOnly
```



L'esempio seguente è una query di dati che usa [l'istruzione REFERENCES OF](references-of-statement.md) e WHERE:


```sql
REFERENCES OF {myClass.keyVal="Value1"} 
    WHERE RequiredQualifier = myQual
```



L'ultimo esempio è una query di schema che usa REFERENCES OF e WHERE:


```sql
REFERENCES OF {myClass} WHERE SchemaOnly
```



Oltre al formato [WMI DATETIME,](date-and-time-format.md) la clausola WHERE WQL supporta diversi altri formati di data e ora:

-   [Formati di data supportati da WQL](wql-supported-date-formats.md)
-   [Formati di ora supportati da WQL](wql-supported-time-formats.md)

 

 
