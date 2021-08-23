---
title: ICM_DRAW_SETTIME messaggio (Vfw.h)
description: Il ICM \_ DRAW \_ SETTIME fornisce informazioni di sincronizzazione a un driver di rendering che gestisce l'intervallo dei frame di disegno.
ms.assetid: 211e8ecc-ef36-4598-aa1d-cb0a06e64f14
keywords:
- ICM_DRAW_SETTIME messaggio Windows Multimediali
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
ms.openlocfilehash: 62c291b736b0138386c235703c29fffdae470d011f55284e8aaac4c4cfd604a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691141"
---
# <a name="icm_draw_settime-message"></a>\_ICM Messaggio DRAW \_ SETTIME

**L ICM \_ DRAW \_ SETTIME fornisce** informazioni di sincronizzazione a un driver di rendering che gestisce l'intervallo di disegno dei frame. Le informazioni di sincronizzazione sono il numero di esempio del frame da disegnare. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**ICDrawSetTime.**](/windows/desktop/api/Vfw/nf-vfw-icdrawsettime)


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

Restituisce ICERR \_ OK in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

In genere, il driver confronta il valore specificato con il numero di frame associato all'ora del clock interno e tenta di sincronizzare i due se la differenza è significativa.

Utilizzare questo messaggio quando l'hardware esegue la propria decompressione asincrona, temporizzazione e disegno e l'hardware si basa su un segnale di sincronizzazione esterno (l'hardware non viene usato come master di sincronizzazione).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Gestione compressione video](video-compression-manager.md)
</dt> <dt>

[Messaggi di compressione video](video-compression-messages.md)
</dt> </dl>

 

 





