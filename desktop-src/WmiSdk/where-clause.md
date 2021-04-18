---
description: Utilizzare la clausola WHERE per limitare l'ambito di una query di dati, eventi o schemi.
ms.assetid: b275f8e0-773d-422c-be21-b427e7a1fb6b
ms.tgt_platform: multiple
title: Clausola WHERE (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a72e68d8266b72f6e41e17c0b85766b7a58bb197
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318839"
---
# <a name="where-clause-wmi"></a>Clausola WHERE (WMI)

Utilizzare la clausola WHERE per limitare l'ambito di una query di dati, eventi o schemi. Per ulteriori informazioni, vedere [esecuzione di query con WQL](querying-with-wql.md). La clausola WHERE è costituita da una proprietà o una parola chiave, da un operatore e da una costante. Tutte le clausole WHERE devono specificare uno degli operatori predefiniti inclusi nel linguaggio WQL (Strumentazione gestione Windows WMI). È possibile aggiungere la clausola WHERE all'istruzione SELECT utilizzando uno dei formati seguenti:


```sql
SELECT * FROM class WHERE property operator constant
SELECT * FROM class WHERE constant operator property
```



dove \* è l'elemento su cui viene eseguita la query, la classe è la classe in cui eseguire una query, mentre Constant, operator e Property sono la costante, l'operatore e la proprietà o la parola chiave da usare. Per ulteriori informazioni sull'istruzione SELECT, vedere istruzione [Select per](select-statement-for-data-queries.md)le query di dati, [istruzione SELECT per le query di eventi](select-statement-for-event-queries.md)o [istruzione SELECT per le query dello schema](select-statement-for-schema-queries.md).

Il valore della costante deve essere del tipo corretto per la proprietà. Inoltre, l'operatore deve essere incluso nell'elenco degli [operatori WQL](wql-operators.md)validi. È necessario che un nome di proprietà o una costante sia presente su entrambi i lati dell'operatore nella clausola WHERE.

È possibile utilizzare valori letterali stringa, ad esempio "NTFS", in una clausola WHERE. Se si desidera includere i caratteri speciali seguenti nella stringa, è necessario innanzitutto eseguire l'escape del carattere anteponendo il carattere con una barra rovesciata ( \) :

-   barra rovesciata\\\)
-   virgolette doppie ( \\ ")
-   virgolette singole ( \\ ')

Impossibile utilizzare espressioni aritmetiche arbitrarie. Ad esempio, la query seguente restituisce solo le istanze della classe [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) che rappresentano le unità NTFS:


```sql
SELECT * FROM Win32_LogicalDisk WHERE FileSystem = "NTFS"
```



I nomi di proprietà non possono essere visualizzati su entrambi i lati dell'operatore. La query seguente è un esempio di query non valida:


```sql
SELECT * FROM PhysicalDisk WHERE Partitions < (4 + 7 - 2) 
    OR   (Partitions = SectorsPerTrack / 7)
```



Per la maggior parte degli utilizzi dei descrittori di classe in una clausola WHERE, WMI contrassegna la query come non valida e restituisce un errore. Tuttavia, usare l'operatore punto (.) per le proprietà di tipo **Object** in WMI. Ad esempio, la query seguente è valida se prop è una proprietà valida di MyClass ed è Type **Object**:

``` syntax
SELECT * FROM MyClass WHERE Prop.embedprop = 5
```

I test di confronto non fanno mai distinzione tra maiuscole e minuscole. Ovvero le tre istruzioni seguenti restituiscono tutte **true**:


```sql
SELECT * FROM MyClass WHERE Prop1 = "cat"
SELECT * FROM MyClass WHERE Prop1 = "CAT"
SELECT * FROM MyClass WHERE Prop1 = "cAt"
```



È possibile creare una query che includa tipi di dati booleani, ma gli unici tipi di operando booleani validi sono i tipi =,! = e <> . Il valore **true** equivale al numero 1 e il valore **false** è equivalente al numero 0. Gli esempi seguenti sono di query che confrontano un valore booleano con i valori **true** o **false**.


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



Gli esempi seguenti sono di query non valide che tentano di usare operandi non validi.


```sql
SELECT * FROM MyClass WHERE BoolProp <= TRUE
SELECT * FROM MyClass WHERE BoolProp >= 0
SELECT * FROM MyClass WHERE BoolProp > FALSE
SELECT * FROM win32_computersystem WHERE infraredsupported >= null
```



È possibile combinare più gruppi di proprietà, operatori e costanti in una clausola WHERE usando operatori logici e sottoespressioni parentesi. Ogni gruppo deve essere unito agli [operatori](wql-operators.md) and, or o not, come illustrato nelle query seguenti. La prima query recupera tutte le istanze della classe [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) con la proprietà **Name** impostata su C o D:


```sql
SELECT * FROM Win32_LogicalDisk WHERE Name = "C:" OR Name = "D:"
```



La seconda query recupera i dischi denominati "C:" o "D:" solo se hanno una certa quantità di spazio libero rimanente e hanno file system NTFS:


```sql
SELECT * FROM Win32_LogicalDisk WHERE (Name = "C:" OR Name = "D:") 
    AND  FreeSpace > 2000000  AND   FileSystem = "NTFS"
```



In questo esempio viene illustrata una query di schema che utilizza la clausola WHERE.


```sql
SELECT * FROM meta_class WHERE __this ISA "myClassName"
```



La \_ metaclasse della classe identifica questo oggetto come query dello schema, la proprietà denominata che \_ \_ identifica la classe di destinazione della query e le definizioni delle richieste dell' [operatore ISA](isa-operator-for-schema-queries.md) per le sottoclassi della classe di destinazione. La query precedente restituisce pertanto la definizione per la classe e le definizioni di classe e per tutte le relative sottoclassi.

L'esempio seguente è una query di dati che usa gli [associatori dell'istruzione](associators-of-statement.md) con Where:


```sql
ASSOCIATORS OF {myClass.keyVal="Value1"} WHERE ClassDefsOnly
```



Nell'esempio seguente viene illustrata una query di schema che utilizza gli ASSOCIATOri di e in cui:


```sql
ASSOCIATORS OF {myClass} WHERE SchemaOnly
```



L'esempio seguente è una query di dati che usa i [riferimenti dell'istruzione](references-of-statement.md) e dove:


```sql
REFERENCES OF {myClass.keyVal="Value1"} 
    WHERE RequiredQualifier = myQual
```



Questo ultimo esempio è una query di schema che usa i riferimenti di e dove:


```sql
REFERENCES OF {myClass} WHERE SchemaOnly
```



Oltre al formato [DateTime](date-and-time-format.md) WMI, la clausola WHERE WQL supporta diversi formati di data e ora:

-   [Formati di data supportati da WQL](wql-supported-date-formats.md)
-   [Formati di ora supportati da WQL](wql-supported-time-formats.md)

 

 
