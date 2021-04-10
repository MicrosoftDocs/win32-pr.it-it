---
title: Messaggio di ICM_DRAW_STOP_PLAY (VFW. h)
description: Il \_ messaggio di \_ interruzione riproduzione del progetto ICM \_ notifica a un driver di rendering una volta completata un'operazione di riproduzione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro ICDrawStopPlay.
ms.assetid: cfe2ee98-80d0-4554-bcbd-9873769da674
keywords:
- ICM_DRAW_STOP_PLAY messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DRAW_STOP_PLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea3964b623c93d452ab7bf9a32c6b9d9b1573fec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121686"
---
# <a name="icm_draw_stop_play-message"></a>\_Messaggio di \_ interruzione \_ riproduzione del progetto ICM

Il messaggio di **\_ \_ interruzione \_ riproduzione del progetto ICM** notifica a un driver di rendering una volta completata un'operazione di riproduzione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICDrawStopPlay**](/windows/desktop/api/Vfw/nf-vfw-icdrawstopplay) .


```C++
ICM_DRAW_STOP_PLAY 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="remarks"></a>Commenti

Utilizzare questo messaggio al termine dell'operazione di riproduzione. Per terminare la temporizzazione, utilizzare il messaggio di [**\_ \_ interruzione di progetto ICM**](icm-draw-stop.md) .

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

 

 





