---
title: ICM_DECOMPRESS_BEGIN messaggio (Vfw.h)
description: Il ICM \_ MESSAGGIO DECOMPRESS BEGIN notifica a un driver di decompressione video di prepararsi per \_ la decompressione dei dati. È possibile inviare questo messaggio in modo esplicito o tramite la macro ICDecompressBegin.
ms.assetid: 24cd5220-d473-4968-8678-b00670eecf8f
keywords:
- ICM_DECOMPRESS_BEGIN messaggio Windows Multimediali
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
ms.openlocfilehash: f1d26a0ea99f089d558da639dfad99d4551237b180e595912973e0d22f634f5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678351"
---
# <a name="icm_decompress_begin-message"></a>\_ICM MESSAGGIO DECOMPRESS \_ BEGIN

Il **ICM \_ MESSAGGIO DECOMPRESS \_ BEGIN** notifica a un driver di decompressione video di prepararsi per la decompressione dei dati. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**ICDecompressBegin.**](/windows/desktop/api/Vfw/nf-vfw-icdecompressbegin)


```C++
ICM_DECOMPRESS_BEGIN 
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

Restituisce ICERR \_ OK se la decompressione specificata è supportata o ICERR BADFORMAT in \_ caso contrario.

## <a name="remarks"></a>Commenti

Quando il driver riceve questo messaggio, deve allocare buffer ed eseguire qualsiasi operazione dispendiosa in termini di tempo in modo che possa elaborare ICM [**\_ messaggi DECOMPRESS**](icm-decompress.md) in modo efficiente.

Se si vuole che il driver decomprime i dati direttamente sullo schermo, inviare il messaggio [**ICM \_ DRAW.**](icm-draw.md)

I **ICM \_ DECOMPRESS \_ BEGIN** [**e ICM \_ DECOMPRESS \_ END**](icm-decompress-end.md) non vengono annidato. Se il driver riceve ICM **\_ DECOMPRESS \_ BEGIN** prima che la decompressione venga arrestata con ICM **\_ DECOMPRESS \_ END,** deve riavviare la decompressione con nuovi parametri.

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

 

