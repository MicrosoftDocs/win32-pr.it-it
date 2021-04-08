---
title: Messaggio di MCIWNDM_NOTIFYMEDIA (VFW. h)
description: Il \_ messaggio MCIWNDM NOTIFYMEDIA notifica alla finestra padre di un'applicazione che il supporto è stato modificato.
ms.assetid: cc31502d-09a9-4580-9ff8-9c2be51c8e35
keywords:
- MCIWNDM_NOTIFYMEDIA messaggi multimediali di Windows
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
ms.openlocfilehash: 7026bd984e1d79775aac52caad56c87be6e8098e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741151"
---
# <a name="mciwndm_notifymedia-message"></a>\_Messaggio MCIWNDM NOTIFYMEDIA

Il messaggio **MCIWNDM \_ NOTIFYMEDIA** notifica alla finestra padre di un'applicazione che il supporto è stato modificato.


```C++
MCIWNDM_NOTIFYMEDIA 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*HWND*
</dt> <dd>

Handle per la finestra MCIWnd.

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*LP*
</dt> <dd>

Puntatore a una stringa con terminazione null che contiene il nuovo nome file. Se il supporto è in chiusura, specifica una stringa null.

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile abilitare la notifica delle modifiche dei supporti specificando lo \_ stile della finestra NOTIFYMEDIA di MCIWNDF.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



 

 





