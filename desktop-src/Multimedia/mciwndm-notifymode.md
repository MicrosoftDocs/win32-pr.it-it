---
title: MCIWNDM_NOTIFYMODE messaggio (Vfw.h)
description: Il messaggio MCIWNDM NOTIFYMODE notifica alla finestra padre di un'applicazione che la modalità operativa del dispositivo \_ MCI è stata modificata.
ms.assetid: 08adfa8b-4d88-4953-acd8-8a4728f9e1b6
keywords:
- MCIWNDM_NOTIFYMODE messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYMODE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c610904512e2b39a5c0f16781c1d9f27155f7826941aebfc66fcd9259f7ee8a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525421"
---
# <a name="mciwndm_notifymode-message"></a>Messaggio NOTIFYMODE MCIWNDM \_

Il **messaggio MCIWNDM \_ NOTIFYMODE** notifica alla finestra padre di un'applicazione che la modalità operativa del dispositivo MCI è stata modificata.


```C++
MCIWNDM_NOTIFYMODE 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) mode; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*Hwnd*
</dt> <dd>

Handle per la finestra MCIWnd.

</dd> <dt>

<span id="mode"></span><span id="MODE"></span>*Modalità*
</dt> <dd>

Intero corrispondente alla modalità MCI.

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile abilitare la notifica delle modifiche di modalità di un dispositivo MCI specificando lo stile della finestra \_ NOTIFYMODE MCIWNDF.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



 

 





