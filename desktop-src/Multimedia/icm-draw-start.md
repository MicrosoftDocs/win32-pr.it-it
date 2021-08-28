---
title: ICM_DRAW_START messaggio (Vfw.h)
description: Il ICM DRAW START notifica a un driver di rendering di avviare il clock interno per \_ \_ l'intervallo dei fotogrammi di disegno. È possibile inviare questo messaggio in modo esplicito o tramite la macro ICDrawStart.
ms.assetid: d49e0d97-5a29-46f7-82d7-e3d4b4f7666f
keywords:
- ICM_DRAW_START messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- ICM_DRAW_START
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 720d8c2f919d2b00955892a42ba8fca95b2b426c3cbb396aa4ac71a5cf912307
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690951"
---
# <a name="icm_draw_start-message"></a>\_ICM Messaggio DRAW \_ START

Il **ICM \_ DRAW \_ START** notifica a un driver di rendering di avviare il clock interno per l'intervallo di disegno dei fotogrammi. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**ICDrawStart.**](/windows/desktop/api/Vfw/nf-vfw-icdrawstart)


```C++
ICM_DRAW_START 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo messaggio viene usato dall'hardware che esegue la decompressione asincrona, l'intervallo e il disegno.

Quando il driver riceve questo messaggio, deve iniziare a eseguire il rendering dei dati alla velocità specificata con il ICM [**\_ DRAW \_ BEGIN.**](icm-draw-begin.md)

I **ICM \_ DRAW \_ START** [**e ICM \_ DRAW \_ STOP**](icm-draw-stop.md) non vengono annidato. Se il driver riceve ICM **\_ DRAW \_ START** prima che il rendering venga arrestato ICM **DRAW \_ \_ STOP,** il rendering deve essere riavviato con nuovi parametri.

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

 

 





