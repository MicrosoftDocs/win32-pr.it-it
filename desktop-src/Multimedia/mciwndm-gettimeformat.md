---
title: Messaggio di MCIWNDM_GETTIMEFORMAT (VFW. h)
description: Il \_ messaggio MCIWNDM GETTIMEFORMAT Recupera il formato dell'ora corrente di un dispositivo MCI in due formati come valore numerico e come stringa. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndGetTimeFormat.
ms.assetid: 01844872-5444-4f3b-92a3-64f80b94d3a0
keywords:
- MCIWNDM_GETTIMEFORMAT messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_GETTIMEFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a09f969c009ff23bc0951ed2efbc0dbf7aa95dda
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740239"
---
# <a name="mciwndm_gettimeformat-message"></a>\_Messaggio MCIWNDM GETTIMEFORMAT

Il messaggio **MCIWNDM \_ GETTIMEFORMAT** Recupera il formato dell'ora corrente di un dispositivo MCI in due formati: come valore numerico e come stringa. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) .


```C++
MCIWNDM_GETTIMEFORMAT 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="len"></span><span id="LEN"></span>*Len*
</dt> <dd>

Dimensione, in byte, del buffer.

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*LP*
</dt> <dd>

Puntatore a un buffer per contenere il formato stringa a terminazione null del formato ora.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un Integer che corrisponde alla costante MCI che definisce il formato dell'ora.

## <a name="remarks"></a>Commenti

Se la stringa di formato dell'ora è più lunga del buffer restituito, MCIWnd tronca la stringa.

Un dispositivo MCI può supportare uno o più dei seguenti formati di ora.



| Formato ora                      | Costante MCI               |
|----------------------------------|----------------------------|
| Byte                            | \_byte in formato MCI \_         |
| Frame                           | \_frame di formato MCI \_        |
| Ore, minuti, secondi          | \_formato MCI \_ HMS           |
| Millisecondi                     | \_ \_ millisecondi formato MCI  |
| Minuti, secondi, fotogrammi         | \_MSF formato \_ MCI           |
| Esempi                          | \_esempi di formato MCI \_       |
| SMPTE 24                         | \_Formato MCI \_ \_ 24     |
| SMPTE 25                         | \_Formato MCI \_ \_ 25     |
| Rilascio SMPTE 30                    | \_Formato MCI \_ \_ 30DROP |
| SMPTE 30 (non-drop)              | \_Formato MCI \_ \_ 30     |
| Tracce, minuti, secondi, frame | \_formato MCI \_ TMSF          |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat)
</dt> </dl>

 

 





