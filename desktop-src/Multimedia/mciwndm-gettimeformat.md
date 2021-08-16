---
title: MCIWNDM_GETTIMEFORMAT messaggio (Vfw.h)
description: Il messaggio MCIWNDM GETTIMEFORMAT recupera il formato dell'ora corrente di un dispositivo MCI in due formati come valore \_ numerico e come stringa. È possibile inviare questo messaggio in modo esplicito o tramite la macro MCIWndGetTimeFormat.
ms.assetid: 01844872-5444-4f3b-92a3-64f80b94d3a0
keywords:
- MCIWNDM_GETTIMEFORMAT messaggio Windows Multimediali
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
ms.openlocfilehash: 3badb7c7722db6444d3bd928535790876e0a128e69e50323cea3fe39c2dd987a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117985909"
---
# <a name="mciwndm_gettimeformat-message"></a>Messaggio MCIWNDM \_ GETTIMEFORMAT

Il **messaggio MCIWNDM \_ GETTIMEFORMAT** recupera il formato dell'ora corrente di un dispositivo MCI in due formati: come valore numerico e come stringa. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**MCIWndGetTimeFormat.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat)


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

<span id="lp"></span><span id="LP"></span>*Lp*
</dt> <dd>

Puntatore a un buffer per contenere il formato stringa con terminazione Null del formato dell'ora.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un intero corrispondente alla costante MCI che definisce il formato dell'ora.

## <a name="remarks"></a>Commenti

Se la stringa di formato dell'ora è più lunga del buffer restituito, MCIWnd tronca la stringa.

Un dispositivo MCI può supportare uno o più dei formati di ora seguenti.



| Formato ora                      | Costante MCI               |
|----------------------------------|----------------------------|
| Byte                            | BYTE IN FORMATO MCI \_ \_         |
| Fotogrammi                           | FRAME IN FORMATO MCI \_ \_        |
| Ore, minuti, secondi          | FORMATO MCI \_ \_ HMS           |
| Millisecondi                     | MILLISECONDI \_ DI FORMATO \_ MCI  |
| Minuti, secondi, fotogrammi         | FORMATO MCI \_ \_ MSF           |
| Esempi                          | ESEMPI DI FORMATO MCI \_ \_       |
| SMPTE 24                         | FORMATO MCI \_ \_ SMPTE \_ 24     |
| SMPTE 25                         | FORMATO MCI \_ \_ SMPTE \_ 25     |
| Eliminazione di SMPTE 30                    | FORMATO MCI \_ \_ SMPTE \_ 30DROP |
| SMPTE 30 (senza eliminazione)              | FORMATO MCI \_ \_ SMPTE \_ 30     |
| Tracce, minuti, secondi, fotogrammi | FORMATO MCI \_ \_ TMSF          |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat)
</dt> </dl>

 

 





