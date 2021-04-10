---
title: Messaggio di ICM_COMPRESS_GET_SIZE (VFW. h)
description: Il \_ messaggio MCI compress \_ get \_ size richiede che il driver di compressione video fornisca la dimensione massima di un frame di dati quando viene compresso nel formato di output specificato. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro ICCompressGetSize.
ms.assetid: 6910e588-e60f-43b1-8fa6-113c2ec32a53
keywords:
- ICM_COMPRESS_GET_SIZE messaggi multimediali di Windows
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
ms.openlocfilehash: 38b0b61c78cc684de27d1e9a2747498e30eb3fe9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964726"
---
# <a name="icm_compress_get_size-message"></a>\_ \_ Messaggio dimensioni compressione Get MCI \_

Il messaggio **MCI \_ compress \_ get \_ size** richiede che il driver di compressione video fornisca la dimensione massima di un frame di dati quando viene compresso nel formato di output specificato. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICCompressGetSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) .


```C++
ICM_COMPRESS_GET_SIZE 
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

Restituisce il numero massimo di byte che può essere occupato da un singolo frame compresso.

## <a name="remarks"></a>Commenti

In genere, le applicazioni inviano questo messaggio per determinare la dimensione di un buffer da allocare per il frame compresso.

Il driver deve calcolare la dimensione del frame possibile più grande in base ai formati di input e di output.

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

 

