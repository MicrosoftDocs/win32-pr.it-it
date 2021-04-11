---
description: Per le query sui dati dello schema viene utilizzata l'istruzione SELECT con una sintassi simile a quella per le query di dati.
ms.assetid: e7150aaa-5829-4d64-a13b-39f83adc5b98
ms.tgt_platform: multiple
title: Istruzione SELECT per le query dello schema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91f9f3f9ae8cc11a94d4d868e36af56ee7dffd2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233458"
---
# <a name="select-statement-for-schema-queries"></a>Istruzione SELECT per le query dello schema

Per le query sui dati dello schema viene utilizzata l'istruzione SELECT con una sintassi simile a quella per le [query di dati](select-statement-for-data-queries.md). La differenza consiste nell'utilizzo di una classe speciale denominata "meta \_ Class", che identifica la query come query dello schema.

Nell'esempio seguente vengono richieste tutte le definizioni di classe nello spazio dei nomi corrente.


```sql
SELECT * FROM meta_class
```



Le query di schema supportano solo " \* ". Per restringere l'ambito delle definizioni restituite, un provider può aggiungere una clausola WHERE che specifica una determinata classe.

Nell'esempio seguente viene illustrato come aggiungere una clausola WHERE per specificare una classe specifica.


```sql
SELECT * FROM meta_class WHERE __this ISA "Win32_LogicalDisk"
```



La speciale **\_ \_ proprietà denominata identifica la classe** di destinazione per una query di schema. Si noti che è necessario usare l'operatore ISA con **\_ \_ questa** proprietà per richiedere definizioni per le sottoclassi della classe di destinazione. La query precedente restituisce la definizione per la classe [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) e le definizioni per tutte le relative sottoclassi.

Nell'esempio seguente viene illustrato come richiedere una definizione di classe per una singola classe utilizzando la proprietà di sistema della **\_ \_ classe** .


```sql
SELECT * FROM meta_class WHERE __Class = "Win32_LogicalDisk"
```



Questa query equivale a chiamare il metodo [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) o [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) con il parametro del percorso dell'oggetto impostato su "Win32 \_ disco logico".

Nell'esempio di codice VBScript seguente vengono recuperate tutte le classi figlio di una classe WMI di primo livello. La \_ \_ proprietà di sistema WMI Dynasty include il nome della classe di primo livello da cui viene derivata una classe, che è possibile usare per recuperare tutte le classi in uno spazio dei nomi derivato da una classe di primo livello, inclusa quella classe.


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



Il codice VBScript seguente recupera le classi figlio immediate per una classe WMI.


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



Il codice VBScript seguente recupera le classi di primo livello. Per tutte le classi di primo livello in uno spazio dei nomi WMI, la \_ \_ proprietà di sistema superclass è null. Pertanto, è possibile recuperare le classi di primo livello cercando una superclasse null.


```VB
 Retrieve top level classes in root\cimv2

Set objWmi = GetObject ("winmgmts:root\cimv2")

Set colClasses = objWmi.ExecQuery _
    ("Select * From meta_class Where __Superclass Is Null")

For Each objClass In colClasses
    WScript.Echo objClass.SystemProperties_("__Class")

```



 

 
