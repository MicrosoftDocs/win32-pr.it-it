---
description: Il metodo SWbemRefresher. DeleteAll rimuove tutti gli elementi dalla raccolta nell'oggetto SWbemRefresher. Oggetto SWbemRefresher.
ms.assetid: c6e462d3-52b3-40c0-9a9c-fa268415a5f0
ms.tgt_platform: multiple
title: Metodo SWbemRefresher. DeleteAll (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.DeleteAll
- ISWbemRefresher.DeleteAll
- ISWbemRefresher.DeleteAll
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: ddeb1c5fc8e7fb1f9c5682a2da0d9a1d6f53ba5d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320584"
---
# <a name="swbemrefresherdeleteall-method"></a>SWbemRefresher. DeleteAll, metodo

Il metodo **SWbemRefresher. DeleteAll** rimuove tutti gli elementi dalla raccolta nell'oggetto [**SWbemRefresher**](swbemrefresher.md) .

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
SWbemRefresher.DeleteAll()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il valore di [**SWbemRefreshableItem**](swbemrefreshableitem.md) corrispondente per ogni elemento rimosso ha la proprietà di [**aggiornamento**](swbemrefreshableitem-refresher.md) impostata su **null**, a indicare che non è più disponibile un aggiornamento padre.

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

 

 




