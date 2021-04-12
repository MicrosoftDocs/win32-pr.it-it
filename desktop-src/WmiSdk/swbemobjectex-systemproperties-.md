---
description: Restituisce un oggetto SWbemPropertySet che contiene la raccolta di proprietà di sistema WMI che si applicano all'oggetto.
ms.assetid: e95c325a-8851-4f55-a99d-4346d064e308
ms.tgt_platform: multiple
title: Proprietà SWbemObjectEx.SystemProperties_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx.SystemProperties_
- ISWbemObjectEx.SystemProperties_
- ISWbemObjectEx.get_SystemProperties_
- ISWbemObjectEx.put_SystemProperties_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cf8b7e15536c0d4e3116f0583662b3cd0b7d0887
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233672"
---
# <a name="swbemobjectexsystemproperties_-property"></a>SWbemObjectEx.Sys\_ Proprietà temProperties

La **proprietà \_ SystemProperties** dell'oggetto [**SWbemObjectEx**](swbemobjectex.md) restituisce un oggetto [**SWbemPropertySet**](swbempropertyset.md) che contiene la raccolta di [proprietà di sistema WMI](wmi-system-properties.md) che si applicano all'oggetto.

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
SWbemObjectEx.SystemProperties_ As Object
```



## <a name="property-value"></a>Valore proprietà

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente vengono recuperati i valori delle proprietà per la \_ classe del processo Win32.


```VB
Set objWmi = GetObject ("winmgmts:root\cimv2")
Set objClass = objWmi.Get("Win32_Process")

' SWbemObjectEx.SystemProperties_ returns 
' an SWbemPropertySet object that contains the collection
' of sytem properties for Win32_Process class

For Each objProperty In objClass.SystemProperties_

    WScript.Echo vbCrLf & objProperty.Name & ":"

    ' Have to take into account that
    ' __Derivation is an array

    If Not objProperty.IsArray Then
        WScript.Echo vbTab & objProperty.Value
    Else
        For Each strValue In objProperty.Value
            WScript.Echo vbTab & strValue
        Next
    End If

Next
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMOBJECTEX CLSID<br/>                                                         |
| IID<br/>                      | \_ISWBEMOBJECTEX IID<br/>                                                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SWbemObjectEx**](swbemobjectex.md)
</dt> </dl>

 

 




