---
title: Messaggio di ICM_DRAW_END (VFW. h)
description: Il \_ messaggio di \_ fine disegno ICM notifica a un driver di rendering di decomprimere l'immagine corrente sullo schermo e di rilasciare le risorse allocate per la decompressione e il disegno. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro ICDrawEnd.
ms.assetid: 03910752-6122-4a5a-84ff-2cecf66cf439
keywords:
- ICM_DRAW_END messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DRAW_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e420ac37791bc6c5aa7f660d71005be65fc87fff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741962"
---
# <a name="icm_draw_end-message"></a>\_Messaggio finale di disegnato ICM \_

Il messaggio di **\_ \_ fine disegno ICM** notifica a un driver di rendering di decomprimere l'immagine corrente sullo schermo e di rilasciare le risorse allocate per la decompressione e il disegno. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICDrawEnd**](/windows/desktop/api/Vfw/nf-vfw-icdrawend) .


```C++
ICM_DRAW_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valore restituito

Restituisce ICERR \_ OK se ha esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

I messaggi di [**\_ \_ inizio**](icm-draw-begin.md) e **di \_ \_ fine progetto** ICM non nidificano. Se il driver riceve **l' \_ \_ inizio dell'estrazione ICM** prima che la decompressione venga arrestata con la **\_ \_ fine del progetto ICM**, dovrebbe riavviare la decompressione con nuovi parametri.

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

 

 





