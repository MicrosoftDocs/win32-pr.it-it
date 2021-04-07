---
title: Messaggio di ICM_COMPRESS_BEGIN (VFW. h)
description: Il \_ \_ messaggio di inizio della compressione ICM notifica a un driver di compressione video di preparare la compressione dei dati. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro ICCompressBegin.
ms.assetid: dd1d3a66-c625-4f55-b65a-8545c1c16301
keywords:
- ICM_COMPRESS_BEGIN messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_COMPRESS_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e358aa3ab589af0be1e4e490c141ed41baeb5874
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048744"
---
# <a name="icm_compress_begin-message"></a>\_Messaggio di \_ inizio compressione MCI

Il messaggio di **\_ \_ inizio** della compressione ICM notifica a un driver di compressione video di preparare la compressione dei dati. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICCompressBegin**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) .


```C++
ICM_COMPRESS_BEGIN 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*
</dt> <dd>

Puntatore a una struttura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) contenente il formato di input.

</dd> <dt>

<span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*
</dt> <dd>

Puntatore a una struttura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) contenente il formato di output.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce ICERR \_ OK se il driver supporta la compressione specificata o ICERR \_ BADFORMAT se il formato di input o di output non è supportato.

## <a name="remarks"></a>Commenti

Il driver deve allocare e inizializzare qualsiasi tabella o memoria necessaria per comprimere i formati di dati quando riceve il messaggio di [**\_ compressione ICM**](icm-compress.md) .

VCM Salva le impostazioni del messaggio di **inizio della \_ compressione \_ ICM** più recente. I messaggi di fine compressione **MCI \_ \_ Begin** e [**ICM \_ compress \_**](icm-compress-end.md) non vengono annidati. Se il driver riceve **l' \_ \_ inizio** della compressione ICM prima che la compressione venga arrestata con la **\_ \_ fine** della compressione MCI, dovrebbe riavviare la compressione con i nuovi parametri.

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

 

