---
title: MCIWNDM_SENDSTRING messaggio (Vfw.h)
description: Il messaggio SENDSTRING MCIWNDM invia un comando MCI in formato stringa al dispositivo \_ associato alla finestra MCIWnd. È possibile inviare questo messaggio in modo esplicito o tramite la macro MCIWndSendString.
ms.assetid: 0e999a0e-588d-4f06-a1bc-fd3f245d8980
keywords:
- MCIWNDM_SENDSTRING messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- MCIWNDM_SENDSTRING
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b98ee008346821c2d489b19d01bb372c37cd3d541380fd8dae3b72bf613051f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037931"
---
# <a name="mciwndm_sendstring-message"></a>Messaggio SENDSTRING MCIWNDM \_

Il **messaggio \_ SENDSTRING MCIWNDM** invia un comando MCI in formato stringa al dispositivo associato alla finestra MCIWnd. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**MCIWndSendString.**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring)


```C++
MCIWNDM_SENDSTRING 
wParam = 0; 
lParam = (LPARAM) (LPSTR) sz; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="sz"></span><span id="SZ"></span>*Sz*
</dt> <dd>

Comando stringa da inviare al dispositivo MCI.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

Il gestore di messaggi **per MCIWNDM \_ SENDSTRING** aggiunge un alias di dispositivo al comando MCI inviato al dispositivo. Pertanto, è consigliabile non utilizzare alcun alias in un comando MCI che si invia con **MCIWNDM \_ SENDSTRING**.

Per ottenere la stringa restituita, che contiene il risultato del comando, inviare il [**messaggio MCIWNDM \_ RETURNSTRING.**](mciwndm-returnstring.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring)
</dt> <dt>

[Stringhe di comando multimediali](multimedia-command-strings.md)
</dt> </dl>

 

 





