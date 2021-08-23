---
title: MMIOM_SEEK messaggio (Mmsystem.h)
description: Il messaggio MMIOM SEEK viene inviato a una procedura di I/O dalla funzione mmioSeek per richiedere lo spostamento della posizione \_ corrente del file.
ms.assetid: 428b231a-6e00-4458-9ba2-e9b0b028843a
keywords:
- MMIOM_SEEK di messaggi Windows multimediali
topic_type:
- apiref
api_name:
- MMIOM_SEEK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ea33db15de3a4617561c437f2d5086afbf4bff2155e657677b171b1413b1c96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065301"
---
# <a name="mmiom_seek-message"></a>Messaggio MMIOM \_ SEEK

Il **messaggio MMIOM \_ SEEK** viene inviato a una procedura di I/O dalla funzione [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) per richiedere lo spostamento della posizione corrente del file.


```C++
MMIOM_SEEK 
lParam1 = (LPARAM) lNewFilePos 
lParam2 = (LPARAM) lChangeFlag 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lNewFilePos"></span><span id="lnewfilepos"></span><span id="LNEWFILEPOS"></span>*lNewFilePos*
</dt> <dd>

Nuova posizione del file. Il significato di questo valore dipende dal flag specificato in **lChangeFlag**.

</dd> <dt>

<span id="lChangeFlag"></span><span id="lchangeflag"></span><span id="LCHANGEFLAG"></span>*lChangeFlag*
</dt> <dd>

Flag che specifica la modalità di modifica della posizione del file. Vengono definiti i valori seguenti:



| Requisito | Valore |
|-----------|------------------------------------------------------------------------------------------------------------------------|
| SEEK \_ CUR | Spostare la posizione del file in *byte lNewFilePos* dalla posizione corrente. *lNewFilePos* può essere positivo o negativo. |
| SEEK \_ END | Spostare la posizione del file in *byte lNewFilePos* dalla fine del file.                                             |
| SEEK \_ SET | Spostare la posizione del file in *byte lNewFilePos* dall'inizio del file.                                       |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la nuova posizione del file. Se si verifica un errore, il valore restituito è 1.

## <a name="remarks"></a>Commenti

La procedura di I/O è responsabile della gestione della posizione del file corrente nel membro **lDiskOffset** della [**struttura MMIOINFO.**](/previous-versions//dd757322(v=vs.85))

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Mmsystem.h (includere Windows.h)</dt> </dl> |



 

