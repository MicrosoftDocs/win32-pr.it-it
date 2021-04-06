---
title: Messaggio di MCIWNDM_SENDSTRING (VFW. h)
description: Il \_ messaggio MCIWNDM SENDSTRING Invia un comando MCI in formato stringa al dispositivo associato alla finestra MCIWnd. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndSendString.
ms.assetid: 0e999a0e-588d-4f06-a1bc-fd3f245d8980
keywords:
- MCIWNDM_SENDSTRING messaggi multimediali di Windows
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
ms.openlocfilehash: d36a034a3459803b1652bafed4eb389866add211
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742487"
---
# <a name="mciwndm_sendstring-message"></a>\_Messaggio MCIWNDM SENDSTRING

Il messaggio **MCIWNDM \_ SENDSTRING** Invia un comando MCI in formato stringa al dispositivo associato alla finestra MCIWnd. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) .


```C++
MCIWNDM_SENDSTRING 
wParam = 0; 
lParam = (LPARAM) (LPSTR) sz; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="sz"></span><span id="SZ"></span>*SZ*
</dt> <dd>

Comando stringa da inviare al dispositivo MCI.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

Il gestore di messaggi per **MCIWNDM \_ SENDSTRING** Accoda un alias del dispositivo al comando MCI inviato al dispositivo. Pertanto, non usare alcun alias in un comando MCI emesso con **MCIWNDM \_ SENDSTRING**.

Per ottenere la stringa restituita, che contiene il risultato del comando, inviare il messaggio [**MCIWNDM \_ RETURNSTRING**](mciwndm-returnstring.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring)
</dt> <dt>

[Stringhe di comando multimediali](multimedia-command-strings.md)
</dt> </dl>

 

 





