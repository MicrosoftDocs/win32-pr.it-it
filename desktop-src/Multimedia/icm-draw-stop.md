---
title: ICM_DRAW_STOP messaggio (Vfw.h)
description: Il ICM DRAW STOP notifica a un driver di rendering di arrestare il clock interno per \_ \_ l'intervallo di disegno dei frame. È possibile inviare questo messaggio in modo esplicito o tramite la macro ICDrawStop.
ms.assetid: 9ffda595-e3d6-48f0-9487-69f7e95979c2
keywords:
- ICM_DRAW_STOP messaggio Windows Multimediali
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
ms.openlocfilehash: 41bdb8fbc9a0cddf470733fa35b2f25dc62675175cbb40c427d0b160074c5409
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038791"
---
# <a name="icm_draw_stop-message"></a>\_ICM Messaggio DRAW \_ STOP

Il **ICM \_ DRAW \_ STOP** notifica a un driver di rendering di arrestare il clock interno per l'intervallo di disegno dei frame. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**ICDrawStop.**](/windows/desktop/api/Vfw/nf-vfw-icdrawstop)


```C++
ICM_DRAW_STOP 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo messaggio viene utilizzato dall'hardware che esegue la decompressione asincrona, l'intervallo e il disegno.

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

 

 





