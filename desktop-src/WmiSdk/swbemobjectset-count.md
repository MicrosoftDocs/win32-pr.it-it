---
description: Usare la proprietà Count dell'oggetto SWbemObjectSet per determinare il numero di elementi presenti in una raccolta SWbemObjectSet. Questa proprietà è di sola lettura.
ms.assetid: ad3d1265-a11e-4962-b1f3-60092d2f79ef
ms.tgt_platform: multiple
title: Proprietà SWbemObjectSet.Count (Wbemdisp.h)
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
ms.openlocfilehash: c1305cc0119f002f8ac3229664227d5c21bea9d865eedb0a31fcb7eb77250424
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857231"
---
# <a name="swbemobjectsetcount-property"></a>Proprietà SWbemObjectSet.Count

Usare la **proprietà Count** dell'oggetto [**SWbemObjectSet**](swbemobjectset.md) per determinare il numero di elementi presenti in una **raccolta SWbemObjectSet.** Questa proprietà è di sola lettura.

Per una spiegazione di questa sintassi, vedere [Convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
SWbemObjectSet.Count As Integer
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

Un aspetto da prestare attenzione quando si usa Count è che WMI non mantiene un conteggio in esecuzione del numero di elementi in una raccolta. Se si richiede Count per una raccolta, WMI non può rispondere immediatamente con un numero. deve invece contare letteralmente gli elementi, enumerando l'intera raccolta. Per una raccolta con relativamente pochi elementi, ad esempio servizi, questa enumerazione richiede probabilmente meno di un secondo. Il conteggio del numero di eventi in una raccolta di log eventi può tuttavia richiedere molto più tempo.

Si supponga quindi di voler visualizzare i valori delle proprietà per ogni evento nella raccolta. In tal caso, WMI dovrà enumerare l'intera raccolta una seconda volta.

> [!Note]  
> Se si tenta di ottenere questa proprietà da un [**oggetto SWbemObjectSet**](swbemobjectset.md) restituito da un metodo in cui i flag specificati includono il flag wbemFlagForwardOnly, si riceverà un errore wbemErrFailed.

 

## <a name="examples"></a>Esempio

Per la maggior parte, l'unica operazione che si può eseguire con un oggetto SWbemObjectSet è enumerare tutti gli oggetti contenuti nella raccolta stessa. Conteggio, tuttavia, che può essere utile nello scripting di amministrazione del sistema. Come suggerisce il nome, Count indica il numero di elementi nella raccolta. Ad esempio, questo script recupera una raccolta di tutti i servizi installati in un computer e quindi restituisce il numero totale di servizi trovati:


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
Wscript.Echo "Services installed on target computer: " & colSWbemObjectSet.Count

```



Ciò che rende Utile Count è che può indicare se un'istanza specifica è disponibile in un computer. Ad esempio, questo script recupera una raccolta di tutti i servizi in un computer con il nome W3SVC. Se count è 0 (ed è valido per le raccolte senza istanze), significa che il servizio W3SVC non è installato nel computer.


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
| Intestazione<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectSet<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemObjectSet<br/>                                                         |



 

 




