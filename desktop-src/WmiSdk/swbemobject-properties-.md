---
description: La \_ Proprietà Properties dell'oggetto SWbemObject restituisce un oggetto SWbemPropertySet che è una raccolta di proprietà per la classe o l'istanza corrente. Questa proprietà è di sola lettura.
ms.assetid: 8dd49678-47e7-4c6b-ab12-42532065eaf2
ms.tgt_platform: multiple
title: Proprietà SWbemObject.Properties_ (wbemdisp. h)
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
ms.openlocfilehash: 2b215abb7a0ca466c8a93fe20f20518f8d7b2ec8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309821"
---
# <a name="swbemobjectproperties_-property"></a>Proprietà SWbemObject. Properties \_

La **proprietà \_ Properties** dell'oggetto [**SWbemObject**](swbemobject.md) restituisce un oggetto [**SWbemPropertySet**](swbempropertyset.md) che è una raccolta di proprietà per la classe o l'istanza corrente. Questa proprietà è di sola lettura.

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
SWbemObject.Properties_ As Object
```



## <a name="property-value"></a>Valore proprietà

## <a name="examples"></a>Esempio

L'esempio di codice PowerShell [Genera script di classe WMI PowerShell](https://Gallery.TechNet.Microsoft.Com/b435aa68-a1df-4f62-af05-1f504f683146) nella raccolta TechNet usa la \_ proprietà proprietà per generare uno script per ognuna delle classi WMI che elenca il nome della classe WMI e le proprietà.

Il codice seguente, tratto dall' [elenco di tutte le proprietà di un](https://Gallery.TechNet.Microsoft.Com/0f66f392-05b6-4431-b596-9379124d7a32) esempio di codice VBScript della classe WMI nella raccolta TechNet, elenca le proprietà di una classe WMI specificata.


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
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMOBJECT CLSID<br/>                                                           |
| IID<br/>                      | \_ISWBEMOBJECT IID<br/>                                                            |



 

 




