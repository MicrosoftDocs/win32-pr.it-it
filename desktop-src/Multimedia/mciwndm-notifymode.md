---
title: Messaggio di MCIWNDM_NOTIFYMODE (VFW. h)
description: Il \_ messaggio MCIWNDM NOTIFYMODE notifica alla finestra padre di un'applicazione che la modalità operativa del dispositivo MCI è cambiata.
ms.assetid: 08adfa8b-4d88-4953-acd8-8a4728f9e1b6
keywords:
- MCIWNDM_NOTIFYMODE messaggi multimediali di Windows
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
ms.openlocfilehash: 7fe75048a53023dab67bef4048d6149438ad54d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047830"
---
# <a name="mciwndm_notifymode-message"></a>\_Messaggio MCIWNDM NOTIFYMODE

Il messaggio **MCIWNDM \_ NOTIFYMODE** notifica alla finestra padre di un'applicazione che la modalità operativa del dispositivo MCI è cambiata.


```C++
MCIWNDM_NOTIFYMODE 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) mode; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*HWND*
</dt> <dd>

Handle per la finestra MCIWnd.

</dd> <dt>

<span id="mode"></span><span id="MODE"></span>*modalità*
</dt> <dd>

Intero corrispondente alla modalità MCI.

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile abilitare la notifica delle modifiche alla modalità di un dispositivo MCI specificando lo \_ stile della finestra NOTIFYMODE di MCIWNDF.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



 

 





