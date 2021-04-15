---
title: Messaggio di ICM_COMPRESS_END (VFW. h)
description: Il \_ \_ messaggio di fine compressione ICM notifica a un driver di compressione video di terminare la compressione e liberare le risorse allocate per la compressione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro ICCompressEnd.
ms.assetid: 5d4b5962-c4f0-44eb-a3a9-36026f167a5a
keywords:
- ICM_COMPRESS_END messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_COMPRESS_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 320cc99ed4223b7919b85d2b39e15d4d9b76aa90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476007"
---
# <a name="icm_compress_end-message"></a>\_ \_ Messaggio finale compresso ICM

Il messaggio di **\_ \_ fine compressione ICM** notifica a un driver di compressione video di terminare la compressione e liberare le risorse allocate per la compressione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICCompressEnd**](/windows/desktop/api/Vfw/nf-vfw-iccompressend) .


```C++
ICM_COMPRESS_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valore restituito

Restituisce ICERR \_ OK se ha esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

VCM Salva le impostazioni del messaggio di [**inizio della \_ compressione \_ ICM**](icm-compress-begin.md) più recente. **ICM \_ COMPRESS \_ Begin** e **MCI \_ compress \_ end** non nidificano. Se il driver riceve **l' \_ \_ inizio** della compressione ICM prima che la compressione venga arrestata con la **\_ \_ fine** della compressione MCI, dovrebbe riavviare la compressione con i nuovi parametri.

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

 

 





