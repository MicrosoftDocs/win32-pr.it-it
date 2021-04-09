---
description: Il metodo SWbemRefresher. Remove rimuove l'oggetto SWbemRefreshableItem con l'indice specificato dall'aggiornamento.
ms.assetid: db5ac740-e2b3-4667-b511-d750cb092e0f
ms.tgt_platform: multiple
title: Metodo SWbemRefresher. Remove (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.Remove
- ISWbemRefresher.Remove
- ISWbemRefresher.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9504b81ce83a91695765e75e74de374437c188d4
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103968932"
---
# <a name="swbemrefresherremove-method"></a>Metodo SWbemRefresher. Remove

Il metodo **SWbemRefresher. Remove** rimuove l'oggetto [**SWbemRefreshableItem**](swbemrefreshableitem.md) con l'indice specificato dall'aggiornamento. L'oggetto **SWbemRefreshableItem** può rappresentare un singolo oggetto o un set di oggetti.

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
objRefresher = .Remove( _
  ByVal LIndex, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedvalueSet ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*LIndex* 
</dt> <dd>

Indice dell'elemento nell'oggetto [**SWbemRefresher**](swbemrefresher.md) .

</dd> <dt>

*iFlags* \[ opzionale\]
</dt> <dd>

I flag devono essere impostati T0 (zero).

</dd> <dt>

*objWbemNamedvalueSet* \[ opzionale\]
</dt> <dd>

Null.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

**Codici di errore** Se l'aggiornamento non ha alcun elemento con l'indice specificato, viene generato **wbemErrNotFound** .

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

[**SWbemRefresher**](swbemrefresher.md)
</dt> </dl>

 

 




