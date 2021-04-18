---
title: Messaggio MMIOM_OPEN (mmsystem. h)
description: Il \_ messaggio aperto MMIOM viene inviato a una routine di i/O dalla funzione mmioOpen per richiedere l'apertura o l'eliminazione di un file.
ms.assetid: 02b2cf22-21a3-4f49-b90e-7b44478c0168
keywords:
- MMIOM_OPEN messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MMIOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9ea2b5ddc0c79cb3efe00038a628373ce3665bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302770"
---
# <a name="mmiom_open-message"></a>MMIOM \_ messaggio aperto

Il **messaggio \_ aperto MMIOM** viene inviato a una routine di i/O dalla funzione [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) per richiedere l'apertura o l'eliminazione di un file.


```C++
MMIOM_OPEN 
lParam1 = (LPARAM) lpszFileName 
lParam2 = reserved 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpszFileName"></span><span id="lpszfilename"></span><span id="LPSZFILENAME"></span>*lpszFileName*
</dt> <dd>

Stringa con terminazione null che contiene il nome del file da aprire.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Riservato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce MMSYSERR \_ NOERROR se ha esito positivo o un errore in caso contrario. Di seguito sono riportati i possibili valori di errore:



| Requisito | Valore |
|--------------------|---------------------------------------------|
| \_CANNOTOPEN MMIOM  | Non è stato possibile aprire il file.               |
| \_OutOfMemory MMIOM | Memoria insufficiente per eseguire l'operazione. |



 

## <a name="remarks"></a>Commenti

Il membro **dwFlags** della struttura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) contiene i flag passati alla funzione [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) .

Il membro **lDiskOffset** della struttura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) è inizializzato su zero. Se questo valore non è corretto, è necessario che la procedura di I/O venga corretta.

Se l'applicazione ha passato una struttura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) a [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen), il valore restituito viene restituito nel membro **wErrorRet** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Mmsystem. h (include Windows. h)</dt> </dl> |



 

