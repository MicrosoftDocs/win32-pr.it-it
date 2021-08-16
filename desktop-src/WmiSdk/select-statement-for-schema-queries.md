---
description: Le query di dati dello schema usano l'istruzione SELECT con una sintassi simile a quella per le query di dati.
ms.assetid: e7150aaa-5829-4d64-a13b-39f83adc5b98
ms.tgt_platform: multiple
title: Istruzione SELECT per le query dello schema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd08cffa3fccc9a8cc2bf50452dcefcc1b7bfc0a62e512069b2db098bc6d13c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315675"
---
# <a name="select-statement-for-schema-queries"></a>Istruzione SELECT per le query dello schema

Le query sui dati dello schema usano l'istruzione SELECT con una sintassi simile a quella per [le query di dati](select-statement-for-data-queries.md). La differenza è l'uso di una classe speciale denominata \_ "metaclasse", che identifica la query come query dello schema.

Nell'esempio seguente vengono richieste tutte le definizioni di classe che si trova all'interno dello spazio dei nomi corrente.


```sql
SELECT * FROM meta_class
```



Le query dello schema supportano solo " \* ". Per limitare l'ambito delle definizioni restituite, un provider può aggiungere una clausola WHERE che specifica una classe specifica.

Nell'esempio seguente viene illustrato come aggiungere una clausola WHERE per specificare una classe specifica.


```sql
SELECT * FROM meta_class WHERE __this ISA "Win32_LogicalDisk"
```



La proprietà speciale denominata **\_ \_ this** identifica la classe di destinazione per una query dello schema. Si noti che l'operatore ISA deve essere usato con la proprietà **\_ \_ this** per richiedere definizioni per le sottoclassi della classe di destinazione. La query precedente restituisce la definizione per la [**classe \_ LogicalDisk Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) e le definizioni per tutte le relative sottoclassi.

Nell'esempio seguente viene illustrato come richiedere una definizione di classe per una singola classe usando la proprietà di sistema **\_ \_ Class.**


```sql
SELECT * FROM meta_class WHERE __Class = "Win32_LogicalDisk"
```



Questa query equivale a chiamare il metodo [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) o [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) con il parametro del percorso dell'oggetto impostato su "Win32 \_ LogicalDisk".

L'esempio di codice VBScript seguente recupera tutte le classi figlio di una classe WMI di primo livello. La proprietà di sistema Dinastino WMI contiene il nome della classe di primo livello da cui deriva una classe, che è possibile usare per recuperare tutte le classi in uno spazio dei nomi derivato da una classe di primo livello, inclusa tale \_ \_ classe.


```VB
' Retrieve immediate child classes for Cim_DataFile

Set objWmi = GetObject ("winmgmts:root\cimv2")

Set colClasses = objWmi.ExecQuery _ 
    ("Select * From meta_class " _
    & "Where __Dynasty = 'Win32_CurrentTime'")

For Each objClass In colClasses 
    WScript.Echo objClass.SystemProperties_("__Class")
Next
```



Il codice VBScript seguente recupera una classe figlio immediata per una classe WMI.


```VB
' Retrieve immediate child classes for Cim_DataFile

Set objWmi = GetObject ("winmgmts:root\cimv2")

Set colClasses = objWmi.ExecQuery _ 
    ("Select * From meta_class " _
    & "Where __Superclass = 'Cim_DataFile'")

For Each objClass In colClasses 
    WScript.Echo objClass.SystemProperties_("__Class")
Next
```



Il codice VBScript seguente recupera le classi di primo livello. Per tutte le classi di primo livello in uno spazio dei nomi WMI, la \_ \_ proprietà di sistema Superclass è Null. È quindi possibile recuperare le classi di primo livello cercando una superclasse Null.


```VB
 Retrieve top level classes in root\cimv2

Set objWmi = GetObject ("winmgmts:root\cimv2")

Set colClasses = objWmi.ExecQuery _
    ("Select * From meta_class Where __Superclass Is Null")

For Each objClass In colClasses
    WScript.Echo objClass.SystemProperties_("__Class")

```



 

 
