---
title: Messaggio di ICM_DECOMPRESSEX (VFW. h)
description: Il \_ messaggio ICM DECOMPRESSEX notifica a un driver di compressione video di decomprimere un frame di dati direttamente sullo schermo, decomprimerlo in una DIB a discesa o decomprimere le immagini descritte con i rettangoli di origine e di destinazione.
ms.assetid: ed253280-c246-4e86-91f1-ad1e1132d732
keywords:
- ICM_DECOMPRESSEX messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d33451547bc598250a97e73682712e157aa13a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048633"
---
# <a name="icm_decompressex-message"></a>\_Messaggio DECOMPRESSEX ICM

Il messaggio **ICM \_ DECOMPRESSEX** notifica a un driver di compressione video di decomprimere un frame di dati direttamente sullo schermo, decomprimerlo in una DIB a discesa o decomprimere le immagini descritte con i rettangoli di origine e di destinazione.


```C++
ICM_DECOMPRESSEX 
wParam = (DWORD_PTR) (LPVOID) &icdex; 
lParam = sizeof(ICDECOMPRESSEX); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="icdex"></span><span id="ICDEX"></span>*icdex*
</dt> <dd>

Puntatore a una struttura [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) .

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Dimensioni, in byte, di [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce ICERR \_ OK se ha esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

Questo messaggio è simile a [**ICM \_ decomprimete**](icm-decompress.md) , ad eccezione del fatto che usa la struttura [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) per definire le informazioni di decompressione.

Se si desidera che il driver decomprimere i dati direttamente sullo schermo, inviare il messaggio di [**\_ progetto ICM**](icm-draw.md) .

Il driver restituisce un errore se questo messaggio viene ricevuto prima del messaggio di [**\_ \_ inizio DECOMPRESSEX di ICM**](icm-decompressex-begin.md) .

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

 

 





