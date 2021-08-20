---
title: MMIOM_RENAME messaggio (Mmsystem.h)
description: Il messaggio MMIOM RENAME viene inviato a una procedura di I/O dalla funzione mmioRename per richiedere la ridenominazione \_ del file specificato.
ms.assetid: 38a746c8-3a6f-4cb2-a5b4-c11bd1e73c8a
keywords:
- MMIOM_RENAME messaggio Windows Multimediali
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
ms.openlocfilehash: bcfd90b53f1cc42030bd00e6553d52de0f036ff274b3d4ff942c48667e4347b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065311"
---
# <a name="mmiom_rename-message"></a>Messaggio MMIOM \_ RENAME

Il **messaggio MMIOM \_ RENAME** viene inviato a una procedura di I/O dalla funzione [**mmioRename**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiorename) per richiedere la ridenominazione del file specificato.


```C++
MMIOM_RENAME 
lParam1 = (LPARAM) lpszOldFilename 
lParam2 = (LPARAM) lpszNewFilename 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpszOldFilename"></span><span id="lpszoldfilename"></span><span id="LPSZOLDFILENAME"></span>*lpszOldFilename*
</dt> <dd>

Puntatore a una stringa contenente il nome file del file da rinominare.

</dd> <dt>

<span id="lpszNewFilename"></span><span id="lpsznewfilename"></span><span id="LPSZNEWFILENAME"></span>*lpszNewFilename*
</dt> <dd>

Puntatore a una stringa contenente il nuovo nome file.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il file viene rinominato correttamente, il valore restituito è zero. Se il file specificato non è stato trovato, il valore restituito è MMIOERR \_ FILENOTFOUND.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Mmsystem.h (includere Windows.h)</dt> </dl> |



 

