---
description: La \_ proprietà Path dell'oggetto SWbemLastError restituisce un oggetto SWbemObjectPath che rappresenta il percorso dell'oggetto della classe o dell'istanza corrente. Questa proprietà può essere passata come parametro ai metodi che richiedono un percorso dell'oggetto.
ms.assetid: 5472e463-54cb-4ba2-8c00-08b70013e38d
ms.tgt_platform: multiple
title: Proprietà SWbemLastError.Path_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.Path_
- ISWbemLastError.Path_
- ISWbemLastError.get_Path_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c979fd76ffb4ee97f62362d53fac4151de17bae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050230"
---
# <a name="swbemlasterrorpath_-property"></a>Proprietà SWbemLastError. Path \_

La **proprietà \_ path** dell'oggetto [**SWbemLastError**](swbemlasterror.md) restituisce un oggetto [**SWbemObjectPath**](swbemobjectpath.md) che rappresenta il percorso dell'oggetto della classe o dell'istanza corrente. Questa proprietà può essere passata come parametro ai metodi che richiedono un percorso dell'oggetto.

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
SWbemLastError.Path_ As Object
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

È possibile modificare solo la proprietà [**Class**](swbemobjectpath-class.md) dell'istanza [**SWbemObjectPath**](swbemobjectpath.md) restituita. Se si tenta di modificare qualsiasi altra proprietà o si tenta di chiamare i metodi [**SetAsClass**](swbemobjectpath-setasclass.md) o [**SetAsSingleton**](swbemobjectpath-setassingleton.md) , si ottiene un errore di **wbemErrReadOnly**.

Per questo motivo, non è possibile modificare l'oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) che corrisponde al valore della proprietà [**Keys**](swbemobjectpath-keys.md) dell'istanza di [**SWbemObjectPath**](swbemobjectpath.md) restituita. Se si tenta di chiamare i metodi [**Add**](swbemnamedvalueset-add.md), [**Remove**](swbemnamedvalueset-remove.md)o [**DeleteAll**](swbemnamedvalueset-deleteall.md) su questo valore, si ottiene un errore **wbemErrReadOnly** . Non è inoltre possibile modificare i [**SWbemNamedValue**](swbemnamedvalue.md) ottenuti da questa raccolta. I tentativi di modificare la proprietà [**value**](swbemnamedvalue-value.md) restituiscono lo stesso codice di errore.

Tuttavia, se si chiama [**SWbemObject. Clone \_**](swbemobject-clone-.md) per creare una copia, la [**proprietà \_ path**](swbemobject-path-.md) della copia è completamente modificabile.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMLASTERROR CLSID<br/>                                                        |
| IID<br/>                      | \_ISWBEMLASTERROR IID<br/>                                                         |



 

 




