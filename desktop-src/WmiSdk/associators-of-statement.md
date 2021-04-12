---
description: Recupera tutte le istanze associate a una particolare istanza di origine.
ms.assetid: d6bd9643-523d-4d81-8bf1-da52ccc7524d
ms.tgt_platform: multiple
title: ASSOCIATOrs OF Statement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec595584efb5c32342e5bbdaa8bae309b21b29d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347636"
---
# <a name="associators-of-statement"></a><span data-ttu-id="81dd0-103">ASSOCIATOrs OF Statement</span><span class="sxs-lookup"><span data-stu-id="81dd0-103">ASSOCIATORS OF Statement</span></span>

<span data-ttu-id="81dd0-104">L'ASSOCIAZIONErs OF Statement recupera tutte le istanze associate a una particolare istanza di origine.</span><span class="sxs-lookup"><span data-stu-id="81dd0-104">The ASSOCIATORS OF statement retrieves all instances that are associated with a particular source instance.</span></span> <span data-ttu-id="81dd0-105">Le istanze recuperate vengono definite endpoint.</span><span class="sxs-lookup"><span data-stu-id="81dd0-105">The instances that are retrieved are referred to as the endpoints.</span></span> <span data-ttu-id="81dd0-106">Ogni endpoint viene restituito il numero di volte in cui sono presenti associazioni tra l'oggetto e l'oggetto di origine.</span><span class="sxs-lookup"><span data-stu-id="81dd0-106">Each endpoint is returned as many times as there are associations between it and the source object.</span></span> <span data-ttu-id="81dd0-107">Si supponga, ad esempio, che esistano istanze A, B, X e Y. Sono presenti due istanze di associazione, una che collega A e X e un'altra che collega B e Y. La query seguente restituisce il singolo endpoint X:</span><span class="sxs-lookup"><span data-stu-id="81dd0-107">For example, assume there are instances A, B, X, and Y. Two association instances exist, one that links A and X and another that links B and Y. The following query returns the single endpoint X:</span></span>


```sql
ASSOCIATORS OF {A}
```



<span data-ttu-id="81dd0-108">Tuttavia, se è presente un'altra associazione che collega A e X, la query precedente restituisce due endpoint X.</span><span class="sxs-lookup"><span data-stu-id="81dd0-108">However, if there is another association linking A and X, the above query returns two X endpoints.</span></span>

<span data-ttu-id="81dd0-109">La sintassi di base per gli ASSOCIATOri dell'istruzione è la seguente:</span><span class="sxs-lookup"><span data-stu-id="81dd0-109">The basic syntax for the ASSOCIATORS OF statement is:</span></span>

``` syntax
ASSOCIATORS OF {ObjectPath}
```

<span data-ttu-id="81dd0-110">Si noti che le parentesi graffe fanno parte della sintassi.</span><span class="sxs-lookup"><span data-stu-id="81dd0-110">Note that the braces are part of the syntax.</span></span> <span data-ttu-id="81dd0-111">Per ObjectPath è possibile usare qualsiasi percorso di oggetto valido.</span><span class="sxs-lookup"><span data-stu-id="81dd0-111">Any valid object path can be used for ObjectPath.</span></span> <span data-ttu-id="81dd0-112">I token all'interno del percorso dell'oggetto non possono contenere spazi vuoti.</span><span class="sxs-lookup"><span data-stu-id="81dd0-112">The tokens within the object path cannot contain any white space.</span></span> <span data-ttu-id="81dd0-113">Ad esempio, la query nell'elenco seguente restituisce le istanze associate al disco logico specificato:</span><span class="sxs-lookup"><span data-stu-id="81dd0-113">For example, the query in the following list returns instances that are associated with the specified logical disk:</span></span>

<dl> <dt>

<span data-ttu-id="81dd0-114"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query</span><span class="sxs-lookup"><span data-stu-id="81dd0-114"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"}
```



</dd> <dt>

<span data-ttu-id="81dd0-115"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Risultati</span><span class="sxs-lookup"><span data-stu-id="81dd0-115"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

``` syntax
Win32_ComputerSystem.Name="mycomputer"
Win32_DiskPartition.DeviceID="Disk #0, Partition #0"
```

</dd> </dl>

<span data-ttu-id="81dd0-116">Come con l' [istruzione SELECT](select-statement-for-data-queries.md), un ASSOCIATOre di un'istruzione può includere una [clausola WHERE](where-clause.md), ma la clausola WHERE per un Associator of Statement è molto diversa dalla clausola SELECT statementWHERE.</span><span class="sxs-lookup"><span data-stu-id="81dd0-116">As with the [SELECT statement](select-statement-for-data-queries.md), an ASSOCIATORS OF statement can include a [WHERE clause](where-clause.md), but the WHERE clause for an ASSOCIATORS OF statement is very different from the SELECT statementWHERE clause.</span></span>

<span data-ttu-id="81dd0-117">La [clausola WHERE](where-clause.md) dell'istruzione associaters of può includere una o più delle seguenti parole chiave predefinite e i relativi valori:</span><span class="sxs-lookup"><span data-stu-id="81dd0-117">The [WHERE clause](where-clause.md) of the ASSOCIATORS OF statement can include one or more of the following predefined keywords and their values:</span></span>


```sql
ASSOCIATORS OF {ObjectPath} WHERE
    AssocClass = AssocClassName
    ClassDefsOnly
    RequiredAssocQualifier = QualifierName
    RequiredQualifier = QualifierName
    ResultClass = ClassName
    ResultRole = PropertyName
    Role = PropertyName
```



<span data-ttu-id="81dd0-118">Si noti che le sottoclausole facoltative non sono separate da virgole.</span><span class="sxs-lookup"><span data-stu-id="81dd0-118">Note that the optional subclauses are not separated by commas.</span></span>

<span data-ttu-id="81dd0-119">La parola chiave **AssocClass** indica che gli endpoint restituiti devono essere associati all'origine tramite la classe specificata o una delle relative classi derivate.</span><span class="sxs-lookup"><span data-stu-id="81dd0-119">The **AssocClass** keyword indicates that the returned endpoints must be associated with the source through the specified class or one of its derived classes.</span></span> <span data-ttu-id="81dd0-120">Ad esempio, la query nell'elenco seguente restituisce solo gli endpoint associati all'origine tramite la classe di associazione [**Win32 \_ SystemDevices**](/windows/desktop/CIMWin32Prov/win32-systemdevices) o una delle relative classi derivate:</span><span class="sxs-lookup"><span data-stu-id="81dd0-120">For example, the query in the following list returns only endpoints that are associated with the source through the [**Win32\_SystemDevices**](/windows/desktop/CIMWin32Prov/win32-systemdevices) association class or any of its derived classes:</span></span>

<dl> <dt>

<span data-ttu-id="81dd0-121"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query</span><span class="sxs-lookup"><span data-stu-id="81dd0-121"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE AssocClass = Win32_SystemDevices
```



</dd> <dt>

<span data-ttu-id="81dd0-122"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Risultati</span><span class="sxs-lookup"><span data-stu-id="81dd0-122"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_ComputerSystem.Name="mycomputer"
```

</dd> </dl>

<span data-ttu-id="81dd0-123">La parola chiave **ClassDefsOnly** indica che la clausola restituisce un set di risultati di oggetti definizione di classe anziché le istanze effettive delle classi.</span><span class="sxs-lookup"><span data-stu-id="81dd0-123">The **ClassDefsOnly** keyword indicates that the clause returns a result set of class definition objects rather than actual instances of the classes.</span></span> <span data-ttu-id="81dd0-124">Questi oggetti sono le definizioni delle classi a cui appartengono le istanze dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="81dd0-124">These objects are the definitions of classes to which the endpoint instances belong.</span></span> <span data-ttu-id="81dd0-125">Ad esempio, la query nell'elenco seguente restituisce le definizioni per la [**\_ directory Win32**](/windows/desktop/CIMWin32Prov/win32-directory) e le classi [**Win32 \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) :</span><span class="sxs-lookup"><span data-stu-id="81dd0-125">For example, the query in the following list returns definitions for the [**Win32\_Directory**](/windows/desktop/CIMWin32Prov/win32-directory) and [**Win32\_ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) classes:</span></span>

<dl> <dt>

<span data-ttu-id="81dd0-126"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query</span><span class="sxs-lookup"><span data-stu-id="81dd0-126"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE ClassDefsOnly
```



</dd> <dt>

<span data-ttu-id="81dd0-127"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Risultati</span><span class="sxs-lookup"><span data-stu-id="81dd0-127"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_Directory
```

``` syntax
Win32_ComputerSystem
Win32_DiskPartition
```

</dd> </dl>

<span data-ttu-id="81dd0-128">Le parole chiave **ClassDefsOnly** e **ResultClass** si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="81dd0-128">The **ClassDefsOnly** and **ResultClass** keywords are mutually exclusive.</span></span> <span data-ttu-id="81dd0-129">Il loro utilizzo combinato causa un errore di query non valido.</span><span class="sxs-lookup"><span data-stu-id="81dd0-129">Using them together causes an invalid query error.</span></span>

<span data-ttu-id="81dd0-130">La parola chiave **RequiredAssocQualifier** indica che gli endpoint restituiti devono essere associati all'oggetto di origine tramite una classe di associazione che include il qualificatore specificato.</span><span class="sxs-lookup"><span data-stu-id="81dd0-130">The **RequiredAssocQualifier** keyword indicates that the returned endpoints must be associated with the source object through an association class that includes the specified qualifier.</span></span> <span data-ttu-id="81dd0-131">Questo tipo di filtro viene usato per eliminare ampi intervalli di endpoint a meno che gli endpoint non siano associati alla destinazione tramite un particolare set di classi di associazione con tag.</span><span class="sxs-lookup"><span data-stu-id="81dd0-131">This type of filtering is used to eliminate broad ranges of endpoints unless the endpoints are associated with the target through a particular set of tagged association classes.</span></span> <span data-ttu-id="81dd0-132">Ad esempio, la query nell'elenco seguente restituisce le istanze dell'endpoint se la classe Association include un qualificatore denominato **Association**.</span><span class="sxs-lookup"><span data-stu-id="81dd0-132">For example, the query in the following list returns endpoint instances if the association class includes a qualifier called **Association**.</span></span>

<dl> <dt>

<span data-ttu-id="81dd0-133"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query</span><span class="sxs-lookup"><span data-stu-id="81dd0-133"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"}
   WHERE RequiredAssocQualifier = Association
```



</dd> <dt>

<span data-ttu-id="81dd0-134"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Risultati</span><span class="sxs-lookup"><span data-stu-id="81dd0-134"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

``` syntax
Win32_ComputerSystem.Name="mycomputer"
Win32_DiskPartition.DeviceID="Disk #0, Partition #0"
```

</dd> </dl>

<span data-ttu-id="81dd0-135">La parola chiave **RequiredQualifier** indica che gli endpoint restituiti associati all'oggetto di origine devono includere il qualificatore specificato.</span><span class="sxs-lookup"><span data-stu-id="81dd0-135">The **RequiredQualifier** keyword indicates that the returned endpoints associated with the source object must include the specified qualifier.</span></span> <span data-ttu-id="81dd0-136">La parola chiave **RequiredQualifier** può essere utilizzata per includere tipi particolari di istanze nel set di risultati.</span><span class="sxs-lookup"><span data-stu-id="81dd0-136">The **RequiredQualifier** keyword can be used to include particular types of instances in the result set.</span></span> <span data-ttu-id="81dd0-137">Ad esempio, la query nell'elenco seguente restituisce le istanze dell'endpoint che includono un qualificatore denominato [**impostazioni locali**](swbemobjectpath-locale.md).</span><span class="sxs-lookup"><span data-stu-id="81dd0-137">For example, the query in the following list returns endpoint instances that include a qualifier called [**Locale**](swbemobjectpath-locale.md).</span></span>

<dl> <dt>

<span data-ttu-id="81dd0-138"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query</span><span class="sxs-lookup"><span data-stu-id="81dd0-138"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE RequiredQualifier = Locale
```



</dd> <dt>

<span data-ttu-id="81dd0-139"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Risultati</span><span class="sxs-lookup"><span data-stu-id="81dd0-139"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

``` syntax
Win32_ComputerSystem.Name="mycomputer"
Win32_DiskPartition.DeviceID="Disk #0, Partition #0"
```

</dd> </dl>

<span data-ttu-id="81dd0-140">La parola chiave **ResultClass** indica che gli endpoint restituiti associati all'oggetto di origine devono appartenere o essere derivati dalla classe specificata.</span><span class="sxs-lookup"><span data-stu-id="81dd0-140">The **ResultClass** keyword indicates that the returned endpoints associated with the source object must belong to or be derived from the specified class.</span></span> <span data-ttu-id="81dd0-141">Ad esempio, la query nell'elenco seguente restituisce le istanze dell'endpoint derivate dalla classe [**CIM \_ directory**](/windows/desktop/CIMWin32Prov/cim-directory) :</span><span class="sxs-lookup"><span data-stu-id="81dd0-141">For example, the query in the following list returns endpoint instances that are derived from the [**CIM\_Directory**](/windows/desktop/CIMWin32Prov/cim-directory) class:</span></span>

<dl> <dt>

<span data-ttu-id="81dd0-142"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query</span><span class="sxs-lookup"><span data-stu-id="81dd0-142"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE ResultClass = Cim_Directory
```



</dd> <dt>

<span data-ttu-id="81dd0-143"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Risultati</span><span class="sxs-lookup"><span data-stu-id="81dd0-143"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

</dd> </dl>

<span data-ttu-id="81dd0-144">Le parole chiave **ClassDefsOnly** e **ResultClass** si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="81dd0-144">The **ClassDefsOnly** and **ResultClass** keywords are mutually exclusive.</span></span> <span data-ttu-id="81dd0-145">Il loro utilizzo combinato causa un errore di query non valido.</span><span class="sxs-lookup"><span data-stu-id="81dd0-145">Using them together causes an invalid query error.</span></span>

<span data-ttu-id="81dd0-146">La parola chiave **RESULTROLE** indica che gli endpoint restituiti devono riprodurre un particolare ruolo nella propria associazione con l'oggetto di origine.</span><span class="sxs-lookup"><span data-stu-id="81dd0-146">The **ResultRole** keyword indicates that the returned endpoints must play a particular role in their association with the source object.</span></span> <span data-ttu-id="81dd0-147">Il ruolo viene definito dalla proprietà specificata, una proprietà Reference di tipo [ref](references.md). È ad esempio possibile usare la parola chiave **RESULTROLE** per recuperare tutti gli endpoint che hanno la proprietà **GroupComponent** nella propria associazione a un oggetto di origine, come illustrato nella query seguente.</span><span class="sxs-lookup"><span data-stu-id="81dd0-147">The role is defined by the specified property, a reference property of type [ref](references.md). For example, the **ResultRole** keyword can be used to retrieve all endpoints that have the **GroupComponent** property in their association with a source object, as the following query illustrates.</span></span>

<dl> <dt>

<span data-ttu-id="81dd0-148"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query</span><span class="sxs-lookup"><span data-stu-id="81dd0-148"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE ResultRole = GroupComponent
```



</dd> <dt>

<span data-ttu-id="81dd0-149"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Risultati</span><span class="sxs-lookup"><span data-stu-id="81dd0-149"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_ComputerSystem.Name="mycomputer"
```

</dd> </dl>

<span data-ttu-id="81dd0-150">La parola chiave **Role** indica che gli endpoint restituiti partecipano a un'associazione con l'oggetto di origine in cui l'oggetto di origine svolge un particolare ruolo.</span><span class="sxs-lookup"><span data-stu-id="81dd0-150">The **Role** keyword indicates that the returned endpoints participate in an association with the source object where the source object plays a particular role.</span></span> <span data-ttu-id="81dd0-151">Il ruolo viene definito dalla proprietà specificata, una proprietà Reference di tipo **ref**. È ad esempio possibile utilizzare la parola chiave **Role** per recuperare tutti gli endpoint associati a un oggetto di origine con la proprietà **GroupComponent** , come illustrato nella query seguente.</span><span class="sxs-lookup"><span data-stu-id="81dd0-151">The role is defined by the specified property, a reference property of type **ref**. For example, the **Role** keyword can be used to retrieve all endpoints associated with a source object that have the **GroupComponent** property, as the following query illustrates.</span></span>

<dl> <dt>

<span data-ttu-id="81dd0-152"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query</span><span class="sxs-lookup"><span data-stu-id="81dd0-152"><span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:</span></span>
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"}
   WHERE Role = GroupComponent
```



</dd> <dt>

<span data-ttu-id="81dd0-153"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Risultati</span><span class="sxs-lookup"><span data-stu-id="81dd0-153"><span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Results:</span></span>
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

</dd> </dl>

> [!Note]  
> <span data-ttu-id="81dd0-154">Le query complesse non possono usare "and" o "or" per separare le parole chiave per gli ASSOCIATOri di e i [riferimenti delle](references-of-statement.md) istruzioni.</span><span class="sxs-lookup"><span data-stu-id="81dd0-154">Complex queries cannot use "And" or "Or" to separate keywords for ASSOCIATORS OF and [REFERENCES OF](references-of-statement.md) statements.</span></span> <span data-ttu-id="81dd0-155">Inoltre, il segno di uguale è l'unico operatore valido che può essere utilizzato in tali query.</span><span class="sxs-lookup"><span data-stu-id="81dd0-155">Furthermore, the equal sign is the only valid operator that can be used in such queries.</span></span> <span data-ttu-id="81dd0-156">Viene ad esempio considerata valida la query seguente:</span><span class="sxs-lookup"><span data-stu-id="81dd0-156">For example, the following query is valid:</span></span>

 


```sql
ASSOCIATORS OF {win32_LogicalDisk="C:"} WHERE resultClass = Win32_Directory requiredQualifier = Dynamic
```



> [!Note]  
> <span data-ttu-id="81dd0-157">Gli esempi successivi non sono validi.</span><span class="sxs-lookup"><span data-stu-id="81dd0-157">The next examples are not valid.</span></span> <span data-ttu-id="81dd0-158">Il primo esempio non usa il segno di uguale e il secondo esempio tenta erroneamente di usare la parola chiave **e** .</span><span class="sxs-lookup"><span data-stu-id="81dd0-158">The first example does not use the equal sign and the second example erroneously attempts to use the **AND** keyword.</span></span>

 

``` syntax
Associators of {win32_LogicalDisk="C:"} where resultClass = Win32_Directory requiredQualifier <> Dynamic

Associators of {win32_LogicalDisk="C:"} where resultClass = Win32_Directory AND requiredQualifier = Dynamic
```

 

 
