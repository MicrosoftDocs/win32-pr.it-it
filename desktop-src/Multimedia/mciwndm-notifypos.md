---
title: Messaggio di MCIWNDM_NOTIFYPOS (VFW. h)
description: Il \_ messaggio MCIWNDM NOTIFYPOS notifica alla finestra padre di un'applicazione che la posizione della finestra è cambiata.
ms.assetid: ccc8903b-ad79-495a-8003-20e120ad28ff
keywords:
- MCIWNDM_NOTIFYPOS messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYPOS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bebb3a8facd6478c21888cf0cf5ca81e3735ff8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964722"
---
# <a name="mciwndm_notifypos-message"></a>\_Messaggio MCIWNDM NOTIFYPOS

Il messaggio **MCIWNDM \_ NOTIFYPOS** notifica alla finestra padre di un'applicazione che la posizione della finestra è cambiata.


```C++
MCIWNDM_NOTIFYPOS 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) pos; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*HWND*
</dt> <dd>

Handle per la finestra MCIWnd.

</dd> <dt>

<span id="pos"></span><span id="POS"></span>*POS*
</dt> <dd>

Descrive la nuova posizione.

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile abilitare la notifica delle modifiche nella posizione di una finestra MCIWnd specificando lo \_ stile della finestra NOTIFYPOS MCIWNDF.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



 

 





