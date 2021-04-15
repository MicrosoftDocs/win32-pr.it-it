---
title: Messaggio di ICM_DRAW_START (VFW. h)
description: Il \_ \_ messaggio di avvio del disegno ICM notifica a un driver di rendering di avviare il clock interno per la tempistica di disegno dei frame. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro ICDrawStart.
ms.assetid: d49e0d97-5a29-46f7-82d7-e3d4b4f7666f
keywords:
- ICM_DRAW_START messaggi multimediali di Windows
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
ms.openlocfilehash: 538659eb9878be819ee6ec1506403fcce314eb0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400536"
---
# <a name="icm_draw_start-message"></a>Messaggio di avvio del \_ progetto ICM \_

Il messaggio di **\_ \_ avvio del disegno ICM** notifica a un driver di rendering di avviare il clock interno per la tempistica di disegno dei frame. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICDrawStart**](/windows/desktop/api/Vfw/nf-vfw-icdrawstart) .


```C++
ICM_DRAW_START 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="remarks"></a>Commenti

Questo messaggio viene usato dall'hardware che esegue la decompressione, la temporizzazione e il disegno asincroni.

Quando il driver riceve questo messaggio, deve iniziare a eseguire il rendering dei dati alla velocità specificata con il messaggio di [**\_ \_ inizio del progetto ICM**](icm-draw-begin.md) .

I messaggi di **\_ \_ avvio** e [**di \_ \_ arresto del progetto**](icm-draw-stop.md) ICM non vengono annidati. Se il driver riceve **l' \_ \_ avvio del progetto ICM** prima che il rendering venga interrotto con l' **\_ \_ arresto del progetto ICM**, dovrebbe riavviare il rendering con nuovi parametri.

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

 

 





