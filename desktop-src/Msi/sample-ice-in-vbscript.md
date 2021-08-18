---
description: Questo codice di esempio deriva da un'azione personalizzata ICE (ICE08). L'ice verifica che ogni componente nella tabella Component abbia un GUID univoco. Se la tabella Component non esiste, non viene eseguita alcuna convalida.
ms.assetid: 785c3fd6-7120-4532-b055-b73a9a44f75d
title: Ice di esempio in VBScript
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a21ce87547923cca67b115f1f5c9ea93c4cfac6676924e9ad88e7f1d2b332d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996311"
---
# <a name="sample-ice-in-vbscript"></a>Ice di esempio in VBScript

Questo codice di esempio deriva da un'azione personalizzata ICE ( [ICE08](ice08.md)). Ice verifica che ogni componente nella tabella [Component abbia](component-table.md) un [GUID univoco](guid.md). Se la tabella Component non esiste, non viene eseguita alcuna convalida.


```VB
Function ICE08()

'Give creation data
Set recInfo=Installer.CreateRecord(1)
recInfo.StringData(0)="ICE08" & Chr(9) & "3" 
    & Chr(9) & "Created 05/21/98 by <insert 
    author's name here>"
Message &h03000000, recInfo

'Give last modification date
recInfo.StringData(0)="ICE08" & Chr(9) & "3" 
    & Chr(9) & "Modified 05/21/98 by <insert 
    author's name here>"
Message &h03000000, recInfo

'Give description of test
recInfo.StringData(0)="ICE08" & Chr(9) & "3" 
    & Chr(9) & "Checks for duplicate GUIDs 
    in Component table"
Message &h03000000, recInfo

'Is there a Component table in the database?
iStat = Database.TablePersistent("Component")
If 1 <> iStat Then
recInfo.StringData(0)="ICE08" & Chr(9) & "2" 
    & Chr(9) & "Table: 'Component' missing. 
    ICE08 cannot continue its validation." 
    & Chr(9) & "https://mypage2"
Message &h03000000, recInfo
ICE08 = 1
Exit Function
End If

'process component table
Set view=Database.OpenView("SELECT 
    `Component`,`ComponentId` FROM 
    `Component` ORDER BY `ComponentId`")
view.Execute
Do
Set rec=view.Fetch
If rec Is Nothing Then Exit Do

'compare for duplicate 
If lastGuid=rec.StringData(2) Then
rec.StringData(0)="ICE08" & Chr(9) 
    & "1" & Chr(9) & "Component: [1] 
    has a duplicate GUID: [2]" & Chr(9) 
    & "https://mypage2" & Chr(9) & 
    "Component" & Chr(9) & "ComponentId" & Chr(9) & "[1]"
Message &h03000000,rec
End If

'set for next compare
lastGuid=rec.StringData(2)
Loop

'Return iesSuccess 
ICE08 = 1

End Function
```



 

 



