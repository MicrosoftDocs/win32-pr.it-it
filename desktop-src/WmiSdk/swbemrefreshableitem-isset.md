---
description: La proprietà SWbemRefreshableItem.IsSet è un valore booleano che indica se l'oggetto SWbemRefreshableItem rappresenta un singolo oggetto o un set di oggetti. L'oggetto SWbemRefreshableItem rappresenta un singolo oggetto o un set di oggetti.
ms.assetid: 4be5d27c-9020-4150-84ce-f9efc55be947
ms.tgt_platform: multiple
title: Proprietà SWbemRefreshableItem.IsSet (Wbemdisp.h)
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
ms.openlocfilehash: 055c776c1beffe1550033d61b54256d7b2e983ca70ac13f1b9fc899920910d4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312920"
---
# <a name="swbemrefreshableitemisset-property"></a>Proprietà SWbemRefreshableItem.IsSet

La **proprietà SWbemRefreshableItem.IsSet** è un valore booleano che indica se l'oggetto [**SWbemRefreshableItem**](swbemrefreshableitem.md) rappresenta un singolo oggetto o un set di oggetti.

Per una spiegazione di questa sintassi, vedere [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
SWbemRefreshableItem.IsSet As Boolean
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

Se **SWbemRefreshableItem.IsSet** è **TRUE,** l'elemento rappresenta un [**oggetto SWbemObjectSet**](swbemobjectset.md) e la proprietà [**Object**](swbemrefreshableitem-object.md) sarà **NULL.** Se **FALSE,** l'elemento rappresenta un [**oggetto SWbemObject**](swbemobject.md) e la **proprietà Object** è **NULL.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemRefreshableItem<br/>                                                  |
| IID<br/>                      | IID \_ ISWbemRefreshableItem<br/>                                                   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SWbemRefreshableItem**](swbemrefreshableitem.md)
</dt> <dt>

[**SWbemRefreshableItem**](swbemrefresher.md)
</dt> </dl>

 

 




