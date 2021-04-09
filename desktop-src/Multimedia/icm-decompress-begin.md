---
title: Messaggio di ICM_DECOMPRESS_BEGIN (VFW. h)
description: Il \_ \_ messaggio di inizio della DEcompressione ICM invia una notifica a un driver di decompressione video per preparare la decompressione dei dati. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro ICDecompressBegin.
ms.assetid: 24cd5220-d473-4968-8678-b00670eecf8f
keywords:
- ICM_DECOMPRESS_BEGIN messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59b8f55ebb5543c73e0d7a9c9ee800fabfc483d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120942"
---
# <a name="icm_decompress_begin-message"></a>\_Messaggio di inizio decompressione ICM \_

Il messaggio di **\_ \_ inizio** della decompressione ICM invia una notifica a un driver di decompressione video per preparare la decompressione dei dati. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICDecompressBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressbegin) .


```C++
ICM_DECOMPRESS_BEGIN 
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

Restituisce ICERR \_ OK se la decompressione specificata è supportata o ICERR \_ BADFORMAT in caso contrario.

## <a name="remarks"></a>Commenti

Quando il driver riceve questo messaggio, deve allocare buffer ed eseguire operazioni che richiedono molto tempo, in modo che sia in grado di elaborare i messaggi di [**\_ decompressione ICM**](icm-decompress.md) in modo efficiente.

Se si desidera che il driver decomprimere i dati direttamente sullo schermo, inviare il messaggio di [**\_ progetto ICM**](icm-draw.md) .

I messaggi di fine decompressione di **MCI \_ \_ Begin** e [**ICM \_ decomprimete \_**](icm-decompress-end.md) non vengono annidati. Se il driver riceve la decompressione **MCI \_ \_ inizia** prima che la decompressione venga interrotta con la **\_ \_ terminazione MCI decomprimere**, deve riavviare la decompressione con nuovi parametri.

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

 

