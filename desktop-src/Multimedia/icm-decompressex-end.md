---
title: Messaggio di ICM_DECOMPRESSEX_END (VFW. h)
description: Il \_ \_ messaggio di fine DECOMPRESSEX ICM notifica a un driver di decompressione video di terminare la decompressione e liberare le risorse allocate per la decompressione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro ICDecompressExEnd.
ms.assetid: 7ed63a4e-bb17-43a3-b593-25c4a51be942
keywords:
- ICM_DECOMPRESSEX_END messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7e96f6a069e9ed2c9c52dc2f07f1ab4c5210ecd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518640"
---
# <a name="icm_decompressex_end-message"></a>\_ \_ Messaggio finale DECOMPRESSEX ICM

Il messaggio di **\_ \_ fine DECOMPRESSEX ICM** notifica a un driver di decompressione video di terminare la decompressione e liberare le risorse allocate per la decompressione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICDecompressExEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexend) .


```C++
ICM_DECOMPRESSEX_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valore restituito

Restituisce ICERR \_ OK se ha esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

Il driver libera tutte le risorse allocate per il messaggio di [**\_ \_ inizio DECOMPRESSEX ICM**](icm-decompressex-begin.md) .

[**ICM \_ DECOMPRESSEX \_ Begin**](icm-decompressex-begin.md) e **ICM \_ DECOMPRESSEX \_ end** non nidificano. Se il driver riceve **la \_ DECOMPRESSEX MCI \_ iniziare** prima che la decompressione venga interrotta con la **\_ \_ fine di DECOMPRESSEX ICM**, dovrebbe riavviare la decompressione con nuovi parametri.

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

 

 





