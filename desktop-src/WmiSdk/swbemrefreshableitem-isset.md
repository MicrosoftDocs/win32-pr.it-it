---
description: La proprietà SWbemRefreshableItem. IsSet è un valore booleano che indica se l'oggetto SWbemRefreshableItem rappresenta un singolo oggetto o un set di oggetti. L'oggetto SWbemRefreshableItem rappresenta un singolo oggetto o un set di oggetti.
ms.assetid: 4be5d27c-9020-4150-84ce-f9efc55be947
ms.tgt_platform: multiple
title: Proprietà SWbemRefreshableItem. IsSet (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefreshableItem.IsSet
- ISWbemRefreshableItem.IsSet
- ISWbemRefreshableItem.get_IsSet
- ISWbemRefreshableItem.put_IsSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 71fb5f84ec7ad35f1d9beab32cb74db5b7591057
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320558"
---
# <a name="swbemrefreshableitemisset-property"></a>Proprietà SWbemRefreshableItem. IsSet

La proprietà **SWbemRefreshableItem. IsSet** è un valore booleano che indica se l'oggetto [**SWbemRefreshableItem**](swbemrefreshableitem.md) rappresenta un singolo oggetto o un set di oggetti.

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
SWbemRefreshableItem.IsSet As Boolean
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

Se **SWbemRefreshableItem. IsSet** è **true**, l'elemento rappresenta un oggetto [**SWbemObjectSet**](swbemobjectset.md) e la proprietà dell' [**oggetto**](swbemrefreshableitem-object.md) sarà **null**. Se **false**, l'elemento rappresenta un oggetto [**SWbemObject**](swbemobject.md) e la proprietà dell' **oggetto** è **null**.

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

[**SWbemRefreshableItem**](swbemrefreshableitem.md)
</dt> <dt>

[**SWbemRefreshableItem**](swbemrefresher.md)
</dt> </dl>

 

 




