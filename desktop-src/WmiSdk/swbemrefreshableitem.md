---
description: Rappresenta un singolo elemento in un oggetto SWbemRefresher.
ms.assetid: 6a12c8eb-3ef9-4292-810c-6954294fc8c7
ms.tgt_platform: multiple
title: Oggetto SWbemRefreshableItem (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefreshableItem
- ISWbemRefreshableItem
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4bc4f85145926aba2bd050052c33eb5669dfee8a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103761411"
---
# <a name="swbemrefreshableitem-object"></a>Oggetto SWbemRefreshableItem

L'oggetto **SWbemRefreshableItem** rappresenta un singolo elemento in un oggetto [**SWbemRefresher**](swbemrefresher.md) . Un oggetto **SWbemRefreshableItem** viene ottenuto tramite i metodi [**Add**](swbemrefresher-add.md) e [**AddEnum**](swbemrefresher-addenum.md) di [**SWbemRefresher**](swbemrefresher.md). Questo oggetto non può essere creato dalla chiamata [CreateObject](creating-an-object-using-vbscript.md) di VBScript.

## <a name="members"></a>Membri

L'oggetto **SWbemRefreshableItem** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **SWbemRefreshableItem** dispone di questi metodi.



| Metodo                                        | Descrizione                                                                                                             |
|:----------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**Rimuovi**](swbemrefreshableitem-remove.md) | Rimuove l'oggetto **SWbemRefreshableItem** dall'oggetto [**SWbemRefresher**](swbemrefresher.md) padre.<br/> |



 

### <a name="properties"></a>Proprietà

L'oggetto **SWbemRefreshableItem** dispone di queste proprietà.



| Proprietà                                                       | Tipo di accesso           | Descrizione                                                                                                                          |
|:---------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------|
| [**Indice**](swbemrefreshableitem-index.md)<br/>         | Lettura/Scrittura<br/> | Indice dell'elemento nell'oggetto [**SWbemRefresher**](swbemrefresher.md) padre.<br/>                                          |
| [**IsSet**](swbemrefreshableitem-isset.md)<br/>         | Lettura/Scrittura<br/> | Indica se l'oggetto **SWbemRefreshableItem** rappresenta un singolo oggetto o un set di oggetti.<br/>                        |
| [**Oggetto**](swbemrefreshableitem-object.md)<br/>       | Lettura/Scrittura<br/> | Rappresenta un singolo oggetto [**SWbemObject**](swbemobject.md) che viene aggiornato.<br/>                                          |
| [**ObjectSet**](swbemrefreshableitem-objectset.md)<br/> | Lettura/Scrittura<br/> | Rappresenta il set di oggetti da aggiornare.<br/>                                                                                |
| [**Aggiornamento**](swbemrefreshableitem-refresher.md)<br/> | Sola lettura<br/>  | Rappresenta l'oggetto [**SWbemRefresher**](swbemrefresher.md) padre che contiene l'oggetto **SWbemRefreshableItem** .<br/> |



 

## <a name="remarks"></a>Commenti

Non è possibile usare il metodo VBScript [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) per creare direttamente oggetti **SWbemRefreshableItem** .

## <a name="examples"></a>Esempio

Nello script seguente viene illustrata la creazione di un oggetto [**SWbemRefresher**](swbemrefresher.md) e l'aggiunta di un singolo oggetto e di un enumeratore **SWbemRefreshableItem** .


```VB
' Get some namespace connections
set cimv2 = GetObject("winmgmts:root\cimv2")
set default = GetObject("winmgmts:root\default")    

' Create a refresher
set refresher = CreateObject("WbemScripting.SWbemRefresher")

' Add a single object to the refresher.
' The @ is used because this is a singleton 
' system class so only one instance exists.
set item1 = refresher.Add (default, "__CIMOMIdentification=@").Object
MsgBox "WMI Version " item1
' Add an enumerator to the refresher.
' Note that the SWbemRefreshableItem.ObjectSet 
' property must be used to designate
' this as an object set rather than a single object.
set item2 = refresher.AddEnum (cimv2, "Win32_Process").ObjectSet

' Loop three times, refreshing the items

For I= 1 To 3
MsgBox "Refresh number " & I
refresher.Refresh

' Iterate through the collection of
' processes in item2 with name of wscript
    For each process in item2
        If process.name = "wscript.exe" then
        MsgBox "Process " & process.Name & _
           " Page Faults " & process.PageFaults
        End If
    Next 
Next

' Clear out the refresher
refresher.DeleteAll 

' The following should return 0
MsgBox "Number of items in Refresher after DeleteAll " _
    & refresher.Count
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMREFRESHABLEITEM CLSID<br/>                                                  |
| IID<br/>                      | \_ISWBEMREFRESHABLEITEM IID<br/>                                                   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti API di scripting](scripting-api-objects.md)
</dt> </dl>

 

 




