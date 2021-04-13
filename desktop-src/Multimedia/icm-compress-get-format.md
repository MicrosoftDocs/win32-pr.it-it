---
title: Messaggio di ICM_COMPRESS_GET_FORMAT (VFW. h)
description: Il \_ messaggio MCI compress \_ get \_ format richiede il formato di output dei dati compressi da un driver di compressione video. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro ICCompressGetFormat.
ms.assetid: ac12d415-bad5-4838-b206-09c8097d3fd9
keywords:
- ICM_COMPRESS_GET_FORMAT messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_COMPRESS_GET_FORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d096ceafa382bdbae5e4efe16975b3518735e773
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478467"
---
# <a name="icm_compress_get_format-message"></a>\_ \_ \_ Messaggio formato COMPRIMI Get formato ICM

Il messaggio **MCI \_ compress \_ get \_ Format** richiede il formato di output dei dati compressi da un driver di compressione video. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICCompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformat) .


```C++
ICM_COMPRESS_GET_FORMAT 
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

Puntatore a una struttura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) per contenere il formato di output. È possibile specificare zero per questo parametro per richiedere solo le dimensioni del formato di output, come nella macro [**ICCompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformatsize) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se *lpbiOutput* è zero, restituisce le dimensioni della struttura.

Se *lpbiOutput* è diverso da zero, restituisce ICERR \_ OK in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

Se *lpbiOutput* è diverso da zero, il driver deve riempire la struttura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) con il formato di output predefinito corrispondente al formato di input specificato per *lpbiInput*. Se il compressore può produrre diversi formati, il formato predefinito dovrebbe essere quello che conserva la maggior quantità di informazioni.

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

 

