---
description: L'oggetto SWbemRefresher è un oggetto contenitore in grado di aggiornare i dati per tutti gli oggetti aggiunti. Il set di oggetti aggiunti, ogni elemento rappresentato da un'istanza di SWbemRefreshableItem può essere considerato come una raccolta ed enumerata.
ms.assetid: cc5872a1-932b-4b68-9f5e-a91d35c8e117
ms.tgt_platform: multiple
title: Oggetto SWbemRefresher (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher
- ISWbemRefresher
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f763ec4f738b612b9f2fef32871a63d6b170f96d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103968929"
---
# <a name="swbemrefresher-object"></a>Oggetto SWbemRefresher

L'oggetto **SWbemRefresher** è un oggetto contenitore in grado di aggiornare i dati per tutti gli oggetti aggiunti. Le istanze singole e gli enumeratori di istanza possono essere aggiunti o rimossi dal contenitore. Il set di oggetti aggiunti, ogni elemento rappresentato da un'istanza di [**SWbemRefreshableItem**](swbemrefreshableitem.md) , può essere considerato come una raccolta ed enumerata. Le istanze WMI di qualsiasi classe possono essere aggiunte all'oggetto **SWbemRefresher** . Anche se il provider per i dati dell'istanza non è un provider a prestazioni elevate, l'oggetto di aggiornamento può comunque aggiornare i dati nella chiamata di [**aggiornamento**](swbemrefresher-refresh.md) . Se i dati vengono forniti tramite un provider a prestazioni elevate e la proprietà [**AutoReconnect**](swbemrefresher-autoreconnect.md) è **true**, l'oggetto **SWbemRefresher** tenta di ristabilire una connessione interruppe al provider di dati. Questo oggetto può essere creato dalla chiamata **CreateObject** di VBScript.

È possibile eseguire l'operazione di aggiornamento chiamando il metodo [**SWbemRefresher. Refresh**](swbemrefresher-refresh.md) o [**\_ SWbemObjectEx. Refresh**](swbemobjectex-refresh-.md) .

## <a name="members"></a>Membri

L'oggetto **SWbemRefresher** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **SWbemRefresher** dispone di questi metodi.



| Metodo                                        | Descrizione                                                                                           |
|:----------------------------------------------|:------------------------------------------------------------------------------------------------------|
| [**Aggiungere**](swbemrefresher-add.md)             | Aggiunge un nuovo oggetto aggiornabile alla raccolta nell'oggetto di aggiornamento.<br/>                   |
| [**AddEnum**](swbemrefresher-addenum.md)     | Aggiunge un nuovo enumeratore all'oggetto di aggiornamento.<br/>                                             |
| [**DeleteAll**](swbemrefresher-deleteall.md) | Rimuove tutti gli elementi dalla raccolta nell'oggetto di aggiornamento.<br/>                             |
| [**Elemento**](swbemrefresher-item.md)           | Restituisce un elemento di aggiornamento specificato dalla raccolta.<br/>                                    |
| [**Aggiorna**](swbemrefresher-refresh.md)     | Aggiorna tutti gli elementi contenuti nell'oggetto di aggiornamento.<br/>                          |
| [**Rimuovi**](swbemrefresher-remove.md)       | Rimuove dall'aggiornamento l'oggetto o il set di oggetti dell'elemento di aggiornamento con un indice specificato.<br/> |



 

### <a name="properties"></a>Proprietà

L'oggetto **SWbemRefresher** dispone di queste proprietà.



| Proprietà                                                         | Tipo di accesso          | Descrizione                                                                                                           |
|:-----------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------------------|
| [**AutoReconnect**](swbemrefresher-autoreconnect.md)<br/> | Sola lettura<br/> | Indica se l'aggiornamento viene riconnesso automaticamente a un provider remoto se la connessione è interruppe.<br/> |
| [**Conteggio**](swbemrefresher-count.md)<br/>                 | Sola lettura<br/> | Contiene il numero di elementi nell'oggetto di aggiornamento.<br/>                                                      |



 

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrata la creazione di un oggetto **SWbemRefresher** , l'utilizzo dei metodi [**Add**](swbemrefresher-add.md) e [**AddEnum**](swbemrefresher-addenum.md) per archiviare una singola istanza e un'istanza di enumerazione, l'aggiornamento dei dati e l'utilizzo della proprietà Item per ottenere gli oggetti [**SWbemRefreshableItem**](swbemrefreshableitem.md) .


```VB
' Get namespace connections
set objServicesCimv2 = GetObject("winmgmts:root\cimv2")
set objServicesDefault = GetObject("winmgmts:root\default")

' Create a refresher object
set objRefresher = CreateObject("WbemScripting.SWbemRefresher")

' Add a single object (SWbemObjectEx) to the refresher. The "@"
' is used because _CIMOMIdentification is a singleton class- only 
' one instance exists. Note that the
' SWbemRefreshableItem.Object property must 
' be specified or the SWbemRefresher.Refresh call will fail.

set objRefreshableItem1 = objRefresher. _
    Add (objServicesDefault, "__CIMOMIdentification=@").Object

' Add an enumerator (SWbemObjectSet object)
' to the refresher. Note that the
' SWbemRefreshableItem.ObjectSet property
' must be specified or the SWbemRefresher.Refresh call will fail. 
set objRefreshableItem2 = objRefresher. _
    AddEnum (objServicesCimv2, "Win32_Process").ObjectSet

' Display number of items in refresher and update the data.
MsgBox "Number of items in refresher = " & objRefresher.Count
objRefresher.Refresh

' Iterate through the refresher. SWbemRefreshable
' Item.IsSet checks for whether the item is an enumerator.
for each RefreshableItem in objRefresher
 if RefreshableItem.IsSet then  
    MsgBox "Item with index " & RefreshableItem.Index &_
    " is an enumerator containing "_
    & RefreshableItem.ObjectSet.Count & " processes"
 else  
      MsgBox "Item with index " & RefreshableItem.Index _
          & " is a single object containing WMI version "_
          &  objRefreshableItem1.VersionCurrentlyRunning
 end if
next
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMREFRESHER CLSID<br/>                                                        |
| IID<br/>                      | \_ISWBEMREFRESHER IID<br/>                                                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SWbemRefreshableItem**](swbemrefreshableitem.md)
</dt> <dt>

[**SWbemObjectEx**](swbemobjectex.md)
</dt> <dt>

[Oggetti API di scripting](scripting-api-objects.md)
</dt> </dl>

 

 




