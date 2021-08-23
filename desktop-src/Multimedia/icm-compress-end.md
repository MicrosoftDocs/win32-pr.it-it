---
title: ICM_COMPRESS_END messaggio (Vfw.h)
description: Il ICM COMPRESS END invia una notifica a un driver di compressione video per terminare la compressione e \_ liberare le risorse allocate per la \_ compressione. È possibile inviare questo messaggio in modo esplicito o tramite la macro ICCompressEnd.
ms.assetid: 5d4b5962-c4f0-44eb-a3a9-36026f167a5a
keywords:
- ICM_COMPRESS_END messaggio Windows Multimediali
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
ms.openlocfilehash: 9c320190da37d286db1c20329a849ea09ac6d915087e9d3bdbb2333d31cec3e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785041"
---
# <a name="icm_compress_end-message"></a>\_ICM MESSAGGIO COMPRESS \_ END

Il **ICM \_ COMPRESS \_ END** invia una notifica a un driver di compressione video per terminare la compressione e liberare le risorse allocate per la compressione. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**ICCompressEnd.**](/windows/desktop/api/Vfw/nf-vfw-iccompressend)


```C++
ICM_COMPRESS_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valore restituito

Restituisce ICERR \_ OK in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

VCM salva le impostazioni del messaggio COMPRESS [**\_ \_ BEGIN ICM più**](icm-compress-begin.md) recente. **ICM \_ COMPRESS \_ BEGIN** e **ICM COMPRESS \_ \_ END** non vengono annidato. Se il driver riceve ICM **\_ COMPRESS \_ BEGIN** prima che la compressione venga arrestata ICM **COMPRESS \_ \_ END**, deve riavviare la compressione con nuovi parametri.

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

 

 





