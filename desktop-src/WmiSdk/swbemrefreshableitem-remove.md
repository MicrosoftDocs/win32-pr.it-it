---
description: Il metodo SWbemRefreshableItem. Remove rimuove l'oggetto SWbemRefreshableItem dall'oggetto SWbemRefresher padre. Oggetto SWbemRefreshableItem dall'oggetto SWbemRefresher padre.
ms.assetid: 8d3f5e22-c343-4191-a20a-6bca2ec9b01a
ms.tgt_platform: multiple
title: Metodo SWbemRefreshableItem. Remove (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefreshableItem.Remove
- ISWbemRefreshableItem.Remove
- ISWbemRefreshableItem.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 028bff202108481ce498be02c6014141313f27cc
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320585"
---
# <a name="swbemrefreshableitemremove-method"></a>Metodo SWbemRefreshableItem. Remove

Il metodo **SWbemRefreshableItem. Remove** rimuove l'oggetto [**SWbemRefreshableItem**](swbemrefreshableitem.md) dall'oggetto [**SWbemRefresher**](swbemrefresher.md) padre.

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
SWbemRefreshableItem.Remove( _
  [ ByVal lFlags ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*è* \[ in, facoltativo\]
</dt> <dd>

Questo parametro deve essere impostato su 0 (zero).

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
| CLSID<br/>                    | \_SWBEMREFRESHABLEITEM CLSID<br/>                                                  |
| IID<br/>                      | \_ISWBEMREFRESHABLEITEM IID<br/>                                                   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SWbemRefreshableItem**](swbemrefreshableitem.md)
</dt> <dt>

[**SWbemRefresher**](swbemrefresher.md)
</dt> </dl>

 

 




