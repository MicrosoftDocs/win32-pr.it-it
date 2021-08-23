---
description: La proprietà Path \_ dell'oggetto SWbemLastError restituisce un oggetto SWbemObjectPath che rappresenta il percorso dell'oggetto della classe o dell'istanza corrente. Questa proprietà può essere passata come parametro ai metodi che richiedono un percorso di oggetto.
ms.assetid: 5472e463-54cb-4ba2-8c00-08b70013e38d
ms.tgt_platform: multiple
title: SWbemLastError.Path_ proprietà (Wbemdisp.h)
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
ms.openlocfilehash: 5503d11d5c73f2bf955b25da9b5dbccbc18d41b9bc9b84bc3235993562938b5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612201"
---
# <a name="swbemlasterrorpath_-property"></a>Proprietà SWbemLastError.Path \_

La **\_ proprietà Path** dell'oggetto [**SWbemLastError**](swbemlasterror.md) restituisce un [**oggetto SWbemObjectPath**](swbemobjectpath.md) che rappresenta il percorso dell'oggetto della classe o dell'istanza corrente. Questa proprietà può essere passata come parametro ai metodi che richiedono un percorso di oggetto.

Per una spiegazione di questa sintassi, vedere [Convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
SWbemLastError.Path_ As Object
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

È possibile [**modificare**](swbemobjectpath-class.md) solo la proprietà Class dell'istanza [**di SWbemObjectPath**](swbemobjectpath.md) restituita. Se si tenta di modificare qualsiasi altra proprietà o di chiamare i metodi [**SetAsClass**](swbemobjectpath-setasclass.md) o [**SetAsSingleton,**](swbemobjectpath-setassingleton.md) viene visualizzato un errore **wbemErrReadOnly**.

Per questo scopo, non è possibile modificare [**l'oggetto SWbemNamedValueSet**](swbemnamedvalueset.md) che è il valore della [**proprietà Keys**](swbemobjectpath-keys.md) dell'istanza [**di SWbemObjectPath**](swbemobjectpath.md) restituita. Se si tenta di chiamare i [**metodi Add**](swbemnamedvalueset-add.md), [**Remove**](swbemnamedvalueset-remove.md)o [**DeleteAll**](swbemnamedvalueset-deleteall.md) su questo valore, viene visualizzato un errore **wbemErrReadOnly.** Inoltre, non è possibile modificare [**SWbemNamedValue ottenuto**](swbemnamedvalue.md) da questa raccolta. I tentativi di modificare [**la proprietà Value**](swbemnamedvalue-value.md) restituiscono lo stesso codice di errore.

Tuttavia, se si chiama [**\_ SWbemObject.Clone**](swbemobject-clone-.md) per creare una copia, la [**proprietà Path \_**](swbemobject-path-.md) della copia è completamente modificabile.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemLastError<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemLastError<br/>                                                         |



 

 




