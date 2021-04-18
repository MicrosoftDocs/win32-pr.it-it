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
# <a name="where-clause-wmi"></a><span data-ttu-id="9501b-103">Clausola WHERE (WMI)</span><span class="sxs-lookup"><span data-stu-id="9501b-103">WHERE Clause (WMI)</span></span>

<span data-ttu-id="9501b-104">Utilizzare la clausola WHERE per limitare l'ambito di una query di dati, eventi o schemi.</span><span class="sxs-lookup"><span data-stu-id="9501b-104">Use the WHERE clause to narrow the scope of a data, event, or schema query.</span></span> <span data-ttu-id="9501b-105">Per ulteriori informazioni, vedere [esecuzione di query con WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="9501b-105">For more information, see [Querying with WQL](querying-with-wql.md).</span></span> <span data-ttu-id="9501b-106">La clausola WHERE è costituita da una proprietà o una parola chiave, da un operatore e da una costante.</span><span class="sxs-lookup"><span data-stu-id="9501b-106">The WHERE clause is made up of a property or keyword, an operator, and a constant.</span></span> <span data-ttu-id="9501b-107">Tutte le clausole WHERE devono specificare uno degli operatori predefiniti inclusi nel linguaggio WQL (Strumentazione gestione Windows WMI).</span><span class="sxs-lookup"><span data-stu-id="9501b-107">All WHERE clauses must specify one of the predefined operators that are included in the Windows Management Instrumentation (WMI) Query Language (WQL).</span></span> <span data-ttu-id="9501b-108">È possibile aggiungere la clausola WHERE all'istruzione SELECT utilizzando uno dei formati seguenti:</span><span class="sxs-lookup"><span data-stu-id="9501b-108">You can append the WHERE clause to the SELECT statement using one of the following forms:</span></span>


```sql
SELECT * FROM class WHERE property operator constant
SELECT * FROM class WHERE constant operator property
```



<span data-ttu-id="9501b-109">dove \* è l'elemento su cui viene eseguita la query, la classe è la classe in cui eseguire una query, mentre Constant, operator e Property sono la costante, l'operatore e la proprietà o la parola chiave da usare.</span><span class="sxs-lookup"><span data-stu-id="9501b-109">where \* is the item queried about, class is the class in which to query, and constant, operator, and property are the constant, operator, and property or keyword to use.</span></span> <span data-ttu-id="9501b-110">Per ulteriori informazioni sull'istruzione SELECT, vedere istruzione [Select per](select-statement-for-data-queries.md)le query di dati, [istruzione SELECT per le query di eventi](select-statement-for-event-queries.md)o [istruzione SELECT per le query dello schema](select-statement-for-schema-queries.md).</span><span class="sxs-lookup"><span data-stu-id="9501b-110">For more information about the SELECT statement, see [SELECT Statement for Data Queries](select-statement-for-data-queries.md), [SELECT Statement for Event Queries](select-statement-for-event-queries.md), or [SELECT Statement for Schema Queries](select-statement-for-schema-queries.md).</span></span>

<span data-ttu-id="9501b-111">Il valore della costante deve essere del tipo corretto per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="9501b-111">The value of the constant must be of the correct type for the property.</span></span> <span data-ttu-id="9501b-112">Inoltre, l'operatore deve essere incluso nell'elenco degli [operatori WQL](wql-operators.md)validi.</span><span class="sxs-lookup"><span data-stu-id="9501b-112">Moreover, the operator must be among the list of valid [WQL operators](wql-operators.md).</span></span> <span data-ttu-id="9501b-113">È necessario che un nome di proprietà o una costante sia presente su entrambi i lati dell'operatore nella clausola WHERE.</span><span class="sxs-lookup"><span data-stu-id="9501b-113">Either a property name or a constant must appear on either side of the operator in the WHERE clause.</span></span>

<span data-ttu-id="9501b-114">È possibile utilizzare valori letterali stringa, ad esempio "NTFS", in una clausola WHERE.</span><span class="sxs-lookup"><span data-stu-id="9501b-114">You may use string literals, such as "NTFS", in a WHERE clause.</span></span> <span data-ttu-id="9501b-115">Se si desidera includere i caratteri speciali seguenti nella stringa, è necessario innanzitutto eseguire l'escape del carattere anteponendo il carattere con una barra rovesciata ( \) :</span><span class="sxs-lookup"><span data-stu-id="9501b-115">If you wish to include the following special characters in your string, you must first escape the character by prefixing the character with a backslash (\):</span></span>

-   <span data-ttu-id="9501b-116">barra rovesciata\\\)</span><span class="sxs-lookup"><span data-stu-id="9501b-116">backslash (\\\)</span></span>
-   <span data-ttu-id="9501b-117">virgolette doppie ( \\ ")</span><span class="sxs-lookup"><span data-stu-id="9501b-117">double quotes (\\")</span></span>
-   <span data-ttu-id="9501b-118">virgolette singole ( \\ ')</span><span class="sxs-lookup"><span data-stu-id="9501b-118">single quotes (\\')</span></span>

<span data-ttu-id="9501b-119">Impossibile utilizzare espressioni aritmetiche arbitrarie.</span><span class="sxs-lookup"><span data-stu-id="9501b-119">Arbitrary arithmetic expressions cannot be used.</span></span> <span data-ttu-id="9501b-120">Ad esempio, la query seguente restituisce solo le istanze della classe [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) che rappresentano le unità NTFS:</span><span class="sxs-lookup"><span data-stu-id="9501b-120">For example, the following query returns only the instances of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class that represent NTFS drives:</span></span>


```sql
SELECT * FROM Win32_LogicalDisk WHERE FileSystem = "NTFS"
```



<span data-ttu-id="9501b-121">I nomi di proprietà non possono essere visualizzati su entrambi i lati dell'operatore.</span><span class="sxs-lookup"><span data-stu-id="9501b-121">Property names cannot appear on both sides of the operator.</span></span> <span data-ttu-id="9501b-122">La query seguente è un esempio di query non valida:</span><span class="sxs-lookup"><span data-stu-id="9501b-122">The following query is an example of an invalid query:</span></span>


```sql
SELECT * FROM PhysicalDisk WHERE Partitions < (4 + 7 - 2) 
    OR   (Partitions = SectorsPerTrack / 7)
```



<span data-ttu-id="9501b-123">Per la maggior parte degli utilizzi dei descrittori di classe in una clausola WHERE, WMI contrassegna la query come non valida e restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="9501b-123">For most uses of class descriptors in a WHERE clause, WMI flags the query as invalid and returns an error.</span></span> <span data-ttu-id="9501b-124">Tuttavia, usare l'operatore punto (.) per le proprietà di tipo **Object** in WMI.</span><span class="sxs-lookup"><span data-stu-id="9501b-124">However, use the dot (.) operator for properties of type **object** in WMI.</span></span> <span data-ttu-id="9501b-125">Ad esempio, la query seguente è valida se prop è una proprietà valida di MyClass ed è Type **Object**:</span><span class="sxs-lookup"><span data-stu-id="9501b-125">For example, the following query is valid if Prop is a valid property of MyClass and is type **object**:</span></span>

``` syntax
SELECT * FROM MyClass WHERE Prop.embedprop = 5
```

<span data-ttu-id="9501b-126">I test di confronto non fanno mai distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="9501b-126">Comparison tests are always case-insensitive.</span></span> <span data-ttu-id="9501b-127">Ovvero le tre istruzioni seguenti restituiscono tutte **true**:</span><span class="sxs-lookup"><span data-stu-id="9501b-127">That is, the following three statements all evaluate to **TRUE**:</span></span>


```sql
SELECT * FROM MyClass WHERE Prop1 = "cat"
SELECT * FROM MyClass WHERE Prop1 = "CAT"
SELECT * FROM MyClass WHERE Prop1 = "cAt"
```



<span data-ttu-id="9501b-128">È possibile creare una query che includa tipi di dati booleani, ma gli unici tipi di operando booleani validi sono i tipi =,! = e <> .</span><span class="sxs-lookup"><span data-stu-id="9501b-128">You can construct a query that includes Boolean data types, but the only valid Boolean operand types are the =, != and <> types.</span></span> <span data-ttu-id="9501b-129">Il valore **true** equivale al numero 1 e il valore **false** è equivalente al numero 0.</span><span class="sxs-lookup"><span data-stu-id="9501b-129">The value **TRUE** is equivalent to the number 1, and the value **FALSE** is equivalent to the number 0.</span></span> <span data-ttu-id="9501b-130">Gli esempi seguenti sono di query che confrontano un valore booleano con i valori **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="9501b-130">The following examples are of queries that compare a Boolean value against the values **TRUE** or **FALSE**.</span></span>


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



<span data-ttu-id="9501b-131">Gli esempi seguenti sono di query non valide che tentano di usare operandi non validi.</span><span class="sxs-lookup"><span data-stu-id="9501b-131">The following examples are of invalid queries that attempt to use invalid operands.</span></span>


```sql
SELECT * FROM MyClass WHERE BoolProp <= TRUE
SELECT * FROM MyClass WHERE BoolProp >= 0
SELECT * FROM MyClass WHERE BoolProp > FALSE
SELECT * FROM win32_computersystem WHERE infraredsupported >= null
```



<span data-ttu-id="9501b-132">È possibile combinare più gruppi di proprietà, operatori e costanti in una clausola WHERE usando operatori logici e sottoespressioni parentesi.</span><span class="sxs-lookup"><span data-stu-id="9501b-132">Multiple groups of properties, operators, and constants can be combined in a WHERE clause using logical operators and parenthetical subexpressions.</span></span> <span data-ttu-id="9501b-133">Ogni gruppo deve essere unito agli [operatori](wql-operators.md) and, or o not, come illustrato nelle query seguenti.</span><span class="sxs-lookup"><span data-stu-id="9501b-133">Each group must be joined with the AND, OR, or NOT [operators](wql-operators.md) as is shown in the following queries.</span></span> <span data-ttu-id="9501b-134">La prima query recupera tutte le istanze della classe [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) con la proprietà **Name** impostata su C o D:</span><span class="sxs-lookup"><span data-stu-id="9501b-134">The first query retrieves all instances of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class with the **Name** property set to either C or D:</span></span>


```sql
SELECT * FROM Win32_LogicalDisk WHERE Name = "C:" OR Name = "D:"
```



<span data-ttu-id="9501b-135">La seconda query recupera i dischi denominati "C:" o "D:" solo se hanno una certa quantità di spazio libero rimanente e hanno file system NTFS:</span><span class="sxs-lookup"><span data-stu-id="9501b-135">The second query retrieves disks named "C:" or "D:" only if they have a certain amount of free space remaining and have NTFS file systems:</span></span>


```sql
SELECT * FROM Win32_LogicalDisk WHERE (Name = "C:" OR Name = "D:") 
    AND  FreeSpace > 2000000  AND   FileSystem = "NTFS"
```



<span data-ttu-id="9501b-136">In questo esempio viene illustrata una query di schema che utilizza la clausola WHERE.</span><span class="sxs-lookup"><span data-stu-id="9501b-136">This example shows a schema query using the WHERE clause.</span></span>


```sql
SELECT * FROM meta_class WHERE __this ISA "myClassName"
```



<span data-ttu-id="9501b-137">La \_ metaclasse della classe identifica questo oggetto come query dello schema, la proprietà denominata che \_ \_ identifica la classe di destinazione della query e le definizioni delle richieste dell' [operatore ISA](isa-operator-for-schema-queries.md) per le sottoclassi della classe di destinazione.</span><span class="sxs-lookup"><span data-stu-id="9501b-137">The class meta\_class identifies this as a schema query, the property called \_\_this identifies the target class of the query and the [ISA operator](isa-operator-for-schema-queries.md) requests definitions for the subclasses of the target class.</span></span> <span data-ttu-id="9501b-138">La query precedente restituisce pertanto la definizione per la classe e le definizioni di classe e per tutte le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="9501b-138">Therefore, the preceding query returns the definition for the myClassName class and definitions for all of its subclasses.</span></span>

<span data-ttu-id="9501b-139">L'esempio seguente è una query di dati che usa gli [associatori dell'istruzione](associators-of-statement.md) con Where:</span><span class="sxs-lookup"><span data-stu-id="9501b-139">The following example is a data query using the [ASSOCIATORS OF statement](associators-of-statement.md) with WHERE:</span></span>


```sql
ASSOCIATORS OF {myClass.keyVal="Value1"} WHERE ClassDefsOnly
```



<span data-ttu-id="9501b-140">Nell'esempio seguente viene illustrata una query di schema che utilizza gli ASSOCIATOri di e in cui:</span><span class="sxs-lookup"><span data-stu-id="9501b-140">The next example shows a schema query using ASSOCIATORS OF and WHERE:</span></span>


```sql
ASSOCIATORS OF {myClass} WHERE SchemaOnly
```



<span data-ttu-id="9501b-141">L'esempio seguente è una query di dati che usa i [riferimenti dell'istruzione](references-of-statement.md) e dove:</span><span class="sxs-lookup"><span data-stu-id="9501b-141">The following example is a data query using the [REFERENCES OF statement](references-of-statement.md) and WHERE:</span></span>


```sql
REFERENCES OF {myClass.keyVal="Value1"} 
    WHERE RequiredQualifier = myQual
```



<span data-ttu-id="9501b-142">Questo ultimo esempio è una query di schema che usa i riferimenti di e dove:</span><span class="sxs-lookup"><span data-stu-id="9501b-142">This last example is a schema query using REFERENCES OF and WHERE:</span></span>


```sql
REFERENCES OF {myClass} WHERE SchemaOnly
```



<span data-ttu-id="9501b-143">Oltre al formato [DateTime](date-and-time-format.md) WMI, la clausola WHERE WQL supporta diversi formati di data e ora:</span><span class="sxs-lookup"><span data-stu-id="9501b-143">In addition to the WMI [DATETIME](date-and-time-format.md) format, the WQL WHERE clause supports several other date and time formats:</span></span>

-   [<span data-ttu-id="9501b-144">Formati di data supportati da WQL</span><span class="sxs-lookup"><span data-stu-id="9501b-144">WQL-Supported Date Formats</span></span>](wql-supported-date-formats.md)
-   [<span data-ttu-id="9501b-145">Formati di ora supportati da WQL</span><span class="sxs-lookup"><span data-stu-id="9501b-145">WQL-Supported Time Formats</span></span>](wql-supported-time-formats.md)

 

 
