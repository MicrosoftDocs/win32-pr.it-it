---
description: Recupera tutte le istanze associate a una determinata istanza di origine.
ms.assetid: d6bd9643-523d-4d81-8bf1-da52ccc7524d
ms.tgt_platform: multiple
title: Istruzione ASSOCIATORS OF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9af4b3d6455e81f87882bdd185ac7a8ef245f2d57c5d8f2c863f58d9c30c7b34
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071581"
---
# <a name="associators-of-statement"></a>Istruzione ASSOCIATORS OF

L'istruzione ASSOCIATORS OF recupera tutte le istanze associate a una determinata istanza di origine. Le istanze recuperate vengono definite endpoint. Ogni endpoint viene restituito il numero di volte in cui sono presenti associazioni tra l'endpoint e l'oggetto di origine. Si supponga, ad esempio, che siano presenti istanze A, B, X e Y. Esistono due istanze di associazione, una che collega A e X e un'altra che collega B e Y. La query seguente restituisce il singolo endpoint X:


```sql
ASSOCIATORS OF {A}
```



Tuttavia, se è presente un'altra associazione che collega A e X, la query precedente restituisce due endpoint X.

La sintassi di base per l'istruzione ASSOCIATORS OF è la seguente:

``` syntax
ASSOCIATORS OF {ObjectPath}
```

Si noti che le parentesi graffe fanno parte della sintassi. Qualsiasi percorso di oggetto valido può essere usato per ObjectPath. I token all'interno del percorso dell'oggetto non possono contenere spazi vuoti. Ad esempio, la query nell'elenco seguente restituisce le istanze associate al disco logico specificato:

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"}
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Risultati:
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

``` syntax
Win32_ComputerSystem.Name="mycomputer"
Win32_DiskPartition.DeviceID="Disk #0, Partition #0"
```

</dd> </dl>

Come per l'istruzione [SELECT](select-statement-for-data-queries.md), un'istruzione ASSOCIATORS OF può includere una clausola [WHERE](where-clause.md), ma la clausola WHERE per un'istruzione ASSOCIATORS OF è molto diversa dalla clausola SELECT statementWHERE.

La [clausola WHERE](where-clause.md) dell'istruzione ASSOCIATORS OF può includere una o più delle parole chiave predefinite seguenti e i relativi valori:


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



Si noti che le sottoclause facoltative non sono separate da virgole.

La **parola chiave AssocClass** indica che gli endpoint restituiti devono essere associati all'origine tramite la classe specificata o una delle classi derivate. Ad esempio, la query nell'elenco seguente restituisce solo gli endpoint associati all'origine tramite la classe di associazione [**\_ SystemDevices Win32**](/windows/desktop/CIMWin32Prov/win32-systemdevices) o una delle classi derivate:

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE AssocClass = Win32_SystemDevices
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Risultati:
</dt> <dd>

``` syntax
Win32_ComputerSystem.Name="mycomputer"
```

</dd> </dl>

La **parola chiave ClassDefsOnly** indica che la clausola restituisce un set di risultati di oggetti definizione di classe anziché istanze effettive delle classi. Questi oggetti sono le definizioni delle classi a cui appartengono le istanze dell'endpoint. Ad esempio, la query nell'elenco seguente restituisce le definizioni per le [**classi \_ Win32 Directory**](/windows/desktop/CIMWin32Prov/win32-directory) e [**Win32 \_ ComputerSystem:**](/windows/desktop/CIMWin32Prov/win32-computersystem)

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE ClassDefsOnly
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Risultati:
</dt> <dd>

``` syntax
Win32_Directory
```

``` syntax
Win32_ComputerSystem
Win32_DiskPartition
```

</dd> </dl>

Le **parole chiave ClassDefsOnly e** **ResultClass** si escludono a vicenda. L'uso di queste due combinazioni causa un errore di query non valido.

La **parola chiave RequiredAssocQualifier** indica che gli endpoint restituiti devono essere associati all'oggetto di origine tramite una classe di associazione che include il qualificatore specificato. Questo tipo di filtro viene usato per eliminare ampi intervalli di endpoint, a meno che gli endpoint non siano associati alla destinazione tramite un particolare set di classi di associazione con tag. Ad esempio, la query nell'elenco seguente restituisce istanze di endpoint se la classe di associazione include un qualificatore denominato **Association**.

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"}
   WHERE RequiredAssocQualifier = Association
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Risultati:
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

``` syntax
Win32_ComputerSystem.Name="mycomputer"
Win32_DiskPartition.DeviceID="Disk #0, Partition #0"
```

</dd> </dl>

La **parola chiave RequiredQualifier** indica che gli endpoint restituiti associati all'oggetto di origine devono includere il qualificatore specificato. La **parola chiave RequiredQualifier** può essere usata per includere tipi specifici di istanze nel set di risultati. Ad esempio, la query nell'elenco seguente restituisce istanze di endpoint che includono un qualificatore denominato [**Impostazioni locali**](swbemobjectpath-locale.md).

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE RequiredQualifier = Locale
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Risultati:
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

``` syntax
Win32_ComputerSystem.Name="mycomputer"
Win32_DiskPartition.DeviceID="Disk #0, Partition #0"
```

</dd> </dl>

La **parola chiave ResultClass** indica che gli endpoint restituiti associati all'oggetto di origine devono appartenere o essere derivati dalla classe specificata. Ad esempio, la query nell'elenco seguente restituisce le istanze dell'endpoint derivate dalla [**classe \_ CIM Directory:**](/windows/desktop/CIMWin32Prov/cim-directory)

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE ResultClass = Cim_Directory
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Risultati:
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

</dd> </dl>

Le **parole chiave ClassDefsOnly e** **ResultClass** si escludono a vicenda. L'uso di queste due combinazioni causa un errore di query non valido.

La **parola chiave ResultRole** indica che gli endpoint restituiti devono svolgere un ruolo specifico nella relativa associazione all'oggetto di origine. Il ruolo è definito dalla proprietà specificata, una proprietà di riferimento di tipo [ref](references.md). Ad esempio, la parola chiave **ResultRole** può essere usata per recuperare tutti gli endpoint che hanno la proprietà **GroupComponent** nella relativa associazione a un oggetto di origine, come illustrato nella query seguente.

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"} WHERE ResultRole = GroupComponent
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Risultati:
</dt> <dd>

``` syntax
Win32_ComputerSystem.Name="mycomputer"
```

</dd> </dl>

La parola chiave **Role** indica che gli endpoint restituiti fanno parte di un'associazione con l'oggetto di origine in cui l'oggetto di origine svolge un ruolo specifico. Il ruolo è definito dalla proprietà specificata, una proprietà di riferimento di tipo **ref**. Ad esempio, la parola chiave **Role** può essere usata per recuperare tutti gli endpoint associati a un oggetto di origine con la **proprietà GroupComponent,** come illustrato nella query seguente.

<dl> <dt>

<span id="Query_"></span><span id="query_"></span><span id="QUERY_"></span>Query:
</dt> <dd>


```sql
ASSOCIATORS OF {Win32_LogicalDisk.DeviceID="C:"}
   WHERE Role = GroupComponent
```



</dd> <dt>

<span id="Results_"></span><span id="results_"></span><span id="RESULTS_"></span>Risultati:
</dt> <dd>

``` syntax
Win32_Directory.Name="C:\\"
```

</dd> </dl>

> [!Note]  
> Le query complesse non possono usare "And" o "Or" per separare le parole chiave per le istruzioni ASSOCIATORS OF [e REFERENCES OF.](references-of-statement.md) Inoltre, il segno di uguale è l'unico operatore valido che può essere usato in tali query. Viene ad esempio considerata valida la query seguente:

 


```sql
ASSOCIATORS OF {win32_LogicalDisk="C:"} WHERE resultClass = Win32_Directory requiredQualifier = Dynamic
```



> [!Note]  
> Gli esempi successivi non sono validi. Il primo esempio non usa il segno di uguale e il secondo esempio tenta erroneamente di usare la **parola chiave AND.**

 

``` syntax
Associators of {win32_LogicalDisk="C:"} where resultClass = Win32_Directory requiredQualifier <> Dynamic

Associators of {win32_LogicalDisk="C:"} where resultClass = Win32_Directory AND requiredQualifier = Dynamic
```

 

 
