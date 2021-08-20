---
title: ICM_COMPRESS_FRAMES_INFO messaggio (Vfw.h)
description: Il ICM COMPRESS FRAMES INFO notifica a un driver di compressione di \_ impostare i parametri per la compressione in \_ \_ sospeso.
ms.assetid: d2f6f3b7-dff6-4fef-a642-cb77b00119af
keywords:
- ICM_COMPRESS_FRAMES_INFO messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- ICM_COMPRESS_FRAMES_INFO
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2382a930b0ce12e212adf78ddaf3c7e1b3300e47597b4671d0eae223cb536f73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140912"
---
# <a name="icm_compress_frames_info-message"></a>\_ICM MESSAGGIO \_ COMPRIMI \_ FRAME INFO

Il **ICM COMPRESS FRAMES \_ \_ \_ INFO** notifica a un driver di compressione di impostare i parametri per la compressione in sospeso.


```C++
ICM_COMPRESS_FRAMES_INFO 
wParam = (DWORD) (LPVOID) &icf; 
lParam = sizeof(ICCOMPRESSFRAMES); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="icf"></span><span id="ICF"></span>*Icf*
</dt> <dd>

Puntatore a [**una struttura ICCOMPRESSFRAMES.**](/windows/desktop/api/Vfw/ns-vfw-iccompressframes) I **membri GetData** **e PutData** di questa struttura non vengono usati con questo messaggio.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Dimensioni, in byte, di [**ICCOMPRESSFRAMES**](/windows/desktop/api/Vfw/ns-vfw-iccompressframes).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce ICERR \_ OK in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

Un modello di compressione può usare questo messaggio per determinare la quantità di spazio da allocare per ogni frame durante la compressione.

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

 

 





