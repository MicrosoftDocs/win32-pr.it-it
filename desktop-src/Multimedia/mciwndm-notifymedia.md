---
title: MCIWNDM_NOTIFYMEDIA messaggio (Vfw.h)
description: Il messaggio MCIWNDM NOTIFYMEDIA notifica alla \_ finestra padre di un'applicazione che il supporto è stato modificato.
ms.assetid: cc31502d-09a9-4580-9ff8-9c2be51c8e35
keywords:
- MCIWNDM_NOTIFYMEDIA messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYMEDIA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa64b17fb3910e518e5b5d4318f8d988cf71f8c314f047a5f2eed1ff80cc843d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783022"
---
# <a name="mciwndm_notifymedia-message"></a>Messaggio NOTIFYMEDIA MCIWNDM \_

Il **messaggio MCIWNDM \_ NOTIFYMEDIA** notifica alla finestra padre di un'applicazione che il supporto è stato modificato.


```C++
MCIWNDM_NOTIFYMEDIA 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*Hwnd*
</dt> <dd>

Handle per la finestra MCIWnd.

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*Lp*
</dt> <dd>

Puntatore a una stringa con terminazione Null contenente il nuovo nome file. Se il supporto è in chiusura, specifica una stringa Null.

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile abilitare la notifica delle modifiche ai supporti specificando lo stile della finestra \_ NOTIFYMEDIA MCIWNDF.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



 

 





