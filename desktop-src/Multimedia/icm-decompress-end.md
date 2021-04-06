---
title: Messaggio di ICM_DECOMPRESS_END (VFW. h)
description: Il \_ \_ messaggio di fine decompressione ICM notifica a un driver di decompressione video di terminare la decompressione e liberare le risorse allocate per la decompressione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro ICDecompressEnd.
ms.assetid: 16ce2424-9606-455f-afbd-84326457538e
keywords:
- ICM_DECOMPRESS_END messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e25155755b6bfbb893905e6facad890dbf98f175
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742970"
---
# <a name="icm_decompress_end-message"></a>\_Messaggio finale di decompressione ICM \_

Il messaggio di **\_ \_ fine** decompressione ICM notifica a un driver di decompressione video di terminare la decompressione e liberare le risorse allocate per la decompressione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICDecompressEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressend) .


```C++
ICM_DECOMPRESS_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valore restituito

Restituisce ICERR \_ OK se ha esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

Il driver deve liberare tutte le risorse allocate per il messaggio di [**\_ \_ inizio della decompressione ICM**](icm-decompress-begin.md) .

[**ICM \_ Decomprimi \_ Begin**](icm-decompress-begin.md) e **MCI \_ Decompress \_ end** non nidificano. Se il driver riceve la decompressione **MCI \_ \_ inizia** prima che la decompressione venga interrotta con la **\_ \_ terminazione MCI decomprimere**, deve riavviare la decompressione con nuovi parametri.

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

 

 





