---
title: MCIWNDM_NOTIFYERROR messaggio (Vfw.h)
description: Il messaggio MCIWNDM NOTIFYERROR notifica alla finestra padre di un'applicazione che \_ si è verificato un errore MCI.
ms.assetid: 0f54886a-77dc-43cc-be46-2d322c75471a
keywords:
- MCIWNDM_NOTIFYERROR messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYERROR
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5dcca10f593c14e1532aa53b59b8c0bb106ea721ad0d09bde742727fddaeb07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118374132"
---
# <a name="mciwndm_notifyerror-message"></a>Messaggio NOTIFYERROR MCIWNDM \_

Il **messaggio MCIWNDM \_ NOTIFYERROR** notifica alla finestra padre di un'applicazione che si è verificato un errore MCI.


```C++
MCIWNDM_NOTIFYERROR 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) errorCode; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*Hwnd*
</dt> <dd>

Handle per la finestra MCIWnd.

</dd> <dt>

<span id="errorCode"></span><span id="errorcode"></span><span id="ERRORCODE"></span>*Errorcode*
</dt> <dd>

Codice numerico per l'errore MCI.

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile abilitare la notifica degli errori MCI specificando lo stile della finestra NOTIFYERROR DI \_ MCIWNDF.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



 

 





