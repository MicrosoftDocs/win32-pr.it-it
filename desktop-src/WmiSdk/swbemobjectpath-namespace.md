---
description: La proprietà Namespace dell'oggetto SWbemObjectPath contiene il nome dello spazio dei nomi che fa parte del percorso dell'oggetto.
ms.assetid: be88670d-6f0d-4b9d-886f-3e70bf4758ed
ms.tgt_platform: multiple
title: Proprietà SWbemObjectPath.Namespace (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Namespace
- ISWbemObjectPath.Namespace
- ISWbemObjectPath.get_Namespace
- ISWbemObjectPath.put_Namespace
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f9daa9b74918c16d58546f6830bb474e40e449a8c596f61f7e27f03342c47b4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119503761"
---
# <a name="swbemobjectpathnamespace-property"></a>Proprietà SWbemObjectPath.Namespace

La **proprietà Namespace** dell'oggetto [**SWbemObjectPath**](swbemobjectpath.md) contiene il nome dello spazio dei nomi che fa parte del percorso dell'oggetto. Ad esempio, il percorso seguente mostra la proprietà dello spazio dei nomi che restituisce \\ cimv2 radice:

``` syntax
\\computer\root\cimv2:win32_logicaldisk="a:"
```

Per la spiegazione della sintassi, vedere [Convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
SWbemObjectPath.Namespace As String
```



## <a name="property-value"></a>Valore proprietà

## <a name="examples"></a>Esempio

L'esempio seguente illustra come ottenere il nome dello spazio dei nomi dalle istanze di [**\_ LogicalDisk Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) che sono dischi rigidi. Lo script si connette allo spazio dei nomi predefinito.


```VB
Const HARD_DISK = 3
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer)

Set colDisks = objWMIService.ExecQuery _
    ("Select * from Win32_LogicalDisk " _
    & "Where DriveType = " & HARD_DISK & "")
For Each objDisk in colDisks
    Set objpath = objDisk.path_
    Wscript.Echo "Path of Win32_Logical disk instance " _
    & objDisk.DeviceID & " = " & objpath.Namespace   
Next
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectPath<br/>                                                       |
| IID<br/>                      | IID \_ ISWbemObjectPath<br/>                                                        |



 

