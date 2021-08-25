---
description: La proprietà \_ Properties dell'oggetto SWbemObject restituisce un oggetto SWbemPropertySet che è una raccolta delle proprietà per la classe o l'istanza corrente. Questa proprietà è di sola lettura.
ms.assetid: 8dd49678-47e7-4c6b-ab12-42532065eaf2
ms.tgt_platform: multiple
title: SWbemObject.Properties_ proprietà (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Properties_
- ISWbemObject.Properties_
- ISWbemObject.get_Properties_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 413e13b725fce117b9358a254a860c631fc5fbe3158bf7f6d277ebca22647168
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857311"
---
# <a name="swbemobjectproperties_-property"></a>Proprietà SWbemObject.Properties \_

La **\_ proprietà Properties** dell'oggetto [**SWbemObject**](swbemobject.md) restituisce un [**oggetto SWbemPropertySet**](swbempropertyset.md) che è una raccolta di proprietà per la classe o l'istanza corrente. Questa proprietà è di sola lettura.

Per una spiegazione di questa sintassi, vedere [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
SWbemObject.Properties_ As Object
```



## <a name="property-value"></a>Valore proprietà

## <a name="examples"></a>Esempio

L'esempio di codice PowerShell Generate Powershell WMI Class Scripts (Genera script di classe WMI di [PowerShell)](https://Gallery.TechNet.Microsoft.Com/b435aa68-a1df-4f62-af05-1f504f683146) in TechNet Gallery usa la proprietà Properties per generare uno script per ognuna delle classi WMI in cui verranno elencati il nome della classe WMI e \_ le proprietà.

Il codice seguente, tratto dall'esempio di codice VBScript Elenca tutte le proprietà per una classe [WMI](https://Gallery.TechNet.Microsoft.Com/0f66f392-05b6-4431-b596-9379124d7a32) nella raccolta TechNet, elenca le proprietà per una classe WMI specificata.


```VB
strComputer = "." 
strNameSpace = "root\cimv2" 
strClass = "Win32_Service" 
  
Set objClass = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & _  
    strComputer & "\" & strNameSpace & ":" & strClass) 
  
WScript.Echo strClass & " Class Properties" 
WScript.Echo "------------------------------" 
  
For Each objClassProperty In objClass.Properties_ 
    WScript.Echo objClassProperty.Name 
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
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemObject<br/>                                                            |



 

 




