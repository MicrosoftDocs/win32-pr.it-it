---
title: Messaggio di ICM_DRAW_SETTIME (VFW. h)
description: Il \_ \_ periodo di tempo di disegno MCI fornisce le informazioni di sincronizzazione a un driver di rendering che gestisce la tempistica di disegno dei frame.
ms.assetid: 211e8ecc-ef36-4598-aa1d-cb0a06e64f14
keywords:
- ICM_DRAW_SETTIME messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DRAW_SETTIME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ce1e37709477ba6080219e5225b3fde02dfed75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873633"
---
# <a name="icm_draw_settime-message"></a>\_Messaggio di tempo di rielaborazione ICM \_

Il **\_ periodo di \_ tempo** di disegno MCI fornisce le informazioni di sincronizzazione a un driver di rendering che gestisce la tempistica di disegno dei frame. Le informazioni di sincronizzazione sono il numero di esempio del fotogramma da creare. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICDrawSetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawsettime) .


```C++
ICM_DRAW_SETTIME 
wParam = (DWORD_PTR) lpTime; 
lParam = 0; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpTime"></span><span id="lptime"></span><span id="LPTIME"></span>*lpTime*
</dt> <dd>

Numero di esempio del frame di cui eseguire il rendering.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce ICERR \_ OK se ha esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

In genere, il driver confronta il valore specificato con il numero di frame associato all'ora del clock interno e tenta di sincronizzare i due se la differenza è significativa.

Utilizzare questo messaggio quando l'hardware esegue la decompressione asincrona, la temporizzazione e il disegno e l'hardware si basa su un segnale di sincronizzazione esterno (l'hardware non viene utilizzato come master di sincronizzazione).

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

 

 





