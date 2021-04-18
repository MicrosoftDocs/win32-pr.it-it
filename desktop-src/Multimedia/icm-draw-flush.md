---
title: Messaggio di ICM_DRAW_FLUSH (VFW. h)
description: Il \_ messaggio di \_ SCARICAmento ICM invia una notifica a un driver di rendering per eseguire il rendering del contenuto di tutti i buffer di immagine in attesa di essere disegnati. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro ICDrawFlush.
ms.assetid: c29ed751-c773-4476-98fe-6edef3ff0cf4
keywords:
- ICM_DRAW_FLUSH messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DRAW_FLUSH
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38ec42c51222313f7d3599c3b4f264dbd21a9434
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301826"
---
# <a name="icm_draw_flush-message"></a>\_Messaggio di \_ scaricamento del progetto ICM

Il messaggio di **\_ \_ scaricamento ICM** invia una notifica a un driver di rendering per eseguire il rendering del contenuto di tutti i buffer di immagine in attesa di essere disegnati. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICDrawFlush**](/windows/desktop/api/Vfw/nf-vfw-icdrawflush) .


```C++
ICM_DRAW_FLUSH 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valore restituito

Restituisce ICERR \_ OK se ha esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

Questo messaggio viene usato solo dall'hardware che esegue la decompressione, la temporizzazione e il disegno asincroni.

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

 

 





