---
title: ICM_DECOMPRESS_END messaggio (Vfw.h)
description: Il ICM DECOMPRESS END notifica a un driver di decompressione video di terminare la decompressione e liberare le risorse allocate per \_ \_ la decompressione. È possibile inviare questo messaggio in modo esplicito o tramite la macro ICDecompressEnd.
ms.assetid: 16ce2424-9606-455f-afbd-84326457538e
keywords:
- ICM_DECOMPRESS_END messaggio Windows Multimedia
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
ms.openlocfilehash: a0c877afac3db0e4cf4d7c476ca3806d2acd15bdf72764549b2958490574a4f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691161"
---
# <a name="icm_decompress_end-message"></a>\_ICM DECOMPRESS \_ END message

Il **ICM \_ DECOMPRESS \_ END** notifica a un driver di decompressione video di terminare la decompressione e liberare le risorse allocate per la decompressione. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**ICDecompressEnd.**](/windows/desktop/api/Vfw/nf-vfw-icdecompressend)


```C++
ICM_DECOMPRESS_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valore restituito

Restituisce ICERR \_ OK in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

Il driver deve liberare tutte le risorse allocate per il [**ICM \_ DECOMPRESS \_ BEGIN.**](icm-decompress-begin.md)

[**ICM \_ DECOMPRESS \_ BEGIN**](icm-decompress-begin.md) e **ICM \_ DECOMPRESS \_ END** non vengono annidato. Se il driver riceve ICM **\_ DECOMPRESS \_ BEGIN** prima che la decompressione venga arrestata con **ICM \_ DECOMPRESS \_ END,** deve riavviare la decompressione con i nuovi parametri.

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

 

 





