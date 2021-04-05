---
title: Messaggio di MCIWNDM_NOTIFYERROR (VFW. h)
description: Il \_ messaggio MCIWNDM NOTIFYERROR notifica alla finestra padre di un'applicazione che si è verificato un errore MCI.
ms.assetid: 0f54886a-77dc-43cc-be46-2d322c75471a
keywords:
- MCIWNDM_NOTIFYERROR messaggi multimediali di Windows
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
ms.openlocfilehash: bbef9180c31091f3bd1a85f23a08990c2f7e7ea0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048235"
---
# <a name="mciwndm_notifyerror-message"></a>\_Messaggio MCIWNDM NOTIFYERROR

Il messaggio **MCIWNDM \_ NOTIFYERROR** notifica alla finestra padre di un'applicazione che si è verificato un errore MCI.


```C++
MCIWNDM_NOTIFYERROR 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) errorCode; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*HWND*
</dt> <dd>

Handle per la finestra MCIWnd.

</dd> <dt>

<span id="errorCode"></span><span id="errorcode"></span><span id="ERRORCODE"></span>*errorCode*
</dt> <dd>

Codice numerico per l'errore MCI.

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile abilitare la notifica di errore MCI specificando lo \_ stile della finestra NOTIFYERROR di MCIWNDF.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



 

 





