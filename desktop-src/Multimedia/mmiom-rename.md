---
title: Messaggio MMIOM_RENAME (mmsystem. h)
description: Il \_ messaggio MMIOM Rename viene inviato a una routine di i/O dalla funzione mmioRename per richiedere che il file specificato venga rinominato.
ms.assetid: 38a746c8-3a6f-4cb2-a5b4-c11bd1e73c8a
keywords:
- MMIOM_RENAME messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MMIOM_RENAME
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b71770dec6a92693a50e8e0210da3f9b8028587c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478455"
---
# <a name="mmiom_rename-message"></a>MMIOM \_ Rinomina messaggio

Il messaggio **MMIOM \_ Rename** viene inviato a una routine di i/O dalla funzione [**mmioRename**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiorename) per richiedere che il file specificato venga rinominato.


```C++
MMIOM_RENAME 
lParam1 = (LPARAM) lpszOldFilename 
lParam2 = (LPARAM) lpszNewFilename 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpszOldFilename"></span><span id="lpszoldfilename"></span><span id="LPSZOLDFILENAME"></span>*lpszOldFilename*
</dt> <dd>

Puntatore a una stringa contenente il nome del file da rinominare.

</dd> <dt>

<span id="lpszNewFilename"></span><span id="lpsznewfilename"></span><span id="LPSZNEWFILENAME"></span>*lpszNewFilename*
</dt> <dd>

Puntatore a una stringa che contiene il nuovo nome file.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il file viene rinominato correttamente, il valore restituito è zero. Se il file specificato non è stato trovato, il valore restituito è MMIOERR \_ FileNotFound.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Mmsystem. h (include Windows. h)</dt> </dl> |



 

