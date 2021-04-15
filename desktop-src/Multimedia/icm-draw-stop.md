---
title: Messaggio di ICM_DRAW_STOP (VFW. h)
description: Il messaggio di arresto del disegno ICM \_ \_ notifica a un driver di rendering di arrestare il clock interno per la tempistica di disegno dei frame. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro ICDrawStop.
ms.assetid: 9ffda595-e3d6-48f0-9487-69f7e95979c2
keywords:
- ICM_DRAW_STOP messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DRAW_STOP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3bde99dfcf483e67aa6a601de2718814cc22439
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476246"
---
# <a name="icm_draw_stop-message"></a>Messaggio di arresto del \_ progetto ICM \_

Il messaggio di **\_ \_ arresto** del disegno ICM notifica a un driver di rendering di arrestare il clock interno per la tempistica di disegno dei frame. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICDrawStop**](/windows/desktop/api/Vfw/nf-vfw-icdrawstop) .


```C++
ICM_DRAW_STOP 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="remarks"></a>Commenti

Questo messaggio viene usato dall'hardware che esegue la decompressione, la temporizzazione e il disegno asincroni.

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

 

 





