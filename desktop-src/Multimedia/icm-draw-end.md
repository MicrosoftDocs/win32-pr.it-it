---
title: ICM_DRAW_END messaggio (Vfw.h)
description: Il ICM DRAW END notifica a un driver di rendering di decomprimere l'immagine corrente sullo schermo e di rilasciare le risorse allocate per \_ \_ la decompressione e il disegno. È possibile inviare questo messaggio in modo esplicito o tramite la macro ICDrawEnd.
ms.assetid: 03910752-6122-4a5a-84ff-2cecf66cf439
keywords:
- ICM_DRAW_END messaggio Windows Multimediali
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
ms.openlocfilehash: daac4fed37908596bab68b37bf5ae20c9c4652a6550288d52b892e640be612cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117987445"
---
# <a name="icm_draw_end-message"></a>\_ICM Messaggio DRAW \_ END

Il **ICM \_ DRAW \_ END** notifica a un driver di rendering di decomprimere l'immagine corrente sullo schermo e di rilasciare le risorse allocate per la decompressione e il disegno. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**ICDrawEnd.**](/windows/desktop/api/Vfw/nf-vfw-icdrawend)


```C++
ICM_DRAW_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valore restituito

Restituisce ICERR \_ OK in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

I [**ICM \_ DRAW \_ BEGIN**](icm-draw-begin.md) **e ICM \_ DRAW \_ END** non vengono annidato. Se il driver riceve **ICM \_ DRAW \_ BEGIN** prima che la decompressione venga arrestata ICM **DRAW \_ \_ END,** deve riavviare la decompressione con nuovi parametri.

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

 

 





