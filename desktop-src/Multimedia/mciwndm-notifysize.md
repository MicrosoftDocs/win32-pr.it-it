---
title: Messaggio di MCIWNDM_NOTIFYSIZE (VFW. h)
description: Il \_ messaggio MCIWNDM NOTIFYSIZE notifica alla finestra padre di un'applicazione che le dimensioni della finestra sono state modificate.
ms.assetid: 76e1f663-bfc6-4d3c-9486-c8c7f79e4265
keywords:
- MCIWNDM_NOTIFYSIZE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYSIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59db02d69302127937a7203729de9cc8b98a58f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119539"
---
# <a name="mciwndm_notifysize-message"></a>\_Messaggio MCIWNDM NOTIFYSIZE

Il messaggio **MCIWNDM \_ NOTIFYSIZE** notifica alla finestra padre di un'applicazione che le dimensioni della finestra sono state modificate.


```C++
MCIWNDM_NOTIFYSIZE 
wParam = (WPARAM) (HWND) hwnd; 
lParam = 0; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*HWND*
</dt> <dd>

Handle per la finestra MCIWnd.

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile abilitare la notifica delle modifiche apportate alle dimensioni di una finestra MCIWnd specificando lo \_ stile della finestra NOTIFYSIZE MCIWNDF.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



 

 





