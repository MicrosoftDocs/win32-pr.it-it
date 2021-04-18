---
description: Usare la proprietà Count dell'oggetto SWbemObjectSet per determinare il numero di elementi presenti in una raccolta SWbemObjectSet. Questa proprietà è di sola lettura.
ms.assetid: ad3d1265-a11e-4962-b1f3-60092d2f79ef
ms.tgt_platform: multiple
title: Proprietà SWbemObjectSet. Count (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.Count
- ISWbemObjectSet.Count
- ISWbemObjectSet.get_Count
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3154e22bbdbc75080ceebdf8b1eef602cf5c3be3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318508"
---
# <a name="swbemobjectsetcount-property"></a>Proprietà SWbemObjectSet. Count

Usare la proprietà **count** dell'oggetto [**SWbemObjectSet**](swbemobjectset.md) per determinare il numero di elementi presenti in una raccolta **SWbemObjectSet** . Questa proprietà è di sola lettura.

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
SWbemObjectSet.Count As Integer
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

Una cosa da fare quando si usa count è che WMI non mantiene un conteggio parziale del numero di elementi in una raccolta. Se si richiede il conteggio per una raccolta, WMI non può rispondere immediatamente con un numero; al contrario, deve contare letteralmente gli elementi, enumerando l'intero insieme. Per una raccolta con un numero relativamente basso di elementi, ad esempio servizi, questa enumerazione richiede probabilmente meno di un secondo. Il conteggio del numero di eventi in una raccolta di log eventi, tuttavia, può richiedere molto più tempo.

Si supponga quindi di voler visualizzare i valori delle proprietà per ogni evento nella raccolta. In tal caso, WMI dovrà enumerare l'intera raccolta una seconda volta.

> [!Note]  
> Se si tenta di ottenere questa proprietà da un oggetto [**SWbemObjectSet**](swbemobjectset.md) restituito da un metodo in cui i flag specificati sono inclusi il flag wbemFlagForwardOnly, verrà visualizzato un errore wbemErrFailed.

 

## <a name="examples"></a>Esempio

Nella maggior parte dei casi, l'unica cosa che si può fare con un SWbemObjectSet è enumerare tutti gli oggetti contenuti nella raccolta stessa. Il conteggio dei conteggi, tuttavia, può essere utile nell'esecuzione di script per l'amministrazione del sistema. Come suggerisce il nome, Count indica il numero di elementi nella raccolta. Questo script, ad esempio, recupera una raccolta di tutti i servizi installati in un computer e quindi restituisce il numero totale di servizi trovati:


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
Wscript.Echo "Services installed on target computer: " & colSWbemObjectSet.Count

```



Ciò che rende utile count è la possibilità di indicare se un'istanza specifica è disponibile in un computer. Questo script, ad esempio, recupera una raccolta di tutti i servizi in un computer con il nome W3SVC. Se il conteggio è 0 (ed è valido per le raccolte senza istanze), significa che il servizio W3SVC non è installato nel computer.


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.ExecQuery _
    ("SELECT * FROM Win32_Service WHERE Name='w3svc'")
If colSWbemObjectSet.Count = 0 Then
    Wscript.Echo "W3SVC service is not installed on target computer."
Else
    For Each objSWbemObject In colSWbemObjectSet
        ' Perform task on World Wide Web Publishing service.
    Next
End If
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMOBJECTSET CLSID<br/>                                                        |
| IID<br/>                      | \_ISWBEMOBJECTSET IID<br/>                                                         |



 

 




