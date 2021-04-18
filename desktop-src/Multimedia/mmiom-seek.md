---
title: Messaggio MMIOM_SEEK (mmsystem. h)
description: Il \_ messaggio MMIOM Seek viene inviato a una routine di i/O dalla funzione mmioSeek per richiedere che la posizione corrente del file venga spostata.
ms.assetid: 428b231a-6e00-4458-9ba2-e9b0b028843a
keywords:
- MMIOM_SEEK messaggi multimediali di Windows
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
ms.openlocfilehash: 4855ec4e610f1456e1bf26ee05800e31933f05fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302504"
---
# <a name="mmiom_seek-message"></a>\_Messaggio MMIOM seek

Il messaggio **MMIOM \_ Seek** viene inviato a una routine di i/O dalla funzione [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) per richiedere che la posizione corrente del file venga spostata.


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
| Cerca \_ cur | Spostare la posizione del file in *lNewFilePos* byte dalla posizione corrente. *lNewFilePos* può essere positivo o negativo. |
| \_fine ricerca | Spostare la posizione del file in *lNewFilePos* byte dalla fine del file.                                             |
| SET di ricerca \_ | Spostare la posizione del file in *lNewFilePos* i byte dall'inizio del file.                                       |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la nuova posizione del file. Se si verifica un errore, il valore restituito è 1.

## <a name="remarks"></a>Commenti

La procedura di I/O è responsabile della gestione della posizione corrente del file nel membro **lDiskOffset** della struttura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Mmsystem. h (include Windows. h)</dt> </dl> |



 

