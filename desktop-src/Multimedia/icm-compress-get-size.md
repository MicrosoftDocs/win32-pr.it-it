---
title: ICM_COMPRESS_GET_SIZE messaggio (Vfw.h)
description: Il ICM messaggio COMPRESS GET SIZE richiede al driver di compressione video di specificare le dimensioni massime di un frame di dati quando vengono compressi \_ nel formato di output \_ \_ specificato. È possibile inviare questo messaggio in modo esplicito o tramite la macro ICCompressGetSize.
ms.assetid: 6910e588-e60f-43b1-8fa6-113c2ec32a53
keywords:
- ICM_COMPRESS_GET_SIZE messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- ICM_COMPRESS_GET_SIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ac84919b81eda747263877a79e8ce6fe6ab3bdfc50d37e77ce2026288fbe321
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117988174"
---
# <a name="icm_compress_get_size-message"></a>\_ICM MESSAGGIO COMPRESS \_ GET \_ SIZE

Il **ICM \_ messaggio COMPRESS GET \_ \_ SIZE** richiede al driver di compressione video di specificare le dimensioni massime di un frame di dati quando vengono compressi nel formato di output specificato. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**ICCompressGetSize.**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize)


```C++
ICM_COMPRESS_GET_SIZE 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*
</dt> <dd>

Puntatore a una [**struttura BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) contenente il formato di input.

</dd> <dt>

<span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*
</dt> <dd>

Puntatore a una [**struttura BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) contenente il formato di output.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il numero massimo di byte che un singolo frame compresso può occupare.

## <a name="remarks"></a>Commenti

In genere, le applicazioni inviano questo messaggio per determinare le dimensioni di un buffer da allocare per il frame compresso.

Il driver deve calcolare le dimensioni del frame più grande possibile in base ai formati di input e output.

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

 

