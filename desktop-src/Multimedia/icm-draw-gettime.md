---
title: Messaggio di ICM_DRAW_GETTIME (VFW. h)
description: Il \_ messaggio ICM Draw \_ getTime richiede un driver di rendering che controlla la tempistica di disegno dei frame per restituire il valore corrente del clock interno. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro ICDrawGetTime.
ms.assetid: 77f0a322-c0bc-4cfe-a3d0-7633cf8d682a
keywords:
- ICM_DRAW_GETTIME messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DRAW_GETTIME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f756a76408d01cb72ee1762f14bb8a5eab19e475
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301827"
---
# <a name="icm_draw_gettime-message"></a>Messaggio di tempo di \_ richiamo ICM \_

Il messaggio **ICM \_ Draw \_ getTime** richiede un driver di rendering che controlla la tempistica di disegno dei frame per restituire il valore corrente del clock interno. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICDrawGetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawgettime) .


```C++
ICM_DRAW_GETTIME 
wParam = (DWORD_PTR) (LPVOID) lplTime; 
lParam = 0; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lplTime"></span><span id="lpltime"></span><span id="LPLTIME"></span>*lplTime*
</dt> <dd>

Indirizzo che contiene l'ora corrente. Il valore restituito deve essere specificato negli esempi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce ICERR \_ OK se ha esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

Questo messaggio è generalmente supportato da hardware che esegue la decompressione, la temporizzazione e il disegno asincroni. Il messaggio può essere inviato anche se l'hardware è usato come master di sincronizzazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Gestione compressione video](video-compression-manager.md)
</dt> <dt>

[Messaggi di compressione video](video-compression-messages.md)
</dt> </dl>

 

 





