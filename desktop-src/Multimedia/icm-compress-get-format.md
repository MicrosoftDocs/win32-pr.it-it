---
title: ICM_COMPRESS_GET_FORMAT messaggio (Vfw.h)
description: Il ICM COMPRESS GET FORMAT richiede il formato di output dei \_ \_ dati \_ compressi da un driver di compressione video. È possibile inviare questo messaggio in modo esplicito o tramite la macro ICCompressGetFormat.
ms.assetid: ac12d415-bad5-4838-b206-09c8097d3fd9
keywords:
- ICM_COMPRESS_GET_FORMAT messaggio Windows Multimediali
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
ms.openlocfilehash: 7ac1bf9b3c9a3ae0535da008786bf8baef19c8b51e27446b84e4b95805a1c4a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785031"
---
# <a name="icm_compress_get_format-message"></a>\_ICM Messaggio COMPRESS \_ GET \_ FORMAT

Il **ICM \_ COMPRESS GET \_ \_ FORMAT** richiede il formato di output dei dati compressi da un driver di compressione video. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**ICCompressGetFormat.**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformat)


```C++
ICM_COMPRESS_GET_FORMAT 
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

Puntatore a una [**struttura BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) per contenere il formato di output. È possibile specificare zero per questo parametro per richiedere solo le dimensioni del formato di output, come nella macro [**ICCompressGetFormatSize.**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformatsize)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se *lpbiOutput* è zero, restituisce le dimensioni della struttura .

Se *lpbiOutput* è diverso da zero, restituisce ICERR OK in caso di esito \_ positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

Se *lpbiOutput* è diverso da zero, il driver deve riempire la struttura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) con il formato di output predefinito corrispondente al formato di input specificato per *lpbiInput*. Se il compressore può produrre diversi formati, il formato predefinito deve essere quello che mantiene la maggior quantità di informazioni.

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

 

