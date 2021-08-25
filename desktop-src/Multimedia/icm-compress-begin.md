---
title: ICM_COMPRESS_BEGIN messaggio (Vfw.h)
description: Il ICM \_ COMPRESS \_ BEGIN invia una notifica a un driver di compressione video per preparare la compressione dei dati. È possibile inviare questo messaggio in modo esplicito o tramite la macro ICCompressBegin.
ms.assetid: dd1d3a66-c625-4f55-b65a-8545c1c16301
keywords:
- ICM_COMPRESS_BEGIN di messaggi Windows multimediali
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
ms.openlocfilehash: 33a6ee9c080e2dfc7a779abd4ae2a788bbe136ddcab1ef529714639065553ad0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140949"
---
# <a name="icm_compress_begin-message"></a>\_ICM Messaggio COMPRESS \_ BEGIN

Il ICM COMPRESS BEGIN invia **\_ \_ una** notifica a un driver di compressione video per preparare la compressione dei dati. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**ICCompressBegin.**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin)


```C++
ICM_COMPRESS_BEGIN 
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

Restituisce ICERR OK se il driver supporta la compressione specificata \_ o ICERR BADFORMAT se il formato di input o output non è \_ supportato.

## <a name="remarks"></a>Commenti

Il driver deve allocare e inizializzare le tabelle o la memoria necessarie per comprimere i formati di dati quando riceve il messaggio compresso ICM [**\_ compresso.**](icm-compress.md)

VCM salva le impostazioni della versione più recente **del ICM \_ COMPRESS \_ BEGIN.** I **ICM \_ COMPRESS \_ BEGIN** e ICM [**COMPRESS \_ \_ END**](icm-compress-end.md) non vengono annidato. Se il driver riceve una **ICM \_ COMPRESS \_ BEGIN** prima che la compressione venga arrestata ICM **COMPRESS \_ \_ END**, deve riavviare la compressione con nuovi parametri.

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

 

