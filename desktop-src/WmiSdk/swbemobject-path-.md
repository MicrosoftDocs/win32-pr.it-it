---
description: La \_ proprietà Path dell'oggetto SWbemObject restituisce un oggetto SWbemObjectPath che rappresenta il percorso dell'oggetto della classe o dell'istanza corrente. Questa proprietà può essere passata come parametro ai metodi che richiedono un percorso dell'oggetto.
ms.assetid: 85a55159-5f10-49b5-bc37-39d7b4dfccd7
ms.tgt_platform: multiple
title: Proprietà SWbemObject.Path_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Path_
- ISWbemObject.Path_
- ISWbemObject.get_Path_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 773f6f9bb04aa31290bc351550a45d849d74e06f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232206"
---
# <a name="swbemobjectpath_-property"></a>Proprietà SWbemObject. Path \_

La **proprietà \_ path** dell'oggetto [**SWbemObject**](swbemobject.md) restituisce un oggetto [**SWbemObjectPath**](swbemobjectpath.md) che rappresenta il percorso dell'oggetto della classe o dell'istanza corrente. Questa proprietà può essere passata come parametro ai metodi che richiedono un percorso dell'oggetto.

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
SWbemObject.Path_ As Object
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

È possibile modificare solo la proprietà [**Class**](swbemobjectpath-class.md) dell'istanza [**SWbemObjectPath**](swbemobjectpath.md) restituita. Se si tenta di modificare qualsiasi altra proprietà o si tenta di chiamare i metodi [**SetAsClass**](swbemobjectpath-setasclass.md) o [**SetAsSingleton**](swbemobjectpath-setassingleton.md), si otterrà un errore **wbemErrReadOnly** .

Per questo motivo, non è possibile modificare l'oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) che corrisponde al valore della proprietà [**Keys**](swbemobjectpath-keys.md) dell'istanza di [**SWbemObjectPath**](swbemobjectpath.md) restituita. Se si tenta di chiamare i metodi [**Add**](swbemnamedvalueset-add.md), [**Remove**](swbemnamedvalueset-remove.md)o [**DeleteAll**](swbemnamedvalueset-deleteall.md) su questo valore, si otterrà un errore wbemErrReadOnly. Non è inoltre possibile modificare i [**SWbemNamedValue**](swbemnamedvalue.md) ottenuti da questa raccolta. I tentativi di modificare la proprietà **value** restituiscono lo stesso codice di errore.

Tuttavia, se si chiama [**SWbemObject. Clone \_**](swbemobject-clone-.md) per creare una copia, la proprietà [**SWbemObjectPath. Path**](swbemobjectpath-path.md) della copia è completamente modificabile.

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente, tratto da un [elenco di tutte le classi WMI cimV2](https://Gallery.TechNet.Microsoft.Com/5649568b-074e-4f5d-be52-e8b7d8fe4517) nella raccolta TechNet, viene utilizzata la \_ proprietà Path per elencare tutte le classi cimV2 di WMI.


```VB
strComputer = "." 
Set objWMIService=GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & _  
    strComputer & "\root\cimv2") 
  
For Each objclass in objWMIService.SubclassesOf() 
    Wscript.Echo objClass.Path_.Class 
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



 

 




