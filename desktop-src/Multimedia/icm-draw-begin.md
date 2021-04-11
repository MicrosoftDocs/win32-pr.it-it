---
title: Messaggio di ICM_DRAW_BEGIN (VFW. h)
description: Il \_ \_ messaggio inizio progetto ICM notifica a un driver di rendering di prepararsi a creare dati.
ms.assetid: e5ecd7dd-376b-422c-bbb8-4e7c41e3cac8
keywords:
- ICM_DRAW_BEGIN messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DRAW_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db7b9e20a0b0621038e1c7e092a871a6727566cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964723"
---
# <a name="icm_draw_begin-message"></a>\_ \_ Messaggio inizio estrazione ICM

Il **messaggio \_ \_ inizio progetto ICM** notifica a un driver di rendering di prepararsi a creare dati.


```C++
ICM_DRAW_BEGIN 
wParam = (DWORD) (LPVOID) &icdrwBgn; 
lParam = sizeof(ICDRAW); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="icdrwBgn"></span><span id="icdrwbgn"></span><span id="ICDRWBGN"></span>*icdrwBgn*
</dt> <dd>

Puntatore a una struttura [**ICDRAWBEGIN**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin) contenente il formato di input.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Dimensioni, in byte, di **ICDRAWBEGIN**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce ICERR \_ OK se il driver supporta il disegno dei dati sullo schermo con la modalità e il formato specificati oppure un codice di errore. I possibili valori di errore includono i seguenti.



| Valore               | Significato                                                                       |
|---------------------|-------------------------------------------------------------------------------|
| \_BADFORMAT ICERR    | Il formato di input o output non è supportato.                                      |
| \_NotSupported ICERR | Il driver non viene disegnato direttamente sullo schermo o non supporta questo messaggio. |



 

## <a name="remarks"></a>Commenti

Se si desidera che il driver decomprimere i dati in un buffer, inviare il messaggio di [**\_ \_ inizio di decompressione ICM**](icm-decompress-begin.md) .

I messaggi di **\_ \_ inizio** e [**di \_ \_ fine progetto**](icm-draw-end.md) ICM non nidificano. Se il driver riceve **l' \_ \_ inizio dell'estrazione ICM** prima che la decompressione venga arrestata con la **\_ \_ fine del progetto ICM**, dovrebbe riavviare la decompressione con nuovi parametri.

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

 

 





